# Jogo-de-Adivinha
Jogo de Adivinhação criado no segundo dia de Imersão Dev da Alura

HTML
<div class="container">
  <h1 class="page-title">
    JOGO DE ADIVINHAÇÃO
  </h1>
  <img src="https://www.alter-a.com/wp-content/uploads/2019/07/Test-Logo-Small-Black-transparent-1.png" class="page-logo" alt="">
</div>
<a href="https://alura.com.br/" target="_blank">
  <img src="https://www.alura.com.br/assets/img/home/alura-logo.svg" alt="" class="alura-logo">
 
</a>


CSS
body {
  font-family: "Roboto Mono", monospace;
  text-align: center;
  background-image: url("https://th.bing.com/th/id/OIP.3bh88WfqYjAi-0SfLsCuEgHaHa?pid=ImgDet&rs=1");
  background-color: #000000;
  background-size: cover;
  background-position: center top;
  background-repeat: no-repeat;
  height: 100vh;
}

.container {
  text-align: center;
  padding: 20px;
}

.page-title {
  color: #ffffff;
  margin: 0 0 5px;
}

.page-subtitle {
  color: #ffffff;
  margin-top: 5px;
}

.page-logo {
  width: 200px;
}

.alura-logo {
  width: 40px;
  position: absolute;
  top: 10px;
  right: 10px;
}

body > img {
  margin: 0 10px;
}

img {
  max-height: 350px;
}


JS
var numeroSecreto = Math.ceil(Math.random() * 1000); 
var tentativas = 0; 
var limite = 8; 
var chute; 

while (tentativas < limite) { 
  chute = prompt('Digite um número entre 1 e 1000.' + "  Você pode tentar 8 vezes ou perde"); 
  tentativas++; 
  if (chute == numeroSecreto) {
    alert('Parabéns, você acertou o número em ' + tentativas + ' tentativas!'); 
    break; 
  } else if (chute > numeroSecreto) { 
    alert('Errou... o número secreto é menor'); 
  } else if (chute < numeroSecreto) { 
    alert('Errou... o número secreto é maior'); 
  }
}

if (tentativas == limite) { 
  alert('Você perdeu o jogo. O número secreto era ' + numeroSecreto);
}
