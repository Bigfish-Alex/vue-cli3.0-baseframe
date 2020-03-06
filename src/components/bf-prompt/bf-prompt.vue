<template>
    <div class="bf-prompt">
        <button :num="num" @click="saySomething">Click{{num}}</button>
    </div>
</template>

<script>
export default {
    data(){
        return{

        }
    },
    props:{
        num:{
            type:Number,
            default:0
        }
    },
    methods:{
        saySomething(){
            this.$emit('patherSay',1)
        }
    }
}
</script>