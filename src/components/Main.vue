<template>
  <div class="main">
    <ProductList :cssValues="values" />
    <div class="input_manager_container">
      <div class="input_title">컬럼수</div>
      <input type="number" min="1" v-model="values.columnCount" />
      <div class="input_title">브랜드명</div>
      <div class="input_container">
        <div class="input_wrapper">
          글씨색상
          <input type="text" v-model="values.brandColor" />
        </div>
        <div class="input_wrapper">
          글씨크기
          <input type="number" v-model="values.brandFontSize" min="10" />
        </div>
      </div>
      <div class="input_title">상품명</div>
      <div class="input_container">
        <div class="input_wrapper">
          글씨색상
          <input type="text" v-model="values.productColor" />
        </div>
        <div class="input_wrapper">
          글씨크기
          <input type="number" v-model="values.productFontSize" min="10" />
        </div>
      </div>
      <div class="input_title">설명</div>
      <div class="input_container">
        <div class="input_wrapper">
          글씨색상
          <input type="text" v-model="values.subColor" />
        </div>
        <div class="input_wrapper">
          글씨크기
          <input type="number" v-model="values.subFontSize" min="10" />
        </div>
      </div>
      <div class="input_title">판매금액</div>
      <div class="input_container">
        <div class="input_wrapper">
          글씨색상
          <input type="text" v-model="values.priceColor" />
        </div>
        <div class="input_wrapper">
          글씨크기
          <input type="number" v-model="values.priceFontSize" min="10" />
        </div>
      </div>
      <div class="input_title">할인금액</div>
      <div class="input_container">
        <div class="input_wrapper">
          글씨색상
          <input type="text" v-model="values.saleColor" />
        </div>
        <div class="input_wrapper">
          글씨크기
          <input type="number" v-model="values.saleFontSize" min="10" />
        </div>
      </div>
      <div class="input_title">원가</div>
      <div class="input_container">
        <div class="input_wrapper">
          글씨색상
          <input type="text" v-model="values.originPriceColor" />
        </div>
        <div class="input_wrapper">
          글씨크기
          <input type="number" v-model="values.originPriceFontSize" min="10" />
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import ProductList from "./layout/ProductList.vue";
import Header from "./layout/Header.vue";
export default {
  name: "Main",
  components: {
    ProductList,
    Header,
  },
  data: function () {
    return {
      values: {
        columnCount: "3",
        brandColor: "",
        brandFontSize: 12,
        productColor: "",
        productFontSize: 15,
        subColor: "",
        subFontSize: 13,
        priceColor: "",
        priceFontSize: 18,
        saleColor: "",
        saleFontSize: 15,
      },
    };
  },
  methods: {},
};
</script>
<style>
.main {
  display: flex;
  background-color: white;
}
.input_manager_container {
  width: 40%;
  background-color: white;
  color: black;
  padding: 10px;
}
.input_container {
  display: flex;
  flex-direction: column;
}

p {
  min-width: 70px;
}
.input_title {
  width: 200px;
  margin-bottom: 5px;
  font-weight: 700;
}
input {
  margin-bottom: 5px;
}
</style>
