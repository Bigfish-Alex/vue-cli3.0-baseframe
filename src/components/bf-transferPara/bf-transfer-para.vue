<template>
    <div>
        <button :fatherToSon="fatherToSon" @click="saySomething" class="sonComponents">Click</button>
        <div>{{fatherToSon}}</div>
    </div>
</template>

<script>
export default {
    data(){
        return{

        }
    },
    props:{
        fatherToSon:{
            type:Number,
            default:0
        }
    },
    methods:{
        saySomething(){
            this.$emit('patherSay','A para from son,')
        }
    }
}
</script>

<style scoped lang='scss'>
    .sonComponents{
        width: 84%;
        height: 100px;
        border-radius: 100px;
        background: $color-tiffanyBlue;
        color: #fff;
        margin: 20px auto;   
        border: none; 
    }
    .sonComponents:active{
        background: #999;
    }
</style>