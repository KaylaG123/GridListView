<template>
    <div class="product-list">
        <div class="view-bar">
            <a href="#" @click="changeView('list')">List</a> | <a href="#" @click="changeView('grid')">Grid</a>
            <hr />
        </div>
        <div class="products" :class="{'grid' : gridView}">
            <product
            v-for="product in products"
            :name="product.name"
            :price="product.price"
            :key="product.id"
            >
                {{ product.description }}
            </product>
        </div>
    </div>
</template>

<script>
    import Product from './product.vue'

    export default {
        components: { Product },

        methods: {
            changeView(type) {
                if(type == 'grid') {
                    this.gridView = true;
                } else {
                    this.gridView = false;
                }
            }
        },
        data(){
            return {

                gridView: false,

                products: [
                    {
                        id: 1,
                        name: 'Roomba',
                        description: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.',
                        price: 399.99
                    },
                    {
                        id: 2,
                        name: 'Mat',
                        description: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.',
                        price: 9.99
                    },
                    {
                        id: 3,
                        name: 'Lamp',
                        description: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.',
                        price: 19.99
                    },
                    {
                        id: 4,
                        name: 'Vacuum',
                        description: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.',
                        price: 599.99
                    },
                    {
                        id: 5,
                        name: 'Hair Dryer',
                        description: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.',
                        price: 99.99
                    },
                    {
                        id: 6,
                        name: 'Fan',
                        description: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.',
                        price: 39.99
                    }
                ]
            }
        }
    }

</script>

<style scoped>
.product-list {
    padding: 2rem;
    border: 1px solid #ccc;
    border-radius: 4px;
}
.products {
    display: flex;
    flex-direction: column;
}
.grid {
    flex-direction: row;
    flex-wrap: wrap;
}
.product {
    flex-basis: 25%;
}

.view-bar {
    text-align: right;
}

</style>
