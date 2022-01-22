<template>
    <div class="v-cart-item">
        <img

            :src="require(`../assets/images/${cart_item_data.image}`)"
            alt="image"
        />
        <div class="v-cart-item__info">
            <p>{{ cart_item_data.name }}</p>
            <p>{{ cart_item_data.price }}</p>
            <p>{{ cart_item_data.article }}</p>
        </div>
        <div class="v-cart-item__quantity">
            <p>Quantity</p>
            {{ cart_item_data.quantity }}
        </div>
        <button @click="deleteFromCart">Delete</button>
    </div>
</template>

<script>
    export default {
        name: "v-cart-item",
        data() {
            return {}
        },
        methods: {
            deleteFromCart() {
                this.$emit('deleteFromCart')
            }
        },
        props: {
            cart_item_data: {
                type: Object,
                default() {
                    return {}
                }
            }
        },
        mounted() {
            // eslint-disable-next-line vue/no-mutating-props
            this.cart_item_data.quantity = 1
        }
    }
</script>

<style lang="scss">
    .v-cart-item {
        display: flex;
        justify-content: space-between;
        align-items: center;
        flex-wrap: nowrap;
        padding: 16px;
        margin-bottom: 16px;
        box-shadow: 0 0 8px #e5e5e5;
        border-radius: 4px;

        img {
            max-width: 80px;
        }
    }
</style>
