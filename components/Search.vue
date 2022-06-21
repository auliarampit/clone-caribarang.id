<template>
  <div class="flex items-center lg:mx-36 md:mx-10 mx-5">
    <div class="flex relative flex-col mt-16 justify-center w-32">
      <button
        id="dropdownDefault"
        v-on:click="handleShow"
        class="
          text-gray-600er
          bg-transparent
          cursor-pointer
          font-semibold
          text-sm
          px-4
          text-center
          inline-flex
          items-center
          border border-gray
          h-10
          focus:outline-none focus:transparent
          rounded-l-lg
        "
        type="button"
      >
        Keyword
        <svg
          class="w-4 h-4 ml-2"
          fill="none"
          stroke="currentColor"
          viewBox="0 0 24 24"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M19 9l-7 7-7-7"
          ></path>
        </svg>
      </button>
      <!-- Dropdown menu -->
      <div
        id="dropdown"
        v-bind:class="{ hidden: !show }"
        style="position: absolute; top: 40px"
        class="bg-white divide-y divide-gray rounded shadow w-32 dark:bg-gray"
      >
        <div
          class="py-1 text-sm text-gray dark:text-gray text-left"
          aria-labelledby="dropdownDefault"
        >
          <a
            href="#"
            class="
              block
              px-4
              py-2
              hover:bg-gray
              dark:hover:bg-gray dark:hover:text-white
            "
            >Dashboard</a
          >

          <a
            href="#"
            class="
              block
              px-4
              py-2
              hover:bg-gray
              dark:hover:bg-gray dark:hover:text-white
            "
            >Settings</a
          >

          <a
            href="#"
            class="
              block
              px-4
              py-2
              hover:bg-gray
              dark:hover:bg-gray dark:hover:text-white
            "
            >Earnings</a
          >

          <a
            href="#"
            class="
              block
              px-4
              py-2
              hover:bg-gray
              dark:hover:bg-gray dark:hover:text-white
            "
            >Sign out</a
          >
        </div>
      </div>
    </div>
    <div
      class="
        flex
        relative
        mt-16
        items-center
        justify-between
        px-5
        w-full
        border-r border-b border-t border-gray
        rounded-r-lg
        h-10
      "
    >
      <input
        placeholder="Search"
        type="text"
        @input="handleInput($event)"
        class="w-full h-full focus:outline-none"
      />
      <button
        v-on:click="clickSearch"
        class="
          inline-flex
          items-center
          pr-2
          pl-2
          -mr-5
          h-full
          border border-blue-600
          text-sm
          rounded-r-lg
          font-auto
          text-lg text-white
          bg-blue-600
          focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo
        "
      >
        <svg
          class="h-5"
          xmlns="http://www.w3.org/2000/svg"
          x="0px"
          y="0px"
          width="30"
          height="30"
          viewBox="0 0 30 30"
        >
          <path
            fill="#FFF"
            d="M 13 3 C 7.4889971 3 3 7.4889971 3 13 C 3 18.511003 7.4889971 23 13 23 C 15.396508 23 17.597385 22.148986 19.322266 20.736328 L 25.292969 26.707031 A 1.0001 1.0001 0 1 0 26.707031 25.292969 L 20.736328 19.322266 C 22.148986 17.597385 23 15.396508 23 13 C 23 7.4889971 18.511003 3 13 3 z M 13 5 C 17.430123 5 21 8.5698774 21 13 C 21 17.430123 17.430123 21 13 21 C 8.5698774 21 5 17.430123 5 13 C 5 8.5698774 8.5698774 5 13 5 z"
          ></path>
        </svg>
        cari
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: "Search",
  props: {
    handleInput: Function,
    clickSearch: Function,
    inputSearch: String,
  },
};
</script>