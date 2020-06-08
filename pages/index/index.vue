<template>
	<view class="content">
		<cropper :option="cropperOption" ref="cropper"></cropper>
	</view>
</template>

<script>
	import cropper from '../../components/mpvue-cropper.vue'
	export default {
		components:{
			cropper
		},
		data() {
			return {
				cropperOption:{
					id: 'canvasId',
					targetId: 'targetId',
					pixelRatio: wx.getSystemInfoSync().pixelRatio
				}
			}
		},
		onLoad() {

		},
		methods: {

		},
		mounted:function(){
			this.$refs.cropper.pushOrigin('https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1591633864720&di=ebfa3b33add1640409e50b36c9fcc266&imgtype=0&src=http%3A%2F%2Fa2.att.hudong.com%2F36%2F48%2F19300001357258133412489354717.jpg')
		}
	}
</script>

<style>
	.content {
		width: 100vw;
		height: 100vh;
	}
</style>
