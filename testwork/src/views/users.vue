<template>
  <div class="users">
    <div class="content">
      <div class="users-head__block">
        <form class="users-head__block-form" action="">
          <input placeholder="Поиск по системе" type="text">
          <button type="submit">
            <img :src="search" alt="">
          </button>
        </form>
        <div class="users-head__block-person">
          <img :src="user" alt="">
          <div class="users-head__block-person-info">
            <p class="users-head__block-person-info__name">Alexander C.</p>
            <p class="users-head__block-person-info__status">Администратор</p>
          </div>
        </div>
      </div>
      <breadcrumbs></breadcrumbs>
      <userFrom></userFrom>
    </div>
  </div>
</template>
<script>
  import search from '../assets/img/search.svg'
  import user from '../assets/img/administrator.png'
  import breadcrumbs from "../components/breadcrumbs";
  import userFrom from "../components/userFrom";

  export default {
    name: 'Home',
    components:{breadcrumbs, userFrom},
    data(){
      return{
        search, user
      }
    },

  }
</script>
