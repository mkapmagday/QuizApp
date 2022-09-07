/* eslint-disable */
<template>
<head>
        <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.0/dist/css/bootstrap.min.css" integrity="sha384-gH2yIJqKdNHPEq0n4Mqa/HGKIhSkIHeL5AyhkYV8i59U5AR6csBvApHHNl/vI1Bx" crossorigin="anonymous">
</head>
    <div id="app" style="margin-left: 20%; margin-top: 50px; ">
            <p> Enter Text : <input type="text" name="text" v-model="text"></p>
            <br/>
            <br/>
        <table>
             <tr>
                <th><button @click="getVowelCount()" class="btn btn-success">Get Vowel Count</button></th>
                <th>&nbsp;</th> 
                <th><button @click="getConsCount()" class="btn btn-success">Get Constant Count</button></th>
                <th>&nbsp;</th> 
                <th><button @click="getNumCount()" class="btn btn-success">Get Num Count</button></th>
                <th>&nbsp;</th>     
                <th><button @click="getConvert()" class="btn btn-success">Convert</button></th>
                <th>&nbsp;</th> 
                <th><button @click="clear()" class="btn btn-success">Clear</button></th>
            </tr>
        </table>
           
                
            <br/>
            <br/>

            <p>Vowel Count : {{ vowelCount }}</p>
            <br/>
            <p>Consonant Count: {{ consCount }}</p>
            <br/>
            <p>Number Count: {{ numCount }}</p>
            <br/>
            <p>Conver Vowels to * : {{ convert }}</p>

</div>
</template>

<script>
export default {
    data(){
        return{
            text: "",
            vowelCount:0,
            consCount:0,    
		    numCount:0,
            convert:"",
        }
    },
    methods:{
        getVowelCount:function(){
            this.vowelCount = this.text.match(/[aeiou]/gi).length
    },
    getConsCount:function(){
            this.consCount = this.text.match(/[bcdfghjklmnpqrstvwxys]/gi).length

    },
    getNumCount:function(){
            this.numCount = this.text.match(/[0-9]/ig).length
    },
    getConvert:function(){
            this.convert = this.text.replace(/[aeiou]/gi,'*')
    },
    clear:function(){
   					this.vowelCount = 0;
            this.consCount = 0;
            this.convert = "";
            this.numCount = 0;
            this.text = "";
    }
    }

}
</script>

<style scoped>

button{
    width: 175px;
}
table,tr,th {
  border: 0px solid;
  border-radius: 25px;
}
#id{
  margin: auto;
  width: 50%;
  border: 3px solid green;
  padding: 10px;}

</style>
