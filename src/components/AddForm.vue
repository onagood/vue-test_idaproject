<template>
  <form class="form" action="#">
    <div class="form_name">
      <label class="form_after" for="product-name">{{ product_name }}</label>
      <input
        required
        id="product-name"
        type="text"
        placeholder="Введите наименование товара"
      />
    </div>

    <div class="form_text">
      <label for="product-text">{{ product_text }}</label>
      <textarea id="product-text" placeholder="Введите описание товара" />
    </div>

    <div class="form_link">
      <label class="form_after" for="product-link">{{ product_link }}</label>
      <input
        required
        id="product-link"
        type="text"
        placeholder="Введите ссылку"
      />
    </div>

    <div class="form_price">
      <label class="form_after" for="product-price">{{ product_price }}</label>
      <input
        required
        id="product-price"
        type="text"
        placeholder="Введите цену"
      />
    </div>

    <button class="form_button" type="submit">{{ button }}</button>
  </form>
</template>

<script>
export default {
  data() {
    return {
      product_name: "Наименование товара",
      product_text: "Описание товара",
      product_link: "Ссылка на изображение товара",
      product_price: "Цена товара",
      button: "Добавить товар",
    };
  },
};
</script>

<style lang="scss" scoped>
.form {
  display: flex;
  padding: 24px;
  flex-direction: column;
  width: 332px;
  height: 440px;
  background: #fffefb;
  box-shadow: 0px 20px 30px rgba(0, 0, 0, 0.04),
    0px 6px 10px rgba(0, 0, 0, 0.02);
  border-radius: 4px;
  font-size: 10px;
  &_button {
    width: 100%;
    height: 36px;
    background-color: #eeeeee;
    border-radius: 10px;
    border: none;
    color: #b4b4b4;
    cursor: pointer;
    transition: all 0.05s ease-in-out;
    &:active {
      background-color: rgb(204, 204, 204);
      color: white;
      transform: scale(1.02);
    }
  }
  &_after::after {
    content: "";
    position: absolute;
    width: 4px;
    height: 4px;
    background: #ff8484;
    border-radius: 4px;
  }
  & input,
  & textarea {
    margin-top: 4px;
    padding: 10px 16px;
    font-size: 14px;
    background: #fffefb;
    box-shadow: 0px 2px 5px rgba(0, 0, 0, 0.1);
    border-radius: 4px;
    border: none;
    color: #b4b4b4;
  }
  & input,
  & textarea:focus {
    color: black;
  }
  &_name,
  &_text,
  &_link,
  &_price {
    display: flex;
    flex-direction: column;
    margin-bottom: 16px;
  }
  &_text {
    flex: 1;
    textarea {
      resize: none;
      height: 100%;
    }
  }
}
@media screen and (max-width: 1200px) {
  .form {
    width: 300px;
    font-size: 12px;
  }
}
</style>
