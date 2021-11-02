<template>
  <div>
    <div class="name">
      <label for="username">Username: </label>
      <h2 id="username">{{ Username }}</h2>
    </div>
    <div class="age">
      <label for="age">Age: </label>
      <h3 id="age">{{ age }}</h3>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    Username: {
      type: String,
      required: true,
    },
    age: {
      type: String,
      required: true,
    },
  },
  data() {
    return {};
  },
};
</script>
<style scoped>
.name h2 {
  display: inline;
  padding-left: 10px;
}
label {
  font-weight: bold;
}
.age h3 {
  display: inline;
  padding-left: 10px;
}
</style>
