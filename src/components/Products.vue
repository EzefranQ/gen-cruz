<template>
    <section class="products-container">
        <article class="products-content" v-for="item in divs" :key="item.id">
            <div class="product-img">
                <img :src="item.image" alt="">
            </div>
            <div class="product-title">
                <p>{{ item.title }}</p>
            </div>
        </article>

    </section>
</template>

<script>

export default {
    setup() {
        let divs = [
            { title: 'Productos Hidrobiologicos CEGERCRUZ PERU', image: require('../assets/img/produccion_productos_hidrobiologicos-10.webp')},
            { title: 'Productos Hidrobiologicos CEGERCRUZ PERU', image: require('../assets/img/produccion_productos_hidrobiologicos-11.webp')},
            { title: 'Productos Hidrobiologicos CEGERCRUZ PERU', image: require('../assets/img/produccion_productos_hidrobiologicos-12.webp')},
            { title: 'Productos Hidrobiologicos CEGERCRUZ PERU', image: require('../assets/img/produccion_productos_hidrobiologicos-13.webp')},
            // { title: 'Productos Hidrobiologicos CEGERCRUZ PERU', image: require('../assets/img/produccion_productos_hidrobiologicos-14.webp')},
            { title: 'Productos Hidrobiologicos CEGERCRUZ PERU', image: require('../assets/img/produccion_productos_hidrobiologicos-16.webp')},
            { title: 'Productos Hidrobiologicos CEGERCRUZ PERU', image: require('../assets/img/produccion_productos_hidrobiologicos-17.webp')},
            { title: 'Productos Hidrobiologicos CEGERCRUZ PERU', image: require('../assets/img/produccion_productos_hidrobiologicos-15.webp')},
            { title: 'Productos Hidrobiologicos CEGERCRUZ PERU', image: require('../assets/img/produccion_productos_hidrobiologicos-19.webp')},
            { title: 'Productos Hidrobiologicos CEGERCRUZ PERU', image: require('../assets/img/produccion_productos_hidrobiologicos-7-300x225.webp')},
            { title: 'Productos Hidrobiologicos CEGERCRUZ PERU', image: require('../assets/img/produccion_productos_hidrobiologicos-6-300x192.webp')},
            { title: 'Productos Hidrobiologicos CEGERCRUZ PERU', image: require('../assets/img/produccion_productos_hidrobiologicos-5-300x198.webp')},
            { title: 'Productos Hidrobiologicos CEGERCRUZ PERU', image: require('../assets/img/produccion_productos_hidrobiologicos-29.webp')},
        
        ]
        return {
            divs
        }
    },
}

</script>

<style scoped>
.products-container {
    display: grid;
    grid-template-columns: repeat(auto-fill, 330px);
    width: 100%;
    justify-content: center;
    align-items: center;
    padding: 4rem 0;
    row-gap: 40px;
}

.product-title {
    width: 90%;
}
.product-title p{
    width: 50%;
    margin: 0 auto;
    text-align: center;
}

.products-content {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    gap: 5px;
}

.product-img {
    width: 300px;
    height: 120px;
    margin: 0 auto;
}
.product-img img{
    object-fit: cover;
}


@media screen and (max-width: 350px) {
    .product-img {
        width: 250px;
    }
    .products-container {
        grid-template-columns: repeat(auto-fill, 250px);
    }

}

</style>