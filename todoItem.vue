<template>
    <view class="container">
        <switch :value="item.status" :on-value-change="handleChange"></switch>
        <text class="text-primary">
            {{item.id}}. {{item.text}}
        </text>
    </view>
</template>
<script>
export default {
    
    props: {
        item:{
            Type: Object,
            status: false,
            text: "",
        }
    },
    methods: {
        handleChange: function(){
            this.item.status = !item.status 
        }
    },
};
</script>
<style>
    .container{
        flex-direction: row;
    }
    .text-primary{
        color: #dfdfdf;
    }
</style>
