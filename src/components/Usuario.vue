<template>
    <div class="container">
        <h1>Componente Usuário</h1>
        <p>{{ name }}</p>
        <button @click="change">Alterar nome</button>
        <hr />
        <div class="componentes">
            <app-usuario-info
                :p_name="name"
                @renewEvent="changeRenew($event)"
                :restartFn="restartName"
            />
            <app-usuario-editar />
        </div>
    </div>
</template>

<script>
import AppUsuarioInfo from './UsuarioInfo';
import AppUsuarioEditar from './UsuarioEditar';

export default {
    data() {
        return {
            name: 'Tiago',
        };
    },
    methods: {
        change() {
            this.name = 'Marcos';
        },
        changeRenew(e) {
            this.name = e;
        },
        restartName(name) {
            this.name = name;
        },
    },
    components: { AppUsuarioInfo, AppUsuarioEditar },
};
</script>

<style scoped>
.container {
    background-color: #27363b;
    color: #fff;
    padding: 10px;
}

.container hr {
    margin: 20px 10px;
}

.componentes {
    display: flex;
}

.componentes > * {
    margin: 10px;
}
</style>
