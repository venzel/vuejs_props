<template>
    <div class="componente">
        <h2>As Informações de Usuário</h2>
        <p>Name: {{ p_name }}</p>
    </div>
</template>

<script>
export default {
    props: ['p_name'],
};
</script>

<style scoped>
.componente {
    flex: 1;
    background-color: #ec485f;
    color: #fff;
}
</style>
