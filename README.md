# rachid-leads-poller

Robô que lê os leads novos do Meta (Lead Ads) e empurra pro webhook do CRM da Rachid.

Só isto. **Não** tem código do site, **não** tem dado de cliente, **não** tem senha no código
(o token do Meta fica em *Actions Secrets*, cifrado). É público só pra ter minutos de Actions
ilimitados e entregar os leads rápido.

- Lê de um IP que o Meta libera (o IP da Vercel é bloqueado pra listar leads).
- Janela de 3 dias + criação idempotente no CRM = nenhum lead se perde.
- Disparado a cada poucos minutos pelo cron da Vercel (workflow_dispatch); o `schedule` é só reserva.
