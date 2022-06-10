<script >
import NavBar from '@/components/NavBar.vue'
import FooterNav from '@/components/FooterNav.vue'

export default {
  components: { NavBar, FooterNav }
}

</script>

<template>
  <body class="flex flex-col min-h-screen">
    <header v-if="!loggedIn" class="self-center">
      <img
        alt="Personal Logo"
        src="@/assets/KnyHeads.png"
        class="max-w-sm mt-2"
      />
      <!-- <h1 class="text-xl align-middle">Header text or Company name</h1> -->
    </header>
    <nav>
      <div class="text-2xl text-center">
        <NavBar />
      </div>
    </nav>
    <main>
      <router-view />
    </main>
    <footer class="mt-auto">
      <div class="text-2xl text-center">
        <FooterNav />
      </div>
    </footer>
  </body>
</template>
