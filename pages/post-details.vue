<template>
	<view class="post-details">
		<view class="title">
			<u--text size="18px" text="这是帖子的标题"></u--text>
		</view>
		<view class="post-info">
			<view class="topic">
				<u-tag text="西安城事" size="mini" plain></u-tag>
			</view>
			<view class="views-comments">
				<view class="views">
					<u-icon color="#808080" size="12px" name="eye"></u-icon>
					<u--text color="#808080" size="12px" text="666"></u--text>
				</view>
				<view class="comments">
					<u-icon color="#808080" size="12px" name="chat"></u-icon>
					<u--text color="#808080" size="12px" text="57"></u--text>
				</view>
			</view>
		</view>
		<u-line margin="10px 0"></u-line>
		<view class="user-info">
			<view class="user">
				<u-avatar :src="avatarSrc"></u-avatar>
				<view class="name-time">
					<u--text text="孤烟暮蝉"></u--text>
					<u--text color="#808080" size="12px" text="1小时前"></u--text>
				</view>
			</view>
			<view class="floor-number">
				<u--text text="1楼"></u--text>
			</view>
		</view>
		<view class="descript">
			<u--text text="这是描述"></u--text>
		</view>
		<u-line margin="10px 0"></u-line>
		<view class="comment-title">
			<image class="circle-icon" src="../static/images/circle.png"></image>
			<u--text text="热门评论"></u--text>
		</view>
		<view class="comment-content">
			<comment-item />
			<u-line margin="10px 0"></u-line>
			<comment-item />
			<u-line margin="10px 0"></u-line>
			<comment-item />
		</view>
		<comment-toolbar class="toolbar"></comment-toolbar>
	</view>
</template>

<script>
	import CommentItem from '../components/comment-item.vue';
	import CommentToolbar from '../components/comment-toolbar.vue';
	export default {
		components: {
			'comment-item': CommentItem,
			'comment-toolbar': CommentToolbar
		},
		data() {
			return {
				avatarSrc: 'https://cdn.uviewui.com/uview/album/1.jpg'
			}
		},
		methods: {

		}
	}
</script>

<style scoped lang="scss">
	.post-details {
		padding: 2%;

		.title {}

		.post-info {
			margin: 10px 0;
			display: flex;
			align-items: center;
			justify-content: space-between;
			// clear float
			// &::after {
			// 	content: '';
			// 	clear: both;
			// 	display: block;
			// }

			// .topic {
			// 	float: left;
			// }
			.views-comments {
				display: flex;

				.views,
				.comments {
					// float: right;
					display: flex;
					align-items: center;
				}

				.comments {
					margin-left: 5px;
				}
			}

		}

		.user-info {
			display: flex;
			justify-content: space-between;
			align-items: center;

			.user {
				display: flex;
				align-items: center;

				.name-time {
					display: flex;
					flex-direction: column;
					align-items: flex-start;
					margin-left: 10px;
				}
			}
		}

		.descript {
			margin: 20px 0;
		}

		.comment-title {
			display: flex;
			align-items: center;
			margin: 20px 0;

			.circle-icon {
				width: 12px;
				height: 12px;
				margin-right: 2px;
			}
		}

		.toolbar {
			position: fixed;
			left: 0;
			/* top: 0; */
			bottom: 0;
			width: 100%;
			/* width: 100vw; */
			/* opacity: 1; */
			background-color: #fff;
		}
	}
</style>
