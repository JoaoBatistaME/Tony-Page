
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Vakinha - Pelo Tony</title>
  <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="bg-gray-50 text-gray-800">
  <!-- Header -->
  <header class="bg-indigo-600 text-white">
    <div class="max-w-6xl mx-auto px-4 py-6 flex flex-col md:flex-row md:items-center md:justify-between">
      <h1 class="text-2xl font-bold">Vakinha Pelo Tony</h1>
      <a href="#doar" class="mt-3 md:mt-0 bg-white text-indigo-600 px-5 py-2 rounded-xl font-semibold shadow hover:bg-indigo-50 transition">Quero Ajudar</a>
    </div>
  </header>

  <!-- Hero -->
  <section class="max-w-6xl mx-auto px-4 py-12 grid md:grid-cols-2 gap-8 items-center">
    <div>
      <h2 class="text-3xl font-bold mb-4">Ajude o Tony a realizar esse sonho 🙏</h2>
      <p class="text-gray-600 mb-6">
        Estamos arrecadando fundos para apoiar o Tony. Qualquer valor faz diferença e ajuda a transformar essa história.
      </p>
      <a href="#doar" class="inline-block bg-indigo-600 text-white px-6 py-3 rounded-2xl font-semibold shadow hover:bg-indigo-700 transition">Contribuir Agora</a>
    </div>
    <div class="bg-white rounded-2xl shadow p-6">
      <p class="font-semibold mb-2">Meta: R$ 10.000,00</p>
      <div class="w-full bg-gray-200 rounded-full h-4 mb-2">
        <div id="progressBar" class="bg-indigo-600 h-4 rounded-full" style="width: 35%"></div>
      </div>
      <p class="text-sm text-gray-600">Arrecadado: <span id="valorArrecadado">R$ 3.500,00</span> (35%)</p>
    </div>
  </section>

  <!-- História -->
  <section class="max-w-6xl mx-auto px-4 py-8">
    <div class="bg-white rounded-2xl shadow p-8">
      <h3 class="text-2xl font-bold mb-4">A História do Tony</h3>
      <p class="text-gray-600 leading-relaxed">
        Tony sempre foi conhecido por ajudar quem estava ao seu redor. Mesmo com poucas condições, nunca deixou de estender a mão para amigos, familiares e vizinhos.
        <br><br>
        Nos últimos meses, porém, a vida trouxe um desafio inesperado. Uma situação difícil — que envolve saúde, trabalho e estabilidade financeira — colocou Tony e sua família em uma posição delicada. As despesas aumentaram, as oportunidades diminuíram, e o sonho de seguir em frente pareceu cada vez mais distante.
        <br><br>
        Esta vakinha nasceu para dar ao Tony a chance de recomeçar. Cada contribuição representa mais do que dinheiro: é esperança, solidariedade e a prova de que ninguém precisa enfrentar momentos difíceis sozinho.
        <br><br>
        Se você chegou até aqui, saiba que sua ajuda, por menor que pareça, pode mudar completamente essa história. Vamos juntos escrever um novo capítulo para o Tony.
      </p>
    </div>
  </section>

  <!-- Doação -->
  <section id="doar" class="max-w-6xl mx-auto px-4 py-10">
    <div class="bg-white rounded-2xl shadow p-8">
      <h3 class="text-2xl font-bold mb-6">Faça sua Doação 💖</h3>

      <div class="grid md:grid-cols-3 gap-4 mb-6">
        <button onclick="selecionarValor(10)" class="border rounded-xl py-3 font-semibold hover:bg-indigo-50">R$ 10</button>
        <button onclick="selecionarValor(30)" class="border rounded-xl py-3 font-semibold hover:bg-indigo-50">R$ 30</button>
        <button onclick="selecionarValor(50)" class="border rounded-xl py-3 font-semibold hover:bg-indigo-50">R$ 50</button>
      </div>

      <div class="mb-4">
        <label class="block text-sm font-semibold mb-1">Outro valor (R$)</label>
        <input id="valorInput" type="number" placeholder="Digite o valor" class="w-full border rounded-xl px-4 py-2 focus:outline-none focus:ring-2 focus:ring-indigo-500" />
      </div>

      <div class="bg-gray-100 rounded-xl p-4 mb-4">
        <p class="font-semibold">Chave PIX (exemplo)</p>
        <p class="text-sm text-gray-600 break-all">pelotony@pix.com.br</p>
      </div>

      <button onclick="simularDoacao()" class="w-full bg-indigo-600 text-white py-3 rounded-2xl font-semibold shadow hover:bg-indigo-700 transition">Confirmar Doação</button>
      <p id="mensagem" class="mt-4 text-green-600 font-semibold hidden">Obrigado pela sua contribuição! 🙌</p>
    </div>
  </section>

  <!-- Footer -->
  <footer class="bg-gray-900 text-gray-300">
    <div class="max-w-6xl mx-auto px-4 py-6 text-center text-sm">
      <p>© 2026 Vakinha Pelo Tony • Todos os direitos reservados</p>
    </div>
  </footer>

  <script>
    function selecionarValor(valor) {
      document.getElementById('valorInput').value = valor;
    }

    function simularDoacao() {
      const valor = parseFloat(document.getElementById('valorInput').value || 0);
      if (valor <= 0) {
        alert('Digite um valor válido!');
        return;
      }
      document.getElementById('mensagem').classList.remove('hidden');
    }
  </script>
</body>
</html>
