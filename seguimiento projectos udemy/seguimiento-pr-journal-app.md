1. yarn create journal-app abre en vs
2.creas estructura de directorio que vas a utilizar -autenticacion,router principal, rutas protegidas-carpeta de temas ..en fin hay que modularizar.
3.del boiler solo dejamos main.js y el index de css lo cambio a styles.css
4.Creo un archivo hermano a los archivos anteriores main.js e index.css llamado JournalApp.jsx y lo importamos en main.
5.dentro de src creo un modulo o carpeta de autenticacion llamado auth- en auth tendre diferentes paginas componentes para que todo lo que este en esa carpeta este relacionado a la autenticacion.
6. crear carpeta hermana a auth llamada journal. Aqui se crearan las paginas layouts componentes y todo lo relacionado con la aplicacion
7. crear la carpeta router hermana a las carpetas anteriores (este sera el router principal) y tambien de la misma forma crearemos la carpeta theme. en theme se establecen los temas globales que se van a utilizar.
configuramos las rutas primarias y secundarias para lo cual instalamos react router dom : yarn add react-router-dom@6    ******ojo que tiene que ser con yarn si estas con yarn  y el arroba es para que use la version 6
 
8. Dentro de la arpeta auth creamos el componente AppRouter  y en ese componente importamos Routes y Route . 
9. Dentro de auth creo tres carpetas que son : layout, pages, routes . layout es como el cascaron que todas las paginas dentro de auth van a tener.

Dentor de pages creamos los siguientes componentes: LoginPage.jsx . Le colcamos LoginPage y no simplemente login porque LoginPage tendria una idea de pagina...es mas semantico.

De la misma forma creamos el modulo (o componente ) RegisterPage.jsx 
creamos un archivo de barril index.jsx que exporte todo de login y de register-

Ahora vamos a la carpeta rotes que esta dentro de auth  y creamos el modulo AuthRoutes.jsx wue simple mente seria un funcional component exportado por nombre que tendra Routes.Asi luce: 
export const AuthRoutes = () => {
  return (
    <>
        <Routes>
            <Route path='login' element = {<LoginPage/>}/>
            <Route path='register' element = {<RegisterPage/>}/> 
            <Route path='/*' element = {<Navigate to='/auth/login'/>}/> 
            </Routes>
    </>
  )
}


Ahora para la carpeta journal,que sera una sola pagina, creamos una carpeta pages y una carpeta routes.

Dentro de lacarpeta pages creamos el modulo JournalPage.jsx
Dentro de routes me creo el modulo JournalRoutes.jsx y dentro este establecemos la ruta a esa pagina.

Ahora nos vamos al router principal