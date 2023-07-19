<template>
  <div class="bg-blue">
    
  <div class="bg-blue-800">
    <div class="container mx-auto flex justify-between items-center py-4">
      <div class="flex items-center">
        <button class="text-white font-bold mr-4">Clothing</button>
        <button class="text-white font-bold mr-4">Living</button>
        <button class="text-white font-bold mr-4">Archive</button>
        <button class="text-white font-bold">Search</button>
      </div>
      <h1 class="text-white text-2xl font-bold">RODEN GRAY</h1>
      <div class="flex items-center">
        <button class="text-white font-bold mr-4">CAD</button>
        <button class="text-white font-bold mr-4">Account</button>
        <button class="text-white font-bold mr-4">Bag(0)</button>
      </div>
    </div>
  </div>

    <div class="bg-white top-0 left-0 right-0 mx-auto max-w-4xl py-4">
      <h1 class="text-blue-500 text-2xl font-bold text-center mb-4">New Arrivals</h1>
      <div class="flex justify-between items-center px-4 mb-4">
        <div class="flex items-center">
          <button class="text-gray-500 font-bold mr-40" @click="sortProducts()">Sort</button>
          <button class="text-gray-500 font-bold mr-40" @click="sortProducts()">Alphabetically, A-Z</button>
        </div>
        <button class="bg-gray-500 hover:bg-gray-600 text-white font-bold px-4 py-2 rounded mr-4" @click="showFilters = !showFilters">Filter</button>
        <div class="flex items-center">
          <label for="size-select" class="text-gray-500 font-bold mr-20">Size:</label>
          <select id="size-select" class="border border-gray-500 px-2 py-1" v-model="selectedSize">
            <option value="">All</option>
            <option value="small">Small</option>
            <option value="medium">Medium</option>
            <option value="large">Large</option>
          </select>
          <label for="brand-select" class="text-gray-500 font-bold mx-4">Brand:</label>
          <select id="brand-select" class="border border-gray-500 px-2 py-1" v-model="selectedBrand">
            <option value="">All</option>
            <option value="nike">Nike</option>
            <option value="adidas">Adidas</option>
            <option value="puma">Puma</option>
            <option value="shein">SHEIN</option>
            <option value="dior">DIOR</option>
            <option value="zara">ZARA</option>
          </select>
        </div>
      </div>
      <div v-if="showFilters">
        <!-- Insert filter options here -->
      </div>
    </div>

    <div>
      <div>
        <ul>
          <li><img src=""></li>
        </ul>
      </div>
    </div>

    <div>    
      
    <button @click="showForm = true" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded focus:outline-none focus:shadow-outline">Je veux vendre</button>
    <form v-if="showForm" @submit.prevent="addProduct">

     <form @submit.prevent="addProduct">
      <div class="mb-4">
        <label for="name" class="block text-gray-700 font-bold mb-2">Nom:</label>
        <input type="text" id="name" v-model="name" class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline">
      </div>
      <div class="mb-4">
        <label for="category" class="block text-gray-700 font-bold mb-2">Catégorie:</label>
        <select id="category" class="border border-gray-500 px-2 py-1" v-model="selectedSize">
            <option value="sandales">Sandales</option>
            <option value="basket">Basket</option>
            <option value="tongs">Tongs</option>
            <option value="escarpins">Escarpins</option>
            <option value="sac">Sacs</option>
          </select>
      </div>
      <div class="mb-4">
        <label for="detail" class="block text-gray-700 font-bold mb-2">Détail:</label>
        <input type="text" id="detail" v-model="detail" class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline">
      </div>
      <div class="mb-4">
        <label for="description" class="block text-gray-700 font-bold mb-2">Description:</label>
        <textarea id="description" v-model="description" class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"></textarea>
      </div>
      <div class="mb-4">
        <label for="price" class="block text-gray-700 font-bold mb-2">Prix:</label>
        <input type="number" id="price" v-model="price" class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline">
      </div>
      <div class="mb-4">
        <label for="photo" class="block text-gray-700 font-bold mb-2">Photo:</label>
        <input type="file" id="photo" @change="handlePhoto" class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline">
      </div>
      <button type="submit" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded focus:outline-none focus:shadow-outline">Ajouter le produit</button>
    </form>
    </form>
  </div>
   
   
  <hr class="border-blue-800 my-8">

   
<footer class="bg-white">
  <div class="container mx-auto flex justify-between items-center py-8 px-4">
      <div class="flex items-center">
        <a href="#" class="text-gray font-bold mr-4 hover:text-blue-500">About</a>
        <a href="#" class="text-gray font-bold mr-4 hover:text-blue-500">Customer Care</a>
        <a href="#" class="text-gray font-bold mr-4 hover:text-blue-500">Connect</a>
        <a href="#" class="text-gray font-bold mr-4 hover:text-blue-500">Journal</a>
        <a href="#" class="text-gray font-bold mr-4 hover:text-blue-500">Archive</a>
        <a href="#" class="text-gray font-bold mr-4 hover:text-blue-500">Newsletter</a>

      </div>
      <h1 class="text-blue-800 text-2xl font-bold">RODEN GRAY</h1>
      <div class="flex items-center">
        <p class="text-gray-500">2023 RODEN GRAY. All Rights Reserved</p>
        <a href="#" class="text-gray font-bold mr-4 hover:text-blue-500">Terms &amp; Conditions</a>
        <a href="#" class="text-gray font-bold mr-4 hover:text-blue-500">Privacy Policy</a>


      </div>
  </div>
</footer>

 </div>

</template>

<script>

export default {
  name: 'HelloWorld',
  props: {
  },
  icons:{
    
  },
  images:{

  },
  data() {
    return {
      showForm: false,
      // Les autres propriétés de données nécessaires au formulaire
    }
  },
  methods: {
    addProduct() {
     <button type="submit" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded focus:outline-none focus:shadow-outline">Ajouter le produit</button>
    },
    handlePhoto(event) {
      const file = event.target.files[0];
    if (!file) {
      return;
    }
    this.selectedPhoto = file; 
    },
    // Les autres méthodes nécessaires au formulaire
  }

}
</script>

<style scoped>
  @import 'https://cdn.jsdelivr.net/npm/tailwindcss/dist/tailwind.min.css';
  hr {
    height: 1px;
  }

</style>
