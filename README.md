# movie-booking
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Movie Booking System</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            margin: 0;
            padding: 0;
        }

        header {
            background-color: #333;
            color: #fff;
            text-align: center;
            padding: 1em;
        }

        nav {
            background-color: #007BFF;
            padding: 1em;
            display: flex;
            justify-content: center;
        }

        nav a {
            color: #fff;
            text-decoration: none;
            margin-right: 1em;
        }

        section {
            padding: 2em;
        }

        .section {
            display: none;
            justify-content: center;
            align-items: center;
            text-align: center;
        }

        .active {
            display: flex;
        }

        .form-container, .food-menu, .seat-categories {
            background-color: #fff;
            padding: 2em;
            margin: 1em;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            max-width: 600px;
            width: 100%;
        }

        h2 {
            margin-top: 0;
            color: #333;
            text-align: center;
        }

        form {
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        label {
            margin-bottom: 0.5em;
            color: #333;
            font-weight: bold;
            align-self: flex-start;
            width: 100%;
            max-width: 400px;
        }

        input, select {
            padding: 0.5em;
            margin-bottom: 1em;
            border-radius: 4px;
            border: 1px solid #ccc;
            font-size: 1rem;
            width: 100%;
            max-width: 400px;
        }

        button {
            padding: 0.7em;
            background-color: #007BFF;
            color: #fff;
            border: none;
            cursor: pointer;
            border-radius: 4px;
            font-size: 1rem;
            width: 100%;
            max-width: 200px;
            align-self: center;
        }

        button:hover {
            background-color: #0056b3;
        }

        .food-item {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-top: 1rem;
        }

        .seat-categories .seat-category {
            padding: 1rem;
            border-radius: 4px;
            color: #fff;
            text-align: center;
            cursor: pointer;
            margin-bottom: 1rem;
            width: 100%;
            max-width: 200px;
            align-self: center;
        }

        .gold {
            background-color: #ffd700;
        }

        .silver {
            background-color: #c0c0c0;
        }

        .platinum {
            background-color: #e5e4e2;
        }

        footer {
            background-color: #333;
            color: #fff;
            text-align: center;
            padding: 1em;
            position: fixed;
            bottom: 0;
            width: 100%;
        }
    </style>
</head>
<body>
    <header>
        <h1>Movie Booking System</h1>
    </header>

    <nav>
        <a href="#" onclick="showSection('register-section')">Register</a>
        <a href="#" onclick="showSection('login-section')">Login</a>
        <a href="#" onclick="showSection('food-section')">Food Ordering</a>
        <a href="#" onclick="showSection('seat-section')">Seat Management</a>
    </nav>

    <section id="register-section" class="section active">
        <div class="form-container">
            <h2>Register</h2>
            <form id="register-form" onsubmit="registerUser(event)">
                <label for="name">Name:</label>
                <input type="text" id="name" name="name" required>
                
                <label for="email">Email:</label>
                <input type="email" id="email" name="email" required>
                
                <label for="password">Password:</label>
                <input type="password" id="password" name="password" required>
                
                <button type="submit">Register</button>
            </form>
        </div>
    </section>

    <section id="login-section" class="section">
        <div class="form-container">
            <h2>Login</h2>
            <form id="login-form" onsubmit="loginUser(event)">
                <label for="email">Email:</label>
                <input type="email" id="login-email" name="email" required>
                
                <label for="password">Password:</label>
                <input type="password" id="login-password" name="password" required>
                
                <button type="submit">Login</button>
            </form>
        </div>
    </section>

    <section id="food-section" class="section">
        <div class="food-menu">
            <h2>Food Ordering</h2>
            <div class="food-item">
                <span>Popcorn</span>
                <button onclick="addToCart('Popcorn')">Add to Cart</button>
            </div>
            <div class="food-item">
                <span>Nachos</span>
                <button onclick="addToCart('Nachos')">Add to Cart</button>
            </div>
            <div class="food-item">
                <span>Soda</span>
                <button onclick="addToCart('Soda')">Add to Cart</button>
            </div>
            <div class="food-item">
                <span>Hot Dog</span>
                <button onclick="addToCart('Hot Dog')">Add to Cart</button>
            </div>
        </div>
    </section>

    <section id="seat-section" class="section">
        <div class="seat-categories">
            <h2>Seat Management</h2>
            <div class="seat-category gold" onclick="selectSeat('Gold')">Gold</div>
            <div class="seat-category silver" onclick="selectSeat('Silver')">Silver</div>
            <div class="seat-category platinum" onclick="selectSeat('Platinum')">Platinum</div>
        </div>
    </section>

    <footer>
        &copy; 2024 Movie Booking System. All rights reserved.
    </footer>

    <script>
        function showSection(sectionId) {
            document.querySelectorAll('.section').forEach(section => {
                section.classList.remove('active');
            });
            document.getElementById(sectionId).classList.add('active');
        }

        function registerUser(event) {
            event.preventDefault();
            // Perform form validation and submission logic here
            alert('Registration functionality will be implemented.');
        }

        function loginUser(event) {
            event.preventDefault();
            // Perform login validation and submission logic here
            alert('Login functionality will be implemented.');
        }

        function addToCart(item) {
            alert('Added ' + item + ' to cart.');
        }

        function selectSeat(category) {
            alert('Selected ' + category + ' seat.');
        }
    </script>
</body>
</html>
