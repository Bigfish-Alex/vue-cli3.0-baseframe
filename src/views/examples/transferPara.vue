<template>
    <div class="components-list-container">
       <bfPrompt :fatherToSon='num' @patherSay="patherSay"></bfPrompt>
    </div>
</template>

<script>
import bfPrompt from '@/components/bf-transferPara/bf-transfer-para.vue'
export default{
    components:{
        bfPrompt
    },
    data(){
        return{
            num:0
        }
    },
    methods:{
        patherSay(_sonPara){
            this.num++;
            console.log('i am father!'+_sonPara)
        }
    }
}
</script>
<style scoped lang="scss">
.components-list-container{
    font-size:32px;
    ul{
        list-style: none;
        margin: 0;
        padding: 0;
        li{
            height: 100px;
            line-height: 100px;
            border-bottom: 1px solid #f2f2f2;
        }
    }
}
</style>
