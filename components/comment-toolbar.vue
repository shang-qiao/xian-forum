<template>
	<view class="toolbar-wrapper">
		<view class="content">
			<view class="input-wrapper">
				<u--input shape="circle" placeholder="缺少你的神评" border="surround" fontSize="13px"
					:customStyle="{'height': '12px'}" v-model="value" @focus="handleFocus" @change="change"></u--input>
			</view>
			<view class="thumb-up">
				<u-icon name="thumb-up"></u-icon>
			</view>
			<view class="collect">
				<u-icon name="star"></u-icon>
			</view>
			<view class="share">
				<u-icon name="share"></u-icon>
			</view>
		</view>
		<u-popup :show="show" mode="bottom" duration="0" @close="close" @open="open">
			<view class="popup-wrapper">
				<u-notice-bar :text="text1"></u-notice-bar>
				<u--textarea v-model="value1" height="70" border="none" placeholder="请输入内容"></u--textarea>
				<view class="btn-wrapper">
					<u-button
						:customStyle="{'width': '20px', 'float': 'right', 'margin': '10px 20px'}"
						type="primary" size="small" shape="circle" text="发布">
					</u-button>
				</view>
			</view>
		</u-popup>
	</view>
	</view>
</template>

<style lang="scss" scoped>
	.toolbar-wrapper {
		width: 100%;
		border-top: 1px solid #d6d7d9;

		.content {
			display: flex;
			align-items: center;
			justify-content: space-around;

			.input-wrapper {
				width: 70%;
				padding: 5px 18px;
			}

			.thumb-up {
				width: 10%;
			}

			.collect {
				width: 10%;
			}

			.share {
				width: 10%;
			}
		}

		.popup-wrapper {
			.btn-wrapper {

				// display: flex;
				// justify-content: end;
				//  /deep/	.u-button__text {
				// 	font-size: 14px !important;
				// }
			}
		}
	}
</style>

<script>
	export default {
		name: "comment-toolbar",
		data() {
			return {
				show: false,
				text1: 'uView UI众多组件覆盖开发过程的各个需求，组件功能丰富，多端兼容。让您快速集成，开箱即用',
				value1: ''
			}
		},
		methods: {
			handleFocus() {
				console.log('focus');
				this.show = true;
			},
			open() {
				// console.log('open');
			},
			close() {
				this.show = false
				// console.log('close');
			}
		}
	}
</script>
