<template>
  <div class="header_wrapper">
    <h1>Добавление товара</h1>
    <div class="select">
      <select>
        <option>По умолчанию</option>
        <option>По умолчанию 2</option>
      </select>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.header_wrapper {
  display: flex;
  justify-content: space-between;
  & h1 {
    font-size: 28px;
  }
}
.select {
  position: relative;
  height: 36px;
  background: #fffefb;
  box-shadow: 0px 2px 5px rgba(0, 0, 0, 0.1);
  border-radius: 4px;
  &:after {
    content: url("../assets/img/arrow.png");
    position: absolute;
    width: 4px;
    height: 4px;
    top: 16%;
    right: 19px;
    z-index: 1;
  }
  & select {
    border: none;
    appearance: none;
    color: #b4b4b4;
    font-size: 12px;
    outline: none;
    padding: 10px 15px;
    cursor: pointer;
  }
}
@media screen and (max-width: 576px) {
  .header_wrapper h1 {
    font-size: 20px;
  }
}
</style>
