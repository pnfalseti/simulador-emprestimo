# Simulador de Empréstimos DeFi (BTC)

Simulador de aportes mensais em Bitcoin combinado com empréstimo com garantia
(Aave / Ledn). Projeta preço do BTC, patrimônio, dívida e o LTV mês a mês,
indicando quando a posição seria liquidada.

## Funcionalidades

- Aporte mensal, PLR e aporte único, com projeção de valorização do BTC.
- Empréstimo com garantia (LTV alvo), uso de reserva e saque mensal.
- **Empréstimo em andamento (opcional):** informe a dívida atual (USDT) e a
  garantia atual (BTC); o LTV passa a considerar a posição vigente somada ao que
  for sendo pego emprestado mês a mês.
- **Ponto de liquidação configurável:** o LTV de liquidação é um campo editável.
- Validação das entradas com mensagens de erro.
- Tema claro/escuro, gráfico de dívida x patrimônio e salvamento local das
  simulações (localStorage).

## Como usar

Abra o arquivo [`index.html`](index.html) no navegador. Não há dependências de
build — apenas Chart.js carregado via CDN.

Atalho: `Ctrl + Enter` executa a simulação.

## Observações

- A dívida do empréstimo em andamento é informada em USDT e convertida para
  reais usando o câmbio informado (USDT ≈ USD).
- No modelo Aave, a garantia é o BTC travado no protocolo; no Ledn o colateral é
  reposto anualmente, então a garantia atual entra como reserva disponível.
- Projeção meramente ilustrativa — não é recomendação de investimento.
