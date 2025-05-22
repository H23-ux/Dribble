# Project Responsive Web Design using Bootstrap
## Date:22.05.25

## AIM:
To create a simplified clone of Dribbble (https://dribbble.com/) landing page.


## DESIGN STEPS:

### Step 1:
Clone the repository from GitHub.

### Step 2:
Create Django Admin project.

### Step 3:
Create a New App under the Django Admin project.

### Step 4:
Insert the necessary CSS and JavaScript files as external in order to use Bootstrap.

### Step 5:
Create a HTML file and include the needed Bootstrap components.

### Step 6:
Publish the website in the LocalHost.

## PROGRAM :
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dribbble Clone</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
    <style>
        /* Custom styles for Dribbble-like feel */
        body {
            font-family: 'Helvetica Neue', Helvetica, Arial, sans-serif;
            background-color: #f8f8f8;
        }
        .navbar {
            background-color: #ffffff;
            border-bottom: 1px solid #eeeeee;
        }
        .navbar-brand {
            font-weight: bold;
            color: #ea4c89 !important; /* Dribbble pink */
        }
        .nav-link {
            color: #6e6d7a !important;
            font-weight: 500;
        }
        .btn-dribbble {
            background-color: #ea4c89;
            color: white;
            border-radius: 8px;
            padding: 8px 16px;
            font-weight: 600;
        }
        .btn-dribbble:hover {
            background-color: #e0447c;
            color: white;
        }
        .hero-section {
            background-color: #f8f8f8;
            padding: 80px 0;
            text-align: center;
        }
        .hero-section h1 {
            font-size: 3.5rem;
            font-weight: bold;
            color: #0d0c22;
        }
        .hero-section p {
            font-size: 1.25rem;
            color: #6e6d7a;
            max-width: 700px;
            margin: 20px auto;
        }
        .search-bar-hero {
            max-width: 500px;
            margin: 30px auto;
            position: relative;
        }
        .search-bar-hero input {
            border-radius: 50px;
            padding: 12px 20px 12px 50px;
            border: 1px solid #e0e0e0;
            font-size: 1.1rem;
            background-color: #f2f2f2;
        }
        .search-bar-hero .search-icon {
            position: absolute;
            left: 20px;
            top: 50%;
            transform: translateY(-50%);
            color: #999;
        }
        .content-section {
            padding: 60px 0;
        }
        .card-shot {
            border: none;
            border-radius: 12px;
            overflow: hidden;
            margin-bottom: 30px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.05);
            transition: transform 0.2s ease-in-out;
        }
        .card-shot:hover {
            transform: translateY(-5px);
        }
        .card-shot img {
            border-bottom-left-radius: 0;
            border-bottom-right-radius: 0;
            object-fit: cover;
            height: 200px; /* Fixed height for consistency */
            width: 100%;
        }
        .card-shot .card-body {
            padding: 15px;
            background-color: #ffffff;
        }
        .card-shot .card-title {
            font-size: 1.1rem;
            font-weight: 600;
            color: #0d0c22;
        }
        .card-shot .card-text {
            font-size: 0.9rem;
            color: #999;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        .footer {
            background-color: #f8f8f8;
            padding: 40px 0;
            border-top: 1px solid #eeeeee;
            color: #6e6d7a;
            font-size: 0.9rem;
        }
        .footer .social-icons a {
            color: #6e6d7a;
            margin-right: 15px;
            font-size: 1.2rem;
        }
    </style>
</head>
<body>

    <nav class="navbar navbar-expand-lg">
        <div class="container">
            <a class="navbar-brand" href="#">dribbble</a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav me-auto mb-2 mb-lg-0">
                    <li class="nav-item">
                        <a class="nav-link" href="#">Inspiration</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Find Work</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Learn Design</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Go Pro</a>
                    </li>
                </ul>
                <form class="d-flex me-3 position-relative">
                    <input class="form-control rounded-pill pe-5" type="search" placeholder="Search..." aria-label="Search" style="width: 180px;">
                    <i class="fas fa-search position-absolute end-0 top-50 translate-middle-y me-3 text-muted"></i>
                </form>
                <div class="d-flex">
                    <a href="#" class="btn btn-link text-decoration-none nav-link me-2">Log in</a>
                    <a href="#" class="btn btn-dribbble">Sign up</a>
                </div>
            </div>
        </div>
    </nav>

    <section class="hero-section">
        <div class="container">
            <h1>The world’s leading community for creatives to share, grow, and get hired.</h1>
            <p>
                Discover the best design inspiration from leading designers around the world.
            </p>
            <div class="search-bar-hero">
                <input type="text" class="form-control" placeholder="Search for designs by category or tag...">
                <i class="fas fa-search search-icon"></i>
            </div>
            <p class="mt-3 text-muted">Trending searches: <span class="fw-bold">landing page, app design, icon, ui design, web design</span></p>
        </div>
    </section>

    <section class="content-section bg-white">
        <div class="container">
            <h2 class="mb-4 text-center">Trending Shots</h2>
            <div class="row row-cols-1 row-cols-md-2 row-cols-lg-3 row-cols-xl-4 g-4">
                <div class="col">
                    <div class="card card-shot">
                        <img src="image.png" class="card-img-top" alt="Design 1">
                        <div class="card-body">
                            <h5 class="card-title">Awesome UI Kit</h5>
                            <p class="card-text">
                                <span><i class="far fa-eye me-1"></i> 1.2K</span>
                                <span><i class="far fa-heart me-1"></i> 345</span>
                            </p>
                        </div>
                    </div>
                </div>
                <div class="col">
                    <div class="card card-shot">
                        <img src="image copy.png" class="card-img-top" alt="Design 2">
                        <div class="card-body">
                            <h5 class="card-title">Mobile App Concept</h5>
                            <p class="card-text">
                                <span><i class="far fa-eye me-1"></i> 980</span>
                                <span><i class="far fa-heart me-1"></i> 210</span>
                            </p>
                        </div>
                    </div>
                </div>
                <div class="col">
                    <div class="card card-shot">
                        <img src="image copy 2.png " class="card-img-top" alt="Design 3">
                        <div class="card-body">
                            <h5 class="card-title">Website Redesign</h5>
                            <p class="card-text">
                                <span><i class="far fa-eye me-1"></i> 1.5K</span>
                                <span><i class="far fa-heart me-1"></i> 400</span>
                            </p>
                        </div>
                    </div>
                </div>
                <div class="col">
                    <div class="card card-shot">
                        <img src="image copy 3.png" class="card-img-top" alt="Design 4">
                        <div class="card-body">
                            <h5 class="card-title">Icon Set Collection</h5>
                            <p class="card-text">
                                <span><i class="far fa-eye me-1"></i> 750</span>
                                <span><i class="far fa-heart me-1"></i> 180</span>
                            </p>
                        </div>
                    </div>
                </div>
    <footer class="footer">
        <div class="container text-center">
            <p>&copy; 2025 Dribbble Clone. Designed by HARSHENI.S.</p>
            <div class="social-icons mt-3">
                <a href="#"><i class="fab fa-twitter"></i></a>
                <a href="#"><i class="fab fa-facebook-f"></i></a>
                <a href="#"><i class="fab fa-instagram"></i></a>
                <a href="#"><i class="fab fa-linkedin-in"></i></a>
            </div>
        </div>
    </footer>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
    <script src="https://kit.fontawesome.com/a076d05399.js" crossorigin="anonymous"></script>
</body>
</html>
```

## OUTPUT:

![image](https://github.com/user-attachments/assets/f1bef4b6-062f-42f0-9c6e-bf14a5f9ef30)

## RESULT:
The Project for responsive web design using Bootstrap is completed successfully.
