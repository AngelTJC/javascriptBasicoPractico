## VARIABLES Y OPERACIONES

## 1️⃣ Responde las siguientes preguntas:

    - ¿Qué es una variable y para qué sirve?
            Cajitas(espacios de memoria) donde podemos guardar información.
    - ¿Cuál es la diferencia entre declarar e inicializar una variable?
            Declarar es cuando le decimos a JavaScript que vamos a crear una variable
            con su nombre. Mientras que inicializar es darle(asignarle) un valor a esa
            variable.
    - ¿Cuál es la diferencia entre sumar números y concatenar strings?

    - ¿Cuál operador me permite sumar o concatenar?
            El operador que no permite sumar o concatenar es '+';

## 2️⃣ Determina el nombre y tipo de dato para almacenar en variables la siguiente información:

   - Nombre: strign
   - Apellido : string
   - Nombre de usuario en Platzi: string (@fulanito)
   - Edad: number
   - Correo electrónico: string (lasjdkf@gmail.com)
   - Mayor de edad: boolean
   - Dinero ahorrado: number
   - Deudas: number

## 3️⃣ Traduce a código JavaScript las variables del ejemplo anterior y deja tu código en los comentarios.

...
let nombre = 'Angel';
let apellido='Gutierrez';
let username='LuisGC';
let edad= 12;
let email='perro@gmail.com';
let esMayorEdad= true;
let dineroAhorrado= 10500;
let deudas= 1000;
...

## 4️⃣ Calcula e imprime las siguientes variables a partir de las variables del ejemplo anterior:

- Nombre completo (nombre y apellido)

- Dinero real (dinero ahorrado menos deudas)

```
let nombreCompleto=nombre + ' ' + apellido;
let dineroReal= dineroAhorrado - deudas;

```

### FUNCIONES
### 1️⃣ Responde las siguientes preguntas

    - ¿Qué es una función?
        R.- Las funciones son bloques de codigo encapsulados producto de
        una abstraccion de alguna accion que se quiere realizar. Nos permiten
        reutilizarlos.
    - ¿Cuándo me sirve usar una función en mi código?
        R.-Cuando tengamos que realizar una accion muchas veces. Tambien
        se usa para dividir un codigo muy grande en pedasos de funciones
        (divide y venceras).
    - ¿Cuál es la diferencia entre parámetros y argumentos de una función?
        R.- las funciones reciben parametros cuando las creamos. Y les enviamos
        argumentos cuando las ejecutamos.

### 2️⃣ Convierte el siguiente código en una función, pero, cambiando cuando sea necesario las variables constantes por parámetros y argumentos en una función:
```js
const name = "Juan David";
const lastname = "Castro Gallego";
const completeName = name + lastname;
const nickname = "juandc";

console.log("Mi nombre es " + completeName + ", pero prefiero que me digas " + nickname + ".");
```
```js
function nombreCompleto(name, lastname){
  return name+' '+lastname;
}

function saludo(name, lastname, nickname){
  const completeName=nombreCompleto(name,lastname);

  console.log(`Mi nombre es ${completeName}, pero prefiero que me digas ${nickname}.`);
}

saludo('Luis', 'Cantuta', 'Gato');
```

### CONDICIONALES
### 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

    - ¿Qué es un condicional?
        R.-Son la forma en que ejecutamos un bloque de codigo u  otro dependiendo
        de alguna condicion o validacion.

    - ¿Qué tipos de condicionales existen en JavaScript y cuáles son sus diferencias?
        R.- if(else, else if) y switch
        El condicional if nos permite hacer validaciones completamente distintas
        en cada validacion o condicional. En cambio, en el switch todos los cases
        se comparan con la misma variable o condicion que definimos en el switch.

    - ¿Puedo combinar funciones y condicionales?
        R.-Sí, Las funciones pueden encapsular cualquier bloque de codigo, incluyendo
        condicionales.

### 2️⃣ Replica el comportamiento del siguiente código que usa la sentencia switch utilizando if, else y else if:

```js
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
```js
if(tipoDeSuscripcion == "Free"){
       console.log("Solo puedes tomar los cursos gratis");
}else if(tipoDeSuscripcion == "Basic"){
       console.log("Puedes tomar casi todos los cursos de Platzi durante un mes");
}else if(tipoDeSuscripcion == 'Expert'){
       console.log("Puedes tomar casi todos los cursos de Platzi durante un año");
}else if(tipoDeSuscripcion == 'ExpertPlus'){
       console.log("Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año");
}

```

### 3️⃣ Replica el comportamiento de tu condicional anterior con if, else y else if, pero ahora solo con if (sin else ni else if).

```js

function suscripcion(tipoDeSuscripcion){
    if(tipoDeSuscripcion == "Free"){
       console.log("Solo puedes tomar los cursos gratis");
       return ;
}
if(tipoDeSuscripcion == "Basic"){
       console.log("Puedes tomar casi todos los cursos de Platzi durante un mes");
       return ;
}
if(tipoDeSuscripcion == 'Expert'){
       console.log("Puedes tomar casi todos los cursos de Platzi durante un año");
       return ;
}
if(tipoDeSuscripcion == 'ExpertPlus'){
       console.log("Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año");
       return ;
}
console.warn("No existe la suscripcion");
}
suscripcion("Free");

```
> 💡 Bonus: si ya eres una experta o experto en el lenguaje, te desafío a comentar cómo replicar este comportamiento con arrays u objetos y un solo condicional. 😏

```js
function conseguirTipoSuscripcion(suscripcion){
  if(tiposDeSuscripciones[suscripcion]){
    console.log(tiposDeSuscripciones[suscripcion]);
    return;
  }
  console.warn('Ese tipo de suscripcion no existe!');
}

const tiposDeSuscripciones={
  Free: "Solo puedes tomar los cursos gratis",
  Basic: "Puedes tomar casi todos los cursos de Platzi durante un mes",
  Expert:"Puedes tomar casi todos los cursos de Platzi durante un año",
  ExpertPlus:"Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año"
};

conseguirTipoSuscripcion("ExpertPlus");

```





### CICLOS
### 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

    - ¿Qué es un ciclo?
        R.- La forma de ejecutar un bloque de código haste que se cumpla cierta condición.

    - ¿Qué tipos de ciclos existen en JavaScript?
        R.- while, do while, for.
    - ¿Qué es un ciclo infinito y por qué es un problema?
        R.- Es cuando la validacion de nuestros condicionales nunca se cumple y
        se termina toteando(dañando) la aplicacion.
    - ¿Puedo mezclar ciclos y condicionales?
        R.- Sí, los ciclos son una especie de condicionales y podemos agregar mas
        condicionales dentro del blucle.

### 2️⃣ Replica el comportamiento de los siguientes ciclos for utilizando ciclos while:

```js
for (let i = 0; i < 5; i++) {
    console.log("El valor de i es: " + i);
}

let i = 0;
while(i < 5){
        console.log("El valor de i es: "+ i);
        i++;
}

```
```js

for (let i = 10; i >= 2; i--) {
    console.log("El valor de i es: " + i);
}

let i=10;
while(i >= 2){
        console.log(`El valor de i es: ${i}`);
        i--;
}

```

### 3️⃣ Escribe un código en JavaScript que le pregunte a los usuarios cuánto es 2 + 2. Si responden bien, mostramos un mensaje de felicitaciones, pero si responden mal, volvemos a empezar.
💡 Pista: puedes usar la función prompt de JavaScript.

```js
let input;
do{
	input=prompt('¿ Cuanto es 2 + 2 ?');
}while(input != "4");
console.log("Felicitaciones!!!!!");

```

### LISTAS
### 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

    - ¿Qué es un array?
        R.- Es una lista de elementos.

```js
        const array=[1, 'hola', true, false];
```
    - ¿Qué es un objeto?
        R.-Es una lista de elementos, pero cada elemento tiene un nombre y clave.

```js
        const obj={
                nombre:luis,
                edad:28,
                carrera: 'Ingenieria de Sistemas'
        };

```
    - ¿Cuándo es mejor usar objetos o arrays?
        R.-Arrays se usan para lista de datos secuenciales indexados.
        objetos: cuando esten relacionados y necesitemos ponerles nombre y valor.

    - ¿Puedo mezclar arrays con objetos o incluso objetos con arrays?
        R.-Los arrays pueden guardar objetos. Y los objetos pueden guardar arrays
        entre sus propiedades.

### 2️⃣ Crea una función que pueda recibir cualquier array como parámetro e imprima su primer elemento.

```js
function imprimirPrimerElementoArray(arr){
  console.log(arr[0]);
}

imprimirPrimerElementoArray(["Hola", "Mundo", "Preparate"]);

```

### 3️⃣ Crea una función que pueda recibir cualquier array como parámetro e imprima todos sus elementos uno por uno (no se vale imprimir el array completo).

```js
function imprimirElementoPorElemento(arr){
  for(let elemento of arr){
    console.log(elemento);
  }
}

imprimirElementoPorElemento(["Hi", "guys",'How are you?']);

```

### 4️⃣ Crea una función que pueda recibir cualquier objeto como parámetro e imprima todos sus elementos uno por uno (no se vale imprimir el objeto completo).

```js
function imprimirObjeto(obj){
  let arr=Object.entries(obj);
  for(let elem of arr){
    console.log(elem);
  }
}

let obj={
                nombre:'Luis',
                edad:28,
                carrera: 'Ingenieria de Sistemas'
        };

imprimirObjeto(obj);

```