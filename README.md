# ☕ Grão & Arte — Torrefação e Café Especial

> Landing page institucional e interativa para uma torrefação artesanal de cafés especiais, desenvolvida focando em semântica HTML5, arquitetura de CSS moderno, metodologia BEM, acessibilidade e responsividade fluida.

---

## 📌 Visão Geral e Objetivo do Projeto

O **Grão & Arte** é uma solução front-end para um cliente fictício do segmento de cafés especiais. A aplicação apresenta a marca a apreciadores de cafés e métodos artesanais, exibindo o catálogo de microlotes exclusivos, a explicação do processo de torra, os planos do clube de assinatura e uma seção interativa de perguntas frequentes (FAQ).

### Objetivos do Projeto:
* **Simulação de Ambiente Profissional:** Desenvolvimento autônomo com foco na entrega de código limpo, organizado e versionado de acordo com boas práticas.
* **Acessibilidade e Semântica:** Uso rigoroso de elementos do HTML5 semântico e componentes nativos acessíveis (`<details>` e `<summary>`).
* **Design System e Consistência Visual:** Implementação de tokens CSS com escala tipográfica relativa (`rem`) e suporte completo a breakpoints responsivos.

---

## 🛠️ Tecnologias e Conceitos Aplicados

### Tecnologias
* **HTML5 Semântico:** Estruturação limpa da interface utilizando tags como `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<details>`, `<summary>` e `<footer>`.
* **CSS3 Moderno:**
  * Uso de **Variáveis Globais (Custom Properties)** para Design System (cores, sombras, tipografia, transições).
  * Layout flexível com **Flexbox**.
  * Unidades relativas (`rem`, `%`, `vh`, `vw`) garantindo escalabilidade.
* **Google Fonts:** Importação e padronização das famílias `Merriweather` (títulos) e `Open Sans` (corpo e interface).
* **Git & GitHub:** Versionamento de código com histórico de commits frequentes e descritivos.

### Conceitos e Metodologias
* **Metodologia BEM (Block Element Modifier):** Padronização rigorosa da nomenclatura de classes e seletores CSS (ex: `.card`, `.card__title`, `.card--highlighted`).
* **Separação de Responsabilidades (RNF04):** Estilização 100% isolada em arquivos CSS externos, sem estilos inline ou blocos `<style>` internos.
* **Escala Relativa Baseada na Raiz (RNF06):** Ajuste proporcional do elemento `html` em porcentagem para resgate preciso do dimensionamento padrão de navegadores.
* **Navegação Suave (Scroll Behavior):** Transição fluida entre seções via menu superior fixo, mantendo recuo relativo para não cobrir títulos.
* **Integração com WhatsApp Web API:** Botão flutuante fixado (`position: fixed`) direcionando para atendimento direto com número institucional pré-configurado.

---

## 📁 Organização da Arquitetura de Arquivos

A estrutura de diretórios adota uma arquitetura limpa e modularizada, separando as responsabilidades de marcadores HTML, folhas de estilo e ativos visuais:

```text
grao-e-arte/
├── assets/
│   ├── css/
│   │   ├── variables.css   # Definição dos tokens do Design System (:root)
│   │   ├── reset.css       # Normalização de estilos padrão e box-sizing
│   │   ├── main.css        # Estilos gerais, tipografia base e layout
│   │   ├── components.css  # Estilização de componentes BEM (cards, botões, FAQ)
│   │   └── responsive.css  # Breakpoints e regras de mídia (@media)
│   └── images/             # Otimização de recursos visuais e favicons
├── index.html              # Estrutura principal da aplicação HTML5
└── README.md               # Documentação técnica do repositório
```

---

## 🚀 Instruções de Visualização e Execução

### Opção 1: Execução Local Directa

1. **Clonar o Repositório:**
   ```bash
   git clone https://github.com/seu-usuario/grao-e-arte.git
   ```
2. **Navegar até a pasta do projeto:**
   ```bash
   cd grao-e-arte
   ```
3. **Abrir no Navegador:**
   * Basta dar um duplo clique no arquivo `index.html` ou abrir através de seu navegador de preferência.

### Opção 2: Utilizando a Extensão Live Server (VS Code)

1. Abra a pasta do projeto no **Visual Studio Code**.
2. Certifique-se de ter a extensão **Live Server** instalada.
3. Clique com o botão direito sobre o arquivo `index.html` e selecione **"Open with Live Server"**.
4. O projeto será executado localmente em `http://127.0.0.1:5500`.

---

## 💡 Principais Desafios Técnicos e Aprendizados

* **Compensação do Header Fixo na Navegação Suave:**
  * *Desafio:* Ao clicar nos links do menu fixo topo, a rolagem suave acabava cobrindo a parte superior do título das seções.
  * *Solução:* Aplicação da propriedade CSS `scroll-margin-top` nas seções alvo do menu para ajustar a compensação da altura exata do `<header>`.
* **Implementação Rigorosa da Escala REM:**
  * *Desafio:* Converter e alinhar espaçamentos, bordas e fontes para a escala relativa sem quebrar a proporção do layout em resoluções menores.
  * *Solução:* Ajuste da escala no elemento `html { font-size: 62.5%; }` (para corresponder a `10px` na base) facilitando a conversão de `rem` com precisão.
* **Componentização Semântica do FAQ:**
  * *Desafio:* Criar um efeito expansível no FAQ sem dependência de JavaScript.
  * *Solução:* Utilização das tags nativas `<details>` e `<summary>` estilizadas com seletores CSS e animações suaves na abertura do conteúdo.
* **Manutenção da Metodologia BEM:**
  * *Desafio:* Evitar a especificidade exagerada nos seletores CSS e a repetição indesejada de classes.
  * *Solução:* Refatoração contínua da estrutura HTML e CSS, garantindo que blocos e elementos fossem independentes e reutilizáveis.

---

### 📄 Licença e Direitos

Projeto desenvolvido para fins educacionais simulando ambiente profissional.  
© 2026 **Grão & Arte**. Todos os direitos reservados.