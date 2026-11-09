# Shepherd's Toolkit · Web

Front-end do **Shepherd's Toolkit**, uma plataforma de gestão para pastores e líderes de igreja. Reúne em um só painel membros, finanças, agenda, metas, Bíblia, planos de leitura, um editor de sermões e o **Caleb**, assistente de IA que conhece os escritos do usuário.

> API: [LucasPires-dev-shepherds-toolkit-api](https://github.com/LucasPires-dev/LucasPires-dev-shepherds-toolkit-api) · Integra com o [Koinonia](https://github.com/LucasPires-dev/koinonia-app)

## ✨ Funcionalidades

- **Dashboard** com visão geral da igreja e do pastor
- **Membros, finanças, metas e pedidos de oração**
- **Agenda** de eventos
- **Bíblia** com várias versões, notas por versículo e **planos de leitura**
- **Escritos**: editor rico (TipTap, com tabelas e alinhamento) e exportação para **Word (.docx)** e **PDF**
- **Biblioteca** com destaques
- **Caleb**, assistente de IA em painel lateral, com respostas baseadas nos escritos e anotações do usuário
- **Assinatura** do plano Pro via Stripe, com acompanhamento da cota de IA
- **Conexão com o Koinonia** para levar eventos e escritos ao WhatsApp
- **Tema claro e escuro**, rotas protegidas por login

## 🛠️ Stack

React 19 · TypeScript · Vite · Redux Toolkit · TanStack Query · TanStack Table · React Router · Material UI · Tailwind CSS · TipTap · Axios

## 🧠 Destaques técnicos

- **Modo demonstração**: com `VITE_USE_MOCK_DATA=true`, um *adapter* do Axios e um `baseQuery` mockado do RTK Query respondem com dados de exemplo. O app inteiro roda **sem backend**.
- **Estado em duas camadas**: Redux Toolkit para o estado de interface (módulos ativos, perfil, Bíblia) e TanStack Query para os dados do servidor.
- **Exportação no navegador**: escritos viram `.docx` e PDF sem passar pelo servidor.
- **Camada de serviços tipada**: cada domínio tem seu serviço e seus tipos (`src/services`, `src/types`).

## 🚀 Como rodar

```bash
npm install
cp .env.example .env
npm run dev
```

| Variável | Uso |
|---|---|
| `VITE_API_URL` | URL da API (ex.: `http://127.0.0.1:8000/api/`) |
| `VITE_USE_MOCK_DATA` | `true` para rodar com dados de exemplo, sem backend |

Outros scripts: `npm run build`, `npm run typecheck`, `npm run lint`.

## 📁 Estrutura

```
src/
  components/   # telas por módulo (Members, Finances, Writings, Caleb…)
  feature/      # slices do Redux
  services/     # chamadas à API por domínio
  mocks/        # dados e adapters do modo demonstração
  context/      # autenticação e tema
  types/
```

---

Desenvolvido por [Lucas C. Pires](https://github.com/LucasPires-dev) · Full-stack Python
