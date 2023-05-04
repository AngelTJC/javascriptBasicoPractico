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
```
const name = "Juan David";
const lastname = "Castro Gallego";
const completeName = name + lastname;
const nickname = "juandc";

console.log("Mi nombre es " + completeName + ", pero prefiero que me digas " + nickname + ".");
```
```
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
