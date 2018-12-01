<template>
  <section class="forum">
    <h2>Forum</h2>
    <div class="topics">
      <h3>Topic</h3>
      <ul>
        <nuxt-link to="thread/first-thread">
          <h3>First thread</h3>
          <!-- Beskrivelse -->
          <!-- Forfatter -->
          <!-- Date -->
        </nuxt-link>
        <nuxt-link to="thread/second-thread">Second thread</nuxt-link>
        <nuxt-link to="thread/third-thread">Third thread</nuxt-link>
        <nuxt-link to="thread/fourth-thread">Fourth thread</nuxt-link>
      </ul>
    </div>
    <div class="topics">
      <h3>Topic</h3>
      <ul>
        <nuxt-link to="thread/first-thread">First thread</nuxt-link>
        <nuxt-link to="thread/second-thread">Second thread</nuxt-link>
        <nuxt-link to="thread/third-thread">Third thread</nuxt-link>
        <nuxt-link to="thread/fourth-thread">Fourth thread</nuxt-link>
      </ul>
    </div>
  </section>
</template>

<script>
import Logo from '~/components/Logo.vue'
export default {
  components: {
    Logo
  }
}
</script>
