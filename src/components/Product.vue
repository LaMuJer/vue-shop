<template>
  <div class="col-6 col-md-4 col-xl-3 mb-4">
    <div class="card ">
      <div class="card-body ">
        <div class="d-flex flex-column justify-content-between product-card-height">
          <div class="">
            <figure>
              <img :src="productDetail.image" class="product-img" alt="">
            </figure>
            <p>{{ productDetail.title }}</p>
          </div>
          <div class="">
            <div class="d-flex justify-content-between">
              <p>$ {{ productDetail.price }}</p>
              <Rating :rating="productDetail.rating"></Rating>
            </div>
            <button class="btn btn-outline-primary w-100">Add to Cart</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Rating from "@/components/Rating";
export default {
  components: {Rating},
  props: {
    productDetail: {
      type: Object,
      required : true
    },
  },
}
</script>

<style>
.product-img{
  height: 150px;
  max-width: 100%;
}
.product-card-height{
  height: 350px;
}
</style>