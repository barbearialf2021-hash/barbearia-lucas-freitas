<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Barbearia Lucas Freitas</title>

<style>
body {
  margin: 0;
  font-family: Arial;
  background: #0f0f0f;
  color: #fff;
  text-align: center;
}

header {
  padding: 40px 20px;
}

.btn {
  background: #f1c40f;
  padding: 15px;
  display: inline-block;
  margin-top: 15px;
  color: #000;
  border: none;
  border-radius: 8px;
  font-weight: bold;
}

.section { padding: 30px; }

select, input {
  padding: 10px;
  margin: 10px;
  width: 80%;
  border-radius: 5px;
  border: none;
}
</style>
</head>

<body>

<header>
  <h1>Barbearia Lucas Freitas</h1>
  <p>Corte na régua, atendimento diferenciado</p>
</header>

<div class="section">
  <h2>Agendar horário</h2>

  <input type="text" id="nome" placeholder="Seu nome">

  <select id="servico">
    <option>Corte - R$30</option>
    <option>Barba - R$25</option>
    <option>Sobrancelha - R$5</option>
  </select>

  <select id="hora">
    <option>08:30</option>
    <option>10:00</option>
    <option>14:00</option>
    <option>16:00</option>
    <option>18:00</option>
  </select>

  <button class="btn" onclick="agendar()">Confirmar</button>
</div>

<script>
function agendar() {
  let nome = document.getElementById('nome').value;
  let servico = document.getElementById('servico').value;
  let hora = document.getElementById('hora').value;

  if(nome === "") {
    alert("Coloque seu nome!");
    return;
  }

  let msg = `Olá, meu nome é ${nome}. Quero agendar ${servico} às ${hora}.`;

  let url = `https://wa.me/5585986845280?text=${encodeURIComponent(msg)}`;

  window.open(url, '_blank');
}
</script>

</body>
</html>
