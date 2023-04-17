<template>
    <div class="conteiner">
        <h1 class="text">Not Found</h1>
        <button @click="goToMainPage" class="btn">Wróć na stronę główną</button>
    </div>
</template>
<script>
import { useRouter  } from "vue-router";

export default {
    name: 'NotFound',
    setup(){
        const router = useRouter()
        const goToMainPage = () => {
            router.push({name: 'home'})
        }
        return { router, goToMainPage }
    }
}
</script>
<style scoped>
*{
    font-family: sans-serif;
}

.conteiner{
    display: grid;
    justify-content: center;
}

.text{
    color: #d41111;
    font-size: 25px;
    text-align: center;
}

.btn{
    width: 100%;
    height: 50px;
    border: 1px solid #4d91ff;
    color: #d41111;
    font-size: 18px;
    border-radius: 40px;
    transition: all 0.3s;
}

.btn:hover{
    border: 3px solid #4d91ff;
    box-shadow: 5px 5px 5px #000000;
    cursor: pointer;
}
</style>