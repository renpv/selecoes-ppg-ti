# Papers recentes — desenvolvimento de software (UECE PPGCC e UFC MDCC)

Levantamento em **2026-11-05**. Preferência: docentes das linhas de ES. Inclui **desenvolvimento / qualidade assistidos por IA**. Ordem: ler primeiro o bloco “IA + ES”, depois qualidade/teste/arquitetura.

Critério de inclusão: artigo com pelo menos um orientador potencial da [lista](docentes/orientadores-potenciais.md) (UECE: Paixão, Maia, Ismayle, Cortés, Freire; MDCC/GREat: Rossana, Lincoln, Valéria, Windson, Ticianne e colaborações cruzadas). Não é revisão sistemática da área mundial.

Estratégia: se entrar nos dois programas, a **opção é UECE**. O mesmo núcleo de leitura serve aos dois (GESAD e GREat já coautoram).

Títulos, resumos e leitura em português: [papers-es-uece-mdcc-pt.md](papers-es-uece-mdcc-pt.md).

---

## 1. IA assistindo engenharia de software (prioridade de leitura)

### Attentionsmelling: Using Large Language Models to Identify Code Smells

- **Onde:** SBES 2025 (CBSoft, Recife). Distinguished Paper.
- **Quem:** Anderson Gomes, Denis Sousa, **Paulo Maia**, **Matheus Paixão** (UECE).
- **O quê:** avalia GPT-4o para detectar Long Method, God Class e Feature Envy; o ganho veio sobretudo de **métricas de código no prompt**, não de hiperparâmetros (AUC 0,50 → 0,82).
- **Por que ler:** encaixa “técnicas e ferramentas” + IA. Núcleo GESAD, o mais alinhado à UECE.
- **Link:** https://sol.sbc.org.br/index.php/sbes/article/view/37005

### 404: Civility Not Found? Evaluating Small Language Models in Detecting Incivility in GitHub Conversations

- **Onde:** SBES 2025. Artefato premiado.
- **Quem:** Patrício, Eufrásio, Uchôa, **Lincoln Rocha** (UFC/MDCC), Coutinho, Pereira, **Matheus Paixão** (UECE), Garcia.
- **O quê:** SLMs para detectar incivilidade em conversas de GitHub (processo social do desenvolvimento).
- **Por que ler:** ponte UECE–MDCC; IA no fluxo de colaboração, não só no código.
- **Link:** anais SBES 2025, p. 304–314 — https://sol.sbc.org.br/index.php/sbes/issue/view/1572

### Automatic Identification of Machine Learning-Specific Code Smells

- **Onde:** SBES 2025.
- **Quem:** Hamfelt, Britto, **Lincoln Rocha**, Camilo Almendra (UFC/MDCC).
- **O quê:** code smells **específicos de código de ML** (qualidade de software em sistemas de IA).
- **Por que ler:** ES de sistemas que *contêm* ML — recorte GREat/Lincoln.
- **Link:** anais SBES 2025, p. 337–347.

### Evaluating Large Language Models on the Classification of Different Technical Debt Types in StackOverflow Discussions

- **Onde:** ISE (Intelligent Software Engineering) @ CBSoft 2025.
- **Quem:** Lucas Amaral, Eliakim Gama, **Matheus Paixão**, Lucas Almeida Aguiar (UECE).
- **O quê:** LLMs classificando tipos de dívida técnica em discussões do Stack Overflow.
- **Por que ler:** IA + qualidade; antecessor em ISE 2023 (abaixo).

### Benchmarking LLM Commit Message Generation through a Developer-centric Pairwise Preference Framework

- **Onde:** LLM4Code 2026 (workshop).
- **Quem:** Lucas Aguiar, Matheus Freitas, **Matheus Paixão**, Rafael Carmo.
- **O quê:** gerar mensagens de commit com LLM, avaliado pelo preferência de desenvolvedores.
- **Por que ler:** IA no fluxo git/code review — tema clássico do Paixão.
- **Fonte:** https://mhepaixao.github.io/homepage/

### AI Support for Test Debt Prevention / Testing Big Data Systems: A Multivocal Review and LLM-Driven Support Tool

- **Onde:** Escola CBSoft 2025 (trabalhos de alunos).
- **Quem:** Levi Almeida / Icaro de Oliveira com **Ismayle Santos** (UECE) e **Rossana Andrade** (UFC).
- **O quê:** IA para prevenir dívida de teste; LLM em teste de sistemas big data.
- **Por que ler:** colaboração explícita UECE–GREat em **teste + IA**.
- **Lista:** https://cbsoft.sbc.org.br/2025/escola/artigos/

### Machine Learning for the Identification and Classification of Technical Debt Types on StackOverflow Discussions

- **Onde:** ISE 2023 (Best Paper). Ainda útil como base.
- **Quem:** Eliakim Gama, **Mariela Cortés**, Adson Damasceno, **Matheus Paixão**.

---

## 2. Processo, revisão de código, clones, arquitetura

### An Exploratory Study on the Lifecycle of Code Clones during Code Review

- **Onde:** SBES 2025.
- **Quem:** Ítalo Uchôa, Denis Sousa, **Matheus Paixão**, Pedro Maia, Anderson Uchôa (UFC), Ragkhitwetsagul.
- **O quê:** o que acontece com clones ao longo do code review.
- **Link:** anais SBES 2025, p. 293–303.

### Code Clone Configuration as a Multi-Objective Search Problem

- **Onde:** ESEM 2024.
- **Quem:** Denis Sousa, **Matheus Paixão**, Ragkhitwetsagul, Italo Uchoa.
- **O quê:** configuração de clones como busca multiobjetivo (herança SBSE do Paixão).

### Behind the Intents: An In-depth Empirical Study on Software Refactoring in Modern Code Review

- **Onde:** MSR 2020 (clássico do grupo; ainda citado).
- **Quem:** **Matheus Paixão** et al.

---

## 3. Teste, qualidade, IoT, dívida técnica (GREat + Ismayle)

### A Guide-based Approach for IoT Interoperability Testing

- **Onde:** Journal of the Brazilian Computer Society, **2026**.
- **Quem:** Castelo Branco, **Valéria Lelli**, Freitas, Carvalho, Rodrigues (UFC/GREat).
- **O quê:** guia para testar interoperabilidade IoT (planejamento, casos, medidas, ferramentas).
- **Link:** https://journals-sol.sbc.org.br/index.php/jbcs/article/view/5473

### Systematic Mapping of Data Quality in the Public Sector / Quality Management in the Public Sector

- **Onde:** Simpósio Brasileiro de Qualidade de Software (SBQS) **2025**.
- **Quem:** **Valéria Lelli**, **Rossana Andrade**, **Ismayle Santos** (e coautores UFC/UECE).
- **O quê:** qualidade de dados e indicadores no setor público — qualidade de software/informação.

### Milestone: A Neural Network Based Framework to Continuous Monitoring and Evaluation of Performance in Self-Adaptive Systems

- **Onde:** ICEIS 2026.
- **Quem:** Belmondo Jr., **Rossana Andrade**, **Valéria Lelli**, Rainara Carvalho, Marcio Maia.
- **O quê:** monitoramento de sistemas autoadaptativos com redes neurais (ES + adaptação + IA).

### TestDCat 3.0: catalog of test debt subtypes and management activities

- **Onde:** Software Quality Journal, 2021 (base do trabalho recente de IA em test debt).
- **Quem:** Aragão, **Rossana**, **Ismayle**, Castro, **Valéria Lelli**, **Ticianne Darin**.

### Assessing Exception Handling Testing Practices in Open-source Libraries

- **Onde:** Empirical Software Engineering, 2021.
- **Quem:** Lima, **Lincoln Rocha**, Carla Bezerra, **Matheus Paixão**.
- **Por que ler:** de novo a ponte UFC–UECE em **teste**.

### The Role of Bug Report Evolution in Reliable Fixing Estimation

- **Onde:** Empirical Software Engineering, 2022.
- **Quem:** Vieira, Mattos, **Lincoln Rocha**, João Paulo Gomes, **Matheus Paixão**.

---

## 4. Ensino de ES e aspectos humanos (complementar)

### Flip for not flopping! Evaluating Gamified Flipped Classes in Software Engineering

- **Onde:** WEI 2025.
- **Quem:** Veras, Olivindo, **Windson Viana**, **Lincoln Rocha**.
- **O quê:** sala invertida + gamificação no ensino de ES.

### Towards Emotionally Intelligent Software Engineers (CHASE 2025)

- **Quem:** Araújo, Kalinowski, **Matheus Paixão**, Graziotin.

### What Characterizes a Software Leader? (EASE 2026)

- **Quem:** Coelho, Campos, Bezerra, **Matheus Paixão**, Araújo, **Sávio Freire** (colaborador UECE).

---

## Pacote mínimo (8 artigos)

Se o tempo for curto, nesta ordem:

1. Attentionsmelling (SBES 2025) — Maia + Paixão  
2. Code clones no code review (SBES 2025) — Paixão  
3. Civility / SLM no GitHub (SBES 2025) — Lincoln + Paixão  
4. ML-specific code smells (SBES 2025) — Lincoln  
5. IoT interoperability testing guide (JBCS 2026) — Valéria  
6. AI Support for Test Debt Prevention (CBSoft Escola 2025) — Ismayle + Rossana  
7. Exception handling testing (EMSE 2021) — Lincoln + Paixão  
8. Página do GESAD no CBSoft 2025 (contexto do grupo): https://www.uece.br/ppgcc/gesad-conquista-premiacao-e-tem-participacao-historica-no-cbsoft-2025/

Isso cobre UECE (prioridade) e MDCC sem mudar o eixo: **técnicas e ferramentas de qualidade, revisão e teste, com e sem IA**.
