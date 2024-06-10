<template>
  <nav class="navbar">
    <a href="#">Home</a>
    <a href="#">Movies</a>
    <a href="#">About</a>
  </nav>
</template>

<script>
export default {
  name: "NavbarComponent", // 이름 명명 규칙에 의해 너무 간단하게(Navbar) 지으면 안됨
};
</script>

<style>
.navbar {
  background: #000;
  padding: 20px;
  text-align: center;
}

.navbar a {
  color: #fff;
  text-decoration: none;
  padding: 1em;
}
</style>
