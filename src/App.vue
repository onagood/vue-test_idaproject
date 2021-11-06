<template>
  <div class="container">
    <div class="form_wrapper">
      <add-form />
    </div>
    <div class="card_wrapper">
      <card-item v-for="carditem in carditems" :key="carditem" />
    </div>
  </div>
</template>

<script>
import AddForm from "@/components/AddForm.vue";
import CardItem from "@/components/CardItem.vue";

export default {
  name: "App",
  components: {
    AddForm,
    CardItem,
  },
  data() {
    return {
      carditems: [{}, {}, {}, {}, {}, {}],
    };
  },
};
</script>

<style lang="scss">
.container {
  width: 1376px;
  margin: 32px auto;
  display: flex;
}
.form_wrapper {
  width: 25%;
}
.card_wrapper {
  width: 75%;
  display: grid;
  gap: 16px;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: repeat(2, 1fr);
}
</style>
