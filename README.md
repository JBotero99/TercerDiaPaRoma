# Tercer Día Pa Roma
### Indicaciones:
Este repositorio utilizaremos el comando if-elif-else para resolver 8 problemas diferentes
## Problema 1
*Dado un número entero, determinar si ese número corresponde al código ASCII de una vocal minúscula*
```python
n : int
n = int(input("Inserte el código de la vocal en ASCII:"))
if n == 97:
  print('corresponde a la letra "a"')
elif n == 101:
  print('corresponde a la letra "e"')
elif n == 105:
  print('corresponde a la letra "i"')
elif n == 111:
  print('corresponde a la letra "o"')
elif n == 117:
  print('corresponde a la letra "u"')
else:
  print("no corresponde a una vocal")
```
## Problema 2
*Dada una cadena de longitud 1, determine si el código ASCII de primera letra de la cadena es par o no.*
```python
lang = input("Inserte cadena de longitud 1: ")
ascii = ord(lang)
if len(lang) > 1: #Limitamos a un solo caracter en caso tal de que inserten una cadena de longitud mayor a 1.
  print("La cadena no es de longitud 1.")
elif ascii%2 == 0: #para el valor obtenido en código ASCII comprobamos su paridad.
  print("la cadena corresponde a "  + str(ascii) + " en el codigo ASCII y es par")
else:
  print("la cadena corresponde a "  + str(ascii) + " en el codigo ASCII y es impar")
```
## Problema 3
*Dado un carácter, construya un programa en Python para determinar si el carácter es un dígito o no.*
```python
lang = input("inserte un carácter ")
ascii = ord(lang)
if ascii >= 48 and ascii <= 57:
  print(str(lang) + " es un dígito.")
else:
  print(str(lang) + " no es un dígito.")
```
## Problema 4
*Realice un programa que lea dos números reales y determine si el primero es múltiplo del segundo.*
```python
a = float(input("a: "))#float() para convertir el string en un número real.
b = float(input("b: "))
if b % a == 0:
  print(str(a) + " es múltiplo de " + str(b))
else:

  print(str(a) + " no es múltiplo de " + str(b))
```
## Problema 5
*Dado un número real x, construya un programa que permita determinar si el número es positivo, negativo o cero.*
```python
x = float(input('Inserte un número: '))
if x < 0:
  print("El número " + str(x) + " es negativo")
elif x > 0:
  print("El número " + str(x) + " es positivo")
else:
  print("El número " + str(x) + " es el neutro para la suma")
```
## Problema 6
*Dado el centro y el radio de un círculo, determinar si un punto de R2 pertenece o no al interior del círculo.*
```python
#Ubicamos el centro del círculo en un sistema de cordenadas x,y (porque estamos en R2) y su radio
centro_x = float(input("Ingrese coordenada x del centro del círculo: "))
centro_y = float(input("Ingrese coordenada y del centro del círculo: "))
radio = float(input("Ingrese el  radio del círculo: "))
#Coordenadas del punto que queremos saber si está en el círculo
punto_x = float(input("Ingrese coordenada x del punto: "))
punto_y = float(input("Ingrese coordenada y del punto: "))
#Con esos puntos calculamos su distancia respecto al centro y si es menor o igual que el radio, el punto está en el círculo.
distancia = ((punto_x-centro_x)**2 + (punto_y-centro_y**2))**0.5
if distancia < radio:
    print("El punto está dentro del círculo.")
elif distancia == radio:
    print("El punto está dentro del círculo.")
else:
    print("El punto no está dentro del círculo.")
#se podría omitir el elif si a la distancia la ponemos menor o igual al radio pero se pone para usar el comando 🤠🤓
```
## Problema 7
*Dadas tres longitudes positivas, determinar si con esas longitudes se puede construir un triángulo.*
```python
#Para que se pueda formar un triangulo la suma de la longitud de: (Escaleno) su dos lados más pequeños tiene que ser mayor que la del lado más grande, (Isóceles) Una de las patas sumado a la base tiene que ser mayor que la de la otra pata, (Equilatero) dos de sus lados tiene que ser mayor a la del lado restante. Con esta información aunque un poco redundante ya podemos empezar a operar.

print("Inserte la longitud de los lados de mayor a menor")
lado_a = float(input("Inserte el lado de mayor tamaño: "))
lado_b = float(input("Inserte el lado de segundo mayor tamaño: "))
lado_c = float(input("Inserte el lado de menor tamaño: "))
if lado_a<lado_b or lado_a<lado_c or lado_b<lado_c:
    print("Inserte los datos de mayor a menor.")
elif lado_b+lado_c <= lado_a:
    print("No se puede construir un triángulo con esas longitudes.")
else:
    print("Se puede construir un triángulo con esas longitudes.")
```
## Problema 8
*Escriba un programa que reciba el nombre en minúsculas de un país de America y retorne la ciudad capital, si el país no pertenece al continente debe arrojar país no identificado (Utilice match-case).*
```python
lang = input("Escriba en minúsculas el nombre de un país de América (sin acentos): ")

match lang:
    case "canada":
        print("Ottawa")
    case "estados unidos":
        print("Washington D.C.")
    case "mexico":
        print("Ciudad De Mexico")
    case "belice":
        print("Belmopán")
    case "guatemala":
        print("Ciudad de Guatemala")
    case "el salvador":
        print("San Salvador")
    case "nonduras":
        print("Tegucigalpa")
    case "nicaragua":
        print("Managua")
    case "costa rica":
        print("San José")
    case "panama":
        print("Ciudad de panama")
    case "cuba":
        print("La Habana")
    case "jamaica":
        print("Kingston")
    case "haiti":
        print("Puerto Príncipe")
    case "republica dominicana":
        print("Santo Domingo")
    case "bahamas":
        print("Nassau")
    case "antigua y barbuda":
        print("Saint Jhon's")
    case "dominica":
        print("Roseau")
    case "san critobal y nieves":
        print("Basseterre")
    case "santa lucia":
        print("castries")
    case "san vicente y las granadinas":
        print("Kingstown")
    case "granada":
        print("Saint George's")
    case "barbados":
        print("Brigetown")
    case "trinidad y tobagoo":
        print("Puerto España")
    case "Guyana":
        print("Georgetown")
    case "Surinam":
        print("Paramaribo")
    case "colombia":
        print("Bogotá")
    case "venezuela":
        print("Caracas")
    case "ecuador":
        print("Quito")
    case "peru":
        print("Lima")
    case "bolivia":
        print("Sucre")
    case "brasil":
        print("Brasilia")
    case "paraguay":
        print("Asunción")
    case "uruguay":
        print("Montevideo")
    case "chile":
        print("Santiago de Chile")
    case "argentina":
        print("Buenos Aires")
    case _:
        print("País no identificado.")
```
***
## Biblografía
[Clase_7](https://github.com/fegonzalez7/pdc_unal_clase7?tab=readme-ov-file#reto-4)
