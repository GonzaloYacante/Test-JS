# Curso Práctico de JavaScript

Link: https://platzi.com/cursos/javascript-practico/?school=_escuela_escuela-web_

### Test de JS

## Instrucciones para tomar esta prueba

- Evalúa muy críticamente tu conocimiento.
- Si logras resolver la prueba, no importa cuánto te cueste, puedo asegurarte que tienes todo para continuar a las siguientes clases y tomar el resto del curso.
- Si no lo logras, no te preocupes, absolutamente nadie puede juzgarte, solo tú. Vuelve al [Curso Básico de JavaScript](https://platzi.com/cursos/basico-javascript/), anota los temas clave donde puedes mejorar, ubica las clases donde puedes aprenderlos y estudia vigorosamente.
- Es completamente válido hacer búsquedas en Google, cursos y tutoriales de Platzi, incluso usar tu cuaderno de notas sin importar si es físico o virtual.

Recuerda que **el éxito no se mide por cuánto tiempo te toma aprender**, esa métrica es relativamente inútil. Mejor concéntrate en completar los cursos de tu ruta de aprendizaje profesional y desarrollar los proyectos que realmente demuestran que dominas cada tecnología.

¡Mucha suerte!

## Variables y operaciones

### 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

- ¿Qué es una variable y para qué sirve?
  - Una variable es un espacio reservado en memoria en el que pueden almacenarse distintos tipos de datos, ya sea un string, number, boolean, Undefined, simbol, bigint, null, objetos, arrays o funciones. Hay 3 maneras de declarar las variables, var, const y let. En ES6 nacen let y const que son variable de tipo scope y esto quiere decir que dependiendo del scope es su accesibilidad.
- ¿Cuál es la diferencia entre declarar e inicializar una variable?
  - Declarar una variable es simplemente nombrarla, sin indicar el tipo de valor o dato que esta almacenara, pero inicializarla estamos indicando el tipo de dato y el valor que esta va a guardar.
  ```jsx
  //Declarar una variable
  let nombre;
  //Inicializar la variable
  nombre = "Gonza";
  //Podemos generar este proceso en una sola linea de código.
  let nombre = "Gonza";
  ```
- ¿Cuál es la diferencia entre sumar números y concatenar strings?
  - Cuando sumamos números estamos haciendo una operación matemática, en cambio cuando concatenamos 2 o más strings (Cadenas de texto), agarramos los strings originales y los juntamos para convertirlos en un nuevo string que contiene toda la información original que almacenaban los anteriores.
- ¿Cuál operador me permite sumar o concatenar?
  - El operador qué permite sumar y/o concatenar es el operador “ + ”.

### 2️⃣ Determina el nombre y tipo de dato para almacenar en variables la siguiente información:

- Nombre = String
- Apellido = String
- Nombre de usuario en Platzi = String
- Edad = Number
- Correo electrónico = String
- Mayor de edad = Boolean
- Dinero ahorrado = Number
- Deudas = Number

### 3️⃣ Traduce a código JavaScript las variables del ejemplo anterior y deja tu código en los comentarios.

```jsx
let nombre = "Gonzalo";
let apellido = "Yacante";
let nombreDeUsuarioEnPlatzi = "gonzaloyacante";
let edad = 18;
let email = "gyacante9@gmail.com";
let mayorDeEdad = true;
let dineroAhorrado = 3000;
let deudas = 1250;
```

### 4️⃣ Calcula e imprime las siguientes variables a partir de las variables del ejemplo anterior:

- Nombre completo (nombre y apellido)

  ```jsx
  let nombre = "Gonzalo";
  let apellido = "Yacante";

  console.log(`Mi nombre completo es ${nombre} ${apellido}`);
  ```

- Dinero real (dinero ahorrado menos deudas)

  ```jsx
  let dineroAhorrado = 3000;
  let deudas = 1250;

  let dineroTotal = dineroAhorrado - deudas;
  console.log(`El total de mi dinero es: ${dineroTotal}`);
  ```

## Funciones

### 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

- ¿Qué es una función?
  - Una función es un conjunto de acciones que nos permitirá reutilizar en nuestro código y siempre deben devolver un resultado. Podemos crear diferentes funciones con parámetros distintos y luego utilizar la información para realizar un evento o acción dentro de nuestro código.
- ¿Cuándo me sirve usar una función en mi código?
  - Usar una función nos sirve cuando hay que reutilizar código y repetir varias veces una misma acción. Por ejemplo, en vez de declarar una variable e inicializarla y poder usarla solo con esos datos, podemos crear una función a la que se le pasen 2 o más parámetros y así cada vez que necesitemos
- ¿Cuál es la diferencia entre parámetros y argumentos de una función?

  - Los parámetros son variables declaradas y solicitadas por una función.
  - Los argumentos son variables que se le asignan a la función cuando es llamada

  ```jsx
  function myFunction(parámetro1 + parámetro2) {
    //... All my code here
  };

  myFunction(argumento + argumento2);
  //Al declarar las variables parámetro1 y parámetro2 estamos generando los argumentos de nuestra función.
  ```

### 2️⃣ Convierte el siguiente código en una función, pero, cambiando cuando sea necesario las variables constantes por parámetros y argumentos en una función:

- Ejemplo

  ```
  const name = "Juan David";
  const lastname = "Castro Gallego";
  const completeName = name + lastname;
  const nickname = "juandc";

  console.log("Mi nombre es " + completeName + ", pero prefiero que me digas " + nickname + ".");
  ```

- Mi solución

  ```
  function saludoDeBienvenida (nombre, apellido, apodo) {
    console.log(`Hola! mi nombre es ${nombre} ${apellido}, pero me gusta que me llamen ${apodo}.`);
  }

  saludoDeBienvenida("Gonzalo", "Yacante", "Gonza")
  ```

## Condicionales

### 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

- ¿Qué es un condicional?
  - Es una expresión que nos permite evaluar si es True o False.
- ¿Qué tipos de condicionales existen en JavaScript y cuáles son sus diferencias?
  - If, else y else if: (Es mala practica anidar mas de 3 else if en un mismo bloque ya que ahí sería más práctico utilizar un Switch)
    - Con el If podemos tener una condición a cumplir, si se cumple se ejecuta el código de adentro, sino, no hace nada.
      ```jsx
      if (tengoPlata == true) {
        // código que se ejecuta si se cumple la condición.
        console.log("Felicitaciones, tenes plata");
      }
      ```
    - Con if else podemos tener una condición a cumplir, si se cumple se ejecuta el código de adentro, si esta no se cumple devuelve lo que le asignemos en el else pero no vuelve a evaluar ninguna condición, simplemente ejecuta el código.
      ```jsx
      if (tengoPlata == true) {
        // código que se ejecuta si se cumple la condición.
        console.log("Felicitaciones, tenes plata");
      } else {
        // código que se ejecuta si no se cumple la condición del if.
        console.log("Que lastima, no tenes plata");
      }
      ```
    - Con else if podemos tener una condición a cumplir, si se cumple se ejecuta el código de adentro, si esta no se cumple tiene otra condición a cumplir y solo si la segunda condición se cumple va a ejecutar el código que tiene dentro. Sino no devuelve nada
      ```jsx
      if (tengoPlata == true) {
        // código que se ejecuta si se cumple la condición.
        console.log("Felicitaciones, tenes plata");
      } else if (tengoPlata == false) {
        // código que se ejecuta si no se cumple la condición del if pero se cumple la condición del else if.
        console.log("Que lastima, no tenes plata");
      }
      ```
  - Switch = toma una sola expresión de entrada pero puede evaluar muchas opciones sin necesidad de comprobar una por una, evalúa tantos casos como sea necesario de una forma más ordenada.
- ¿Puedo combinar funciones y condicionales?
  - Podemos encadenar una respuesta desde un condicional a otro pero no podemos combinarlo dentro de una misma expresión. Si podemos usarlos de forma separada y luego encadenar una acción dependiendo del resultado.

### 2️⃣ Replica el comportamiento del siguiente código que usa la sentencia switch utilizando if, else y else if:

- Ejemplo

  ```jsx
  const tipoDeSuscripcion = "Basic";

  switch (tipoDeSuscripcion) {
    case "Free":
      console.log("Solo puedes tomar los cursos gratis");
      break;
    case "Basic":
      console.log(
        "Puedes tomar casi todos los cursos de Platzi durante un mes"
      );
      break;
    case "Expert":
      console.log(
        "Puedes tomar casi todos los cursos de Platzi durante un año"
      );
      break;
    case "ExpertPlus":
      console.log(
        "Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año"
      );
      break;
  }
  ```

- Mi solución

  ```jsx
  function tipoDeSuscripcion(suscripcionElegida) {
    if (suscripcionElegida == "Free") {
      console.log("Solo puedes tomar los cursos gratis");
    } else if (suscripcionElegida == "Basic") {
      console.log(
        "Puedes tomar casi todos los cursos de Platzi durante un mes"
      );
    } else if (suscripcionElegida == "Expert") {
      console.log(
        "Puedes tomar casi todos los cursos de Platzi durante un año"
      );
    } else if (suscripcionElegida == "ExpertPlus") {
      console.log(
        "Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año"
      );
    } else {
      console.log("No tienes ninguna suscripción");
    }
  }

  tipoDeSuscripcion("Basic");
  ```

### 3️⃣ Replica el comportamiento de tu condicional anterior con if, else y else if, pero ahora solo con if (sin else ni else if).

> 💡 Bonus: si ya eres una experta o experto en el lenguaje, te desafío a comentar cómo replicar este comportamiento con arrays u objetos y un solo condicional. 😏

- Mi solución

  ```jsx
  const tiposDeSuscripciones = {
    free: "Solo puedes tomar los cursos gratis",
    basic: "Puedes tomar casi todos los cursos de Platzi durante un mes",
    expert: "Puedes tomar casi todos los cursos de Platzi durante un año",
    expertduo:
      "Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año",
  };

  function conseguirTipoSuscripcion(suscripcion) {
    if (tiposDeSuscripciones[suscripcion]) {
      console.log(tiposDeSuscripciones[suscripcion]);
      return;
    }
    console.warn("Ese tipo de suscripción no existe");
  }

  conseguirTipoSuscripcion("free");
  ```

## Ciclos

### 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

- ¿Qué es un ciclo?
  - En JavaScript los ciclos son utilizados para realizar tareas repetitivas (se crea un bucle o loop) dependiendo necesariamente de una condición. Como resultados, condiciones devuelven true (verdadero) o false (falso). El bucle continuará ejecutándose hasta que la condición devuelva false.
- ¿Qué tipos de ciclos existen en JavaScript?
  - Existen diferentes tipos de bucles en JavaScript: for, do while, while, for in, for of.
- ¿Qué es un ciclo infinito y por qué es un problema?
  - Un ciclo infinito es cuando el bucle no tiene una manera de finalizar (La condicion nunca se cumple). Por consecuencia nuestro código puede fallar o que se consuman muchos recursos (por no decir todos) del dispositivo que se este utilizando.
- ¿Puedo mezclar ciclos y condicionales?
  - Sí, podemos condicionar un ciclo para que se repita todas las veces hasta que se cumplan una condición que internamente puede tener otra condición para su evaluación.

### 2️⃣ Replica el comportamiento de los siguientes ciclos for utilizando ciclos while:

- Ejemplo

  ```jsx
  for (let i = 0; i < 5; i++) {
    console.log("El valor de i es: " + i);
  }

  for (let i = 10; i >= 2; i--) {
    console.log("El valor de i es: " + i);
  }
  ```

- Mi solución

  ```jsx
  let condicion1 = 0;

  function while1(i) {
    while (i < 5) {
      console.log("El valor de i es: " + i);
      i++;
    }
  }
  while1(condicion1);

  //----------------------------------------------

  let condicion2 = 10;

  function while2(j) {
    while (j >= 2) {
      console.log("El valor de i es: " + j);
      j--;
    }
  }
  while2(condicion2);
  ```

### 3️⃣ Escribe un código en JavaScript que le pregunte a los usuarios cuánto es `2 + 2`. Si responden bien, mostramos un mensaje de felicitaciones, pero si responden mal, volvemos a empezar.

> 💡 Pista: puedes usar la función prompt de JavaScript.

```jsx
let suma = 0;

function sumar(resultado) {
  while (resultado != 4) {
    resultado = prompt("Cuanto es 2 + 2?");
    if (resultado == 4) {
      console.log("Felicitaciones, respondiste 4, es correcto.");
    } else {
      console.log(
        `Uhh, respondiste mal, ${resultado} no es el resultado correcto, por favor vuelve a intentarlo.`
      );
    }
  }
}
sumar(suma);
```

## Listas

### 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

- ¿Qué es un array?
  - Es una variable que puede guardar muchos valores dentro y de distintos tipos como números, strings, objetos e incluso más arrays, no solo 1 como seria una variable de tipo number o string. Se escriben dentro de [ … ], separado por una coma.
- ¿Qué es un objeto?
  - Es una representación en código de un elemento de la vida real. Está compuesto con por atributos y propiedades.
- ¿Cuándo es mejor usar objetos o arrays?
  - Objeto cuando se quiere representar un elemento de la vida real en código. El array se usa cuando en un mismo objeto se quieren guardar varios datos de diferentes tipos
- ¿Puedo mezclar arrays con objetos o incluso objetos con arrays?
  - Si es posible guardar dentro de un array un objeto y viceversa.

### 2️⃣ Crea una función que pueda recibir cualquier array como parámetro e imprima su primer elemento.

```jsx
let arrayListasPunto2 = ["Primer elemento", "segundo elemento"];

function primerElementoDeCualquierArray(array) {
  console.log(array[0]);
}

primerElementoDeCualquierArray(arrayListasPunto2);
```

### 3️⃣ Crea una función que pueda recibir cualquier array como parámetro e imprima todos sus elementos uno por uno (no se vale imprimir el array completo).

```jsx
let arrayListasPunto3 = [
  "Primer elemento",
  "segundo elemento",
  "tercer elemento",
];

function imprimirArray(array) {
  for (let i = 0; i < array.length; i++) {
    console.log(array[i]);
  }
}

imprimirArray(arrayListasPunto3);
```

### 4️⃣ Crea una función que pueda recibir cualquier objeto como parámetro e imprima todos sus elementos uno por uno (no se vale imprimir el objeto completo).

```jsx
let myCar = {
  make: "Ford",
  model: "Mustang",
  year: 1969,
};

function readObject(object) {
  for (let key in object) {
    console.log(object[key]);
  }
}

readObject(myCar);
```
