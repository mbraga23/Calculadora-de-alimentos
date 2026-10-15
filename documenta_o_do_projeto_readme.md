# 🥗 NutriCalc BR — Calculadora Interativa de Dieta e Macronutrientes

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Tabela TACO](https://img.shields.io/badge/Base_de_Dados-Tabela_TACO-10b981?style=for-the-badge)
![License](https://img.shields.io/badge/Licença-MIT-blue?style=for-the-badge)

> **NutriCalc BR** é uma aplicação web interativa (*Single-File Application*) desenvolvida para o cálculo preciso de **Taxa Metabólica Basal (TMB)**, **Gasto Energético Total (GET)**, distribuição de **macronutrientes** e planejamento diário de refeições com base nos alimentos da **Tabela TACO (UNICAMP)** e suplementos populares no Brasil.

🔗 **Acesse a demonstração online (GitHub Pages):**  
👉 [**https://mbraga23.github.io/Calculadora-de-alimentos/**](https://mbraga23.github.io/Calculadora-de-alimentos/)

---

## ✨ Principais Funcionalidades

- **📊 Cálculo de Perfil e Gasto Energético:**
  - Estimativa da **TMB** utilizando a equação padrão-ouro de **Mifflin-St Jeor**.
  - Cálculo do **GET** com multiplicadores de nível de atividade física.
  - Atalhos rápidos para objetivos de **Cutting** ($-20\%$), **Manutenção** ($0\%$) e **Bulking** ($+15\%$), além de controle deslizante para ajuste fino entre $-35\%$ e $+30\%$.
- **⚖️ Divisão Flexível de Macronutrientes e Hidratação:**
  - Alternância em tempo real entre metas por **gramas por quilo corporal ($\text{g/kg}$)** ou **percentual calórico ($\%$)**.
  - Cálculo automático dos carboidratos restantes e da meta diária de **fibras alimentares**.
  - Calculadora de meta diária de água ($\text{ml/kg}$) com rastreador interativo de consumo ($+250\text{ ml}$ / $+500\text{ ml}$).
- **🎯 Painel Visual (Dashboard) & Alertas Inteligentes:**
  - Gráfico de rosca (*Donut Chart*) em SVG dinâmico exibindo a proporção real entre Proteínas, Carboidratos e Gorduras.
  - Barras de progresso comparando o **Consumido vs. Meta** em tempo real.
  - **Diagnóstico Nutricional Automático:** alertas técnicos que avisam se a proteína está abaixo da janela ótima de hipertrofia/preservação magra, se as gorduras estão abaixo do mínimo hormonal ou se há déficit de fibras.
- **🇧🇷 Base de Alimentos da Tabela TACO + Medidas Caseiras:**
  - Mais de 35 alimentos essenciais da dieta brasileira cadastrados (arroz branco/integral, feijão carioca/preto, peito de frango, patinho, tilápia, ovos, pão francês, cuscuz, tapioca, aveia, queijo minas, requeijão light, whey protein, pasta de amendoim, etc.).
  - Botões de atalho para porções e medidas caseiras (ex.: *1 escumadeira*, *1 concha média*, *1 pão francês*, *1 scoop*).
  - **Cadastro de Novos Alimentos:** modal integrado que salva os alimentos personalizados diretamente no `localStorage` do navegador.
- **🍱 Planejador de 5 Refeições & Presets com 1 Clique:**
  - Organização em **Café da Manhã**, **Almoço**, **Lanche da Tarde**, **Jantar** e **Pós-Treino / Ceia**.
  - 3 cardápios pré-configurados prontos para carregar e editar: *Dieta Brasileira Equilibrada*, *Cutting Alto em Proteína* e *Bulking Limpo*.
  - Exportação formatada do cardápio para a área de transferência (pronto para colar no WhatsApp ou bloco de notas).
  - Suporte nativo a **Modo Escuro (Dark Mode)** e **Modo Claro (Light Mode)**.

---

## 🧮 Metodologia e Fórmulas Utilizadas

### 1. Taxa Metabólica Basal (Equação de Mifflin-St Jeor)
Para homens:
$$\text{TMB} = (10 \times \text{peso em kg}) + (6.25 \times \text{altura em cm}) - (5 \times \text{idade em anos}) + 5$$

Para mulheres:
$$\text{TMB} = (10 \times \text{peso em kg}) + (6.25 \times \text{altura em cm}) - (5 \times \text{idade em anos}) - 161$$

### 2. Gasto Energético Total (GET) e Meta Calórica
$$\text{GET} = \text{TMB} \times \text{Fator de Atividade Física}$$

$$\text{Meta Calórica} = \text{GET} \times \left(1 + \frac{\text{Ajuste Percentual}}{100}\right)$$

### 3. Densidade Energética dos Macronutrientes
- **Proteínas:** $4\text{ kcal/g}$
- **Carboidratos:** $4\text{ kcal/g}$
- **Gorduras (Lipídios):** $9\text{ kcal/g}$
- **Fibras Alimentares (Meta):** recomendada em aproximadamente $14\text{ g}$ a cada $1000\text{ kcal}$ (ajustada entre $25\text{ g}$ e $40\text{ g/dia}$).

---

## 🚀 Como Executar o Projeto

Por ser construído em arquitetura **Single-File** (Zero-Dependency Build), você não precisa instalar Node.js, pacotes NPM ou compiladores.

### Rodando Localmente
1. Clone este repositório:
   ```bash
   git clone https://github.com/mbraga23/Calculadora-de-alimentos.git
   ```
2. Acesse a pasta do projeto:
   ```bash
   cd Calculadora-de-alimentos
   ```
3. Basta dar dois cliques no arquivo `index.html` para abri-lo em qualquer navegador moderno (Chrome, Edge, Firefox, Safari) ou utilizar a extensão *Live Server* no VS Code.

---

## 🛠️ Tecnologias Utilizadas

- **HTML5 Semântico**
- **Tailwind CSS (via CDN)** — Estilização responsiva, moderna e suporte a *Dark Mode*.
- **Vanilla JavaScript (ES6+)** — Motor reativo de cálculo nutricional, manipulação de DOM em tempo real e persistência via `localStorage`.
- **Font Awesome 6 & Google Fonts (Inter)** — Iconografia e tipografia de alta legibilidade.

---

## 📂 Estrutura do Repositório

```text
Calculadora-de-alimentos/
├── index.html   # Aplicação completa (Estrutura + Estilo + Lógica + Base TACO)
└── README.md    # Documentação do projeto
```

---

## 👤 Autor

Desenvolvido por **[Matheus Braga (@mbraga23)](https://github.com/mbraga23)**.

---

## 📄 Licença

Este projeto está sob a licença **MIT**. Sinta-se à vontade para usar, modificar e compartilhar!