# funcionalidades.md — Catálogo de Funcionalidades do Portfólio

Este documento cataloga e classifica as funcionalidades existentes e planejadas do portfólio de **Allyson de Santana Almeida**, estruturadas por ordem de prioridade técnica e de experiência do usuário.

---

## 1. Prioridade 1: Funcionalidades Essenciais (Core / Alta Prioridade)

As funcionalidades de Prioridade 1 compõem o núcleo estrutural e narrativo do portfólio. São indispensáveis para transmitir a identidade acadêmica, técnica e pessoal com máxima fidelidade.

### 1.1. Apresentação Hero Cinematográfica (`#hero`)
- **Status:** Implementado.
- **Descrição:** Abertura visual de forte impacto com tipografia mascarada inspirada no estilo Simioni, selo de metadados geográficos (Campinas, SP), crachá de identificação de estudante de TI e iluminação difusa de estúdio.
- **Critérios de Aceite:** O nome emerge através de máscara vertical; a página oferece ação rápida para explorar os capítulos seguintes.

### 1.2. Capítulo 01: Identidade & Essência (`#about`)
- **Status:** Implementado.
- **Descrição:** Exposição clara de quem é o estudante, sua relação com o estudo como ferramenta analítica e seus pilares formativos no Colégio Raphael Di Santo e na região do Garcia.
- **Critérios de Aceite:** Disposição em grade editorial balanceada com destaques de postura, foco e instituição.

### 1.3. Capítulo 02: Linha do Tempo Escolar (`#trajectory`)
- **Status:** Implementado.
- **Descrição:** Timeline semântica estruturada com `<ol>`, marcos cronológicos de aprendizado e linha vertical progressiva que acompanha a rolagem da página.
- **Critérios de Aceite:** Cada marco possui marcador próprio e conteúdo legível; a linha avança sincronizada com a rolagem em dispositivos que não solicitem movimento reduzido.

### 1.4. Capítulo 03: Projetos & Prática de Engenharia (`#building`)
- **Status:** Implementado.
- **Descrição:** Apresentação aprofundada de sistemas reais com estética Blueprint de arquitetura:
  - Projeto principal: `trabiagustavo` (sistema de controle de estoque e ordens de serviço com Node.js, Express, Neon PostgreSQL, Drizzle ORM, Zod, testes Vitest e Playwright).
  - Projeto secundário: `lavtudo-profissional` (sistema com autenticação por cookies HTTP-only).
  - Pilares de engenharia: consolidação acadêmica, habilidades práticas e preparação para o mercado.
- **Critérios de Aceite:** Exibição de tags de tecnologias confirmadas, métricas reais de testes, links verificados para código no GitHub e demonstrações públicas funcionais na Vercel.

### 1.5. Capítulo 04: Perspectiva & Futuro (`#journey`)
- **Status:** Implementado.
- **Descrição:** Conclusão da narrativa reflexiva, consolidando a visão de longo prazo em Tecnologia da Informação, com caixa de síntese e botão nativo de retorno ao topo.
- **Critérios de Aceite:** Resumo biográfico consistente e transição para o rodapé editorial.

### 1.7. Barra de Progresso de Leitura (`#reading-progress`)
- **Status:** Implementado.
- **Descrição:** Barra fina fixada no topo da janela que indica a porcentagem exata de leitura percorrida no documento.
- **Critérios de Aceite:** Atualização suave via `transform: scaleX(...)` com atributos de acessibilidade (`role="progressbar"`, `aria-valuenow`).

### 1.8. Acessibilidade Universal e Movimento Reduzido
- **Status:** Implementado.
- **Descrição:** Conjunto de padrões acessíveis que inclui link de salto (`.skip-link`) para pular o cabeçalho, indicadores evidentes de foco (`:focus-visible`), contraste aprovado e respeito rigoroso à diretiva `@media (prefers-reduced-motion: reduce)`.
- **Critérios de Aceite:** Quando o usuário possui redução de movimento ativa, todas as transições e efeitos de parallax são desativados de imediato.

### 1.9. Responsividade Total
- **Status:** Implementado.
- **Descrição:** Layout fluido adaptável a telas ultrawide, notebooks, tablets e smartphones (breakpoints testados em 1024px, 768px e 480px) sem gerar rolagem horizontal indesejada.

---

## 2. Prioridade 2: Funcionalidades de Interação e Conexão (Média Prioridade)

Funcionalidades voltadas a estreitar o contato com visitantes, enriquecer o dinamismo visual e aprimorar a usabilidade cotidiana.

### 2.1. Formulário de Contato Integrado no Hero (`#contact`)
- **Status:** Implementado.
- **Descrição:** Canal direto de comunicação integrado ao card do Hero (substituindo o card de apresentação anterior), permitindo envio de mensagens com:
  - Nome completo (obrigatório, mínimo 2 caracteres).
  - E-mail (obrigatório, validação de formato regular).
  - Mensagem (obrigatória, mínimo 5 caracteres).
  - Botão de envio "Enviar mensagem" com hover azul e feedback de foco.
  - Validação estrita client-side com confirmação visual clara de validação, sem falsas afirmações de envio de backend.
- **Critérios de Aceite:** Rótulos acessíveis associados aos campos via `for`/`id`, mensagens de erro em tempo real com `role="alert"` e `aria-live="polite"`, estética alinhada à paleta Preto, Azul e Azul-Claro.

### 2.2. Cabeçalho Fixo com Observador de Seção Ativa
- **Status:** Implementado.
- **Descrição:** Menu de navegação superior (`.editorial-header`) com links de ancoragem suave que sincroniza automaticamente a classe `is-active` com o capítulo atualmente visível em tela através de `IntersectionObserver`.
- **Critérios de Aceite:** Destaque em amarelo-limão translúcido no link do capítulo corrente durante a rolagem.

### 2.3. Parallax de Estúdio Reativo ao Ponteiro
- **Status:** Implementado.
- **Descrição:** Efeito de profundidade no Hero onde as luzes e órbitas acompanham sutilmente o cursor em monitores desktop com mouse fino (`hover: hover` e `pointer: fine`).
- **Critérios de Aceite:** O movimento cessa e a animação é congelada assim que o cursor para ou sai da área do Hero, economizando ciclos de processamento.

---

## 3. Prioridade 3: Refinamentos e Evoluções Futuras (Baixa Prioridade)

Funcionalidades de expansão que agregam valor a longo prazo à medida que o portfólio avança.

### 3.1. Expansão do Catálogo de Projetos
- **Status:** Planejado.
- **Descrição:** Adição de novos cartões de projetos conforme novos sistemas em banco de dados, APIs REST ou microsserviços forem desenvolvidos no percurso escolar e técnico.

### 3.2. Internacionalização (Suporte a Inglês)
- **Status:** Planejado.
- **Descrição:** Alternador sutil no cabeçalho permitindo leitura em Inglês (EN) para prospecção internacional e avaliação em repositórios globais.

### 3.3. Tema de Alto Contraste Editorial
- **Status:** Planejado.
- **Descrição:** Opção de visualização monocromática de altíssimo contraste ou modo para impressão formal em PDF para envio com currículos acadêmicos.

### 3.4. Monitoramento Contínuo de Web Vitals
- **Status:** Em acompanhamento.
- **Descrição:** Auditorias periódicas do Google Lighthouse visando manter pontuações de 100/100 em Desempenho, Acessibilidade, Boas Práticas e SEO.
