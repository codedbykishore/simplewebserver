# EX01 Developing a Simple Webserver
## Date:

## AIM:
To develop a simple webserver to serve html pages.

## DESIGN STEPS:
### Step 1: 
HTML content creation.

### Step 2:
Design of webserver workflow.

### Step 3:
Implementation using Python code.

### Step 4:
Serving the HTML pages.

### Step 5:
Testing the webserver.

## PROGRAM:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SEC</title>
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.3/font/bootstrap-icons.min.css">
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
    <style>
      .icon{
        color: #cc324b;
        font-size: 25px;
        border: 0px;
        padding: 10px;
      }
      i:hover{
        color: gray;
      }
      .anc{
        color: #cc324b;
      }
      .anc:hover{
        color:gray;
      }
      .bgc{
        background-color: gainsboro;
      }

    </style>
</head>
<body>
    <div class="row border border-3 bgc">
      <div class="col-7 bgc">
        <i class="bi bi-twitter icon"></i>
        <i class="bi bi-youtube icon"></i>
        <i class="bi bi-facebook icon"></i>
        <i class="bi bi-linkedin icon"></i>
        <i class="bi bi-pinterest icon"></i>
        <i class="bi bi-whatsapp icon"></i>
        <i class="bi bi-instagram icon"></i>
      </div>
      <div class="col-3 bgc">
        <nav class="navbar navbar-expand-lg">
          <div class="container-fluid">
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
              <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarSupportedContent">
              <ul class="navbar-nav me-auto mb-2 mb-lg-0">
                <li class="nav-item">
                  <a class="nav-link anc" aria-current="page" href="#">Alumni</a>
                </li>
                <li class="nav-item">
                  <a class="nav-link anc" href="#">Events</a>
                </li>
                <li class="nav-item dropdown">
                  <a class="nav-link dropdown-toggle anc" href="#" role="button" data-bs-toggle="dropdown" aria-expanded="false">
                    Department
                  </a>
                  <ul class="dropdown-menu">
                    <li><a class="dropdown-item" href="#">CSE</a></li>
                    <li><a class="dropdown-item" href="#">IT</a></li>
                    <li><a class="dropdown-item" href="#">ECE</a></li>
                    <li><a class="dropdown-item" href="#">EEE</a></li>
                    <li><a class="dropdown-item" href="#">AIML</a></li>
                    <li><a class="dropdown-item" href="#">AIDS</a></li>
                  </ul>
                </li>
            </div>
          </div>
        </nav>
      </div>
      <div class="col-2 bgc">
        <nav class="navbar">
          <div class="container-fluid">
            <form class="d-flex" role="search">
              <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search">
              <button class="btn" type="submit" style="color: #cc324b;"><i class="bi bi-search"></i></button>
            </form>
          </div>
        </nav>
      </div>
    </div>
    <div style="display: flex;">
        <div style="width: 30%;">
            <div class="list-group">
                <a href="#" class="list-group-item list-group-item-action active" aria-current="true">ADMISSION ENQUIRY</a>
                <a href="#" class="list-group-item list-group-item-action">Chat with Student Ambassador</a>
                <a href="#" class="list-group-item list-group-item-action">Blogs</a>
            </div>
        </div>
        <div style="width: 70%;">
            <div id="carouselExampleIndicators" class="carousel slide" data-bs-ride="carousel">
                <div class="carousel-indicators">
                  <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="0" class="active" aria-current="true" aria-label="Slide 1"></button>
                  <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="1" aria-label="Slide 2"></button>
                  <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="2" aria-label="Slide 3"></button>
                  <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="3" aria-label="Slide 4"></button>
                  <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="4" aria-label="Slide 1"></button>
                </div>
                <div class="carousel-inner">
                  <div class="carousel-item active" data-bs-interval="2000">
                    <img src="1.jpeg" class="d-block w-100" alt="...">
                  </div>
                  <div class="carousel-item" data-bs-interval="2000">
                    <img src="2.jpg" class="d-block w-100" alt="...">
                  </div>
                  <div class="carousel-item" data-bs-interval="2000">
                    <img src="3.jpg" class="d-block w-100" alt="...">
                  </div>
                  <div class="carousel-item" data-bs-interval="2000">
                    <img src="4.jpg" class="d-block w-100" alt="...">
                  </div>
                  <div class="carousel-item" data-bs-interval="2000">
                    <img src="5.jpg" class="d-block w-100" alt="...">
                  </div>
                </div>
                <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide="prev">
                  <span class="carousel-control-prev-icon" aria-hidden="true"></span>
                  <span class="visually-hidden">Previous</span>
                </button>
                <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide="next">
                  <span class="carousel-control-next-icon" aria-hidden="true"></span>
                  <span class="visually-hidden">Next</span>
                </button>
            </div>
        </div>
    </div>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz" crossorigin="anonymous"></script>
</body>
</html>
```
## OUTPUT:
![alt text](<Screenshot 2024-03-27 083131.png>)

## RESULT:
The program for implementing simple webserver is executed successfully.
