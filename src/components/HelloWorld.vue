<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h3>Con <span class="emoji">❤️</span> desde el team hacia el team</h3>
    <span style="font-size: 0.7em; font-style: italic ">Sistemas FUMH &copy;</span>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.emoji {
  font-family: apple color emoji, segoe ui emoji, noto color emoji,
    android emoji, emojisymbols, emojione mozilla, twemoji mozilla,
    segoe ui symbol;
}
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
a {
  color: #42b983;
}
</style>
