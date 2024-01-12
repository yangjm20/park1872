<template>
	<view class="page">

		<view class="title">生活联系录，查询联系方式</view>
		<view class="header">

			<image src="/images/search.png"></image>
			<input class="txt" type="txt" placeholder="搜索" />
			<picker @change="bindPickerChange" :value="index" :range="array">
				<view class="picker">
					<image class="img1" src="/images/xian.png" />
					<view>{{array[index]}}</view>
					<image class="img2" src="/images/down.png"></image>
				</view>
			</picker>

		</view>

		<view class="content">
			<view class="box" v-for="item in contacts">
				<view class="con">
					<view class="type">{{item.title}}</view>
					<view class="cons">{{item.type}}</view>
					<view class="name">{{item.name}}</view>
				</view>

				<view class="phone">
					<button :class="{myClaas:state}" :style="{background:color}" @tap="call">立即联系</button>
				</view>

			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: "",
				message: {
					name: "",
					phone: "",
					content: ""
				},
				name: "",
				color: "#234",
				array: ['公园1872-南区', '公园1872-北区'],
				objectArray: [{
						id: 0,
						name: '公园1872-南区'
					},
					{
						id: 1,
						name: '公园1872-北区'
					}

				],
				index: 0,
				state: false,
				contacts: [{
						"title": "帮忙代养宠物几天",
						"type": "到家代养",
						"name": "jianm"
					},
					{
						"title": "帮忙打扫卫生",
						"type": "上门",
						"name": "jianm"
					},
					{
						"title": "辅导作业",
						"type": "周末有空",
						"name": "jianm"
					}
				]
			};

		},
		methods: {
			bindPickerChange: function(e) {
				console.log('picker发送选择改变，携带值为', e)
				this.index = e.detail.value
			},

			call() {
				uni.showToast({
					title: '18018590001',
					icon: "none",
				})

				let color = String(Math.random()).substring(3, 6)
				console.log(color)
				this.color = "#" + color
				this.state = !this.state
			},

			subMit() {
				console.log(this.message)
			},

			tt(e) {
				console.log(e)
			},
			myenv(e) {
				console.log(e)
				this.name = e
			},
			onC() {
				console.log("123")
			}
		},
		computed: {
			toCaseUp() {
				return this.title.toLocaleUpperCase()
			}
		}

	}
</script>

<style lang="scss">
	/* pages/contact/contact.wxss */

	.test {
		.row {
			border: solid 1rpx black;
			padding: 10rpx 10rpx;
			box-sizing: border-box;
			margin: 10rpx 10rpx;
		}
	}

	.page {
		height: 100vh;
	}

	.title {
		font-size: 22rpx;
		text-align: center;
		padding-bottom: 20rpx;
	}

	.header {

		margin-left: 10rpx;
		display: flex;
		justify-content: left;
		align-items: center;
		width: 720rpx;
		height: 100rpx;
		background-color: rgb(203, 216, 245);
		border-radius: 20rpx;
	}

	.header image {
		margin-left: 20rpx;
		flex: 1;
		height: 80rpx;
	}


	.header input {
		flex: 4;
		height: 80rpx;

		margin-left: 10rpx;
		font-size: 24rpx;

	}

	.picker {
		flex: 5;
		display: flex;
		justify-content: space-between;
		align-items: center;

		padding-left: 100rpx;
		font-size: 24rpx;
		color: rgb(139, 131, 131);

	}

	.picker .img1 {
		height: 70rpx;
		width: 40rpx;
		padding: 0rpx 10rpx;
	}

	.picker .img2 {
		height: 25rpx;
		width: 25rpx;

		padding: 0rpx 20rpx;
	}

	.content {
		margin-top: 20rpx;
		padding-top: 20rpx;

	}

	.content .box {

		display: flex;
		justify-content: space-between;
		margin: 30rpx 30rpx;
		background-color: rgb(203, 216, 245);
		border-radius: 10rpx;

		height: 150rpx;
	}

	.con {
		padding-left: 20rpx;
		display: flex;
		flex-direction: column;
		justify-content: space-between;
		align-items: left;
		height: 100%;
	}

	.con .type {
		padding-top: 20rpx;
		font-size: 30rpx;
	}

	.con .cons {
		font-size: 20rpx;
		color: rgb(44, 117, 75);
	}

	.con .name {
		font-size: 25rpx;
		color: rgb(110, 112, 114);
		padding-bottom: 20rpx;
	}

	.phone {
		display: flex;
		align-items: center;

	}

	.myClaas {
		font-size: 100rpx;
		color: red;
	}

	.phone button {
		display: flex;
		align-items: center;
		justify-content: center;
		height: 100%;
		width: 200rpx;
		padding: 0 0;

		background-color: rgb(98, 145, 110);
	}
</style>