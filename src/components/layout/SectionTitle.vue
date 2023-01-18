<template>
  <div class="section_title_wrapper">
    <div class="title">{{ listTitle }}</div>
    <div class="sub_title">{{ subTitle }}</div>
  </div>
</template>
<script>
export default {
  name: "SectionTitle",
  props: {
    listTitle: String,
    subTitle: String,
  },
};
</script>
<style>
.section_title_wrapper {
  height: 60px;
  color: white;
  color: black;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 30px;
  background-color: white;
}
.title {
  font-size: 25px;
  font-weight: 700;
}
.sub_title {
  font-size: 15px;
  color: black;
}
</style>
