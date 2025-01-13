# EjemplosMundoReal_POO
Dentro de este directorio, desarrollaremos programas en Python que utilicen los principios de POO. 
# hotel.py
class Habitacion:
    def __init__(self, numero, tipo, precio):
        self.numero = numero
        self.tipo = tipo
        self.precio = precio
        self.ocupada = False

    def ocupar(self):
        self.ocupada = True

    def desocupar(self):
        self.ocupada = False

class Huesped:
    def __init__(self, nombre, apellido, dni):
        self.nombre = nombre
        self.apellido = apellido
        self.dni = dni

class Reserva:
    def __init__(self, huesped, habitacion, fecha_entrada, fecha_salida):
        self.huesped = huesped
        self.habitacion = habitacion
        self.fecha_entrada = fecha_entrada
        self.fecha_salida = fecha_salida

    def realizar_reserva(self):
        if not self.habitacion.ocupada:
            self.habitacion.ocupar()
            print("Reserva realizada exitosamente.")
        else:
            print("La habitación está ocupada.")

# hotel.py
if __name__ == "__main__":
    # Creando objetos
    habitacion1 = Habitacion(101, "Doble", 100)
    huesped1 = Huesped("Juan", "Pérez", "12345678A")
    reserva1 = Reserva(huesped1, habitacion1, "2023-11-01", "2023-11-05")

    # Realizando la reserva
    reserva1.realizar_reserva()
