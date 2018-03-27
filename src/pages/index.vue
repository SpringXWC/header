<template>
  <div>
   <header-Top title="个人中心" :bg="true">
            <router-link to="" slot="left">
              <img class="icon-img" src="../assets/image/return_36x36px.png"/>
            </router-link>
            <a href="javascript:;" slot="right">分享</a>
    </header-Top>
   
  


  </div>
</template>
<script>
  import headerTop from '../components/header.vue';
  export default{
    components:{
      headerTop,
 
    },
    data(){
      return{
       
      }
    }
  }
</script>
