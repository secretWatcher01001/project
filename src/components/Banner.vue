<template> 
    <div id="banner">
        <h1>Somos todos seus fans</h1>
    </div>
</template>

<script>
    export default {
        name: "Banner"
    }
</script>

<style scoped>
    #banner {
        background-image: url('/home/danielrubioklein/project/public/img/pamela.jpg');
        background-repeat: no-repeat;
        background-size: cover;
        background-position: center;
        height: 83vh;
        margin: 0px;
        padding: 0px;
        display: flex;
        align-items: center;
    }
    #banner h1 {
        font-size: 0.9em;
        color: rgb(255, 255, 255);
        width: 23vh;
        padding: 10px;
        background-color: rgba(37, 37, 37, 0.884);
        border-top-right-radius: 20px;
        border-bottom-right-radius: 20px;
    }
</style>