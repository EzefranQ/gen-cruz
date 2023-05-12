<template>

    <section class="home">

        <div class="home-img">
            <img src="../assets/img/img_fishing_ship_1920-1500x585.webp" alt="">
        </div>

        <article class="home-content">
            <div class="home-text">
                <h1>Generación
                    <span class="h-block">La cruz</span>
                </h1>
                <p style="margin-top: 15px;">Productos <span>Hidrocarburos</span></p>
                <div class="home-btns">
                    <Buttons btn="Productos" href="#"/>
                    <Buttons btn="WhatsApp" href="#"/>
                </div>
            </div>
        </article>

    </section>

</template>

<script>

  import Buttons from '@/components/Buttons.vue'
  export default {
    name: 'App',
    components: {
      Buttons
    }
  }

</script>

<style scoped>
.home{
    height: 80vh;
    width: 100%;
}
.home-img{
    height: 80vh;
    width: 100%;
    position: absolute;
    z-index: -1;
}
img{
    object-fit: cover;
}

.home-content{
    padding: 13rem 0 0 5rem;
    display: flex;
    gap: 20px;
}
.home-text{
    padding: 1rem;
    min-width: 40%;
    background: rgb(0, 0, 0, .6);
    border-radius: 1.5rem;
    color: #fff;
}

.home-text h1{
    font-size: 60px;
    line-height: 55px;
}
.home-text .h-block{
    display: block;
    color: #1ea0c3;
}
.home-text p span{
    color: #1ea0c3;
}
.home-text p{
    font-size: 20px;
}
.home-btns{
    display: flex;
    gap: 20px;
    margin: 0 auto;
    margin-top: 15px;
}


@media screen and (max-width: 875px) {
    .home-content{
        padding: 10rem 0 0 0;
        margin: 0 5px;
        justify-content: center;
    }
    .home-text{
        min-width: 60%;
        text-align: center;
    }
    .home-btns{
        justify-content: center;
    }
    .home-text h1{
        font-size: 50px;
        line-height: 40px;
    }
}
@media screen and (max-width: 350px) {
    .home-btns{
        justify-content: center;
    }
    .home-text h1{
        font-size: 35px;
        line-height: 35px;
    }
    .home-text p{
        font-size: 16px;
    }
    .home-btns{
        gap: 10px;
    }
}


</style>