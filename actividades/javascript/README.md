# Actividades de JavaScript

## 🌐 Introducción a JavaScript

JavaScript es el lenguaje de programación de la web. Permite crear páginas interactivas y es esencial para el desarrollo front-end moderno. También se usa en el servidor con Node.js.

## 📝 Nivel Básico

### Actividad 1: Hola Mundo y Variables
**Objetivo**: Crear tu primer script y entender variables básicas.

```javascript
// Tu primer programa
console.log("¡Hola Mundo!");

// Variables con let (valor cambiante)
let nombre = "Juan";
let edad = 25;
let altura = 1.75;

// Constantes con const (valor fijo)
const PI = 3.14159;
const pais = "España";

// Variables antiguas con var (evitar usar)
var ciudad = "Madrid";

console.log(`Me llamo ${nombre}, tengo ${edad} años`);
```

**Ejercicio**: 
- Crea variables con tu información personal (nombre, edad, ciudad)
- Prueba cambiar el valor de una variable `let` y de una `const`
- Imprime una presentación usando template literals

### Actividad 2: Tipos de Datos
**Objetivo**: Conocer los tipos de datos en JavaScript.

```javascript
// Tipos primitivos
let numero = 42;                    // Number
let texto = "JavaScript";            // String
let booleano = true;                // Boolean
let indefinido = undefined;         // Undefined
let nulo = null;                    // Null
let simbolo = Symbol("id");         // Symbol

// Tipos de referencia
let objeto = { nombre: "Ana" };     // Object
let arreglo = [1, 2, 3];           // Array (tipo especial de Object)

// Verificar tipos
console.log(typeof numero);         // "number"
console.log(typeof texto);          // "string"
console.log(Array.isArray(arreglo)); // true
```

**Ejercicio**: 
- Crea variables de cada tipo y verifica su tipo con `typeof`
- Prueba operaciones entre diferentes tipos y observa el resultado
- Investiga la diferencia entre `null` y `undefined`

### Actividad 3: Operadores y Expresiones
**Objetivo**: Realizar operaciones matemáticas y lógicas.

```javascript
// Operadores aritméticos
let suma = 10 + 5;
let resta = 10 - 5;
let multiplicacion = 10 * 5;
let division = 10 / 5;
let modulo = 10 % 3;
let potencia = 2 ** 3;

// Operadores de comparación
console.log(5 == "5");   // true (compara valor)
console.log(5 === "5");  // false (compara valor y tipo)
console.log(10 > 5);     // true
console.log(10 <= 10);   // true

// Operadores lógicos
let and = true && false;  // false
let or = true || false;   // true
let not = !true;          // false
```

**Ejercicio**: 
- Crea una calculadora básica que realice las 4 operaciones
- Practica la diferencia entre `==` y `===`
- Crea expresiones lógicas complejas con AND, OR, NOT

### Actividad 4: Condicionales
**Objetivo**: Tomar decisiones en tu código.

```javascript
// If-else simple
let edad = 18;

if (edad >= 18) {
    console.log("Eres mayor de edad");
} else {
    console.log("Eres menor de edad");
}

// If-else if-else
let nota = 85;

if (nota >= 90) {
    console.log("Excelente");
} else if (nota >= 70) {
    console.log("Bien");
} else if (nota >= 50) {
    console.log("Aprobado");
} else {
    console.log("Reprobado");
}

// Switch
let dia = "lunes";

switch (dia) {
    case "lunes":
        console.log("Inicio de semana");
        break;
    case "viernes":
        console.log("Fin de semana cercano");
        break;
    default:
        console.log("Día normal");
}

// Operador ternario
let resultado = edad >= 18 ? "Mayor" : "Menor";
```

**Ejercicio**: 
- Crea un programa que determine si un año es bisiesto
- Implementa un sistema de menú con switch
- Usa el operador ternario para determinar si un número es par o impar

### Actividad 5: Bucles
**Objetivo**: Repetir acciones de manera eficiente.

```javascript
// Bucle for tradicional
for (let i = 0; i < 5; i++) {
    console.log(`Iteración ${i}`);
}

// Bucle while
let contador = 0;
while (contador < 5) {
    console.log(`Contador: ${contador}`);
    contador++;
}

// Bucle do-while
let num = 0;
do {
    console.log(`Número: ${num}`);
    num++;
} while (num < 3);

// For...of (para arrays)
let frutas = ["manzana", "banana", "naranja"];
for (let fruta of frutas) {
    console.log(fruta);
}

// For...in (para objetos)
let persona = { nombre: "Ana", edad: 25 };
for (let propiedad in persona) {
    console.log(`${propiedad}: ${persona[propiedad]}`);
}
```

**Ejercicio**: 
- Imprime los números del 1 al 10
- Crea la tabla de multiplicar de un número
- Suma todos los números del 1 al 100
- Imprime un patrón de asteriscos en forma de pirámide

## 📚 Nivel Intermedio

### Actividad 6: Arrays (Arreglos)
**Objetivo**: Manejar colecciones de datos.

```javascript
// Crear arrays
let numeros = [1, 2, 3, 4, 5];
let nombres = ["Ana", "Luis", "María"];
let mixto = [1, "dos", true, { id: 1 }];

// Métodos básicos
numeros.push(6);           // Agregar al final
numeros.unshift(0);        // Agregar al inicio
let ultimo = numeros.pop(); // Eliminar del final
let primero = numeros.shift(); // Eliminar del inicio

// Acceso y modificación
console.log(numeros[0]);   // Primer elemento
console.log(numeros[numeros.length - 1]); // Último elemento
numeros[2] = 100;          // Modificar elemento

// Métodos útiles
let longitudNumeros = numeros.length;
let incluye = numeros.includes(3);
let indice = numeros.indexOf(3);
let subarray = numeros.slice(1, 3);
```

**Ejercicio**: 
- Crea una lista de compras y manipúlala con diferentes métodos
- Encuentra el mayor y menor número en un array
- Invierte un array sin usar el método `.reverse()`

### Actividad 7: Métodos de Arrays Avanzados
**Objetivo**: Usar métodos funcionales de arrays.

```javascript
let numeros = [1, 2, 3, 4, 5];

// map - transforma cada elemento
let cuadrados = numeros.map(num => num ** 2);
console.log(cuadrados); // [1, 4, 9, 16, 25]

// filter - filtra elementos
let pares = numeros.filter(num => num % 2 === 0);
console.log(pares); // [2, 4]

// reduce - reduce a un solo valor
let suma = numeros.reduce((acc, num) => acc + num, 0);
console.log(suma); // 15

// find - encuentra el primer elemento que cumple
let mayorQue3 = numeros.find(num => num > 3);
console.log(mayorQue3); // 4

// some - verifica si al menos uno cumple
let hayPares = numeros.some(num => num % 2 === 0);

// every - verifica si todos cumplen
let todosPositivos = numeros.every(num => num > 0);

// forEach - itera sobre cada elemento
numeros.forEach(num => console.log(num * 2));
```

**Ejercicio**: 
- Usa `map` para convertir temperaturas de Celsius a Fahrenheit
- Usa `filter` para obtener palabras con más de 5 letras
- Usa `reduce` para calcular el promedio de un array de números
- Combina varios métodos en una cadena

### Actividad 8: Objetos
**Objetivo**: Trabajar con estructuras de datos complejas.

```javascript
// Crear objetos
let persona = {
    nombre: "Ana",
    edad: 25,
    ciudad: "Madrid",
    activo: true
};

// Acceso a propiedades
console.log(persona.nombre);      // Notación de punto
console.log(persona["edad"]);     // Notación de corchetes

// Modificar propiedades
persona.edad = 26;
persona["ciudad"] = "Barcelona";

// Agregar propiedades
persona.profesion = "Ingeniera";

// Eliminar propiedades
delete persona.activo;

// Métodos en objetos
let calculadora = {
    sumar: function(a, b) {
        return a + b;
    },
    restar(a, b) {  // Sintaxis corta
        return a - b;
    }
};

console.log(calculadora.sumar(5, 3)); // 8

// Object methods
let llaves = Object.keys(persona);
let valores = Object.values(persona);
let entradas = Object.entries(persona);
```

**Ejercicio**: 
- Crea un objeto representando un libro con sus propiedades
- Crea un objeto con métodos para gestionar una cuenta bancaria
- Itera sobre las propiedades de un objeto e imprímelas

### Actividad 9: Funciones
**Objetivo**: Crear funciones reutilizables.

```javascript
// Declaración de función
function saludar(nombre) {
    return `¡Hola ${nombre}!`;
}

// Expresión de función
const despedir = function(nombre) {
    return `¡Adiós ${nombre}!`;
};

// Función flecha (arrow function)
const sumar = (a, b) => a + b;
const cuadrado = x => x ** 2;  // Un solo parámetro
const imprimir = () => console.log("Hola"); // Sin parámetros

// Función con parámetros por defecto
function presentar(nombre, edad = 18) {
    return `${nombre} tiene ${edad} años`;
}

// Función con rest parameters
function sumarTodos(...numeros) {
    return numeros.reduce((sum, num) => sum + num, 0);
}

console.log(sumarTodos(1, 2, 3, 4, 5)); // 15

// Callback functions
function procesar(numero, operacion) {
    return operacion(numero);
}

let resultado = procesar(5, x => x * 2); // 10
```

**Ejercicio**: 
- Crea una función que calcule el área de diferentes figuras
- Crea una función que determine si una palabra es palíndromo
- Implementa una función que use callbacks para procesar arrays
- Convierte funciones tradicionales a arrow functions

### Actividad 10: Scope y Closures
**Objetivo**: Entender el alcance de variables y closures.

```javascript
// Scope global
let global = "soy global";

function funcionExterna() {
    // Scope de función
    let externa = "soy externa";
    
    function funcionInterna() {
        // Scope interno
        let interna = "soy interna";
        console.log(global);   // Puede acceder
        console.log(externa);  // Puede acceder
        console.log(interna);  // Puede acceder
    }
    
    funcionInterna();
    // console.log(interna); // Error: no puede acceder
}

// Closure
function crearContador() {
    let cuenta = 0;
    
    return {
        incrementar: function() {
            cuenta++;
            return cuenta;
        },
        obtener: function() {
            return cuenta;
        }
    };
}

let contador = crearContador();
console.log(contador.incrementar()); // 1
console.log(contador.incrementar()); // 2
console.log(contador.obtener());     // 2
```

**Ejercicio**: 
- Crea un closure que simule una variable privada
- Implementa un generador de IDs únicos usando closures
- Crea una función que recuerde el último valor con el que fue llamada

## 🚀 Nivel Avanzado

### Actividad 11: Programación Orientada a Objetos
**Objetivo**: Crear y usar clases.

```javascript
// Definir una clase
class Persona {
    constructor(nombre, edad) {
        this.nombre = nombre;
        this.edad = edad;
    }
    
    saludar() {
        return `Hola, soy ${this.nombre}`;
    }
    
    cumplirAnios() {
        this.edad++;
    }
    
    // Método estático
    static especie() {
        return "Homo sapiens";
    }
}

// Usar la clase
let persona1 = new Persona("Ana", 25);
console.log(persona1.saludar());
persona1.cumplirAnios();
console.log(Persona.especie());

// Herencia
class Estudiante extends Persona {
    constructor(nombre, edad, carrera) {
        super(nombre, edad);
        this.carrera = carrera;
    }
    
    estudiar() {
        return `${this.nombre} está estudiando ${this.carrera}`;
    }
}

let estudiante1 = new Estudiante("Luis", 20, "Ingeniería");
console.log(estudiante1.saludar());
console.log(estudiante1.estudiar());
```

**Ejercicio**: 
- Crea una clase `CuentaBancaria` con métodos para depositar y retirar
- Crea una jerarquía de clases: `Vehiculo` → `Coche`, `Moto`
- Implementa getters y setters en una clase

### Actividad 12: Destructuring y Spread
**Objetivo**: Usar sintaxis moderna de ES6+.

```javascript
// Destructuring de arrays
let numeros = [1, 2, 3, 4, 5];
let [primero, segundo, ...resto] = numeros;
console.log(primero);  // 1
console.log(resto);    // [3, 4, 5]

// Destructuring de objetos
let persona = {
    nombre: "Ana",
    edad: 25,
    ciudad: "Madrid"
};
let { nombre, edad } = persona;
console.log(nombre);   // "Ana"

// Renombrar al destructurar
let { nombre: nombrePersona } = persona;

// Valores por defecto
let { pais = "España" } = persona;

// Spread operator con arrays
let arr1 = [1, 2, 3];
let arr2 = [4, 5, 6];
let combinado = [...arr1, ...arr2];

// Spread operator con objetos
let obj1 = { a: 1, b: 2 };
let obj2 = { c: 3, d: 4 };
let objCombinado = { ...obj1, ...obj2 };

// Rest parameters en funciones
function sumar(...numeros) {
    return numeros.reduce((sum, n) => sum + n, 0);
}
```

**Ejercicio**: 
- Usa destructuring para intercambiar valores de variables
- Clona un objeto y modifícalo sin afectar el original
- Crea una función que acepte parámetros nombrados usando destructuring

### Actividad 13: Promesas y Async/Await
**Objetivo**: Manejar operaciones asíncronas.

```javascript
// Crear una promesa
function esperar(ms) {
    return new Promise((resolve, reject) => {
        setTimeout(() => {
            resolve(`Esperé ${ms}ms`);
        }, ms);
    });
}

// Usar promesas con .then()
esperar(1000)
    .then(mensaje => {
        console.log(mensaje);
        return esperar(1000);
    })
    .then(mensaje => {
        console.log(mensaje);
    })
    .catch(error => {
        console.error("Error:", error);
    });

// Async/Await
async function ejemploAsync() {
    try {
        let mensaje1 = await esperar(1000);
        console.log(mensaje1);
        
        let mensaje2 = await esperar(1000);
        console.log(mensaje2);
    } catch (error) {
        console.error("Error:", error);
    }
}

// Múltiples promesas en paralelo
async function paralelo() {
    let resultados = await Promise.all([
        esperar(1000),
        esperar(2000),
        esperar(1500)
    ]);
    console.log(resultados);
}
```

**Ejercicio**: 
- Crea una función que simule una petición HTTP con promesas
- Implementa un sistema de retry con promesas
- Usa async/await para hacer múltiples operaciones en secuencia

### Actividad 14: Manipulación del DOM (para navegador)
**Objetivo**: Interactuar con páginas web.

```javascript
// Seleccionar elementos
let elemento = document.getElementById("miId");
let elementos = document.querySelectorAll(".miClase");
let primerElemento = document.querySelector(".miClase");

// Modificar contenido
elemento.textContent = "Nuevo texto";
elemento.innerHTML = "<strong>Texto en negrita</strong>";

// Modificar estilos
elemento.style.color = "blue";
elemento.style.fontSize = "20px";

// Modificar atributos
elemento.setAttribute("data-id", "123");
let valor = elemento.getAttribute("data-id");

// Agregar/remover clases
elemento.classList.add("nueva-clase");
elemento.classList.remove("vieja-clase");
elemento.classList.toggle("activo");

// Crear elementos
let nuevoDiv = document.createElement("div");
nuevoDiv.textContent = "Soy nuevo";
document.body.appendChild(nuevoDiv);

// Eventos
elemento.addEventListener("click", function(event) {
    console.log("¡Elemento clickeado!");
    event.preventDefault(); // Prevenir comportamiento por defecto
});

// Evento con arrow function
elemento.addEventListener("mouseover", (e) => {
    e.target.style.backgroundColor = "yellow";
});
```

**Ejercicio**: 
- Crea un contador que incremente al hacer click
- Implementa un cambio de tema (claro/oscuro)
- Crea un formulario que valide datos antes de enviar

### Actividad 15: Proyecto - Lista de Tareas Interactiva
**Objetivo**: Aplicar todos los conceptos en un proyecto web.

```html
<!DOCTYPE html>
<html>
<head>
    <title>Lista de Tareas</title>
    <style>
        .completada { text-decoration: line-through; }
    </style>
</head>
<body>
    <h1>Mi Lista de Tareas</h1>
    <input type="text" id="nuevaTarea" placeholder="Nueva tarea">
    <button id="agregar">Agregar</button>
    <ul id="listaTareas"></ul>

    <script>
        class GestorTareas {
            constructor() {
                this.tareas = [];
                this.cargarDesdeLStorage();
            }
            
            agregar(texto) {
                const tarea = {
                    id: Date.now(),
                    texto: texto,
                    completada: false
                };
                this.tareas.push(tarea);
                this.guardarEnLStorage();
                return tarea;
            }
            
            completar(id) {
                const tarea = this.tareas.find(t => t.id === id);
                if (tarea) {
                    tarea.completada = !tarea.completada;
                    this.guardarEnLStorage();
                }
            }
            
            eliminar(id) {
                this.tareas = this.tareas.filter(t => t.id !== id);
                this.guardarEnLStorage();
            }
            
            guardarEnLStorage() {
                localStorage.setItem('tareas', JSON.stringify(this.tareas));
            }
            
            cargarDesdeLStorage() {
                const datos = localStorage.getItem('tareas');
                if (datos) {
                    this.tareas = JSON.parse(datos);
                }
            }
        }
        
        const gestor = new GestorTareas();
        const lista = document.getElementById('listaTareas');
        const input = document.getElementById('nuevaTarea');
        const boton = document.getElementById('agregar');
        
        function renderizar() {
            lista.innerHTML = '';
            gestor.tareas.forEach(tarea => {
                const li = document.createElement('li');
                li.className = tarea.completada ? 'completada' : '';
                li.innerHTML = `
                    <span>${tarea.texto}</span>
                    <button onclick="completarTarea(${tarea.id})">✓</button>
                    <button onclick="eliminarTarea(${tarea.id})">✗</button>
                `;
                lista.appendChild(li);
            });
        }
        
        function completarTarea(id) {
            gestor.completar(id);
            renderizar();
        }
        
        function eliminarTarea(id) {
            gestor.eliminar(id);
            renderizar();
        }
        
        boton.addEventListener('click', () => {
            if (input.value.trim()) {
                gestor.agregar(input.value);
                input.value = '';
                renderizar();
            }
        });
        
        input.addEventListener('keypress', (e) => {
            if (e.key === 'Enter') {
                boton.click();
            }
        });
        
        renderizar();
    </script>
</body>
</html>
    ```

**Ejercicio**: 
- Añade la capacidad de editar tareas
- Implementa filtros (todas, pendientes, completadas)
- Agrega fechas de vencimiento a las tareas
- Mejora el diseño con CSS

## 📖 Recursos Recomendados

- [MDN Web Docs - JavaScript](https://developer.mozilla.org/es/docs/Web/JavaScript)
- [JavaScript.info](https://javascript.info/)
- [Eloquent JavaScript](https://eloquentjavascript.net/)
- [You Don't Know JS](https://github.com/getify/You-Dont-Know-JS)

## 🎯 Siguientes Pasos

Una vez completadas estas actividades:
1. Aprende un framework como React, Vue o Angular
2. Explora Node.js para desarrollo backend
3. Practica con APIs y fetch
4. Construye proyectos personales
5. Contribuye a proyectos open source

¡Sigue practicando y conviértete en un maestro de JavaScript! 🚀
