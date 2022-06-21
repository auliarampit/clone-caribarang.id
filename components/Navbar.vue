<template>
  <div class="flex justify-between md:justify-around shadow p-4 items-center">
    <div class="flex justify-between">
      <a href="#pablo">
        <img
          src="https://caribarang.oss-ap-southeast-1.aliyuncs.com/assets/logo-navbar.png"
          alt="Caribarang Logo"
          class="h-8 w-auto md:block"
        />
      </a>
    </div>

    <div class="md:flex items-center">
      <ul class="flex flex-col md:flex-row list-none ml-auto">
        <a href="/" class="font-extrabold text-blue-600 md:block hidden"
          >Produk 1688.com</a
        >
        <p class="font-extrabold text-gray-500 ml-10 md:block hidden">
          Produk Lokal Indonesia
        </p>
      </ul>

      <button
        class="
          text-black
          cursor-pointer
          text-xl
          leading-none
          px-3
          py-1
          border border-solid border-transparent
          rounded
          bg-transparent
          block
          outline-none
          lg:hidden
          focus:outline-none
        "
        type="button"
      >
        <svg
          class="w-6 h-6 text-gray-500"
          x-show="!showMenu"
          fill="none"
          stroke-linecap="round"
          stroke-linejoin="round"
          stroke-width="2"
          viewBox="0 0 24 24"
          stroke="currentColor"
        >
          <path d="M4 6h16M4 12h16M4 18h16"></path>
        </svg>
      </button>
    </div>

    <div class="hidden lg:block">
      <ul class="flex flex-col lg:flex-row list-none ml-auto">
        <button
          class="
            ml-6
            inline-flex
            items-center
            px-6
            py-2
            border border-transparent
            text-sm
            font-medium
            rounded-lg
            shadow-sm
            text-white
            bg-blue-600
            focus:outline-none
            focus:ring-2
            focus:ring-offset-2
            focus:ring-indigo
          "
        >
          Masuk
        </button>
        <button
          class="
            ml-6
            inline-flex
            items-center
            px-6
            py-2
            border border-blue-600
            text-sm
            font-medium
            rounded-lg
            shadow-sm
            text-blue-600
            bg-transparent
            focus:outline-none
            focus:ring-2
            focus:ring-offset-2
            focus:ring-indigo
          "
        >
          Daftar
        </button>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "Navbar",
};
</script>