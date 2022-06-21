<template>
  <div class="shadow-md rounded-sm">
    <div class="">
      <img
        :src="data.cover"
        class="w-full h-full object-center object-cover group-hover:opacity-75"
      />
    </div>
    <div class="p-2">
      <p class="text-sm text-gray-500 cttext">{{data.name}}</p>
      <p class="text-blue-600 font-semibold">Rp. 30.000</p>
      <div class="flex flex-cols justify-between">
        <p>kucing</p>
        <p>meow</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Product",
  props:[
      "data"
  ]
};
</script>

<style>
.cttext {
    overflow: hidden;
    display: -webkit-box;
    -webkit-line-clamp: 1;
    -webkit-box-orient: vertical;
}
</style>