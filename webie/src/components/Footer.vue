<template>
  <footer class="footer">
    <p>&copy; 2024 jozef.javorsky.dodo@gmail.com</p>
    <div class="links">
      <a
        href="https://github.com/jozef-javorsky-dodo"
        target="_blank"
        rel="noopener noreferrer"
      >
        GitHub
      </a>
      <a href="mailto:jozef.javorsky.dodo@gmail.com">Email</a>
    </div>
  </footer>
</template>

<script>
export default {
  name: "Footer",
};
</script>

<style scoped>
.footer {
  background-color: #f0f0f0;
  padding: 15px;
  text-align: center;
  font-size: 0.9em;
}

.links {
  display: flex;
  justify-content: center;
  gap: 10px;
  margin-top: 10px;
}

.links a {
  color: #333;
  text-decoration: none;
}
</style>
