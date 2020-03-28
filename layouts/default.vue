<template>
  <div>
    <v-header></v-header>
    <main class="content-container" ref="container" :class="headFixed == true ? 'marginTop' : ''">
      <nuxt/>
    </main>
    <v-footer></v-footer>
  </div>
</template>

<style>
  .marginTop{
    margin-top: 170px;
  }
  .content-container{
    min-height: 776px;
  }
</style>

<script>
  import VHeader from '~/components/home/header'
  import VFooter from '~/components/home/footer'

  export default {
    components: {
      VHeader,
      VFooter
    },
    data (){
      return {
        headFixed:false,
        maxClientWidth: 980
      }
    },
    mounted (){
      //监听滚动条，固定头部
      window.addEventListener('scroll',this.handleScroll);
 
    },
    methods: {
      handleScroll (){
        var scrollTop = window.pageYOffset || document.documentElement.scrollTop || document.body.scrollTop;
        var offsetTop = document.querySelector('.h-nav-list').offsetTop;
        if (scrollTop > offsetTop) {
          this.headFixed = true;
        } else {
          this.headFixed = false;
        }
      }
    },
    destroyed (){
      window.removeEventListener('scroll',this.handleScroll)
    }
  }
</script>
