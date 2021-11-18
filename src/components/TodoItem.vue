<template>
  <div class='item'>
    <div>
      <input class='input' placeholder="твои дела на сегодня">
      <div class='line'></div>
    </div>
    <img class='sqare__img' @click="state = true" :class="state ? 'focus' : ''" src="@/assets/good.svg">
    <img class='sqare__img' @click="state = false" :class="state ? '' : 'focus'" src="@/assets/bad.svg">
  </div>
</template>

<script>
export default {
  name: 'TodoItem',
  data() {
    return {
      state: false,
    }
  }
}
</script>

<style lang="scss" scoped>
  .item{
    display: flex;
    align-items: center;
    padding: 10px 15px;
  }
  .input{
    border: none;
    margin-right: 15px;
    background: #FFF0EE;
  }
  input:focus {
    outline: none;
  }
  .line{
    background-color: #33322E;
    height: 1px;
  }
  .sqare__img{
    width: 22px;
    height: 22px;
    min-width: 22px;
    min-height: 22px;
    opacity: 0.3;
    cursor: pointer;
  }
  .focus {
    opacity: 1;
  }
</style>