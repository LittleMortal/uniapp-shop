<template>
	<view>
		<uni-swiper-dot :info="info" :current="current" field="content" :mode="mode">
			<swiper class="swiper-box" @change="change">
				<swiper-item v-for="(item ,index) in info" :key="index">
					<view class="swiper-item">
						{{item.content}}
					</view>
				</swiper-item>
			</swiper>
		</uni-swiper-dot>
	</view>
</template>

<script>
	export default{
		data(){
			return{
				info: [{
					content: '内容 A'
					}, {
						content: '内容 B'
					}, {
						content: '内容 C'
					}],
					current: 0,
					mode: 'round',
			}
		},
		methods:{
			change(e) {
				this.current = e.detail.current;
			}
		}
	}
</script>

<style lang="scss" scoped>
	.swiper-box{
		background-color: hotpink;
	}

</style>