<template>
  <div>
    <button v-if="isAdded" class="btn btn-outline-primary w-100 active" @click.stop>Added</button>
    <button v-else class="btn btn-outline-primary w-100" @click.stop="addToCart">Add to Cart</button>
  </div>
</template>

<script>
export default {
  name: "AddToCartButton",
  data() {
    return {
      isAdded: false
    }
  },
  methods: {
    addToCart() {
      this.isAdded = true
    }
  },
}
</script>

<style scoped>

</style>