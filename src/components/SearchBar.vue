<template>
  <div>
    <form class="flex items-center mt-6 mb-6">
      <label for="voice-search" class="sr-only">Search</label>
      <div class="relative w-full">
        <div
          id="p"
          class="flex absolute inset-y-0 left-0 items-center pointer-events-none pl-2"
        >
          <p>P</p>
        </div>
        <div
          id="vertical"
          class="flex absolute inset-y-0 left-9 items-center pl-3 pointer-events-none mt-3"
        ></div>
        <div
          class="flex absolute inset-y-0 left-8 items-center pl-3 pointer-events-none"
        >
          <span class="material-symbols-outlined"> schedule </span>
        </div>
        <div
          id="vertical"
          class="flex absolute inset-y-0 ml-14 left-16 items-center pl-9 pointer-events-none mt-3"
        ></div>
        <div
          class="flex text-gray-500 absolute inset-y-0 left-11 items-center pl-8 pointer-events-none"
        >
          <p>0min</p>
        </div>
        <div
          class="flex text-gray-500 absolute inset-y-0 left-11 items-center ml-12 pl-9 pointer-events-none"
        >
          <span class="material-symbols-outlined"> account_circle </span>
        </div>
        <div
          id="vertical"
          class="flex absolute inset-y-0 ml-24 left-16 items-center pl-11 pointer-events-none mt-3"
        ></div>
        <div
          class="flex text-gray-500 absolute inset-y-0 left-11 items-center ml-24 pl-9 pointer-events-none"
        >
        <span class="material-symbols-outlined">
          call_received
        </span>
        </div>
        <input
          type="text"
          id="voice-search"
          class="border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full pl-52 p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
          placeholder="0"
          required=""
        />
        <button
          type="button"
          class="flex absolute inset-y-0 right-0 items-center pr-1"
        >
          <span class="material-symbols-outlined"> more_vert </span>
        </button>
        <button
          type="button"
          class="flex absolute inset-y-0 right-4 items-center pr-2 text-blue-200"
        >
          <span class="material-symbols-outlined"> cloudy </span>
        </button>
        <button
          type="button"
          class="flex absolute inset-y-0 right-11 items-center pr-2"
        >
          <span class="material-symbols-outlined"> task_alt </span>
        </button>
      </div>
    </form>
  </div>
</template>
<script>
export default {
  name: "SearchBar",
};
</script>

<style scoped>
#vertical {
  border-left: 1px solid gray;
  height: 20px;
}
#p {
  background-color: aqua;
  margin-bottom: 5px;
  padding-right: 5px;
  margin-top: 5px;
  margin-left: 5px;
}
</style>
