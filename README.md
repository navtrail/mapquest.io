<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>NavTrail - All-in-One</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background: linear-gradient(to right, #a8c0ff, #3f2b96); /* Blue-Purple Gradient */
            color: #fff;
        }
        header {
            background: #6a11cb; /* Purple Shade */
            padding: 15px;
            text-align: center;
            font-size: 24px;
            font-weight: bold;
            color: white;
            position: sticky;
            top: 0;
            z-index: 1000;
        }
        .nav {
            display: flex;
            justify-content: center;
            gap: 20px;
            padding: 10px;
            background: #957DAD;
            position: sticky;
            top: 50px;
            z-index: 999;
        }
        .nav a {
            text-decoration: none;
            color: white;
            font-size: 18px;
            font-weight: bold;
            transition: 0.3s;
        }
        .nav a:hover {
            color: #ffd700;
        }
        section {
            padding: 50px;
            text-align: center;
            background: rgba(255, 255, 255, 0.2);
            margin: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            backdrop-filter: blur(10px);
        }
        .collapsible {
            cursor: pointer;
            padding: 10px;
            width: 100%;
            text-align: center;
            border: none;
            outline: none;
            font-size: 18px;
            background: #6a11cb;
            color: white;
            border-radius: 5px;
            transition: 0.3s;
        }
        .collapsible:hover {
            background: #957DAD;
        }
        .content {
            display: none;
            padding: 20px;
        }
        footer {
            text-align: center;
            padding: 20px;
            background: #6a11cb;
            color: white;
            margin-top: 20px;
        }
    </style>
    <script>
        document.addEventListener("DOMContentLoaded", function () {
            let collapsibles = document.querySelectorAll(".collapsible");
            collapsibles.forEach(btn => {
                btn.addEventListener("click", function () {
                    let content = this.nextElementSibling;
                    content.style.display = content.style.display === "block" ? "none" : "block";
                });
            });
        });
    </script>
</head>
<body>
    <header>NavTrail - Explore the World</header>
    <div class="nav">
        <a href="#home">Home</a>
        <a href="#explore">Explore</a>
        <a href="#plan-trip">Plan Trip</a>
        <a href="#community">Community</a>
        <a href="#about">About</a>
        <a href="#profile">Profile</a>
        <a href="#login">Login</a>
        <a href="#signup">Sign Up</a>
    </div>

    <button class="collapsible">Welcome to NavTrail</button>
    <div class="content" id="home">
        <p>Plan your next adventure with ease!</p>
    </div>

    <button class="collapsible">Explore Destinations</button>
    <div class="content" id="explore">
        <p>Discover amazing places around the world.</p>
    </div>

    <button class="collapsible">Plan Your Trip</button>
    <div class="content" id="plan-trip">
        <p>Create a personalized itinerary with smart suggestions.</p>
    </div>

    <button class="collapsible">Join the Community</button>
    <div class="content" id="community">
        <p>Connect with travelers, share experiences, and explore.</p>
    </div>

    <button class="collapsible">About NavTrail</button>
    <div class="content" id="about">
        <p>Learn about our mission and values.</p>
    </div>

    <button class="collapsible">Your Profile</button>
    <div class="content" id="profile">
        <p>Manage your account and travel history.</p>
    </div>

    <button class="collapsible">Login</button>
    <div class="content" id="login">
        <p>Access your account.</p>
    </div>

    <button class="collapsible">Sign Up</button>
    <div class="content" id="signup">
        <p>Create your NavTrail account today.</p>
    </div>

    <footer>
        <p>&copy; 2024 NavTrail. All rights reserved.</p>
    </footer>
</body>
</html>


