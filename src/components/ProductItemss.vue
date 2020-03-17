<template>


        <div class="itemss">
            <div>
                 <img :src="mada.imageLink" height="100px">     
             </div>
            <div>
                <p> {{ mada.itemName }} </p>
                <small>
                    {{ mada.itemPrice }}
                </small> <br>
                 <b-button href="#" variant="primary">BUY NOW</b-button>
            </div> 

        </div>    
        
        
    
</template>

<script>
export default {
     name: 'ProductItemss',
    props: ["mada"]
    
}
</script>

<style scoped>
.itemss {
     /* background-color: aqua;  */
    width : 30%;
    height: 70%;
    display: inline-block;
    border: 1px solid #ccc;
    border-radius: 5px;
    padding : 10px;
    clear: both;
    margin-top: 10px;
    margin-left: 5px;
}
</style>