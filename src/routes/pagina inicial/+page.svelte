<script>
    let email = "";
    let senha = "";
    let mensagem = "";
   
    function realizarLogin() {
     if (email && senha) {
      mensagem = "Login concluído!";
     } else {
      mensagem = "Preencha todos os campos!";
     }
    }
   </script>
   
   <style>
    /* Estilo da página */
    .container {
     display: flex;
     justify-content: center;
     align-items: center;
     height: 100vh;
     background-size: cover;
     background-position: center;
     animation: trocaImagem 10s infinite alternate;
    }
   
   
   
    /* Estilo do formulário */
    .login-box {
     background: rgba(255, 255, 255, 0.8);
     padding: 30px;
     border-radius: 10px;
     box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.3);
     text-align: center;
     width: 350px;
     position: relative;
    }
   
    /* Estilo dos inputs */
    input {
     font-family: 'Cursive', sans-serif;
     color: #add8e6;
    }
   
    .btn-custom {
     background-color: #add8e6;
     border: none;
     color: white;
    }
   
    /* Estilo do link pequeno */
    .link-pequeno {
     position: absolute;
     right: 10px;
     bottom: 10px;
     font-size: 12px;
     color: #007bff;
     text-decoration: none;
    }
   
    .link-pequeno:hover {
     text-decoration: underline;
    }
   
    /* Mensagem de login */
    .mensagem {
     margin-top: 10px;
     color: rgb(114, 237, 251);
     font-weight: bold;
    }
   </style>
   
   <div class="container">
    <div class="login-box">
     <h2 class="mb-4">Login</h2>
     <input class="form-control mb-3" type="email" bind:value={email} placeholder="Digite seu e-mail" />
     <input class="form-control mb-3" type="password" bind:value={senha} placeholder="Digite sua senha" />
     <button class="btn btn-custom w-100" on:click={realizarLogin}>Entrar</button>
     <p class="mensagem">{mensagem}</p>
    
    </div>
   </div>
   