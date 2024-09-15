# Definición de las ciudades, días de la semana y número de semanas
ciudades = ["Quito", "Guayaquil", "Cuenca"]
dias_semana = ["Lunes", "Martes", "Miércoles", "Jueves", "Viernes", "Sábado", "Domingo"]
semanas = 4

# matriz 3*7*3
# Crear una matriz 3D (Ciudades x Días x Semanas) con temperaturas aleatorias (entre 10°C y 35°C)

arreglo_temperaturas=[
    [# Quito
        [16, 17, 18, 19, 20, 21, 22], # semana 1
        [8, 9, 10, 11, 12, 13, 14], # semana 2
        [10, 12, 14, 16, 18, 20, 22], # semana 3
        [13, 15, 17, 19, 21, 23, 25], # semana 4
    ],
    [# Guayaquil
        [16, 17, 18, 19, 20, 21, 22], # semana 1
        [8, 9, 10, 11, 12, 13, 14], # semana 2
        [10, 12, 14, 16, 18, 20, 22], # semana 3
        [13, 15, 17, 19, 21, 23, 25], # semana 4
    ],
    [# Cuenca
        [16, 17, 18, 19, 20, 21, 22], # semana 1
        [8, 9, 10, 11, 12, 13, 14], # semana 2
        [10, 12, 14, 16, 18, 20, 22], # semana 3
        [13, 15, 17, 19, 21, 23, 25], # semana 4
    ]
]
# Mostrar la matriz de temperaturas
print("Matriz de temperaturas (Ciudades x Días x Semanas):")
for i, ciudad in enumerate(ciudades):
    print(f"\n{ciudad}:")
    for semana in range(semanas):
        print(f"  Semana {semana + 1}: {arreglo_temperaturas[i][semana]}")

# Cálculo del promedio de temperaturas por ciudad y semana
for i, ciudad in enumerate(ciudades):
    print(f"\nPromedios de temperatura para {ciudad}:")
    for semana in range(semanas):
        # Calcular el promedio de temperaturas de la ciudad en la semana
        promedio_semana = sum(arreglo_temperaturas[i][semana]) / len(arreglo_temperaturas[i][semana])
        # Mostrar el resultado
        print(f"  Semana {semana + 1}: {promedio_semana:.2f}°C")
