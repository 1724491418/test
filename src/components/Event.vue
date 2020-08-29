<template>
    <div>
        name: {{ name|| "--" }}
        <br/>
        <input :value="name" @change="handleChange">
        <br/>
        <br/>
        <div @click = "handleDivClick">
            <button @click="handleClick">重置成功</button>
            <button @click.stop="handleClick">重置失败</button>
        </div>


    </div>
</template>
<script>
export default{
    name: "EventDemo",
    props:{
        name:String
    },
    methods:{
        handleChange(e){
            console.log('i')
            console.log(e.target.value)
            this.$emit("change",e.target.value);
        },
        handleDivClick(){
            console.log('1')
            this.$emit("change","");
        },
        handleClick(){
            //都会失败
        }
    }
}
</script>
<style>


</style>