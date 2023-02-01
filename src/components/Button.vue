<template>
    <button v-on:click="Click()" :style="{ background:color }" class="btn">{{text }}</button>
</template>

<script>



    export default{
        name:'Button-component',
        props:{
            text: String,
            color: String,
        },
        methods:{
            Click(){
                console.log('click');
            }
        }
    }
</script>