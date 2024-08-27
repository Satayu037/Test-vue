<script setup>

const products = [
  {
    imageSrc: '/image/1.png',
    title: 'กระโปรงนักศึกษาผ้ายาว',
    price: '฿99.00',
    details: '1.1K ชิ้น | ⭐⭐⭐⭐⭐(999+) กรุงเทพมหานคร'
  },
  {
    imageSrc: '/image/pic2.png',
    title: 'กระโปรงนักศึกษาสั้น',
    price: '฿100.00',
    details: '143 ชิ้น | ⭐⭐⭐⭐⭐(999+) กรุงเทพมหานคร'
  },
  {
    imageSrc: '/image/pic3.png',
    title: 'กระโปรงนักศึกษาเอวยาว',
    price: '฿129.00',
    details: '435 ชิ้น | ⭐⭐⭐⭐⭐(999+) กรุงเทพมหานคร'
  },
  {
    imageSrc: '/image/pic4.png',
    title: 'กระโปรงนักศึกษาผ้ายาว',
    price: '฿99.00',
    details: '932 ชิ้น | ⭐⭐⭐⭐⭐(999+) ปทุมธานี'
  }
]

</script>

<template>
  <header>

    <div id="app">
      <div class="product-grid">
        <div v-for="(product, index) in products" :key="index" class="product-card">
          <img :src="product.imageSrc" :alt="product.title">
          <div class="product-info">
            <h3>{{ product.title }}</h3>
            <p class="price">{{ product.price }}</p>
            <p>{{ product.details }}</p>
          </div>
        </div>
      </div>
    </div>
  </header>

  <main>
    <TheWelcome />
  </main>
</template>

<style>
body {
  font-family: Arial, sans-serif;
  background-color: #f8f8f8;
  margin: 0;
  padding: 20px;
}

.product-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 30px;

}

.product-card {
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 10px;
  overflow: hidden;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  text-align: center;
  padding: 20px;
  width: 300px;
  height: 550px;
}

.product-card img {
  width: 100%;
  height: auto;
}

.product-info h3 {
  font-size: 18px;
  margin: 15px 0 10px 0;
}

.product-info .price {
  color: #ff9500 !important;
  font-weight: bold;
  font-size: 18px;
}

.p {
  color: #ff9500;
}

@media (max-width: 768px) {
  .product-grid {
    grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
  }

  .product-info h3 {
    font-size: 16px;
  }

  .product-info .price {
    font-size: 16px;
  }
}

@media (max-width: 480px) {
  .product-grid {
    grid-template-columns: 1fr;
  }

  .product-info h3 {
    font-size: 14px;
  }

  .product-info .price {
    font-size: 14px;
  }
}
</style>