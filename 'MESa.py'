import time

class ContadorPuntos:
    def __init__(self):
        self.puntos_azul = 0
        self.puntos_rojo = 0

    def agregar_puntos_azul(self, puntos):
        self.puntos_azul += puntos

    def agregar_puntos_rojo(self, puntos):
        self.puntos_rojo += puntos

    def mostrar_puntaje(self):
        print("Puntaje:")
        print(f"Azul: {self.puntos_azul} puntos")
        print(f"Rojo: {self.puntos_rojo} puntos")

# Función para convertir segundos a formato de tiempo (minutos:segundos)
def convertir_tiempo(segundos):
    minutos = segundos // 60
    segundos_restantes = segundos % 60
    return f"{minutos:02}:{segundos_restantes:02}"

# Duración del juego en segundos
DURACION_JUEGO = 300  # 5 minutos

contador = ContadorPuntos()
tiempo_inicio = time.time()
tiempo_actual = time.time()

while tiempo_actual - tiempo_inicio < DURACION_JUEGO:
    tiempo_restante = int(DURACION_JUEGO - (tiempo_actual - tiempo_inicio))
    print(f"\nTiempo restante: {convertir_tiempo(tiempo_restante)}")

    print("\nMenu:")
    print("1. Agregar puntos al equipo azul")
    print("2. Agregar puntos al equipo rojo")
    print("3. Mostrar puntaje")
    print("4. Salir")

    opcion = input("Seleccione una opción: ")

    if opcion == "1":
        puntos = int(input("Ingrese la cantidad de puntos a agregar al equipo azul (1 o 2): "))
        if puntos in [1, 2]:
            contador.agregar_puntos_azul(puntos)
        else:
            print("Opción inválida. Ingrese 1 o 2.")

    elif opcion == "2":
        puntos = int(input("Ingrese la cantidad de puntos a agregar al equipo rojo (1 o 2): "))
        if puntos in [1, 2]:
            contador.agregar_puntos_rojo(puntos)
        else:
            print("Opción inválida. Ingrese 1 o 2.")

    elif opcion == "3":
        contador.mostrar_puntaje()

    elif opcion == "4":
        break

    else:
        print("Opción inválida. Intente nuevamente.")

    tiempo_actual = time.time()

print("\nTiempo agotado. Fin del juego.")
contador.mostrar_puntaje()
