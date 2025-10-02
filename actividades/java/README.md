# Actividades de Java

## ☕ Introducción a Java

Java es un lenguaje de programación orientado a objetos, robusto y multiplataforma. Es ampliamente utilizado en aplicaciones empresariales, desarrollo Android y sistemas grandes.

## 📝 Nivel Básico

### Actividad 1: Hola Mundo y Estructura Básica
**Objetivo**: Crear tu primer programa Java.

```java
// HolaMundo.java
public class HolaMundo {
    public static void main(String[] args) {
        System.out.println("¡Hola Mundo!");
        System.out.println("Bienvenido a Java");
    }
}
```

Para compilar y ejecutar:
```bash
javac HolaMundo.java
java HolaMundo
```

**Ejercicio**: 
- Crea un programa que imprima tu nombre y edad
- Modifica el programa para imprimir varias líneas
- Usa `System.out.print()` vs `System.out.println()` y observa la diferencia

### Actividad 2: Variables y Tipos de Datos
**Objetivo**: Entender los tipos de datos primitivos.

```java
public class TiposDatos {
    public static void main(String[] args) {
        // Tipos enteros
        byte edad = 25;           // -128 a 127
        short año = 2024;         // -32768 a 32767
        int poblacion = 1000000;  // -2^31 a 2^31-1
        long distancia = 9460730472580800L; // -2^63 a 2^63-1
        
        // Tipos decimales
        float precio = 19.99f;    // 32 bits
        double pi = 3.14159265359; // 64 bits
        
        // Otros tipos
        char inicial = 'A';
        boolean esEstudiante = true;
        
        // String (no es primitivo)
        String nombre = "Juan";
        
        // Imprimir
        System.out.println("Nombre: " + nombre);
        System.out.println("Edad: " + edad);
        System.out.println("Es estudiante: " + esEstudiante);
    }
}
```

**Ejercicio**: 
- Crea variables de cada tipo primitivo
- Prueba los límites de cada tipo
- Investiga qué pasa si excedes el límite de un tipo

### Actividad 3: Operadores
**Objetivo**: Realizar operaciones matemáticas y lógicas.

```java
public class Operadores {
    public static void main(String[] args) {
        // Operadores aritméticos
        int a = 10, b = 3;
        System.out.println("Suma: " + (a + b));
        System.out.println("Resta: " + (a - b));
        System.out.println("Multiplicación: " + (a * b));
        System.out.println("División: " + (a / b));        // 3
        System.out.println("Módulo: " + (a % b));          // 1
        
        // División con decimales
        double division = (double) a / b;  // Casting
        System.out.println("División decimal: " + division);
        
        // Operadores de incremento/decremento
        int contador = 5;
        contador++;  // Equivale a: contador = contador + 1
        System.out.println(contador);  // 6
        
        // Operadores de comparación
        System.out.println(a > b);   // true
        System.out.println(a == b);  // false
        System.out.println(a != b);  // true
        
        // Operadores lógicos
        boolean x = true, y = false;
        System.out.println(x && y);  // AND: false
        System.out.println(x || y);  // OR: true
        System.out.println(!x);      // NOT: false
    }
}
```

**Ejercicio**: 
- Crea una calculadora que realice las 4 operaciones básicas
- Calcula el área de un círculo (πr²)
- Convierte temperatura de Celsius a Fahrenheit

### Actividad 4: Entrada de Datos
**Objetivo**: Leer datos del usuario.

```java
import java.util.Scanner;

public class EntradaDatos {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        // Leer diferentes tipos de datos
        System.out.print("Ingresa tu nombre: ");
        String nombre = scanner.nextLine();
        
        System.out.print("Ingresa tu edad: ");
        int edad = scanner.nextInt();
        
        System.out.print("Ingresa tu altura (m): ");
        double altura = scanner.nextDouble();
        
        System.out.println("\n--- Información ---");
        System.out.println("Nombre: " + nombre);
        System.out.println("Edad: " + edad);
        System.out.println("Altura: " + altura + "m");
        
        scanner.close();
    }
}
```

**Ejercicio**: 
- Crea un programa que calcule el IMC (peso / altura²)
- Pide dos números al usuario y muestra su suma y producto
- Crea un conversor de monedas interactivo

### Actividad 5: Condicionales
**Objetivo**: Tomar decisiones en tu código.

```java
import java.util.Scanner;

public class Condicionales {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        // If-else simple
        System.out.print("Ingresa tu edad: ");
        int edad = scanner.nextInt();
        
        if (edad >= 18) {
            System.out.println("Eres mayor de edad");
        } else {
            System.out.println("Eres menor de edad");
        }
        
        // If-else if-else
        System.out.print("Ingresa tu nota (0-100): ");
        int nota = scanner.nextInt();
        
        if (nota >= 90) {
            System.out.println("Calificación: A");
        } else if (nota >= 80) {
            System.out.println("Calificación: B");
        } else if (nota >= 70) {
            System.out.println("Calificación: C");
        } else if (nota >= 60) {
            System.out.println("Calificación: D");
        } else {
            System.out.println("Calificación: F");
        }
        
        // Switch
        System.out.print("Ingresa un día (1-7): ");
        int dia = scanner.nextInt();
        
        switch (dia) {
            case 1:
                System.out.println("Lunes");
                break;
            case 2:
                System.out.println("Martes");
                break;
            case 3:
                System.out.println("Miércoles");
                break;
            case 4:
                System.out.println("Jueves");
                break;
            case 5:
                System.out.println("Viernes");
                break;
            case 6:
            case 7:
                System.out.println("Fin de semana");
                break;
            default:
                System.out.println("Día inválido");
        }
        
        // Operador ternario
        String mensaje = edad >= 18 ? "Mayor" : "Menor";
        System.out.println("Eres: " + mensaje);
        
        scanner.close();
    }
}
```

**Ejercicio**: 
- Determina si un número es positivo, negativo o cero
- Crea un programa que determine si un año es bisiesto
- Implementa una calculadora con menú usando switch

### Actividad 6: Bucles
**Objetivo**: Repetir acciones de manera eficiente.

```java
public class Bucles {
    public static void main(String[] args) {
        // Bucle for
        System.out.println("--- Bucle for ---");
        for (int i = 1; i <= 5; i++) {
            System.out.println("Iteración " + i);
        }
        
        // Bucle while
        System.out.println("\n--- Bucle while ---");
        int contador = 1;
        while (contador <= 5) {
            System.out.println("Contador: " + contador);
            contador++;
        }
        
        // Bucle do-while
        System.out.println("\n--- Bucle do-while ---");
        int num = 1;
        do {
            System.out.println("Número: " + num);
            num++;
        } while (num <= 5);
        
        // For mejorado (para arrays)
        int[] numeros = {10, 20, 30, 40, 50};
        System.out.println("\n--- For mejorado ---");
        for (int numero : numeros) {
            System.out.println(numero);
        }
        
        // Break y continue
        System.out.println("\n--- Break y Continue ---");
        for (int i = 1; i <= 10; i++) {
            if (i == 5) {
                continue;  // Salta la iteración 5
            }
            if (i == 8) {
                break;     // Termina el bucle
            }
            System.out.println(i);
        }
    }
}
```

**Ejercicio**: 
- Imprime la tabla de multiplicar de un número
- Suma todos los números del 1 al 100
- Imprime un patrón de asteriscos en forma de pirámide
- Encuentra números primos entre 1 y 50

## 📚 Nivel Intermedio

### Actividad 7: Arrays (Arreglos)
**Objetivo**: Manejar colecciones de datos.

```java
public class Arrays {
    public static void main(String[] args) {
        // Declaración e inicialización
        int[] numeros = new int[5];
        numeros[0] = 10;
        numeros[1] = 20;
        numeros[2] = 30;
        
        // Inicialización directa
        int[] valores = {1, 2, 3, 4, 5};
        String[] nombres = {"Ana", "Luis", "María"};
        
        // Acceso y modificación
        System.out.println("Primer elemento: " + valores[0]);
        System.out.println("Longitud: " + valores.length);
        valores[2] = 100;
        
        // Recorrer array
        for (int i = 0; i < valores.length; i++) {
            System.out.println("valores[" + i + "] = " + valores[i]);
        }
        
        // For mejorado
        for (String nombre : nombres) {
            System.out.println(nombre);
        }
        
        // Arrays multidimensionales
        int[][] matriz = {
            {1, 2, 3},
            {4, 5, 6},
            {7, 8, 9}
        };
        
        System.out.println("Elemento [1][2]: " + matriz[1][2]); // 6
        
        // Recorrer matriz
        for (int i = 0; i < matriz.length; i++) {
            for (int j = 0; j < matriz[i].length; j++) {
                System.out.print(matriz[i][j] + " ");
            }
            System.out.println();
        }
    }
}
```

**Ejercicio**: 
- Encuentra el mayor y menor elemento en un array
- Calcula el promedio de un array de números
- Invierte un array
- Suma dos matrices

### Actividad 8: Métodos (Funciones)
**Objetivo**: Organizar código en bloques reutilizables.

```java
public class Metodos {
    // Método sin retorno y sin parámetros
    public static void saludar() {
        System.out.println("¡Hola!");
    }
    
    // Método con parámetros
    public static void saludarPersona(String nombre) {
        System.out.println("¡Hola " + nombre + "!");
    }
    
    // Método con retorno
    public static int sumar(int a, int b) {
        return a + b;
    }
    
    // Método con múltiples parámetros
    public static double calcularPromedio(double[] numeros) {
        double suma = 0;
        for (double num : numeros) {
            suma += num;
        }
        return suma / numeros.length;
    }
    
    // Sobrecarga de métodos
    public static int multiplicar(int a, int b) {
        return a * b;
    }
    
    public static double multiplicar(double a, double b) {
        return a * b;
    }
    
    // Método recursivo
    public static int factorial(int n) {
        if (n <= 1) {
            return 1;
        }
        return n * factorial(n - 1);
    }
    
    public static void main(String[] args) {
        saludar();
        saludarPersona("Ana");
        
        int resultado = sumar(5, 3);
        System.out.println("Suma: " + resultado);
        
        double[] notas = {8.5, 9.0, 7.5, 8.0};
        double promedio = calcularPromedio(notas);
        System.out.println("Promedio: " + promedio);
        
        System.out.println("Multiplicar enteros: " + multiplicar(5, 3));
        System.out.println("Multiplicar decimales: " + multiplicar(5.5, 2.0));
        
        System.out.println("Factorial de 5: " + factorial(5));
    }
}
```

**Ejercicio**: 
- Crea un método que determine si un número es primo
- Crea un método que calcule la potencia de un número
- Implementa un método que busque un elemento en un array
- Crea un método recursivo para calcular Fibonacci

### Actividad 9: Strings
**Objetivo**: Manipular cadenas de texto.

```java
public class Cadenas {
    public static void main(String[] args) {
        String texto = "Hola Mundo";
        
        // Métodos básicos
        int longitud = texto.length();
        char primerCaracter = texto.charAt(0);
        String mayusculas = texto.toUpperCase();
        String minusculas = texto.toLowerCase();
        
        System.out.println("Longitud: " + longitud);
        System.out.println("Primer carácter: " + primerCaracter);
        System.out.println("Mayúsculas: " + mayusculas);
        
        // Comparación
        String texto1 = "Java";
        String texto2 = "Java";
        String texto3 = "Python";
        
        System.out.println(texto1.equals(texto2));        // true
        System.out.println(texto1.equalsIgnoreCase("JAVA")); // true
        System.out.println(texto1.compareTo(texto3));     // Negativo
        
        // Búsqueda
        String frase = "Java es un lenguaje de programación";
        boolean contiene = frase.contains("lenguaje");
        int indice = frase.indexOf("lenguaje");
        boolean empieza = frase.startsWith("Java");
        boolean termina = frase.endsWith("programación");
        
        System.out.println("Contiene 'lenguaje': " + contiene);
        System.out.println("Índice de 'lenguaje': " + indice);
        
        // Extracción
        String substring = frase.substring(0, 4);  // "Java"
        System.out.println("Substring: " + substring);
        
        // División
        String[] palabras = frase.split(" ");
        for (String palabra : palabras) {
            System.out.println(palabra);
        }
        
        // Reemplazo
        String reemplazo = frase.replace("Java", "Python");
        System.out.println(reemplazo);
        
        // Eliminar espacios
        String conEspacios = "  Hola  ";
        String sinEspacios = conEspacios.trim();
        System.out.println("'" + sinEspacios + "'");
        
        // Concatenación
        String nombre = "Juan";
        String apellido = "Pérez";
        String nombreCompleto = nombre + " " + apellido;
        String nombreCompleto2 = nombre.concat(" ").concat(apellido);
        
        // StringBuilder (más eficiente para muchas concatenaciones)
        StringBuilder sb = new StringBuilder();
        sb.append("Hola");
        sb.append(" ");
        sb.append("Mundo");
        String resultado = sb.toString();
    }
}
```

**Ejercicio**: 
- Crea un método que invierta una cadena
- Determina si una palabra es palíndromo
- Cuenta cuántas vocales tiene un texto
- Convierte la primera letra de cada palabra a mayúscula

### Actividad 10: Clases y Objetos
**Objetivo**: Introducción a la Programación Orientada a Objetos.

```java
// Persona.java
public class Persona {
    // Atributos (variables de instancia)
    private String nombre;
    private int edad;
    private String ciudad;
    
    // Constructor
    public Persona(String nombre, int edad, String ciudad) {
        this.nombre = nombre;
        this.edad = edad;
        this.ciudad = ciudad;
    }
    
    // Constructor sobrecargado
    public Persona(String nombre) {
        this.nombre = nombre;
        this.edad = 0;
        this.ciudad = "Desconocida";
    }
    
    // Getters
    public String getNombre() {
        return nombre;
    }
    
    public int getEdad() {
        return edad;
    }
    
    // Setters
    public void setEdad(int edad) {
        if (edad >= 0) {
            this.edad = edad;
        }
    }
    
    // Métodos
    public void saludar() {
        System.out.println("Hola, soy " + nombre);
    }
    
    public void cumplirAnios() {
        edad++;
        System.out.println(nombre + " ahora tiene " + edad + " años");
    }
    
    public String obtenerInfo() {
        return "Nombre: " + nombre + ", Edad: " + edad + ", Ciudad: " + ciudad;
    }
}

// Main.java
public class Main {
    public static void main(String[] args) {
        // Crear objetos
        Persona persona1 = new Persona("Ana", 25, "Madrid");
        Persona persona2 = new Persona("Luis", 30, "Barcelona");
        
        // Usar métodos
        persona1.saludar();
        System.out.println(persona1.obtenerInfo());
        
        persona1.cumplirAnios();
        
        // Usar getters y setters
        String nombre = persona1.getNombre();
        persona1.setEdad(26);
    }
}
```

**Ejercicio**: 
- Crea una clase `CuentaBancaria` con métodos depositar, retirar y consultarSaldo
- Crea una clase `Libro` con atributos título, autor, páginas
- Crea una clase `Rectangulo` que calcule área y perímetro

## 🚀 Nivel Avanzado

### Actividad 11: Herencia
**Objetivo**: Reutilizar código mediante herencia.

```java
// Clase base (superclase)
public class Animal {
    protected String nombre;
    protected int edad;
    
    public Animal(String nombre, int edad) {
        this.nombre = nombre;
        this.edad = edad;
    }
    
    public void comer() {
        System.out.println(nombre + " está comiendo");
    }
    
    public void dormir() {
        System.out.println(nombre + " está durmiendo");
    }
}

// Clase derivada (subclase)
public class Perro extends Animal {
    private String raza;
    
    public Perro(String nombre, int edad, String raza) {
        super(nombre, edad);  // Llamar al constructor de la superclase
        this.raza = raza;
    }
    
    public void ladrar() {
        System.out.println(nombre + " está ladrando: ¡Guau guau!");
    }
    
    @Override
    public void comer() {
        System.out.println(nombre + " está comiendo croquetas");
    }
}

public class Gato extends Animal {
    private String color;
    
    public Gato(String nombre, int edad, String color) {
        super(nombre, edad);
        this.color = color;
    }
    
    public void maullar() {
        System.out.println(nombre + " está maullando: ¡Miau!");
    }
}

// Uso
public class Main {
    public static void main(String[] args) {
        Perro perro = new Perro("Max", 3, "Labrador");
        perro.comer();
        perro.dormir();
        perro.ladrar();
        
        Gato gato = new Gato("Luna", 2, "Negro");
        gato.comer();
        gato.maullar();
    }
}
```

**Ejercicio**: 
- Crea una jerarquía: `Vehiculo` → `Coche`, `Moto`
- Crea una jerarquía: `Figura` → `Circulo`, `Rectangulo`, `Triangulo`
- Implementa método `calcularArea()` en cada figura

### Actividad 12: Polimorfismo
**Objetivo**: Usar objetos de diferentes tipos de manera uniforme.

```java
// Polimorfismo
public class Main {
    public static void main(String[] args) {
        // Un array de tipo Animal que contiene diferentes animales
        Animal[] animales = new Animal[3];
        animales[0] = new Perro("Max", 3, "Labrador");
        animales[1] = new Gato("Luna", 2, "Negro");
        animales[2] = new Perro("Rocky", 5, "Bulldog");
        
        // Polimorfismo: cada animal ejecuta su versión de comer()
        for (Animal animal : animales) {
            animal.comer();  // Llamará a la versión correcta
            animal.dormir();
        }
        
        // instanceof para verificar tipo
        for (Animal animal : animales) {
            if (animal instanceof Perro) {
                Perro perro = (Perro) animal;  // Casting
                perro.ladrar();
            } else if (animal instanceof Gato) {
                Gato gato = (Gato) animal;
                gato.maullar();
            }
        }
    }
}
```

**Ejercicio**: 
- Crea un sistema de empleados con diferentes tipos (Gerente, Programador, etc.)
- Cada tipo tiene un método `calcularSalario()` diferente
- Crea un array de empleados y calcula el total de salarios

### Actividad 13: Clases Abstractas e Interfaces
**Objetivo**: Definir contratos para clases.

```java
// Clase abstracta
public abstract class Figura {
    protected String color;
    
    public Figura(String color) {
        this.color = color;
    }
    
    // Método abstracto (debe ser implementado por subclases)
    public abstract double calcularArea();
    public abstract double calcularPerimetro();
    
    // Método concreto
    public void mostrarColor() {
        System.out.println("Color: " + color);
    }
}

public class Circulo extends Figura {
    private double radio;
    
    public Circulo(String color, double radio) {
        super(color);
        this.radio = radio;
    }
    
    @Override
    public double calcularArea() {
        return Math.PI * radio * radio;
    }
    
    @Override
    public double calcularPerimetro() {
        return 2 * Math.PI * radio;
    }
}

// Interface
public interface Dibujable {
    void dibujar();
    void mover(int x, int y);
}

public class Rectangulo extends Figura implements Dibujable {
    private double ancho;
    private double alto;
    
    public Rectangulo(String color, double ancho, double alto) {
        super(color);
        this.ancho = ancho;
        this.alto = alto;
    }
    
    @Override
    public double calcularArea() {
        return ancho * alto;
    }
    
    @Override
    public double calcularPerimetro() {
        return 2 * (ancho + alto);
    }
    
    @Override
    public void dibujar() {
        System.out.println("Dibujando rectángulo");
    }
    
    @Override
    public void mover(int x, int y) {
        System.out.println("Moviendo rectángulo a (" + x + ", " + y + ")");
    }
}
```

**Ejercicio**: 
- Crea una interfaz `Reproducible` para elementos multimedia
- Implementa la interfaz en clases `Audio`, `Video`
- Crea una clase abstracta `Instrumento` con subclases para diferentes instrumentos

### Actividad 14: Collections Framework
**Objetivo**: Usar colecciones de Java.

```java
import java.util.*;

public class Colecciones {
    public static void main(String[] args) {
        // ArrayList - Lista dinámica
        ArrayList<String> nombres = new ArrayList<>();
        nombres.add("Ana");
        nombres.add("Luis");
        nombres.add("María");
        nombres.add("Juan");
        
        System.out.println(nombres.get(0));  // Ana
        nombres.remove("Luis");
        System.out.println("Tamaño: " + nombres.size());
        
        for (String nombre : nombres) {
            System.out.println(nombre);
        }
        
        // HashSet - Conjunto sin duplicados
        HashSet<Integer> numeros = new HashSet<>();
        numeros.add(5);
        numeros.add(10);
        numeros.add(5);  // No se agregará (duplicado)
        System.out.println(numeros);  // [5, 10]
        
        // HashMap - Mapa clave-valor
        HashMap<String, Integer> edades = new HashMap<>();
        edades.put("Ana", 25);
        edades.put("Luis", 30);
        edades.put("María", 28);
        
        System.out.println("Edad de Ana: " + edades.get("Ana"));
        
        // Iterar sobre HashMap
        for (Map.Entry<String, Integer> entry : edades.entrySet()) {
            System.out.println(entry.getKey() + ": " + entry.getValue());
        }
        
        // LinkedList - Lista enlazada
        LinkedList<String> cola = new LinkedList<>();
        cola.add("Primero");
        cola.add("Segundo");
        cola.addFirst("Nuevo primero");
        cola.addLast("Último");
        
        // TreeSet - Conjunto ordenado
        TreeSet<Integer> numerosOrdenados = new TreeSet<>();
        numerosOrdenados.add(5);
        numerosOrdenados.add(1);
        numerosOrdenados.add(10);
        numerosOrdenados.add(3);
        System.out.println(numerosOrdenados);  // [1, 3, 5, 10]
    }
}
```

**Ejercicio**: 
- Crea un sistema de gestión de estudiantes usando HashMap
- Implementa una agenda telefónica con HashMap
- Usa TreeSet para ordenar palabras alfabéticamente

### Actividad 15: Proyecto Final - Sistema de Biblioteca
**Objetivo**: Aplicar todos los conceptos aprendidos.

```java
// Libro.java
public class Libro {
    private String isbn;
    private String titulo;
    private String autor;
    private boolean disponible;
    
    public Libro(String isbn, String titulo, String autor) {
        this.isbn = isbn;
        this.titulo = titulo;
        this.autor = autor;
        this.disponible = true;
    }
    
    // Getters y setters
    public String getIsbn() { return isbn; }
    public String getTitulo() { return titulo; }
    public String getAutor() { return autor; }
    public boolean isDisponible() { return disponible; }
    public void setDisponible(boolean disponible) { this.disponible = disponible; }
    
    @Override
    public String toString() {
        return String.format("ISBN: %s, Título: %s, Autor: %s, Disponible: %s", 
            isbn, titulo, autor, disponible ? "Sí" : "No");
    }
}

// Biblioteca.java
import java.util.*;

public class Biblioteca {
    private HashMap<String, Libro> libros;
    private ArrayList<String> prestamos;
    
    public Biblioteca() {
        libros = new HashMap<>();
        prestamos = new ArrayList<>();
    }
    
    public void agregarLibro(Libro libro) {
        libros.put(libro.getIsbn(), libro);
        System.out.println("Libro agregado: " + libro.getTitulo());
    }
    
    public void prestarLibro(String isbn) {
        Libro libro = libros.get(isbn);
        if (libro == null) {
            System.out.println("Libro no encontrado");
        } else if (!libro.isDisponible()) {
            System.out.println("Libro no disponible");
        } else {
            libro.setDisponible(false);
            prestamos.add(isbn);
            System.out.println("Libro prestado: " + libro.getTitulo());
        }
    }
    
    public void devolverLibro(String isbn) {
        Libro libro = libros.get(isbn);
        if (libro == null) {
            System.out.println("Libro no encontrado");
        } else {
            libro.setDisponible(true);
            prestamos.remove(isbn);
            System.out.println("Libro devuelto: " + libro.getTitulo());
        }
    }
    
    public void listarLibros() {
        System.out.println("\n--- Lista de Libros ---");
        for (Libro libro : libros.values()) {
            System.out.println(libro);
        }
    }
    
    public void buscarPorAutor(String autor) {
        System.out.println("\n--- Libros de " + autor + " ---");
        for (Libro libro : libros.values()) {
            if (libro.getAutor().equalsIgnoreCase(autor)) {
                System.out.println(libro);
            }
        }
    }
}

// Main.java
public class Main {
    public static void main(String[] args) {
        Biblioteca biblioteca = new Biblioteca();
        
        // Agregar libros
        biblioteca.agregarLibro(new Libro("001", "El Quijote", "Cervantes"));
        biblioteca.agregarLibro(new Libro("002", "Cien años de soledad", "García Márquez"));
        biblioteca.agregarLibro(new Libro("003", "1984", "George Orwell"));
        
        // Listar libros
        biblioteca.listarLibros();
        
        // Prestar libro
        biblioteca.prestarLibro("001");
        
        // Listar libros después del préstamo
        biblioteca.listarLibros();
        
        // Devolver libro
        biblioteca.devolverLibro("001");
        
        // Buscar por autor
        biblioteca.buscarPorAutor("Cervantes");
    }
}
```

**Ejercicio**: 
- Añade la funcionalidad de buscar libros por título
- Implementa un sistema de usuarios que puedan tener múltiples préstamos
- Agrega fechas de vencimiento para los préstamos
- Implementa multas por retrasos

## 📖 Recursos Recomendados

- [Oracle Java Tutorials](https://docs.oracle.com/javase/tutorial/)
- [Java Documentation](https://docs.oracle.com/en/java/)
- [Head First Java](http://shop.oreilly.com/product/9780596009205.do)
- [Effective Java](https://www.oreilly.com/library/view/effective-java/9780134686097/)

## 🎯 Siguientes Pasos

Una vez completadas estas actividades:
1. Aprende sobre manejo de excepciones
2. Explora Java 8+ (Streams, Lambda expressions)
3. Aprende Spring Framework para desarrollo web
4. Practica con proyectos personales
5. Estudia patrones de diseño
6. Explora desarrollo Android

¡Sigue practicando y conviértete en un experto en Java! ☕
