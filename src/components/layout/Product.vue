<template>
  <div class="product">
    <!-- <img
      class="img_container"
      :src="`../assets/productImage/${eachProduct.imageUrl}`"
    /> -->
    <h5>{{ eachProduct.company }}</h5>
    <h3>{{ eachProduct.productName }}</h3>
    <h5>{{ eachProduct.sub }}</h5>
    <div class="price_wrapper">
      <h3 class="price">{{ eachProduct.price }}원</h3>
      <h3 class="sale">-{{ eachProduct.sale }}원</h3>
    </div>
    <h4 class="origin_price">{{ eachProduct.originPrice }}원</h4>
  </div>
</template>
<script>
export default {
  name: "Product",
  props: {
    eachProduct: Object,
    cssValues: Object,
  },

  data() {
    return {};
  },
};
</script>
<style>
.product {
  background-color: white;
  color: black;
  width: calc(100% / 4);
  min-width: 200px;

  display: flex;
  flex-direction: column;
  padding: 10px;
}
.img_container {
  min-width: 180px;
  product: 1px solid grey;
  min-height: 200px;
}
.price_wrapper {
  display: flex;
}
.price {
  font-weight: 800;
}
.sale {
  margin-left: 10px;
  color: red;
  font-weight: 800;
}
.origin_price {
  text-decoration: line-through;
  color: gray;
  font-weight: 700;
}
</style>
