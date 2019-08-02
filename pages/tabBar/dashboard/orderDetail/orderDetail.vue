<template>
<view class="example">
    <media-list :options="newsitem" @close="close(index1,index2)"></media-list>
    <uni-steps :options="list2" :active="active" direction="column" />
</view>
</template>
<script>
import mediaList from '@/components/tab-nvue/mediaList.vue';
import uniSteps from '@/components/uni-steps/uni-steps.vue'
export default {
    components: {
        mediaList,
        uniSteps
    },
    data() {
        return {
            title: '',
            active: 1,
            list2: [{
                title: '买家下单',
                desc: '2018-11-11'
            }, {
                title: '卖家发货',
                desc: '2018-11-12'
            }, {
                title: '买家签收',
                desc: '2018-11-13'
            }, {
                title: '交易完成',
                desc: '2018-11-14'
            }],
            newsitem: {
                "datetime": "40分钟前",
                "article_type": 0,
                "title": "不锈钢管订购合同1",
                "source": "订单号：000002352356",
                "image_url": "https://img-cdn-qiniu.dcloud.net.cn/uniapp/images/shuijiao.jpg?imageView2/3/w/200/h/100/q/90",
                "comment_count": 0
            },
        }
    },
    onLoad(e) {
        this.title = e.title || '';
    }
}
</script>
<style>
page {
    display: flex;
    flex-direction: column;
    box-sizing: border-box;
    background:linear-gradient(top,rgb(49, 147, 186,1) 1%,rgb(117, 216, 250) 99%);
}
</style>
