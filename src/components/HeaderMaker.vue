<template>
  <div>
    <div v-for="list in lists" :key="list.text">
      <h1 v-if="list.ish1mode">{{ list.text }}</h1>
      <p v-if="!list.ish1mode">{{list.text}}</p>
    </div>
    <div v-if="lists.length > 0">
      <button
        @click="clear"
        class="capitalize py-2 px-4 font-semibold rounded-md text-white bg-red-600 my-2"
      >
        Clear
      </button>
    </div>
    <textarea v-if="!h1mode"
      id="smaller-text"
      @keyup="checkVal($event)"
      v-model="inputValue"
      rows="4"
      cols="62"
      class="block p-2.5 text-gray-900 rounded-lg border border-gray-30 focus:ring-blue-500 focus:border-blue-50 dark:bg-gray-700 dark:border-gray-60 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-50"
      placeholder="Type / for blocks, @ to link docs or people"
    ></textarea>
    <textarea
      v-else
      @keyup="printHeader($event)"
      v-model="h1message"
      rows="3"
      cols="34"
      class="block p-2.5 text-3xl text-gray-900 rounded-lg focus:ring-blue-500 focus:border-blue-500 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
      placeholder="Heading 1"
    ></textarea>
    <HeaderOptionCard @h1Triggerd="proptHeader" v-if="showHeaderOption" class="mb-20" />
  </div>
</template>

<script>
import HeaderOptionCard from "./HeaderOptionCard.vue"
export default {
  name: "HeaderMaker",
  components: {
    HeaderOptionCard,
  },
  data() {
    return {
      inputValue: "",
      lists: [],
      h1mode: false,
      h1message: "",
      showHeaderOption: false,
    };
  },
  methods: {
    checkVal(event) {
      if (this.inputValue == "/1" && event.key != "Backspace") {
        this.showHeaderOption = true
      }
      if (event.key == "Enter") {
        this.lists.push({text: this.inputValue, ish1mode: false});
        this.inputValue = "";
      }
    },
    printHeader(event) {
        if(event.key == "Enter") {
            this.lists.push({text: this.h1message, ish1mode: true})
            this.h1mode = false;
            this.h1message = "";
        }
    },
    proptHeader() {
        this.showHeaderOption = false;
        this.h1mode = true;
        this.inputValue = "";
    },
    clear() {
      this.lists = [];
    }
  },
};
</script>
<style scoped>
h1 {
  @apply text-3xl;
}
</style>
