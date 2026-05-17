## **`README.md`**

```markdown
# 🐩 Poodle - Análise Inteligente de Contratos com IA

[![React](https://img.shields.io/badge/React-18.2-61dafb)](https://reactjs.org/)
[![Vite](https://img.shields.io/badge/Vite-6.1-646cff)](https://vitejs.dev/)
[![TailwindCSS](https://img.shields.io/badge/TailwindCSS-3.4-38bdf8)](https://tailwindcss.com/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

## 🎯 Sobre o Projeto

**Poodle** é uma landing page institucional para uma plataforma SaaS que automatiza a análise de contratos jurídicos utilizando Inteligência Artificial. O site apresenta os serviços, planos e permite contato com a equipe comercial.

### ✨ Funcionalidades do Site

- 📄 **Landing page completa** com todas as seções
- 📞 **Formulário de contato** integrado com Formspree
- 🎨 **Design moderno e responsivo** (mobile-first)
- 🌙 **Tema escuro** com cores personalizadas
- 🎬 **Animações suaves** com Framer Motion
- 📱 **Menu mobile** responsivo

### 🎯 Seções do Site

| Seção | Descrição |
|-------|-----------|
| Hero | Título principal e call-to-action |
| Features | 6 funcionalidades principais |
| Como Funciona | Fluxo de 3 passos |
| Perfis de Clientes | 6 segmentos atendidos |
| Planos | Tabela de preços (Starter, Profissional, Enterprise) |
| CTA | Chamada final para ação |
| Contato | Formulário e informações de contato |
| Termos de Uso | Documento legal |

## 🚀 Demonstração

### Tecnologias Utilizadas

- **React 18** + Hooks
- **Vite** - Build tool ultrarrápida
- **React Router DOM** - Navegação entre páginas
- **TailwindCSS** - Estilização utility-first
- **Framer Motion** - Animações
- **Lucide React** - Ícones
- **Formspree** - Backend do formulário de contato

## 📁 Estrutura do Projeto

```
poodle-landing/
├── public/
│   └── manifest.json
├── src/
│   ├── api/
│   │   └── contactService.js      # Integração Formspree
│   ├── components/
│   │   ├── home/                  # Seções da landing
│   │   │   ├── HeroSection.jsx
│   │   │   ├── FeaturesSection.jsx
│   │   │   ├── HowItWorksSection.jsx
│   │   │   ├── ClientProfilesSection.jsx
│   │   │   ├── PricingSection.jsx
│   │   │   └── CtaSection.jsx
│   │   ├── layout/                # Layout principal
│   │   │   ├── SiteLayout.jsx
│   │   │   ├── Navbar.jsx
│   │   │   └── Footer.jsx
│   │   └── ui/                    # Componentes UI
│   │       ├── button.jsx
│   │       ├── input.jsx
│   │       ├── label.jsx
│   │       ├── textarea.jsx
│   │       ├── select.jsx
│   │       ├── badge.jsx
│   │       └── sheet.jsx
│   ├── lib/
│   │   ├── utils.js               # Função cn() para Tailwind
│   │   └── PageNotFound.jsx       # Página 404
│   ├── pages/
│   │   ├── Home.jsx               # Landing page
│   │   ├── Contact.jsx            # Página de contato
│   │   └── TermsOfUse.jsx         # Termos de uso
│   ├── App.jsx
│   ├── main.jsx
│   └── index.css
├── .env.example
├── .gitignore
├── index.html
├── package.json
├── postcss.config.js
├── tailwind.config.js
├── vite.config.js
└── README.md
```

## 🔧 Instalação e Execução

### Pré-requisitos
- Node.js 18+ ou 20+
- npm ou yarn

### Passos

```bash
# 1. Clone o repositório
git clone https://github.com/seu-usuario/poodle-landing.git
cd poodle-landing

# 2. Instale as dependências
npm install

# 3. Configure as variáveis de ambiente
cp .env.example .env.local
# Edite o arquivo com seu ID do Formspree (opcional)

# 4. Execute em desenvolvimento
npm run dev

# 5. Build para produção
npm run build

# 6. Preview do build
npm run preview
```

### Variáveis de Ambiente

```env
# Formspree (para o formulário de contato funcionar)
# Crie uma conta gratuita em https://formspree.io
VITE_FORMSPREE_ID=seu_id_aqui
```

> **Nota**: O formulário funciona mesmo sem configurar o Formspree (apenas simula o envio em desenvolvimento). Para produção, configure o ID.

## 🚢 Deploy

### GitHub Pages

```bash
# 1. Configure o base path no vite.config.js
# Adicione: base: '/nome-do-repositorio/'

# 2. Instale o gh-pages
npm install --save-dev gh-pages

# 3. Faça o deploy
npm run deploy
```

### Vercel

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/seu-usuario/poodle-landing)

### Netlify

[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/seu-usuario/poodle-landing)

## 📞 Formulário de Contato

O formulário envia os seguintes dados:

```javascript
{
  name: string,      // Nome completo
  email: string,     // E-mail
  phone: string,     // Telefone (opcional)
  company: string,   // Empresa (opcional)
  subject: string,   // Assunto (demo, pricing, support, partnership, other)
  message: string    // Mensagem
}
```

### Configurando o Formspree

1. Acesse [formspree.io](https://formspree.io)
2. Crie uma conta gratuita
3. Crie um novo formulário
4. Copie o ID do formulário (ex: `xyzabc123`)
5. Adicione no `.env.local`: `VITE_FORMSPREE_ID=xyzabc123`
6. Nas configurações do Formspree, adicione seu domínio aos "Allowed Domains"

## 🎨 Personalização

### Cores principais (edite em `src/index.css`)

```css
--primary: 220 90% 60%;     /* Azul #437ef7 */
--accent: 355 90% 65%;       /* Vermelho #f2545b */
--background: 228 47% 7%;    /* Azul escuro fundo */
--card: 228 42% 11%;         /* Cards */
```

### Conteúdo

- **Textos**: Edite diretamente nos componentes JSX
- **Planos e preços**: Altere no `PricingSection.jsx`
- **Funcionalidades**: Altere no `FeaturesSection.jsx`
- **Perfis de clientes**: Altere no `ClientProfilesSection.jsx`

## 📱 Responsividade

O site é totalmente responsivo:
- 📱 Mobile: < 640px
- 📟 Tablet: 640px - 1024px
- 💻 Desktop: > 1024px

## 📄 Licença

Este projeto está sob a licença MIT.

## 🤝 Suporte

- **Email**: contato@poodle.com.br
- **Site**: [poodle.com.br](https://poodle.com.br)

## 📝 Notas de Desenvolvimento

### Scripts Disponíveis

| Comando | Descrição |
|---------|-----------|
| `npm run dev` | Inicia servidor de desenvolvimento |
| `npm run build` | Gera build de produção |
| `npm run preview` | Visualiza build localmente |
| `npm run deploy` | Deploy no GitHub Pages |

### Dependências Principais

```json
{
  "react": "^18.2.0",
  "react-router-dom": "^6.26.0",
  "framer-motion": "^11.16.4",
  "tailwindcss": "^3.4.17",
  "lucide-react": "^0.475.0"
}
```

## 🗺️ Rotas

| Rota | Página |
|------|--------|
| `/` | Home (Landing page) |
| `/contato` | Contato |
| `/termos-de-uso` | Termos de Uso |
| `*` | 404 - Página não encontrada |

---

Desenvolvido com ❤️ por [Seu Nome] - [@seuinstagram](https://instagram.com/seuinstagram)
