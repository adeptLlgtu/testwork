<template>
    <div class="nav">
        <router-link to="/">
            <div class="ring"></div>
        </router-link>
        <router-link id="quizes" class="nav-item" to="/">
            <img :src="doc" alt="">
            <p>Опросы</p>
        </router-link>
        <router-link id="users" class="nav-item" to="/">
            <img :src="users" alt="">
            <p>Пользователи</p>
        </router-link>
        <router-link id="black-list" class="nav-item" to="/">
            <img :src="flag" alt="">
            <p>Черные списки</p>
        </router-link>
        <router-link id="call-centre" class="nav-item" to="/">
            <img :src="phone" alt="">
            <p>Колл-центр</p>
        </router-link>
        <router-link id="questions" class="nav-item" to="/">
            <div>
                <p>?</p>
            </div>
        </router-link>
    </div>
</template>

<script>
    import doc from '../assets/img/doc.svg'
    import users from '../assets/img/users.svg'
    import flag from '../assets/img/flag.svg'
    import phone from '../assets/img/phone.svg'

    export default {
        name: "Nav",
        data(){
            return{
                doc, users, flag, phone
            }
        }
    }
</script>

<style scoped>

</style>