<template>
  <div>
    <NavBar msg="Welcom here"/>
    <div class="center space-y-6">
      <SearchBar />
      <Instruction />
      <HeaderMaker />
  </div>
  </div>
</template>

<script>
import NavBar from "./NavBar.vue";
import SearchBar from "./SearchBar.vue";
import HeaderMaker from "./HeaderMaker.vue";
import Instruction from "./Instruction.vue";
export default {
  name: 'Home',
  components: {
    NavBar,
    SearchBar,
    HeaderMaker,
    Instruction
}
}
</script>
<style scoped>
  .center {
    margin-left: 25%;
    margin-right: 25%
  }
</style>

