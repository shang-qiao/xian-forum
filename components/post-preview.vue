<template>
	<view class="post_preview">
		<view class="container" @click="handleClick">
			<view class="title">
				<u--text :lines="lines" :text="title"></u--text>
			</view>
			<view v-if="imageList.length >= 3" class="image_list">
				<u-image width="110" height="75" radius="4" v-for="imageUrl in imageList" :src="imageUrl">
				</u-image>
			</view>
			<view class="post_info">
				<view class="username">{{ '西安城事' }}</view>
				<view class="page_view">{{ '999阅读' }}</view>
				<view class="post_time">{{ '昨天 22:44' }}</view>
			</view>
		</view>
		<view v-if="imageList.length < 3 && imageList.length > 0" class="single_img image_list">
			<u-image width="120" height="80" radius="4" :src="imageList[0]">
			</u-image>
		</view>
	</view>
</template>

<script>
	export default {
		name: "post-preview",
		props: {
			title: {
				type: String,
				default: 'xxxx'
			},
			imageList: {
				type: Array,
				default: []
			}
		},
		data() {
			return {

			};
		},
		computed: {
			lines: function() {
				return this.imageList.length >= 3 ? 2 : 3;
			}
		},
		methods: {
			handleClick() {
				console.log('click');
				uni.navigateTo({
					url: '/pages/post-details'
				})
			}
		}
	}
</script>

<style scoped lang="scss">
	.post_preview {
		display: flex;

		.container {
			width: 100%;
			display: flex;
			flex-direction: column;
			justify-content: space-between;

			.title {
				padding: 0 2%;
				margin-bottom: 10px;
			}

			.image_list {
				width: 96%;
				margin-left: 2%;
				display: flex;
				justify-content: space-between;
			}

			.post_info {
				padding: 0 2%;
				font-size: 10px;
				margin-top: 10px;
				color: #ccc;

				&::after {
					content: '';
					clear: both;
					display: block;

				}

				.username {
					margin-right: 4px;
				}

				.username,
				.page_view {
					float: left;
				}

				.post_time {
					float: right;
				}
			}
		}

	}

	.single_img {
		padding: 0 2%;
	}
</style>
