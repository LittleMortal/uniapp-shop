<template>
	<view>
		<!-- 轮播图 -->
		<swiper indicator-dots autoplay :interval="3000" :duration="300" indicator-color="#fff" circular>
			<swiper-item v-for="(item,index) in bannerList" :key="index">
				<view class="swiper-item on">
					{{item.content}}
				</view>
			</swiper-item>
		</swiper>
		<!-- 功能导航 -->
		<view class="nav">
			<view class="username" v-for="item in goodsList" :key="item">
				{{item.username}}
			</view>
		</view>
	</view>
</template>

<script>
	export default{
		data(){
			return{
				bannerList:[
					{content:'内容一'},
					{content:'内容二'},
					{content:'内容三'},
					{content:'内容四'},
				],
				goodsList:[
					{username:'帽子'},
					{username:'衣服'},
					{username:'连衣裙'},
					{username:'衬衫'},
					{username:'T恤'},
					{username:'夹克'},
					{username:'鞋子'},
					{username:'手机'},
					{username:'电脑'},
					{username:'更多...'},
				]
			}
		},
		methods:{
			
		}
	}
</script>

<style lang="scss" scoped>
	.swiper-item{
		height: 100%;
		width: 100%;
	}
	.on{
		height: 100%;
		width: 100%;
		background-color: #ccc;
		font-size: 56.25rpx;
		display: flex;justify-content: center;align-items: center;
	}
	.nav{
		height: 262.52rpx;
		display: flex;
		flex-wrap: wrap;
		justify-content: space-between;
		padding:0 37.5rpx;
		margin-bottom: 46.88rpx;
	}
	.username{
		// border-bottom-color: #ccc;
		background-color: #ccc;
		margin: 37.5rpx 11rpx 0 0;
		height: 90rpx;
		width: 16%;
		border-radius: 50%;
		display: flex;
		justify-content: center;align-items: center;
		font-size: 22.5rpx;
	}

</style>