<script>
    // Redirecionamento para páginas específicas
    function goToPg2() {
      window.location.href = '/pg2';
    }
    
  </script>
  
  <style>
    /* Fundo geral */
    :global(body) {
      background-color: #f2f2f2;
      color: black;
    }
  
    /* Navbar fixa com ícones */
    .navbar {
      position: fixed;
      top: 0;
      width: 100%;
      z-index: 1000;
      background: #7ba1c7;
      padding: 10px;
    }
  
    .navbar .btn {
      color: rgb(167, 38, 38);
      margin-right: 10px;
    }
  
    /* Estilização do carrossel */
    .carousel {
      margin-top: 60px; /* Para evitar sobreposição com a navbar */
    }
  
    .carousel-caption {
      bottom: 20%;
    }
  
    /* Cards dos Doramas */
    .dorama-grid {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 15px;
      padding: 20px;
    }
  
    .dorama-card {
      border: none;
      border-radius: 10px;
      overflow: hidden;
      box-shadow: 0 4px 8px rgba(0,0,0,0.1);
      transition: transform 0.3s;
      text-align: center;
    }
  
    .dorama-card img {
      height: 180px;
      object-fit: cover;
    }
  
    .dorama-card:hover {
      transform: scale(1.02);
    }
  
    /* Cards pequenos no centro */
    .small-card-container {
      display: flex;
      justify-content: center;
      gap: 15px;
      margin-top: 20px;
    }
  
    .small-card {
      width: 220px;
      text-align: center;
      cursor: pointer;
      border-radius: 10px;
      background: linear-gradient(to right, #add8e6, #ffdde1);
      box-shadow: 0 4px 8px rgba(0,0,0,0.1);
      transition: transform 0.3s;
    }
  
    .small-card:hover {
      transform: scale(1.05);
    }
  
    /* Footer */
    .footer {
      background-color: #7b97b3;
      color: white;
      padding: 20px;
      text-align: center;
      margin-top: 20px;
    }
  </style>
  
  <!-- Navbar com ícones -->
  <nav class="navbar navbar-expand-lg navbar-light bg-light">
    <a class="navbar-brand" href="#">Seu Guia de Doramas</a>
    <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNavDropdown" aria-controls="navbarNavDropdown" aria-expanded="false" aria-label="Alterna navegação">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNavDropdown">
      <ul class="navbar-nav">
        <li class="nav-item active">
          <a class="nav-link" href="#">Home <span class="sr-only"></span></a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Destaques</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Links

          </a>
        </li>
        <li class="nav-item dropdown">
          <a class="nav-link dropdown-toggle" href="#" id="navbarDropdownMenuLink" role="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
            Link dropdown
          </a>
          <div class="dropdown-menu" aria-labelledby="navbarDropdownMenuLink">
            <a class="dropdown-item" href="#">Ação</a>
            <a class="dropdown-item" href="#">Romances</a>
            <a class="dropdown-item" href="#">Suspense de Época</a>
          </div>
        </li>
      </ul>
    </div>
  </nav>
  Formulários
  
  <div class="container-fluid p-0">
    <!-- CAROUSEL -->
    <div id="mainCarousel" class="carousel slide" data-bs-ride="carousel">
      <!-- Indicadores do Carousel -->
      <div class="carousel-indicators">
        <button type="button" data-bs-target="#mainCarousel" data-bs-slide-to="0" class="active"></button>
        <button type="button" data-bs-target="#mainCarousel" data-bs-slide-to="1"></button>
      </div>
  
      <!-- Itens do Carousel -->
      <div class="carousel-inner">
        <div class="carousel-item active">
          <img src="/images.jfif" class="d-block w-100" alt="Imagem Dorama 1">
          <div class="carousel-caption d-none d-md-block">
            <h1 class="display-4">Seu guia de Dorama</h1>
          </div>
        </div>
        <div class="carousel-item">
          <img src="/dorama-.jpg" class="d-block w-100" alt="Imagem Dorama 2">
          <div class="carousel-caption d-none d-md-block">
            <h1 class="display-4">Seu guia de Dorama</h1>
          </div>
        </div>
      </div>
  
      <!-- Controles do Carousel -->
      <button class="carousel-control-prev" type="button" data-bs-target="#mainCarousel" data-bs-slide="prev">
        <span class="carousel-control-prev-icon"></span>
      </button>
      <button class="carousel-control-next" type="button" data-bs-target="#mainCarousel" data-bs-slide="next">
        <span class="carousel-control-next-icon"></span>
      </button>
    </div>
  
    <!-- CARDS DOS DORAMAS (4 EM UMA FILEIRA) -->
    <div class="container my-4">
      <div class="dorama-grid">
        <div class="card dorama-card">
          <img src="/dorama 1.jfif" alt="Dorama 1">
          <div class="card-body">
            <h5 class="card-title">: )</h5>
          </div>
        </div>
        <div class="card dorama-card">
          <img src="/dorama 2.jfif" alt="Dorama 2">
          <div class="card-body">
            <h5 class="card-title">: )</h5>
          </div>
        </div>
        <div class="card dorama-card">
          <img src="/dorama 3.jfif" alt="Dorama 3">
          <div class="card-body">
            <h5 class="card-title">: )</h5>
          </div>
        </div>
        <div class="card dorama-card">
          <img src="/download.jfif" alt="Dorama 4">
          <div class="card-body">
            <h5 class="card-title">: )</h5>
          </div>
        </div>
      </div>
    </div>
  
    <!-- CARDS PEQUENOS CENTRALIZADOS -->
    <div class="small-card-container">
      <div class="card small-card" on:click={goToPg2}>
        <div class="card-body">
          <h5 class="card-title">Seu guia completo</h5>
          <a class="btn btn-outline-dark">Acessar</a>
        </div>
      </div>
      <div class="card small-card">
        <div class="card-body">
          <h5 class="card-title">Lançados Recentemente</h5>
          <a href="#" class="btn btn-outline-dark">Ver Mais</a>
        </div>
      </div>
    </div>
  
    <!-- FOOTER -->
    <footer class="footer">
      <p>@Instagram: <a href="https://instagram.com" target="_blank" style="color: white;">@seuguia.Doramas</a></p>
      <p>Telefone: (11) 1234-5678</p>
      <p>Email: Dorameir@seuguia.com</p>
      <p><a href="https://www.exemplo.com" target="_blank" style="color: white;">Não Sabe Onde assistir os Doramas? Acesse Logo Abaixo. </a></p>
      <p><a href="https://www.netflix.com/br/">https://www.netflix.com/br/</a></p>
      <p><a href="https://www.viki.com/?locale=pt">https://www.viki.com/?locale=pt </a></p>
      <p><a href="https://wetv.vip/pt">https://wetv.vip/pt </a></p>
  </div>
  