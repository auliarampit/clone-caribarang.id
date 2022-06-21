<template>
  <div>
    <Navbar />
    <Search :handleInput="search" :clickSearch="clickSearch"  />
    <div
      class="
        mt-16
        lg:px-36
        md:px-10
        px-5
        grid grid-cols-2
        gap-5
        lg:grid-cols-6
        md:grid-cols-5
        sm:grid-cols-3
      "
    >
      <Product v-for="product of products" :key="product.id" :data="product" />
    </div>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import axios from "axios";

export default Vue.extend({
  components: {},
  name: "IndexPage",
  methods: {
    search: function (searchText: any) {
      // this.products = this.productsData.filter((e: any) => e.name.includes(searchText.target.value))
      this.inputSearch = searchText.target.value
    },
    clickSearch: function() {
      this.products = this.productsData.filter((e: any) => e.name.includes(this.inputSearch))
    }
  },

  data() {
    return {
      products: [],
      productsData: [],
      inputSearch: "",
    };
  },
  async mounted() {
    axios.get("https://api.caribarang.id/api/products?page=1").then((res) => {
      this.products = res.data.data;
      this.productsData = res.data.data;
    });
  },
});
</script>


