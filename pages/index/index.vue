<template>
	<view class="content">
		<view class="swiper">
			<u-swiper :list="list1"></u-swiper>
		</view>
		<!-- <view class="iconfont icon-qinggan"></view> -->
		<view class="nav">
			<view class="nav-item">
				<view class="iconfont icon-qinggan"></view>
				<view class="label">人才招聘</view>
			</view>
			<view class="nav-item">
				<view class="iconfont icon-qinggan"></view>
				<view class="label">西安城事</view>
			</view>
			<view class="nav-item">
				<view class="iconfont icon-qinggan"></view>
				<view class="label">曝光台</view>
			</view>
			<view class="nav-item">
				<view class="iconfont icon-qinggan"></view>
				<view class="label">情感天地</view>
			</view>
			<view class="nav-item">
				<view class="iconfont icon-qinggan"></view>
				<view class="label">征婚交友</view>
			</view>
			<view class="nav-item">
				<view class="iconfont icon-qinggan"></view>
				<view class="label">企业招聘</view>
			</view>
			<view class="nav-item">
				<view class="iconfont icon-qinggan"></view>
				<view class="label">房屋租赁</view>
			</view>
			<view class="nav-item">
				<view class="iconfont icon-qinggan"></view>
				<view class="label">二手市场</view>
			</view>
			<view class="nav-item">
				<view class="iconfont icon-qinggan"></view>
				<view class="label">二手车</view>
			</view>
			<view class="nav-item">
				<view class="iconfont icon-qinggan"></view>
				<view class="label">全部板块</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				list1: [
					'https://cdn.uviewui.com/uview/swiper/swiper1.png',
					'https://cdn.uviewui.com/uview/swiper/swiper2.png',
					'https://cdn.uviewui.com/uview/swiper/swiper3.png',
				]
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style lang="scss">
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: space-between;

		.swiper {
			/* height: 100%; */
			width: 96%;
		}

		.nav {
			margin-top: 20px;
			display: flex;
			justify-content: center;
			align-items: center;
			flex-wrap: wrap;
			height: 180px;

			// .zhaopin {
			// 	background: url('@/static/zhaopin.png') no-repeat;
			// }
			.nav-item {
				text-align: center;

				.iconfont {
					font-size: 50px;
					margin: 0 10px;
					width: 50px;
					height: 50px;
					border-radius: 30px;
					color: #fff;
					background-color: #6ab600;
				}

				.label {
					font-size: 14px;
					padding: 4px 0;
				}

			}
		}
	}
</style>
