<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Para Você 💞</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      height: 100vh;
      overflow: hidden;
      font-family: 'Poppins', sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      background: url('https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiBPHVoF5fgcgv-0T4EJTwNvrwDoGC_AR21yRnORLL9vkrhqwNvFwACmqgBlU3eTAs3TTrn0Mdqg7ir2Z_7J5OJgIHd4GY8ffGXGdHC6SUrofr4Xta55Sd9Bc3ycmxm_PgXopGz5tiCwrjg/s1600/tumblr_ou3d8ziJOp1vg5r8io1_500.gif') no-repeat center center/cover;
    }

    .overlay {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-color: rgba(0,0,0,0.4);
      z-index: 1;
    }

    .container {
      position: relative;
      z-index: 2;
      text-align: center;
      color: #fff;
      padding: 30px;
      max-width: 800px;
    }

    button {
      background-color: #ff7cb8;
      border: none;
      border-radius: 20px;
      padding: 15px 30px;
      font-size: 1.2em;
      color: white;
      cursor: pointer;
      box-shadow: 0 0 15px rgba(255,192,203,0.7);
      transition: all 0.3s ease;
    }

    button:hover {
      background-color: #ff559d;
      transform: scale(1.05);
    }

    .texto {
      display: none;
      font-size: 1.1em;
      line-height: 1.6em;
      white-space: pre-line;
      background-color: rgba(0,0,0,0.6);
      padding: 25px;
      border-radius: 15px;
      box-shadow: 0 0 20px rgba(255,192,203,0.6);
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }

    .show {
      display: block;
      animation: fadeIn 1.5s ease forwards;
    }

    /* Pétalas caindo */
    .petala {
      position: absolute;
      top: -50px;
      width: 15px;
      height: 15px;
      background: pink;
      border-radius: 50%;
      opacity: 0.8;
      animation-name: cair;
      animation-iteration-count: infinite;
    }

    @keyframes cair {
      0% { transform: translateY(0) rotate(0deg); opacity: 0.8; }
      100% { transform: translateY(110vh) rotate(360deg); opacity: 0.2; }
    }

  </style>
</head>
<body>
  <div class="overlay"></div>
  <div class="container">
    <button id="botao">Clique aqui 💞</button>
    <div class="texto" id="texto">
Oi, agora são 20h34 do dia 21/10/2025.
Sou péssimo com isso, então me desculpa caso não fique do jeito que você gosta ou espera :')

Eu estava planejando te dar várias coisas, mas infelizmente meu orçamento não permitiu. Queria te dar aquele buquê grande ou a rosa encantada — não porque você quisesse ou curtisse essas coisas, mas porque você merece.

Esses tempos atrás eu estava conversando com uma menina do trabalho e a gente acabou falando sobre morte e tal... Aí fiquei me perguntando: se eu morresse hoje, quem ficaria horas do lado do meu caixão chorando?
Então comecei a pensar nas pessoas que eu conheço, e me veio você na cabeça.

Você foi a única que realmente me baqueou. Fiquei pensativo... Se você morresse hoje, eu não ia conseguir viver em paz nunca mais.

Pode parecer carência ou dependência emocional, mas não é.
É que, na minha vida agora, eu não consigo mais imaginar ela sem você.

Você é especial pra mim de um jeito que nem imagina.
Então, separei dois textos — nenhum dos dois é criação minha, mas eles são importantes pra mim do mesmo jeito que você é.

Eu já vivi sem você.
Já fui feliz antes de te conhecer, já tive bons momentos sem a sua presença.
Mas nada se compara ao que é ter você por perto.

Não é que eu precise de você pra viver, é que agora eu conheci a vida contigo — e qualquer coisa sem isso parece sem graça.

Eu já soube ser feliz sozinho,
mas agora quero ser feliz com você.
E, sinceramente, eu não consigo mais viver sem te ter.

Caso amanhã eu não esteja aqui, quero que cada sorriso que um dia tirei de você te faça levar um pedacinho da minha eternidade neste plano, perto de você.
Porque, caso amanhã eu não esteja aqui, quero que o tempo não apague o amor que um dia foi recíproco.
Porque, caso amanhã eu não esteja aqui, quero que você saiba que foi minha maior certeza em um mundo que só me apresentou dúvidas.
Caso amanhã eu não esteja aqui, saiba que meu espírito seguirá te protegendo e te guardando.
Porque, caso amanhã eu não esteja aqui, quero que você saiba que cada abraço que te dei era a minha maneira de dizer que você sempre foi meu porto seguro.
Caso amanhã eu já não esteja aqui, quero que você saiba que cada estrela no céu contém os sonhos e alegrias que desejo pra você — basta apenas olhar pro céu.
E, caso amanhã eu não esteja aqui, você vai estar em mim para todo o sempre.

Não é uma obra minha, mas desde que vi esse vídeo, toda vez choro e penso em mandar pra você.
Te amo, garota. Feliz aniversário 💞
    </div>
  </div>

  <!-- YouTube invisível -->
  <iframe id="youtubeAudio" width="0" height="0" src="https://www.youtube.com/watch?v=A_BLO50bRig" frameborder="0" allow="autoplay"></iframe>

  <script>
    const botao = document.getElementById('botao');
    const texto = document.getElementById('texto');

    botao.addEventListener('click', () => {
      texto.classList.add('show');
      botao.style.display = 'none';
    });

    // Criar pétalas animadas
    for(let i=0;i<50;i++){
      let petala = document.createElement('div');
      petala.classList.add('petala');
      petala.style.left = Math.random() * window.innerWidth + 'px';
      petala.style.animationDuration = (5 + Math.random()*5) + 's';
      petala.style.width = (10 + Math.random()*20) + 'px';
      petala.style.height = petala.style.width;
      document.body.appendChild(petala);
    }
  </script>
</body>
</html>

