<template>
	<view class="content">
		<view class="swiper">
			<u-swiper :list="list1" previousMargin="20" nextMargin="20" circular radius="5" bgColor="#ffffff">
			</u-swiper>
		</view>
		<!-- <view class="icon"></view> -->
		<view class="nav">
			<view class="nav-item">
				<view class="icon xian-story"></view>
				<view class="label">西安城事</view>
			</view>
			<view class="nav-item">
				<view class="icon house-rent"></view>
				<view class="label">房屋租赁</view>
			</view>
			<view class="nav-item">
				<view class="icon lighthouse"></view>
				<view class="label">曝光台</view>
			</view>
			<view class="nav-item">
				<view class="icon marriage-seeking"></view>
				<view class="label">征婚交友</view>
			</view>
			<view class="nav-item">
				<view class="icon secondhand-market"></view>
				<view class="label">二手市场</view>
			</view>
		</view>
		<!-- <view class="separator"></view> -->
		<u-line length="96%" margin="10px"></u-line>
		<post-preview title="怎么学习微信小程序怎么学习微信小程序怎么学习微信小程序怎么学习微信小程序怎么学习微信小程序" :imageList="images1"></post-preview>
		<!-- <view class="separator"></view> -->
		<u-line length="96%" margin="10px"></u-line>
		<post-preview title="怎么学习微信小程序怎么学习微信小程序怎么学习微信小程序怎么学习微信小程序怎么学习微信小程序" :imageList="images2"></post-preview>
		<!-- <view class="separator"></view> -->
		<u-line length="96%" margin="10px"></u-line>
		<post-preview title="怎么学习微信小程序怎么学习微信小程序怎么学习微信小程序怎么学习微信小程序怎么学习微信小程序"></post-preview>
		<u-line length="96%" margin="10px"></u-line>
	</view>
</template>

<script>
	import PostPreview from '../../components/post-preview.vue';
	export default {
		components: {
			'post-preview': PostPreview
		},
		data() {
			return {
				list1: [
					'https://cdn.uviewui.com/uview/swiper/swiper1.png',
					'https://cdn.uviewui.com/uview/swiper/swiper2.png',
					'https://cdn.uviewui.com/uview/swiper/swiper3.png',
				],
				images1: [
					'https://cdn.uviewui.com/uview/album/1.jpg',
					'https://cdn.uviewui.com/uview/album/2.jpg',
					'https://cdn.uviewui.com/uview/album/3.jpg'
				],
				images2: [
					'https://cdn.uviewui.com/uview/album/1.jpg'
				]
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style scoped lang="scss">
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: space-between;

		.swiper {
			/* height: 100%; */
			width: 100%;
		}

		.nav {
			width: 96%;
			margin: 20px 0 15px;
			;
			display: flex;
			align-items: center;
			justify-content: space-between;

			.nav-item {
				// text-align: center;
				display: flex;
				flex-direction: column;
				align-items: center;

				.icon {
					/* font-size: 40px; */
					/* margin: 0 5px; */
					width: 40px;
					height: 40px;
					/* border-radius: 30px; */
					color: #fff;
					background-size: 40px 40px;
					background-repeat: no-repeat;
				}

				.xian-story {
					background-image: url('../../static/images/xian_story.png');
				}

				.lighthouse {
					background-image: url('../../static/images/lighthouse.png');
				}

				.marriage-seeking {
					background-image: url('../../static/images/marriage_seeking.png');
				}

				.house-rent {
					background-image: url('../../static/images/house_rent.png');
				}

				.secondhand-market {
					background-image: url('../../static/images/secondhand_market.png');
				}

				.label {
					font-size: 12px;
					padding-top: 4px;
				}

			}
		}

		.separator {
			width: 96%;
			margin: 10px 0;
			// height: 1px;
			border-top: 1px solid #ccc;
		}

		post-preview {
			width: 100%;
		}
	}
</style>
