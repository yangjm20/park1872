<template>
	<view>
		<web-view :src="wxurl"></web-view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				wxurl: ""
			};
		},
		methods: {

		},

		onLoad: function(option) { //option为object类型，会序列化上个页面传递的参数
			console.log(option.wxurl); //打印出上个页面传递的参数。
			
			
			this.wxurl = option.wxurl
		}
	}
</script>

<style lang="scss">

</style>