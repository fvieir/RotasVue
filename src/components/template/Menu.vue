<template>
    <nav class="menu">
        <ul>
            <router-link to='/' tag="li" active-class="active" exact>
                <a>Inicio</a></router-link>
            <router-link to="/usuario" tag="li" active-class="active" > 
                <a>Usuario</a></router-link>
        </ul>
    </nav>
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss" scoped>

</style>