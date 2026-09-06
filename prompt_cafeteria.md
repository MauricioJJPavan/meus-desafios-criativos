# Desafio Criativo N8N - Automação de Atendimento para Cafeteria

Abaixo está o planejamento da automação e o prompt final para a criação do fluxo no N8N.

## Passo 1: Defina a automação desejada

Quero criar uma automação no N8N para **atendimento virtual de uma cafeteria (chatbot)**.

**Público ou responsável:**
Clientes (interação) e equipe de atendimento/gerência (acompanhamento).

**Resultado esperado:**
Responder dúvidas sobre o cardápio, registrar pedidos e agendar reservas de mesas ou do espaço completo, salvando as informações em uma planilha e notificando a equipe.

---

## Passo 2: Adicione contexto e regras

**Ferramentas envolvidas:**
WhatsApp, IA/OpenAI, Google Sheets e n8n.

**Fluxo desejado:**
1. Receber uma nova mensagem do cliente pelo WhatsApp.
2. Usar a IA para classificar a intenção (Dúvida/Cardápio, Fazer Pedido, Fazer Reserva).
3. Processar a intenção: consultar o cardápio para responder, coletar itens para o pedido ou coletar data/hora para a reserva.
4. Salvar os dados estruturados do pedido ou da reserva no Google Sheets.
5. Enviar uma mensagem de confirmação para o cliente.

**Regras importantes:**
- O tom de voz do bot deve ser acolhedor e educado.
- Para pedidos, sempre listar os itens e pedir a confirmação final do cliente antes de salvar.
- Para reservas de "espaço completo", informar ao cliente que a equipe entrará em contato para aprovação e pagamento de sinal.
- Caso a IA não entenda a solicitação, transferir para atendimento humano.

---

## Passo 3: Prompt Final

Você pode copiar o prompt abaixo e enviá-lo para uma Inteligência Artificial (como o ChatGPT ou Claude) para que ela detalhe exatamente como construir esse fluxo no N8N.

***

**Atue como um especialista em N8N.**

**Crie uma automação para:** 
Atendimento inteligente via chatbot para uma cafeteria.

**Público:** 
Clientes da cafeteria e equipe de gestão/atendimento.

**Ferramentas envolvidas:** 
WhatsApp (Trigger/Responder), Agent de IA/OpenAI (para interpretar linguagem natural e ler o cardápio), Google Sheets (para banco de dados) e n8n.

**Fluxo:** 
1. Receber mensagens do WhatsApp.
2. Roteamento Inteligente (IA): descobrir se o cliente quer ver o cardápio/tirar dúvidas, fazer um pedido ou realizar uma reserva (mesa ou espaço completo).
3. Se for Dúvida: Ler as informações do cardápio e responder com os produtos, valores e detalhes.
4. Se for Pedido: Coletar os itens desejados, calcular o total, salvar a nova linha no Google Sheets e enviar um recibo no WhatsApp.
5. Se for Reserva: Coletar data, horário, tipo de reserva e quantidade de pessoas, salvar no Google Sheets e enviar a confirmação no WhatsApp.

**Regras:** 
- O bot deve ser educado e utilizar um tom acolhedor.
- Nos pedidos, exija a confirmação dos itens pelo cliente antes de disparar o salvamento no Sheets.
- Nas reservas do espaço completo, adicione um aviso informando que a gerência entrará em contato para aprovar a reserva e combinar o sinal.
- Se o bot não conseguir processar o fluxo, ele deve enviar uma mensagem de transbordo para um atendente humano.

**Explique quais nós do N8N devem ser utilizados e a lógica de funcionamento do workflow passo a passo.**
