<template>
  <div id="app">
    <NavBar />
    <router-view></router-view>
  </div>
</template>

<script>
import NavBar from './components/NavBar.vue'

export default {
  name: 'App',
  components: {
    NavBar
  }
}
</script>

<style>
body {
  background-color: black;
  font-family: 'Montserrat', sans-serif;
}

#content {
  background: black;
  margin: 0 auto;
  width: 100%;
}

/* Media queries */
@media (max-width: 499px) {
  #content {
    display: grid;
    grid-template-areas:
      "header"
      "nav"
      "main"
      "banner"
      "content";
  }

  .main-nav a {
    display: none;
  }

  .main-head div.icon {
    right: 0;
    position: absolute;
    float: right;
    display: block;
  }

/* Open hamburger */ 
  .main-nav.open {
    position: absolute;
    right: 0.75rem;
    margin-top: 3rem;
    padding: 1rem;
    background-color: rgba(50,50,50,0.8);
  }

  .main-nav.open .nav-home {
    top: 3rem;
  }

  .main-nav.open .icon {
    position: absolute;
    right: 0;
    top: 0;
  }

  .main-nav.open a {
    float: none;
    display: block;
    text-align: right;
  }

  .main-nav.open :hover {
    color: grey;
  }

  /* Logo */
  .main-logo {
    position: absolute;
    left: 0.3125rem;
    height: 2.5rem;
    width: 2.5rem;
  }

  #logo{
    display: none;
  }

  /* Menu */
  .mainMenu {
    padding-top: 3rem;
  }
}

@media (min-width: 500px) {
  #content {
    grid-template-columns: 1fr 3fr;
    grid-template-areas: 
      "header  header"
      "nav     nav"
      "main    main";
    overflow: hidden;
  }

  .main-head div.icon {
    display: none;
    right: 0;
    position: absolute;
  }

  .main-nav a {
    padding: 2rem 1rem;
  }

  .main-logo {
    display: none;
  }

  nav {
    display: flex;
    justify-content: space-around;
    align-items: center;
    background-color:rgba(105,105,105,0.3);
  }

  .nav-links {
    font-size: 1.2rem;
    text-transform: uppercase;
    text-decoration: none;
    color: rgba(255,255,255);
    border-left: 0.0625rem solid transparent;
    border-right: 0.0625rem solid transparent;
  }
  
  .nav-links:hover {
    color: grey;
    padding: 2rem 1rem;
    border-color: grey;
  }

  .main-content {
    position: relative;
  }

  .text {
    position: absolute;
    right: 1rem;  
    justify-content: right;
    height: 9.375rem;
    width: 9.375rem;
  }

  #logo {
    height: 2.5rem;
    width: 2.5rem;
  }
}

@media (min-width: 600px) {
  .text {
    right: 1rem;
    font-size: 1.4rem;
    height: 13.375rem;
    width: 12.375rem;
  }
}

@media (min-width: 800px) {
  .text {
    right: 4rem;
    font-size: 1.4rem;
    height: 13.375rem;
    width: 12.375rem;
  }

  .logo {
    padding: 0.875rem 1rem;
    height: 3.5rem;
    width: 3.5rem;
  }
}
</style>
