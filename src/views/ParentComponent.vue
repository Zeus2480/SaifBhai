
<template>
    <div>
        <h1>Parent</h1>
        <Child :ChildCalling="ParentText"></Child>
        <button @click="childCalling">Click me</button>
        <input type="text" v-model.trim="inputText">
    </div>
</template>
<script>
/* eslint-disable */
import Child from './ChildComponent.vue'
export default {
    data(){
        return {
            ParentText: 'Click to change text',
            inputText:"",
        }
    
    },
    components:{
        Child
    },
    methods:{
        childCalling(){
            console.log(this.inputText);  
            this.ParentText=this.inputText;
        }
    }
    
}
</script>