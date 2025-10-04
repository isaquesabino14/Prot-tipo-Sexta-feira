<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Trilha Fullstack</title>
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      background-color: #f4f4f4;
      margin: 0;
      padding: 0;
    }

    header {
      background-color: #333;
      color: #fff;
      padding: 30px;
      text-align: center;
    }

    .container {
      max-width: 1000px;
      margin: 30px auto;
      padding: 20px;
    }

    .card {
      background-color: white;
      border-radius: 8px;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
      margin-bottom: 30px;
      padding: 20px;
      transition: transform 0.2s;
    }

    .card:hover {
      transform: translateY(-5px);
    }

    .card img {
      max-width: 100%;
      border-radius: 5px;
      margin-top: 15px;
    }

    h2 {
      color: #444;
    }

    ul {
      padding-left: 20px;
    }

    button.toggle-btn {
      background-color: #333;
      color: white;
      padding: 10px 15px;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      margin-top: 10px;
    }

    button.toggle-btn:hover {
      background-color: #555;
    }

    .content {
      display: none;
      margin-top: 15px;
    }

    .price {
      font-weight: bold;
      color: #008000;
      margin-top: 10px;
    }
  </style>
</head>
<body>

<header>
  <h1>Trilha de aprendizagem para se tornar um desenvolvedor Fullstack</h1>
</header>

<div class="container">

  <!-- EXEMPLO DE MÓDULO -->
  <section class="card">
    <h2>Fundamentos da Web & Front-End Básico</h2>
    <button class="toggle-btn">Ver Conteúdo</button>
    <div class="content">
      <ul>
        <li>Estrutura de uma página HTML (tags, títulos, listas, links, imagens).</li>
        <li>Como usar CSS para estilizar (cores, fontes, tamanhos, margens).</li>
        <li>Criar layouts simples e responsivos.</li>
        <li>Primeiros passos com Git e GitHub (salvar e versionar código).</li>
        <li>Montar páginas estáticas (tipo um site institucional simples).</li>
      </ul>
      <p class="price">Tudo isso por R$40</p>
      <img src="frontend.img" alt="Ícone computador">
    </div>
  </section>

  <!-- DEMAIS MÓDULOS - copie a estrutura acima -->
  <section class="card">
    <h2>JavaScript (Fundamentos)</h2>
    <button class="toggle-btn">Ver Conteúdo</button>
    <div class="content">
      <ul>
        <li>Variáveis, tipos de dados e operadores.</li>
        <li>Estruturas de controle: if, for, while.</li>
        <li>Funções, arrays e objetos.</li>
        <li>Manipulação do DOM (alterar textos, imagens e estilos via JS).</li>
        <li>Páginas interativas (menus, botões, etc.).</li>
      </ul>
      <p class="price">Tudo isso por R$40</p>
      <img src="java.img" alt="Imagem JavaScript">
    </div>
  </section>

  <!-- Adicione os outros módulos da mesma forma -->
  <!-- ... outros módulos com toggle igual acima -->

</div>

<script>
  // Interatividade: mostrar/esconder conteúdo
  document.querySelectorAll('.toggle-btn').forEach((button) => {
    button.addEventListener('click', () => {
      const content = button.nextElementSibling;
      const isVisible = content.style.display === 'block';

      // Oculta todos os outros
      document.querySelectorAll('.content').forEach((c) => c.style.display = 'none');
      document.querySelectorAll('.toggle-btn').forEach((btn) => btn.textContent = 'Ver Conteúdo');

      // Se não estava visível, mostra este
      if (!isVisible) {
        content.style.display = 'block';
        button.textContent = 'Ocultar Conteúdo';
      }
    });
  });
</script>

</body>
</html>
