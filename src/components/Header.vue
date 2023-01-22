<template>
  <header>
    <div class="logo-container">
      <img src="../assets/logo.svg" alt="Logo">
    </div>
    <div class="header-right">
      <div v-if="!loggedIn" @click="loginWithDiscord" class="login-button">Login</div>
      <div v-else class="user-menu">
        <img src="./avatar.png" alt="Avatar">
        <div class="dropdown-content">
          <a href="#">Profile</a>
          <a href="#">Settings</a>
          <a href="#" @click="logout">Logout</a>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  data() {
    return {
      loggedIn: false
    }
  },
  methods: {
    loginWithDiscord() {
      // Redirect to the Discord OAuth2 authorization URL
      window.location.href = 
		  `https://discord.com/oauth2/authorize?client_id=943855772415193118&scope=identify&response_type=token&redirect_uri=https://vue.subsidised.repl.co/`
    }
  }
}
</script>

<style>
header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 20px;
    background-color: #1e1e1e; /* dark gray */
}

.logo-container {
    display: flex;
    align-items: center;
}

.logo-container img {
    height: 50px;
}

.header-right {
    display: flex;
    align-items: center;
}

.login-button {
    padding: 10px 20px;
    border: 2px solid #FF215C; /* white */
    border-radius: 20px;
    color: #fff; /* white text */
    text-decoration: none;
    transition: all 0.2s ease-in-out;
    cursor: pointer;
}

.login-button:hover {
    background-color: #FF215C; /* white */
    color: #fff; /* dark gray text */
}

.user-menu {
    position: relative;
    display: flex;
    align-items: center;
}

.user-menu img {
    height: 50px;
    width: 50px;
    border-radius: 50%;
    margin-right: 10px;
}

.user-menu .dropdown-content {
    display: none;
    position: absolute;
    top: 60px;
    right: 0;
    background-color: #1e1e1e; /* dark gray */
    box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
    z-index: 1;
}

.user-menu:hover .dropdown-content {
    display: block;
}

.user-menu .dropdown-content a {
    color: #fff; /* white text */
    text-decoration: none;
    padding: 12px 16px;
    display: block;
}

.user-menu .dropdown-content a:hover {
    background-color: #fff; /* white */
    color: #1e1e1e; /* dark gray text */
}
</style>
