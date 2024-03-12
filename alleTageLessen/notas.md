instalaciones para react:
simple react snippets
autoclose tags

Notas de react
Reacct al ser una libreria declarativa hace facil trabajar con patrones de diseño
react es una libreria declarativa


mira si no vas  a cambiar el valor de la variable dentro del codigo => usa const
si va a cambiar => usa let

oye si tienes ya declarada la variable let y quieres darle un nuevo valor a esa misma variable entonces porfavor no vuelvas a tipear let solamente tipea el nopmbre de variable y ya esta.

let crea variable de scope. si tu asignas un valor a una let y luego dentro del mismo archivo creas una funcion y dentro de esta funcion asignas un nuevo valor a let y le das console.log alli dentro de la funcion te arroja ese mismo valor que le has asignado.PERO si das consolel.log fuera de esa funcion entonces va a tomar el valor con el que fue asignado por fuera. ya que el alcance queda limitado a la funcion.

*truquito: cuando quieres mostrar por consola un objeto le puedes dar console.table y te lo muestra a forma de tabla

*porfa dale un repaso al objeto literal

****git checkout -- .    si eliminas un archivo o varios por accidente, este comando rehace todo y te ponne el proyecto como estaba antes del commit. es como si dijeras lo siento vamos justo atras.

*el push modifica el arreglo original es por eso que no se recomienda.
*ten en cuenta que el arreglo tambien es un objeto en javascript

*El spread operator es utilizado para crear copias por ejempolo de un array..literalmente toma los elementos de la estructura de datos y la pone en la nueva structura de datos que quieras hacer.

*Es muy importante tener en cuenta que el map crea un nuevo arreglo. y si te vas al proto de los arreglos te vas a encontrar que array.map es uno de los metodos del proto de los array.


*****Observe y practica este uso de backcticts en esta pequeña funcion:
function saludar(nombre){ return `hola ${nombre}`}

***las funciones tradicionales deben tener un return explicito
***Para las funciones flechas las puedo simplificar cuando tenemos una sola linea despues del return. para esto le quitamos las llaves..ya quitandole las llaves le puedo quirtar el return

***practicar find y filter

****puedo tener una importacion por defecto y varias importaciones individuales de un mismo archivo en una misma linea de codigo.la importacion nombrada o especifica se encierra entre llaves como si de una desestructuracion se tratara.


**********OJO APRENDER PRACTICAR MANIPULACION DEL DOM

******************************REACT***************************************************************

COMPONENTE: una pieza de codigo encapsulado  reutilizable que realiza un trabajo en especifico que puede tener estado o no.

NOTA: FERNANDO HERRERA USA YARN PARA DEPENDENCIAS LOCALES Y NPM PARA DEPENDENCIAS GLOBALES.

****El tree shaking consiste en eliminar todos aquellos paquetes o depoendencias que nosotros no utlizamos.Generalmenmte se hace durante el build.

**la finaliddad de cra es crear un spa => como es un spa se requiere un solo index=>ese index se encuentra en public.Nosotros montamos nuestra aplicaccion de react en el div que tiene id='root'


********Una de las granades ventajas que +tiene vite es la forma de hacer el hot module replacement que es la forma de cambiar modulos en caliente la cual es tan rapida que no se percibe al momento que se hace ctr + s ya esta desplegado el cambio.

******consejo si en un projecto de vite con yarn quieres cambiar para trabajar con npm simplemente elimina el archivo de bloqueo yarn.lock y dale npm install

*****dato que no sabia : para renderizar un objeto en react no se puede hacer directamente, ni siquiera colocando dovle corchte,para que se pueda renderizar se utiliza dentro de los corchetes el JSON.stringify(nombre de la variable que contiene el objeto)

****ojo que una promesa no puede ser renderizada, ya que estas son objetos



**********en cuanto al css para que este ordenado alfabeticamente le das ctr + shift+ p luego tipeas sorting lines y le das ascending,.

*******para mandar un numero como props

******ESTUDIAR LAS PROPTYPES EN EL CURSO O CON MIRCHA
*****ESTUDIAR DEFAULT PROPS DEL CURSO O CON MIRCHA

****Que es un custom hooks?un custom hook nos va ayudar a saber cuando estamos cargando informacion,cuando terminamos de cargarla,cuando cometemos un error y todo eso lo vamos a tener centralizado.De tel manera que si a dia de mañana necesitas hacer una llamada a una api usas tu custom hook.


*En react no hay una estructura de archivo ddefinida mas bien hay mas libertad y quesa de parte del desarrollador elegir la granularidad de la estructura de archivo,.

LEER articulo sobre estructura de archivos: https://hackernoon.com/structuring-projects-and-naming-components-in-react-1261b6e18d76