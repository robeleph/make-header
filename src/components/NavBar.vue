<template>
  <div class="hello flex justify-between p-2">
    <div>
      <ul>
        <li><a href="/" id="a">>></a></li>
        <li>
          <a href="/" id="a"
            ><span class="material-symbols-outlined align-middle px-2"
              >import_contacts</span
            >Main</a
          >
        </li>
        <li><a id="a">/</a></li>
        <li><a href="/" id="a" rel="noopener">Getting Started</a></li>
        <li><a id="a">/</a></li>
        <li>
          <a href="/" id="a" rel="noopener"
            >Front-end developer test pro...</a
          >
        </li>
      </ul>
    </div>
    <div>
      <ul>
        <li>
          <a href="/" id="a" rel="noopener" class="text-end"
            ><span class="material-symbols-outlined text-lg align-middle">
              lock
            </span>
            Editing</a
          >
        </li>
        <li>
          <span
          id="vertical"
          class="align-middle"
        ></span>
        </li>
        <li id="public-text">
          <a href="/" class="text-end">Publish Space </a>
          <span class="material-symbols-outlined align-middle px-2">
            expand_more
          </span>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "NavBar",
  props: {
    msg: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
#a {
  color: #8c8f8d;
}
h1 {
  font-size: 30px;
  color: red;
  text-transform: uppercase;
  text-align: center;
  margin: 0 0 35px 0;
  text-shadow: 0px 1px 0px #f2f2f2;
}
#vertical {
  border-left: 1px solid gray;
  height: 20px;
}
#public-text {
  color: blue;
}
</style>
