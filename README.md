<!DOCTYPE html>
<html>
<head>
  <style>
    .header-container {
      position: relative;
      width: 100%;
      max-width: 800px;
      margin: 0 auto;
    }
    .animated-text {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      color: white;
      font-size: 2rem;
      font-weight: bold;
      text-align: center;
      text-shadow: 2px 2px 8px #000;
      opacity: 0;
      transition: opacity 1.5s ease-in-out;
      width: 80%;
    }
    .active {
      opacity: 1;
    }
  </style>
</head>
<body>
  <div class="header-container">
    <img src="https://raw.githubusercontent.com/miromannino/Miro-D3-Animated-Headers/refs/heads/resources/tree.gif" 
         alt="Cabeçalho animado" 
         style="width: 100%; border-radius: 8px;"/>
    
    <div class="animated-text active" id="text1">Bem-vindo ao meu Git</div>
    <div class="animated-text" id="text2">Meu nome é João Pedro Portela</div>
    <div class="animated-text" id="text3">Formado em Relações Internacionais</div>
    <div class="animated-text" id="text4">Aprendendo Ciência de Dados</div>
  </div>

  <script>
    const texts = document.querySelectorAll('.animated-text');
    let current = 0;
    
    setInterval(() => {
      texts[current].classList.remove('active');
      current = (current + 1) % texts.length;
      texts[current].classList.add('active');
    }, 3000);
  </script>
</body>
</html>
