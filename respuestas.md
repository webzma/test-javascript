## Respuestas al Test de JavaScript

## Variables y operaciones

### 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

- ¿Qué es una variable y para qué sirve?

Una variable es un espacio en memoria que nos permite guardar un valor o información, de tal modo que funciona como una cajita donde podemos guardar algún tipo de dato (dependiendo del lenguaje que usemos);

- ¿Cuál es la diferencia entre declarar e inicializar una variable?

Declarar una variable es básicamente cuando la creamos y la nombramos mediante un nombre, y inicializar una variable es cuando le asignamos un valor.

- ¿Cuál es la diferencia entre sumar números y concatenar strings?

La diferencia entre ellas radica en los tipos de datos de los valores que estemos intentando sumar o concatenar XD. De modo que, si intentamos sumar un String y número se va a concatenar y se convertirá en un string, y si intentamos sumar dos tipos de datos númericos se sumarán esos valores. En resumen el operador (+) sirve tanto para concatenar y sumar, todo va a depender de los tipos de datos.

- ¿Cuál operador me permite sumar o concatenar?

    El operador de suma (+).

### 2️⃣ Determina el nombre y tipo de dato para almacenar en variables la siguiente información:

- Nombre (String)
- Apellido (String)
- Nombre de usuario en Platzi (String)
- Edad (Number)
- Correo electrónico (String)
- Mayor de edad (Boolean)
- Dinero ahorrado (Number)
- Deudas (Number)

### 3️⃣ Traduce a código JavaScript las variables del ejemplo anterior y deja tu código en los comentarios.

```
const nombre = "Wilberk ";
const apellido = "Ledezma";
let nombreDeUsuario = "webzma";
let edad = 19;
const correo = "wilberkledezma51@gmail.com";
let mayorDeEdad = true;
let dineroAhorrado = 1000;
let deudas = 300;
```

### 4️⃣ Calcula e imprime las siguientes variables a partir de las variables del ejemplo anterior:

- Nombre completo (nombre y apellido)
- Dinero real (dinero ahorrado menos deudas)

```
let nombreCompleto = nombre + apellido;
let dineroReal = dineroAhorrado - deudas;
```

## Funciones

### 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

- ¿Qué es una función?

Una función es un bloque de código con el que podemos hacer algo y retornar un valor. Las funciones la podemos invocar o utilizar en cualquier sitio de nuestro código, por otro lado, también podemos y tenemos la ventaja de poder reutilizar ese bloque de código.

- ¿Cuándo me sirve usar una función en mi código?

Podemos utilizar una función cuando queramos que nuestra aplicación ejecute una función o haga una acción, de esta manera la aplicación podrá reaccionar a las acciones del usuario. 

- ¿Cuál es la diferencia entre parámetros y argumentos de una función?

Las funciones reciben parámetros cuando la creamos y cuando la invocamos o llamamos le pasamos argumentos.

### 2️⃣ Convierte el siguiente código en una función, pero, cambiando cuando sea necesario las variables constantes por parámetros y argumentos en una función:

```
const name = "Juan David";
const lastname = "Castro Gallego";
const completeName = name + lastname;
const nickname = "juandc";

console.log("Mi nombre es " + completeName + ", pero prefiero que me digas " + nickname + ".");


// FUNCIÓN
function printName(name, lastname, nickname) {
    console.log(`Mi nombre es ${name} ${lastname}, pero prefiero que digas ${nickname}.`);
}

printName("Wilberk", "Ledezma", "webzma");
```

## Condicionales

### 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

- ¿Qué es un condicional?

Una condicional es un bloque de código que se ejecuta si una condición se cumple. Las condicionales nos permiten tomar desiciones en nuestro programa.

- ¿Qué tipos de condicionales existen en JavaScript y cuáles son sus diferencias?

El condiconal IF (else y else if) nos permite hacer validaciones completamente distintas si así queremos. En el Switch siempre se compara una sola cosa.

- ¿Puedo combinar funciones y condicionales?

Sí las funciones pueden encapsular condicionales y viceversa.

### 2️⃣ Replica el comportamiento del siguiente código que usa la sentencia switch utilizando if, else y else if:

```
const tipoDeSuscripcion = "Basic";

switch (tipoDeSuscripcion) {
   case "Free":
       console.log("Solo puedes tomar los cursos gratis");
       break;
   case "Basic":
       console.log("Puedes tomar casi todos los cursos de Platzi durante un mes");
       break;
   case "Expert":
       console.log("Puedes tomar casi todos los cursos de Platzi durante un año");
       break;
   case "ExpertPlus":
       console.log("Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año");
       break;
}
```

```
if (tipoDeSuscripcion === "Basic") {
    console.log("Puedes tomar casi todos los cursos de Platzi durante un mes");
} else if (tipoDeSuscripcion === "Expert") {
    console.log("Puedes tomar casi todos los cursos de Platzi durante un año");
} else if (tipoDeSuscripcion === "ExpertPlus") {
    console.log("Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año");
} else {
    console.log("Solo puedes tomar los cursos gratis");
}
```

### 3️⃣ Replica el comportamiento de tu condicional anterior con if, else y else if, pero ahora solo con if (sin else ni else if).

```
if (tipoDeSuscripcion === "Basic") {
    console.log("Puedes tomar casi todos los cursos de Platzi durante un mes");
}  
if (tipoDeSuscripcion === "Expert") {
    console.log("Puedes tomar casi todos los cursos de Platzi durante un año");
}  
if (tipoDeSuscripcion === "ExpertPlus") {
    console.log("Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año");
} if (tipoDeSuccripcion === "Free") {
    console.log("Solo puedes tomar los cursos gratis");
}
```

> 💡 Bonus: si ya eres una experta o experto en el lenguaje, te desafío a comentar cómo replicar este comportamiento con arrays y un solo condicional. 😏

```
function findOutSuscription(suscription) {
	const tipoDesSuscripcion = {
        "Free": "Solo puedes tomar los cursos gratis",
        "Basic": "Puedes tomar casi todos los cursos de Platzi durante un mes",
        "Expert": "Puedes tomar casi todos los cursos de Platzi durante un año",
        "ExpertPlus": "Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año"
	}
			
	if (tipoDesSuscripcion[suscription]) {
		console.log(tipoDesSuscripcion[suscription])
	}   else {
		    console.warn("Ese tipo de suscripción no existe.")
		}
}
findOutSuscription("Basic");
```

## Ciclos

### 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

- ¿Qué es un ciclo?

Es una forma de ejecutar un bloque de código de manera repetitiva mientras que una condición o valores que estén siendo evaluados se cumplan. Por ejemplo: "Mientras que la variable numero sea menor que 10 se ejecutará una acción".

- ¿Qué tipos de ciclos existen en JavaScript?

Tipos de ciclos: FOR, WHILE, DO WHILE.

- ¿Qué es un ciclo infinito y por qué es un problema?

Un ciclo infinito se ejecuta repetitivamente sin detenerse, de modo que la condición se cumple siempre que es evaluada y no tiene un valor diferente que haga que determinado bucle no pare.

Es un problema porque se ejecutará infinitamente sin retornar un valor.

- ¿Puedo mezclar ciclos y condicionales?

Sí, todo depende del caso. Los ciclos tienen su propias condiciones, aunque todo depende de lo que se quiera lograr.

### 2️⃣ Replica el comportamiento de los siguientes ciclos for utilizando ciclos while:

```
for (let i = 0; i < 5; i++) {
    console.log("El valor de i es: " + i);
}

for (let i = 10; i >= 2; i--) {
    console.log("El valor de i es: " + i);
}

let count1 = 0;

while (count1 < 5) {
    console.log("El valor de i es: " + count1);
    count1++;
}

let count2 = 10;

while (count2 >= 2) {
    console.log("El valor de i es: " + count2);
    --count2;
} 

```

### 3️⃣ Escribe un código en JavaScript que le pregunte a los usuarios cuánto es `2 + 2`. Si responden bien, mostramos un mensaje de felicitaciones, pero si responden mal, volvemos a empezar.

> 💡 Pista: puedes usar la función prompt de JavaScript.

```
let numero = 0;
		
while(numero != 4) {
	numero = prompt("¿Cuánto es 2 + 2");
}
```


## Listas

### 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

- ¿Qué es un array?

Un array es una lista que nos permite almacenar varios datos y de diferentes tipos.

Ejemplo: 

```
let numbers = [1, 2, 3, 4, 5]
```

- ¿Qué es un objeto?

Es una lista muy similar a un array pero en este caso, los objetos están conformados por un nombre clave (propiedad) y su valor.

Ejemplo: 

```
let wilberk = {
    name: "Wilberk",
    lastname: "Ledezma",
    age: 20
}
```

- ¿Cuándo es mejor usar objetos o arrays?

Un array lo utilizamos cuando simplemente queremos tener una lista de alguna cosa y los objetos solemos utilizarlos para tener más datos (propiedades que conforman un solo objeto).

- ¿Puedo mezclar arrays con objetos o incluso objetos con arrays?

Sí. Podemos mezclar tanto arrays con objetos y viceversa.

### 2️⃣ Crea una función que pueda recibir cualquier array como parámetro e imprima su primer elemento.

```
let array = [1, 2, 3, 5, 10];

function printArray(array) {
    console.log(array[0])
}
printArray(array);
```

### 3️⃣ Crea una función que pueda recibir cualquier array como parámetro e imprima todos sus elementos uno por uno (no se vale imprimir el array completo).

```
let array = [1, 2, 3, 5, 10];

function printArray(array) {
    for(i of array) {
        console.log(i)
    }
}
printArray(array);
```

### 4️⃣ Crea una función que pueda recibir cualquier objeto como parámetro e imprima todos sus elementos uno por uno (no se vale imprimir el objeto completo).

```
let objeto = {
    name: "Objetito",
    id: 10,
    color: "red"
}

function printArray(objeto) {
    const arr = Object.values(objeto)
    for(i of arr) {
        console.log(i)
    }
}
printArray(objeto);
```