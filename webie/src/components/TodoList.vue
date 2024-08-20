<template>
  <div class="todo-list">
    <h1>📝 To-Do-List 📒</h1>
    <ul v-if="items.length > 0">
      <li v-for="item in items" :key="item.id">
        {{ item.text }}
        <button @click="deleteItem(item.id)">Delete</button>
      </li>
    </ul>
    <p v-else>Your list is empty. Add some tasks!</p>
    <form @submit.prevent="addItem">
      <input type="text" v-model="newItemText" placeholder="Add new item" />
      <button type="submit">Add</button>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [],
      newItemText: "",
    };
  },
  methods: {
    addItem() {
      if (this.newItemText.trim() !== "") {
        this.items.push({
          id: Date.now(),
          text: this.newItemText,
        });
        this.newItemText = "";
      }
    },
    deleteItem(itemId) {
      this.items = this.items.filter((item) => item.id !== itemId);
    },
  },
};
</script>

<style scoped>
.todo-list {
  text-align: center;
}

.todo-list ul {
  list-style: none;
  padding: 0;
}

.todo-list li {
  padding: 10px;
  border-bottom: 1px solid #eee;
  display: flex;
  justify-content: space-between;
  align-items: center;
}
</style>
