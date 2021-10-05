<template>
  <button @click="color(index)">Done</button>
</template>

<script>
export default {
  methods: {
    color(index) {
      if (this.items[index].activeColor == "red") {
        this.items[index].activeColor = "green";
      }
    },
  }
};
</script>

<style>
</style>