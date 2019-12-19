<template>
	<view class="ray-msg-container">
		<view class="ray-msg-mask"></view>
		<view class="ray-msg-content">
			<view class="ray-msg-icon ${opts.type == 'success' ? '' : 'ray-msg-error'}">
				<text></text>
			</view>
			<view>${opts.title ? opts.title : opts.type == 'success' ? '操作成功' : '操作失败'}</view>
			<view class="${opts.info == '' ? '' : 'fixed-msg-info'}">${opts.info}</view>
			<view class="ray-msg-btn">${opts.btn}</view>
		</view>
	</view>
</template>

<script>
	export default {
		name: "yangr-msg",
		//属性
		props: {
			title: {
				type: String,
				value: "" // title 为空时根据 type ，显示"操作成功"/"操作失败"
			},
			type: {
				type: String, // success or error
				value: "success" // 默认值
			},
			info: {
				type: String,
				value: "" // info 为空时不显示
			},
			btn: {
				type: String,
				value: ""
			},
		},
		//组件生命周期
		created: function(e) {

		},
		methods: {

		}
	}
</script>

<style lang="scss">
	@import './yangr-msg.scss';
</style>
