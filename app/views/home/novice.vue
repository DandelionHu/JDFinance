<template>
    <panel title="新手特权" :class="$style.panel">
        <div :class="$style.content">
            <div :class="$style.item">
                <h4>下载App<span :class="$style.red">送888元礼包</span></h4>
                <p :class="$style.gray">新手专享</p>
                <img src="//img12.360buyimg.com/jrpmobile/jfs/t1/1216/39/659/4516/5b923b1cE5943d1c6/dabaf8b842f57eb9.png?width=90&height=90" alt="">
            </div>
            <div :class="$style.item">
                <ul>
                    <li>
                        <img src="//img12.360buyimg.com/jrpmobile/jfs/t1/1216/39/659/4516/5b923b1cE5943d1c6/dabaf8b842f57eb9.png?width=90&height=90" alt="">
                        <h4 :class="$style.red">领128元新手礼包</h4>
                        <p :class="$style.gray">立即开通</p>
                    </li>
                    <li>
                        <img src="//img12.360buyimg.com/jrpmobile/jfs/t1/1216/39/659/4516/5b923b1cE5943d1c6/dabaf8b842f57eb9.png?width=90&height=90" alt="">
                        <h4>打白条<span :class="$style.red">享免息</span></h4>
                        <p :class="$style.gray">立即开通享豪礼</p>
                    </li>
                </ul>
            </div>
        </div>
    </panel>
</template>

<script>
import Panel from '../components/panel'
export default {
    components:{
        Panel
    }
}
</script>

<style lang="scss" module>
    @import '../../css/element.scss';
    .panel{
        @include panel;
        >h4{
            border-bottom: 1px solid #ddd;
        }
        .content{
            @include list(row);
            .item{
                width: 50%;
                box-sizing: border-box;
                &:first-child{
                    padding: 32px 20px;
                    text-align: center;
                    border-right: 1px solid #ddd;
                    img{
                        width: 132px;
                        height: 132px;
                        margin: 20px auto 0;
                    }
                }
                h4{
                    font-size: 26px;
                    line-height: 40px;
                }
                .red{
                    color:#f00;
                }
                .gray{
                    color: #999;
                    font-size: 24px
                }
                p{
                    margin-top: 6px;
                    font-size: 24px;
                }
                ul{
                    width: 100%;
                    li{
                        height: 144px;
                        width: 100%;
                        padding: 32px 28px;
                        box-sizing: border-box;
                        &:first-child{
                            border-bottom: 1px solid #ddd;
                        }
                        img{
                            width: 80px;
                            height: 80px;
                            float: right;
                        }
                        h4{
                            @include nowrap;
                            text-align: left;
                        }
                    }
                }
            }
        }
    }
</style>