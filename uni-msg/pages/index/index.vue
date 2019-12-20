<template>
	<view class="content">
		<view class="text-area">
			<text class="title" @click="yangrMsgShow = true">弹出 msg</text>
		</view>
		
		
		<yangr-msg v-if="yangrMsgShow" :title="title" type="success" :info="info" btn="确定" @yangrMsgEvent="closeYangrMsg"></yangr-msg>
	</view>
</template>

<script>
	import yangrMsg from "@/components/yangr-msg/yangr-msg.vue"
	export default {
		components: {yangrMsg},
		data() {
			return {
				title: '小程序测试标题',
				info: '小程序测试提示信息小程序测试提示信息小程序测试提示信息小程序',
				yangrMsgShow: false,
			}
		},
		onLoad() {

		},
		methods: {
			closeYangrMsg(){
				this.yangrMsgShow = false;
			}
		}
	}
</script>

<style>
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}

	.logo {
		height: 200rpx;
		width: 200rpx;
		margin-top: 200rpx;
		margin-left: auto;
		margin-right: auto;
		margin-bottom: 50rpx;
	}

	.text-area {
		display: flex;
		justify-content: center;
	}

	.title {
		font-size: 36rpx;
		color: #8f8f94;
	}
</style>
