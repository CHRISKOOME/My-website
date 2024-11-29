<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Welcome</title>

    <!-- Bootstrap CSS -->
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css" integrity="sha384-ggOyR0iXCbMQv3Xipma34MD+dH/1fQ784/j6cY/iJTQUOhcWr7x9JvoRxT2MZw1T" crossorigin="anonymous">

    <!-- Google Fonts: Roboto -->
    <link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Roboto:300,400,500,700&display=swap">

    <!-- Custom Styles -->
    <style>
        body {
            font-family: 'Roboto', sans-serif;
            background-color: whitesmoke;:
            transition: background-color 0.5s ease;
        }
        .logo {
            border-radius: 50%;
            width: 150px;
            height: 150px;
        }
        .ion-padding {
            padding: 100px;
        }
        .ion-text-center {
            text-align: center;
        }
        .btn-custom {
            background-color: red;
            color: #fff;
            border: 1px solid #fff;
            padding: 10px 50px;
            transition: background-color 0.3s, border 0.3s, color 0.3s;
        }
        .btn-custom:hover {
            background-color: red;
            border: 1px solid #dc3545;
            color: #dc3545;
        }
        .social-login {
            display: flex;
            justify-content: center;
            gap: 10px;
            margin-top: 20px;
        }
        .social-button {
            border: 1px solid #dc3545;
            padding: 10px 20px;
            background-color: white;
            color: #dc3545;
            cursor: pointer;
            transition: background-color 0.3s, color 0.3s;
        }
        .social-button:hover {
            background-color: #dc3545;
            color: white;
        }
        .navbar-light .navbar-brand {
            color: white;
        }
        .dark-mode {
            background-color: #1a1a1a;
            color: #f1f1f1;
        }
        .spinner-border {
            display: none;
        }
        .register-btn {
            margin-top: 20px;
            padding: 10px 30px;
            background-color: #28a745;
            color: white;
            border: none;
            border-radius: 5px;
            transition: background-color 0.3s;
        }
        .register-btn:hover {
            background-color: #218838;
        }
    </style>
</head>

<body>

    <!-- Navbar -->
    <header>
        <nav class="navbar navbar-expand-lg navbar-danger bg-danger">
            <a class="navbar-brand text-light" href="#">Welcome</a>
            <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav ml-auto">
                    <li class="nav-item active">
                    </li>
                </ul>
            </div>
        </nav>
    </header>

    <!-- Dark Mode Toggle -->
    <div class="d-flex justify-content-end p-3">
        <button class="btn btn-secondary" onclick="toggleDarkMode()">🌗change to darkmode</button>
    </div>

    <!-- Main Content -->
    <div class="container-fluid">
        <div class="row">
            <div class="col-md-12 ion-padding">
                <div class="ion-text-center">
                    <!-- Logo -->
                    <img src="/IMG_2583.jpeg" alt="Logo" class="logo">

                    <!-- Brand Name -->
                    <h1 class="font-weight-bold">MATHPASS</h1>

                    <!-- Welcome Message -->
                    <h1><p><span style="COLOR:blue;">FIRST BEFORE WE START; SIGN IN</span></p></h1>
                    <!-- Register Button -->
                    <button class="register-btn" onclick="goToLoginPage(/login.html)"><a href="/login.html">LOGIN</a></button>
                            <div>
                    <button class="register-btn" onclick="goToRegisterPage(/registration.html)"><a href="/registration.html">Register</a></button>
                </div>

                <!-- Loading Spinner -->
                <div class="text-center mt-3">
                    <div class="spinner-border text-danger" id="loadingSpinner" role="status">
                        <span class="sr-only">Loading...</span>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- Bootstrap JS and dependencies -->
    <script src="https://code.jquery.com/jquery-3.3.1.slim.min.js" integrity="sha384-q8i/X+965DzO0rT7abK41JStQIAqVgRVzpbzo5smXKp4YfRvH+8abtTE1Pi6jizo" crossorigin="anonymous"></script>
    <script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.10.2/dist/umd/popper.min.js" integrity="sha384-73L/B5Nb5cdWU7qzyts3+1F6sV+0g9iC8fwW8Wg/Ee8tl1IaEo/EE7woCpHxyJs" crossorigin="anonymous"></script>
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/js/bootstrap.min.js" integrity="sha384-JjSmVgyd0p3pXB1rRibZUAYoIIy6mgg9uUPOB4N0LZz5KR6QaAC2bJ86U7EsxPDi" crossorigin="anonymous"></script>

    <!-- Custom Script -->
    <script>
        function toggleDarkMode() {
            document.body.classList.toggle('dark-mode');
        }

        // Redirect to the preferred login platform
        function redirectTo(platform) {
            document.getElementById('loadingSpinner').style.display = 'block';  // Show spinner

            setTimeout(function() {
                alert(`Redirecting to login with ${platform}...`);
                // Here you can redirect to the actual login page for each platform
                // For demo purposes, let's just simulate successful login
                window.location.href = 'template.html';  // Redirect to template.html after login
            }, 1000);  // 1 second delay for demo
        }

        // Redirect to the registration page
        function goToRegisterPage() {
            window.location.href = 'register.html';
        }
    </script>
</body>
</html>
<style include="print-preview-shared cr-hidden-style throbber">...</style>
