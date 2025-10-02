# Actividades de Python

## 🐍 Introducción a Python

Python es un lenguaje de programación de alto nivel, interpretado y de propósito general. Es conocido por su sintaxis clara y legible, lo que lo hace ideal para principiantes.

## 📝 Nivel Básico

### Actividad 1: Hola Mundo y Variables
**Objetivo**: Crear tu primer programa y entender variables básicas.

```python
# Tu primer programa
print("¡Hola Mundo!")

# Variables
nombre = "Juan"
edad = 25
altura = 1.75
es_estudiante = True

print(f"Me llamo {nombre}, tengo {edad} años")
```

**Ejercicio**: 
- Crea variables con tu nombre, edad y ciudad
- Imprime una presentación personal usando estas variables

### Actividad 2: Operaciones Matemáticas
**Objetivo**: Realizar cálculos básicos.

```python
# Operaciones básicas
suma = 10 + 5
resta = 10 - 5
multiplicacion = 10 * 5
division = 10 / 5
potencia = 2 ** 3
modulo = 10 % 3

print(f"Suma: {suma}")
print(f"División: {division}")
```

**Ejercicio**: 
- Crea una calculadora simple que sume, reste, multiplique y divida dos números
- Calcula el área de un círculo (πr²) dado el radio

### Actividad 3: Tipos de Datos y Conversiones
**Objetivo**: Entender los diferentes tipos de datos.

```python
# Tipos de datos
numero_entero = 42
numero_decimal = 3.14
texto = "Python"
booleano = True

# Conversiones
texto_numero = "100"
numero = int(texto_numero)
texto_de_numero = str(42)

print(type(numero_entero))
print(type(texto))
```

**Ejercicio**: 
- Pide al usuario su edad como texto y conviértela a número
- Calcula en qué año nacieron

### Actividad 4: Condicionales (if, elif, else)
**Objetivo**: Tomar decisiones en tu código.

```python
# Condicionales simples
edad = 18

if edad >= 18:
    print("Eres mayor de edad")
else:
    print("Eres menor de edad")

# Condicionales múltiples
nota = 85

if nota >= 90:
    print("Excelente")
elif nota >= 70:
    print("Bien")
elif nota >= 50:
    print("Aprobado")
else:
    print("Reprobado")
```

**Ejercicio**: 
- Crea un programa que determine si un número es positivo, negativo o cero
- Crea un sistema de calificaciones con letras (A, B, C, D, F)

### Actividad 5: Bucles (for y while)
**Objetivo**: Repetir acciones de manera eficiente.

```python
# Bucle for
for i in range(5):
    print(f"Iteración {i}")

# Bucle sobre lista
frutas = ["manzana", "banana", "naranja"]
for fruta in frutas:
    print(f"Me gusta la {fruta}")

# Bucle while
contador = 0
while contador < 5:
    print(f"Contador: {contador}")
    contador += 1
```

**Ejercicio**: 
- Imprime los números del 1 al 10
- Crea un programa que imprima la tabla de multiplicar de un número
- Suma todos los números del 1 al 100

## 📚 Nivel Intermedio

### Actividad 6: Listas
**Objetivo**: Manejar colecciones de datos.

```python
# Crear y modificar listas
numeros = [1, 2, 3, 4, 5]
nombres = ["Ana", "Luis", "María"]

# Operaciones con listas
numeros.append(6)
numeros.insert(0, 0)
numeros.remove(3)
ultimo = numeros.pop()

print(f"Primer elemento: {numeros[0]}")
print(f"Último elemento: {numeros[-1]}")
print(f"Longitud: {len(numeros)}")
```

**Ejercicio**: 
- Crea una lista de compras y permite agregar/eliminar elementos
- Ordena una lista de números de mayor a menor
- Encuentra el número mayor y menor en una lista

### Actividad 7: Diccionarios
**Objetivo**: Trabajar con pares clave-valor.

```python
# Crear diccionarios
estudiante = {
    "nombre": "Ana",
    "edad": 20,
    "carrera": "Ingeniería",
    "promedio": 8.5
}

# Acceder y modificar
print(estudiante["nombre"])
estudiante["edad"] = 21
estudiante["ciudad"] = "Madrid"

# Iterar sobre diccionario
for clave, valor in estudiante.items():
    print(f"{clave}: {valor}")
```

**Ejercicio**: 
- Crea un diccionario con información de un libro (título, autor, año, páginas)
- Crea un programa de agenda telefónica simple
- Cuenta la frecuencia de palabras en un texto

### Actividad 8: Funciones
**Objetivo**: Organizar código en bloques reutilizables.

```python
# Función simple
def saludar(nombre):
    return f"¡Hola {nombre}!"

# Función con múltiples parámetros
def sumar(a, b):
    return a + b

# Función con valor por defecto
def presentar(nombre, edad=18):
    return f"{nombre} tiene {edad} años"

# Usar las funciones
mensaje = saludar("Carlos")
resultado = sumar(5, 3)
print(presentar("Ana", 25))
```

**Ejercicio**: 
- Crea una función que calcule el área de un rectángulo
- Crea una función que determine si un número es par o impar
- Crea una función que convierta temperatura de Celsius a Fahrenheit

### Actividad 9: Manejo de Archivos
**Objetivo**: Leer y escribir archivos.

```python
# Escribir en un archivo
with open("datos.txt", "w") as archivo:
    archivo.write("Primera línea\n")
    archivo.write("Segunda línea\n")

# Leer un archivo
with open("datos.txt", "r") as archivo:
    contenido = archivo.read()
    print(contenido)

# Leer línea por línea
with open("datos.txt", "r") as archivo:
    for linea in archivo:
        print(linea.strip())
```

**Ejercicio**: 
- Crea un programa que guarde notas en un archivo
- Lee un archivo y cuenta cuántas líneas tiene
- Crea un programa de diario personal que guarde entradas con fecha

### Actividad 10: Manejo de Excepciones
**Objetivo**: Manejar errores de manera elegante.

```python
# Try-except básico
try:
    numero = int(input("Ingresa un número: "))
    resultado = 10 / numero
    print(f"Resultado: {resultado}")
except ValueError:
    print("Error: Debes ingresar un número válido")
except ZeroDivisionError:
    print("Error: No se puede dividir por cero")
finally:
    print("Operación finalizada")
```

**Ejercicio**: 
- Crea una calculadora que maneje errores de entrada
- Lee un archivo con manejo de excepciones por si no existe
- Valida entrada de usuario para una edad (debe ser número entre 0 y 120)

## 🚀 Nivel Avanzado

### Actividad 11: Programación Orientada a Objetos (POO)
**Objetivo**: Crear y usar clases.

```python
# Definir una clase
class Persona:
    def __init__(self, nombre, edad):
        self.nombre = nombre
        self.edad = edad
    
    def saludar(self):
        return f"Hola, soy {self.nombre}"
    
    def cumplir_años(self):
        self.edad += 1

# Usar la clase
persona1 = Persona("Ana", 25)
print(persona1.saludar())
persona1.cumplir_años()
print(f"Ahora tiene {persona1.edad} años")

# Herencia
class Estudiante(Persona):
    def __init__(self, nombre, edad, carrera):
        super().__init__(nombre, edad)
        self.carrera = carrera
    
    def estudiar(self):
        return f"{self.nombre} está estudiando {self.carrera}"
```

**Ejercicio**: 
- Crea una clase `CuentaBancaria` con métodos de depositar y retirar
- Crea una clase `Libro` con atributos y un método para mostrar información
- Crea una jerarquía de clases: `Animal` → `Perro`, `Gato`

### Actividad 12: Comprensiones de Listas
**Objetivo**: Crear listas de manera concisa.

```python
# Comprensión de lista básica
cuadrados = [x**2 for x in range(10)]

# Con condición
pares = [x for x in range(20) if x % 2 == 0]

# Transformación
nombres = ["ana", "luis", "maría"]
mayusculas = [nombre.upper() for nombre in nombres]

# Comprensión de diccionario
numeros = [1, 2, 3, 4, 5]
cuadrados_dict = {x: x**2 for x in numeros}
```

**Ejercicio**: 
- Crea una lista de números divisibles por 3 entre 1 y 50
- Convierte una lista de temperaturas Celsius a Fahrenheit
- Filtra una lista de palabras para obtener solo las que tienen más de 5 letras

### Actividad 13: Módulos y Paquetes
**Objetivo**: Organizar código en módulos.

```python
# Importar módulos estándar
import math
import random
import datetime

# Usar funciones de módulos
print(math.pi)
print(math.sqrt(16))
numero_aleatorio = random.randint(1, 10)
fecha_actual = datetime.datetime.now()

# Importar específico
from math import sqrt, pi
from random import choice

opciones = ["rock", "paper", "scissors"]
eleccion = choice(opciones)
```

**Ejercicio**: 
- Usa el módulo `random` para crear un juego de adivinanza
- Usa `datetime` para crear un programa que muestre cuántos días faltan para tu cumpleaños
- Crea tu propio módulo con funciones matemáticas personalizadas

### Actividad 14: Proyecto - Sistema de Gestión de Tareas
**Objetivo**: Aplicar todos los conceptos aprendidos.

```python
class Tarea:
    def __init__(self, titulo, descripcion):
        self.titulo = titulo
        self.descripcion = descripcion
        self.completada = False
    
    def marcar_completada(self):
        self.completada = True
    
    def __str__(self):
        estado = "✓" if self.completada else "✗"
        return f"[{estado}] {self.titulo}: {self.descripcion}"

class GestorTareas:
    def __init__(self):
        self.tareas = []
    
    def agregar_tarea(self, tarea):
        self.tareas.append(tarea)
    
    def listar_tareas(self):
        for i, tarea in enumerate(self.tareas, 1):
            print(f"{i}. {tarea}")
    
    def completar_tarea(self, indice):
        if 0 <= indice < len(self.tareas):
            self.tareas[indice].marcar_completada()

# Usar el sistema
gestor = GestorTareas()
gestor.agregar_tarea(Tarea("Estudiar Python", "Completar actividades"))
gestor.agregar_tarea(Tarea("Hacer ejercicio", "30 minutos"))
gestor.listar_tareas()
```

**Ejercicio**: 
- Extiende el sistema para guardar tareas en un archivo
- Agrega fechas de vencimiento a las tareas
- Implementa la capacidad de editar y eliminar tareas

### Actividad 15: Proyecto - Juego de Texto
**Objetivo**: Crear un juego interactivo.

**Ejercicio**: 
Crea un juego de aventura de texto que incluya:
- Diferentes habitaciones/locaciones
- Inventario de objetos
- Sistema de puntuación
- Múltiples finales según las decisiones del jugador

## 📖 Recursos Recomendados

- [Python.org - Tutorial Oficial](https://docs.python.org/es/3/tutorial/)
- [Real Python](https://realpython.com/)
- [Python para Todos](https://www.py4e.com/)
- [Automate the Boring Stuff with Python](https://automatetheboringstuff.com/)

## 🎯 Siguientes Pasos

Una vez completadas estas actividades:
1. Construye proyectos personales
2. Contribuye a proyectos open source
3. Explora frameworks como Django (web) o Pandas (datos)
4. Participa en comunidades de Python

¡Sigue practicando y divirtiéndote programando en Python! 🐍
