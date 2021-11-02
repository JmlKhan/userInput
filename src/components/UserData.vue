<template>
  <form @submit.prevent="submitData">
    <div>
      <label for="Username">Username: </label>
      <input type="text" v-model="Username" />
    </div>
    <div>
      <label for="age">Age: </label>
      <input type="age" v-model="age" />
    </div>
    <div>
      <button>Add User</button>
    </div>
  </form>
</template>

<script>
export default {
  emits: ['add-user'],
  data() {
    return {
      Username: '',
      age: '',
    };
  },
  methods: {
    submitData() {
      this.$emit('add-user', this.Username, this.age);
    },
  },
};
</script>
