<template>
    <div id="cal">
        <form name="calculator" id="calculator">
        <input type="text" id="input" v-model="message" placeholder="copyright by elius">
        <div>
            <input type="button" id="one" value="1" v-on:click="input">
            <input type="button" id="two" value="2" v-on:click="input">
            <input type="button" id="three" value="3" v-on:click="input">
            <input type="button" id="plus" value="+" v-on:click="operator">
        </div>
        <div>
            <input type="button" id="four" value="4" v-on:click="input">
            <input type="button" id="five" value="5" v-on:click="input">
            <input type="button" id="six" value="6" v-on:click="input">
            <input type="button" id="minus" value="-" v-on:click="operator">
        </div>
        <div>
            <input type="button" id="seven" value="7" v-on:click="input">
            <input type="button" id="eight" value="8" v-on:click="input">
            <input type="button" id="nine" value="9" v-on:click="input">
            <input type="button" id="mul" value="*" v-on:click="operator">
        </div>
        <div>
            <input type="button" id="zero" value="0" v-on:click="input">
            <input type="button" id="dot" value="." v-on:click="input">
            <input type="button" id="div" value="/" v-on:click="operator">
            <input type="button" id="mod" value="%" v-on:click="operator">
        </div>
        <div>
            <input type="button" id="result" value="=" v-on:click="results">
            <button type="button" id="c" v-on:click="clear">Clear</button>
        </div>
    </form>
    </div>
</template>
<script>
export default {
    data(){
        return{
            message: '',
        }
    },
    methods:{
        input: function(e) {
            this.message += e.target.value;
      },
        operator: function(e) {
            this.message = this.message+ e.target.value;
        },
        results: function(){
            this.message = eval(this.message);
        },
        clear: function(){
            this.message = '';
        }
    },            
}
</script>
<style scoped>
#cal{
    display: flex;
    justify-content: center;
    margin-top: 20px;
}
div input[type='button'], button {
	width: 50px;
	height: 50px;
    margin: 2px 0;
    background-color: rgb(43, 189, 226);
    box-sizing: border-box;
    border-radius: 10px;
}
#input{
    width: 209px;
    height: 40px;
    background-color: rgb(142, 194, 196);
}
#c,#result{
    width: 104px;
}

</style>

