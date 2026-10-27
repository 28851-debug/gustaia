# referencias.md — Inspirações, Referências e Estética Visual

Este documento detalha o repertório de referências visuais, conceituais e interativas que norteiam o portfólio pessoal e editorial de **Allyson de Santana Almeida**.

---

## 1. Referência Primordial: Estúdio Simioni

A principal referência de direção de arte, coreografia e iluminação do projeto advém do universo estético do **site Simioni**:

1. **Iluminação de Estúdio Fotográfico:**
   - Efeito de *spot glow* atmosférico posicionado estrategicamente no fundo (`.hero-spot-glow` e `.ambient-glow`).
   - Gradientes radiais extremamente difusos em tons de amarelo-limão translúcido (`rgba(212, 244, 52, 0.12)` até `transparent`), criando uma sensação de luz indireta de estúdio em contraluz sobre fundo escuro.

2. **Coreografia e Revelação Tipográfica com Máscaras:**
   - Títulos com revelação vertical mascarada (`.name-line-mask` e `.name-line`).
   - Em vez de um simples fade-in, o texto emerge de dentro de um recorte (*overflow: hidden*) com curvas cúbicas refinadas (`cubic-bezier(0.16, 1, 0.3, 1)`), simulando a abertura de créditos e vinhetas cinematográficas de alta produção.

3. **Parallax Suave e Profundidade ao Cursor (Desktop):**
   - Micro-movimento baseado na posição do ponteiro do mouse (`heroStage.addEventListener("mousemove")`), aplicando interpolação linear (LERP) sobre as luzes difusas e as órbitas decorativas, conferindo tridimensionalidade discreta sem interferir na estabilidade do texto legível.

---

## 2. Inspiração Editorial e Design Contemporâneo

Além da iluminação de estúdio, o projeto bebe da fonte do design editorial técnico contemporâneo e de plataformas de vanguarda (Awwwards, FWA):

1. **Estrutura por Capítulos Numerados:**
   - O portfólio organiza-se como uma narrativa estruturada em capítulos numerados (`01/05`, `02/05`, etc.).
   - Cabeçalhos acompanhados de *stamps* editoriais, etiquetas em caixa alta com espaçamento ampliado (`letter-spacing: 0.12em`) e réguas gráficas animadas (`.chapter-rule`).

2. **Identidade e Contexto Formativo:**
   - Referência explícita à localidade de nascimento e formação (Campinas, SP e região do Garcia), conferindo autenticidade, raiz e senso de lugar.

3. **Apresentação Blueprint de Engenharia:**
   - Para a vitrine de projetos (como o *trabiagustavo* e o *lavtudo-profissional*), a referência visual afasta-se de mockups genéricos de smartphones e adota a estética de **Blueprint de Arquitetura de Software**:
     - Painéis com dots decorativos de terminal.
     - Diagramas de fluxo de dados (Frontend ➔ API ➔ Persistência).
     - Métricas auditáveis (quantidade de testes automatizados, cobertura de regras e categorias).

---

## 3. Elementos Visuais Que Devem Servir de Inspiração Contínua

Ao expandir ou criar novos componentes no site, devem ser mantidos os seguintes elementos característicos:

| Elemento Visual | Papel no Portfólio | Implementação de Referência |
| :--- | :--- | :--- |
| **Linhas Finas de Grid** | Demarcar o ritmo editorial | `.ambient-grid`, bordas com `rgba(255, 255, 255, 0.08)` |
| **Régua de Transição** | Marcar a transição de cenas/capítulos | Linha horizontal com gradiente de amarelo-limão para transparente que se expande via `scaleX` |
| **Linha do Tempo Contínua** | Simbolizar a continuidade escolar | Traço vertical sutil acompanhado de marcadores que se acendem ao entrar no campo visual |
| **Barra de Leitura Superior** | Guiar a progressão do visitante | Barra fina com indicador `scaleX` de 0 a 100% no topo da janela |
| **Badges de Status** | Indicar prontidão e contexto acadêmico | Pílula translúcida com ponto luminoso verde/limão pulsante |

---

## 4. Anti-Referências: O Que Jamais Deve Ser Feito

Para manter a integridade visual sofisticada do portfólio, é estritamente proibido:

- **Gradientes "Cyberpunk" ou "SaaS Clichê":** nada de gradientes roxo com azul ou rosa chiclete que descaracterizem o contraste Carvão/Amarelo-Limão.
- **Glassmorphism Exagerado:** evitar efeitos de vidro fosco com sombras brancas espessas e bordas brilhantes excessivas.
- **Cartões Flutuantes Desconectados:** não utilizar cartões genéricos sem hierarquia ou sem contexto com a linha editorial.
- **Animações Contínuas Sem Propósito:** evitar elementos girando indefinidamente ou textos piscando sem ação do usuário.
- **Tipografia Padrão do Sistema sem Hierarquia:** nunca desobedecer à dobradinha Syne / Plus Jakarta Sans.
