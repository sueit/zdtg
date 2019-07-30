<template>
<view>
    <view class="list-cell" hover-class="uni-list-cell-hover" @click="bindClick">
        <view class="media-list" v-if="options.title">

            <view class="uni-list">
                <view class="uni-list-cell" hover-class="uni-list-cell-hover">
                    <view class="uni-media-list">
                        <view class="uni-media-list-logo">
                            <image :src="options.image_url"></image>
                        </view>
                        <view class="uni-media-list-body">
                            <view class="uni-media-list-text-top">{{options.title}}</view>
                            <view class="uni-media-list-text-bottom uni-ellipsis">{{options.title}}</view>
                        </view>
                    </view>
                </view>
            </view>
						<view class="uni-triplex-row">
								<view class="uni-triplex-left">
										<text class="uni-title uni-ellipsis">列表主标题</text>
										<text class="uni-text">列表副标题</text>
										<text class="uni-text-small uni-ellipsis">列表内容文字,列表内容文字,列表内容文字,列表内容文字,列表内容文字,列表内容文字</text>
								</view>
								<view class="uni-triplex-right">
										<text class="uni-h5">12:15</text>
								</view>
						</view>

      			<view class="progress-box">
      				<progress percent="80" show-info activeColor="#10AEFF" backgroundColor="#000" active stroke-width="6" />
      			</view>
        </view>
    </view>
</view>
</template>

<script>
export default {
    props: {
        options: {
            type: Object,
            default: function(e) {
                return {}
            }
        }
    },
    methods: {
        close(e) {
            this.$emit('close');
        },
        bindClick() {
            this.$emit('click');
        }
    }
}
</script>

<style>
.title {
    padding: 20upx;
}
</style>
