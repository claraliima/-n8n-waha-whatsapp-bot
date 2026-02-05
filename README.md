n8n-waha-whatsapp-bot
------------------------

Este projeto implementa um agente de IA integrado ao WhatsApp, desenvolvido com n8n e Waha, com o objetivo de ajudar usuários a decidir qual presente dar para a Clara.

O agente conversa de forma interativa, faz perguntas simples e considera as respostas ao longo do diálogo. Para manter o contexto entre mensagens, o fluxo utiliza memória persistente com Redis, permitindo recomendações mais consistentes durante a conversa.

A automação explora, na prática, conceitos como IA aplicada a fluxos conversacionais, controle de eventos do WhatsApp e organização de automações no n8n. O projeto foi desenvolvido com foco em aprendizado e portfólio, servindo como um experimento real de integração entre automação e inteligência artificial.

 Principais componentes do fluxo
----------------------------------

- Webhook – Receber mensagem
  Recebe os eventos de mensagens do WhatsApp enviados pelo Waha via HTTP.

- Filtro – Ignorar mensagens de grupo
  Garante que o bot responda apenas mensagens de conversas individuais.

- Switch – Validar evento como mensagem
  Filtra os eventos recebidos, permitindo que apenas mensagens sigam para o processamento.

- Agente de IA + Redis
  Gera respostas utilizando um modelo de linguagem, mantendo o contexto da conversa por meio de memória persistente no Redis.

- WhatsApp – Marcar como visualizado / Enviar mensagem
  Marca a mensagem como visualizada e envia a resposta gerada pelo agente ao usuário.
