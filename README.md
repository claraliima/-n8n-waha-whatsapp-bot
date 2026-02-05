# -n8n-waha-whatsapp-bot
## 🔧 Estrutura do Fluxo
O fluxo foi desenvolvido no n8n e é composto pelos seguintes nós principais:

### Webhook
Responsável por receber os eventos de mensagens do WhatsApp enviados pelo Waha.

### Switch Node
Utilizado para validar o tipo de evento recebido e garantir que apenas mensagens sejam processadas pelo fluxo.

### Send Seen
Marca a mensagem como visualizada no WhatsApp, melhorando a experiência do usuário final.

### AI Agent + Redis Memory
Responsável por gerar respostas utilizando um modelo de IA, mantendo o contexto da conversa através de memória persistente no Redis.

