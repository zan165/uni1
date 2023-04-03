<template>
	<view class="content">
	<view class="content1">
		<image class="logo" src="/static/contanor1.png"></image>
	</view>
	<view class="content2">
		<image class="titleimg" src="/static//01.png"></image>
	</view>
	<view class="content3">
		<image class="backimg" src="../../static/中间空白.png"></image>
		<view class="textview">
				<text class="fontsstyle1">{{text1}}</text>
		</view>
	</view>
	
	<view class="content2">	
		<image class="titleimg" src="/static//02.png"></image>
	</view>
	<view class="content3">
		<image class="backimg" src="../../static/中间空白.png"></image>
		<view class="activeTime">
				<text>{{activeTime}}</text>
				<view class="fontlable">{{label01}}</view>
				<view class="threeButtons">
					<button class="flexbuttonitem" type="primary" @click="jumpToSubmit(1)" >{{lb01}}</button>
					<button class="flexbuttonitem" type="primary" @click="jumpToSubmit(2)" >{{lb02}}</button>
					<button class="flexbuttonitem" type="primary" @click="jumpToSubmit(3)"  disabled>{{lb03}}</button>
					
				</view>
				<view >
					<text>{{activeinfo}}</text>
				</view>
		</view>
		
	</view>
	
	<view class="content3">
		<image class="backimg" src="../../static/中间空白.png"></image>
		<view class="activeTime">
				<text>{{ctciveEndTime}}</text>
				<view class="fontlable">{{label02}}</view>
				<view class="threeButtons">
					<button class="flexbuttonitem" type="primary" @click="jumpToSubmit(4)" disabled>{{lastlb01}}</button>
					<button class="flexbuttonitem" type="primary" @click="jumpToSubmit(5)" disabled>{{lastlb02}}</button>
					<button class="flexbuttonitem" type="primary" @click="jumpToSubmit(6)" disabled>{{lastlb03}}</button>
					
				</view>
				<view class="activeinfo">
					<text>{{lastactiveinfo}}</text>
					
				</view>
				
		</view>
		
	</view>
	
	<view class="content5">
		<image class="backimg" src="../../static/中间空白.png"></image>
		<view class="outview">
				<view class="fontlable">{{label03}}</view>
				<view class="outViewInfo">
					<text>{{outViewInfo}}</text>
				</view>
				<button type="primary" @click="jumpToSubmit(0)" >查看名单</button>
		</view>
		
	</view>
	
	
	<view class="content2">
		<image class="titleimg" src="/static//03.png"></image>
	</view>
	
	<view class="content4">
		<image class="backimg" src="../../static/中间空白.png"></image>
		<view class="textview">
				<text class="fontsstyle1">{{text4}}</text>
		</view>
	</view>
	
	</view>
</template>
<script>
	export default {
		data() {
			return {
				title: 'Hello',
				title1:'活动政策',
				text1:'1、Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean euismod bibendum laoreet. Proin 。',
				text2:'2、Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean euismod bibendum laoreet. Proin 。',
				text3:'',
				text4:"1、Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean euismod bibendum laoreet. Proin 。2、Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean euismod bibendum laoreet. Proin 。3、Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean euismod bibendum laoreet. Proin4、Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean euismod bibendum laoreet. Proin 。5、Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean euismod bibendum laoreet. Proin。6、Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean euismod bibendum laoreet. Proin。7、Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean euismod bibendum laoreet. Proin。8、Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean euismod bibendum laoreet. Proin。",
				activeTime:'2023年3月16日-2023年4月16日',
				ctciveEndTime:'截止日期2023年4月6日',
				activeinfo:'初审报名3600人 通过100人',
				outViewInfo:'初审通过1000人  终审通过500人',
				lastactiveinfo:'终审报名3600人 通过100人',
				label01:'报名初审',
				lb01:'提交资料',
				lb02:'初审进度',
				lb03:'初审结果',
				label02:'资格终审',
				lastlb01:'提交资料',
				lastlb02:'终审进度',
				lastlb03:'终审结果',
				label03:'名单公示',
				label04:'注意事项',
				
			}
		},
		onLoad() {

		},
		methods: {
			jumpToSubmit(para){
				console.log("clicked  button1",para)
				let urlpath=["../outview/outview","/pages/submitview/submitview","/pages/submitview/submitview","","","",""];
				console.log("clicked  button1",urlpath[para])
				if(urlpath[para]=="")urlpath[para]="../404/404";
				uni.navigateTo({
					url:urlpath[para]
				})
			}
		}
	}
</script>

<style>
	.content{
		display: flex;
		flex-direction: column;
		width: 100%;
		
	}
	.content1 {
		display: flex;
		width: 100%;
		height: 606rpx;
		background-color: #d6e5ff;
	}
	
	.logo {
		height: 600rpx;
		width: 700rpx;
		margin-top: 1rpx;
		margin-left: auto;
		margin-right: auto;
		margin-bottom: 5rpx;
	}
	
	.titleimg{
		width: 100%;
		height: 95rpx;
	}
	.backimg{
		position: absolute;
		width: 100%;
		height: 100%;
	}

	.content2{
		flex-direction: column;
		font-style: normal;
		display: flex;
		background-color: #d6e5ff;
		height:80rpx;
		
	}
	
	.textview{
		position: absolute;
		display: flex;
		left: 30rpx;
		top: 20rpx;
	}
	.activeTime{
		display: flex;
		position: absolute;
		margin-left: 10%;
		margin-right: 10%;
		justify-content: center;
		align-items: center;
		font-size: 40;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		align-items: center;
	}
	.content3{
		position: relative;
		background-color: #d6e5ff;
		width: 100%;
		height: 150px;
		border: #d6e5ff;
		align-items: center;
	}
	.threeButtons{
		display: flex;
		flex-direction: row;
		justify-content: space-evenly;
	}
	.flexbuttonitem{
		margin: 5px;
		background-color: blue;
	}



	.text-area {
		display: flex;
		justify-content: center;
	}

	.title {
		font-size: 36rpx;
		color: #d6e5ff;
	}
	.title1{
		font-size: 50rpx;
		color: #d6e5ff;
		margin-left: 25rpx;
		text-shadow: #ffffff;
	}
	.title2{
		font-size: 40rpx;
		color: #000000;
		text-shadow: #ffffff;
		text-align: center;
		margin:auto;
	}
	.fontsstyle1{
		width: 85%;
		margin-left: 7.5%;
		margin-right: 7.5%;
		float: left;
		text-align: justify;
		user-select: ;
	}
	.fontlable{
		margin: 10rpx 10rpx 0 0;
		border-radius: 2px;
		font-size: 45rpx;
	}	
	.content4{
		position: relative;
		background-color: #d6e5ff;
		width: 100%;
		height: 600px;
		border: #d6e5ff;
		align-items: center;
	}
	.content5{
		position: relative;
		background-color: #d6e5ff;
		width: 100%;
		height: 160px;
		border: #d6e5ff;
		align-items: center;
	}
	.outview{
		display: flex;
		position: absolute;
		margin-left: 10%;
		margin-right: 10%;
		justify-content: center;
		align-items: center;
		font-size: 40;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		align-items: center;
		width: 80%;
	}
	
	.outViewInfo{
		margin-top: 30rpx;
		margin-bottom: 30rpx;
	}
	
</style>
