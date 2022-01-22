<template>
  <div class="v-main-wrapper">
    <h1>{{ title }}</h1>
    <vCatalog></vCatalog>
    <vCart
        v-if="CART.length"
        :cart_data="CART"
    ></vCart>
  </div>
</template>

<script>
import vCatalog from './v-catalog';
import vCart from './v-cart';
import {mapGetters} from 'vuex'

export default {
  name: "v-main-wrapper",
  components:{
    vCatalog,
    vCart
  },
  computed: {
    ...mapGetters([
      'CART'
    ])
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
    flex-direction: column;
    justify-content: center;

    max-width: 900px;
    margin: 0 auto;
  }
</style>
