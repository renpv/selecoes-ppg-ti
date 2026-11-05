# Traduções (título + resumo + leitura em português)

Tradução dos artigos listados em [papers-es-uece-mdcc.md](papers-es-uece-mdcc.md). **Não é o texto integral:** os PDFs são protegidos por direitos autorais; o que segue é o **título em português**, o **resumo oficial traduzido** e uma **leitura objetiva** (método, resultado, por que importa para o pré-projeto).

Atualizado em **2026-11-05**. Termos técnicos comuns (code smell, LLM, SLM, code review, clone, prompt) ficam em inglês quando são o nome do conceito na literatura.

---

## 1. IA assistindo engenharia de software

### Attentionsmelling: usando grandes modelos de linguagem para identificar code smells

- **Original:** Attentionsmelling: Using Large Language Models to Identify Code Smells  
- **Onde / quem:** SBES 2025. Anderson Gomes, Denis Sousa, Paulo Maia, Matheus Paixão (UECE). Distinguished Paper.  
- **Link:** https://sol.sbc.org.br/index.php/sbes/article/view/37005 — DOI 10.5753/sbes.2025.9921

**Resumo (tradução).** LLMs estão se tornando ferramentas essenciais em engenharia de software, automatizando geração de código, testes unitários e revisão. O potencial para identificar *code smells* (indicadores de má qualidade) ainda é pouco explorado. Este estudo avalia a eficácia do GPT-4 em identificar três smells comuns (Long Method, God Class e Feature Envy) em quatro montagens experimentais: só código-fonte e definições; depois contexto extra, métricas e otimização de hiperparâmetros. Houve ganhos notáveis em todas as métricas ao enriquecer o prompt: cerca de 64% na curva ROC e 56% no F1. Os resultados destacam o impacto de métricas e ajuste de hiperparâmetros nos prompts, avançando a avaliação automatizada de qualidade.

**Leitura.** O salto de desempenho não veio “só de usar GPT”, e sim de **colocar métricas de código no prompt**. Isso é o recorte GESAD mais direto para um projeto UECE: ferramenta + IA + qualidade.

---

### 404: civilidade não encontrada? Avaliando modelos de linguagem pequenos na detecção de incivilidade em conversas do GitHub

- **Original:** 404: Civility Not Found? Evaluating the Effectiveness of Small Language Models in Detecting Incivility in GitHub Conversations  
- **Onde / quem:** SBES 2025. Patrício, Eufrásio, Uchôa, Lincoln Rocha (UFC), Coutinho, Pereira, Matheus Paixão (UECE), Garcia. Artefato premiado.  
- **Link:** https://sol.sbc.org.br/index.php/sbes/article/view/37008 — DOI 10.5753/sbes.2025.9933 — replicação: https://github.com/reset-ufc/slm-evaluation-incivility

**Resumo (tradução).** Incivilidade em plataformas OSS como o GitHub prejudica colaboração, desestimula contribuidores e pode afetar qualidade. Ferramentas de ML/NLP atuais falham em tipos sutis ou implícitos. **Objetivo:** avaliar SLMs na detecção grosseira (civil vs. incivil) e fina (tipos específicos) em issues e pull requests, e o efeito de estratégias de *prompt*. **Método:** dez SLMs (3B–14B parâmetros), cinco estratégias de prompt, mais de 6 mil conversas rotuladas; comparação com cinco modelos clássicos de ML. **Resultados:** SLMs detectam bem comentários civis; em incivis, o tamanho importa (9B+ melhor, p.ex. deepseek-r1, gpt-4o-mini). Na granularidade fina, *prompt* baseado em papel (role-based) foi o melhor, inclusive em ironia e zombaria. ML clássico ainda vai bem em ameaça e insulto explícitos. **Conclusão:** SLMs e prompts melhoram a moderação no desenvolvimento colaborativo.

**Leitura.** Ponte UECE–MDCC: IA no **processo social** (conversa de revisão), não só no código. Pacote de replicação no GitHub/Zenodo.

---

### Identificação automática de code smells específicos de aprendizado de máquina

- **Original:** Automatic Identification of Machine Learning-Specific Code Smells  
- **Onde / quem:** SBES 2025. Hamfelt, Britto, Lincoln Rocha, Camilo Almendra (UFC).  
- **Link:** https://sol.sbc.org.br/index.php/sbes/article/view/37011 — arXiv: https://arxiv.org/abs/2508.02541

**Resumo (tradução).** ML cresceu e virou crítico em várias indústrias, mas faltam ferramentas e estudos sobre smells **específicos** de aplicações de ML. O trabalho investiga métodos para projetar o **MLpylint**, analisador estático baseado em critérios desses smells. Usou Design Science: revisão da literatura para listar smells; depois revisão e especialistas para implementar a ferramenta. Avaliação em 160 aplicações ML open-source no GitHub e validação estática com 15 profissionais. Os resultados indicam eficácia e utilidade. Os autores pretendem integrar o MLpylint ao fluxo de desenvolvimento.

**Leitura.** Recorte Lincoln/MDCC: qualidade de **sistemas que contêm ML**, não “IA que analisa código qualquer”. Dívida técnica oculta em pipelines Python.

---

### Avaliando grandes modelos de linguagem na classificação de tipos de dívida técnica em discussões do Stack Overflow

- **Original:** Evaluating Large Language Models on the Classification of Different Technical Debt Types in Stack Overflow Discussions  
- **Onde / quem:** ISE 2025 (CBSoft). Lucas Amaral, Eliakim Gama, Matheus Paixão, Lucas Aguiar (UECE).  
- **Link:** https://sol.sbc.org.br/index.php/ise/article/view/36857 — DOI 10.5753/ise.2025.14868

**Resumo (tradução).** Dívida técnica (TD) são decisões subótimas com ganho de curto prazo e custo de manutenção. Gerir TD é crítico. Trabalhos anteriores com ML em dados do Stack Overflow tiveram desempenho limitado. Este estudo testa LLMs baseados em transformer (BERT, BART, GPT-2) para identificar e classificar tipos de TD em discussões do SO. Contribuições: pipeline reproduzível e comparação com estudos anteriores. LLMs chegam a 85% de F1 e 78,6% de F1 médio, superando resultados prévios em 8–23%.

**Leitura.** BART teve o melhor equilíbrio (F1 médio ~77,6%); BERT o maior *recall* (~92,4%). Melhor em dívida de testes e infraestrutura; pior em dívida de projeto (design). Continuação direta do ISE 2023 (abaixo). O GESAD já divulgou o título em português: “Avaliação de Grandes Modelos de Linguagem na Classificação de Diferentes Tipos de Dívida Técnica no Stack Overflow”.

---

### Avaliando a geração de mensagens de commit por LLM com um framework de preferência em pares centrado no desenvolvedor

- **Original:** Benchmarking LLM Commit Message Generation through a Developer-centric Pairwise Preference Framework  
- **Onde / quem:** LLM4Code 2026. Lucas Aguiar, Matheus Freitas, Matheus Paixão, Rafael Carmo.  
- **PDF do autor:** https://mhepaixao.github.io/homepage/files/llm4code26benchmarking.pdf — DOI 10.1145/3786181.3788728

**Resumo (tradução).** Mensagens de commit documentam a evolução e comunicam a equipe, mas escrever bem custa tempo. LLMs geram mensagens com bom desempenho aparente, porém o *benchmark* é frágil: mensagens “de desenvolvedor” nos datasets variam de qualidade, e BLEU/ROUGE (comparar com o texto humano) não capturam o que o desenvolvedor valoriza. Os autores propõem um framework **Elo** com comparações em pares. Compararam mensagens humanas e três geradores: OMG (LLM), FIRA (rede neural clássica) e NNGen (baseado em recuperação). **RQ1:** desalinhamento — desenvolvedores preferem o LLM; métricas clássicas preferem a rede neural. **RQ2:** OMG supera as mensagens humanas em detalhe; em alguns critérios, seria preferido mais de 80% das vezes. Conclusão: avaliação centrada no desenvolvedor é necessária para *benchmark* de LLMs em código.

**Leitura.** Argumento forte para pré-projeto: **como medir** ferramenta de IA no fluxo git, não só “gerar texto”.

---

### Apoio de IA à prevenção de dívida de teste / Teste de sistemas big data: revisão multivocal e ferramenta com LLM

- **Original:** AI Support for Test Debt Prevention; Testing Big Data Systems: A Multivocal Review and LLM-Driven Support Tool  
- **Onde / quem:** Escola CBSoft 2025 (pôsteres de alunos). Levi Almeida + Ismayle Santos (UECE) + Rossana Andrade (UFC); Ícaro de Oliveira + Ismayle + Rossana.  
- **Lista:** https://cbsoft.sbc.org.br/2025/escola/artigos/

**Leitura (não há resumo longo publicado na página da escola).** O primeiro parte de um catálogo de estratégias de **prevenção** de dívida de teste e usa IA para torná-las mais acessíveis no dia a dia. O segundo combina revisão multivocal de teste em sistemas big data com uma ferramenta apoiada por LLM. São trabalhos de formação, mas **assinados por Ismayle e Rossana** — a colaboração UECE–GREat em teste + IA.

---

### Aprendizado de máquina para identificar e classificar tipos de dívida técnica em discussões do Stack Overflow

- **Original:** Machine Learning for the Identification and Classification of Technical Debt Types on StackOverflow Discussions  
- **Onde / quem:** ISE 2023 (Best Paper). Eliakim Gama, Mariela Cortés, Adson Damasceno, Matheus Paixão (UECE).  
- **Link:** https://sol.sbc.org.br/index.php/ise/article/view/26119 — PDF: https://mhepaixao.github.io/homepage/files/ise23TDidentification.pdf

**Resumo (tradução).** Entender e gerir TD é crucial; ela aparece em plataformas de Q&A como o Stack Overflow. Análises manuais são caras e enviesadas. Os autores propõem identificação e classificação automáticas com ML e PLN: pré-processamento, PLN, algoritmos de ML e métricas. ML conseguiu recall de 85% em dívida de teste e precisão de 78% em dívida de projeto. Dataset e modelos pré-treinados foram disponibilizados.

**Leitura.** Baseline clássico do GESAD; o ISE 2025 troca ML tradicional por BERT/BART/GPT-2 no mesmo problema.

---

## 2. Processo, revisão de código, clones

### Estudo exploratório do ciclo de vida de clones de código durante a revisão

- **Original:** An Exploratory Study on the Lifecycle of Code Clones During Code Review  
- **Onde / quem:** SBES 2025. Ítalo Uchôa, Denis Sousa, Matheus Paixão, Pedro Maia, Anderson Uchôa, Ragkhitwetsagul.  
- **Link:** https://sol.sbc.org.br/index.php/sbes/article/view/37007 — DOI 10.5753/sbes.2025.9930

**Resumo (tradução).** Revisão moderna (MCR) é iterativa e assíncrona. Clones são trechos copiados, às vezes com pequenas mudanças; um defeito no clone exige ajuste em todos, o que pesa na manutenibilidade. Havia lacuna sobre clones **durante** a revisão. Com o dataset CROP (>28 mil revisões, >80 mil versões) e o detector Siamese, identificaram 27.656 clones relevantes em 6 sistemas. Amostra manual: Tipo I 46,74% e Tipo III 45,3%. Revisões classificadas em *Single* (clone numa só revisão, 224) e *Recurring* (várias versões, 1.258), com 236 na interseção. Métricas Duration e Distance: em média o clone entra no começo da revisão, **sobrevive** e é *merged*.

**Leitura.** Recurring: ciclo completo (~54%) é o mais comum; ~80% dos clones recorrentes entram no projeto final. Duração média 0,71; distância 0,17. A revisão **não** está “limpando” clones.

---

### Configuração de detecção de clones como problema de busca multiobjetivo

- **Original:** Code Clone Configuration as a Multi-Objective Search Problem  
- **Onde / quem:** ESEM 2024. Denis Sousa, Matheus Paixão, Ragkhitwetsagul, Ítalo Uchôa.  
- **DOI:** 10.1145/3674805.3690757

**Resumo (tradução).** Detectores *rank-based* (ex.: Siamese) lidam com corpora grandes (clones online), mas são sensíveis a parâmetros; otimizadores existentes não servem a esse tipo de ferramenta. Os autores definem *Multi-objective Code Clone Configuration*. Compararam 3 buscas-baseline e NSGA-II. NSGA-II foi o melhor; configurações otimizadas melhoraram 71,08% e 46,29% nas funções de *fitness* (MOP e MRR) frente ao default.

**Leitura.** Linhagem SBSE do Paixão: **como calibrar a ferramenta** de clones usada no paper do SBES 2025.

---

### Por trás das intenções: estudo empírico profundo de refatoração na revisão moderna de código

- **Original:** Behind the Intents: An In-depth Empirical Study on Software Refactoring in Modern Code Review  
- **Onde / quem:** MSR 2020. Matheus Paixão, Anderson Uchôa, Ana Carla Bibiano, Daniel Oliveira, Alessandro Garcia, Jens Krinke, Emilio Arvonio.  
- **PDF do autor:** https://mhepaixao.github.io/homepage/files/msr20intent.pdf

**Resumo (tradução).** Refatorações são centrais na revisão: o time preserva, revê, acrescenta ou desfaz refatorações nas versões da mudança, para garantir a intenção. Intenções vão de melhoria estrutural pura a facilitar feature ou correção. Havia pouca compreensão da prática **durante** a revisão. Mineraram 1.780 mudanças revisadas em 6 sistemas de duas comunidades OSS; classificaram intenções em 7 categorias. Observaram seleção, composição e evolução das refatorações ao longo da revisão e a relação com as intenções. Desenvolvedores aplicam sequências não triviais, cruzando vários trechos, para **uma** adição de feature. Novas intenções surgem no meio da revisão e mudam a composição. Dataset enriquecido foi disponibilizado.

**Leitura.** Clássico do grupo; ainda é a base conceitual de “o que acontece na revisão”.

---

## 3. Teste, qualidade, IoT, dívida técnica

### Uma abordagem baseada em guia para teste de interoperabilidade IoT

- **Original:** A Guide-based Approach for IoT Interoperability Testing  
- **Onde / quem:** JBCS 2026. Castelo Branco, Valéria Lelli, Freitas, Carvalho, Rodrigues (UFC/GREat).  
- **Link:** https://journals-sol.sbc.org.br/index.php/jbcs/article/view/5473

**Resumo (tradução).** A IoT amplia a Internet a objetos inteligentes que coletam e compartilham dados. Tráfego intenso e diversidade de interações geram desafio de **interoperabilidade** (sistemas distintos comunicarem com integridade). Teste de interoperabilidade avalia essa cooperação. Desafios: arquitetura em camadas, diversidade de protocolos, heterogeneidade de dispositivos. O artigo propõe um **guia** para sistematizar o teste, construído com revisões, extração e observação em ambientes reais. Cobre 12 tópicos (características IoT, casos abstratos, medidas, custo-benefício, ferramentas). Avaliação em três etapas: TAM (aceitação), experimento controlado em aplicação real, e especialistas. Resultados positivos em planejamento, execução e falhas específicas de IoT.

**Leitura.** Linha Valéria/Rossana: **guia de teste** como artefato de ES, não só paper empírico.

---

### Mapeamento sistemático de qualidade de dados no setor público: dimensões, métricas e práticas

- **Original:** Systematic Mapping of Data Quality in the Public Sector: Dimensions, Metrics and Practices  
- **Onde / quem:** SBQS 2025. Silva, Luna, Cavalcante, Valéria Lelli, Rossana Andrade, Monteiro (UFC), Ismayle Santos (UECE).  
- **Link:** https://sol.sbc.org.br/index.php/sbqs/article/view/39004

**Resumo (tradução).** Qualidade de dados é crítica para SI no setor público, mas ecossistemas fragmentados, legado e falta de avaliação padronizada atrapalham. Mapeamento de 53 estudos: dimensões e métricas mais usadas; técnicas de regras clássicas até ML para anomalia e imputação; barreiras (pouca automação, governança, recursos). Recomendações práticas, com vistas à Sefaz-CE.

**Leitura.** Qualidade de **informação/dados** no governo; Ismayle aparece como ponte UECE.

---

### Milestone: framework com rede neural para monitoramento contínuo e avaliação de desempenho em sistemas autoadaptativos

- **Original:** Milestone: A Neural Network Based Framework to Continuous Monitoring and Evaluation of Performance in Self-Adaptive Systems  
- **Onde / quem:** ICEIS 2026. Belmondo Jr., Rossana Andrade, Valéria Lelli, Rainara Carvalho, Nogueira, Marcio Maia (GREat/MDCC).  
- **Ficha:** https://www.insticc.org/node/TechnicalProgram/iceis/2026/presentationDetails/148383

**Resumo (tradução).** Sistemas autoadaptativos (SAS) monitoram, analisam, planejam e executam adaptações. O desafio é transformar requisitos não funcionais (sobretudo desempenho) em evidência em tempo de execução. Milestone troca avaliação frágil por regras por um componente com rede neural: sensores leves, classificação de estados de desempenho, apoio ao planejamento e reúso de conhecimento. Avaliação no Google 2019 Cluster Sample: ROC-AUC 0,86, loss 0,43; latência de planejamento < 1 s, taxa de sucesso 66,67%. Prova de conceito com SA-BSN (rede de sensores corporais autoadaptativa).

**Leitura.** ES + adaptação + IA no GREat; útil se o pré-projeto MDCC for monitoramento/qualidade em runtime.

---

### TestDCat 3.0: catálogo de subtipos de dívida de teste e atividades de gestão

- **Original:** TestDCat 3.0: catalog of test debt subtypes and management activities  
- **Onde / quem:** Software Quality Journal, 2021/2022. Aragão, Rossana, Ismayle, Castro, Valéria Lelli, Ticianne Darin.  
- **DOI:** 10.1007/s11219-020-09533-y — site: https://great-ufc.github.io/TestDCat/index.html

**Resumo (versão conferência ICTSS, mesma linha).** Quando prazo e recurso apertam, teste é o primeiro a ser cortado. Atividades abortadas com ganho de curto prazo são dívida técnica; no teste, **dívida de teste**. Soluções anteriores cobriam tipos pontuais, não o processo inteiro. O catálogo associa subtipos a atividades de gestão, com ações no modelo 5W1H, a partir de entrevistas com profissionais (projetos da indústria). Objetivo: apoiar a gestão da dívida durante o processo de teste.

**Leitura.** Base conceitual do pôster “AI Support for Test Debt Prevention” (2025).

---

### Avaliando práticas de teste de tratamento de exceções em bibliotecas open-source

- **Original:** Assessing Exception Handling Testing Practices in Open-source Libraries  
- **Onde / quem:** Empirical Software Engineering, 2021. Lima, Lincoln Rocha, Carla Bezerra, Matheus Paixão.  
- **arXiv:** https://arxiv.org/html/2105.00500

**Resumo (tradução).** Linguagens modernas separam tratamento de erro do código regular, mas os fluxos de exceção complicam a testabilidade. EH costuma ser negligenciado. Este estudo exploratório (i) mediu cobertura (instrução, ramo, método) do código de EH e (ii) mediu eficácia via mutação com operadores específicos de EH. 27 bibliotecas Java longevas. Instruções e ramos em `catch` e `throw` são **menos cobertos** (com significância) que o restante. Ainda assim, a maioria das suítes detectou mais de 70% das falhas injetadas; de 12.331 mutantes, 68% foram detectados. Ferramenta **XaviEH**.

**Leitura.** Ponte UFC–UECE em **teste empírico** de qualidade.

---

### O papel da evolução do relatório de bug na estimativa confiável de correção

- **Original:** The Role of Bug Report Evolution in Reliable Fixing Estimation  
- **Onde / quem:** Empirical Software Engineering, 2022. Vieira, Mattos, Lincoln Rocha, João Paulo Gomes, Matheus Paixão.  
- **DOI:** 10.1007/s10664-022-10213-7

**Resumo (tradução).** Relatórios de bug alimentam modelos de esforço, em geral treinados no **estado final** (já corrigido). Na prática, o agendamento ocorre perto da **abertura**, quando o relatório é mais pobre — a estimativa fica irreal. Os autores usam **todos os estados** do relatório (evolução) como instâncias. JIRA de dez projetos OSS; classificação com vários ML e balanceamento. Campos são atualizados com frequência. Melhor desempenho predizendo se a correção leva mais ou menos de cinco dias, sobretudo nas **versões iniciais** (o cenário real): F-measure 0,44–0,85, precisão 0,34–0,74, recall 0,62–0,99. Dataset público.

**Leitura.** Processo + ML sobre artefatos de manutenção; Lincoln + Paixão de novo.

---

## 4. Ensino de ES e aspectos humanos

### Flip para não flopar! Avaliando salas invertidas gamificadas em engenharia de software

- **Original:** Flip for not flopping! Evaluating Gamified Flipped Classes in Software Engineering  
- **Onde / quem:** WEI 2025. Veras, Olivindo, Windson Viana, Lincoln Rocha.  
- **Link:** https://sol.sbc.org.br/index.php/wei/article/view/36202

**Resumo (já em português no SOL).** O ensino de ES tem dificuldade em promover habilidades práticas. Experimento de oito meses, ensino híbrido, 111 estudantes (técnico e superior). Dois modelos de sala invertida — com e sem gamificação — em 18 aulas. Gamificação aumentou motivação e esforço (sobretudo no técnico) e o desenvolvimento de habilidades na graduação.

---

### Rumo a engenheiros de software emocionalmente inteligentes

- **Original:** Towards Emotionally Intelligent Software Engineers: Understanding Students' Self Perceptions After a Cooperative Learning Experience  
- **Onde / quem:** CHASE 2025. Araújo, Kalinowski, Matheus Paixão, Graziotin.

**Resumo (tradução).** Inteligência emocional (EI) afeta comunicação, conflito e estresse em ES; a formação ainda privilegia o técnico. Estudo de caso com 29 alunos em quatro squads, dois meses, PBL. Questionários, grupos focais, *brainwriting*. Alunos gerem melhor as próprias emoções do que interpretam as dos outros. Sem treino formal, criaram planejamento estruturado e rede de pares, ligados a produtividade e resolução de conflito.

---

### O que caracteriza um líder de software? Práticas a partir das mídias sociais de profissionais

- **Original:** What Characterizes a Software Leader? Identifying Leadership Practices from Practitioners' Social Media  
- **Onde / quem:** EASE 2026. Coelho, Campos, Bezerra, Matheus Paixão, Araújo, Sávio Freire.

**Resumo (tradução).** Liderança na literatura foca papéis formais e modelos ágeis; falta o que o profissional **relata**. Análise de conteúdo de 116 artigos em Dev.to: 103 práticas (recomendadas e desencorajadas) em cinco categorias (pessoas, processo, crescimento, comunicação, visão). Mais citadas no positivo: habilidades interpessoais, delegação, habilidades gerenciais. No negativo: microgerenciamento, padrões improdutivos de trabalho e de comunicação. Mapa conceitual: liderança associada mais a gestão e interpessoal do que a expertise técnica.

---

## Como usar na preparação

1. Ler em português **esta ficha**.  
2. Abrir o PDF original só para figuras, tabelas e seção de ameaças (entrevista/projeto citam isso).  
3. Pacote mínimo (mesma ordem do levantamento): Attentionsmelling → clones no review → civility/SLM → MLpylint → guia IoT → dívida de teste + IA → exception handling.

Textos integrais: SOL/SBC, páginas dos autores e arXiv (quando houver). Não substituir a leitura do original na hora de citar.
