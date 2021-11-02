<template>
  <section>
    <user-data @add-user="addUser" />
    <active-user
      v-for="user in users"
      :key="user.id"
      :Username="user.Username"
      :age="user.age"
    />
  </section>
</template>

<script>
export default {
  data() {
    return {
      users: [
        {
          id: '1',
          Username: 'Ronaldo',
          age: '36',
        },
        {
          id: '2',
          Username: 'Messi',
          age: '34',
        },
      ],
    };
  },
  methods: {
    addUser(Username, age) {
      const newUser = {
        id: new Date().toISOString(),
        Username: Username,
        age: age,
      };

      this.users.push(newUser);
    },
  },
};
</script>
