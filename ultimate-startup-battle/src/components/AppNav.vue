<template>
    <nav class="nav navbar-default">
        <div class="navbar-header">
            <router-link to="/" class="navvar-brand"> The Ultimate Startup Battle Ground</router-link>
        </div>
    </nav>
    <ul class="nav navbar-nav navnar-right">
        <li>
            <button @click="handleLogout()"type="button" class="btn btn-danger log"name="button">Log Out</button>
            <button @click="handeLogin()"type="button" class="btn btn-info log"name="button">Log In</button>

        </li>

    </ul>
</template>

<script>
import { isLoggedIn, login, logout } from '../../utils/auth';

export default {
  name: 'app-nav',
  methods: {
    handleLogin() {
      login();
    },
    handleLogout() {
      logout();
    },
    isLoggedIn() {
      return isLoggedIn();
    },
  },
};

</script>

<style scoped>
.navbar-right { margin-right: 0px !important}

.log {
  margin: 5px 10px 0 0;
}
</style>
