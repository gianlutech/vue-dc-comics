<template>
  <section id="jumbo" class="align-text">
    <div class="container card-container">
      <div>
        <ComicsCard
          v-for="(card, index) in comicsCards"
          :key="index"
          :card="card"
        />
      </div>
    </div>
  </section>
</template>

<script>
import ComicsCard from "./ComicsCard.vue";
export default {
  name: "Jumbotron",
  components: {
    ComicsCard,
  },
  props: ["comicsCards"],
};
</script>

<style lang="scss" >
#jumbo {
  color: white;
  background-color: #1c1c1c;
  min-height: 100px;
}
.align-text {
  display: flex;
  align-items: center;
}
</style>