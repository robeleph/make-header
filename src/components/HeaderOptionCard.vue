<template>
  <div class="h-120 w-60" id="card">
    <div class="bg-white rounded overflow-hidden shadow-lg">
      <div class="">
        <div class="pl-3 pb-2">
          <p class="text-sm font-medium text-gray-800 leading-none pb-2 pt-2">
            Add blocks
          </p>
          <p class="text-xs text-gray-500">
            Keep typing to filter, or escape to exit
          </p>
        </div>
        <span class="text-sm text-gray-500 pl-3">Filtering keyboard </span
        ><span class="h-1 w-1 rounded-full px-0.5 bg-blue-600 text-white">1</span>
        <button href="#" class="w-full px-4 py-2 pb-2 hover:bg-gray-100 flex" @click="headerOptionClicked">
          <div class="flex gap-3">
						<p class="text-xl block text-gray-500">T</p>
						<div class="flex flex-col">
							<p class="text-sm font-medium mr-16">
                Heading 1
              </p>
              <p class="text-xs text-gray-500">Shortcut: type # + space</p>
						</div>
          </div>
        </button>
        <button href="#" class="w-full px-4 py-2 pb-4 hover:bg-gray-100 flex" @click="headerOptionClicked">
          <div class="flex gap-3">
						<p class="text-xl block text-gray-500">T</p>
						<div class="flex flex-col">
							<p class="text-sm font-medium">
                Expandable Heading 1
              </p>
              <p class="text-xs text-gray-500">Shortcut: type >># + space</p>
						</div>
          </div>
        </button>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "HeaderOptionCard",
  methods: {
    headerOptionClicked() {
        this.$emit('h1Triggerd');
    }
}
};
</script>
<style scoped>
#card {
    position:absolute; 
    left:26%; 
    top:47%;
  }
</style>
