<template>
  <div id="app" class="container">
    <main>
      <TodoList />
    </main>
    <Footer />
  </div>
</template>

<script>
import Footer from "./components/Footer.vue";
import TodoList from "./components/TodoList.vue";

export default {
  components: {
    TodoList,
    Footer,
  },
};
</script>

<style>
#app {
  font-family: sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  display: flex;
  flex-direction: column;
  min-height: 100vh;
  width: 100%;
  /* Use max-width for responsiveness */
  max-width: 320px;
  margin: 0 auto;
  padding: 16px; /* Slightly smaller padding */
  background-color: #fff;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

main {
  flex-grow: 1;
}
</style>
