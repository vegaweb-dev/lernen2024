Permisos
Estando en windows trabajaba mandando cambios a mi repo de github vega-web-dev relacionado al correo carlosjuniorrvega@hotmail.com. Posteriormente quice trabajar desde este mismo equipo(estacion 1 equipo portatil Dell) pero mandando cambios a un repositorio distinto relacionado al correo carlosjuniorvega94@gmail.com . Al momento de querer empujar mi primer cambio me aparecia en la terminal un error de permisos pues mit git estaba amarrado a mis credenciales carlosjuniorrvega@hotmail.com que corresponde al github vegaweb-dev.

Procedi a cambiar mis credenciales con git config --global user.name <nombre>
Procedi a cambiar mis credenciales con git config --global user.name <nombre>
                                       git config --global user.email carlosjuniorvega94@gmail.com

Luego de verificar que habia cambiado las credenciales el error persistia. 
Un compañero fue al credential manager del computador y nos dimos cuenta que aun la cuenta anterior estaba persistida. es decir el github vegaweb-dev permanecia a pesar de haber cambiado las credenciales. 

Solucion: procedimos a remover la cuenta de github del credential manager y le dimos git push. todo funciono.