<template>
	<view>
			<view class="flex m-3">
					<image src="../../static/20.png" style="height: 85rpx;width: 85rpx;" class="rounded-circle mr-3"></image>
					<view class="flex flex-column">
						<text class="font-weight-bolder">想看会儿海</text>
						<text class="font-sm text-secondary">总帖子10，今日发帖0</text>
					</view>
					<uni-list-item class="showArrow"  showArrow>
						
					</uni-list-item>
		</view>
		<view class="flex  align-center px-3 py-2">
			<view class="flex-1 flex flex-column align-center justify-center" v-for="(item,index) in myData" :key="index" >
				<text class="font-lg font-weight-bold">{{item.num}}</text>
				<text class="font text-muted">{{item.name}}</text>
			</view>
			
		</view>
		<view class="px-3 py-2">
		</view>
		<uni-list-item title="我的优惠券" showExtraIcon></uni-list-item>
		<uni-list-item title="申请团长" showExtraIcon>
			<text slot="icon" class="iconfont uni-icon-person"></text>
		</uni-list-item>
		<uni-list-item title="客服热线" showExtraIcon>
			<text slot="icon" class="iconfont icon-keyboard"></text>
		</uni-list-item>
		
	</view>
</template>

<script>
	import uniListItem from '@/components/uni-list-item/uni-list-item.vue'
	export default {
		components:{
			uniListItem 
		},
		data() {
			return {
				myData:[{
					name:'帖子',
					num:1
				},{
					name:'动态',
					num:1
				},{
					name:'评论',
					num:10
				},{
					name:'粉丝',
					num:1
				}
				]
				
			};
		}
	}
</script>

<style lang="scss">
.showArrow{
	width: 170rpx;
	margin-left: 135rpx;
}
</style>
