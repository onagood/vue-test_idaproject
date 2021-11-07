<template>
  <div class="container">
    <Header />
    <div class="content_wrapper">
      <div class="form_wrapper">
        <AddForm />
      </div>
      <div class="card_wrapper">
        <CardItem v-for="carditem in carditems" :key="carditem.id" />
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
      carditems: [
        { id: 1 },
        { id: 2 },
        { id: 3 },
        { id: 4 },
        { id: 5 },
        { id: 6 },
        { id: 7 },
        { id: 8 },
        { id: 9 },
      ],
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
  grid-template-rows: repeat(3, 1fr);
}
@media screen and (max-width: 1400px) {
  .container {
    width: 1200px;
    padding: 0 20px;
  }
  .card_wrapper {
    width: 70%;
    grid-template-columns: repeat(2, 1fr);
    grid-template-rows: repeat(3, 1fr);
    justify-items: center;
  }
  .form_wrapper {
    width: 30%;
  }
}
@media screen and (max-width: 1200px) {
  .container {
    width: 1024px;
  }
}
@media screen and (max-width: 992px) {
  .container {
    width: 768px;
  }
  .card_wrapper {
    width: 50%;
    grid-template-columns: 1fr;
    justify-items: center;
  }
  .form_wrapper {
    width: 50%;
  }
}
@media screen and (max-width: 576px) {
  .container {
    width: 320px;
  }
  .content_wrapper {
    flex-direction: column;
  }
  .card_wrapper {
    margin-top: 15px;
    width: 100%;
  }
}
</style>
