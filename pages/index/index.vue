<template>
	<view>

		<view class="header">
			<view class="container selfcontainer">

				<text class="container_text">尊贵的公园1872业主</text>
			</view>
		</view>
		<view class="notic">公示公告</view>
		<view class="banner" bindtap="btnCC">
			<swiper class="swiper" autoplay indicator-dots>
				<swiper-item>
					<image src="/static/images/banner_1.png" />
				</swiper-item>
				<swiper-item>
					<image src="/static/images/banner_2.png" />
				</swiper-item>
			</swiper>
		</view>

		<scroll-view class="major" scroll-x>

			<navigator class="box" hover-class="navigator-hover" @tap="openMap">
				<image class="pic" src="/static/images/daohang.png"></image>
				<view class="txt">导航</view>
			</navigator>

			<navigator class="box" hover-class="navigator-hover" url="/pages/sky/sky" open-type="navigate">
				<image class="pic" src="/static/images/sky.png"></image>
				<view class="txt">天气</view>

			</navigator>

			<navigator class="box" hover-class="navigator-hover" url="/pages/contact/contact" open-type="navigate">
				<image class="pic" src="/static/images/txl_cli.png"></image>
				<view class="txt">通讯录</view>
			</navigator>

			<navigator class="box" hover-class="navigator-hover"
				url="/pages/layout/layout?wxurl=https://mp.weixin.qq.com/s/6D0UBN36RgRg1221toRnUA" open-type="navigate">
				<image class="pic" src="/static/images/huxing.png"></image>
				<view class="txt">户型图</view>
			</navigator>



			<navigator class="box" hover-class="navigator-hover"
				url="/pages/layout/layout?wxurl=https://mp.weixin.qq.com/s/6D0UBN36RgRg1221toRnUA" open-type="navigate">
				<image class="pic" src="/static/images/jianshejinzhan.png"></image>
				<view class="txt">建设进展</view>
			</navigator>

		</scroll-view>

		<notice :activitys="activity"></notice>
		<view class="tarBar">
			<view v-for="(item,index) in arr" class="item" :class="navIndex==index ? 'active' :'' " :key="item.id"
				@click="btnClick(index)">{{item.title}}</view>
		</view>

		<view>{{title}}</view>
		<input type="text" v-model="title" />


	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: "fff",
				navIndex: -1,
				arr: [{
					"id": 1,
					"title": "首页"
				}, {
					"id": 2,
					"title": "新闻"
				}, {
					"id": 3,
					"title": "列表"
				}, {
					"id": 4,
					"title": "我的"
				}],
				activity: [{
						"title": "羽毛球活动",
						"address": "兰香湖",
						"time": "2023-11-01",
						"imgs": "/static/images/yumaoqiu.jpg"
					},
					{
						"title": "宠物活动",
						"address": "兰香湖",
						"time": "2023-11-01",
						"imgs": "/static/images/chongwu.jpeg"
					},
					{
						"title": "亲子活动",
						"address": "兰香湖",
						"time": "2023-11-01",
						"imgs": "/static/images/qinzi.jpeg"
					}
				],
			};
		},

		methods: {
			btnClick(e) {
				this.navIndex = e
			},

			openMap() {
				console.log("location")
				uni.getLocation({
					type: 'gcj02',
					success:function(res) {
						const latitude = 31.032257
						const longitude = 121.472041
						uni.openLocation({
							latitude:latitude,
							longitude:longitude,
							scale: 15,
							address: "紫龙路211弄",
							name: "象屿招商公园1872",
							success:function() {
								console.log("success");
							}
						})
					}
				})
			}
		}
	}
</script>

<style lang="scss">
	.tarBar {
		display: flex;
		justify-content: space-between;
		align-items: center;

		.item {
			flex: 1;

			&.active {
				background-color: red;
			}
		}



	}

	.header {
		width: 750rpx;
		height: 50rpx;
	}

	.selfcontainer {
		display: flex;
		justify-content: center;
	}

	.container_text {
		text-align: center;
		line-height: 50rpx;
		font-size: 30rpx;
		color: rgb(173, 32, 7);
	}

	.notic {
		font-size: 36rpx;
		padding: 0rpx 20rpx;
		color: black;
	}

	.banner {
		width: 100%;
		height: 380rpx;
		padding: 10rpx 10rpx;
	}

	.banner .swiper {
		height: 100%;
		width: 100%;
	}

	.swiper swiper-item {
		border-radius: 20rpx;
	}

	.banner image {
		height: 380rpx;
		width: 100%;
	}

	.major {
		white-space: nowrap;
		padding: 20rpx 0;
	}

	.major .box {
		text-align: center;
		width: 220rpx;
		display: inline-block;
	}

	.major .navigator-hover {
		background-color: rgb(76, 204, 226);
	}

	.major .navigator-hover view {
		color: white;
	}

	.major .pic {
		width: 80rpx;
		height: 80rpx;
	}

	.major .txt {
		font-size: 26rpx;
		margin-top: 10rpx;
		color: rgb(77, 113, 155);
	}
</style>