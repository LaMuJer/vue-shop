<template>
  <div>
    <Nav></Nav>
    <RouterView></RouterView>
  </div>
</template>

<script>
import Nav from "@/components/Nav";
export default {
  components: {Nav}
}
</script>

<style>

@import "~bootstrap/dist/css/bootstrap.min.css";
@import "~@fortawesome/fontawesome-free/css/all.min.css";
@import "~animate.css/animate.min.css";

</style>