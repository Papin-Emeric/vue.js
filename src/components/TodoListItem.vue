<template>
    <span v-bind:style="styleObject">
        {{ item.task }}
    </span>
</template>

<script>
export default {
    data() {
    return {
      items: [{ task: "fo", activeColor: "red" }, { task: "bar" }],
      tasks: null,
    };
  },
}
</script>

<style>

</style>