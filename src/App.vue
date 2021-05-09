<template>
  <div id="app">
    <Header />
    <router-view />
    <Footer />
  </div>
</template>

<script>
import './styles/global.css'
import 'bootstrap'
import 'bootstrap/dist/css/bootstrap.min.css'

import Header from '@/components/Header'
import Footer from '@/components/Footer'

export default {
  components: { Header, Footer }
}
</script>

<style>
h1 {
  color: var(--color-blue);
}
</style>
