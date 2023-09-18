<template> 
    <h3>this is home</h3>
</template>
<script>
    export default{
        unmounted(){
            console.log("the Home Component is unmounted")
        },
        activiated (){
            console.log('deactiated About component')
        },
        deactivated(){
            console.log('deactived home component')
        }

    }
</script>