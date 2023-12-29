<template>
    <div class="containerBody">
        <HeaderAdmin />

        <h1 class="title">Administração da livraria</h1>

        <div class="container-form">
            <form id="form" @submit.prevent="loginSubmit">
                <div class="container-input">
                    <label for="username">Username:</label>
                    <input type="text" name="username" id="username" v-model="formValues.usuario" required>
                </div>
                <div class="container-input">
                    <label for="password">Password:</label>
                    <input type="password" name="password" id="password" v-model="formValues.senha" required>
                </div>

                <div class="container-submit">
                    <input type="submit" value="Login" name="submit" id="submit">
                </div>
            </form>
        </div>
    </div>
</template>

<script setup>
import { ref } from 'vue';
import { useRouter } from 'vue-router';
import axios from 'axios';
import HeaderAdmin from '../components/HeaderAdmin.vue';

const router = useRouter();

const formValues = ref({
    usuario: '',
    senha: ''
})


async function loginSubmit() {
    let infoFormData = new FormData();

    infoFormData.append('usuario', formValues.value.usuario);
    infoFormData.append('senha', formValues.value.senha);

    const response = await axios.post("http://localhost:80/backend_library/login_admin.php", infoFormData);

    if (response.data === 'Sucesso no login!') {
        router.push('/');
    }
}
</script>

<style scoped>
.containerBody {
    height: 100vh;
}

.title {
    text-align: center;
    margin-top: 20px;
}

.container-form {
    display: flex;
    justify-content: space-evenly;
    align-items: center;
    margin-top: 80px;
}

#form {
    width: 70%;
}

.container-input {
    display: flex;
    flex-direction: column;
    gap: 20px;
}

.container-input > label {
    font-size: 1.5em;
}

#username, #password {
    width: 100%;
    height: 40px;
    padding: 0 0 0 10px;
}

.container-submit {
    margin-top: 10px;
}

.container-submit > input {
    padding: 5px;
    width: 100px;
    background-color: #5687a6;
    border: none;
    border-radius: 3px;
    outline: none;
    color: #FDFDFD;
}
</style>