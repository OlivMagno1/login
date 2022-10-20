<template>
  <div class="home">
    <p class="card">
      <router-link to="/login" class="card__link" href="#"
        >Login <i class="fas fa-arrow-right"></i
      ></router-link>
      <router-link to="/cadastro" class="card__link" href="#"
        >Cadastro <i class="fas fa-arrow-right"></i
      ></router-link>
    </p>
  </div>
</template>

<script>
export default {
  name: "HomeView",
  components: {},
};
</script>

<style scoped>
.home {
  width: 100%;
  height: 100%;

  display: flex;
  justify-content: center;
  align-items: center;
}

.selectionCard {
  height: 10rem;

  display: flex;
  flex-flow: column nowrap;
  justify-content: space-evenly;
}

.cards {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
}

.card {
  margin: 20px;
  padding: 20px;
  width: 500px;
  min-height: 200px;
  display: flex;
  flex-flow: column nowrap;
  border-radius: 10px;
  box-shadow: 0px 6px 10px rgba(0, 0, 0, 0.25);
  transition: all 0.2s;
  background: radial-gradient(#1fe4f5, #3fbafe);
}

.card__link {
  position: relative;
  text-decoration: none;
  color: rgba(255, 255, 255, 0.9);
}

.card__link::after {
  position: absolute;
  top: 25px;
  left: 0;
  content: "";
  width: 0%;
  height: 3px;
  background-color: rgba(255, 255, 255, 0.6);
  transition: all 0.5s;
}

.card__link:hover::after {
  width: 100%;
}

.card__exit {
  grid-row: 1/2;
  justify-self: end;
}
</style>
