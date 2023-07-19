<template>
    <div>

    </div>
</template>
  
  <script>
  export default {
    data() {
    return {
      name: '',
      category: '',
      detail: '',
      description: '',
      price: '',
      photo: null
    }
  },
  methods: {
    handlePhoto(event) {
      this.photo = event.target.files[0];
    },
    async addProduct() {
      const formData = new FormData();
      formData.append('name', this.name);
      formData.append('category', this.category);
      formData.append('detail', this.detail);
      formData.append('description', this.description);
      formData.append('price', this.price);
      formData.append('photo', this.photo);
      await axios.post('/api/products', formData,); {
        // eslint-disable-next-line no-empty
        headers: {
        }
      }
    }
  }

  };
  </script>