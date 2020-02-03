<template>
<div class="main-content">
  <img class="banner" alt="ramen bowl" src="../assets/ramen.jpg">
  <p class="text">`"For a bowl of soul warming, slurp-able goodness,
    head to Ponsonby's hot new Ramen restaurant."<br />
    - The Denizen`</p>
</div>
</template>

<script>

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.banner {
  grid-area: banner;
  max-width: 100%;
  height: auto;
}

.text {
  grid-area: content;
  color: rgba(255,255,255);
  background-color: rgba(50,50,50,0.8);
  padding: 1rem;
  top: 1.875rem;
  right: 0.625rem;
}
</style>
