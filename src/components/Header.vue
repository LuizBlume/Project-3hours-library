<template>
  <header>
    <nav class="navbar">
      <div class="container-fluid">
        <a class="navbar-brand" href="#">
          <img
            src="../assets/images/logo.png"
            alt="Logo"
            width="100"
            height="100"
            class="d-inline-block align-text-top"
          />
        </a>
        <ul class="nav justify-content-end">
          <li class="nav-item">
            <router-link to="/" class="nav-link">
              <img src="../assets/images/favoritos.png" alt="" id="icon-fav" class="icons" />
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
    width: 40px;
    height: 40px;
    margin: 0 10px;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
}

#icon-fav {
  position: relative;
  left: 15px;
}

.text-icons {
    font-size: 1.5rem;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
}
</style>