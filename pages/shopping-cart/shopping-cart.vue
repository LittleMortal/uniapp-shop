<template>
	<view class="content">
		<view class="main">
			Lorem ipsum dolor sit amet consectetur adipisicing elit. Nulla quae obcaecati assumenda dicta? Nulla blanditiis ut, ea eum expedita, voluptate adipisci commodi earum odit nostrum cupiditate dolorum culpa unde corporis.
			Lorem ipsum dolor sit amet consectetur adipisicing elit. Nulla quae obcaecati assumenda dicta? Nulla blanditiis ut, ea eum expedita, voluptate adipisci commodi earum odit nostrum cupiditate dolorum culpa unde corporis.
			Lorem ipsum dolor sit amet consectetur adipisicing elit. Nulla quae obcaecati assumenda dicta? Nulla blanditiis ut, ea eum expedita, voluptate adipisci commodi earum odit nostrum cupiditate dolorum culpa unde corporis.
			Lorem ipsum dolor sit amet consectetur adipisicing elit. Nulla quae obcaecati assumenda dicta? Nulla blanditiis ut, ea eum expedita, voluptate adipisci commodi earum odit nostrum cupiditate dolorum culpa unde corporis.
			Lorem ipsum dolor sit amet consectetur adipisicing elit. Nulla quae obcaecati assumenda dicta? Nulla blanditiis ut, ea eum expedita, voluptate adipisci commodi earum odit nostrum cupiditate dolorum culpa unde corporis.
			Lorem ipsum dolor sit amet consectetur adipisicing elit. Nulla quae obcaecati assumenda dicta? Nulla blanditiis ut, ea eum expedita, voluptate adipisci commodi earum odit nostrum cupiditate dolorum culpa unde corporis.
			Lorem ipsum dolor sit amet consectetur adipisicing elit. Nulla quae obcaecati assumenda dicta? Nulla blanditiis ut, ea eum expedita, voluptate adipisci commodi earum odit nostrum cupiditate dolorum culpa unde corporis.
			Lorem ipsum dolor sit amet consectetur adipisicing elit. Nulla quae obcaecati assumenda dicta? Nulla blanditiis ut, ea eum expedita, voluptate adipisci commodi earum odit nostrum cupiditate dolorum culpa unde corporis.
		</view>
		<view class="footer" v-if="goodsList.length>0">
			<view class="foo-left">
				<label class="radio"><radio value="r1" @tap="editChecked()" :checked="checked" color="#fd5432"/>全选</label>
			</view>
			<view class="foo-center">
				<view class="count">
					已选{{count}}件
				</view>
				<view class="total">
					合计:999.99
				</view>
			</view>
			<button class="pay-btn">结算</button>
		</view>
	</view>
</template>

<script>
	export default{
		data(){
			return{
				checked:false,
				count:0,
				goodsList:[1,2]
			}
		},
		methods:{
			// 全选按钮,改变状态
			editChecked(){
				this.checked=!this.checked
			}
		}
	}
</script>

<style lang="scss" scoped>
	
	page
	.content{
		height: 100%;
		width: 100%;
		display: flex;
		flex-direction: column;
		justify-content: space-between;
		
	}
	.main{
		flex: 1;
		overflow: hidden;
		overflow-y: scroll;
		background-color: #ccc;
	}
	.footer{
		box-shadow: 4px 4px 4px 4px #ccc;
		height: 100upx;
		width: 100%;
		padding: 0 28.13rpx;
		display: flex;
		justify-content: space-between;
		align-items: center;
		box-sizing: border-box;
		.foo-left{
			width: 20%;
			height: 100%;
			display: flex;
			align-items: center;
			font-size: 26.25rpx;
			.radio{
				font-size: 26.25rpx;
				display: flex;
				align-items: center;
			}
		}
		.foo-center{
			flex: 1;
			overflow: hidden;
			height: 100%;
			display: flex;align-items: center;font-size: 26.25rpx;justify-content: flex-end;padding-right: 15rpx;
		}
		.pay-btn{
			background-color: #fd5432;
			width: 30%;
			color: #fff;
			height: 75rpx;
			font-size: 26.25rpx;
			text-align: center;
			line-height: 75rpx;
			border-radius: 37.5rpx;
		}
	}
</style>