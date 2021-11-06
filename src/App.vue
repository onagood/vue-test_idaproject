<template>
  <div class="container">
    <Header />
    <div class="content_wrapper">
      <div class="form_wrapper">
        <AddForm />
      </div>
      <div class="card_wrapper">
        <CardItem v-for="(carditem, index) in carditems" :key="index" />
      </div>
    </div>
  </div>
</template>

<script>
import AddForm from "@/components/AddForm.vue";
import CardItem from "@/components/CardItem.vue";
import Header from "@/components/Header.vue";

export default {
  name: "App",
  components: {
    AddForm,
    CardItem,
    Header,
  },
  data() {
    return {
      carditems: [{}, {}, {}, {}, {}, {}, {}, {}, {}],
    };
  },
};
</script>

<style lang="scss" scoped>
.container {
  width: 1376px;
  margin: 32px auto;
}
.content_wrapper {
  display: flex;
  margin-top: 16px;
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
