# 📖 Manual do Sistema — MPB Conexão Humana

Plataforma de Desenvolvimento Contínuo e Gestão de Feedbacks sob a Identidade Estética da **Clear IT**.

**Link da Aplicação no Lovable:**
👉 [https://mpb-conexao-humana.lovable.app](https://mpb-conexao-humana.lovable.app)

---

## 1. Descrição do Sistema

O **MPB Conexão Humana** é uma ferramenta estratégica de gestão de pessoas projetada para aproximar líderes e colaboradores através de agendas periódicas de alinhamento contínuo (reuniões de 1:1) e ciclos de feedback bidirecional privado.

O principal objetivo da plataforma é remover a burocracia do registro pós-reunião, transformando notas rústicas e desabafos informais de liderança em relatórios estruturados no modelo de liderança **SBI (Situação, Comportamento e Impacto)** com suporte para planos de desenvolvimento individual (PDI).

Tudo isso opera sob uma camada rígida de moderação por Inteligência Artificial (local ou via API do Google Gemini), garantindo que agressões verbais sejam suavizadas e informações sensíveis de saúde mental ou física sejam higienizadas/anonimizadas, cumprindo estritamente a Lei Geral de Proteção de Dados (LGPD) e o respeito aos Direitos Humanos.

---

## 2. Principais Funcionalidades

A plataforma disponibiliza fluxos específicos e independentes baseados em três níveis de acesso (Líder, Liderado, RH):

### 2.1. Preparação Inteligente de 1:1
*   **Pautas por Cargo/Level:** O sistema identifica o nível técnico e comportamental do colaborador (L1, L2, L3) e injeta as competências comportamentais esperadas e pautas personalizadas voltadas ao desenvolvimento de carreira para direcionar o líder durante o encontro.

### 2.2. Fechamento Rápido e Questionário Dinâmico
*   **Questionário sem Atrito:** Composto por 5 perguntas binárias rápidas de Sim/Não, cujos enunciados mudam dinamicamente por sinônimos a cada carregamento para não tornar o processo repetitivo.
*   **Campos Livres Opcionais:** Campos textuais para justificar respostas negativas são totalmente opcionais e não possuem exigência de tamanho mínimo de caracteres, otimizando o tempo do gestor.

### 2.3. Inteligência Artificial de Moderação (Filtro SBI/LGPD)
*   **Conversão SBI:** Estrutura relatos brutos no modelo de alto impacto (*Situation-Behavior-Impact*).
*   **Travas de Compliance:** A IA remove automaticamente termos pejorativos, desabafos inadequados de liderança e neutraliza dados sensíveis de saúde (por exemplo, genericizando a palavra "depressão" para "desafios de saúde pessoal" e sugerindo amparo corporativo).

### 2.4. Assinatura Eletrônica e Exportação
*   **Validação por Token OTP:** Para garantir a autenticidade jurídica da ata de reunião, ambos assinam o termo na tela. O liderado recebe um código de verificação numérico simulado em tela/e-mail para finalizar.
*   **Exportação em PDF Filtrado:** Gera um relatório limpo em PDF contendo exclusivamente a análise SBI gerada pela IA e as assinaturas digitais, ocultando os dados binários ou notas informais do líder.
*   **Simulador de Inbox de E-mails:** Área integrada no rodapé que simula as notificações recebidas pelo colaborador com link para download do relatório.

### 2.5. Feedback Bidirecional Confidencial
*   **Ciclo de Avaliação Recíproca:** Permite que líder e liderado troquem avaliações periódicas em estrelas (1 a 5) com comentários textuais.
*   **Higienização Textual:** Os comentários passam pela mesma moderação da IA antes de serem arquivados, mantendo o tom construtivo.
*   **Privacidade:** Os textos são privados entre os envolvidos e acessíveis unicamente pelo RH na auditoria individual.

### 2.6. Dashboard Analítico de RH (People Analytics)
*   **Indicadores de Aderência:** Gráficos da cadência média de reuniões, controle de alertas de risco (colaboradores sem 1:1 há mais de 30 dias) e média acumulada de estrelas em feedbacks.
*   **Auditoria Singular por ID:** Permite ao RH selecionar colaboradores por IDs anonimizados (para preservar a LGPD) e visualizar todo o histórico estruturado de pautas, níveis de competência atingidos, PDIs e feedbacks bidirecionais higienizados.

---

## 3. O que ainda não está funcionando (Limitações do MVP / Simulados)

Sendo uma Prova de Conceito (PoC) autônoma e portátil executada 100% no navegador, certos serviços de infraestrutura centralizada operam como simulação:
1.  **Disparo de E-mails Reais:** O envio de e-mails de alerta e tokens OTP de assinatura digital é simulado internamente através da aba de "Simulador de Inbox" no rodapé da página.
2.  **API Gateway da IA em Produção:** Se nenhuma chave de API do Gemini for fornecida nas configurações do topo do app, o sistema recorre a um motor inteligente local de substituição de termos e estruturação SBI predefinida com delay de simulação de 2 segundos.
3.  **Persistência Relacional Corporativa:** Os dados e sessões residem no `localStorage` do navegador. A limpeza de dados do navegador apagará o banco de dados temporário.
4.  **Integração com ERP/Sólides:** Não há comunicação síncrona com sistemas de RH de terceiros.

---

## 4. Sugestões de Próximos Passos & Evoluções

*   **Persistência em Nuvem (Backend):** Implementação de banco de dados SQL (como PostgreSQL no Supabase) com criptografia em repouso dos logs de feedback.
*   **Autenticação Unificada (SSO):** Integração com Active Directory ou provedores de identidade corporativos (como Microsoft Azure ou Okta) via SAML2/OAuth2.
*   **Análise NLP de Clima Organizacional:** Treinar modelos de IA focados em análise de sentimentos agregada para detectar precocemente sinais de desengajamento generalizados ou exaustão (burnout) por setores, sem quebrar o anonimato individual dos colaboradores.

---

## 👥 Grupo e Integrantes

**Grupo:** Conexão Humana MPB
*   **João Pedro** — *Product Manager / Product Designer*
*   **Pedro** — *Lead Backend Engineer*
*   **Gustavo** — *Machine Learning / Prompt Engineer*
*   **Nathalia** — *Frontend Engineer*
*   **Mikael** — *QA & Compliance Engineer*
