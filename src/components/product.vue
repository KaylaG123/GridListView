<template>
    <div class="product">
        <h3>{{ name }}</h3>
        <h5>{{ price }}</h5>
        <slot></slot>
    </div>
</template>

<script>
export default {
    props: ['name', 'price']
}
</script>

<style>
    .product {
        padding: 1rem;
        border: 1px solid #CCC;
        box-shadow: 3px 3px 8px rgba(0, 0, 0, 0.2);
    }
</style>
