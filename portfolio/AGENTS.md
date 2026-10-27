# AGENTS.md — Regras, Arquitetura e Diretrizes para IA

Este documento estabelece as diretrizes técnicas, arquiteturais e comportamentais para agentes de inteligência artificial e desenvolvedores que operam ou prestam manutenção no repositório do portfólio pessoal e editorial de **Allyson de Santana Almeida**.

---

## 1. Visão Geral do Projeto

- **Titular:** Allyson de Santana Almeida (Monograma: `ASA`)
- **Perfil:** Estudante de Tecnologia da Informação no Colégio Raphael Di Santo (Campinas, SP)
- **Proposta:** Narrativa pessoal cinematográfica e portfólio técnico autoral, estruturado com foco em maturidade de engenharia, raciocínio lógico e solidez conceitual.
- **Estilo Visual:** Editorial cinematográfico com estética de iluminação de estúdio, paleta oficial em Preto (`#07090e`), Azul (`#2563eb`) e Azul-Claro (`#38bdf8`), tipografia expressiva e micro-interações refinadas.

---

## 2. Tecnologias Utilizadas

O projeto adota uma filosofia **Vanilla First** estrita, sem dependência de frameworks ou empacotadores pesados:

1. **HTML5 Semântico:**
   - Estrutura clara baseada em capítulos narrativos (`<section id="...">`, `<header>`, `<main>`, `<article>`, `<footer`, `<ol>`, `<nav>`).
   - Recursos completos de acessibilidade (WAI-ARIA, `role="progressbar"`, `aria-label`, `aria-hidden="true"`, skip-links).

2. **CSS3 Puro (Modern Vanilla CSS):**
   - Sistema de design fundamentado em variáveis CSS (`:root`).
   - Layouts modernos baseados exclusivamente em **CSS Grid** e **Flexbox**.
   - Tipografia e espaçamentos fluidos calculados com `clamp()`.
   - Suporte nativo e obrigatório à diretiva `@media (prefers-reduced-motion: reduce)`.
   - Sem frameworks de terceiros (sem Tailwind CSS, Bootstrap, Sass ou Less).

3. **JavaScript Puro (Vanilla ES6+):**
   - Execução estrita (`"use strict"`), sem poluição do escopo global.
   - Padrão **Progressive Enhancement**: a classe `js-ready` é injetada no elemento raiz apenas após a inicialização do script, assegurando que o conteúdo seja 100% legível caso o JavaScript esteja desativado.
   - Utilização de `IntersectionObserver` para revelações suaves de elementos e sincronização de links ativos no menu de navegação.
   - Performance de rolagem otimizada: **apenas um único listener de scroll** global com `{ passive: true }` gerenciado por `requestAnimationFrame`.
   - Interações táteis/desktop com LERP (Linear Interpolation) que entram em repouso automático sem loops contínuos.

4. **Tipografia & Ativos Gráficos:**
   - Fontes: **Syne** (pesos 700 e 800 para títulos e display) e **Plus Jakarta Sans** (pesos 400 a 700 para leitura e corpo).
   - Ícones e glifos em **SVG inline** de peso leve, sem pacotes de fontes de ícones externas.

---

## 3. Organização do Código e Estrutura de Pastas

```text
/
├── index.html            # Estrutura semântica completa e narrativa por capítulos
├── style.css             # Design tokens, reset, componentes, mídia e acessibilidade
├── script.js             # Lógica de interação, observadores e efeitos de profundidade
├── README.md             # Informações básicas do repositório
└── portfolio/            # Documentação estrutural e diretrizes do projeto
    ├── AGENTS.md         # Regras para agentes de IA e desenvolvedores (este arquivo)
    ├── referencias.md    # Referências estéticas, visuais e conceituais
    ├── identidade.md     # Identidade visual, tokens cromáticos, fontes e biografia
    └── funcionalidades.md# Catálogo e priorização de funcionalidades do portfólio
```

---

## 4. Regras e Restrições Mandatórias para Agentes de IA

Qualquer agente que realize alterações neste código deve seguir rigorosamente as regras abaixo:

### 4.1. Preservação Arquitetural e de Conteúdo
- **Não recriar o site do zero:** toda melhoria deve ser incremental e cirúrgica, respeitando os padrões de nomenclatura e a estrutura existente.
- **Não apagar capítulos existentes:** a narrativa é composta por capítulos cronológicos e conceituais que devem ser mantidos intactos (`#hero`, `#about`, `#trajectory`, `#building`, `#journey`).
- **Não instalar frameworks sem solicitação explícita:** não adicionar React, Vue, Tailwind, jQuery ou empacotadores quando a tarefa puder ser resolvida em HTML/CSS/JS nativo.

### 4.2. Integridade do Design e Estética
- **Respeitar a paleta oficial:** trabalhar exclusivamente com Preto (`#07090e`, `#0c1017`, `#101622`), Azul (`#2563eb`), Azul-Claro (`#38bdf8`) e Marfim Gélido (`#f8fafc`, `#94a3b8`).
- **Proibido cartões e gradientes genéricos:** não aplicar gradientes coloridos aleatórios (estilo roxo/azul clichê), sombras pesadas ou cartões com bordas arredondadas excessivas que quebrem a linguagem editorial sóbria.
- **Parallax apenas em elementos decorativos:** nunca aplicar deslocamentos de parallax em blocos de texto ou conteúdos legíveis; limitar o efeito às luzes atmosféricas e grades de fundo.

### 4.3. Performance e Listeners
- **Não duplicar listeners de rolagem:** qualquer cálculo dependente do scroll deve ser acoplado à função `updateScrollState` já existente em `script.js`, mantendo o padrão passivo e orquestrado por `requestAnimationFrame`.
- **Não criar loops infinitos de animação:** micro-interações disparadas por mouse ou eventos devem convergir para o repouso assim que o movimento do usuário cessar.

### 4.4. Acessibilidade (a11y)
- **Respeito absoluto a `prefers-reduced-motion`:** qualquer nova animação ou transição deve possuir supressão imediata na media query de redução de movimento.
- **Foco visível obrigatório:** todos os elementos clicáveis e interativos devem fornecer indicador de foco evidente (`:focus-visible`).
- **Navegação por teclado:** garanta ordem lógica de tabulação e uso de rótulos semânticos (`aria-label`, `<label for="...">`).

### 4.5. Formulários e Tratamento de Dados
- **Nunca simular envios falsos:** caso um formulário não possua backend ativo ou serviço de terceiros conectado, nunca exiba uma mensagem de "Mensagem enviada com sucesso" se os dados não tiverem sido verdadeiramente despachados.
- **Sem segredos no front-end:** nunca expor chaves privadas, tokens de API ou credenciais no código client-side.
- **Não inventar dados pessoais ou e-mails:** se for necessário um e-mail de destino para integrações e ele não estiver documentado no projeto, o agente deve solicitar a informação ao usuário antes de finalizar.
