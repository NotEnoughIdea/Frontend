<template>
<div class="hero-head">
  <header class="navbar">
    <div class="container">
      <div class="navbar-brand">
        <span class="navbar-item">
        <a class="button is-dark is-inverted">NotEnoughIdea</a>
        </span>
        <span class="navbar-burger burger" data-target="navbarMenuHeroC">
          <span></span>
          <span></span>
          <span></span>
        </span>
      </div>
      <div id="navbarMenuHeroC" class="navbar-menu">
        <div class="navbar-end">
          <a class="navbar-item is-active" href="https://github.com/NotEnoughIdea/Ideas" target="_blank">How to contribute ?</a>
          <a class="navbar-item" href="https://github.com/LightDiscord" target="_blank">Made by @LightDiscord</a>
          <span class="navbar-item">
            <a class="button is-dark is-inverted" href="https://github.com/NotEnoughIdea" target="_blank">
              <span class="icon">
                <i class="fa fa-github"></i>
              </span>
              <span>See on GitHub</span>
            </a>
          </span>
        </div>
      </div>
    </div>
  </header>
</div>
</template>

<script>
export default {
  name: 'HeroHead'
}
</script>
