<template>
    <div>
        <Slider :cname="$style.slider" :items="items"/>
        <div :class="$style.list">
            <div :class="$style.item" v-for="item in enters" :key="item.img">
                <router-link :to="{name:item.href}">
                    <img :src="item.img" :alt="item.title">
                    <span>{{item.title}}</span>
                </router-link>
            </div>
        </div>
    </div>
</template>

<script>
import Slider from '../components/slider'
export default {
    components:{
        Slider
    },
    data(){
        return{
            items:[
                {
                    href:'home',
                    src:'//img12.360buyimg.com/jrpmobile/jfs/t1/74158/28/9036/59801/5d6cd491E392e16c3/bcdb89bae38b1ff2.jpg?width=750&height=320'
                },
                {
                    href:'home',
                    src:'//img12.360buyimg.com/jrpmobile/jfs/t1/74158/28/9036/59801/5d6cd491E392e16c3/bcdb89bae38b1ff2.jpg?width=750&height=320'
                },
                {
                    href:'home',
                    src:'//img12.360buyimg.com/jrpmobile/jfs/t1/74158/28/9036/59801/5d6cd491E392e16c3/bcdb89bae38b1ff2.jpg?width=750&height=320'
                },
                {
                    href:'home',
                    src:'//img12.360buyimg.com/jrpmobile/jfs/t1/74158/28/9036/59801/5d6cd491E392e16c3/bcdb89bae38b1ff2.jpg?width=750&height=320'
                },
                {
                    href:'home',
                    src:'//img12.360buyimg.com/jrpmobile/jfs/t1/74158/28/9036/59801/5d6cd491E392e16c3/bcdb89bae38b1ff2.jpg?width=750&height=320'
                }
            ],
            enters:[
                {
                    href:'home',
                    img:'//img12.360buyimg.com/jrpmobile/jfs/t3991/64/2521945388/12110/93c0139/58d1e462Ncf294123.png?width=132&amp;height=132',
                    title:'优惠券'
                },
                {
                    href:'home',
                    img:'//img12.360buyimg.com/jrpmobile/jfs/t5590/252/875247023/17343/946aa72c/59224650N0f7ffc92.png?width=132&height=132',
                    title:'领红包'
                },
                {
                    href:'home',
                    img:'//img12.360buyimg.com/jrpmobile/jfs/t4393/329/2180608902/13217/c88c0cec/58ec9dcdN1534e2d7.png?width=132&height=132',
                    title:'抢钢镚'
                },
                {
                    href:'home',
                    img:'//img12.360buyimg.com/jrpmobile/jfs/t1/36242/13/119/12214/5cb06492E0c73a66f/a284f91242e27af1.png?width=90&height=90',
                    title:'领京豆'
                },
                {
                    href:'home',
                    img:'//img12.360buyimg.com/jrpmobile/jfs/t5488/298/1036263348/12073/b4f4de97/590ac8e8Ne9def22e.png?width=135&height=135',
                    title:'白条提款'
                }
            ],
        }
    }
}
</script>

<style lang="scss" module>
    @import '../../css/element.scss';
    .slider{
        margin-top: 120px;
        img{
            width: 100%;
        }
    }
    .list{
        @include list(row);
        background: #fff;
        padding-top: 40px;
        padding-bottom: 20px;
        justify-content: space-around;
        .item{
            text-align: center;
            a{
                text-decoration: none;
                img{
                    display: inline-block;
                    width: 90px;
                    height: 90px;
                }
                span{
                    display: block;
                    text-align: center;
                    font-size: 26px;
                    margin-top: 12px;
                    color: #666;
                }
            }
        }
    }
</style>