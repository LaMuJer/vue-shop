<template>
  <div class="d-flex flex-row-reverse">
    <i v-for="n in 5" :key="n" :class="['fa-solid fa-star',{'text-warning':n<=star}]"></i>
  </div>
</template>

<script>
export default {
  props: {
    rating: {
      type: Object,
      required : true
    },
  },
  computed: {
    star() {
      return Math.ceil(this.rating.rate)
    }
  },
}
</script>

<style scoped>

</style>