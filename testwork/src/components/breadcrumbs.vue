<template>
    <div class="breadcrumbs">
        <router-link to="/" class="breadcrumbs-past-link">
            <img :src="home" alt="">
        </router-link>
        <p class="breadcrumbs-arrow">&#10141;</p>
        <router-link to="/" class="breadcrumbs-past-link">Опросы</router-link>
        <p class="breadcrumbs-arrow">&#10141;</p>
        <router-link to="/" class="breadcrumbs-active-link">Добавить опрос</router-link>
    </div>
</template>

<script>
    import home from '../assets/img/home.svg'
    export default {
        name: "breadcrumbs",
        data(){
            return{
                home
            }
        }
    }
</script>

