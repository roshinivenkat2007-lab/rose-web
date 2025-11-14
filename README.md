<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>E-Commerce Portal</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f4f4f9;
      margin: 0;
      padding: 0;
    }

    header {
      background-color: #0078d7;
      color: white;
      padding: 20px;
      text-align: center;
    }

    nav ul {
      list-style: none;
      margin: 0;
      padding: 0;
      overflow: hidden;
      background-color: #333;
    }

    nav li {
      float: left;
    }

    nav li a {
      display: block;
      color: white;
      text-align: center;
      padding: 14px 16px;
      text-decoration: none;
    }

    nav li a:hover {
      background-color: #111;
    }

    .container {
      padding: 20px;
      text-align: center;
    }

    .product {
      display: inline-block;
      background-color: white;
      border-radius: 10px;
      box-shadow: 0 0 5px rgba(0, 0, 0, 0.2);
      margin: 15px;
      width: 230px;
      padding: 10px;
    }

    .product img {
      width: 100%;
      height: 200px;
      border-radius: 10px;
      object-fit: cover;
    }

    .product h3 {
      margin: 10px 0;
    }

    button {
      background-color: #0078d7;
      color: white;
      border: none;
      border-radius: 5px;
      padding: 8px 10px;
      cursor: pointer;
    }

    button:hover {
      background-color: #005fa3;
    }

    #cart {
      text-align: left;
      max-width: 600px;
      margin: 0 auto;
      background: white;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 0 5px gray;
    }

    footer {
      background-color: #333;
      color: white;
      text-align: center;
      padding: 15px;
      margin-top: 30px;
    }
  </style>
</head>
<body>

  <header>
    <h1>My E-Commerce Store</h1>
  </header>

  <nav>
    <ul>
      <li><a href="#home">Home</a></li>
      <li><a href="#products">Products</a></li>
      <li><a href="#cart">Cart</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>

  <div class="container" id="home">
    <h2>Welcome to Our Online Store!</h2>
    <p>Shop the best products at amazing prices!</p>
  </div>

  <div class="container" id="products">
    <h2>Our Products</h2>

    <div class="product">
      <img src="https://images.unsplash.com/photo-1605546960121-24e957eb8c15?q=80&w=1936&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D">
      <h3>Smartphone</h3>
      <p>Price: </p>
      <button onclick="addToCart('Smartphone', 499)">Add to Cart</button>
    </div>

    

    <div class="product">
      <img src="https://images.unsplash.com/photo-1517336714731-489689fd1ca8" alt="Laptop">
      <h3>Laptop</h3>
      <p>Price: $899</p>
      <button onclick="addToCart('Laptop', 899)">Add to Cart</button>
    </div>

    <div class="product">
      <img src="https://images.unsplash.com/photo-1516116216624-53e697fedbea" alt="Smartwatch">
      <h3>Smartwatch</h3>
      <p>Price: $149</p>
      <button onclick="addToCart('Smartwatch', 149)">Add to Cart</button>
    </div>

    <div class="product">
      <img src="https://www.tataneu.com/pages/electronics/_next/image?url=https%3A%2F%2Fd1msew97rp2nin.cloudfront.net%2Fprodin%2Ftnelectronics%2Fblogimages%2Fcomparing-dslr-camera-pixels-which-model-is-superior-ef4fa474-0bb1-4f72-965d-d33e0882a1bf.webp&w=1920&q=75" alt="Camera">
      <h3>Camera</h3>
      <p>Price: $299</p>
      <button onclick="addToCart('Camera', 299)">Add to Cart</button>
    </div>

    <div class="product">
      <img src="https://images.unsplash.com/photo-1542291026-7eec264c27ff" alt="Shoes">
      <h3>Sports Shoes</h3>
      <p>Price: $79</p>
      <button onclick="addToCart('Sports Shoes', 79)">Add to Cart</button>
    </div>

    <div class="product">
      <img src="https://plus.unsplash.com/premium_photo-1664110691115-790e20a41744?q=80&w=653&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D">
      <h3>Backpack</h3>
      <p>Price: $59</p>
      <button onclick="addToCart('Backpack', 59)">Add to Cart</button>
    </div>

    <div class="product">
      <img src="https://images.unsplash.com/photo-1503341455253-b2e723bb3dbb" alt="Jacket">
      <h3>Jacket</h3>
      <p>Price: $129</p>
      <button onclick="addToCart('Jacket', 129)">Add to Cart</button>
    </div>

  </div>

  <div class="container" id="cart">
    <h2>Your Cart</h2>
    <ul id="cartItems"></ul>
    <h3>Total: $<span id="cartTotal">0</span></h3>
  </div>

  <footer>
    <p>© 2025 My E-Commerce Store | Designed by Student</p>
  </footer>

  <script>
    const cartItems = document.getElementById('cartItems');
    const cartTotal = document.getElementById('cartTotal');
    let total = 0;

    function addToCart(product, price) {
      const li = document.createElement('li');
      li.textContent = `${product} - $${price}`;
      cartItems.appendChild(li);
      total += price;
      cartTotal.textContent = total;
      alert(`${product} added to cart!`);
    }
  </script>
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Contact Us - My E-Commerce Store</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f4f4f9;
      margin: 0;
      padding: 0;
    }

    header {
      background-color: #0078d7;
      color: white;
      text-align: center;
      padding: 20px;
    }

    nav ul {
      list-style: none;
      margin: 0;
      padding: 0;
      overflow: hidden;
      background-color: #333;
    }

    nav li {
      float: left;
    }

    nav li a {
      display: block;
      color: white;
      text-align: center;
      padding: 14px 16px;
      text-decoration: none;
    }

    nav li a:hover {
      background-color: #111;
    }

    .container {
      padding: 40px;
      max-width: 600px;
      margin: auto;
      background: white;
      border-radius: 10px;
      box-shadow: 0 0 5px gray;
      margin-top: 40px;
    }

    h2 {
      color: #0078d7;
      text-align: center;
    }

    label {
      display: block;
      margin: 10px 0 5px;
    }

    input, textarea {
      width: 100%;
      padding: 10px;
      border-radius: 5px;
      border: 1px solid #ccc;
      box-sizing: border-box;
    }

    textarea {
      resize: none;
    }

    button {
      margin-top: 15px;
      width: 100%;
      background-color: #0078d7;
      color: white;
      border: none;
      padding: 10px;
      border-radius: 5px;
      cursor: pointer;
      font-size: 16px;
    }

    button:hover {
      background-color: #005fa3;
    }

    footer {
      background-color: #333;
      color: white;
      text-align: center;
      padding: 15px;
      margin-top: 50px;
    }
  </style>
</head>
<body>

  <header>
    <h1>Contact Us</h1>
  </header>

  <nav>
    <ul>
      <li><a href="index.html">Home</a></li>
      <li><a href="index.html#products">Products</a></li>
      <li><a href="index.html#cart">Cart</a></li>
      <li><a href="contact.html">Contact Us</a></li>
    </ul>
  </nav>

  <div class="container">
    <h2>Get in Touch</h2>
    <p style="text-align:center;">We’d love to hear from you! Fill out the form below and our team will get back to you soon.</p>

    <form id="contactForm" onsubmit="return validateForm()">
      <label for="name">Full Name:</label>
      <input type="text" id="name" placeholder="Enter your name">

      <label for="email">Email Address:</label>
      <input type="email" id="email" placeholder="Enter your email">

      <label for="message">Message:</label>
      <textarea id="message" rows="5" placeholder="Write your message"></textarea>

      <button type="submit">Send Message</button>
    </form>
  </div>

  <footer>
    <p>© 2025 My E-Commerce Store | Designed by Student</p>
  </footer>

  <script>
    function validateForm() {
      const name = document.getElementById('name').value.trim();
      const email = document.getElementById('email').value.trim();
      const message = document.getElementById('message').value.trim();

      if (name === "" || email === "" || message === "") {
        alert("Please fill in all fields before submitting.");
        return false;
      }
      if (!email.includes("@")) {
        alert("Please enter a valid email address.");
        return false;
      }

      alert("Message sent successfully!");
      document.getElementById('contactForm').reset();
      return false; // Prevent actual submission for demo
    }
  </script>

</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>User Registration - My E-Commerce Store</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f4f4f9;
      margin: 0;
      padding: 0;
    }

    header {
      background-color: #0078d7;
      color: white;
      text-align: center;
      padding: 20px;
    }

    nav ul {
      list-style: none;
      margin: 0;
      padding: 0;
      overflow: hidden;
      background-color: #333;
    }

    nav li {
      float: left;
    }

    nav li a {
      display: block;
      color: white;
      text-align: center;
      padding: 14px 16px;
      text-decoration: none;
    }

    nav li a:hover {
      background-color: #111;
    }

    .container {
      padding: 40px;
      max-width: 500px;
      margin: auto;
      background: white;
      border-radius: 10px;
      box-shadow: 0 0 5px gray;
      margin-top: 40px;
    }

    h2 {
      color: #0078d7;
      text-align: center;
    }

    label {
      display: block;
      margin: 10px 0 5px;
    }

    input {
      width: 100%;
      padding: 10px;
      border-radius: 5px;
      border: 1px solid #ccc;
      box-sizing: border-box;
    }

    button {
      margin-top: 15px;
      width: 100%;
      background-color: #0078d7;
      color: white;
      border: none;
      padding: 10px;
      border-radius: 5px;
      cursor: pointer;
      font-size: 16px;
    }

    button:hover {
      background-color: #005fa3;
    }

    footer {
      background-color: #333;
      color: white;
      text-align: center;
      padding: 15px;
      margin-top: 50px;
    }

    .link {
      text-align: center;
      margin-top: 10px;
    }
  </style>
</head>
<body>

  <header>
    <h1>User Registration</h1>
  </header>

  <nav>
    <ul>
      <li><a href="index.html">Home</a></li>
      <li><a href="login.html">Login</a></li>
      <li><a href="register.html">Register</a></li>
      <li><a href="contact.html">Contact</a></li>
    </ul>
  </nav>

  <div class="container">
    <h2>Create Your Account</h2>
    <form id="registerForm" onsubmit="return validateRegister()">
      <label for="name">Full Name:</label>
      <input type="text" id="name" placeholder="Enter your full name">

      <label for="email">Email:</label>
      <input type="email" id="email" placeholder="Enter your email">

      <label for="password">Password:</label>
      <input type="password" id="password" placeholder="Enter password (min 6 characters)">

      <label for="confirm">Confirm Password:</label>
      <input type="password" id="confirm" placeholder="Confirm your password">

      <button type="submit">Register</button>
    </form>
    <div class="link">
      <p>Already have an account? <a href="login.html">Login here</a></p>
    </div>
  </div>

  <footer>
    <p>© 2025 My E-Commerce Store | Designed by Student</p>
  </footer>

  <script>
    function validateRegister() {
      const name = document.getElementById('name').value.trim();
      const email = document.getElementById('email').value.trim();
      const password = document.getElementById('password').value.trim();
      const confirm = document.getElementById('confirm').value.trim();

      if (!name || !email || !password || !confirm) {
        alert("Please fill in all fields.");
        return false;
      }
      if (!email.includes("@")) {
        alert("Enter a valid email address.");
        return false;
      }
      if (password.length < 6) {
        alert("Password must be at least 6 characters.");
        return false;
      }
      if (password !== confirm) {
        alert("Passwords do not match.");
        return false;
      }

      alert("Registration successful!");
      document.getElementById('registerForm').reset();
      return false;
    }
  </script>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Login - My E-Commerce Store</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f4f4f9;
      margin: 0;
      padding: 0;
    }

    header {
      background-color: #0078d7;
      color: white;
      text-align: center;
      padding: 20px;
    }

    nav ul {
      list-style: none;
      margin: 0;
      padding: 0;
      overflow: hidden;
      background-color: #333;
    }

    nav li {
      float: left;
    }

    nav li a {
      display: block;
      color: white;
      text-align: center;
      padding: 14px 16px;
      text-decoration: none;
    }

    nav li a:hover {
      background-color: #111;
    }

    .container {
      padding: 40px;
      max-width: 400px;
      margin: auto;
      background: white;
      border-radius: 10px;
      box-shadow: 0 0 5px gray;
      margin-top: 50px;
    }

    h2 {
      color: #0078d7;
      text-align: center;
    }

    label {
      display: block;
      margin: 10px 0 5px;
    }

    input {
      width: 100%;
      padding: 10px;
      border-radius: 5px;
      border: 1px solid #ccc;
      box-sizing: border-box;
    }

    button {
      margin-top: 15px;
      width: 100%;
      background-color: #0078d7;
      color: white;
      border: none;
      padding: 10px;
      border-radius: 5px;
      cursor: pointer;
      font-size: 16px;
    }

    button:hover {
      background-color: #005fa3;
    }

    footer {
      background-color: #333;
      color: white;
      text-align: center;
      padding: 15px;
      margin-top: 50px;
    }

    .link {
      text-align: center;
      margin-top: 10px;
    }
  </style>
</head>
<body>

  <header>
    <h1>User Login</h1>
  </header>

  <nav>
    <ul>
      <li><a href="index.html">Home</a></li>
      <li><a href="login.html">Login</a></li>
      <li><a href="register.html">Register</a></li>
      <li><a href="contact.html">Contact</a></li>
    </ul>
  </nav>

  <div class="container">
    <h2>Login to Your Account</h2>
    <form id="loginForm" onsubmit="return validateLogin()">
      <label for="email">Email:</label>
      <input type="email" id="email" placeholder="Enter your email">

      <label for="password">Password:</label>
      <input type="password" id="password" placeholder="Enter your password">

      <button type="submit">Login</button>
    </form>
    <div class="link">
      <p>Don’t have an account? <a href="register.html">Register here</a></p>
    </div>
  </div>

  

  <script>
    function validateLogin() {
      const email = document.getElementById('email').value.trim();
      const password = document.getElementById('password').value.trim();

      if (!email || !password) {
        alert("Please fill in all fields.");
        return false;
      }
      if (!email.includes("@")) {
        alert("Enter a valid email address.");
        return false;
      }
      if (password.length < 6) {
        alert("Password must be at least 6 characters.");
        return false;
      }

      alert("Login successful!");
      document.getElementById('loginForm').reset();
      return false;
    }
  </script>
</body>
</html>


</body>
</html># rose-web
