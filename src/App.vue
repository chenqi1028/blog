<template>
<div class="container">
	<img alt="陈琦" src="./assets/imgs/logo.png" class="app-top-img">
	<div class="nav">
		<router-link to="/">首页</router-link> 
		<router-link to="/note">笔记</router-link>
		<router-link to="/tool">工具</router-link>
		<router-link to="/about">关于</router-link>
	</div>
	<router-view class="content"/>
</div>
</template>

<style lang="scss">
#app{
	overflow-x: hidden;
	overflow-y: auto;
}
</style>
<style lang="scss" scoped>
.container {
	position: fixed;
	top: 0;
	bottom: 0;
	left: 0;
	right: 0;
	overflow: hidden;
	overflow-y: auto;
	.content{
		padding: 0 18px;
	}
}
.app-top-img{
	position: relative;
	left:50%;
	transform: translateX(-50%);
	width: 2.4rem;
	margin: 0.5rem 0;
}
.nav{
	display: flex;
	justify-content: space-between;
	padding: 0 4rem .4rem;
	font-size: 0.7rem;
	border-bottom: 1px solid #eee;
	margin-bottom:1.5rem;
}
</style>