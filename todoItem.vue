<template>
    <view>
        <switch :value="item.status"></switch>
        <text>
            {{item.id}}. {{item.text}}
        </text>
    </view>
</template>
<script>
export default {
    props: {
        item:{
            Type: Object
        }
    }
};
</script>

