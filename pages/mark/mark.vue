<template>
	
		<notice :activitys="goods"></notice>
</template>

<script>
	export default {
		data() {
			return {
				goods: [{
						"title": "自行车",
						"address": "21号楼",
						"time": "2023-11-01",
						"imgs": "/static/images/zixingche.jpeg"
					},
					{
						"title": "钢笔",
						"address": "11号楼",
						"time": "2023-11-01",
						"imgs": "/static/images/gangbi.jpeg"
					},
					{
						"title": "包包",
						"address": "2号楼",
						"time": "2023-11-02",
						"imgs": "/static/images/bao.jpeg"
					}
				]
			};
		}
	}
</script>

<style lang="scss">
	
</style>