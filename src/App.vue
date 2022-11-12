<template>
  <section>
    <user-data @add-contact="addContact"> </user-data>
    <br />

    <ul class="ul-class">
      <active-user v-for="user in users"
        :key="user.id"
        :id="user.id"
        :username="user.username"
        :age = "user.age"
        ></active-user>
    </ul>
  </section>
</template>

<script>
import ActiveUser from "./components/ActiveUser.vue";
export default {
  components: { ActiveUser },
  data() {
    return {
      users: [
        {
          id: 'manuel',
          username: 'Manuel Lorenz',
          age: '0123 45678 90',
        },
        {
          id: 'julie',
          username: 'Julie Jones',
          age: '0987 654421 21',
        },
      ],
    };
  },
  methods: {
    addContact(name, age) {
      const newuserContact = {
        id: new Date().toISOString(),
        username: name,
        age: age,

      };
      this.users.push(newuserContact);
    }
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.ul-class
{
  padding: 0%;
}
</style>
