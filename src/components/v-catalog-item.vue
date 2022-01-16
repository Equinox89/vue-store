<template>
  <div class="v-catalog-item">
    <img
      class="v-catalog-item__image"
      :src="require(`../assets/images/${product_data.image}`)"
      alt="image"
    />
    <p>Price: {{ product_data.price }}</p>
    <p>Name: {{ product_data.name }}</p>
    <button btn @click="sendDataToParent">Add to cart</button>
  </div>
</template>

<script>
export default {
  name: "v-catalog-item",
  props: {
    product_data: {
      type: Object,
      default() {
        return {};
      },
    },
  },
  methods: {
    sendDataToParent() {
      this.$emit("sendDataToParent", this.product_data.name);
    },
  },
};
</script>

<style lang="scss">
.v-catalog-item {
  padding: 16px;
  margin-bottom: 16px;
  box-shadow: 0 0 8px #e5e5e5;
  border-radius: 4px;

  &__image {
    width: 100px;
  }
}
</style>
