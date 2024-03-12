CURSO COMPETO DE TESTING

*EXISTEN DOS TIPOS DE PRUEBAS: PRUEBAS UNITARIAS Y PRUEBAS DE INTEGRACION
UNITARIAS: PRUEBA PEQUEÑAS PIEZAS DE LA APLICACION
DE INTEGRACION: COMO FUNCIONAN VARIAS PIEZAS EN CONJUNTO

LAS PRUEBAS UNIARIAS DEBEN SER FACILES DE ESCRIBIR,LEER,CONFIABLES,RAPIDAS Y PRINCIPALMENTE UNITARIAS

AAA = ARRANGE, ACT, ASSERT

LAS PRUEBAS SE PUEDEN AUTOMATIZAR POSTERIORMENTE PERO PRIMERO DEBEN SER CREADAS.

***LA RECOMENDACION : PROBAR SIEMPRE LA RUTA CRITICA PARA AHORRAR DESPERDICIOS DE TIEMPO.

CON CRA NO HAY QUE HACER TANTAS CONFIGURACIONES PORQUE LA MAYORIA DE LAS COSAS VIENE PRECONFIGURADAS.
CON VITE SI HAY QUE HACER CONFIGURACIONES.

***LA CONFIGURACIOLN DEL FRAMEWORK DE PRUEBA ES ALGO QUE HAY QUE HACER DE MANERA REPETIDA PARA MEMORIZARLO Y ACOSTUNBRARSE A TESTEAR.

**SE TRABAJA CON JEST Y REACT TESTING LIBRAY QUE SON AMBOS COLABORATICVOS Y NO SE REEMPLAZAN ENTRE SI

CONFIGURACION:
1. yarn add --dev jest
2. en los scripts del paquete json agregar "test": "jest" o "test": "jest --watchAll" el --watchAll es preferible ya que pone al test alerta de cualquier cambio.
3. Abres otra ventana de la terminal y ejecutas el comando : yarn test para npm : npm run test (te generarea)
4. el carpetaa de pruebas puede tomar uno de varios lugares en el file system. Seria buena practica colocarlo al lado del proyecto src y no dentro de el para no hacer el src mas pesado o mas grande.entonces se crea una carpeta test al lado o a nivel de src.Esta carpeta va a ser una carpeta espejo de src es como si fuera un src2 solo que las extenciones de los archivos sera .test.js
5. Dentro de test creamos un archivo demo.test.js y corremos el comando yarn test ...obvio me generqara un error diciendo que p'or lo menos debe haber una prueba.

Sintaxis basica de una prueba:
test('esta prueba no debe fallar',()=>{

})

Ejemplos: 
1.test('Esta prueva np puede fallar',()=>{
if(0===0){
throw new Error('No se puede dividir entre cero')
}
})   Aqui la prueba falla porque if da true entonces se lanza el error prefabricado.

2.test('Esta prueva np puede fallar',()=>{
if(1===0){
throw new Error('No se puede dividir entre cero')
}
})   
Al dar false la condicion no se entra a las llaves por lo cual no se genera error y la prueba pasa

Ahora con jest no tememos que tener codigo dentro de nuestra sintaxis basica de porueba. Solo tener en cuanta el concepto de AAA
Ejemplo:

test('esta es una prueba',()=>{
//A
const message1 = 'Hola Mundo';
//A
const message2 = message1.trim();
//A

expect(message1).toBe(message2);


})


para activar el autocompletado y sugerencias de la jerga de jest se instala como dependencisa de desarrollo el @types/jest como dependencia de desarrollo de la siguiente forma: 
yarn add -D @types/jest

nota: por temas de presentacion podemos usar un describe..el uso de describe me da mas organizacion

el cascaron de describe es asi: 
describe('pruebas en <Democomonent/>'()=>{}
Aqui metes la prueba anterior:
test('esta es una prueba',()=>{
//A
const message1 = 'Hola Mundo';
//A
const message2 = message1.trim();
//A

expect(message1).toBe(message2);


})
})