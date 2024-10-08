<template>
  <footer>
    <!-- Seção Laranja -->
    <div class="footer-top">
      <div class="links">
        <router-link to="/">Privacy Policy</router-link>
        <router-link to="/">Salvadores</router-link>
        <router-link to="/">RGPD</router-link>
        <router-link to="/">Cookie Policies</router-link>
      </div>
      <div class="social-icons">
        <i class="bi bi-whatsapp"></i>
        <i class="bi bi-instagram"></i>
        <i class="bi bi-facebook"></i>
        <i class="bi bi-twitter"></i>
      </div>
    </div>

    <!-- Seção Escura -->
    <div class="footer-bottom">
      <p>
        Todos os quadrinhos e livros deste site são apenas prévias dos quadrinhos originais, podendo haver muitos erros de linguagem, nomes de personagens e enredos. Para a versão original, compre o quadrinho se estiver disponível em sua cidade.
      </p>
    </div>
  </footer>
</template>

<style scoped>
/* Estilo da área superior (laranja) */
.footer-top {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: #ff7f00; /* Laranja */
  padding: 20px;
}

.links {
  display: flex;
  gap: 20px;
}

.links a {
  color: white;
  text-decoration: none;
  font-size: 14px;
}

.social-icons i {
  font-size: 24px;
  margin-left: 20px;
  color: white;
  cursor: pointer;
}

/* Estilo da área inferior (escura) */
.footer-bottom {
  background-color: #333333; /* Cinza escuro */
  color: white;
  padding: 20px;
  text-align: center;
  font-size: 12px;
}

p {
  margin: 0;
}
</style>
