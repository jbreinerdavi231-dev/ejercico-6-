# ejercico-6-
numero = int(input("Ingrese un número: "))

cantidad = 0
positivos = 0
negativos = 0
pares = 0
impares = 0
suma = 0

mayor = None
menor = None

while numero != 0:

    cantidad = cantidad + 1
    suma = suma + numero

    if numero > 0:
        positivos = positivos + 1
    else:
        negativos = negativos + 1

    if numero % 2 == 0:
        pares = pares + 1
    else:
        impares = impares + 1

    if mayor is None or numero > mayor:
        mayor = numero

    if menor is None or numero < menor:
        menor = numero

    numero = int(input("Ingrese otro número (0 para terminar): "))


if cantidad == 0:
    print("No se ingresaron números.")
else:
    promedio = suma / cantidad

    print("ESTADÍSTICAS ")
    print("Cantidad de números:", cantidad)
    print("Cantidad de positivos:", positivos)
    print("Cantidad de negativos:", negativos)
    print("Cantidad de pares:", pares)
    print("Cantidad de impares:", impares)
    print("Suma total:", suma)
    print("Promedio:", promedio)
    print("Número mayor:", mayor)
    print("Número menor:", menor)
