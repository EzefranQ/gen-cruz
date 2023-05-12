<template>
    <header class="header">
        <nav class="desktop">
            <div class="logo">
                <img src="../assets/logo_340.webp" alt="">
            </div>
            <ul class="menu-desktop">
                <li class="link" v-for="link in links">
                    <a :href="link.link">
                        {{ link.name }}
                    </a>
                </li>
            </ul>
        </nav>
        <nav class="mobile">
            <div class="open-close">
                <div class="logo">
                    <img src="../assets/logo_340.webp" alt="">
                </div>
                <div 
                class="hamburger"
                @click="ShowMenu()"
                >
                    <div></div>
                    <div></div>
                    <div></div>
                </div>
            </div>
            <ul class="menu-mobile" 
            :class="this.ShowMobile ? 'open-menu' : 'closed-menu'">
                <li class="link" v-for="link in links">
                    <a :href="link.link">
                        {{ link.name }}   
                    </a>
                </li>
            </ul>
        </nav>
    </header>
</template>

<script >

    export default{
        data() {
            return {
                ShowMobile: false,
            }
        },
        methods:{
            ShowMenu(){
                this.ShowMobile = !this.ShowMobile;
            }
        },
        setup(){
            let links = [
                {name : 'Inicio', link : '#'},
                {name : 'Productos', link : '#'},
                {name : 'Nosotros', link : '#about-us'},
                {name : 'Servicios', link : '#'},
                {name : 'Contacto', link : '#'},
            ]
            return {links}
        }
    }


</script>

<style scoped>

/* Header */
.header{
    padding: 1rem;
    height: 80px;
    position: relative;
    background: #fff;
}

.logo{
    width: 180px;
}
/* Desktop */
.desktop{
    display: flex;
    align-items: center;
    justify-content: space-around;
    height: 100%;
    width: 100%;
}
.desktop ul{
    display: flex;
    gap: 25px;
}

.header a{
    font-size: 16px;
    font-weight: 300;
    color: #000;
    transition: .5s color;
}
.header a:hover{
    color: #1ea0c3;
}

/* Mobile */

.mobile .logo img{
    vertical-align: middle;
}
.mobile{
    display: none;
}
.hamburger > div{
    width: 1.3rem;
    height: 2px;
    background: #000;
}
.hamburger{
    height: 100%;
    display: flex;
    flex-direction: column;
    gap: 4px;
    cursor: pointer;
}
.open-close{
    width: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
}
.menu-mobile{
    z-index: 1;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    gap: 15px;
    background: #fff;
    width: 100%;
}
.open-menu{
    transition: .5s all;
    transform: translateY(80px);
    position: absolute;
    z-index: 1;
}
.closed-menu{
    transition: .5s all;
    transform: translateY(-400px);
    z-index: 1;
    position: absolute;
}
@media screen and (max-width: 800px){
    .desktop{
        display: none;
    }
    .mobile{
        width: 100%;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        align-items: center;
    }
    .header{
        padding: 0 1rem;
        position: relative;
        background: #fff;
    }
}

</style>