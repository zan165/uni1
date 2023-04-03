<template>
		<view class="content">
			<view class="inputName">
				<view class="title">姓名：{{inputNameValue}}</view>
				<input class="uni-input" @input="onKeyInput" placeholder="姓名"  />
			</view>
			<view class="inputName">
				<view class="title">电话：{{inputNameValue}}</view>
				<input class="uni-input" @input="onKeyInput" placeholder="电话"  />
			</view>
			<view class="inputName">
				<view class="title">性别： </view>
					<radio-group name="radio">
						<label>
							<radio value="radio1" /><text>男</text>
						</label>
						<label>
							<radio value="radio2" /><text>女</text>
						</label>
					</radio-group>
				</view>
			<view class="inputName">
				<view class="title">证件：{{inputNameValue}}</view>
				<input class="uni-input" @input="onKeyInput" placeholder="证件"  />
			</view>
			<view class="inputName">
				<view class="title" style="margin-left: 30%;">车辆信息</view>
			</view>
			<view class="imgInput">
				<view class="imgView">
					<image class="img" src="../../static/grid.png"></image>
					<text>上传购车合同</text>
				</view>
				<view class="imgView">
					<image class="img" src="../../static/grid.png"></image>
					<text>上传购车收据</text>
				</view>
			</view>
			
			<view class="inputButton">
				<button type="primary">提交审核</button>
			</view>
		</view>
		
</template>

<script>
	export default {
			data() {
				return {
				}
			},
			methods: {
				formSubmit: function(e) {
					console.log('form发生了submit事件，携带数据为：' + JSON.stringify(e.detail.value))
					var formdata = e.detail.value
					uni.showModal({
						content: '表单数据内容：' + JSON.stringify(formdata),
						showCancel: false
					});
				},
				formReset: function(e) {
					console.log('清空数据')
				}
			}
		}
</script>

<style>
	.content {
		display: flex;
		flex-direction: column;
		width: 100%;
		background-color: #d6e5ff;
		height: 100%;
	}
	.contentbg{	
		position: static;
		width: 100%;
		height: 100%;
	}
	.inputName{
		margin-left: 10%;
		margin-bottom: 30rpx;
		display: flex;
		flex-direction: row;
		
	}
	.imgView{
		display: flex;
		flex-direction: column;
		width: 96px;
		height: 136px;
		justify-content: center;
		align-items: center;
	}
	.img{
		width: 96px;
		height: 96px;
	}
	.imgInput{
		display: flex;
		justify-content: space-evenly;
	}
	.inputButton{
		margin: 100rpx;
	}
</style>
