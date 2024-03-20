***** INSTRUCCIONES BASICAS PARA CONFIGURAR UN PROYECTO DESDE CERO CON SASS O SCSS

1)arranca el proyecto con vite
2)instala sass con npm i sass o yarn add sass (favor corrobora con la documentacion)
3)cambia las extencionde de css a scss.

4) en el source crea una carpeta scss y dentro de esta carpeta cree las siguientes carpetas:
a)abstracts
dentro de esta carpeta abstracts crea los archivos:
 _variables.scss
_mixins.scss
b)base
_base.scss
-resets.scss

En el archivo index.scss importamos de la siguiente manera:

/*abstracts*/
@use './scss/abstracts/variables';
@use './scss/abstracts/mixins';

/*base*/
@use './scss/base/base';
@use  './scss/base/resets';

** Si tuvieras mas elementos en la carpeta scss tendrias que importarle en index como la seccion anterior.

importacion de la fuente

vas a googlefonts escoges la fuenta a tu gusto y mediante @import haces la importacion de la fuente en el archivo variables de la carpeta abstracts.
@import url('https://fuente')

en este mismo archivo creo las variables:

:root{
/*fonts*/
--font-poppins: 'Poppins', sans-serif;

/*colors*/
recurda que todos estos archivos se estan importando en el index y por tanto estarian disponibles en todo el arbol de los componentes de react.

ahora en la carpeta base hacemos una base muy pequeña de la siguiente manera:
html,body{
font-family:var(--font-poppins);}
alli notaras como cambia el estilo de letra

ahora te vas a el archivo resets en la carpeta base y escribes lo siguiente, aunque para projectos grandes se usa normalize

*{
 box-sizing: border-box;
 margin: 0;
 padding: 0;

}

li{
list-style:none;
}

a{
 text-decoration:none
}

button{
border:none;
background:none;
font-family: var(--font-poppins);//los botones no heredan la fuente del html por eso le asigno fuente.
}