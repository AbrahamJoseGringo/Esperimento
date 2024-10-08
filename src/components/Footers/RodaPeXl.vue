<template>
  <div class="footer-container">
    <div class="footer-links">
      <h4>Políticas</h4>
      <ul>
        <li><router-link class="footer-link" to="/">Privacy Policy</router-link></li>
        <li><router-link class="footer-link" to="/">Salvadores</router-link></li>
        <li><router-link class="footer-link" to="/">RGPD</router-link></li>
        <li><router-link class="footer-link" to="/">Cookie Policies</router-link></li>
      </ul>
    </div>

    <div class="footer-about">
      <h4>Sobre Nós</h4>
      <p>
        Todos os quadrinhos e livros deste site são apenas prévias dos quadrinhos originais, podendo haver
        muitos erros de linguagem, nomes de personagens e enredos. Para a versão original, compre o quadrinho
        se estiver disponível em sua cidade.
      </p>
    </div>

    <div class="footer-social">
      <h4>Redes Sociais</h4>
      <div class="social-icons">
        <a href="#" class="social-icon">WhatsApp</a>
        <a href="#" class="social-icon">Instagram</a>
        <a href="#" class="social-icon">Facebook</a>
        <a href="#" class="social-icon">Twitter</a>
      </div>
    </div>
  </div>
</template>

<style scoped>
.footer-container {
  display: flex;
  justify-content: space-between;
  padding: 30px 50px;
  background-color: #333; /* Cor de fundo escura */
  color: #fff; /* Cor do texto clara */
  font-family: Arial, sans-serif;
}

.footer-links, .footer-about, .footer-social {
  width: 30%;
}

h4 {
  font-size: 18px;
  margin-bottom: 15px;
  color: #ffa500; /* Cor laranja para os títulos */
}

ul {
  list-style: none;
  padding: 0;
}

li {
  margin-bottom: 10px;
}

.footer-link {
  text-decoration: none;
  color: #fff; /* Cor do texto dos links */
  transition: color 0.3s ease;
}

.footer-link:hover {
  color: #ffa500; /* Cor laranja ao passar o mouse */
}

.footer-about p {
  font-size: 14px;
  line-height: 1.6;
}

.footer-social {
  display: flex;
  flex-direction: column;
}

.social-icons {
  display: flex;
  justify-content: space-between;
  margin-top: 10px;
}

.social-icon {
  color: #ffa500; /* Cor laranja para os ícones sociais */
  text-decoration: none;
  transition: color 0.3s ease;
}

.social-icon:hover {
  color: #fff; /* Cor branca ao passar o mouse */
}

@media (max-width: 768px) {
  .footer-container {
    flex-direction: column;
    padding: 20px;
  }

  .footer-links, .footer-about, .footer-social {
    width: 100%;
    margin-bottom: 20px;
  }

  h4 {
    text-align: center;
  }

  p {
    text-align: center;
  }
}
</style>
