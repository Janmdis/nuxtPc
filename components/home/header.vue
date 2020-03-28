<template>
	<header class="v-header clearfix">
		<nuxt-link to="/">首页</nuxt-link>
		<nuxt-link to="/new">新闻</nuxt-link>
		<nuxt-link to="/material">器材</nuxt-link>
		<nuxt-link to="/about">关于我们</nuxt-link>
	</header>
</template>

<script>

	export default{
		name: 'VHeader',
		data (){
			return {

			}
		},
		computed: {
		},
		mounted (){

		},
		methods: {
		},
		destroyed (){
		}
	}
</script>

<style scoped>
.v-header{
	height: 80px;
	border-bottom:1px solid #ddd ;
	line-height: 80px;
	color: #fff;
}
</style>