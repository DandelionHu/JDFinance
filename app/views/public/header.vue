<template>
    <div :class="$style.header">
        <span :class="$style.left">
            <em>注册</em>&nbsp;|&nbsp;<em>登录</em>
        </span>
        <btn :class="$style.right">App下载</btn>
    </div>
</template>

<script>
import btn from '../components/btn';
export default {
    components:{
        btn
    }
}
</script>

<style lang="scss" module>
    .header{
        color: #666;
        height: 100px;
        line-height: 100px;
        position: fixed;
        top:0;
        left: 0;
        right: 0;
        font-size: 32px;
        background:#fff url(//m.jr.jd.com/spe/qyy/main/images/jr-logo.png) center center no-repeat;
        background-size: auto 50%;
        z-index: 100;
        .left{
            font-size: 28px;
            height: 30px;
            line-height: 30px;
            margin: 17px 0 0 18px;
            em{
                font-style: normal
            }
        }
        .right{
            float: right;
            font-size: 24px;
            border-width: 0px;
            height: 56px;
            line-height: 56px;
            min-width: 120px;
            padding: 0px;
            border-radius: 4px;
            margin: 28px 24px 0 0
        }
    }
</style>