<template>
  <div class='page'>
    <Card v-for='day in week' :key='day' :dayOfWeek="day"/>
  </div>
</template>

<script>
import Card from '@/components/Card.vue'
export default {
  name: 'App',
  components:{
    Card
  },
  data() {
    return {
      week: [
        'Monday',
        'Tuesday',
        'Wednesday',
        'Thursday',
        'Friday',
        'Weekend'
      ]
    }
  },
}
</script>

<style lang="scss" scoped>
  .page{
    background-color: #F6A89E;
    height: 100vh;
    padding: 40px;
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    grid-gap: 40px;
  }
</style>
