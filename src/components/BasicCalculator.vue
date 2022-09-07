<template>

<head>
        <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.0/dist/css/bootstrap.min.css" integrity="sha384-gH2yIJqKdNHPEq0n4Mqa/HGKIhSkIHeL5AyhkYV8i59U5AR6csBvApHHNl/vI1Bx" crossorigin="anonymous">
</head>
        <div id="app" class="center">
                
            <p>Enter number 1: <input type="number" name="number1" v-model="number1"></p>
            <br>
            <p>Enter number 2: <input type="number" name="number2" v-model="number2"></p>
            <br/>
            <p>{{ result }}</p>
            <br>
        <ul>
            <table>
                <tr>
                        <th><button @click="sum()" class="btn btn-success">Sum</button></th>
                        <th> &nbsp;</th>
                        <th><button @click="difference()" class="btn btn-success">Difference</button></th>
                        <th> &nbsp;</th>
                        <th><button @click="product()" class="btn btn-success">Product</button></th>
                        <th> &nbsp;</th>
                        <th><button @click="quotient()" class="btn btn-success">Quotient</button></th>
                        <th> &nbsp;</th>
                        <th><button @click="average()" class="btn btn-success">Average</button></th>
                </tr>

            </table>
                
        </ul>
            
      
        
        
        
</div>
</template>
<script>
export default {
        data(){
                return{
                        number1:0,
                        number2:0,
                        result:0,
                }
        },
        methods:{
                sum:function(){
            this.result="SUM: "+ (parseInt(this.number1) + parseInt(this.number2));
    },
   	difference:function(){
            this.result="DIFFERENCE: "+ (parseInt(this.number1) - parseInt(this.number2));
    
    },
   	product:function(){
            this.result="PRODUCT: "+ (parseInt(this.number1) * parseInt(this.number2));
    
    },
   	quotient:function(){
            this.result="QUOTIENT: "+ (parseInt(this.number1) / parseInt(this.number2));
    
    },
       average:function(){
            this.result="AVERAGE: "+ ((parseInt(this.number1) + parseInt(this.number2)) /2);
        }
}
}
</script>
<style scoped>
table,tr,th {
  border: 0px solid;
  border-radius: 25px;
  
}
div {
  padding-top: 30px;
  flex-wrap: wrap;
  align-content: center;
  margin-left: 30%;
}

</style>