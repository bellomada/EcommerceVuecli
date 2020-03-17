<template>
    
    <div>
        <div id="categories">
            <p>
                {{ user.categoryName}}
            </p>
        </div>  

           
        
    </div>
</template>

<script>
export default {
    name: 'ShowMall',
    props: ["user"]
}
</script>

<style scoped>
#categories{
    background-color: aqua;
    width : 100%;
    height: 50px;
    border: 1px solid #ccc;
    border-radius: 5px;
    padding : 10px;
    clear: both;
    margin-top: 10px;
}


</style>