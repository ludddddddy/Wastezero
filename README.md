[README.md](https://github.com/user-attachments/files/20647564/README.md)<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Waste Zero</title>
  <link rel="stylesheet" href="assets/css/styles.css" />
</head>
<body>
  <header>
    <div class="logo">
      <img src="img/image-removebg-preview (2).png" alt="Logo Waste Zero"  width="100px" height="100px"/>
    </div>
    <nav>
      <ul>
        <li class="active">Home</li>
        <li><a href="pedidos.html">Pedidos</a></li>
        <li>Lojas</li>
        <li>Sobre</li>
      </ul>
    </nav>
  </header>

  <section class="hero" id="hero1">
    <div class="hero-text">
      <p>Faça parte de uma</p>
      <h1>Experiência transformadora</h1>
    </div>
    <div class="hero-image">
      <div class="background-circle"></div>
      <img src="img/ChatGPT Image 7 de jun. de 2025, 10_56_15.png" alt="Embalagem" />
    </div>
  </section>

  <section class="hero hidden" id="hero2">
    <div class="hero-image">
      <div class="background-circle left"></div>
      <img src="img/ChatGPT Image 7 de jun. de 2025, 11_00_20.png" alt="Burger" />
    </div>
    <div class="hero-text">
      <p>Vivencie a</p>
      <h1>Sustentabilidade<br />E desfrute sem limites</h1>
    </div>
  </section>

  <script src="assets/js/scripts.js"></script>
  <div class="menu-lateral" id="menuLateral"></div>

<div class="pedido-detalhe">
  <img id="imagem-pedido" />
  <h3 id="nome-pedido"></h3>
  <h2 class="status" id="status-pedido"></h2>
  <div class="linha-progresso">
    <div class="etapa preenchida"></div>
    <div class="etapa preenchida"></div>
    <div class="etapa preenchida"></div>
    <div class="etapa preenchida"></div>
  </div>
  <p class="hora" id="hora-pedido"></p>
</div>

  <div class="menu-lateral" id="menuLateral"></div>


</body>
</html>
# Wastezero

<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <title>Pedidos - Waste Zero</title>
  <link rel="stylesheet" href="assets/css/styles.css">
</head>
<body>
  <header>
    <div class="logo">
      <img src="img/image-removebg-preview (2).png" alt="Logo Waste Zero" width="120px" height="100px">
    </div>
    <nav>
      <ul>
        <li><a href="index.html">Home</a></li>
        <li class="active">Pedidos</li>
        <li>Lojas</li>
        <li>Sobre</li>
      </ul>
    </nav>
  </header>

  <main class="pedidos-container">
    <aside class="menu-lateral">
      <div class="pedido ativo">
        <img src="img/PIZZAAA.jpg" alt="Pizza Margerrita">
        <span>Pizza Margerrita</span>
        <span class="star">★</span>
      </div>
      <div class="pedido">
        <img src="img/pizaa2.jpg" alt="Pizza 2">
      </div>
      <div class="pedido">
        <img src="img/pizaa2.jpg" alt="Pizza 3">
        <span class="star">★</span>
      </div>
    </aside>
    <section class="pedido-detalhe">
      <img src="img/PIZZAAA.jpg" alt="Pizza Margerrita" width="10000px" height="500px">
      <h2>Pizza Margerrita</h2>
      <h1>Saiu para entrega</h1>
      <div class="status-bar">
        <div class="step completo"></div>
        <div class="step completo"></div>
        <div class="step completo"></div>
        <div class="step completo"></div>
      </div>
      <span class="hora">17:00</span>
    </section>
  </main>
</body>
</html>

window.addEventListener("scroll", () => {
  const hero2 = document.getElementById("hero2");
  const scrollY = window.scrollY;

  if (scrollY > 300) {
    hero2.classList.remove("hidden");
  }
});
const pedidos = [
  {
    imagem: "pizza1.jpg",
    nome: "Pizza Margerrita",
    status: "Saiu para entrega",
    hora: "17:00",
  },
  {
    imagem: "pizza2.jpg",
    nome: "Pizza Calabresa",
    status: "Preparando",
    hora: "16:45",
  },
  {
    imagem: "pizza3.jpg",
    nome: "Pizza Quatro Queijos",
    status: "Recebido",
    hora: "16:30",
  },
  
];

function mostrarPedido(indice) {
  const pedido = pedidos[indice];
  document.getElementById("imagem-pedido").src = pedido.imagem;
  document.getElementById("nome-pedido").innerText = pedido.nome;
  document.getElementById("status-pedido").innerText = pedido.status;
  document.querySelector(".hora").innerText = pedido.hora;

  // Atualiza destaque no menu
  document.querySelectorAll(".pedido-item").forEach((item, i) => {
    item.classList.toggle("ativo", i === indice);
  });
}

body {
  margin: 0;
  font-family: 'Inter', sans-serif;
}

header {
  display: flex;
  justify-content: space-between;
  padding: 1rem 2rem;
  border-bottom: 1px solid #ccc;
}

nav ul {
  display: flex;
  list-style: none;
  gap: 2rem;
}

nav ul li.active::after {
  content: "";
  display: block;
  width: 100%;
  height: 3px;
  background: #d87b00;
  margin-top: 5px;
}

.hero {
  display: flex;
  justify-content: space-between;
  padding: 4rem 2rem;
  align-items: center;
  min-height: 100vh;
  transition: opacity 0.8s ease;
}

.hero.hidden {
  opacity: 0;
  transform: translateY(50px);
  pointer-events: none;
}

.hero-image {
  position: relative;
  width: 50%;
}

.background-circle {
  position: absolute;
  background-color: #d87b00;
  width: 1000px;
  height: 1000px;
  border-radius: 50%;
  top: -60px;
  right: -300px;
  z-index: 0;
}

.background-circle.left {
  left: -300px;
  right: auto;
}

.hero-image img {
  position: relative;
  width: 100%;
  z-index: 1;
}

.hero-text {
  max-width: 45%;
}

h1{
  font-size: 90px;
  color: #d87b00;
}
p{
  font-size: 50px;
  color: rgb(64, 112, 8);
}
body {
  margin: 0;
  font-family: 'Inter', sans-serif;
  background-color: #ffffff;
  color: #000000;
}

header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem 2rem;
  border-bottom: 1px solid #ccc;
}

.logo img {
  height: 50px;
}

nav ul {
  display: flex;
  list-style: none;
  padding: 0;
  margin: 0;
}

nav ul li {
  margin-left: 2rem;
  font-weight: 600;
  position: relative;
}

nav ul li.active::after {
  content: "";
  display: block;
  width: 100%;
  height: 3px;
  background-color: #d87b00;
  position: absolute;
  bottom: -5px;
  left: 0;
}

.pedidos-container {
  display: flex;
  height: calc(100vh - 80px);
}

.menu-lateral {
  width: 300px;
  background-color: #f9f9f9;
  border-right: 1px solid #ddd;
  padding: 1rem;
  box-sizing: border-box;
}

.pedido {
  display: flex;
  align-items: center;
  gap: 1rem;
  padding: 1rem;
  background: #fff;
  border: 2px solid #ccc;
  border-radius: 12px;
  margin-bottom: 1rem;
  cursor: pointer;
  transition: 0.2s;
}

.pedido:hover {
  background-color: #f0f0f0;
}

.pedido-item.ativo {
  border: 2px solid orange;
  background-color: #fff7e6;
  border-radius: 10px;
}


.pedido img {
  height: 50px;
  width: 50px;
  border-radius: 8px;
  object-fit: cover;
}

.pedido .star {
  margin-left: auto;
  font-size: 1.2rem;
  color: #ffc107;
}

.pedido-detalhe {
  flex: 3;
  padding: 2rem;
  box-sizing: border-box;
}

.pedido-detalhe img {
  width: 1000px;
  height: 500px;
  border-radius: 16px;
  object-fit: cover;
  margin-bottom: 1rem;
}

.pedido-detalhe h2 {
  margin: 0;
  font-size: 1.5rem;
  font-weight: 600;
}

.pedido-detalhe h1 {
  font-size: 2rem;
  font-weight: 800;
  margin: 0.5rem 0;
}

.status-bar {
  display: flex;
  margin: 1.5rem 0;
  gap: 0.5rem;
}

.status-bar .step {
  flex: 1;
  height: 10px;
  background-color: #ccc;
  border-radius: 5px;
}

.status-bar .step.completo {
  background-color: #4caf50;
}

.hora {
  font-size: 1.2rem;
  color: #888;
}
.pedido-detalhe img {
  width: 1000px;
  height: 500px;
  border-radius: 16px;
  object-fit: cover;
  margin-bottom: 1rem;
}

.pedido-item.ativo {
  border: 2px solid orange;
  background-color: #fff7e6;
  border-radius: 10px;
}
[
  {
    "imagem": "pizza1.jpg",
    "nome": "Pizza Margerrita",
    "status": "Saiu para entrega",
    "hora": "17:00"
  },
  {
    "imagem": "pizza2.jpg",
    "nome": "Pizza Calabresa",
    "status": "Preparando",
    "hora": "16:45"
  },
  {
    "imagem": "pizza3.jpg",
    "nome": "Pizza Quatro Queijos",
    "status": "Recebido",
    "hora": "16:30"
  }
]
[Uploadi
# 📦 Waste Zero

**Waste Zero** é um projeto de interface web que promove a sustentabilidade e o combate ao desperdício de alimentos. Inspirado em iniciativas como o *Food To Save*, este site apresenta uma experiência visual amigável e moderna, permitindo aos usuários conhecer mais sobre a causa e acompanhar pedidos de alimentos.

## 🖼️ Visão Geral

O projeto é composto por duas páginas principais:

- `index.html`: Página inicial com apresentação da proposta da plataforma.
- `pedidos.html`: Página de visualização de pedidos realizados.

---

## 📁 Estrutura de Arquivos

```plaintext
/
├── index.html              # Página inicial com seções de destaque
├── pedidos.html            # Página para acompanhamento dos pedidos
├── assets/
│   ├── css/
│   │   └── styles.css      # Estilos CSS globais
│   └── js/
│       └── scripts.js      # Scripts JS para interação (ex: transições)
├── img/
│   ├── image-removebg-preview (2).png
│   ├── PIZZAAA.jpg
│   ├── pizaa2.jpg
│  
```

---

## 🔍 Descrição das Páginas

### `index.html` – Página Inicial

- Apresenta a marca e slogan da plataforma.
- Inclui duas seções principais (hero) com imagens ilustrativas e textos motivacionais.
- Navegação com links para outras páginas do site.

### `pedidos.html` – Pedidos

- Interface com um menu lateral exibindo itens de pedidos (ex: pizzas).
- Área de detalhe com status da entrega e previsão de horário.
- Uso de ícones e imagens para representar o andamento do pedido.

---

## 🛠️ Tecnologias Utilizadas

- **HTML5**
- **CSS3**
- **JavaScript** (arquivo externo presumido: `scripts.js`)
- Imagens estáticas para ilustração e branding

---

## 🚀 Como Usar

1. Clone ou baixe os arquivos do repositório.
2. Coloque a pasta em um servidor local ou abra `index.html` diretamente no navegador.
3. Clique em “Pedidos” na navegação para ver os detalhes dos pedidos.

---

## 💡 Ideias para Futuras Melhorias

- Integração com back-end para gerenciamento de pedidos em tempo real.
- Responsividade aprimorada para dispositivos móveis.
- Sistema de login para usuários e parceiros.
- Página de lojas e sobre (links existentes no menu, mas ainda não implementados).

---

## 📸 Demonstrações

> *Adicione capturas de tela do site aqui, se desejar ilustrar visualmente.*

---

## 🧾 Licença

Este projeto é apenas um protótipo educacional. Sinta-se livre para adaptar, reutilizar e distribuir conforme sua necessidade.
ng README.md…]()




