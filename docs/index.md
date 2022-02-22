## Simple Blog 2022

In diesem Projekt entsteht eine einfache Blog-Webseite. Es dient der Einführung in Laravel.

### Folge 0: Vorbereitungen

1. [git](https://git-scm.com/download/win) installieren
2. [Laragon](https://laragon.org/download/index.html) installieren
3. [Visual Studio Code](https://code.visualstudio.com/download) installieren
4. In VS Code github Erweiterung installieren

### Folge 1: Home-Template integrieren
Wir nutzen ein statische Bootstrap-Templates von der Seite [startbootstrap.com](startbootstrap.com). Diese werden im Folgenden in unsere Laravel-Projekt integriert.

1. [Blog-Home](https://startbootstrap.com/template/blog-home)
2. [Blog-Post](https://startbootstrap.com/template/blog-post)

Den Body von Blog-Home kopieren wir nach layouts/app.blade.php und ersetzen dabei den vorhandenen Body. Seitenkopf, Navigation und Footer bleiben unverändert, der Hauptinhaltsbereich sowie die Sidebar werden ausgelagert und eingebunden.

```markdown
<!-- Responsive navbar-->
<nav class="navbar navbar-expand-lg navbar-dark bg-dark">
    <div class="container">
        <a class="navbar-brand" href="#!">Start Bootstrap</a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation"><span class="navbar-toggler-icon"></span></button>
        <div class="collapse navbar-collapse" id="navbarSupportedContent">
            <ul class="navbar-nav ms-auto mb-2 mb-lg-0">
                <li class="nav-item"><a class="nav-link" href="#">Home</a></li>
                <li class="nav-item"><a class="nav-link" href="#!">About</a></li>
                <li class="nav-item"><a class="nav-link" href="#!">Contact</a></li>
                <li class="nav-item"><a class="nav-link active" aria-current="page" href="#">Blog</a></li>
            </ul>
        </div>
    </div>
</nav>

<!-- Page header with logo and tagline-->
<header class="py-5 bg-light border-bottom mb-4">
    <div class="container">
        <div class="text-center my-5">
            <h1 class="fw-bolder">Welcome to Blog Home!</h1>
            <p class="lead mb-0">A Bootstrap 5 starter layout for your next blog homepage</p>
        </div>
    </div>
</header>

<!-- Page content-->
<div class="container">
    <div class="row">
        <!-- Blog entries-->
        <div class="col-lg-8">
            @yield('content')
        </div>
        <!-- Side widgets-->
        <div class="col-lg-4">
            @yield('sidebar')
        </div>
    </div>
</div>

<!-- Footer-->
<footer class="py-5 bg-dark">
    <div class="container"><p class="m-0 text-center text-white">Copyright &copy; Your Website 2021</p></div>
</footer>
```        

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/mblanke70/simple-blog-2022/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
