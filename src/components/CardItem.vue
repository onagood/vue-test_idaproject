<template>
  <div class="card">
    <img src="@/assets/img/product.jpg" alt="product" />
    <div class="card_content">
      <h2 class="card_title">{{ card_title }}</h2>
      <p class="card_text">{{ card_text }}</p>
      <p class="card_price">{{ card_price }}</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      card_title: "Наименование товара",
      card_text: `Довольно-таки интересное описание товара в несколько строк. Довольно-таки интересное описание товара в несколько строк`,
      card_price: "10000 руб.",
    };
  },
};
</script>

<style lang="scss" scoped>
.card {
  display: flex;
  flex-direction: column;
  color: #3f3f3f;
  width: 332px;
  height: 423px;
  background: #fffefb;
  box-shadow: 0px 20px 30px rgba(0, 0, 0, 0.04),
    0px 6px 10px rgba(0, 0, 0, 0.02);
  border-radius: 4px;
  transition: transform 0.2s linear;
  &:hover {
    transform: translateY(-10px);
  }
  img {
    margin-bottom: 16px;
  }
  &_content {
    padding: 0 16px 24px 16px;
  }
  &_title {
    margin-bottom: 16px;
  }
  &_text {
    margin-bottom: 32px;
  }
  &_price {
    font-size: 24px;
    font-weight: 600;
  }
}
</style>
