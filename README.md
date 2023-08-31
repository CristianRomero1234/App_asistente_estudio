Create three folders, name them "html, js, css".

Inside directory named html, create file "index.html",

Inside directory named js, create file "main.js",

Inside directory named css, create file "style.css",


At first we will write all the code inside "index.html", then progresively move it to other files.

Make use of https://text-compare.com/ and/or https://onlinetextcompare.com/html to check the differences between one step and thhe following.

When comparing the code make sure to "iterate" at least 2 times. 

1) compare your current code to the code provided on each step.
2) compare the differences and make sure you understand before writing the new code to your program.

Keys for completing this tutorial:

- Compare the code you write with the examples provided.
- Research what you don't understand. But don't let "not knowing" be an obstacle for writting the code provided.
- Mind your keystrokes when transcribing. (type what you read, not what you "think" you read)
- Type the code by yourself (you can copy it and paste it, but imagine the next examples as "pictures" of how the file should look like after each new addition)

Let's jump in:

Write in index.html the basic "well-formed" scaffold.

---

```html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>App my Studies tool</title>
</head>
<body>
    
</body>
</html>


```
As we will focus on learning Bootstrap, then let's include the CDNs for Bootstrap version 5 in our index.html file:

---
```html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <!-- Notice the inclusion of bootstrap's v5.3.1 CDN -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.1/dist/css/bootstrap.min.css" rel="stylesheet">
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.1/dist/js/bootstrap.bundle.min.js"></script>
    
    <title>App my Studies tool</title>
</head>
<body>
    
</body>
</html>


```
Now, for the next step, we will create our "Navigation bar". 
We will include links to google search, google calendar, also placeholder links for other features of our web page.
Notice the use of semantic HTML, other good practices are to include unique "id" attributes for each element inside <body>


---
```html

<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.1/dist/css/bootstrap.min.css" rel="stylesheet">
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.1/dist/js/bootstrap.bundle.min.js"></script>
    <title>App my Studies tool</title>
</head>

<body>
    <!-- A grey horizontal navbar that becomes vertical on small screens -->
    <nav class="navbar navbar-expand-sm bg-light">
        <div class="container-fluid">
            <!-- Links -->
            <ul class="navbar-nav">
                <li class="nav-item">
                    <a target="_blank" href="https://www.google.com/">
                        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/2f/Google_2015_logo.svg/272px-Google_2015_logo.svg.png" alt="Google" style="max-height: 40px">
                    </a>
                </li>
                <li class="nav-link">
                    <a target="_blank" href="https://calendar.google.com/calendar"><img
                        style="max-height: 40px"
                            src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/a5/Google_Calendar_icon_%282020%29.svg/2048px-Google_Calendar_icon_%282020%29.svg.png" alt="Google Calendar" height="75" /> 
                    </a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#">Pomodoro Counter</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#">Block de notas</a>
                </li>
                <li class="nav-item">
                    <a href="#" class="nav-link">Lista de Objetivos</a>
                </li>
            </ul>
        </div>
    </nav>
</body>

</html>

```
Let's change "Block de notas" and make it "Escribir", notice that we replaced the html class attribute for easing the process of writting the necessary CSS code to style a "dropdown menu" with options. (Bootstrap CDN, provides over the internet the CSS+JS code that help us use "Bootstrap Components")  

In this way we can offer a variety of resources, that handle the writing and taking notes tasks (Including writing our own using HTML, CSS and JS).

```html

<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.1/dist/css/bootstrap.min.css" rel="stylesheet">
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.1/dist/js/bootstrap.bundle.min.js"></script>
    <title>App my Studies tool</title>
</head>

<body>
    <!-- A grey horizontal navbar that becomes vertical on small screens -->
    <nav class="navbar navbar-expand-sm bg-light">
        <div class="container-fluid">
            <!-- Links -->
            <ul class="navbar-nav">
                <li class="nav-item">
                    <a target="_blank" href="https://www.google.com/">
                        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/2f/Google_2015_logo.svg/272px-Google_2015_logo.svg.png"
                            alt="Google" style="max-height: 40px">
                    </a>
                </li>
                <li class="nav-link">
                    <a target="_blank" href="https://calendar.google.com/calendar"><img
                        style="max-height: 40px"
                            src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/a5/Google_Calendar_icon_%282020%29.svg/2048px-Google_Calendar_icon_%282020%29.svg.png"
                            alt="Google Calendar" height="75" /> </a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#">Pomodoro Counter</a>
                </li>
                <li class="nav-item dropdown">
                    <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown">Escribir</a>
                    <ul class="dropdown-menu">
                      <li><a class="dropdown-item" href="#">Google Docs</a></li>
                      <li><a class="dropdown-item" href="#">Online PDF editor</a></li>
                      <li><a class="dropdown-item" href="#">Your custom HTML Notepad</a></li>
                    </ul>
                  </li> 
                <li class="nav-item">
                    <a href="#" class="nav-link">Lista de Objetivos</a>
                </li>
            </ul>
        </div>
    </nav>
</body>

</html>

```
Now, features as "Pomodoro counter", "Lista de Objetivos" and "Your Custom HTML Notepad", are better suited to be displayed together but without interfering with one another, so we will append and an "Accordion" that help us with having our three features handy.

---
```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.1/dist/css/bootstrap.min.css" rel="stylesheet">
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.1/dist/js/bootstrap.bundle.min.js"></script>
    <title>App my Studies tool</title>
</head>

<body>
    <!-- A grey horizontal navbar that becomes vertical on small screens -->
    <nav class="navbar navbar-expand-sm bg-light">
        <section class="container-fluid">
            <!-- Links -->
            <ul class="navbar-nav">
                <li class="nav-item">
                    <a target="_blank" href="https://www.google.com/">
                        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/2f/Google_2015_logo.svg/272px-Google_2015_logo.svg.png"
                            alt="Google" style="max-height: 40px">
                    </a>
                </li>
                <li class="nav-link">
                    <a target="_blank" href="https://calendar.google.com/calendar"><img style="max-height: 40px"
                            src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/a5/Google_Calendar_icon_%282020%29.svg/2048px-Google_Calendar_icon_%282020%29.svg.png"
                            alt="Google Calendar" height="75" /> </a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#">Pomodoro Counter</a>
                </li>
                <li class="nav-item dropdown">
                    <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown">Escribir</a>
                    <ul class="dropdown-menu">
                        <li><a class="dropdown-item" href="#">Google Docs</a></li>
                        <li><a class="dropdown-item" href="#">Online PDF editor</a></li>
                        <li><a class="dropdown-item" href="#">Your custom HTML Notepad</a></li>
                    </ul>
                </li>
                <li class="nav-item">
                    <a href="#" class="nav-link">Lista de Objetivos</a>
                </li>
            </ul>
        </section>
    </nav>
    <section class="accordion" id="accordionExample">
        <section class="accordion-item">
            <h2 class="accordion-header" id="headingOne">
                <button class="accordion-button" type="button" data-bs-toggle="collapse" data-bs-target="#collapseOne"
                    aria-expanded="true" aria-controls="collapseOne">
                   Pomodoro Counter
                </button>
            </h2>
            <section id="collapseOne" class="accordion-collapse collapse show" aria-labelledby="headingOne"
                data-bs-parent="#accordionExample">
                <section class="accordion-body">
                   This is where the  pomodoro counter lives
                </section>
            </section>
        </section>
        <section class="accordion-item">
            <h2 class="accordion-header" id="headingTwo">
                <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse"
                    data-bs-target="#collapseTwo" aria-expanded="false" aria-controls="collapseTwo">
                   Lista de Objetivos
                </button>
            </h2>
            <section id="collapseTwo" class="accordion-collapse collapse" aria-labelledby="headingTwo"
                data-bs-parent="#accordionExample">
                <section class="accordion-body">
                    This is where the  lista de objetivos lives
                </section>
            </section>
        </section>
        <section class="accordion-item">
            <h2 class="accordion-header" id="headingThree">
                <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse"
                    data-bs-target="#collapseThree" aria-expanded="false" aria-controls="collapseThree">
                   Your Custom HTML Notepad
                </button>
            </h2>
            <section id="collapseThree" class="accordion-collapse collapse" aria-labelledby="headingThree"
                data-bs-parent="#accordionExample">
                <section class="accordion-body">
                    This is where the  pomodoro counter lives
                </section>
            </section>
        </section>
    </section>
</body>

</html>
``` 
At this point we have the basic structure of our web page that so far only makes use of HTML and Bootstrap v5.3.1,

But we also know the is just a scaffold, and we're set for few more hours of work and learning.

Stop at this point. 

Do not go beyond this point until you've had at least a 6-hour timespan of being offline.

But please, make sure you understand what we have right now, and investigate the topics that sparked doubts.

---

Continue here after the break:

Now we will focus on adding more functionality.

---

First, find the text "Google Docs" inside of anchor tag, we will link to google docs (search for Google Docs anchor tag in you file index.html and add the href attribute pointing to "https://docs.google.com/")

`...   <li><a class="dropdown-item" href="https://docs.google.com/">Google Docs</a></li> ...`

---

Then, find the text "Online PDF editor" inside of anchor tag, we will link to an online pdf editor in our case: https://openpdf.com/lp/edit-pdf.html

(search for "Online PDF editor" anchor tag anchor tag in you file index.html and add the href attribute pointing to "https://openpdf.com/lp/edit-pdf.html")

`... <li><a class="dropdown-item" href="https://openpdf.com/lp/edit-pdf.html">Online PDF editor</a></li> ...`

---

We need to "connect" our links in the nav bar to our accordion, therefore we must do the following changes to the code:

Note that we're basically making use of attributes like `data-bs-toggle, data-bs-target, aria-expanded, aria-controls`, maybe intead of understanding what those are, check where are they being used in the code. (compare where they where being used before in the previous steps, and where are they being used now)

```html

<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.1/dist/css/bootstrap.min.css" rel="stylesheet">
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.1/dist/js/bootstrap.bundle.min.js"></script>
    <title>App my Studies tool</title>
</head>

<body>
    <!-- A grey horizontal navbar that becomes vertical on small screens -->
    <nav class="navbar navbar-expand-sm bg-light">
        <section class="container-fluid">
            <!-- Links -->
            <ul class="navbar-nav">
                <li class="nav-item">
                    <a target="_blank" href="https://www.google.com/">
                        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/2f/Google_2015_logo.svg/272px-Google_2015_logo.svg.png"
                            alt="Google" style="max-height: 40px">
                    </a>
                </li>
                <li class="nav-link">
                    <a target="_blank" href="https://calendar.google.com/calendar"><img style="max-height: 40px"
                            src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/a5/Google_Calendar_icon_%282020%29.svg/2048px-Google_Calendar_icon_%282020%29.svg.png"
                            alt="Google Calendar" height="75" /> </a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#collapseOne" data-bs-toggle="collapse" data-bs-target="#collapseOne" aria-expanded="true"
                        aria-controls="collapseOne">Pomodoro Counter</a>
                </li>
                <li class="nav-item dropdown">
                    <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown">Escribir</a>
                    <ul class="dropdown-menu">
                        <li><a class="dropdown-item" href="https://docs.google.com/">Google Docs</a></li>
                        <li><a class="dropdown-item" href="https://openpdf.com/lp/edit-pdf.html">Online PDF editor</a>
                        </li>
                        <li><a class="dropdown-item"  href="#collapseThree" data-bs-toggle="collapse"
                            data-bs-target="#collapseThree" aria-expanded="false" aria-controls="collapseThree">Your custom HTML Notepad</a></li>
                    </ul>
                </li>
                <li class="nav-item">
                    <a class="nav-link"  href="#collapseTwo" data-bs-toggle="collapse"
                    data-bs-target="#collapseTwo" aria-expanded="false" aria-controls="collapseTwo">Lista de Objetivos</a>
                </li>
            </ul>
        </section>
    </nav>
    <section class="accordion" id="accordionExample">
        <section class="accordion-item">
            <h2 class="accordion-header" id="headingOne">
                <button class="accordion-button" type="button" data-bs-toggle="collapse" data-bs-target="#collapseOne"
                    aria-expanded="true" aria-controls="collapseOne">
                    Pomodoro Counter
                </button>
            </h2>
            <section id="collapseOne" class="accordion-collapse collapse show" aria-labelledby="headingOne"
                data-bs-parent="#accordionExample">
                <section class="accordion-body">
                    This is where the pomodoro counter lives
                </section>
            </section>
        </section>
        <section class="accordion-item">
            <h2 class="accordion-header" id="headingTwo">
                <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse"
                    data-bs-target="#collapseTwo" aria-expanded="false" aria-controls="collapseTwo">
                    Lista de Objetivos
                </button>
            </h2>
            <section id="collapseTwo" class="accordion-collapse collapse" aria-labelledby="headingTwo"
                data-bs-parent="#accordionExample">
                <section class="accordion-body">
                    This is where the lista de objetivos lives
                </section>
            </section>
        </section>
        <section class="accordion-item">
            <h2 class="accordion-header" id="headingThree">
                <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse"
                    data-bs-target="#collapseThree" aria-expanded="false" aria-controls="collapseThree">
                    Your Custom HTML Notepad
                </button>
            </h2>
            <section id="collapseThree" class="accordion-collapse collapse" aria-labelledby="headingThree"
                data-bs-parent="#accordionExample">
                <section class="accordion-body">
                    This is where  Your Custom HTML Notepad lives
                </section>
            </section>
        </section>
    </section>
</body>

</html>

```

---


Now, let's begin "our custom HTML Notepad" by writing a basic "notepad" implementation.

For this we will use <fieldset> tag, along some buttons (for which we will add functionality later on).

Compare your code with the following and update it accordingly.



```html

<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.1/dist/css/bootstrap.min.css" rel="stylesheet">
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.1/dist/js/bootstrap.bundle.min.js"></script>
    <title>App my Studies tool</title>

    <style>
        textarea {
            width: 100%;
            height: 150px;
            padding: 12px 20px;
            box-sizing: border-box;
            border: 2px solid #ccc;
            border-radius: 4px;
            background-color: #f8f8f8;
            font-size: 16px;
            resize: none;
        }
    </style>
</head>

<body>
    <!-- A grey horizontal navbar that becomes vertical on small screens -->
    <nav class="navbar navbar-expand-sm bg-light">
        <section class="container-fluid">
            <!-- Links -->
            <ul class="navbar-nav">
                <li class="nav-item">
                    <a target="_blank" href="https://www.google.com/">
                        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/2f/Google_2015_logo.svg/272px-Google_2015_logo.svg.png"
                            alt="Google" style="max-height: 40px">
                    </a>
                </li>
                <li class="nav-link">
                    <a target="_blank" href="https://calendar.google.com/calendar"><img style="max-height: 40px"
                            src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/a5/Google_Calendar_icon_%282020%29.svg/2048px-Google_Calendar_icon_%282020%29.svg.png"
                            alt="Google Calendar" height="75" /> </a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#collapseOne" data-bs-toggle="collapse" data-bs-target="#collapseOne"
                        aria-expanded="true" aria-controls="collapseOne">Pomodoro Counter</a>
                </li>
                <li class="nav-item dropdown">
                    <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown">Escribir</a>
                    <ul class="dropdown-menu">
                        <li><a class="dropdown-item" href="https://docs.google.com/">Google Docs</a></li>
                        <li><a class="dropdown-item" href="https://openpdf.com/lp/edit-pdf.html">Online PDF editor</a>
                        </li>
                        <li><a class="dropdown-item" href="#collapseThree" data-bs-toggle="collapse"
                                data-bs-target="#collapseThree" aria-expanded="false" aria-controls="collapseThree">Your
                                custom HTML Notepad</a></li>
                    </ul>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#collapseTwo" data-bs-toggle="collapse" data-bs-target="#collapseTwo"
                        aria-expanded="false" aria-controls="collapseTwo">Lista de Objetivos</a>
                </li>
            </ul>
        </section>
    </nav>
    <section class="accordion" id="accordionExample">
        <section class="accordion-item">
            <h2 class="accordion-header" id="headingOne">
                <button class="accordion-button" type="button" data-bs-toggle="collapse" data-bs-target="#collapseOne"
                    aria-expanded="true" aria-controls="collapseOne">
                    Pomodoro Counter
                </button>
            </h2>
            <section id="collapseOne" class="accordion-collapse collapse show" aria-labelledby="headingOne"
                data-bs-parent="#accordionExample">
                <section class="accordion-body">
                    This is where the pomodoro counter lives
                </section>
            </section>
        </section>
        <section class="accordion-item">
            <h2 class="accordion-header" id="headingTwo">
                <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse"
                    data-bs-target="#collapseTwo" aria-expanded="false" aria-controls="collapseTwo">
                    Lista de Objetivos
                </button>
            </h2>
            <section id="collapseTwo" class="accordion-collapse collapse" aria-labelledby="headingTwo"
                data-bs-parent="#accordionExample">
                <section class="accordion-body">
                    This is where the lista de objetivos lives
                </section>
            </section>
        </section>
        <section class="accordion-item">
            <h2 class="accordion-header" id="headingThree">
                <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse"
                    data-bs-target="#collapseThree" aria-expanded="false" aria-controls="collapseThree">
                    Your Custom HTML Notepad
                </button>
            </h2>
            <section id="collapseThree" class="accordion-collapse collapse" aria-labelledby="headingThree"
                data-bs-parent="#accordionExample">
                <section class="accordion-body">
                    <form style="padding: 5px;">


                        <fieldset >
                            <button type="button" class="btn btn-light"
                                onclick="document.execCommand('italic',false,null);"
                                title="Italicize Highlighted Text"><i>I</i>
                            </button>
                            <button type="button" class="btn btn-light"
                                onclick="document.execCommand( 'bold',false,null);"
                                title="Bold Highlighted Text"><b>B</b>
                            </button>
                            <button type="button" class="btn btn-light"
                                onclick="document.execCommand( 'underline',false,null);"
                                title='Underline Highlighted Text'><u>U</u>
                            </button>
                            <section class="btn-group" role="group">
                                <button id="btnGroupDrop1" type="button" class="btn btn-light dropdown-toggle"
                                    data-bs-toggle="dropdown" aria-expanded="false">
                                    Save
                                </button>
                                <ul class="dropdown-menu" aria-labelledby="btnGroupDrop1">
                                    <li><a class="dropdown-item" href="#">Download file</a></li>
                                    <li><a class="dropdown-item" href="#">Save to LocalStorage</a></li>
                                </ul>
                            </section>
                        </fieldset>
                        <fieldset id="editor" contenteditable="true"
                            style="border: 2px solid black; border-radius:15px; min-height: 200px; padding:10px; margin-top:5px;">
                            Some text...
                        </fieldset>



                    </form>
                    <br>

                </section>
            </section>
        </section>
    </section>
</body>

</html>

``` 


We only need to add functionality for the "save" feature, to consider the notepad as "completed". but for now we will stop here.

Take a good rest (so far you have had to type many lines, enjoy being a programmer)

---

The next step is to create our "Lista de Objetivos", 

A High-Level explanation: 

- We will create a `<form>`, along one `<input>` and a button 

Compare your code with the following and update accordingly.

```html

<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.1/dist/css/bootstrap.min.css" rel="stylesheet">
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.1/dist/js/bootstrap.bundle.min.js"></script>
    <title>App my Studies tool</title>

    <style>
        textarea {
            width: 100%;
            height: 150px;
            padding: 12px 20px;
            box-sizing: border-box;
            border: 2px solid #ccc;
            border-radius: 4px;
            background-color: #f8f8f8;
            font-size: 16px;
            resize: none;
        }
    </style>
</head>

<body>
    <!-- A grey horizontal navbar that becomes vertical on small screens -->
    <nav class="navbar navbar-expand-sm bg-light">
        <section class="container-fluid">
            <!-- Links -->
            <ul class="navbar-nav">
                <li class="nav-item">
                    <a target="_blank" href="https://www.google.com/">
                        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/2f/Google_2015_logo.svg/272px-Google_2015_logo.svg.png"
                            alt="Google" style="max-height: 40px">
                    </a>
                </li>
                <li class="nav-link">
                    <a target="_blank" href="https://calendar.google.com/calendar"><img style="max-height: 40px"
                            src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/a5/Google_Calendar_icon_%282020%29.svg/2048px-Google_Calendar_icon_%282020%29.svg.png"
                            alt="Google Calendar" height="75" /> </a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#collapseOne" data-bs-toggle="collapse" data-bs-target="#collapseOne"
                        aria-expanded="true" aria-controls="collapseOne">Pomodoro Counter</a>
                </li>
                <li class="nav-item dropdown">
                    <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown">Escribir</a>
                    <ul class="dropdown-menu">
                        <li><a class="dropdown-item" href="https://docs.google.com/">Google Docs</a></li>
                        <li><a class="dropdown-item" href="https://openpdf.com/lp/edit-pdf.html">Online PDF editor</a>
                        </li>
                        <li><a class="dropdown-item" href="#collapseThree" data-bs-toggle="collapse"
                                data-bs-target="#collapseThree" aria-expanded="false" aria-controls="collapseThree">Your
                                custom HTML Notepad</a></li>
                    </ul>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#collapseTwo" data-bs-toggle="collapse" data-bs-target="#collapseTwo"
                        aria-expanded="false" aria-controls="collapseTwo">Lista de Objetivos</a>
                </li>
            </ul>
        </section>
    </nav>
    <section class="accordion" id="accordionExample">
        <section class="accordion-item">
            <h2 class="accordion-header" id="headingOne">
                <button class="accordion-button" type="button" data-bs-toggle="collapse" data-bs-target="#collapseOne"
                    aria-expanded="true" aria-controls="collapseOne">
                    Pomodoro Counter
                </button>
            </h2>
            <section id="collapseOne" class="accordion-collapse collapse show" aria-labelledby="headingOne"
                data-bs-parent="#accordionExample">
                <section class="accordion-body">
                    This is where the pomodoro counter lives
                </section>
            </section>
        </section>
        <section class="accordion-item">
            <h2 class="accordion-header" id="headingTwo">
                <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse"
                    data-bs-target="#collapseTwo" aria-expanded="false" aria-controls="collapseTwo">
                    Lista de Objetivos
                </button>
            </h2>
            <section id="collapseTwo" class="accordion-collapse collapse" aria-labelledby="headingTwo"
                data-bs-parent="#accordionExample">
                <section class="accordion-body">
                    <form>                
                        <section class="mb-1" style="max-width:50%;">
                            <label for="inputObjetivos" class="form-label">Nuevo Objetivo</label>
                            <input type="text" class="form-control" id="inputObjetivos">
                        </section>
                        <button type="submit" class="btn btn-primary">Añadir</button>
                    </form>
                </section>
            </section>
        </section>
        <section class="accordion-item">
            <h2 class="accordion-header" id="headingThree">
                <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse"
                    data-bs-target="#collapseThree" aria-expanded="false" aria-controls="collapseThree">
                    Your Custom HTML Notepad
                </button>
            </h2>
            <section id="collapseThree" class="accordion-collapse collapse" aria-labelledby="headingThree"
                data-bs-parent="#accordionExample">
                <section class="accordion-body">
                    <form style="padding: 5px;">


                        <fieldset>
                            <button type="button" class="btn btn-light"
                                onclick="document.execCommand('italic',false,null);"
                                title="Italicize Highlighted Text"><i>I</i>
                            </button>
                            <button type="button" class="btn btn-light"
                                onclick="document.execCommand( 'bold',false,null);"
                                title="Bold Highlighted Text"><b>B</b>
                            </button>
                            <button type="button" class="btn btn-light"
                                onclick="document.execCommand( 'underline',false,null);"
                                title='Underline Highlighted Text'><u>U</u>
                            </button>
                            <section class="btn-group" role="group">
                                <button id="btnGroupDrop1" type="button" class="btn btn-light dropdown-toggle"
                                    data-bs-toggle="dropdown" aria-expanded="false">
                                    Save
                                </button>
                                <ul class="dropdown-menu" aria-labelledby="btnGroupDrop1">
                                    <li><a class="dropdown-item" href="#">Download file</a></li>
                                    <li><a class="dropdown-item" href="#">Save to LocalStorage</a></li>
                                </ul>
                            </section>
                        </fieldset>
                        <fieldset id="editor" contenteditable="true"
                            style="border: 2px solid black; border-radius:15px; min-height: 200px; padding:10px; margin-top:5px;">
                            Some text...
                        </fieldset>



                    </form>
                    <br>

                </section>
            </section>
        </section>
    </section>
</body>

</html>

```



- We will show the "objetivos" once one has been created. Note that we are also adding some JavaScript for creating the element and for adding an "Event Listener" to each newly created "objetivo" to deletet it, later we will make it better, and add functionality for editing each "objetivo", etc

Compare your code with the following and update accordingly.

```html

<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.1/dist/css/bootstrap.min.css" rel="stylesheet">
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.1/dist/js/bootstrap.bundle.min.js"></script>
    <title>App my Studies tool</title>

    <style>
        textarea {
            width: 100%;
            height: 150px;
            padding: 12px 20px;
            box-sizing: border-box;
            border: 2px solid #ccc;
            border-radius: 4px;
            background-color: #f8f8f8;
            font-size: 16px;
            resize: none;
        }
    </style>
</head>

<body>
    <!-- A grey horizontal navbar that becomes vertical on small screens -->
    <nav class="navbar navbar-expand-sm bg-light">
        <section class="container-fluid">
            <!-- Links -->
            <ul class="navbar-nav">
                <li class="nav-item">
                    <a target="_blank" href="https://www.google.com/">
                        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/2f/Google_2015_logo.svg/272px-Google_2015_logo.svg.png"
                            alt="Google" style="max-height: 40px">
                    </a>
                </li>
                <li class="nav-link">
                    <a target="_blank" href="https://calendar.google.com/calendar"><img style="max-height: 40px"
                            src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/a5/Google_Calendar_icon_%282020%29.svg/2048px-Google_Calendar_icon_%282020%29.svg.png"
                            alt="Google Calendar" height="75" /> </a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#collapseOne" data-bs-toggle="collapse" data-bs-target="#collapseOne"
                        aria-expanded="true" aria-controls="collapseOne">Pomodoro Counter</a>
                </li>
                <li class="nav-item dropdown">
                    <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown">Escribir</a>
                    <ul class="dropdown-menu">
                        <li><a class="dropdown-item" href="https://docs.google.com/">Google Docs</a></li>
                        <li><a class="dropdown-item" href="https://openpdf.com/lp/edit-pdf.html">Online PDF editor</a>
                        </li>
                        <li><a class="dropdown-item" href="#collapseThree" data-bs-toggle="collapse"
                                data-bs-target="#collapseThree" aria-expanded="false" aria-controls="collapseThree">Your
                                custom HTML Notepad</a></li>
                    </ul>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#collapseTwo" data-bs-toggle="collapse" data-bs-target="#collapseTwo"
                        aria-expanded="false" aria-controls="collapseTwo">Lista de Objetivos</a>
                </li>
            </ul>
        </section>
    </nav>
    <section class="accordion" id="accordionExample">
        <section class="accordion-item">
            <h2 class="accordion-header" id="headingOne">
                <button class="accordion-button" type="button" data-bs-toggle="collapse" data-bs-target="#collapseOne"
                    aria-expanded="true" aria-controls="collapseOne">
                    Pomodoro Counter
                </button>
            </h2>
            <section id="collapseOne" class="accordion-collapse collapse show" aria-labelledby="headingOne"
                data-bs-parent="#accordionExample">
                <section class="accordion-body">
                    This is where the pomodoro counter lives
                </section>
            </section>
        </section>
        <section class="accordion-item">
            <h2 class="accordion-header" id="headingTwo">
                <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse"
                    data-bs-target="#collapseTwo" aria-expanded="false" aria-controls="collapseTwo">
                    Lista de Objetivos
                </button>
            </h2>
            <section id="collapseTwo" class="accordion-collapse collapse" aria-labelledby="headingTwo"
                data-bs-parent="#accordionExample">
                <section class="accordion-body" id="listaObjetivos">
                    <form>
                        <section class="mb-1" style="max-width:50%;">
                            <label for="inputObjetivos" class="form-label">Nuevo Objetivo</label>
                            <input type="text" class="form-control" id="inputObjetivos">
                        </section>
                        <button type="submit" class="btn btn-primary" onclick="crearNuevoObjetivo()">Añadir</button>


                        <script>

                            let objetivos = [];
                            let counter = 0;

                            function crearNuevoObjetivo() {
                                let nuevoObjetivo = document.createElement('p');
                                nuevoObjetivo.innerText = inputObjetivos.value;
                                nuevoObjetivo.style.margin = "5px";
                                objetivos.push(nuevoObjetivo.innerText);
                                nuevoObjetivo.id = counter;
                                counter++;
                                listaObjetivos.appendChild(nuevoObjetivo);
                                inputObjetivos.value = "";
                                nuevoObjetivo.addEventListener("click", () => {
                                    listaObjetivos.removeChild(nuevoObjetivo)
                                })
                            }
                        </script>
                    </form>
                </section>
            </section>
        </section>
        <section class="accordion-item">
            <h2 class="accordion-header" id="headingThree">
                <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse"
                    data-bs-target="#collapseThree" aria-expanded="false" aria-controls="collapseThree">
                    Your Custom HTML Notepad
                </button>
            </h2>
            <section id="collapseThree" class="accordion-collapse collapse" aria-labelledby="headingThree"
                data-bs-parent="#accordionExample">
                <section class="accordion-body">
                    <form style="padding: 5px;">


                        <fieldset>
                            <button type="button" class="btn btn-light"
                                onclick="document.execCommand('italic',false,null);"
                                title="Italicize Highlighted Text"><i>I</i>
                            </button>
                            <button type="button" class="btn btn-light"
                                onclick="document.execCommand( 'bold',false,null);"
                                title="Bold Highlighted Text"><b>B</b>
                            </button>
                            <button type="button" class="btn btn-light"
                                onclick="document.execCommand( 'underline',false,null);"
                                title='Underline Highlighted Text'><u>U</u>
                            </button>
                            <section class="btn-group" role="group">
                                <button id="btnGroupDrop1" type="button" class="btn btn-light dropdown-toggle"
                                    data-bs-toggle="dropdown" aria-expanded="false">
                                    Save
                                </button>
                                <ul class="dropdown-menu" aria-labelledby="btnGroupDrop1">
                                    <li><a class="dropdown-item" href="#">Download file</a></li>
                                    <li><a class="dropdown-item" href="#">Save to LocalStorage</a></li>
                                </ul>
                            </section>
                        </fieldset>
                        <fieldset id="editor" contenteditable="true"
                            style="border: 2px solid black; border-radius:15px; min-height: 200px; padding:10px; margin-top:5px;">
                            Some text...
                        </fieldset>



                    </form>
                    <br>

                </section>
            </section>
        </section>
    </section>
</body>

</html>

``` 
---

Now we will introduce a bigger chunk ofJavascript. Is recommended but not required, to have read  https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/JavaScript_basics_started_with_the_web


As stated before we will include at first everything inside our index.html file.

Now take break again. Use you web a little bit an try to connect how everything is working.

Investigate what is the "Pomodoro technique".

---

After the break, let's implement the pomodoro counter.

In the next example only the HTML will change

```html

<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.1/dist/css/bootstrap.min.css" rel="stylesheet">
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.1/dist/js/bootstrap.bundle.min.js"></script>
    <title>App my Studies tool</title>

    <style>
        textarea {
            width: 100%;
            height: 150px;
            padding: 12px 20px;
            box-sizing: border-box;
            border: 2px solid #ccc;
            border-radius: 4px;
            background-color: #f8f8f8;
            font-size: 16px;
            resize: none;
        }
    </style>
</head>

<body>
    <!-- A grey horizontal navbar that becomes vertical on small screens -->
    <nav class="navbar navbar-expand-sm bg-light">
        <section class="container-fluid">
            <!-- Links -->
            <ul class="navbar-nav">
                <li class="nav-item">
                    <a target="_blank" href="https://www.google.com/">
                        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/2f/Google_2015_logo.svg/272px-Google_2015_logo.svg.png"
                            alt="Google" style="max-height: 40px">
                    </a>
                </li>
                <li class="nav-link">
                    <a target="_blank" href="https://calendar.google.com/calendar"><img style="max-height: 40px"
                            src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/a5/Google_Calendar_icon_%282020%29.svg/2048px-Google_Calendar_icon_%282020%29.svg.png"
                            alt="Google Calendar" height="75" /> </a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#collapseOne" data-bs-toggle="collapse" data-bs-target="#collapseOne"
                        aria-expanded="true" aria-controls="collapseOne">Pomodoro Counter</a>
                </li>
                <li class="nav-item dropdown">
                    <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown">Escribir</a>
                    <ul class="dropdown-menu">
                        <li><a class="dropdown-item" href="https://docs.google.com/">Google Docs</a></li>
                        <li><a class="dropdown-item" href="https://openpdf.com/lp/edit-pdf.html">Online PDF editor</a>
                        </li>
                        <li><a class="dropdown-item" href="#collapseThree" data-bs-toggle="collapse"
                                data-bs-target="#collapseThree" aria-expanded="false" aria-controls="collapseThree">Your
                                custom HTML Notepad</a></li>
                    </ul>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#collapseTwo" data-bs-toggle="collapse" data-bs-target="#collapseTwo"
                        aria-expanded="false" aria-controls="collapseTwo">Lista de Objetivos</a>
                </li>
            </ul>
        </section>
    </nav>
    <section class="accordion" id="accordionExample">
        <section class="accordion-item">
            <h2 class="accordion-header" id="headingOne">
                <button class="accordion-button" type="button" data-bs-toggle="collapse" data-bs-target="#collapseOne"
                    aria-expanded="true" aria-controls="collapseOne">
                    Pomodoro Counter
                </button>
            </h2>
            <section id="collapseOne" class="accordion-collapse collapse show" aria-labelledby="headingOne"
                data-bs-parent="#accordionExample">
                <section class="accordion-body">
                    <section id="pomodoro-app">
                        <section id="container">
                          <section id="timer">
                            <section id="time">
                              <span id="minutes">25</span>
                              <span id="colon">:</span>
                              <span id="seconds">00</span>
                            </section>
                            <section id="filler"></section>
                          </section>
                      
                          <section id="buttons">
                            <button id="work">Work</button>
                            <button id="shortBreak">Short Break</button>
                            <button id="longBreak">Long Break</button>
                            <button id="stop">Stop</button>
                          </section>
                        </section>
                      </section>
                </section>
            </section>
        </section>
        <section class="accordion-item">
            <h2 class="accordion-header" id="headingTwo">
                <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse"
                    data-bs-target="#collapseTwo" aria-expanded="false" aria-controls="collapseTwo">
                    Lista de Objetivos
                </button>
            </h2>
            <section id="collapseTwo" class="accordion-collapse collapse" aria-labelledby="headingTwo"
                data-bs-parent="#accordionExample">
                <section class="accordion-body" id="listaObjetivos">
                    <form id="objetivosForm">
                        <section class="mb-1" style="max-width:50%;">
                            <label for="inputObjetivos" class="form-label">Nuevo Objetivo</label>
                            <input type="text" class="form-control" id="inputObjetivos">
                        </section>
                        <button type="submit" class="btn btn-primary">Añadir</button>


                        <script>
                            //Added this event listener due to form reloading page
                            objetivosForm.addEventListener('submit', (event)=>{
                                event.preventDefault();
                                return crearNuevoObjetivo();
                            })
                            let objetivos = [];
                            let counter = 0;



                            function crearNuevoObjetivo() {
                                
                                let nuevoObjetivo = document.createElement('p');
                                nuevoObjetivo.innerText = inputObjetivos.value;
                                nuevoObjetivo.style.margin = "5px";
                                objetivos.push(nuevoObjetivo.innerText);
                                nuevoObjetivo.id = counter;
                                counter++;
                                listaObjetivos.appendChild(nuevoObjetivo);
                                inputObjetivos.value = "";
                                nuevoObjetivo.addEventListener("click", () => {
                                    listaObjetivos.removeChild(nuevoObjetivo)
                                })
                            }
                        </script>
                    </form>
                </section>
            </section>
        </section>
        <section class="accordion-item">
            <h2 class="accordion-header" id="headingThree">
                <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse"
                    data-bs-target="#collapseThree" aria-expanded="false" aria-controls="collapseThree">
                    Your Custom HTML Notepad
                </button>
            </h2>
            <section id="collapseThree" class="accordion-collapse collapse" aria-labelledby="headingThree"
                data-bs-parent="#accordionExample">
                <section class="accordion-body">
                    <form style="padding: 5px;">


                        <fieldset>
                            <button type="button" class="btn btn-light"
                                onclick="document.execCommand('italic',false,null);"
                                title="Italicize Highlighted Text"><i>I</i>
                            </button>
                            <button type="button" class="btn btn-light"
                                onclick="document.execCommand( 'bold',false,null);"
                                title="Bold Highlighted Text"><b>B</b>
                            </button>
                            <button type="button" class="btn btn-light"
                                onclick="document.execCommand( 'underline',false,null);"
                                title='Underline Highlighted Text'><u>U</u>
                            </button>
                            <section class="btn-group" role="group">
                                <button id="btnGroupDrop1" type="button" class="btn btn-light dropdown-toggle"
                                    data-bs-toggle="dropdown" aria-expanded="false">
                                    Save
                                </button>
                                <ul class="dropdown-menu" aria-labelledby="btnGroupDrop1">
                                    <li><a class="dropdown-item" href="#">Download file</a></li>
                                    <li><a class="dropdown-item" href="#">Save to LocalStorage</a></li>
                                </ul>
                            </section>
                        </fieldset>
                        <fieldset id="editor" contenteditable="true"
                            style="border: 2px solid black; border-radius:15px; min-height: 200px; padding:10px; margin-top:5px;">
                            Some text...
                        </fieldset>



                    </form>
                    <br>

                </section>
            </section>
        </section>
    </section>
</body>

</html>

```
Now we add the CSS 

```html

<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.1/dist/css/bootstrap.min.css" rel="stylesheet">
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.1/dist/js/bootstrap.bundle.min.js"></script>
    <title>App my Studies tool</title>

    <style>
        textarea {
            width: 100%;
            height: 150px;
            padding: 12px 20px;
            box-sizing: border-box;
            border: 2px solid #ccc;
            border-radius: 4px;
            background-color: #f8f8f8;
            font-size: 16px;
            resize: none;
        }
    </style>
</head>

<body>
    <!-- A grey horizontal navbar that becomes vertical on small screens -->
    <nav class="navbar navbar-expand-sm bg-light">
        <section class="container-fluid">
            <!-- Links -->
            <ul class="navbar-nav">
                <li class="nav-item">
                    <a target="_blank" href="https://www.google.com/">
                        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/2f/Google_2015_logo.svg/272px-Google_2015_logo.svg.png"
                            alt="Google" style="max-height: 40px">
                    </a>
                </li>
                <li class="nav-link">
                    <a target="_blank" href="https://calendar.google.com/calendar"><img style="max-height: 40px"
                            src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/a5/Google_Calendar_icon_%282020%29.svg/2048px-Google_Calendar_icon_%282020%29.svg.png"
                            alt="Google Calendar" height="75" /> </a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#collapseOne" data-bs-toggle="collapse" data-bs-target="#collapseOne"
                        aria-expanded="true" aria-controls="collapseOne">Pomodoro Counter</a>
                </li>
                <li class="nav-item dropdown">
                    <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown">Escribir</a>
                    <ul class="dropdown-menu">
                        <li><a class="dropdown-item" href="https://docs.google.com/">Google Docs</a></li>
                        <li><a class="dropdown-item" href="https://openpdf.com/lp/edit-pdf.html">Online PDF editor</a>
                        </li>
                        <li><a class="dropdown-item" href="#collapseThree" data-bs-toggle="collapse"
                                data-bs-target="#collapseThree" aria-expanded="false" aria-controls="collapseThree">Your
                                custom HTML Notepad</a></li>
                    </ul>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#collapseTwo" data-bs-toggle="collapse" data-bs-target="#collapseTwo"
                        aria-expanded="false" aria-controls="collapseTwo">Lista de Objetivos</a>
                </li>
            </ul>
        </section>
    </nav>
    <section class="accordion" id="accordionExample">
        <section class="accordion-item">
            <h2 class="accordion-header" id="headingOne">
                <button class="accordion-button" type="button" data-bs-toggle="collapse" data-bs-target="#collapseOne"
                    aria-expanded="true" aria-controls="collapseOne">
                    Pomodoro Counter
                </button>
            </h2>
            <section id="collapseOne" class="accordion-collapse collapse show" aria-labelledby="headingOne"
                data-bs-parent="#accordionExample">
                <section class="accordion-body">
                    <style>
                        #container {
                            border: 1px solid #333;
                            border-radius: 20px;
                            width: 400px;
                            margin: 20px auto;
                            padding: 20px;
                            text-align: center;
                            background: #333;
                        }

                        #timer {
                            color: #f00;
                            font-size: 50px;
                            margin: 10px auto;
                            border: 5px solid red;
                            border-radius: 50%;
                            width: 200px;
                            height: 200px;
                            overflow: hidden;
                            position: relative;
                            -webkit-user-select: none;
                            -moz-user-select: none;
                            -ms-user-select: none;
                            user-select: none;
                            cursor: default;
                        }

                        #time {
                            margin-top: 70px;
                            z-index: 1;
                            position: relative;
                        }

                        #filler {
                            background: #ddffcc;
                            height: 0px;
                            width: 200px;
                            position: absolute;
                            bottom: 0;
                        }

                        #buttons button {
                            background: #4da6ff;
                            border: none;
                            color: #fff;
                            cursor: pointer;
                            padding: 5px;
                            width: 90px;
                            margin: 10px auto;
                            font-size: 14px;
                            height: 50px;
                            border-radius: 50px;
                        }

                        #buttons button#shortBreak {
                            background: #0c0;
                        }

                        #buttons button#longBreak {
                            background: #080;
                        }

                        #buttons button#stop {
                            background: #f00;
                        }
                    </style>
                    <section id="pomodoro-app">
                        <section id="container">
                            <section id="timer">
                                <section id="time">
                                    <span id="minutes">25</span>
                                    <span id="colon">:</span>
                                    <span id="seconds">00</span>
                                </section>
                                <section id="filler"></section>
                            </section>

                            <section id="buttons">
                                <button id="work">Work</button>
                                <button id="shortBreak">Short Break</button>
                                <button id="longBreak">Long Break</button>
                                <button id="stop">Stop</button>
                            </section>
                        </section>
                    </section>
                </section>
            </section>
        </section>
        <section class="accordion-item">
            <h2 class="accordion-header" id="headingTwo">
                <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse"
                    data-bs-target="#collapseTwo" aria-expanded="false" aria-controls="collapseTwo">
                    Lista de Objetivos
                </button>
            </h2>
            <section id="collapseTwo" class="accordion-collapse collapse" aria-labelledby="headingTwo"
                data-bs-parent="#accordionExample">
                <section class="accordion-body" id="listaObjetivos">
                    <form id="objetivosForm">
                        <section class="mb-1" style="max-width:50%;">
                            <label for="inputObjetivos" class="form-label">Nuevo Objetivo</label>
                            <input type="text" class="form-control" id="inputObjetivos">
                        </section>
                        <button type="submit" class="btn btn-primary">Añadir</button>


                        <script>
                            //Added this event listener due to form reloading page
                            objetivosForm.addEventListener('submit', (event) => {
                                event.preventDefault();
                                return crearNuevoObjetivo();
                            })
                            let objetivos = [];
                            let counter = 0;



                            function crearNuevoObjetivo() {

                                let nuevoObjetivo = document.createElement('p');
                                nuevoObjetivo.innerText = inputObjetivos.value;
                                nuevoObjetivo.style.margin = "5px";
                                objetivos.push(nuevoObjetivo.innerText);
                                nuevoObjetivo.id = counter;
                                counter++;
                                listaObjetivos.appendChild(nuevoObjetivo);
                                inputObjetivos.value = "";
                                nuevoObjetivo.addEventListener("click", () => {
                                    listaObjetivos.removeChild(nuevoObjetivo)
                                })
                            }
                        </script>
                    </form>
                </section>
            </section>
        </section>
        <section class="accordion-item">
            <h2 class="accordion-header" id="headingThree">
                <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse"
                    data-bs-target="#collapseThree" aria-expanded="false" aria-controls="collapseThree">
                    Your Custom HTML Notepad
                </button>
            </h2>
            <section id="collapseThree" class="accordion-collapse collapse" aria-labelledby="headingThree"
                data-bs-parent="#accordionExample">
                <section class="accordion-body">
                    <form style="padding: 5px;">


                        <fieldset>
                            <button type="button" class="btn btn-light"
                                onclick="document.execCommand('italic',false,null);"
                                title="Italicize Highlighted Text"><i>I</i>
                            </button>
                            <button type="button" class="btn btn-light"
                                onclick="document.execCommand( 'bold',false,null);"
                                title="Bold Highlighted Text"><b>B</b>
                            </button>
                            <button type="button" class="btn btn-light"
                                onclick="document.execCommand( 'underline',false,null);"
                                title='Underline Highlighted Text'><u>U</u>
                            </button>
                            <section class="btn-group" role="group">
                                <button id="btnGroupDrop1" type="button" class="btn btn-light dropdown-toggle"
                                    data-bs-toggle="dropdown" aria-expanded="false">
                                    Save
                                </button>
                                <ul class="dropdown-menu" aria-labelledby="btnGroupDrop1">
                                    <li><a class="dropdown-item" href="#">Download file</a></li>
                                    <li><a class="dropdown-item" href="#">Save to LocalStorage</a></li>
                                </ul>
                            </section>
                        </fieldset>
                        <fieldset id="editor" contenteditable="true"
                            style="border: 2px solid black; border-radius:15px; min-height: 200px; padding:10px; margin-top:5px;">
                            Some text...
                        </fieldset>



                    </form>
                    <br>

                </section>
            </section>
        </section>
    </section>
</body>

</html>

```

And now the Javascript necessary to make the Pomodoro counter work.

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.1/dist/css/bootstrap.min.css" rel="stylesheet">
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.1/dist/js/bootstrap.bundle.min.js"></script>
    <title>App my Studies tool</title>

    <style>
        textarea {
            width: 100%;
            height: 150px;
            padding: 12px 20px;
            box-sizing: border-box;
            border: 2px solid #ccc;
            border-radius: 4px;
            background-color: #f8f8f8;
            font-size: 16px;
            resize: none;
        }
    </style>
</head>

<body>
    <!-- A grey horizontal navbar that becomes vertical on small screens -->
    <nav class="navbar navbar-expand-sm bg-light">
        <section class="container-fluid">
            <!-- Links -->
            <ul class="navbar-nav">
                <li class="nav-item">
                    <a target="_blank" href="https://www.google.com/">
                        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/2f/Google_2015_logo.svg/272px-Google_2015_logo.svg.png"
                            alt="Google" style="max-height: 40px">
                    </a>
                </li>
                <li class="nav-link">
                    <a target="_blank" href="https://calendar.google.com/calendar"><img style="max-height: 40px"
                            src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/a5/Google_Calendar_icon_%282020%29.svg/2048px-Google_Calendar_icon_%282020%29.svg.png"
                            alt="Google Calendar" height="75" /> </a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#collapseOne" data-bs-toggle="collapse" data-bs-target="#collapseOne"
                        aria-expanded="true" aria-controls="collapseOne">Pomodoro Counter</a>
                </li>
                <li class="nav-item dropdown">
                    <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown">Escribir</a>
                    <ul class="dropdown-menu">
                        <li><a class="dropdown-item" href="https://docs.google.com/">Google Docs</a></li>
                        <li><a class="dropdown-item" href="https://openpdf.com/lp/edit-pdf.html">Online PDF editor</a>
                        </li>
                        <li><a class="dropdown-item" href="#collapseThree" data-bs-toggle="collapse"
                                data-bs-target="#collapseThree" aria-expanded="false" aria-controls="collapseThree">Your
                                custom HTML Notepad</a></li>
                    </ul>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#collapseTwo" data-bs-toggle="collapse" data-bs-target="#collapseTwo"
                        aria-expanded="false" aria-controls="collapseTwo">Lista de Objetivos</a>
                </li>
            </ul>
        </section>
    </nav>
    <section class="accordion" id="accordionExample">
        <section class="accordion-item">
            <h2 class="accordion-header" id="headingOne">
                <button class="accordion-button" type="button" data-bs-toggle="collapse" data-bs-target="#collapseOne"
                    aria-expanded="true" aria-controls="collapseOne">
                    Pomodoro Counter
                </button>
            </h2>
            <section id="collapseOne" class="accordion-collapse collapse show" aria-labelledby="headingOne"
                data-bs-parent="#accordionExample">
                <section class="accordion-body">
                    <style>
                        #container {
                            border: 1px solid #333;
                            border-radius: 20px;
                            width: 400px;
                            margin: 20px auto;
                            padding: 20px;
                            text-align: center;
                            background: #333;
                        }

                        #timer {
                            color: #f00;
                            font-size: 50px;
                            margin: 10px auto;
                            border: 5px solid red;
                            border-radius: 50%;
                            width: 200px;
                            height: 200px;
                            overflow: hidden;
                            position: relative;
                            -webkit-user-select: none;
                            -moz-user-select: none;
                            -ms-user-select: none;
                            user-select: none;
                            cursor: default;
                        }

                        #time {
                            margin-top: 70px;
                            z-index: 1;
                            position: relative;
                        }

                        #filler {
                            background: #ddffcc;
                            height: 0px;
                            width: 200px;
                            position: absolute;
                            bottom: 0;
                        }

                        #buttons button {
                            background: #4da6ff;
                            border: none;
                            color: #fff;
                            cursor: pointer;
                            padding: 5px;
                            width: 90px;
                            margin: 10px auto;
                            font-size: 14px;
                            height: 50px;
                            border-radius: 50px;
                        }

                        #buttons button#shortBreak {
                            background: #0c0;
                        }

                        #buttons button#longBreak {
                            background: #080;
                        }

                        #buttons button#stop {
                            background: #f00;
                        }
                    </style>
                    <section id="pomodoro-app">
                        <section id="container">
                            <section id="timer">
                                <section id="time">
                                    <span id="minutes">25</span>
                                    <span id="colon">:</span>
                                    <span id="seconds">00</span>
                                </section>
                                <section id="filler"></section>
                            </section>

                            <section id="buttons">
                                <button id="work">Work</button>
                                <button id="shortBreak">Short Break</button>
                                <button id="longBreak">Long Break</button>
                                <button id="stop">Stop</button>
                            </section>
                        </section>
                    </section>
                    <script>
                        var pomodoro = {
                            started: false,
                            minutes: 0,
                            seconds: 0,
                            fillerHeight: 0,
                            fillerIncrement: 0,
                            interval: null,
                            minutesDom: null,
                            secondsDom: null,
                            fillerDom: null,
                            init: function () {
                                var self = this;
                                this.minutesDom = document.querySelector('#minutes');
                                this.secondsDom = document.querySelector('#seconds');
                                this.fillerDom = document.querySelector('#filler');
                                this.interval = setInterval(function () {
                                    self.intervalCallback.apply(self);
                                }, 1000);
                                document.querySelector('#work').onclick = function () {
                                    self.startWork.apply(self);
                                };
                                document.querySelector('#shortBreak').onclick = function () {
                                    self.startShortBreak.apply(self);
                                };
                                document.querySelector('#longBreak').onclick = function () {
                                    self.startLongBreak.apply(self);
                                };
                                document.querySelector('#stop').onclick = function () {
                                    self.stopTimer.apply(self);
                                };
                            },
                            resetVariables: function (mins, secs, started) {
                                this.minutes = mins;
                                this.seconds = secs;
                                this.started = started;
                                this.fillerIncrement = 200 / (this.minutes * 60);
                                this.fillerHeight = 0;
                            },
                            startWork: function () {
                                this.resetVariables(25, 0, true);
                            },
                            startShortBreak: function () {
                                this.resetVariables(5, 0, true);
                            },
                            startLongBreak: function () {
                                this.resetVariables(15, 0, true);
                            },
                            stopTimer: function () {
                                this.resetVariables(25, 0, false);
                                this.updateDom();
                            },
                            toDoubleDigit: function (num) {
                                if (num < 10) {
                                    return "0" + parseInt(num, 10);
                                }
                                return num;
                            },
                            updateDom: function () {
                                this.minutesDom.innerHTML = this.toDoubleDigit(this.minutes);
                                this.secondsDom.innerHTML = this.toDoubleDigit(this.seconds);
                                this.fillerHeight = this.fillerHeight + this.fillerIncrement;
                                this.fillerDom.style.height = this.fillerHeight + 'px';
                            },
                            intervalCallback: function () {
                                if (!this.started) return false;
                                if (this.seconds == 0) {
                                    if (this.minutes == 0) {
                                        this.timerComplete();
                                        return;
                                    }
                                    this.seconds = 59;
                                    this.minutes--;
                                } else {
                                    this.seconds--;
                                }
                                this.updateDom();
                            },
                            timerComplete: function () {
                                this.started = false;
                                this.fillerHeight = 0;
                            }
                        };
                        window.onload = function () {
                            pomodoro.init();
                        };
                    </script>
                </section>
            </section>
        </section>
        <section class="accordion-item">
            <h2 class="accordion-header" id="headingTwo">
                <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse"
                    data-bs-target="#collapseTwo" aria-expanded="false" aria-controls="collapseTwo">
                    Lista de Objetivos
                </button>
            </h2>
            <section id="collapseTwo" class="accordion-collapse collapse" aria-labelledby="headingTwo"
                data-bs-parent="#accordionExample">
                <section class="accordion-body" id="listaObjetivos">
                    <form id="objetivosForm">
                        <section class="mb-1" style="max-width:50%;">
                            <label for="inputObjetivos" class="form-label">Nuevo Objetivo</label>
                            <input type="text" class="form-control" id="inputObjetivos">
                        </section>
                        <button type="submit" class="btn btn-primary">Añadir</button>


                        <script>
                            //Added this event listener due to form reloading page
                            objetivosForm.addEventListener('submit', (event) => {
                                event.preventDefault();
                                return crearNuevoObjetivo();
                            })
                            let objetivos = [];
                            let counter = 0;



                            function crearNuevoObjetivo() {

                                let nuevoObjetivo = document.createElement('p');
                                nuevoObjetivo.innerText = inputObjetivos.value;
                                nuevoObjetivo.style.margin = "5px";
                                objetivos.push(nuevoObjetivo.innerText);
                                nuevoObjetivo.id = counter;
                                counter++;
                                listaObjetivos.appendChild(nuevoObjetivo);
                                inputObjetivos.value = "";
                                nuevoObjetivo.addEventListener("click", () => {
                                    listaObjetivos.removeChild(nuevoObjetivo)
                                })
                            }
                        </script>
                    </form>
                </section>
            </section>
        </section>
        <section class="accordion-item">
            <h2 class="accordion-header" id="headingThree">
                <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse"
                    data-bs-target="#collapseThree" aria-expanded="false" aria-controls="collapseThree">
                    Your Custom HTML Notepad
                </button>
            </h2>
            <section id="collapseThree" class="accordion-collapse collapse" aria-labelledby="headingThree"
                data-bs-parent="#accordionExample">
                <section class="accordion-body">
                    <form style="padding: 5px;">


                        <fieldset>
                            <button type="button" class="btn btn-light"
                                onclick="document.execCommand('italic',false,null);"
                                title="Italicize Highlighted Text"><i>I</i>
                            </button>
                            <button type="button" class="btn btn-light"
                                onclick="document.execCommand( 'bold',false,null);"
                                title="Bold Highlighted Text"><b>B</b>
                            </button>
                            <button type="button" class="btn btn-light"
                                onclick="document.execCommand( 'underline',false,null);"
                                title='Underline Highlighted Text'><u>U</u>
                            </button>
                            <section class="btn-group" role="group">
                                <button id="btnGroupDrop1" type="button" class="btn btn-light dropdown-toggle"
                                    data-bs-toggle="dropdown" aria-expanded="false">
                                    Save
                                </button>
                                <ul class="dropdown-menu" aria-labelledby="btnGroupDrop1">
                                    <li><a class="dropdown-item" href="#">Download file</a></li>
                                    <li><a class="dropdown-item" href="#">Save to LocalStorage</a></li>
                                </ul>
                            </section>
                        </fieldset>
                        <fieldset id="editor" contenteditable="true"
                            style="border: 2px solid black; border-radius:15px; min-height: 200px; padding:10px; margin-top:5px;">
                            Some text...
                        </fieldset>



                    </form>
                    <br>

                </section>
            </section>
        </section>
    </section>
</body>

</html>

```
We now have over 300 lines of code written by ourselves!

And a final product that can help us become better programmers and students.

We will consider this tutorial as completed.

There's still some work to do on the App, but I would recommend that you first implement the App in to your learning process (you as an user) and find out what it needs to be done and where.

The first task I would recommend is to "extract" and "refactor" all the CSS and Javascript to the files mentioned at the begining. (after refactoring the app should be running)
