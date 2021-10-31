<template>
    <div class = "main">
        <ul>
            <li>
                <div class="s1">
                    <img src="https://img13.360buyimg.com/n7/jfs/t1/206076/3/7056/599223/6145a33bEa3e933fe/c57177e1773e962a.jpg" alt="">
                    <div class="textBox">
                        竞派RTX2060/1660super全新<span class="red">显卡</span>
                        <span class="money">{{showM}}</span>
                    </div>
                    <input type="checkbox" ref="box1" @click="box1">
                </div>
            </li>
            <li>
                <div class="s2">
                    <img src="https://img11.360buyimg.com/n7/jfs/t1/204733/28/8282/157215/61505966E26f0e27b/69574fbba5f9745d.jpg" alt="">
                    <div class="textBox">
                        宏硕 酷睿i7/八核/9400F/<span class="red">台式机</span>
                        <span class="money">{{comM}}</span>
                    </div>
                    <input type="checkbox" ref="box2" @click="box2">
                </div>
            </li>
            <li>
                <div class="s3">
                    <img src="https://img11.360buyimg.com/n7/jfs/t1/210489/22/2982/157415/6156d87bE3be98e1b/8744e00c8cc8bc6f.jpg" alt="">
                    <div class="textBox">
                        男潮流青年圆领长袖T恤<span class="red">男士印花卫</span>
                        <span class="money">{{cloM}}</span>
                    </div>
                    <input type="checkbox" ref="box3" @click="box3">
                </div>
            </li>
            <li>
                <div class="s4">
                    <img src="https://img12.360buyimg.com/n7/jfs/t1/200677/27/9835/314354/61580278E0d5ded2a/edf8abd18515a461.jpg" alt="">
                    <div class="textBox">
                        G-SHOCK GA-110男士<span class="red">电子手表</span>
                        <span class="money">{{watchM}}</span>
                    </div>
                    <input type="checkbox" ref="box4" @click="box4">
                </div>
            </li>
            <li>
                <div class="s5">
                    <img src="https://img14.360buyimg.com/n7/jfs/t1/129344/27/3324/101081/5ecf2f24E1d097390/789fafe9e2841773.jpg" alt="">
                    <div class="textBox">
                        【潮】<span class="red">Nike</span> Air Jordan 
                        <span class="money">{{nikeM}}</span>
                    </div>
                    <input type="checkbox" ref="box5" @click="box5">
                </div>
            </li>
        </ul>
    </div>
</template>

<style scoped>
    img {
        width: 90px;
        height: 100px;
        vertical-align: top;
    }

    .red {
        color: red;
    }

    .money {
        display: inline-block;
        width: 60px;
        height: 30px;
        text-align: center;
        line-height: 30px;
        background-color: #f5f5f5;
        border-radius: 25px;
    }

    .main {
        width: 100%;
        height: 508.1px;
        /* background-color: pink; */
    }

    .s1,.s2,.s3,.s4,.s5 {
        width: 100%;
        height: 100px;
        background-color: #fff;
        border-bottom: 2px solid #f5f5f5;
	transition: 0.3s;
    }

    .s1:hover {
        background-color: #f5f5f5;
    }

    .s2:hover {
        background-color: #f5f5f5;
    }

    .s3:hover {
        background-color: #f5f5f5;
    }

    .s4:hover {
        background-color: #f5f5f5;
    }

    .s5:hover {
        background-color: #f5f5f5;
    }

    .textBox {
        display: inline-block;
        width: 295px;
        height: 100px;
        line-height: 100px;
        /* background-color: pink; */
        font-size: 14px;
        border-left: 2px solid #f5f5f5;
        margin-left: 5px;
    } 
</style>

<script>
import bus from '../eventBus.js'

export default{
    data:function(){
        return {
            showM: 3499,
            comM: 1598,
            cloM: 149,
            watchM: 273,
            nikeM: 3049
        }
    },
    methods:{
        box1:function(){
            if(this.$refs.box1.checked == true){
                bus.$emit('share',this.showM)
            }else{
                bus.$emit('share',-this.showM)
            }
        },
        box2:function(){
            if(this.$refs.box2.checked == true){
                bus.$emit('share',this.comM)
            }else{
                bus.$emit('share',-this.comM)
            }
        },
        box3:function(){
            if(this.$refs.box3.checked == true){
                bus.$emit('share',this.cloM)
            }else{
                bus.$emit('share',-this.cloM)
            }
        },
        box4:function(){
            if(this.$refs.box4.checked == true){
                bus.$emit('share',this.watchM)
            }else{
                bus.$emit('share',-this.watchM)
            }
        },
        box5:function(){
            if(this.$refs.box5.checked == true){
                bus.$emit('share',this.nikeM)
            }else{
                bus.$emit('share',-this.nikeM)
            }
        }
    }
}
</script>