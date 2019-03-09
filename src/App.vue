<template>
  <div id="app">
    <h3>SVG tag with dynamic path</h3>
    <svg-path-icon v-for="name in iconNames" :key="name + '_a'" :name="name" />

    <h3>IMG tag with dynamic source</h3>
    <svg-img-icons v-for="name in iconNames" :key="name + '_b'" :name="name" />

    <h3>Inline SVG markup</h3>
    <svg-inline-icons />
  </div>
</template>

<script>
import SvgPathIcon from "./components/SvgPathIcon.vue";
import SvgImgIcons from "./components/SvgImgIcons.vue";
import SvgInlineIcons from "./components/SvgInlineIcons.vue";

export default {
  name: "app",
  data() {
    return {
      iconNames: [
        "currency-1",
        "debit-6",
        "shipping-box-11",
        "shipping-box-2",
        "shipping-box-3",
        "shop-1",
        "shopping-bag-7",
        "shopping-cart-2",
        "shopping-cart-3",
        "shopping-cart-5"
      ]
    };
  },
  components: {
    SvgPathIcon,
    SvgImgIcons,
    SvgInlineIcons
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

svg,
img {
  margin: 8px;
}
</style>
