<template> 
    <div>
        <h1>Sua Opinião Sobre a Honey</h1>
        <form id="form" @submit="postLikes">
            <div class="input-container">
                <label for="name">Nome</label>
                <input type="text" id="name" name="name" v-model="Name" placeholder="Seu nome">
            </div>
            <div class="input-container">
                <label for="like">Você gosta da Honey?</label>
                <select name="like" id="like" v-model="selectedLikebility" >
                    <option v-for="likebility in Likebilitys" :key="likebility.id" :value="likebility">
                    {{ likebility.likebility }}
                    </option>
                </select>

            </div>
            <div class="input-container">
                <label for="opinion">Sua opinião</label>
                <input type="text" id="opinion" name="opinon" v-model="Opinion" placeholder="Sua opinião">
            </div>
            <input type="submit" class="submit-button" value="Enviar Opinião">
        </form>
    </div>
</template>

<script>
    export default {
        name: "Form",
        data() {
            return {
                Likebilitys: null,
                Name: null,
                Likebility: null,
                Likebility_score: null,
                Opinion: null
            }
        },

        methods: {
            async getLikes() {

                const req = await fetch("http://localhost:3000/endpoint");
                const data = await req.json();

                this.Likebilitys = data.likes

            },

            async postLikes(e) {
                e.preventDefault();

                const data = {
                    Name: this.Name,
                    Likebility: this.selectedLikebility.likebility,
                    Likebility_score: this.selectedLikebility.likebility_score,
                    Opinion: this.Opinion
                }

            const dataJson = JSON.stringify(data);
            const req = await fetch("http://localhost:3000/Opinions", {
                method: "POST",
                headers: {"Content-Type": "application/json"},
                body: dataJson
            });

            const res = await req.json();

            console.log(res)

            }
        },

        mounted() {
            this.getLikes();
        }
    }
</script>

<style scoped>


    h1 {
        font-size: 1.4em;
        margin: 45px;
    }

    #form {
        max-width: 400px;
        height: 700px;
        margin: 0 auto;
        display: flex;
        flex-direction: column;
    }

    .input-container {
        display: flex;
        flex-direction: column;
    }

    label {
        margin-bottom: 20px;
        margin-top: 20px;
        font-weight: bold;
        font-size: 0.9em;
    }

    input,select {
        font-family: Arial, Helvetica, sans-serif;
        height: 30px;
        border-radius: 5px;
        border: solid black 1px;
        padding-left: 15px;
    }

    #opinion {
        height: 300px;
        font-family: Arial, Helvetica, sans-serif;

        
    }

    .submit-button {
        text-align: center;
        margin-top: 40px;
        align-self: center;
        width: 300px;
        height: 40px;
        border: none;
        margin-bottom: 40px;
        border-radius: 15px;
        background-color: rgb(105, 56, 0);
        font-size: 0.9em;
        color: white;
        font-weight: bold;
        transition: 0.5s;
    }

    .submit-button:hover {
        width: 350px;
        height: 50px;
        font-size: 0.8em;
    }

</style>