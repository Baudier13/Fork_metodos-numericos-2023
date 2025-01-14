## Cómo instalar Juila con su Jupyter y algunas primeras nociones de uso.

Aqui daremos las instrucciones para instalar Julia y otros accesorios.

### Instalando Julia:

La instalación de los binarios de Julia es bastante sencilla:
    
Ir a la [https://julialang.org/downloads/](https://julialang.org/downloads/)
        
Allí elija la instalación de acuerdo al sistema operativo de su computadora. En particular, constate si su computadora tiene instalado un sistema operativo de 32 bits o de 64 bits (el usual), y en base a ello, baje la versión de Julia correspondiente. 

Complementariamente, puede inspeccionar las instrucciones para instalar Julia en su sistema operativo en la misma página de Julia. Por ejemplo, para instalar Julia en Windows siga [éstas instrucciones](https://julialang.org/downloads/platform/#windows).

        
### Siga las instrucciones de instalación de acuerdo a su sistema. 
        
En todos los sistemas, luego de la instalación, la ejecución les dará una ```Terminal``` donde estará ejecutando el REPL. 
Allí ya puede ejecutar comandos de Julia. 

### Trabajando con Julia

Vamos a trabajar con  `IJulia`, es un notebook similar a Jupyter, pero nativo de Julia. Las instrucciones para su instalación
las pueden encontrar [https://github.com/JuliaLang/IJulia.jl](https://github.com/JuliaLang/IJulia.jl)

Alternativamente se puede bajar una aplicación de Jupyterlab que se puede encontrar en [https://github.com/jupyterlab/jupyterlab-desktop](https://github.com/jupyterlab/jupyterlab-desktop)
   
        
Alternativamente puede usar `Pluto`, es un nuevo tipo de notebook que es muy intersante y tiene varias ventajas sobre los otros. Pero estas ventajas también lo hacen complicado para personas con poca experiencia en la escritura de códigos. Por lo tanto **No lo recomendamos**. 
   De todos modos, las instrucciones para instalarlos están [https://github.com/fonsp/Pluto.jl](https://github.com/fonsp/Pluto.jl)
   
 ## Instalando IJulia
 
Para instalar paquetes debemos primero activar el administrador de paquetes ingresando el comando:

    julia> using Pkg


Luego, para instalar el *paquete* `IJulia` ingrese el comando:

    julia> Pkg.add("IJulia")

Alternativamente a estos dos pasos, puede activar una cónsola REPL especializada en administrar paquetes presionando la tecla `], para luego ingresar el comando:
 
    (@v1.7) pkg> add IJulia
       
Para salir de la cónsola para administrar paquetes y volver a la cónsola común de Julia, presione repetidamente la tecla `borrar` o `delete` o `backspace`.

Una vez instalado el paquete `IJulia`, lo activamos ingresando el comando:

    julia> using IJulia
    
Finalmente, activamos el administrador de notebooks llamado `JupyterLab` ingresando el comando:
    
    julia> jupyterlab()
    
La primera vez que ejecute este comando tomará un tiempo apreciable hasta que se complete el cargado del sofware y se compile el código. En particular, la primera vez le preguntará si desea instalar **Jupyter**, si no lo tiene ya instalado acceda a ello. En tal caso instalará otro paquete, llamado `Conda.jl`. 
Una vez completado el proceso le debería aparecer una página en su navegador (browser) donde podrá comenzar a trabajar con su notebook.
Mientras el administrador de notebooks esté activo, la consola REPL de Julia permanecerá inactiva, por lo que no podrá ingresar comandos en la misma.
La cónsola REPL de Julia volverá a la normalidad, una vez que Ud. apague el administrador de notebooks en el browser.

Cada vez que desee comenzar una nueva sesión para trabajar con el administrador de notebooks, deberá ingresar en la cónsola REPL de julia los dós últimos comandos:

    julia> using IJulia    
    julia> jupyterlab()

Recomendamos ver algún video que les muestre como trabajar. Es la forma más eficiente de aprender lo básico.

### Primer notebook

Para probar que todo el sistema funciona es importante generar una primer notebook donde escribiremos nuestros primeros códigos.

Para ello apretamos el rectángulo azul en la izquierda-arriba que tiene un +, eso abrirá un *launcher* donde verán el logo de Julia
![launcher](assets/launcher.jpeg)
Apretamos el mismo y habremos generado un notebook donde trabajar. En el mismo veremos una región rectangular donde se puede ingresar código, esto se llama una **celda**.
Hay distintos tipos de celda de acuerdo al lenguaje que querramos usar. Cerciorece que la última pestaña que muestra el siguiente gráfico diga **Code**. ![celda](assets/celda.png)

En la primer celda escribimos:

`println("Hola mundo")`

a continuación tecleamos `mayuscula-enter` (`shift-return`) simultáneamente, lo cual ejecutará la primer celda. Si todo anduvo bien debiera imprimirse debajo de la celda
**Hola mundo**. Se abrirá también una segunda donde podremos ingresar más código.

![hola_mundo](assets/hola_mundo.png)

La segunda celda la usaremos para incorporar una librería que usaremos mucho durante el curso, la `Plots.jl`. Para ello ingresaremos,

`using Pkg`

`Pkg.add("Plots")`

`using Plots`

![adding_plots](assets/adding_plots.png)

y luego ejecutamos la celda con `mayuscula-enter`. Julia procederá a instalar el paquete **Plots** y nos irá mostrando el avance. Si todo anda bien culminará sin errores y nos abrirá una nueva celda. 

En ella ingresaremos:

`plot(sin)`

Cuando la ejecutemos se producirá un gráfico de la función *seno*. ![plot_sin](assets/plot_sin.png)

#### Ejercicios: ###

Si quiere seguir aprediendo puede hacer algunos ejercicios símples:

1. Visite la página de la librería Plots.jl, [https://docs.juliaplots.org/latest/tutorial/](https://docs.juliaplots.org/latest/tutorial/) y trate de reproducir y entender la lógica de algunos ejemplos. También hay numerosos videos en youtube mostrando como generar gráficos.
2. Además de las celdas de código hay celdas de *markdown* que es una manera de editar y presentar código en forma grafíca de buena calidad. Practique poniendo título e indicaciones del código que escribió entre las celdas de código. Pueden ver un tutorial en [https://markdown.es/sintaxis-markdown/](https://markdown.es/sintaxis-markdown/). Hay muchísimos otros tutoriales y videos. 

Estos dos ejercicios le brindarán una herramienta poderosa que podrá usar en muchas instancias de su carrera.



       
