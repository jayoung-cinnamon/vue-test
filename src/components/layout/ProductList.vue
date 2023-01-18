<template>
  <div>
    <SectionTitle :listTitle="listTitle" :subTitle="subTitle" />
    <div class="product_list">
      <div
        class="product"
        :style="`width:calc(100%/${Product.columnCount})`"
        v-for="(Product, i) in ProductList"
        :key="i"
      >
        <img
          class="img_container"
          :src="`src/assets/productImage/${Product.imageUrl}`"
        />
        <h5
          :style="{
            fontSize: cssValues.brandFontSize + 'px',
            color: cssValues.brandColor,
          }"
        >
          {{ Product.company }}
        </h5>
        <h3
          :style="{
            fontSize: cssValues.productFontSize + 'px',
            color: cssValues.productColor,
          }"
        >
          {{ Product.productName }}
        </h3>
        <h5
          :style="{
            fontSize: cssValues.subFontSize + 'px',
            color: cssValues.subColor,
          }"
        >
          {{ Product.sub }}
        </h5>
        <div class="price_wrapper">
          <h3
            :style="{
              fontSize: cssValues.priceFontSize + 'px',
              color: cssValues.priceColor,
            }"
            class="price"
          >
            {{ Product.price }}원
          </h3>
          <h3
            :style="{
              fontSize: cssValues.saleFontSize + 'px',
              color: cssValues.saleColor,
            }"
            class="sale"
          >
            -{{ Product.sale }}원
          </h3>
        </div>
        <h4
          :style="{
            fontSize: cssValues.originPriceFontSize + 'px',
            color: cssValues.originPriceColor,
          }"
          class="origin_price"
        >
          {{ Product.originPrice }}원
        </h4>
      </div>
    </div>
  </div>
</template>

<script>
import Product from "./Product.vue";
import SectionTitle from "./SectionTitle.vue";
export default {
  props: {
    cssValues: Object,
  },
  name: "ProductList",
  components: {
    Product,
    SectionTitle,
  },
  data() {
    return {
      listTitle: "신상품",
      subTitle: "새로운 상품을 만나보세요",
      ProductList: [
        {
          imageUrl: "샘표.jpeg",
          company: "샘표",
          productName: "진간장 금S 1.8L",
          sub: "언제나 함께해 온 그 맛",
          price: 4500,
          sale: 3650,
          originPrice: 8150,
        },
        {
          imageUrl: "모카골드.jpeg",
          company: "동서식품",
          productName: "[맥심]모카골드 250T",
          sub: "커피 한 잔의 여유",
          price: 27900,
          sale: 3600,
          originPrice: 31500,
          originPrice: 8980,
        },
        {
          imageUrl: "동원부추.jpeg",
          company: "동원",
          productName: "딤섬 부추 창편390g x 2개입",
          sub: "소스와 함께먹는 부드러운",
          price: 6980,
          sale: 2000,
          originPrice: 8980,
        },
        {
          imageUrl: "동원부추.jpeg",
          company: "동원",
          productName: "딤섬 샤오롱바오 390g x 2개입",
          sub: "고소한 육즙 가득",
          price: 6980,
          sale: 2000,
          originPrice: 8980,
        },
        {
          imageUrl: "동원부추.jpeg",
          company: "동원",
          productName: "딤섬 샤오롱바오 390g x 2개입",
          sub: "고소한 육즙 가득",
          price: 6980,
          sale: 2000,
          originPrice: 8980,
        },
        {
          imageUrl: "동원부추.jpeg",
          company: "동원",
          productName: "딤섬 샤오롱바오 390g x 2개입",
          sub: "고소한 육즙 가득",
          price: 6980,
          sale: 2000,
          originPrice: 8980,
        },
        {
          imageUrl: "동원부추.jpeg",
          company: "동원",
          productName: "딤섬 샤오롱바오 390g x 2개입",
          sub: "고소한 육즙 가득",
          price: 6980,
          sale: 2000,
          originPrice: 8980,
        },
        {
          imageUrl: "동원부추.jpeg",
          company: "동원",
          productName: "딤섬 샤오롱바오 390g x 2개입",
          sub: "고소한 육즙 가득",
          price: 6980,
          sale: 2000,
          originPrice: 8980,
        },
        {
          imageUrl: "동원부추.jpeg",
          company: "동원",
          productName: "딤섬 샤오롱바오 390g x 2개입",
          sub: "고소한 육즙 가득",
          price: 6980,
          sale: 2000,
          originPrice: 8980,
        },
      ],
    };
  },
};
</script>

<style scoped>
.product_list {
  width: 100%;
  gap: 0px 0%;
  /* min-width: 300px; */
  display: flex;
  flex-wrap: wrap;
}
@media (min-width: 1024px) {
}
.product {
  background-color: white;
  color: black;
  min-width: calc(100% / 4);

  display: flex;
  flex-direction: column;
  padding: 10px;
}
.img_container {
  min-width: 180px;
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
  line-height: 25px;
}
.origin_price {
  text-decoration: line-through;
  color: gray;
  font-weight: 700;
}
</style>
