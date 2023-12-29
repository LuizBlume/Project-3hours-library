<template>
  <header>
    <nav class="navbar">
      <div class="container-fluid">
        <a class="navbar-brand" href="#">
          <img
            src="../assets/images/logo.png"
            alt="Logo"
            width="140"
            height="140"
            class="d-inline-block align-text-top"
          />
        </a>
        <ul class="nav justify-content-end">
          <li class="nav-item">
            <router-link to="/" class="nav-link">
              <img src="../assets/images/favoritos.png" alt="" class="icons" />
              <div class="text-icons">
                Favoritos
              </div>
            </router-link>
          </li>
          <li class="nav-item">
            <router-link to="/login" class="nav-link">
              <img src="../assets/images/cesta.png" alt="" class="icons" />
              <div class="text-icons">
                Cesta
              </div>
            </router-link>
          </li>
          <li class="nav-item">
            <router-link to="/login" class="nav-link">
              <img src="../assets/images/perfil.png" alt="" class="icons" />
              <div class="text-icons">
                Perfil
              </div>
            </router-link>
          </li>
        </ul>
      </div>
    </nav>
  </header>
</template>
<style scoped>
header {
  padding: 20px 5px;
  background-color: #5687a6;
}
a {
  color: #fff !important;
  font-size: 2rem;
}
.container-fluid {
  --bs-gutter-x: 0;
}
.icons {
    width: 70px;
    height: 70px;
    margin: 0 10px;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
}
.text-icons {
    font-size: 1.7rem;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
}
.nav-link {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    color: #fff !important;
    font-size: 1.7rem;
    margin: 0 10px;
}
</style>