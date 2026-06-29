[generador_contr.py](https://github.com/user-attachments/files/29447757/generador_contr.py)
import random

longitud = int(input("Ingrese la longitud de la contraseña: "))

caracteres = ""

mayusculas = input("¿Desea usar mayúsculas? (si/no): ")
if mayusculas == "si":
    caracteres = caracteres + "ABCDEFGHIJKLMNOPQRSTUVWXYZ"

minusculas = input("¿Desea usar minúsculas? (si/no): ")
if minusculas == "si":
    caracteres = caracteres + "abcdefghijklmnopqrstuvwxyz"

numeros = input("¿Desea usar números? (si/no): ")
if numeros == "si":
    caracteres = caracteres + "1234567890"

simbolos = input("¿Desea usar símbolos? (si/no): ")
if simbolos == "si":
    caracteres = caracteres + "@#$%&*"

if caracteres == "":
    print("Debe elegir al menos un tipo de carácter.")
else:
    contraseña = ""

    for i in range(longitud):
        contraseña = contraseña + random.choice(caracteres)

    print("Su contraseña es:", contraseña)

    guardar = input("¿Desea guardar la contraseña? (si/no): ")

    if guardar == "si":
        print("Contraseña guardada")
    else:
        print("Contraseña no guardada")

print("Fin del programa")
