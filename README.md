# Agendador de barbearia

Uma plataforma completa de gerenciamento de agendamentos para barbearias.

## Visão geral

Barbearias que gerenciam agendamentos manualmente podem perder horários, criar conflitos de agendamento e deixar os clientes sem confirmação. O Barbershop Scheduler organiza esse fluxo de trabalho em um aplicativo para gerenciamento de clientes, barbeiros, serviços, agendamentos, listas de espera e notificações.

O projeto lida com o gerenciamento de agendamentos com validação de conflitos, rastreamento de clientes em lista de espera, confirmações por WhatsApp e relatórios que dão suporte às operações diárias da barbearia.

## Demonstração

Este projeto faz parte do meu portfólio:

https://lucaspwalter.github.io/portfolio/

## Características

- Agendamento de consultas com detecção de conflitos entre barbeiros, clientes e serviços.
- Lista de espera para clientes que não conseguem encontrar um horário disponível.
- Mecanismo de notificação do WhatsApp usando API Evolution.
- Relatórios para rastreamento de compromissos, serviços e atividades na barbearia.

## Integração com WhatsApp

A integração do WhatsApp requer a instância da API Evolution do próprio usuário.

Documentação:

https://doc.evolution-api.com

Para testar:

- Crie um cliente com um número de telefone real.
- Crie um compromisso para esse cliente.
- Verifique o resultado em `/notifications` no frontend.

## Pilha de tecnologia

-Node.js
- Datilografado
- Fastificar
-PostgreSQL
-Knex
- Próximo.js

## Começando

Com o Docker instalado:

```bash
git clone https://github.com/lucaspwalter/barbershop-scheduler.git
cd barbershop-scheduler
docker compose up
```

Open `http://localhost:3000`. For sample data, keep the backend running and run `npm run seed` in another terminal.

As instruções manuais também estão disponíveis na página do portfólio do projeto:

https://lucaspwalter.github.io/portfolio/

## Estrutura do Projeto

```text
barbershop-scheduler/
├── frontend/
│   ├── app/
│   │   ├── notifications/
│   │   │   └── page.tsx
│   │   ├── globals.css
│   │   ├── layout.tsx
│   │   └── page.tsx
│   ├── public/
│   ├── next.config.mjs
│   ├── package.json
│   └── tsconfig.json
├── src/
│   ├── database/
│   │   ├── migrations/
│   │   ├── connection.ts
│   │   └── knex-config.ts
│   ├── errors/
│   │   └── app-error.ts
│   ├── lib/
│   │   └── evolution.ts
│   ├── modules/
│   │   ├── appointments/
│   │   ├── barbers/
│   │   ├── clients/
│   │   ├── notifications/
│   │   ├── queue/
│   │   ├── reports/
│   │   └── services/
│   └── index.ts
├── knexfile.ts
├── package.json
├── seed.ts
├── setup.ps1
├── setup.sh
└── tsconfig.json
```

## Licença

Licenciado sob a licença MIT. Veja `LICENÇA`.
