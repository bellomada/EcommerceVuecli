<template>
<carousel :per-page= 1 :autoplay= true :autoplayTimeout= 2000 :speed="500" :loop= true :navigationNextLabel="next" :navigationPrevLabel="prev">

    <slide v-for="slidding in carouArray" :key="slidding.id" >
        <img :src="slidding.imageLink" height="300px" width="100%">
        <p> 
            hello
        </p>
    </slide>
</carousel>
    
</template>


<script>
export default {
    data() {
        return {
            carouArray : [
                {
                    id: 1,
                     imageLink: require('../../src/assets/img1.jpg')
                },
                 {
                    id: 2,
                    imageLink: require ('../../src/assets/img3.jpg')
                },
                 {
                    id: 3,
                    imageLink: require ('../../src/assets/img4.jpg')
                },
                 {
                    id: 4,
                    imageLink: require ('../../src/assets/img8.jpg')
                }
            ]

        }
    }
}



</script>