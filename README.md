# ============================================
# FASE 5 - EVALUACIÓN FINAL POA
# PROBLEMA 4 - VIDEOTECA DIGITAL
# ============================================

# Matriz con información de películas
videoteca = [

    ["Interestelar", 2014, 9, "Ciencia Ficción"],
    ["Avatar", 2009, 8, "Acción"],
    ["Encanto", 2021, 9, "Animación"],
    ["The Batman", 2022, 8, "Acción"],
    ["Titanic", 1997, 10, "Drama"],
    ["Duna", 2021, 9, "Ciencia Ficción"],
    ["Oppenheimer", 2023, 10, "Drama"]

]

# ============================================
# FUNCIÓN PARA CONTAR TÍTULOS
# ============================================

def contar_titulos(matriz, calificacion_minima, anio_minimo):

    contador = 0

    # Recorrer la matriz
    for titulo in matriz:

        nombre = titulo[0]
        anio = titulo[1]
        calificacion = titulo[2]

        # Verificar condiciones
        if calificacion >= calificacion_minima and anio >= anio_minimo:

            contador += 1

            print("Título que cumple:",
                  nombre)

    return contador

# ============================================
# DATOS DE PRUEBA
# ============================================

umbral_calificacion = 9
anio_limite = 2020

# ============================================
# LLAMADO DE LA FUNCIÓN
# ============================================

resultado = contar_titulos(
    videoteca,
    umbral_calificacion,
    anio_limite
)

# ============================================
# RESULTADO FINAL
# ============================================

print("\nCantidad total de títulos populares y recientes:",
      resultado)
