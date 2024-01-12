<template>

	<view class="dynamic">
		<view class="container">
			<view class="pubTitle">
				<view class="txt">近期活动公布</view>
				<navigator class="more" bindtap="btnCC">更多 ></navigator>
			</view>

			<view class="dyMain">

				<navigator class="dyItem" url="/pages/detail/detail" v-for="(item, index) in activitys">
					<view class="pic">
						<image :src=item.imgs></image>
					</view>
					<view class="txt">
						<view class="title">{{item.title}}</view>
						<view class="infoandtime">
							<text class="author">地点：{{item.address}}</text>
							<text space="ensp"> - </text>
							<text class="time">时间：{{item.time}}</text>
						</view>
					</view>
				</navigator>

			</view>

		</view>
	</view>


</template>

<script>
	export default {
		name: "notice",
		props: ["activitys"],
		data() {
			return {

			};
		}
	}
</script>

<style lang="scss">
	.dynamic {
		padding: 90rpx 0 70rpx;
	}

	.pubTitle {
		display: flex;
		justify-content: space-between;
		padding-bottom: 20rpx;
		font-size: 26rpx;
	}

	.dyItem {
		display: flex;
		padding: 15rpx 0;
		border: 1rpx dashed #f4f4f4;
		justify-content: space-between;
	}

	.dyItem .pic {
		width: 230rpx;
		height: 150rpx;
	}

	.dyItem .pic image {
		width: 100%;
		height: 100%;
	}

	.dyItem .txt {
		width: 440rpx;
		display: flex;
		flex-direction: column;
		justify-content: space-between;
	}

	.dyItem .title {
		font-size: 30rpx;
	}

	.dyItem .infoandtime {
		font-size: 26rpx;
		color: #888;
	}

	.infoandtime text {
		font-size: 22rpx;
	}
</style>