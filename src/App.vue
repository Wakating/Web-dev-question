<template>
  <div id="app">
    <input
     type="number"     v-model="limit"    @input="updateValue" />
    <Numbers/>
  </div>
</template>

<script>
import Numbers from '@/components/Numbers';

export default {
  name: 'App',
  components: {Numbers},
  data()
  {
    return {
      limit: 100
    }
  },
  methods: {
    updateValue(event){

      const value = event.target.value
      if (value>100) {
          this.limit = 100
      }
       if (value<0) {
          this.limit = 0
      }



    }
  }


}
</script>

<style scoped>
</style>
