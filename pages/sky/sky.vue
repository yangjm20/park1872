<template>
	<view class="page">

		<view class="top0">


			<view class="top">
				<view class="top1">
					<view>21</view>
					<view class="skystutas">晴</view>
				</view>
				<view class="top2">
					<view class="keyvalue">
						<image class="pic1" src="/static/images/temperature.png"></image>
						<view>14~24</view>
					</view>
					<view class="keyvalue">
						<image class="pic1" src="/static/images/wind.png"></image>
						<view>0级</view>
					</view>

					<view class="keyvalue">
						<image class="pic1" src="/static/images/humidity.png"></image>
						<view>62%</view>
					</view>

				</view>
			</view>

		</view>

		<view class="middle">

			<view class="topbox">
				<view class="boxtitle">
					<view class="title">
						<view class="tle">今天</view>
						<view class="val">优</view>
					</view>
					<view class="status">晴</view>
				</view>
				<view class="boxvalue">
					<view>14～24</view>
					<image class="pic" src="/static/images/sky_fine.png"></image>
				</view>
			</view>

			<view class="topbox">
				<view class="boxtitle">
					<view class="title">
						<view class="tle">明天</view>
						<view class="val">优</view>
					</view>
					<view class="status">晴</view>
				</view>
				<view class="boxvalue ">
					<view>14～24</view>
					<image class="pic" src="/static/images/sky_fine.png"></image>
				</view>
			</view>
		</view>

		<view class="boxmain">

			<view class="title">未来20小时</view>
			<scroll-view class="major" scroll-x>
				<view class="box" v-for="item in hourData.result.hourly.temperature">
					<view> {{parseT(item.datetime,'{h}')}}</view>
					<image class="pic" src="/static/images/sky_fine.png"></image>
					<view class="temperature">{{item.value}}</view>
					<view class="bottom">
						<view>优</view>
						<view>30</view>
					</view>
				</view>
			</scroll-view>
		</view>

	</view>
</template>

<script>
	import {parseTime} from "@/utils/tools.js"
	
	export default {
		data() {
			return {
				parseT:parseTime,
				DayData: {

				},
				hourData: {
					"status": "ok",
					"api_version": "v2.6",
					"api_status": "alpha",
					"lang": "zh_CN",
					"unit": "metric",
					"tzshift": 28800,
					"timezone": "Asia/Shanghai",
					"server_time": 1698559759,
					"location": [39.2072, 101.6656],
					"result": {
						"hourly": {
							"status": "ok",
							"description": "多云，云渐少，今天傍晚19点钟后转至晴",
							"precipitation": [{
								"datetime": "2023-10-29T14:00+08:00",
								"value": 0.0,
								"probability": 0
							}, {
								"datetime": "2023-10-29T15:00+08:00",
								"value": 0.0,
								"probability": 0
							}, {
								"datetime": "2023-10-29T16:00+08:00",
								"value": 0.0,
								"probability": 0
							}, {
								"datetime": "2023-10-29T17:00+08:00",
								"value": 0.0,
								"probability": 0
							}, {
								"datetime": "2023-10-29T18:00+08:00",
								"value": 0.0,
								"probability": 0
							}, {
								"datetime": "2023-10-29T19:00+08:00",
								"value": 0.0,
								"probability": 0
							}, {
								"datetime": "2023-10-29T20:00+08:00",
								"value": 0.0,
								"probability": 0
							}, {
								"datetime": "2023-10-29T21:00+08:00",
								"value": 0.0,
								"probability": 0
							}, {
								"datetime": "2023-10-29T22:00+08:00",
								"value": 0.0,
								"probability": 0
							}, {
								"datetime": "2023-10-29T23:00+08:00",
								"value": 0.0,
								"probability": 0
							}, {
								"datetime": "2023-10-30T00:00+08:00",
								"value": 0.0,
								"probability": 0
							}, {
								"datetime": "2023-10-30T01:00+08:00",
								"value": 0.0,
								"probability": 0
							}, {
								"datetime": "2023-10-30T02:00+08:00",
								"value": 0.0,
								"probability": 0
							}, {
								"datetime": "2023-10-30T03:00+08:00",
								"value": 0.0,
								"probability": 0
							}, {
								"datetime": "2023-10-30T04:00+08:00",
								"value": 0.0,
								"probability": 0
							}, {
								"datetime": "2023-10-30T05:00+08:00",
								"value": 0.0,
								"probability": 0
							}, {
								"datetime": "2023-10-30T06:00+08:00",
								"value": 0.0,
								"probability": 0
							}, {
								"datetime": "2023-10-30T07:00+08:00",
								"value": 0.0,
								"probability": 0
							}, {
								"datetime": "2023-10-30T08:00+08:00",
								"value": 0.0,
								"probability": 0
							}, {
								"datetime": "2023-10-30T09:00+08:00",
								"value": 0.0,
								"probability": 0
							}, {
								"datetime": "2023-10-30T10:00+08:00",
								"value": 0.0,
								"probability": 0
							}, {
								"datetime": "2023-10-30T11:00+08:00",
								"value": 0.0,
								"probability": 0
							}, {
								"datetime": "2023-10-30T12:00+08:00",
								"value": 0.0,
								"probability": 0
							}, {
								"datetime": "2023-10-30T13:00+08:00",
								"value": 0.0,
								"probability": 0
							}],
							"temperature": [{
								"datetime": "2023-10-29T14:00+08:00",
								"value": 17.0
							}, {
								"datetime": "2023-10-29T15:00+08:00",
								"value": 17.83
							}, {
								"datetime": "2023-10-29T16:00+08:00",
								"value": 17.67
							}, {
								"datetime": "2023-10-29T17:00+08:00",
								"value": 17.5
							}, {
								"datetime": "2023-10-29T18:00+08:00",
								"value": 16.33
							}, {
								"datetime": "2023-10-29T19:00+08:00",
								"value": 15.17
							}, {
								"datetime": "2023-10-29T20:00+08:00",
								"value": 13.0
							}, {
								"datetime": "2023-10-29T21:00+08:00",
								"value": 13.0
							}, {
								"datetime": "2023-10-29T22:00+08:00",
								"value": 11.1
							}, {
								"datetime": "2023-10-29T23:00+08:00",
								"value": 9.4
							}, {
								"datetime": "2023-10-30T00:00+08:00",
								"value": 7.9
							}, {
								"datetime": "2023-10-30T01:00+08:00",
								"value": 6.6
							}, {
								"datetime": "2023-10-30T02:00+08:00",
								"value": 5.5
							}, {
								"datetime": "2023-10-30T03:00+08:00",
								"value": 4.6
							}, {
								"datetime": "2023-10-30T04:00+08:00",
								"value": 4.2
							}, {
								"datetime": "2023-10-30T05:00+08:00",
								"value": 3.6
							}, {
								"datetime": "2023-10-30T06:00+08:00",
								"value": 3.3
							}, {
								"datetime": "2023-10-30T07:00+08:00",
								"value": 3.0
							}, {
								"datetime": "2023-10-30T08:00+08:00",
								"value": 6.2
							}, {
								"datetime": "2023-10-30T09:00+08:00",
								"value": 7.7
							}, {
								"datetime": "2023-10-30T10:00+08:00",
								"value": 9.1
							}, {
								"datetime": "2023-10-30T11:00+08:00",
								"value": 10.5
							}, {
								"datetime": "2023-10-30T12:00+08:00",
								"value": 12.0
							}, {
								"datetime": "2023-10-30T13:00+08:00",
								"value": 13.45
							}],
							"apparent_temperature": [{
								"datetime": "2023-10-29T14:00+08:00",
								"value": 15.0
							}, {
								"datetime": "2023-10-29T15:00+08:00",
								"value": 16.5
							}, {
								"datetime": "2023-10-29T16:00+08:00",
								"value": 16.3
							}, {
								"datetime": "2023-10-29T17:00+08:00",
								"value": 15.8
							}, {
								"datetime": "2023-10-29T18:00+08:00",
								"value": 14.2
							}, {
								"datetime": "2023-10-29T19:00+08:00",
								"value": 12.4
							}, {
								"datetime": "2023-10-29T20:00+08:00",
								"value": 9.6
							}, {
								"datetime": "2023-10-29T21:00+08:00",
								"value": 9.8
							}, {
								"datetime": "2023-10-29T22:00+08:00",
								"value": 7.5
							}, {
								"datetime": "2023-10-29T23:00+08:00",
								"value": 5.6
							}, {
								"datetime": "2023-10-30T00:00+08:00",
								"value": 3.9
							}, {
								"datetime": "2023-10-30T01:00+08:00",
								"value": 2.5
							}, {
								"datetime": "2023-10-30T02:00+08:00",
								"value": 1.1
							}, {
								"datetime": "2023-10-30T03:00+08:00",
								"value": 0.4
							}, {
								"datetime": "2023-10-30T04:00+08:00",
								"value": -0.4
							}, {
								"datetime": "2023-10-30T05:00+08:00",
								"value": -1.2
							}, {
								"datetime": "2023-10-30T06:00+08:00",
								"value": -1.2
							}, {
								"datetime": "2023-10-30T07:00+08:00",
								"value": -1.0
							}, {
								"datetime": "2023-10-30T08:00+08:00",
								"value": 2.8
							}, {
								"datetime": "2023-10-30T09:00+08:00",
								"value": 3.9
							}, {
								"datetime": "2023-10-30T10:00+08:00",
								"value": 5.6
							}, {
								"datetime": "2023-10-30T11:00+08:00",
								"value": 5.9
							}, {
								"datetime": "2023-10-30T12:00+08:00",
								"value": 6.4
							}, {
								"datetime": "2023-10-30T13:00+08:00",
								"value": 7.7
							}],
							"wind": [{
								"datetime": "2023-10-29T14:00+08:00",
								"speed": 3.6,
								"direction": 70.0
							}, {
								"datetime": "2023-10-29T15:00+08:00",
								"speed": 0.91,
								"direction": 313.24
							}, {
								"datetime": "2023-10-29T16:00+08:00",
								"speed": 0.82,
								"direction": 67.03
							}, {
								"datetime": "2023-10-29T17:00+08:00",
								"speed": 2.38,
								"direction": 112.72
							}, {
								"datetime": "2023-10-29T18:00+08:00",
								"speed": 4.87,
								"direction": 162.15
							}, {
								"datetime": "2023-10-29T19:00+08:00",
								"speed": 7.95,
								"direction": 157.07
							}, {
								"datetime": "2023-10-29T20:00+08:00",
								"speed": 10.89,
								"direction": 144.49
							}, {
								"datetime": "2023-10-29T21:00+08:00",
								"speed": 9.85,
								"direction": 141.69
							}, {
								"datetime": "2023-10-29T22:00+08:00",
								"speed": 10.99,
								"direction": 129.24
							}, {
								"datetime": "2023-10-29T23:00+08:00",
								"speed": 11.43,
								"direction": 129.81
							}, {
								"datetime": "2023-10-30T00:00+08:00",
								"speed": 12.07,
								"direction": 138.18
							}, {
								"datetime": "2023-10-30T01:00+08:00",
								"speed": 12.59,
								"direction": 139.71
							}, {
								"datetime": "2023-10-30T02:00+08:00",
								"speed": 13.33,
								"direction": 141.11
							}, {
								"datetime": "2023-10-30T03:00+08:00",
								"speed": 12.11,
								"direction": 147.47
							}, {
								"datetime": "2023-10-30T04:00+08:00",
								"speed": 13.78,
								"direction": 160.37
							}, {
								"datetime": "2023-10-30T05:00+08:00",
								"speed": 14.78,
								"direction": 175.36
							}, {
								"datetime": "2023-10-30T06:00+08:00",
								"speed": 12.92,
								"direction": 184.38
							}, {
								"datetime": "2023-10-30T07:00+08:00",
								"speed": 10.05,
								"direction": 204.59
							}, {
								"datetime": "2023-10-30T08:00+08:00",
								"speed": 7.95,
								"direction": 227.88
							}, {
								"datetime": "2023-10-30T09:00+08:00",
								"speed": 10.09,
								"direction": 248.33
							}, {
								"datetime": "2023-10-30T10:00+08:00",
								"speed": 8.89,
								"direction": 276.77
							}, {
								"datetime": "2023-10-30T11:00+08:00",
								"speed": 15.16,
								"direction": 299.2
							}, {
								"datetime": "2023-10-30T12:00+08:00",
								"speed": 21.04,
								"direction": 292.26
							}, {
								"datetime": "2023-10-30T13:00+08:00",
								"speed": 22.55,
								"direction": 291.71
							}],
							"humidity": [{
								"datetime": "2023-10-29T14:00+08:00",
								"value": 0.17
							}, {
								"datetime": "2023-10-29T15:00+08:00",
								"value": 0.19
							}, {
								"datetime": "2023-10-29T16:00+08:00",
								"value": 0.19
							}, {
								"datetime": "2023-10-29T17:00+08:00",
								"value": 0.18
							}, {
								"datetime": "2023-10-29T18:00+08:00",
								"value": 0.22
							}, {
								"datetime": "2023-10-29T19:00+08:00",
								"value": 0.23
							}, {
								"datetime": "2023-10-29T20:00+08:00",
								"value": 0.24
							}, {
								"datetime": "2023-10-29T21:00+08:00",
								"value": 0.26
							}, {
								"datetime": "2023-10-29T22:00+08:00",
								"value": 0.26
							}, {
								"datetime": "2023-10-29T23:00+08:00",
								"value": 0.27
							}, {
								"datetime": "2023-10-30T00:00+08:00",
								"value": 0.28
							}, {
								"datetime": "2023-10-30T01:00+08:00",
								"value": 0.29
							}, {
								"datetime": "2023-10-30T02:00+08:00",
								"value": 0.29
							}, {
								"datetime": "2023-10-30T03:00+08:00",
								"value": 0.28
							}, {
								"datetime": "2023-10-30T04:00+08:00",
								"value": 0.28
							}, {
								"datetime": "2023-10-30T05:00+08:00",
								"value": 0.27
							}, {
								"datetime": "2023-10-30T06:00+08:00",
								"value": 0.26
							}, {
								"datetime": "2023-10-30T07:00+08:00",
								"value": 0.27
							}, {
								"datetime": "2023-10-30T08:00+08:00",
								"value": 0.25
							}, {
								"datetime": "2023-10-30T09:00+08:00",
								"value": 0.22
							}, {
								"datetime": "2023-10-30T10:00+08:00",
								"value": 0.2
							}, {
								"datetime": "2023-10-30T11:00+08:00",
								"value": 0.17
							}, {
								"datetime": "2023-10-30T12:00+08:00",
								"value": 0.15
							}, {
								"datetime": "2023-10-30T13:00+08:00",
								"value": 0.15
							}],
							"cloudrate": [{
								"datetime": "2023-10-29T14:00+08:00",
								"value": 0.78
							}, {
								"datetime": "2023-10-29T15:00+08:00",
								"value": 0.57
							}, {
								"datetime": "2023-10-29T16:00+08:00",
								"value": 0.49
							}, {
								"datetime": "2023-10-29T17:00+08:00",
								"value": 0.41
							}, {
								"datetime": "2023-10-29T18:00+08:00",
								"value": 0.27
							}, {
								"datetime": "2023-10-29T19:00+08:00",
								"value": 0.06
							}, {
								"datetime": "2023-10-29T20:00+08:00",
								"value": 0.03
							}, {
								"datetime": "2023-10-29T21:00+08:00",
								"value": 0.0
							}, {
								"datetime": "2023-10-29T22:00+08:00",
								"value": 0.0
							}, {
								"datetime": "2023-10-29T23:00+08:00",
								"value": 0.0
							}, {
								"datetime": "2023-10-30T00:00+08:00",
								"value": 0.0
							}, {
								"datetime": "2023-10-30T01:00+08:00",
								"value": 0.0
							}, {
								"datetime": "2023-10-30T02:00+08:00",
								"value": 0.0
							}, {
								"datetime": "2023-10-30T03:00+08:00",
								"value": 0.0
							}, {
								"datetime": "2023-10-30T04:00+08:00",
								"value": 0.0
							}, {
								"datetime": "2023-10-30T05:00+08:00",
								"value": 0.0
							}, {
								"datetime": "2023-10-30T06:00+08:00",
								"value": 0.0
							}, {
								"datetime": "2023-10-30T07:00+08:00",
								"value": 0.0
							}, {
								"datetime": "2023-10-30T08:00+08:00",
								"value": 0.0
							}, {
								"datetime": "2023-10-30T09:00+08:00",
								"value": 0.0
							}, {
								"datetime": "2023-10-30T10:00+08:00",
								"value": 0.0
							}, {
								"datetime": "2023-10-30T11:00+08:00",
								"value": 0.0
							}, {
								"datetime": "2023-10-30T12:00+08:00",
								"value": 0.0
							}, {
								"datetime": "2023-10-30T13:00+08:00",
								"value": 0.04
							}],
							"skycon": [{
								"datetime": "2023-10-29T14:00+08:00",
								"value": "PARTLY_CLOUDY_DAY"
							}, {
								"datetime": "2023-10-29T15:00+08:00",
								"value": "PARTLY_CLOUDY_DAY"
							}, {
								"datetime": "2023-10-29T16:00+08:00",
								"value": "PARTLY_CLOUDY_DAY"
							}, {
								"datetime": "2023-10-29T17:00+08:00",
								"value": "PARTLY_CLOUDY_DAY"
							}, {
								"datetime": "2023-10-29T18:00+08:00",
								"value": "PARTLY_CLOUDY_DAY"
							}, {
								"datetime": "2023-10-29T19:00+08:00",
								"value": "CLEAR_NIGHT"
							}, {
								"datetime": "2023-10-29T20:00+08:00",
								"value": "CLEAR_NIGHT"
							}, {
								"datetime": "2023-10-29T21:00+08:00",
								"value": "CLEAR_NIGHT"
							}, {
								"datetime": "2023-10-29T22:00+08:00",
								"value": "CLEAR_NIGHT"
							}, {
								"datetime": "2023-10-29T23:00+08:00",
								"value": "CLEAR_NIGHT"
							}, {
								"datetime": "2023-10-30T00:00+08:00",
								"value": "CLEAR_NIGHT"
							}, {
								"datetime": "2023-10-30T01:00+08:00",
								"value": "CLEAR_NIGHT"
							}, {
								"datetime": "2023-10-30T02:00+08:00",
								"value": "CLEAR_NIGHT"
							}, {
								"datetime": "2023-10-30T03:00+08:00",
								"value": "CLEAR_NIGHT"
							}, {
								"datetime": "2023-10-30T04:00+08:00",
								"value": "CLEAR_NIGHT"
							}, {
								"datetime": "2023-10-30T05:00+08:00",
								"value": "CLEAR_NIGHT"
							}, {
								"datetime": "2023-10-30T06:00+08:00",
								"value": "CLEAR_NIGHT"
							}, {
								"datetime": "2023-10-30T07:00+08:00",
								"value": "CLEAR_NIGHT"
							}, {
								"datetime": "2023-10-30T08:00+08:00",
								"value": "CLEAR_DAY"
							}, {
								"datetime": "2023-10-30T09:00+08:00",
								"value": "CLEAR_DAY"
							}, {
								"datetime": "2023-10-30T10:00+08:00",
								"value": "CLEAR_DAY"
							}, {
								"datetime": "2023-10-30T11:00+08:00",
								"value": "CLEAR_DAY"
							}, {
								"datetime": "2023-10-30T12:00+08:00",
								"value": "CLEAR_DAY"
							}, {
								"datetime": "2023-10-30T13:00+08:00",
								"value": "CLEAR_DAY"
							}],
							"pressure": [{
								"datetime": "2023-10-29T14:00+08:00",
								"value": 84913.142
							}, {
								"datetime": "2023-10-29T15:00+08:00",
								"value": 84843.963
							}, {
								"datetime": "2023-10-29T16:00+08:00",
								"value": 84843.963
							}, {
								"datetime": "2023-10-29T17:00+08:00",
								"value": 84843.963
							}, {
								"datetime": "2023-10-29T18:00+08:00",
								"value": 84890.152
							}, {
								"datetime": "2023-10-29T19:00+08:00",
								"value": 84923.963
							}, {
								"datetime": "2023-10-29T20:00+08:00",
								"value": 84923.963
							}, {
								"datetime": "2023-10-29T21:00+08:00",
								"value": 84916.738
							}, {
								"datetime": "2023-10-29T22:00+08:00",
								"value": 84893.748
							}, {
								"datetime": "2023-10-29T23:00+08:00",
								"value": 84890.152
							}, {
								"datetime": "2023-10-30T00:00+08:00",
								"value": 84843.963
							}, {
								"datetime": "2023-10-30T01:00+08:00",
								"value": 84813.748
							}, {
								"datetime": "2023-10-30T02:00+08:00",
								"value": 84763.963
							}, {
								"datetime": "2023-10-30T03:00+08:00",
								"value": 84683.963
							}, {
								"datetime": "2023-10-30T04:00+08:00",
								"value": 84683.963
							}, {
								"datetime": "2023-10-30T05:00+08:00",
								"value": 84683.963
							}, {
								"datetime": "2023-10-30T06:00+08:00",
								"value": 84733.748
							}, {
								"datetime": "2023-10-30T07:00+08:00",
								"value": 84763.963
							}, {
								"datetime": "2023-10-30T08:00+08:00",
								"value": 84843.963
							}, {
								"datetime": "2023-10-30T09:00+08:00",
								"value": 84923.963
							}, {
								"datetime": "2023-10-30T10:00+08:00",
								"value": 84923.963
							}, {
								"datetime": "2023-10-30T11:00+08:00",
								"value": 84970.152
							}, {
								"datetime": "2023-10-30T12:00+08:00",
								"value": 84973.748
							}, {
								"datetime": "2023-10-30T13:00+08:00",
								"value": 84916.738
							}],
							"visibility": [{
								"datetime": "2023-10-29T14:00+08:00",
								"value": 26.95
							}, {
								"datetime": "2023-10-29T15:00+08:00",
								"value": 26.95
							}, {
								"datetime": "2023-10-29T16:00+08:00",
								"value": 26.95
							}, {
								"datetime": "2023-10-29T17:00+08:00",
								"value": 26.95
							}, {
								"datetime": "2023-10-29T18:00+08:00",
								"value": 26.95
							}, {
								"datetime": "2023-10-29T19:00+08:00",
								"value": 26.95
							}, {
								"datetime": "2023-10-29T20:00+08:00",
								"value": 26.95
							}, {
								"datetime": "2023-10-29T21:00+08:00",
								"value": 26.95
							}, {
								"datetime": "2023-10-29T22:00+08:00",
								"value": 26.95
							}, {
								"datetime": "2023-10-29T23:00+08:00",
								"value": 26.95
							}, {
								"datetime": "2023-10-30T00:00+08:00",
								"value": 26.95
							}, {
								"datetime": "2023-10-30T01:00+08:00",
								"value": 26.95
							}, {
								"datetime": "2023-10-30T02:00+08:00",
								"value": 26.95
							}, {
								"datetime": "2023-10-30T03:00+08:00",
								"value": 26.95
							}, {
								"datetime": "2023-10-30T04:00+08:00",
								"value": 26.95
							}, {
								"datetime": "2023-10-30T05:00+08:00",
								"value": 26.95
							}, {
								"datetime": "2023-10-30T06:00+08:00",
								"value": 26.95
							}, {
								"datetime": "2023-10-30T07:00+08:00",
								"value": 26.95
							}, {
								"datetime": "2023-10-30T08:00+08:00",
								"value": 26.95
							}, {
								"datetime": "2023-10-30T09:00+08:00",
								"value": 26.95
							}, {
								"datetime": "2023-10-30T10:00+08:00",
								"value": 26.95
							}, {
								"datetime": "2023-10-30T11:00+08:00",
								"value": 26.95
							}, {
								"datetime": "2023-10-30T12:00+08:00",
								"value": 26.95
							}, {
								"datetime": "2023-10-30T13:00+08:00",
								"value": 26.95
							}],
							"dswrf": [{
								"datetime": "2023-10-29T14:00+08:00",
								"value": 358.194
							}, {
								"datetime": "2023-10-29T15:00+08:00",
								"value": 445.937
							}, {
								"datetime": "2023-10-29T16:00+08:00",
								"value": 401.553
							}, {
								"datetime": "2023-10-29T17:00+08:00",
								"value": 343.801
							}, {
								"datetime": "2023-10-29T18:00+08:00",
								"value": 277.01
							}, {
								"datetime": "2023-10-29T19:00+08:00",
								"value": 221.751
							}, {
								"datetime": "2023-10-29T20:00+08:00",
								"value": 184.977
							}, {
								"datetime": "2023-10-29T21:00+08:00",
								"value": 0.0
							}, {
								"datetime": "2023-10-29T22:00+08:00",
								"value": 0.0
							}, {
								"datetime": "2023-10-29T23:00+08:00",
								"value": 0.0
							}, {
								"datetime": "2023-10-30T00:00+08:00",
								"value": 0.0
							}, {
								"datetime": "2023-10-30T01:00+08:00",
								"value": 0.0
							}, {
								"datetime": "2023-10-30T02:00+08:00",
								"value": 0.0
							}, {
								"datetime": "2023-10-30T03:00+08:00",
								"value": 0.0
							}, {
								"datetime": "2023-10-30T04:00+08:00",
								"value": 0.0
							}, {
								"datetime": "2023-10-30T05:00+08:00",
								"value": 0.0
							}, {
								"datetime": "2023-10-30T06:00+08:00",
								"value": 0.0
							}, {
								"datetime": "2023-10-30T07:00+08:00",
								"value": 0.0
							}, {
								"datetime": "2023-10-30T08:00+08:00",
								"value": 0.0
							}, {
								"datetime": "2023-10-30T09:00+08:00",
								"value": 87.138
							}, {
								"datetime": "2023-10-30T10:00+08:00",
								"value": 158.274
							}, {
								"datetime": "2023-10-30T11:00+08:00",
								"value": 223.055
							}, {
								"datetime": "2023-10-30T12:00+08:00",
								"value": 295.107
							}, {
								"datetime": "2023-10-30T13:00+08:00",
								"value": 352.69
							}],
							"air_quality": {
								"aqi": [{
										"datetime": "2023-10-29T14:00+08:00",
										"value": {
											"chn": 0,
											"usa": 3
										}
									},
									{
										"datetime": "2023-10-29T15:00+08:00",
										"value": {
											"chn": 0,
											"usa": 3
										}
									},
									{
										"datetime": "2023-10-29T16:00+08:00",
										"value": {
											"chn": 0,
											"usa": 3
										}
									},
									{
										"datetime": "2023-10-29T17:00+08:00",
										"value": {
											"chn": 0,
											"usa": 3
										}
									},
									{
										"datetime": "2023-10-29T18:00+08:00",
										"value": {
											"chn": 0,
											"usa": 3
										}
									},
									{
										"datetime": "2023-10-29T19:00+08:00",
										"value": {
											"chn": 0,
											"usa": 3
										}
									},
									{
										"datetime": "2023-10-29T20:00+08:00",
										"value": {
											"chn": 0,
											"usa": 3
										}
									},
									{
										"datetime": "2023-10-29T21:00+08:00",
										"value": {
											"chn": 0,
											"usa": 3
										}
									},
									{
										"datetime": "2023-10-29T22:00+08:00",
										"value": {
											"chn": 0,
											"usa": 3
										}
									},
									{
										"datetime": "2023-10-29T23:00+08:00",
										"value": {
											"chn": 0,
											"usa": 3
										}
									},
									{
										"datetime": "2023-10-30T00:00+08:00",
										"value": {
											"chn": 0,
											"usa": 3
										}
									},
									{
										"datetime": "2023-10-30T01:00+08:00",
										"value": {
											"chn": 0,
											"usa": 3
										}
									},
									{
										"datetime": "2023-10-30T02:00+08:00",
										"value": {
											"chn": 0,
											"usa": 3
										}
									},
									{
										"datetime": "2023-10-30T03:00+08:00",
										"value": {
											"chn": 0,
											"usa": 3
										}
									},
									{
										"datetime": "2023-10-30T04:00+08:00",
										"value": {
											"chn": 0,
											"usa": 3
										}
									},
									{
										"datetime": "2023-10-30T05:00+08:00",
										"value": {
											"chn": 0,
											"usa": 3
										}
									},
									{
										"datetime": "2023-10-30T06:00+08:00",
										"value": {
											"chn": 0,
											"usa": 3
										}
									},
									{
										"datetime": "2023-10-30T07:00+08:00",
										"value": {
											"chn": 0,
											"usa": 3
										}
									},
									{
										"datetime": "2023-10-30T08:00+08:00",
										"value": {
											"chn": 0,
											"usa": 3
										}
									},
									{
										"datetime": "2023-10-30T09:00+08:00",
										"value": {
											"chn": 0,
											"usa": 3
										}
									},
									{
										"datetime": "2023-10-30T10:00+08:00",
										"value": {
											"chn": 0,
											"usa": 3
										}
									},
									{
										"datetime": "2023-10-30T11:00+08:00",
										"value": {
											"chn": 0,
											"usa": 3
										}
									},
									{
										"datetime": "2023-10-30T12:00+08:00",
										"value": {
											"chn": 0,
											"usa": 3
										}
									},
									{
										"datetime": "2023-10-30T13:00+08:00",
										"value": {
											"chn": 0,
											"usa": 3
										}
									}
								],
								"pm25": [{
									"datetime": "2023-10-29T14:00+08:00",
									"value": 0
								}, {
									"datetime": "2023-10-29T15:00+08:00",
									"value": 0
								}, {
									"datetime": "2023-10-29T16:00+08:00",
									"value": 0
								}, {
									"datetime": "2023-10-29T17:00+08:00",
									"value": 0
								}, {
									"datetime": "2023-10-29T18:00+08:00",
									"value": 0
								}, {
									"datetime": "2023-10-29T19:00+08:00",
									"value": 0
								}, {
									"datetime": "2023-10-29T20:00+08:00",
									"value": 0
								}, {
									"datetime": "2023-10-29T21:00+08:00",
									"value": 0
								}, {
									"datetime": "2023-10-29T22:00+08:00",
									"value": 0
								}, {
									"datetime": "2023-10-29T23:00+08:00",
									"value": 0
								}, {
									"datetime": "2023-10-30T00:00+08:00",
									"value": 0
								}, {
									"datetime": "2023-10-30T01:00+08:00",
									"value": 0
								}, {
									"datetime": "2023-10-30T02:00+08:00",
									"value": 0
								}, {
									"datetime": "2023-10-30T03:00+08:00",
									"value": 0
								}, {
									"datetime": "2023-10-30T04:00+08:00",
									"value": 0
								}, {
									"datetime": "2023-10-30T05:00+08:00",
									"value": 0
								}, {
									"datetime": "2023-10-30T06:00+08:00",
									"value": 0
								}, {
									"datetime": "2023-10-30T07:00+08:00",
									"value": 0
								}, {
									"datetime": "2023-10-30T08:00+08:00",
									"value": 0
								}, {
									"datetime": "2023-10-30T09:00+08:00",
									"value": 0
								}, {
									"datetime": "2023-10-30T10:00+08:00",
									"value": 0
								}, {
									"datetime": "2023-10-30T11:00+08:00",
									"value": 0
								}, {
									"datetime": "2023-10-30T12:00+08:00",
									"value": 0
								}, {
									"datetime": "2023-10-30T13:00+08:00",
									"value": 0
								}]
							}
						},
						"primary": 0,
						"forecast_keypoint": "多云，云渐少，今天傍晚19点钟后转至晴"
					}
				},
			};
		},
		methods: {
			filter(time) {
				
				var t = getData(time)
				var h = t.getData()
				console.log(h)
			},
		}
	}
</script>

<style lang="scss">
	.page {
		height: 100vh;
	}

	.top0 {
		padding-top: 50rpx;
		display: flex;
		flex-direction: column;
		align-items: center;
	}

	.top {
		width: 99%;
		height: 500rpx;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		background-color: rgb(189, 214, 243);
		margin-bottom: 10rpx;
		border-radius: 30rpx;

	}

	.top .top2 {
		display: flex;
		justify-content: space-between;
	}

	.top .top1 {
		display: flex;
		align-items: flex-end;
		font-size: 150rpx;
		height: 200rpx;
	}

	.top1 .skystutas {
		font-size: 26rpx;
		margin-bottom: 50rpx;
		margin-left: 20rpx;
	}


	.pic1 {
		width: 40rpx;
		height: 40rpx;
	}

	.top2 .keyvalue {
		display: flex;
		justify-content: center;
		margin-left: 30rpx;
	}

	.keyvalue view {
		margin-left: 10rpx;
	}


	.middle {
		border-radius: 20rpx;
		background-color: rgb(189, 214, 243);
		color: rgb(2, 2, 2);

		display: flex;
		justify-content: space-between;
	}


	.middle .topbox {
		width: 50%;
		display: flex;

	}

	.middle .title {
		font-size: 26rpx;
		display: flex;
		justify-content: left;
	}

	.topbox .boxtitle {
		flex: 1;
		display: flex;
		flex-direction: column;
		justify-content: space-between;
	}

	.boxtitle view {
		margin: 10rpx 20rpx;
	}

	.boxtitle .status {
		margin: 0rpx 40rpx;
		margin-bottom: 20rpx;
		padding-bottom: 10rpx;
		font-size: 30rpx;
	}


	.boxvalue view {
		margin: 10rpx 10rpx;
	}

	.boxvalue view {
		margin: 10rpx 10rpx;
	}

	.boxtitle .val {
		margin-top: 10rpx;
		font-size: 20rpx;
	}




	.boxmain {
		border-radius: 20rpx;
		margin-top: 20rpx;

		background-color: rgb(189, 214, 243);
	}

	.boxmain .title {
		text-align: center;
		padding: 20rpx 0;

		color: rgb(7, 8, 8);
		font-size: 26rpx;
	}

	.major {
		white-space: nowrap;
	}

	.major .box {
		text-align: center;
		width: 128rpx;
		display: inline-block;
	}

	.pic {
		width: 70rpx;
		height: 70rpx;
	}


	.box .time {
		font-size: 24rpx;
		padding-bottom: 20rpx;
		color: rgba(107, 105, 103, 0.808);
	}

	.box .temperature {
		font-size: 24rpx;
		padding: 20rpx 0;

		color: rgb(8, 8, 8);
	}

	.box .bottom {
		font-size: 24rpx;
		padding: 10rpx 0;
		margin-bottom: 20rpx;
		color: rgb(24, 138, 67);
	}
</style>