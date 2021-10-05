<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <ul>
      <li v-for="(item, index) in items" :key="item.task">
        <span v-bind:style="styleObject">
          {{ item.task }}
        </span>
        <button @click="color(index)">Done</button> <button>Supprimer</button>
      </li>
    </ul>
    <input v-model="tasks" placeholder="Ajoutez-moi" />
    <button v-on:click="add">iogdkdj</button>
  </div>
</template>

<script>
export default {
  name: "Todolist",
  styleObject: {
    color: "red",
    fontSize: "13px",
  },
  data() {
    return {
      items: [{ task: "fo", activeColor: "red" }, { task: "bar" }],
      tasks: null,
    };
  },
  methods: {
    color(index) {
      if (this.items[index].activeColor == "red") {
        this.items[index].activeColor = "green";
      }
    },
    suppr(index) {
      this.items.splice(index, 1);
    },

    add() {
      this.items.push({ task: this.tasks });
    },
  },
};
</script>


<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
