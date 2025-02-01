<template>
    <div id="app">
      <header>
        <h1>Genius Plays</h1>
      </header>
  
      <main>
        <section class="product-showcase">
          <h2>Graded Trading Card Display Cases</h2>
          <div class="product-grid">
            <div v-for="product in products" :key="product.id" class="product-item">
              <img :src="product.image" :alt="product.name" class="product-img">
              <h3>{{ product.name }}</h3>
              <p>{{ product.description }}</p>
              <button @click="addToCart(product)" class="add-to-cart">Add to Cart</button>
            </div>
          </div>
        </section>
      </main>
  
      <footer>
        <p>&copy; 2025 Genius Plays. All rights reserved.</p>
      </footer>
    </div>
  </template>
  
  <script>
  export default {
    name: 'App',
    data() {
      return {
        products: [
          {
            id: 1,
            name: 'Elite Case',
            description: 'Perfect for showcasing your prized cards.',
            // image: 'path/to/elite-case.jpg'
          },
          {
            id: 2,
            name: 'Standard Case',
            description: 'Affordable and functional for everyday use.',
            // image: 'path/to/standard-case.jpg'
          },
          // Add more products as needed
        ]
      };
    },
    methods: {
      addToCart(product) {
        // Here you would implement cart functionality, 
        // but for now, we'll just log it.
        console.log(`Added ${product.name} to cart`);
        alert(`Added ${product.name} to cart`);
      }
    }
  }
  </script>
  
  <style>
  body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
  }
  
  #app {
    display: flex;
    flex-direction: column;
    min-height: 100vh;
  }
  
  header {
    background-color: #232f3e;
    color: white;
    text-align: center;
    padding: 1rem;
  }
  
  main {
    flex: 1;
    padding: 2rem;
    background-color: #f0f0f0;
  }
  
  .product-showcase {
    text-align: center;
  }
  
  .product-grid {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
  }
  
  .product-item {
    margin: 1rem;
    padding: 1rem;
    background: white;
    border-radius: 8px;
    box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    width: 200px;
  }
  
  .product-img {
    width: 100%;
    height: auto;
    border-radius: 4px;
  }
  
  .add-to-cart {
    background-color: #FFA41C;
    border: none;
    color: white;
    padding: 10px 20px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 14px;
    margin: 4px 2px;
    cursor: pointer;
    border-radius: 4px;
  }
  
  footer {
    background-color: #232f3e;
    color: white;
    text-align: center;
    padding: 1rem;
  }
  </style>