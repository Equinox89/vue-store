<template>
  <div class="v-main-wrapper">
    <h1>{{ title }}</h1>
  </div>
</template>

<script>
export default {
  name: "v-main-wrapper",
  components:{},
  props: {},
  data(){
    return {
      title: 'I am the new component'
    }
  }

}
</script>

<style scoped>
  .v-main-wrapper {
    display: flex;
    justify-content: center;
    align-items: center;
    max-width: 900px;
    margin: 0 auto;
  }
</style>