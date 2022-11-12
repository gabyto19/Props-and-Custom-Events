<template>
    <section class="inputsection">
        <h2>username: {{username}}</h2>
        <br>
        <h3>Age: {{age}}</h3>
    </section>
  </template>
  
  <script>
  export default {
     props: ['username', 'age'],
    // props: {
     
    // },
    data() {
      return {

    };
    },
    methods: {
    
    },
  };
  </script>