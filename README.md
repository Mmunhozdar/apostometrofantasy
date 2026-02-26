# ⚽ Apostômetro Fantasy — Cartola FC 2026

Gerador de escalação com IA para o Cartola FC 2026. Conecta à API oficial do Cartola para buscar dados ao vivo de jogadores, preços, médias e confrontos.

![Next.js](https://img.shields.io/badge/Next.js-14-black?logo=next.js)
![Vercel](https://img.shields.io/badge/Deploy-Vercel-black?logo=vercel)
![Cartola FC](https://img.shields.io/badge/Cartola_FC-2026-green)

## ✨ Funcionalidades

- 🔌 **Integração com API do Cartola FC** — dados ao vivo de jogadores, preços e status do mercado
- 🔒 **Detecção de mercado fechado** — exibe tela dedicada com data/hora de reabertura
- 🧠 **Otimizador de escalação** — algoritmo greedy com 4 estratégias (Agressiva, Conservadora, Custo-Benefício, Equilibrada)
- ⚽ **Visualização em campo** — posicionamento real dos jogadores por posição
- 📊 **Análise detalhada** — preço, média, pontuação esperada, destaques e valorizações
- 🎨 **Interface chatbot** — UX inspirada no Apostômetro original
- 📱 **Responsivo** — funciona em desktop e mobile

## 🚀 Deploy no Vercel (mais fácil)

1. Suba o projeto no GitHub
2. Acesse [vercel.com](https://vercel.com) e faça login com sua conta GitHub
3. Clique em **"New Project"**
4. Selecione o repositório `apostometro-fantasy`
5. Clique em **"Deploy"** — pronto!

O Vercel detecta automaticamente que é um projeto Next.js.

## 💻 Rodar localmente

```bash
# Instalar dependências
npm install

# Rodar em desenvolvimento
npm run dev

# Acessar
open http://localhost:3000
```

## 📁 Estrutura

```
apostometro-fantasy/
├── src/
│   └── app/
│       ├── layout.js              # Layout + metadata/SEO
│       ├── globals.css            # Estilos globais + animações
│       ├── page.js                # Página principal
│       └── ApostometroFantasy.js  # Componente principal (client)
├── public/                        # Assets estáticos
├── next.config.js                 # Config do Next.js
├── package.json                   # Dependências
└── README.md
```

## 🔌 API do Cartola FC

A aplicação usa os seguintes endpoints públicos (sem autenticação):

| Endpoint | Descrição |
|----------|-----------|
| `/mercado/status` | Status do mercado (aberto/fechado), rodada atual, timestamp de fechamento |
| `/atletas/mercado` | Todos os jogadores com preço, média, status, variação, scouts |
| `/partidas` | Próximos jogos da rodada |

Base URLs tentadas: `api.cartola.globo.com` e `api.cartolafc.globo.com`

### Estados do mercado

| status_mercado | Estado | Comportamento |
|:-:|---|---|
| 1 | Aberto | App funciona normalmente, dados ao vivo |
| 2 | Fechado | Tela de mercado fechado com info de reabertura |
| 3+ | Manutenção | Tela de mercado fechado |

## 🎯 Formações disponíveis

3-4-3 · 3-5-2 · 4-3-3 · 4-4-2 · 4-5-1 · 5-3-2 · 5-4-1

## 📄 Licença

MIT
