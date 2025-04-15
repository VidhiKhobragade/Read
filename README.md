<!-- index.html -->
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>GiftEase - Your Gift Destination</title>
  <link rel="stylesheet" href="style.css" />
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;500;700&display=swap" rel="stylesheet" />
</head>
<body>
  <header>
    <h1>GiftEase</h1>
    <nav>
      <a href="#">Home</a>
      <a href="#products">Gifts</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>

  <section class="hero">
    <h2>Find the Perfect Gift for Every Occasion!</h2>
    <button onclick="scrollToProducts()">Shop Now</button>
  </section>

  <section class="products" id="products">
    <div class="product-card">
      <img src="https://via.placeholder.com/250x200?text=Teddy+Bear" alt="Teddy Bear" />
      <h3>Fluffy Teddy Bear</h3>
      <p>$20</p>
      <button onclick="addToCart('Teddy Bear')">Add to Cart</button>
    </div>
    <div class="product-card">
      <img src="https://via.placeholder.com/250x200?text=Mug" alt="Mug" />
      <h3>Custom Mug</h3>
      <p>$12</p>
      <button onclick="addToCart('Custom Mug')">Add to Cart</button>
    </div>
    <div class="product-card">
      <img src="https://via.placeholder.com/250x200?text=Photo+Frame" alt="Photo Frame" />
      <h3>Photo Frame</h3>
      <p>$15</p>
      <button onclick="addToCart('Photo Frame')">Add to Cart</button>
    </div>
  </section>

  <footer>
    <p>&copy; 2025 GiftEase. All rights reserved.</p>
  </footer>

  <script src="script.js"></script>
</body>
</html>

/* style.css */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Poppins', sans-serif;
}

body {
  background: #fff8f0;
  color: #333;
}

header {
  background: #ff6f61;
  padding: 1rem 2rem;
  color: white;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

header h1 {
  font-size: 1.8rem;
}

nav a {
  color: white;
  margin-left: 20px;
  text-decoration: none;
  font-weight: 500;
}

.hero {
  text-align: center;
  padding: 4rem 2rem;
  background: #ffe4e1;
}

.hero h2 {
  font-size: 2.5rem;
  margin-bottom: 1rem;
}

.hero button {
  padding: 0.8rem 2rem;
  background: #ff6f61;
  color: white;
  border: none;
  border-radius: 5px;
  font-size: 1rem;
  cursor: pointer;
}

.products {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 2rem;
  padding: 3rem 2rem;
}

.product-card {
  background: white;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0,0,0,0.1);
  padding: 1rem;
  text-align: center;
  transition: transform 0.3s;
}

.product-card:hover {
  transform: translateY(-5px);
}

.product-card img {
  width: 100%;
  border-radius: 10px;
}

.product-card h3 {
  margin: 1rem 0 0.5rem;
}

.product-card button {
  padding: 0.5rem 1.5rem;
  background: #ff6f61;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

footer {
  background: #333;
  color: white;
  text-align: center;
  padding: 1rem;
  margin-top: 2rem;
}



// script.js
function scrollToProducts() {
  document.getElementById("products").scrollIntoView({ behavior: "smooth" });
}

function addToCart(item) {
  alert(item + " has been added to your cart!");
}


