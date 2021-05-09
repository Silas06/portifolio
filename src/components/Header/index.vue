<template>
  <header class="justify-content-center">
    <div class="container m-auto">
      <div class="row justify-content-between align-items-center mob">
        <p class="text-white py-4">{{ fullName }}</p>
        <nav>
          <ul class="nav ">
            <li class="nav-item ">
              <router-link :to="{ name: 'Home' }" class="nav-link text-white active" href="">Home</router-link>
            </li>
            <li class="nav-item">
              <router-link :to="{ name: 'Portifolio' }" class="nav-link text-white">Portifólio</router-link>
            </li>
            <li classs="nav-item">
              <a class="nav-link text-white" href="">Contato</a>
            </li>
          </ul>
        </nav>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  data: () => ({
    user: {
      name: 'Silas',
      lastName: 'Paixão de Oliveira'
    }
  }),

  computed: {
    fullName: function () {
      return `${this.user.name} ${this.user.lastName}`
    }
  }
}
</script>

<style scoped>
header {
  background-image: linear-gradient(to right, #1ABDDB 8%, #0A3757 );
}
p {
  font-size: 1.9rem;
}
ul li {
  cursor: pointer;
  list-style: none;
}
ul li:hover {
  opacity: 0.8;
}

@media (max-width: 700px) {
  .mob {
    justify-content: center !important;
  }
}
</style>
