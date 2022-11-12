<template>
  <form class="inputsection" @submit.prevent="submitData">
    <input type="text" v-model="username"/>
    <br />
    <input type="text" v-model="age" />
    <br />
    <button>Submit</button>
  </form>
</template>

<script>
export default {
  emits:['add-contact'],

  data() {
    return {
        username: '',
        age:''
    };
  },
  methods: {
    submitData() {
      this.$emit('add-contact',
        this.username,
        this.age
      );
    }
  },
};
</script>

<style>
.inputsection {
  background-color: gray;
  width: 25%;
  height: 200px;
  margin: auto;
  display: flex;
  flex-direction: column;
  flex-wrap: nowrap;
  justify-content: center;
  border-style: solid;
}
.inputsection input {
  width: 50%;
  margin: 0 auto;
}
.inputsection button {
  width: 20%;
  margin: 0 auto;
}
</style>
