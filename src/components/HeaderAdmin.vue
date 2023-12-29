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
      </div>
    </nav>
  </header>
</template>
<style scoped>
header {
  display: flex;
  justify-content: center;
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

#icon-fav {
  position: relative;
  left: 15px;
}
</style>