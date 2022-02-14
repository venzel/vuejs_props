<template>
    <div class="componente">
        <h2>As Informações de Usuário</h2>
        <p>Name: {{ p_name }}</p>
        <button @click="renew">Alterar novamente</button>
        <button @click="restartFn('Diego')">Alterar novamente callback</button>
    </div>
</template>

<script>
export default {
    props: {
        p_name: {
            type: String,
            // require: true,
            default: 'Jose',
        },
        restartFn: Function,
    },
    methods: {
        renew() {
            this.p_name = 'biroliro';

            this.$emit('renewEvent', this.p_name);
        },
    },
};
</script>

<style scoped>
.componente {
    flex: 1;
    background-color: #ec485f;
    color: #fff;
}
</style>
