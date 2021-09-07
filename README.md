# app-asistente-estudio
--------------------------------------------------------------------------------------------------------------------------------------------
App web Front-End, escrita en HTML, CSS y JS.

Pensada para ofrecer un ambiente de trabajo, basado en las apps de Google, a estudiantes de modalidad on-line o autodidacta-on-line.

Para estudiantes de web development, este proyecto sirve para motivar el aprendizaje y la optimización de proyectos, ya que al ser solo el Front-End, se pudiesen buscar 
soluciones de escalabilidad, además de la gran cantidad de mejoras que pueden ser aplicadas al propio Front-End.

Este proyecto puede ser utilizado para practicar la teoría básica de HTML, CSS y JS.
--------------------------------------------------------------------------------------------------------------------------------------------

##Pre requisitos: https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web
## Instrucciones (6/9/2021-21:34:40-UTC+2): 

1)Abrir una carpeta para alojar la app. Ejemplo:**"App_Asistente_Estudios"**

2)Abrir un archivo index.html.

  2.1) Iniciar Archivo de html. 
  
  
Ejemplo:**"App_Asistente_Estudios/index.html"**

```html

<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>App Asistente Estudios</title> 
	
```

  2.2) Iniciar un Archivo de CSS y llamarlo en el documento html. 
Ejemplo:**"App_Asistente_Estudios/estilo.css"** y **"App_Asistente_Estudios/index.html"**
```html
	<link rel="stylesheet" href="App_Asistente_Estudios/estilo.css">
</head>
```
                         
                                 
 3) Agregar un `<header>` en el documento, para pasar un banner superior y colocar el titulo que se mostrara al usuario. 
    Ejemplo: 
```html
<header>
	<div><h1>Titulo que se muestra al usuario</h1></div>
</header>
```
```html
<header>
        <div type="banner_Superior"><h1 style="font-family: Arial, Helvetica, sans-serif;color:white;background-color: rgb(3, 85, 30);">Asistente de Estudios</h1></div>
</header>
```

3.1) Se escribe en el archivo .CSS. 
 Ejemplo:**"App_Asistente_Estudios/estilo.css "**
 ```css
 div {
	background-color: lightgrey;
	width: 70%;
	border: 15px solid green;
	padding: 50px;
	margin: 20px;
	}
```
                                                      
                                                 

4) Se inicia la etiqueta `<body>`. 
Ejemplo:**"App_Asistente_Estudios/index.html"**
```html
<body style="background-color: orange;">
```
5) Se inicia la Etiqueta `<ul>` dentro de `<body>`; se le pasan los titulos de los elementos que van a componer el Workspace. 
Ejemplo:**"App_Asistente_Estudios/index.html"**
 ```html
 <ul>
	<li>Pomodoro Counter</li>
	<li>Google Docs</li>
	<li>Google</li>
	<li>Calendario</li>
	<li>Lista de Objetivos</li>
</ul>
```
5.1) Agregamos el codigo .css a la etiqueta `<li>` con el atributo `style:""`, en este caso letras blancas `<li style:"color:white">`
```html
<ul>
	<li style="color:white">Pomodoro Counter</li>
	<li style="color:white">Google Docs</li>
	<li style="color:white">Google</li>
	<li style="color:white">Calendario</li>
	<li style="color:white">Lista de Objetivos</li>
</ul>
```                            
        
 5.2) Anclamos a través de la etiqueta `<a>` los hipervinculos para acceder a la herramienta del workspace que el usuario prefiera.     
```html
<ul>
	<li style="color:white"><a target="_blank" href="Pomodoro/pomodoro_Counter.html" >Pomodoro Counter</a></li>
        <li style="color:white"><a target="_blank" href="https://docs.google.com">Google Docs</a></li>
        <li style="color:white"> <a target="_blank" href="https://www.google.es/">Google</a></li>
        <li style="color:white"><a target="_blank" href="https://calendar.google.com/calendar">Calendario</a></li>
        <li style="color:white"><a target="_blank" href="Todos/Todo.html">Lista de Objetivos</a> </li>
</ul>
```
                                   
 5.3) Cerramos la etiqueta `</body>` y la etiqueta `</html>` respetando la indentación correcta para finalizar con el documento .html.
 Ejemplo:**"App_Asistente_Estudios/index.html"**
```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8">
        <title>App Asistente Estudios</title>
        <link rel="stylesheet" href="Pagina_principal/estilo.css">
    </head>
    <header>
    <div type="banner_Superior"><h1 style="font-family: Arial, Helvetica, sans-serif;color:white;background-color: rgb(3, 85, 30);">Asistente de Estudios</h1></div>
    </header>
    <body style="background-color: orange;">
        <ul>
            <li style="color:white"><a target="_blank" href="Pomodoro/pomodoro_Counter.html" >Pomodoro Counter</a></li>
            <li style="color:white"><a target="_blank" href="https://www.sejda.com/es/pdf-editor?">Block de Notas</a></li>
            <li style="color:white"> <a target="_blank" href="https://www.google.es/">Google</a></li>
            <li style="color:white"><a target="_blank" href="https://calendar.google.com/calendar">Calendario</a></li>
            <li style="color:white"><a target="_blank" href="Todos/Todo.html">Lista de Objetivos</a> </li>
        </ul>
        
    </body>
</html>
```
 
 
 
 
6) Creamos 2 carpetas, que contendran los archivos necesarios para el _“Pomodoro Counter”_ y la _“Lista de Tareas”_
  
6.1) **_“Pomodoro Counter”_**
6.1.1) Abrimos carpeta dentro del fichero principal. 
Ejemplo:**"App_Asistente_Estudios/Pomodoro"**
6.1.1.1) Abrimos un Archivo .html para el _“Pomodoro Counter”_ 
Ejemplo:**"App_Asistente_Estudios/Pomodoro/pomodoro_Counter.html"**
6.1.1.1.1) Iniciar Archivo de html. 
Ejemplo:**"App_Asistente_Estudios/Pomodoro/pomodoro_Counter.html"**
```html
<!DOCTYPE html>
<html lang="en">
<head>
      <meta charset="UTF-8">
      <title>Pomodoro Timer</title> 
```

6.1.1.1.2) Iniciar un Archivo de CSS y llamarlo en el documento html. 
Ejemplo:**"App_Asistente_Estudios/Pomodoro/pomodoro_Counter.html"**
```html
	<link rel="stylesheet" href="style_pomodoro_counter.css">
</head>
```
6.1.1.1.3) Iniciar un Archivo de CSS. 
Ejemplo:**"App_Asistente_Estudios/Pomodoro/style_pomodoro_counter.css"**            
```css
html {
	background-color: #f8a323;
	height: 100%;
	font-family: Arial, Helvetica, sans-serif;
}
```
6.1.1.1.4) En el Ejemplo anterior, indicamos el codigo CSS para el layout del codigo html en general, con atributos como `"background-color:; height:; font-family:;"`
6.1.1.1.5) Continuamos definiendo el diseño css dentro del archivo **"App_Asistente_Estudios/Pomodoro/style_pomodoro_counter.css"**. En este caso para la etiqueta `<h1>Pomodoro Timer</h1>`
```css
h1 {
    color: white;
    font-family: Arial, Helvetica, sans-serif;
    text-align: center;
   }
```
6.1.1.1.6) Continuamos definiendo el diseño css dentro del archivo **"App_Asistente_Estudios/Pomodoro/style_pomodoro_counter.css"**. En este caso para `<div id="container">`
```css
#container {
            height: 200px;
            width: 700px;
            background-color: #F5E4C3;
            margin: 0 auto;
            border: 5px solid #88B169;

            display: grid;
            grid-template-columns: repeat(5, 1fr);
            grid-template-rows: repeat(3, 1fr);
            }
                      
```
            
6.1.1.1.1.3) Continuamos definiendo el diseño css dentro del archivo **"App_Asistente_Estudios/Pomodoro/style_pomodoro_counter.css"**. 
                      En este caso para los `class="timer"` dentro de `<div id="container">`. es decir:
              
              
**Dentro del archivo "App_Asistente_Estudios/Pomodoro/pomodoro_Counter.html"**
```html
<!--Work Timer-->
<div id="work-timer" class="timer">
	<p id="w_minutes">25</p><p class="semicolon">:</p><p id="w_seconds">00</p>
</div>

<!--Cycle Counter-->
<p id="counter" class="timer">0</p>

<!--Break Timer-->
<div id="break-timer" class="timer">
	<p id="b_minutes">05</p><p class="semicolon">:</p><p id="b_seconds">00</p>
</div>
```
           
           
 **Dentro del archivo "App_Asistente_Estudios/Pomodoro/style_pomodoro_counter.css".**
```css
/*timers*/
.label {
	align-self: center;
    	justify-self: center;

    	font-size: 30px;
    	font-weight: bold;
	}

#work {
    grid-area: 1 / 2 / 1 / 2;
}
#break {
    grid-area: 1 / 4 / 1 / 4;
}
#cycles {
    grid-area: 1 / 3 / 1 / 3;
}

.timer {
    display: flex;
    align-self: center;
    justify-self: center;

    font-size: 30px;
    font-weight: bold;
}

p {
    margin: 0;
    padding: 0;
}

#counter {
    grid-area: 2 / 3 / 2 / 3;
    color: red;
}

#work-timer {
    grid-area: 2 / 2 / 2 / 2;
}

#break-timer {
    grid-area: 2 / 4 / 2 / 4;
}
```



         
6.1.1.1.1.4) Continuamos definiendo el diseño css dentro del archivo **"App_Asistente_Estudios/Pomodoro/style_pomodoro_counter.css"**. 
En este caso para los botones.
**Dentro del archivo "App_Asistente_Estudios/Pomodoro/style_pomodoro_counter.css".**
```css
/*buttons*/

.btn {
    align-self: center;
    justify-self: center;

    width: 100px;
    height: 30px;

    font-size: 20px;
}

#start {
    grid-area: 3 / 2 / 3 / 2;
}

#reset {
    grid-area: 3 / 3 / 3 / 3;
}

#stop {
    grid-area: 3 / 4 / 3 / 4;
}
```
                      
                      
         
         
         
6.1.1.4) Iniciamos la etiqueta `<body>`
6.1.1.5) iniciamos etiqueta `<h1>` dentro de `<body>`
6.1.1.6) Pasamos un parrafo con codigo css y texto `<p style:""></p>`.
6.1.1.7) Iniciamos una etiqueta `<div>` para crear un objeto con `id="container"` para html y  `#container{}` para css.
6.1.1.8) Pasamos 3 parrafos con codigo css y texto `<p style:""></p>`. que llamaremos:`"Work","cycle","break"` en referencia al tiempo de trabajo (25min), ciclos completos (25+5 min de descanso) y descanso/break(5min)
      6.1.1.9) Anidamos otra etiqueta `<div>` que contendrá: `"work Timer"`. la cerramos `</div>`
      6.1.1.10)Anidamos otra etiqueta `<div>` que contendrá: `"break Timer"`. la cerramos `</div>`
      6.1.1.11)Anidamos una etiqueta` <p> `que muestra los ciclos completos.
      6.1.1.12)Anidamos 3 etiquetas `<button>` correspondientes a:` "Start", "Pause", "Reset"`
      6.1.1.13)Abrimos la etiqueta `<script>` para utilizar las funciones que manejan la funcionalidad del timer
      6.1.1.14)Cerramos `</body>` y `</html>`
  
6.2) “Lista de Tareas”
6.2.1) Abrimos carpeta dentro del fichero principal. Ejemplo:**"App_Asistente_Estudios/Todos"**
6.2.1.1) Abrimos un Archivo `.html` para la **_“Lista de Tareas”_**. Ejemplo:**"App_Asistente_Estudios/Todos/Todo.html**
6.2.1.2) Iniciar Archivo de html. 
Ejemplo:**"App_Asistente_Estudios/Todos/Todo.html"**
```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title></title>
```
                               
6.2.1.3)Iniciar un Archivo de CSS y llamarlo en el documento html. 
Ejemplo:**"App_Asistente_Estudios/Todos/Todo.html"**

```html
	<link rel="stylesheet" href="style_todo.css">
</head>
```                                                
                          

--------------------------------------------------------------------------------------------------------------------------------------------


Repositorio Git: https://github.com/CristianRomero1234/App_asistente_estudio
El Repositorio cuenta con una carpeta principal (App_Asistente_Estudios)
que contiene 2 carpetas adicionales con los archivos necesarios para desplegar el “Pomodoro Counter” (App_Asistente_Estudios/Pomodoro), 
y la “Lista de Tareas”(App_Asistente_Estudios/Todos); y un archivo .HTML (App_Asistente_Estudios/index.html) y un  archivo .CSS (App_Asistente_Estudios/estilo.css).

(App_Asistente_Estudios)
	(App_Asistente_Estudios/Pomodoro)
		(App_Asistente_Estudios/Pomodoro/Pomodoro_counter_Main.js)
		(App_Asistente_Estudios/Pomodoro/pomodoro_Counter.html)
		(App_Asistente_Estudios/Pomodoro/style_pomodoro_counter.css)


	(App_Asistente_Estudios/Todos)
		(App_Asistente_Estudios/Todos/Todo_Main.js)
		(App_Asistente_Estudios/Todos/Todo.html)
		(App_Asistente_Estudios/Todos/style_todo.css)

	(App_Asistente_Estudios/index.html)

	(App_Asistente_Estudios/estilo.css)
-----------------------------------------------------------------------------------------------------------------------------------------

