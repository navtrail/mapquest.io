<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>NavTrail - All-in-One</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        :root {
            --bg-color: linear-gradient(to right, #a8c0ff, #3f2b96);
            --text-color: #fff;
            --nav-bg: #957DAD;
            --header-bg: #6a11cb;
            --section-bg: rgba(255, 255, 255, 0.2);
            --footer-bg: #6a11cb;
        }
        body.dark-mode {
            --bg-color: #121212;
            --text-color: #e0e0e0;
            --nav-bg: #333;
            --header-bg: #222;
            --section-bg: #1e1e1e;
            --footer-bg: #222;
        }
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background: var(--bg-color);
            color: var(--text-color);
        }
        header {
            background: var(--header-bg);
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
            background: var(--nav-bg);
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
        .section {
            text-align: center;
            padding: 20px;
            background: var(--section-bg);
            margin: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        footer {
            text-align: center;
            padding: 20px;
            background: var(--footer-bg);
            color: white;
            margin-top: 20px;
        }
    </style>
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

    <section class="section" id="weather">
        <h2>Current Weather</h2>
        <p>Fetching weather data...</p>
    </section>

    <section class="section" id="map">
        <h2>Map & Location</h2>
        <div id="map"></div>
    </section>

    <section class="section" id="image-slider">
        <h2>Travel Destinations</h2>
        <div class="slider">
            <img src="https://via.placeholder.com/800x400?text=Paris" alt="Paris">
            <img src="https://via.placeholder.com/800x400?text=Tokyo" alt="Tokyo">
            <img src="https://via.placeholder.com/800x400?text=New York" alt="New York">
        </div>
    </section>

    <section class="section" id="chat-support">
        <h2>Live Chat Support</h2>
        <div class="chat-box">
            <p>Chat with our support team.</p>
        </div>
    </section>

    <section class="section" id="itinerary-generator">
        <h2>AI Itinerary Generator</h2>
        <input type="text" id="destination" placeholder="Enter a destination">
        <button onclick="generateItinerary()">Generate</button>
        <p id="itinerary-output"></p>
    </section>

    <section class="section" id="budget-tracker">
        <h2>Budget Tracker</h2>
        <input type="text" id="expense-name" placeholder="Expense Name">
        <input type="number" id="expense-amount" placeholder="Amount">
        <button onclick="addExpense()">Add Expense</button>
        <p id="total-expense">Total Expense: $0.00</p>
    </section>

    <section class="section" id="travel-packages">
        <h2>Travel Packages</h2>
        <input type="number" id="package-budget" placeholder="Enter your budget">
        <button onclick="recommendPackage()">Get Recommendation</button>
        <p id="package-output"></p>
    </section>

    <section class="section" id="phrasebook">
        <h2>Local Phrasebook</h2>
        <select id="language-select">
            <option value="english">English</option>
            <option value="spanish">Spanish</option>
            <option value="french">French</option>
            <option value="german">German</option>
        </select>
        <button onclick="showPhrase()">Show Phrase</button>
        <p id="phrase-output"></p>
    </section>

    <footer>
        <p>&copy; 2024 NavTrail. All rights reserved.</p>
    </footer>
</body>
</html>
