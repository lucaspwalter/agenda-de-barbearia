# Agenda de barbearia

Plataforma para clientes, barbeiros, serviços, agendamentos, lista de espera e notificações.

## Visão geral

Inclui validação de conflitos, lista de espera, Evolution API e relatórios operacionais.

## Funcionalidades

- Cadastro de clientes, barbeiros e serviços.
- Agendamento com validação de conflitos.
- Lista de espera, notificações e relatórios operacionais.

## Tecnologias

Node.js, TypeScript, Fastify, PostgreSQL, Knex e Next.js.

## Como executar

```bash
git clone https://github.com/lucaspwalter/agenda-de-barbearia.git
cd agenda-de-barbearia
docker compose up
```

Acesse `http://localhost:3000`.

## Estrutura do projeto

```text
src/                API Fastify e regras de negócio
frontend/           Interface Next.js
docker-compose.yml  Ambiente com PostgreSQL
```

## Licença

MIT. Consulte [LICENSE](LICENSE).
