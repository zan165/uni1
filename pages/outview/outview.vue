<template>
	<view class="content">
		<view class="awardinfo">
			<text>恭喜您中奖了</text>
		</view>
		<text class="title">领奖说明</text>
		<view class="getAwardInfo">
			<text>
				Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean euismod bibendum laoreet.
			</text>
		</view>
		
		<view class="desc">
			<text class="title02">公示说明</text>
			<scroll-view scroll-y="true" class="scrollAwardList" >
				<view  class="awardInfoItem" style="margin-bottom: 5px;">
					<text class="text01">编号</text>
					<text class="text02">姓名</text>
					<text class="text03">手机</text>
					<text class="text04">价格</text>
				</view>
				<view  class="awardInfoItem" v-for="(item,index) in list" :key="index">
					<text class="text01">{{index}}</text>
					<text class="text02">{{item.name}}</text>
					<text class="text03">{{item.phoneNum}}</text>
					<text class="text04">￥{{item.value}}</text>
				</view> 
			</scroll-view>
			
		</view>
		<view style="height: 200px;"></view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				list:[{name:"胡莉莉",value:3000,phoneNum:130000000000},
				{name:"胡莉莉",value:3000,phoneNum:130000000000},
				{name:"胡莉莉",value:3000,phoneNum:130000000000},
				{name:"胡莉莉",value:3000,phoneNum:130000000000},
				{name:"胡莉莉",value:3000,phoneNum:130000000000}]
			}
		},
		methods: {
			
		}
	}
</script>

<style>
	.content{
		display: flex;
		flex-direction: column;
		background-color: #d6e5ff;
	}
	.awardinfo{
		display: flex;
		width: 100%;
		height: 120px;
		justify-content: center;
		line-height: 120px;
		font-size: 38px;
	}
	.title{
		margin:15px;
		font-size: 28px;
	}
	.getAwardInfo{
		margin: 0 5%;
	}
	.desc{
		display: flex;
		flex-direction: column;
		justify-content: center;
		margin-top: 20px;
	}
	.title02{
		text-align: center;
		font-size: 30px;
		margin-bottom: 15px;
	}
	
	
	.awardInfoItem{
		display: flex;
		flex-direction: row;
		justify-content: space-evenly;
		flex-wrap: wrap;
		text-align: center;
	}
	.text01{
		width: 10%;
	}
	.text02{
		width: 20%;
	}
	.text03{
		width: 40%;
	}
	.text04{
		width: 30%;
	}
	.scrollAwardList{
		height: 100%;
	}
</style>
