<template>
  <div class="v-main-wrapper">
    <h1>{{ title }}</h1>
    <vCatalog></vCatalog>
    <vCart></vCart>
  </div>
</template>

<script>
import vCatalog from './v-catalog';
import vCart from './v-cart';

export default {
  name: "v-main-wrapper",
  components:{
    vCatalog,
    vCart
  },
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