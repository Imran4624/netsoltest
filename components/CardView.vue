<template>
  <div class="card">
    <img :src="product.imageUrl" alt="Card Image" class="card-image" />
    <div class="card-details">
      <div class="card-type">{{ product.type }}</div>
      <h2 class="card-title">{{ product.title }}</h2>
      <p class="card-description">{{ product.description }}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    product: {
      type: Object,
      required: true,
    },
  },
};
</script>

<style scoped>
.card {
  border: none;
  border-radius: 8px;
  display: flex;
  flex-direction: column;
  max-width: 354px;
}

.card-image {
  width: 100%;
  height: auto;
  border-top-left-radius: 8px;
  border-top-right-radius: 8px;
}

.card-details {
  border: none;
}

.card-type {
  font-size: 14px;
  color: #18ebfe;
  font-weight: 700;
  background-color: #ffffff1a;
  padding: 2px;
  width: 41px;
  margin-top: 8px;
  text-align: center;
}

.card-title {
  font-size: 24px;
  font-weight: 500;
  margin: 0;
  padding: 10px 0px;
  color: #ffffff;
}

.card-description {
  font-size: 18px;
  font-weight: 400;
  margin: 0;
  padding: 0;
  color: #ffffff;
}
</style>
