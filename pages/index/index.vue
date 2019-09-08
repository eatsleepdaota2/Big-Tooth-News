<template>
	<view>
		<swiper class="swiper" indicator-dots="true" :autoplay="true" :interval="3000" :duration="500" >
			<swiper-item>
						<image src="../../static/image/news1.jpg" mode="widthFix"></image>
			</swiper-item>
			<swiper-item>
						<image src="../../static/image/news2.jpg" mode="widthFix"></image>
			</swiper-item>
			<swiper-item>
						<image src="../../static/image/news3.jpg" mode="widthFix"></image>	
			</swiper-item>
			<swiper-item>
						<image src="../../static/image/news4.jpg" mode="widthFix"></image>	
			</swiper-item>
			<swiper-item>
						<image src="../../static/image/news5.jpg" mode="widthFix"></image>	
			</swiper-item>
		</swiper>
		<view>
			<navigator  url="../info/info" class="news-list" v-for="(item,index) in news">
				<image class="news-image" :src="{{item.cover}}" mode="widthFix"></image>
				<view class="news-title">{{item.title}}</view>
			</navigator>	
		</view>
	</view>
</template>

<script>
	var _self;
	export default {
		data() {
			
			return {
				news:[]	
			}
		},
		onLoad:function(){
			_self=this;
			this.getNews();
			
		},

		methods: {
			getNews:function(){
				uni.request({
					url:"https://unidemo.dcloud.net.cn/api/news",
					success:function(res){
						console.log(res)
						_self.news=res.data;
						
					},
					
					
				})
				
			}
					
			}	
	}
</script>

<style>
	.news-image{
		width: 200upx;
		height: 120upx;
		padding: 0;
		margin: 0;
		flex-shrink: 0sss;
		
	}
	.news-list{
		display: flex;
		flex-wrap: nowrap;
		padding: 10upx;
	}
	.news-title{
		width: 100%;
		height: autoplay;
		
		
	}
	
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}
	
</style>
