<template>
  <header class="main-header">
    <div class="container">
      <div class="row justify-content-between align-items-center">
        <div class="col-md-3 col-4">
          <nuxt-link class="btn block" to="/">
            <img src="assets/img/logo.svg" />
          </nuxt-link>
        </div>
        <div class="col-md-6 hidden-on-mobile">
          <ul class="main-nav">
            <li><a href="whats-different.html">What's Different</a></li>
            <li><nuxt-link class="btn block" to="/blog">Blog</nuxt-link></li>
            <li><nuxt-link class="btn block" to="/about">About</nuxt-link></li>
            <li><nuxt-link class="btn block" to="/projects">Projects</nuxt-link></li>
            <!-- <li><a href="features.html">Features</a></li>-->
            <li class="submenu">
              <a href="javascript:;" class="popper-init drop-down" data-target="#use-cases-menu">For</a>
              <div
                id="use-cases-menu"
                class="top-dd-menu"
                data-popper-placement="bottom-start"
                style="position: absolute; inset: 0px auto auto 0px; margin: 0px; transform: translate(318px, 24px)"
              >
                <ul class="menu-list">
                  <li><a href="teams.html">Teams &amp; Individuals</a></li>
                  <li><a href="businesses.html">Businesses</a></li>
                </ul>
              </div>
            </li>
            <li><a href="pricing.html">Pricing</a></li>
            <li class="submenu">
              <a href="javascript:;" class="popper-init drop-down" data-target="#more-menu">More</a>
              <div
                id="more-menu"
                class="top-dd-menu"
                data-popper-placement="bottom-start"
                style="position: absolute; inset: 0px auto auto 0px; margin: 0px; transform: translate(472px, 24px)"
              >
                <ul class="menu-list">
                  <li><a href="integrations.html">Integrations</a></li>
                  <li><a href="">eSign Legality Guide*</a></li>
                  <!-- <li><a href="">Security</a></li> -->
                  <li><a href="">Help &amp; Support</a></li>
                  <li><a href="careers.html">Careers</a></li>
                  <li><a href="contact.html	">Contact Us</a></li>
                </ul>
              </div>
            </li>
          </ul>
        </div>
        <div class="col-md-3 col-8">
          <ul class="right-nav">
            <li>
              <a href="" class="top-signin" data-text="Sign in"><span>Sign In</span></a>
            </li>
            <li>
              <a href="" class="top-cta" data-text="Try for FREE"><span>Try for FREE</span></a>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </header>
  <!--
  <nav class="scrim-bg fixed z-40 top-0 inset-x-0 pt-3 px-3" aria-label="Main Menu">
    <ul class="flex">
      <li class="flex-1">
        <nuxt-link class="btn block" to="/">Home</nuxt-link>
      </li>
      <li class="flex-1 ml-2">
        <nuxt-link class="btn block" to="/about">About</nuxt-link>
      </li>
      <li class="flex-1 ml-2">
        <nuxt-link class="btn block" to="/blog">Blog</nuxt-link>
      </li>
      <li class="flex-1 ml-2">
        <nuxt-link class="btn block" to="/projects">Projects</nuxt-link>
      </li>
    </ul>
  </nav>
  -->
</template>

<script>
export default {
  name: 'Header',
}
</script>

<style lang="postcss" scoped>
</style>
