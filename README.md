<h1 align="center">Olá, eu sou Pedro! 👋</h1>

<p align="center">
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=white" alt="JavaScript">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/Java-007396?style=for-the-badge&logo=java&logoColor=white" alt="Java">
  <img src="https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=white" alt="React">
  <img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node-dot-js&logoColor=white" alt="Node.js">
  <img src="https://img.shields.io/badge/Spring%20Boot-6DB33F?style=for-the-badge&logo=spring-boot&logoColor=white" alt="Spring Boot">
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker">
  <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white" alt="Git">
</p>

<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=Pedro-Rcastro&show_icons=true&theme=radical" alt="GitHub Stats">
</div>

## 🚀 Tecnologias e Ferramentas

<table align="center">
  <tr>
    <td><strong>Linguagens</strong></td>
    <td>JavaScript, Python, Java</td>
  </tr>
  <tr>
    <td><strong>Frameworks</strong></td>
    <td>React, Node.js, Spring Boot</td>
  </tr>
  <tr>
    <td><strong>Ferramentas</strong></td>
    <td>Git, Docker, Jenkins</td>
  </tr>
</table>

## 🛠️ Projetos Recentes

- [**Projeto 1**](https://github.com/Pedro-Rcastro/projeto1) - Uma breve descrição do projeto 1.
- [**Projeto 2**](https://github.com/Pedro-Rcastro/projeto2) - Uma breve descrição do projeto 2.
- [**Projeto 3**](https://github.com/Pedro-Rcastro/projeto3) - Uma breve descrição do projeto 3.

## 📚 Estou Aprendendo

- **Linguagens:** Rust, Go
- **Ferramentas e Tecnologias:** Kubernetes, Terraform

## 🌍 Conecte-se Comigo

<p align="center">
  <a href="https://www.linkedin.com/in/seuusuario"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="mailto:seuemail@example.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>
</p>

## 🎥 Vídeo de Apresentação

Aqui está um vídeo de apresentação sobre mim e meus projetos:

<p align="center">
  <a href="https://www.youtube.com/watch?v=<VIDEO_ID>">
    <img src="https://img.youtube.com/vi/<VIDEO_ID>/0.jpg" alt="Watch the video">
  </a>
</p>

## ⚡ Curiosidades

- 😄 Pronouns: Ele/Dele
- 🌱 Fun fact: Adoro resolver quebra-cabeças e desafios de lógica.

---

<div align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=Pedro-Rcastro&theme=radical" alt="GitHub Streak">
  <br>
  <img src="https://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=Pedro-Rcastro&theme=radical" alt="GitHub Profile Summary">
</div>

## 🎮 Jogue um Joguinho

Você pode jogar um joguinho de blocos em movimento diretamente aqui:

<canvas id="gameCanvas" width="320" height="480"></canvas>

<script>
  const canvas = document.getElementById('gameCanvas');
  const context = canvas.getContext('2d');

  const game = {
    width: 320,
    height: 480,
    blockSize: 20,
    rows: 24,
    columns: 16,
    blocks: [],
    player: { x: 7, y: 0, color: 'blue' },
    interval: null,
    init: function() {
      for (let r = 0; r < this.rows; r++) {
        this.blocks[r] = [];
        for (let c = 0; c < this.columns; c++) {
          this.blocks[r][c] = null;
        }
      }
      this.interval = setInterval(this.update.bind(this), 1000 / 2);
    },
    draw: function() {
      context.clearRect(0, 0, this.width, this.height);
      for (let r = 0; r < this.rows; r++) {
        for (let c = 0; c < this.columns; c++) {
          if (this.blocks[r][c]) {
            context.fillStyle = this.blocks[r][c];
            context.fillRect(c * this.blockSize, r * this.blockSize, this.blockSize, this.blockSize);
          }
        }
      }
      context.fillStyle = this.player.color;
      context.fillRect(this.player.x * this.blockSize, this.player.y * this.blockSize, this.blockSize, this.blockSize);
    },
    update: function() {
      if (this.player.y < this.rows - 1 && !this.blocks[this.player.y + 1][this.player.x]) {
        this.player.y++;
      } else {
        this.blocks[this.player.y][this.player.x] = this.player.color;
        this.player = { x: 7, y: 0, color: 'blue' };
        if (this.blocks[0][7]) {
          clearInterval(this.interval);
          alert('Game Over');
        }
      }
      this.draw();
    },
    keyPress: function(event) {
      if (event.key === 'ArrowLeft' && this.player.x > 0 && !this.blocks[this.player.y][this.player.x - 1]) {
        this.player.x--;
      } else if (event.key === 'ArrowRight' && this.player.x < this.columns - 1 && !this.blocks[this.player.y][this.player.x + 1]) {
        this.player.x++;
      }
      this.draw();
    }
  };

  window.addEventListener('keydown', game.keyPress.bind(game));
  game.init();
</script>