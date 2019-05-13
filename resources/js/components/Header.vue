<template>
    <nav class="navbar" role="navigation" aria-label="main navigation">
        <div class="navbar-brand">

            <router-link class="navbar-item" to="/"><img src="https://bulma.io/images/bulma-logo.png" width="112" height="28"></router-link>
            <a role="button" class="navbar-burger burger" aria-label="menu" aria-expanded="false" data-target="navbarBasicExample">
                <span aria-hidden="true"></span>
                <span aria-hidden="true"></span>
                <span aria-hidden="true"></span>
            </a>
        </div>

        <div id="navbarBasicExample" class="navbar-menu">
            <div class="navbar-start">
                <a class="navbar-item">
                    Home
                </a>


                <a class="navbar-item">
                    Documentation
                </a>



                <div class="navbar-item has-dropdown is-hoverable">
                    <a class="navbar-link">
                        More
                    </a>

                    <div class="navbar-dropdown">
                        <a class="navbar-item">
                            About
                        </a>
                        <a class="navbar-item">
                            Jobs
                        </a>
                        <a class="navbar-item">
                            Contact
                        </a>
                        <hr class="navbar-divider">
                        <a class="navbar-item">
                            Report an issue
                        </a>
                    </div>
                </div>
            </div>

            <div class="navbar-end">
                <div class="navbar-item">
                    <template v-if="!currentUser">
                        <div class="buttons">
                            <router-link to="/login" class="button is-primary">Login</router-link>


                            <router-link to="/register" class="button is-light">Register</router-link>
                        </div>
                    </template>
                    <template v-else>
                        <div class="buttons">

                            <router-link to="/customers" class="nav-link">Customers</router-link>


                            <a  class="navbar-item" href="#" >
                                {{ currentUser.name }} <span class="caret"></span>
                            </a>

                            <div class="dropdown-menu" aria-labelledby="navbarDropdown">
                                <a href="#!" @click.prevent="logout" class="dropdown-item">Logout</a>
                            </div>

                        </div>
                        <a href="#!" @click.prevent="logout" class="navbar-item">Logout</a>
                    </template>
                </div>

            </div>
        </div>
    </nav>

</template>

<script>
    export default {
        name: "Header.vue"
    }
</script>

<style scoped>

</style>
