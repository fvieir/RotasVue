<template>
    <div>
        <h3>Usuario Detalhe</h3>
        <hr>
        <p><strong>Código</strong>{{id}}</p>
        <router-link tag="button" primario
            :to="{name: 'editarUsuario', params: {id: $route.params.id},
                query: {completo: true, lingua: 'pt-br'},
                hash: '#rodape'}"
            @click.native="getHttp">
            Editar
        </router-link>
    </div>
</template>

<script>
    export default {
         props:['id'],
        //2º forma de pegar o id e atualiza a cada alteração de rota. Com props é mais simples implementação
        data () {
            return {
                data : ''
            }
        },
        // watch: {
        //     $route(to, from ) {
        //         // eslint-disable-next-line no-console
        //         console.log(to, from )
        //         this.id = to.params.id
        //     }
        // },
        methods: {
            getHttp () {
                this.$http.get('usuario.json' , {
                    nome: 'Fabricio',
                    email: 'fcvieira'
                }).then(res => {
                    // eslint-disable-next-line no-console
                    console.log(res)
                    this.data = res.data
                })
            }
        },
    }
</script>

<style lang="scss" scoped>

</style>