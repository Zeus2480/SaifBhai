<template>
    <div class="childCSS">
        <h1>Child Component</h1>
        <h1>{{text}}</h1>
    </div>
</template>
<script>
export default {
    props:['ChildCalling'],
    data() {
        return {
            text: 'Click to change text'
        }
    },
    watch: {
        ChildCalling(newVal) {
            this.changeText(newVal);
        }
    },
    methods: {
        changeText(newVal) {
            this.text =newVal ;
        }

    }
}
</script>
<style scoped>
.childCSS{
    background-color: #42b983;
    padding: 20px;
    color: #fff;
    text-align: center;
}
</style>