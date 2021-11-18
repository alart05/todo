<template>
  <div class='card'>
    <div class='header'> 
      {{dayOfWeek}}
    </div>  
    <TodoItem/>
    <TodoItem/>
    <TodoItem/>
    <TodoItem/>
    <TodoItem/>
  </div>
</template>

<script>
import TodoItem from '@/components/TodoItem.vue'
export default {
  name: 'Card',
  props:{
    dayOfWeek: { type: String, default: '' }
  },
  components: {
    TodoItem
  },
}
</script>

<style lang="scss" scoped>
  .card{
    background: #FFF0EE;
    border: 4px solid #33322E;
    box-sizing: border-box;
    box-shadow: 12px 12px 0px #33322E;
    border-radius: 24px;
    width: 250px;
    height: 300px;
  }
  .header{
    font-weight: bold;
    font-size: 30px;
    color:#33322E;
    padding: 10px 24px;
    border-bottom: 4px solid #33322E;
  }
</style>