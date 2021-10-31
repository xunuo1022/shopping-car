<template>
    <div>
        合计：{{sum}}
    </div>
</template>

<style scoped>
    div {
        width: 100%;
        height: 44px;
        background-color: skyblue;
        line-height: 44px;
        font-size: 20px;
        color: white;
    }
</style>

<script>
import bus from '../eventBus.js'

export default {
    data:function(){
        return {
            sum:0
        }
    },
    created:function(){
        bus.$on('share',(val) => {
            this.sum += val
        })
    }
}
</script>