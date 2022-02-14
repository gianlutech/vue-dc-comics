<template>
  <header class="container flex-list">
    <figure>
      <img src="../assets/img/dc-logo.png" alt="DC-logo" />
    </figure>
    <nav>
      <ul>
        <li v-for="link in links" :key="link.text">
          <a :href="link.url">{{ link.text }}</a>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  name: "Header",
  props: ["links"],
};
</script>


<style lang="scss" scoped>
header {
  min-height: 70px;
  ul {
    display: flex;
    li {
      list-style-type: none;
      padding: 10px;
      a {
        text-decoration: none;
        color: black;
      }
    }
  }
}
.flex-list {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px;
}
</style>
