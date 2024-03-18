
**************************PRACTICANDO TESTING
En src se crea una carpeta llamada base-pruebas y una carpeta hermana llamada tests. De manera que base-pruebas y tests serian dos carpetas hermanas ambas dentro de src.
Dentro de tests creamos otra carpeta llamada base-pruebas que seria la carpeta espejo de la carpeta base-pruebas que existe en src. La dinamica es que en la carpeta base-pruebas de src hay ejercicios de javascript cada ejercicio en su propio archivo y por cada archivo existente en base-pruebas de src tiene un archivo de mismo nombre en el base-pruebas de la carpeta test.

************************CONFIGURACION INICIAL PARA EL TESTING
Cuando hablamos de CRA hay que hacer pocas configuraciones pero con vite hay que hacer mas configuraciones.Como se indica a continuacion.

Se trabaja con react testing library y jest
Esta configuracion se hace una vez en el proyecto pero segun lo aprendido en el curso de udemy es importante hacerlo de manera reiterativa para tener practica.

*Ir al sitio oficial de jest jest.io
Notica:se trabajara con jest en conjunto con react-testing-library mas adelante.

*En la pagina oficial copiar el comando de instalacion yarn add --dev jest
**Vamos a la terminal de vscode y pegamos el comando y ejecutamos.
**ejecutamos el comando yarn add -D @types/jest  //para activar el intelisence del autocompletado o sugerenciaas de la sintaxis de jest.
Notica: ojo que si estas con npm escojes el comando respectivo de npm y si estas en yarn escoges el de yarn
*Verifica la dependencia en el package.json
*En el package.json pegar el script del test:
{
"scripts":{
"test":"jest"
}
}

Quedaria asi:

"scripts":{
"dev":"vite",
"build":"vite build",
"preview":"vite preview",
"test":"jest --watchAll"     **le metemos watchAll para que escuche constantemente 
}

*Abre una terminal y ejecuta yarn test, eso te dara un pequeño error lo cual es normal

*la carpeta espejo que se creo arriba, se incluye al lado de src como carpeta hermana de src y no se coloca dentro para no abultar la src. en todo caso hay varias maneras de hacer la estructura. para este caso puntual nos fuimos por crear la carpeta test al lado de src como carpeta hermana.
La sintaxis es tipo demo.test.js

*estructura de una prueba: test('este es el modelo de prueba',()=>{})

***Jest - Expect - toBe  => jest nos ayuda a que no tengamos que escribir codigo dentro de las pruebas

Mira el siguiente ejemplo:
test('esto no debe fallar',()=>{
const message1 = 'Hola mundo';//inicializacion
const message2 = message1.trim();//trimear seria el estimulo
expect(message1).toBe(message2);//assert


})

En el ejemplo de arriba en vez de meter un if, usamos la sintaxis de jest


***Para que las pruebas sse vean mas bonitas y organizadas podemos meter las pruebas dentro de un describe. la sintaxis de un describe es la siguiente y podemos utilizar varios describe dentro de un mismo archivo.

describre('pruebas en <ComponenteEjemplo/>',()=>{
//Aqui adentro puedes meter tus tests
})

En la siguiente clase de hace la configuracion parea las pruebas dde nuestros distintos archivos, en caso de ver el error "You appear to be using a native ECMAScript module configuration file, Which only is supported when running babel asinchronously."Cambiar la extensiojn de los archivos jest.config.js y babel.congig.js a .cjs

Para ver mas detalles al respecto pueden ir a https://nodejs.org/docs/latest/api/modules.html#enabling.



