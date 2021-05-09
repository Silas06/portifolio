<template>
  <div class="container m-auto">
    <h1 class="text-center mb-4 mt-5">Portifólio</h1>

    <div class="card-group pt-4">
      <a :href="projeto.link" target="_blank"  class="card shadow" v-for="projeto in portifolio" :key="projeto.title">
        <img
          :src="projeto.image"
          :title="projeto.title"
          :alt="projeto.title"
        />
        <div class="card-body">
          <h5 class="card-title">{{ projeto.title }}</h5>
          <p class="card-text">
            {{ projeto.description }}
          </p>
          <p class="card-text">
            <small class="text-muted">Last updated 3 mins ago</small>
          </p>
        </div>
      </a>
    </div>
  </div>
</template>

<script>
import portifolio from '../../utils/portifolio'
export default {
  data: () => ({
    portifolio
  })
}
</script>

<style scoped>
.card-group {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 23px;
}
a{
text-decoration: none;
color: #0A3757;
cursor: pointer;
}
a:hover{
opacity: .8;
}

@media (max-width: 600px) {
  .card-group {
    display: grid;
    grid-template-columns: 1fr;
    gap: 17px;
  }
}
</style>
