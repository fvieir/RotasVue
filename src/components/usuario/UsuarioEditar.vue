<template>
    <div class="usuario-editar">
        <h3>Editar</h3>
        <hr>
        <p><strong>Código : </strong>{{id}} $router.params.id => {{$route.params.id}}</p>
        <p>Nome Completo : {{$route.query.completo ? 'Sim' : 'Não'}}</p>
        <p>Lingua : {{$route.query.lingua}}</p>
        <p>hash : {{$route.hash}}</p>

        <div id="rodape" style="margin-top: 1000px">
            Footer
        </div>
    </div>
</template>

<script>
    export default {
        props: ['id']
    }
</script>

<style lang="scss" scoped>

</style>