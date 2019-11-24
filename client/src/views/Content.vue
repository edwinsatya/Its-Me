<template>
  <div id="content">
    <section id="home">
      <div class="container">
        <ul id="scene">
          <li class="layer"></li>
          <li class="layer"></li>
          <li class="layer"></li>
          <li class="layer"></li>
          <li class="layer"></li>
        </ul>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: "maincontent"
};
</script>

<style scoped>
.container {
  width: 100%;
  height: 100vh;
  overflow: hidden;
  background: url("../assets/img/home.jpg");
  background-size: cover;
}
</style>
