<template>
    <div>
        <h3>Usuario</h3>    
        <hr>
        <router-view name= "menu"></router-view>
        <transition mode="out-in"
            class="slide"
            leave-active-class="animated rollOut">
            <router-view/>
        </transition>
        <router-view name="menuInferior"></router-view>
        <button sucesso @click="irParaInicio">Voltar</button>
    </div>
</template>

<script>
    export default {
        methods: {
            irParaInicio () {
                //this.$router.push('/')
                //this.$router.push({path: '/'})
                this.$router.push({name : 'home'})
            }
        }
    }
</script>

<style lang="scss" scoped>


</style>