<template>
    <a :href="href">
        <button>{{ btn }}</button>
    </a>
</template>

<script>

    export default{
        props:{
            btn: String,
            href: String
        }
    }

</script>

<style scoped>

    /* button{
        border: 2px solid #feba12;
        background: #000;
        color: #feba12;
        width: 120px;
        height: 40px;
        border-radius: 1.5rem;
        font-size: 17px;
        cursor: pointer;
    } */
    button{
        border: 2px solid #000;
        background: #000;
        color: #1ea0c3;
        width: 120px;
        height: 40px;
        border-radius: .5rem;
        font-size: 17px;
        cursor: pointer;
        transition: .5s border;
    }
    button:hover{
        border: 2px solid #1ea0c3;
    }
    /* button{
        border: none;
        background: #feba12;
        color: #000;
        width: 120px;
        height: 40px;
        border-radius: 1.5rem;
        font-size: 17px;
        cursor: pointer;
    } */

</style>