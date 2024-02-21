<template> 
    <div id="nav">
        <div id="img">
            <router-link to="/">
                <img :src="logo" :alt="alt" id="logo">
            </router-link>
        </div>
        <div id="nav-links">
            <router-link to="/socials" >Redes Sociais</router-link>
            <router-link to="/about" >Sobre</router-link>
            <router-link to="/opinion" >Sua Opiniao</router-link>
        </div>
    </div>
</template>

<script>
export default {
    name: "Navbar",
    props: ["logo", "alt"]
}
</script>

<style scoped>
    #nav {
        background-image: linear-gradient(to top,rgb(255, 115, 0), rgb(255, 168, 96));
        color: white;
        font-weight: bold;
        height: 80px;
        width: 100vw;
        display: flex;
        overflow: hidden;
        align-items: center;
        box-shadow: 1px 1px 10px 1px rgba(0, 0, 0, 0.274);
        
    }

    #nav-links {
        display: flex;
        height: 80px;
        width: 65vw;
        justify-content: flex-start;
        align-items: center;

    }

    #img {
        height: 80px;
        width: 30vw
    }


    #nav a {
        font-size: 0.8em;
        color: rgb(0, 0, 0);
        font-weight: bold;
        text-decoration: none;
        transition: 0.3s;
        margin-right: 25px;
    }

    #nav a:hover {
        font-size: 0.97em;
        
    }

    #logo {
        width: 70px;
        height: 80px;
        margin-top: 5px;
        transition: 0.3s;
    }

    #logo:hover {
        width: 75px;
        height: 90px;
    }

</style>