<template>
    <div class="tab-bar-item" @click="itemClick">
        <div v-if="!isActive"><slot name='item-icon'></slot></div>  
        <div v-else><slot name='item-icon-active'></slot></div>
        <div :class="{active: isActive}"><slot name='item-text'></slot></div>
      </div>
</template>
<script>
export default {
    name:'TabBarItem',
    props:{
        path:String
    },
    data(){
        return {
            isActive:true
        }
    },
    methods:{
        itemClick(){
            this.$router.replace(this.path);
        }
    }
}
</script>
<style>
.active{color:red;}
</style>