# identidade.md — Identidade Visual, Tipografia, Tom de Voz e Biografia

Este documento formaliza as diretrizes de identidade da marca pessoal de **Allyson de Santana Almeida**, abrangendo sua paleta cromática, tipografia, tom de voz editorial e histórico biográfico consolidado no projeto.

---

## 1. Informações Pessoais e Biográficas Oficiais

Todas as informações textuais apresentadas no portfólio fundamentam-se em dados autênticos e confirmados:

- **Nome Completo:** Allyson de Santana Almeida
- **Monograma Oficial:** `ASA`
- **Área de Atuação e Estudo:** Tecnologia da Informação
- **Instituição de Ensino:** Colégio Raphael Di Santo (estudante desde o 6º ano do Ensino Fundamental)
- **Localidade de Origem:** Campinas, São Paulo, Brasil
  - *Contexto Formativo:* Região do Garcia como marco de desenvolvimento pessoal e geográfico
- **Valores Formativos:** Curiosidade investigativa, raciocínio analítico, disciplina metódica de estudos, ética técnica e respeito ao processo de amadurecimento intelectual.
- **Projetos em Destaque:**
  - `trabiagustavo`: Sistema web full-stack de controle de estoque e ordens de serviço (Node.js, Express, PostgreSQL Neon, Drizzle ORM, Zod, Vitest e Playwright).
  - `lavtudo-profissional`: Aplicação web para gestão de lavanderia com autenticação segura via cookies HTTP-only.
- **Repositório GitHub:** `28851-debug`

---

## 2. Paleta Cromática e Tokens do Sistema

A paleta combina a profundidade cinematográfica do preto absoluto com o impacto do azul vibrante e a leveza do azul-claro em contraste editorial refinado:

### 2.1. Preto & Tons de Contraste Profundo
- **Preto Obsidiana Profundo (`--bg-deep`):** `#07090e`  
  *Uso:* Fundo base da página, do hero e de áreas de contraste absoluto.
- **Preto Grafite Suave (`--bg-surface`):** `#0c1017`  
  *Uso:* Alternância de seções narrativas para ritmo visual e leitura confortável.
- **Carvão Azul Petróleo (`--bg-card`):** `#101622`  
  *Uso:* Estrutura de cartões, formulário de contato no Hero, pilares e caixas informativas.
- **Azul Petróleo Escuro (`--bg-card-alt`):** `#141c2c`  
  *Uso:* Painéis internos de especificações técnicas e blueprints de engenharia.

### 2.2. Azul (Interatividade, Botões e Links)
- **Azul Primário Interativo (`--blue-primary`):** `#2563eb`  
  *Uso:* Botões principais de envio (`.btn-submit`), botão de retorno ao topo, botões de ação e links destacados.
- **Azul de Hover (`--blue-hover`):** `#1d4ed8`  
  *Uso:* Estado de hover e foco ativo para botões interativos.
- **Azul Escuro Ativo (`--blue-active`):** `#1e40af`  
  *Uso:* Feedback ao clique (`:active`).

### 2.3. Azul-Claro (Destaques Suaves e Leveza Gráfica)
- **Azul Celeste Editorial (`--blue-light` / `--accent`):** `#38bdf8`  
  *Uso:* Glifos (`✦`), números de capítulos, marcadores da timeline, réguas animadas, indicadores de foco e tags.
- **Azul-Claro Translúcido (`--blue-light-dim`):** `rgba(56, 189, 248, 0.12)`  
  *Uso:* Fundo de badges sutis, links ativos no menu e halo de foco em inputs.
- **Glow Atmosférico (`--blue-light-glow`):** `rgba(56, 189, 248, 0.28)`  
  *Uso:* Brilho suave nos spots de iluminação atmosférica de estúdio.

### 2.4. Tipografia & Legibilidade
- **Marfim Gélido Primário (`--text-primary`):** `#f8fafc`  
  *Uso:* Títulos, manchetes e textos de leitura principal de alto contraste.
- **Cinza Ardósia Secundário (`--text-secondary`):** `#94a3b8`  
  *Uso:* Subtítulos, introduções de seções e parágrafos de apoio.
- **Cinza Azulado Atenuado (`--text-muted`):** `#64748b`  
  *Uso:* Rótulos, metadados e placeholders de formulário.
- **Preto Puro sobre Fundos Claros (`--text-on-light`):** `#07090e`  
  *Uso:* Garantia de contraste AAA em elementos com fundo claro.

### 2.5. Linhas e Divisores
- **Borda Sutil (`--border-subtle`):** `rgba(255, 255, 255, 0.08)`
- **Borda Média (`--border-medium`):** `rgba(56, 189, 248, 0.18)`
- **Borda Ativa (`--border-active`):** `#38bdf8`

---

## 3. Tipografia Oficial

A tipografia do portfólio conjuga o impacto geométrico expressivo com a legibilidade editorial contemporânea:

1. **Fonte de Display e Títulos: `Syne`**
   - *Pesos Utilizados:* 700 (Bold) e 800 (Extra Bold).
   - *Aplicação:* Nome principal no Hero, títulos de capítulos (`.chapter-title`), numerações editoriais e monograma `ASA`.
   - *Estilo:* Espaçamento ligeiramente comprimido nos títulos grandes (`letter-spacing: -0.03em`) para solidez e peso editorial.

2. **Fonte de Leitura e Interface: `Plus Jakarta Sans`**
   - *Pesos Utilizados:* 400 (Regular), 500 (Medium), 600 (Semi-Bold) e 700 (Bold).
   - *Aplicação:* Parágrafos, listas de marcos, cartões de projetos, menus de navegação, botões e labels.
   - *Estilo:* Alta legibilidade em ecrãs de qualquer tamanho, com altura de x generosa e números desenhados para fácil escaneamento.

3. **Escala Tipográfica Responsiva com `clamp()`:**
   - Nome Hero: `clamp(2.8rem, 7.8vw, 7.2rem)`
   - Títulos de Capítulos: `clamp(2rem, 4.5vw, 3.8rem)`
   - Subtítulos e Leads: `clamp(1.1rem, 1.4vw, 1.35rem)`
   - Corpo de Texto: `clamp(0.95rem, 1.1vw, 1.08rem)`
   - Legendas e Selos: `0.72rem` com `letter-spacing: 0.08em` a `0.12em`

---

## 4. Tom de Voz e Personalidade Editorial

O tom de voz do portfólio diferencia-se intencionalmente do padrão comercial comum da internet:

- **Maduro e Centrado em Fundamentos:** não recorre a clichês de autoengrandecimento nem a modismos de marketing. A narrativa valoriza o estudo sério, a lógica matemática e os princípios duradouros da computação.
- **Narrativo e Reflexivo:** cada etapa do percurso escolar (desde o sexto ano) é tratada como um tijolo na construção da maturidade pessoal e profissional.
- **Técnico e Concreto:** as realizações são descritas com rigor de engenharia (persistência relacional, transações atômicas, testes automatizados, proteção contra concorrência), demonstrando apreço pela qualidade real do software.
- **Humilde e Aberto ao Aprendizado:** postura contínua de estudante em evolução, com clareza de propósito e respeito ao tempo que a consolidação técnica exige.
