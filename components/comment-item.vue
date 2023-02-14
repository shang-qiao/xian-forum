<template>
	<view class="comment">
		<view class="user-info">
			<view class="user">
				<u-avatar class="test" :customStyle="{ 'margin-right': '10px' }" :src="avatarSrc"></u-avatar>
				<u--text text="孤烟暮蝉"></u--text>
			</view>
			<view class="floor-number">
				<u--text color="#808080" text="1楼"></u--text>
			</view>
		</view>
		<view class="content">
			<u--text text="这是评论的内容"></u--text>
		</view>
		<view class="time">
			<u--text color="#808080" size="12px" text="1小时前"></u--text>
		</view>
	</view>
</template>

<script>
	export default {
		name: "comment-item",
		data() {
			return {
				avatarSrc: 'https://cdn.uviewui.com/uview/album/1.jpg'
			};
		}
	}
</script>

<style scoped lang="scss">
	.comment {

		.user-info {
			display: flex;
			justify-content: space-between;
			align-items: center;

			.user {
				display: flex;
				align-items: center;

				// /deep/ .u-avatar {
				// 	margin-right: 10px !important;
				// }
			}
		}

		.content {
			margin: 20px 0;
		}

		.time {
			margin-bottom: 10px;
		}
	}
</style>
