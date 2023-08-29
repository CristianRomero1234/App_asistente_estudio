Create three folders, name them "html, js, css".

Inside directory named html, create file "index.html"
Inside directory named js, create file "main.js"
Inside directory named css, create file "style.css"

At first we will write all the code inside "index.html", then progresively move it to other files.

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
At this point we will include links to google search, google calendar, also placeholder links for other features of our web page.
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