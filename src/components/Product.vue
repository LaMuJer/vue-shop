<template>
  <div class="col-6 col-md-4 col-xl-3 mb-4">
    <div class="card " @click="toDetail(productDetail.id)">
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
            <AddToCartButton/>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Rating from "@/components/Rating";
import AddToCartButton from "@/components/AddToCartButton";
export default {
  components: {AddToCartButton, Rating},
  props: {
    productDetail: {
      type: Object,
      required : true
    },
  },
  methods: {
    toDetail(productId) {
      this.$router.push({
        name: "productDetail",
        params: {
          id: productId
        }
      })
    }
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