<template>
	<view>
		<view>
			<zy-search :is-focus="false" :is-block="true" :show-want="false"></zy-search>	
		</view>
		<view class="search-key">
			<view class="search-key-word" @click="keywords">jugg</view>
			<view class="search-key-word">sk</view>
			<view class="search-key-word">sb</view>
			<view class="search-key-word">spe</view>
			<view class="search-key-word">sf</view>
			<view class="search-key-word">ds</view>
			<view class="search-key-word">axe</view>
			<view class="search-key-word">invoker</view>
			<view class="search-key-word">ts</view>
			<view class="search-key-word">ta</view>
			<view class="search-key-word">tb</view>
			<view class="search-key-word">viper</view>
			<view class="search-key-word">lion</view>
			<view class="search-key-word">lina</view>
		</view>
	</view>
</template>

<script>
	import zySearch from '../../components/zy-search/zy-search.vue'
	export default {
		components: {
			zySearch
		}
	}
	
</script>

<style>
	.search-key{
		display: flex;
		flex-wrap: wrap;
	}
	.search-key-word{
		width: 150upx;
		height: 60upx;
		border: 1px solid #333333;
		border-radius: 30%;
		text-align: center;
		margin: 15upx 15upx;
	}
</style>
