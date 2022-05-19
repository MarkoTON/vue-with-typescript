<template>
  <div class="app">
    <p>{{ name }} - {{ age }}</p>
    <button @click="changeName('Zelda')">change name</button>
    <button @click="changeAge(30)">change age</button>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'App',
  components: {},
  data() {
    return {
      name: 'Link',
      age: 25 as number | string
    }
  },
  methods: {
    changeName(name: string) {
      this.name = name
      console.log(name)
      console.log(this.name)
      // ovaj return je nebitan
      return name
    },
    changeAge(age: number | string) {
      this.age = age
      console.log(age)
      console.log(this.age)
      // ovaj return je nebitan
      return age
    }
  }
});
</script>

<style>

</style>
