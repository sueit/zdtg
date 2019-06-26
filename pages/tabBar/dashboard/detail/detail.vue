<template>
	<view class="example">
		<view class="example-title">纵向排列</view>
		<uni-steps :options="list2" :active="active" direction="column" />
	</view>
</template>
<script>
	import uniSteps from '@/components/uni-steps/uni-steps.vue'
	export default {
		components: {
			uniSteps
		},
		data() {
			return {
				title: '',
					active: 1,
				list2: [{
					title: '买家下单',
					desc: '2018-11-11'
				}, {
					title: '卖家发货',
					desc: '2018-11-12'
				}, {
					title: '买家签收',
					desc: '2018-11-13'
				}, {
					title: '交易完成',
					desc: '2018-11-14'
				}]
			}
		},
		onLoad(e) {
			this.title = e.title || '';
		}
	}
</script>
<style>
	page {
		display: flex;
		flex-direction: column;
		box-sizing: border-box;
		background-color: #62c2e7
	}
</style>
