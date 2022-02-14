<template>
  <div>
    <div class="box-card">
      <div class="com-card">
        <img :src="card.thumb" :alt="card.series" />
        <h3>{{ card.series }}</h3>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ComicsCard",
  props: ["card"],
};
</script>

<style lang="scss" scoped>
.com-card {
  flex-basis: 20%;
  padding: 20px;
}
.box-card {
  display: flex;
  flex-wrap: wrap;
}
</style>