<template>
    <div class="container">
        <div class="row justify-content-center">
            <div class="col-md-8">
                <div class="card">
                    <div class="card-header">Example Component</div>

                    <!--<div class="card-body">-->
                        <!--I'm an example component.{{ welcome }}-->
                    <!--</div>-->
                    <div class="notification">
                        This container is <strong>{{ welcome }}</strong> on desktop.
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "Home.vue",
        computed: {
            welcome(){
                return this.$store.getters.welcome
            }

        }
    }
</script>

<style scoped>

</style>
