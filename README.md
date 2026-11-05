# Monitoramento de Seleções — Mestrado e Doutorado em Desenvolvimento de Software

Repositório pessoal para acompanhar processos seletivos de pós-graduação (mestrado e doutorado) nas instituições **IFCE**, **UFC** e **UECE**, com foco em programas cujas linhas de pesquisa envolvam **desenvolvimento de software, engenharia de software, metodologias, arquitetura, ferramentas e soluções de software** — incluindo aplicações de Inteligência Artificial voltadas à construção de sistemas.

## 🎯 Objetivo

Centralizar, versionar e manter atualizadas as informações necessárias para:

- Identificar programas e linhas com maior aderência ao interesse em desenvolvimento de software;
- Acompanhar janelas de inscrição, editais e cronogramas;
- Catalogar docentes e projetos com potencial de orientação;
- Registrar o histórico de editais e resultados ao longo do tempo;
- Planejar as próximas ações de monitoramento.

## 📁 Estrutura do repositório

```text
selecoes-ppg-ti/
├── README.md                          ← este arquivo (painel geral)
├── templates/
│   ├── programa.md
│   ├── edital.md
│   └── docente.md
├── programas/                         ← cadastro estável de cada programa
│   ├── ifce-ppgcc.md
│   ├── ifce-ppget.md
│   ├── ufc-mdcc.md
│   ├── ufc-pcomp-quixada.md
│   ├── ufc-ppgeti.md
│   ├── uece-ppgcc.md
│   ├── uece-ifce-mpcomp.md
│   └── comparativo-uece-mdcc.md
├── editais/                           ← um arquivo por edital/oferta
│   └── AAAA-MM-programa.md
├── docentes/
│   └── orientadores-potenciais.md
├── temas-software.md                  ← filtro entra / borda / fora
├── ranking-candidatos.md              ← ordem de preferência para concorrer
├── papers-es-uece-mdcc.md             ← papers recentes (ES / IA)
├── papers-es-uece-mdcc-pt.md          ← títulos e resumos em português
└── poscomp.md                         ← POSCOMP 2026 e uso no MDCC
```


### Convenções

- **Arquivos de programa:** `instituicao-sigla.md` (minúsculas, hífen como separador).
- **Arquivos de edital:** `AAAA-MM-programa.md` — o prefixo com ano e mês mantém a ordenação cronológica automática.
- **Datas:** sempre no formato `AAAA-MM-DD`.
- **Status de edital:** `aguardando`, `aberto`, `em análise`, `encerrado`, `monitorar próxima turma`.
- **Aderência ao interesse:** escala de 1 a 5, sempre com justificativa curta.

## 📊 Painel de programas

| Instituição | Programa | Nível | Aderência | Janela histórica de seleção | Status atual |
| :--- | :--- | :--- | :---: | :--- | :--- |
| UFC | [PCOMP (Quixadá)](programas/ufc-pcomp-quixada.md) | Mestrado | ⭐⭐⭐⭐⭐ | Set–Out | `em análise` (Edital 01/2026) |
| IFCE | [PPGCC](programas/ifce-ppgcc.md) | Mestrado | ⭐⭐⭐⭐ | Nov e Mai/Jun | `aberto` (Edital 43/2026; inscrições até 2026-11-21) |
| UFC | [MDCC (Fortaleza)](programas/ufc-mdcc.md) | Mestrado/Doutorado | ⭐⭐⭐⭐ | Fluxo amplo (Dez–Jun) | `aguardando` (sem edital 2027.1 em 2026-11-04) |
| UECE | [PPGCC](programas/uece-ppgcc.md) | Mestrado/Doutorado | ⭐⭐⭐⭐ | Set e Dez/Jan | `monitorar próxima turma` |
| UECE/IFCE | [MPCOMP](programas/uece-ifce-mpcomp.md) | Mestrado profissional | ⭐⭐⭐ | Verificar | `monitorar próxima turma` (existência a confirmar) |
| IFCE | [PPGET](programas/ifce-ppget.md) | Mestrado | ⭐⭐ | Nov/Dez e Mai/Jun | `em análise` (Edital 39/2026) |
| UFC | [PPGETI](programas/ufc-ppgeti.md) | Mestrado/Doutorado | ⭐⭐ | Dez/Jan e Jun/Jul | `aberto` (Edital 06/2026; inscrições até 2026-11-13) |

> A escala de aderência e as justificativas detalhadas estão em cada arquivo da pasta `programas/`.
>
> Filtro de **temas de desenvolvimento de software / metodologias / técnicas** (o que entra, o que é borda e o que fica de fora): [temas-software.md](temas-software.md).
>
> Ranking de **onde concorrer** (2026-11-05): [ranking-candidatos.md](ranking-candidatos.md).
>
> Comparativo **UECE PPGCC × UFC MDCC** (recorte ES): [programas/comparativo-uece-mdcc.md](programas/comparativo-uece-mdcc.md).
>
> Papers recentes desses orientadores: [papers-es-uece-mdcc.md](papers-es-uece-mdcc.md) (traduções: [papers-es-uece-mdcc-pt.md](papers-es-uece-mdcc-pt.md)). POSCOMP: [poscomp.md](poscomp.md).

## 🗓️ Calendário de janelas de edital

Períodos típicos identificados no histórico recente — úteis para programar lembretes:

| Mês | Programas com janela histórica |
| :--- | :--- |
| **Setembro** | UFC PCOMP; UECE PPGCC |
| **Outubro** | UFC PCOMP (continuação) |
| **Novembro** | IFCE PPGCC; IFCE PPGET |
| **Dezembro** | UFC MDCC; UFC PPGETI; UECE PPGCC; IFCE PPGET |
| **Janeiro** | UFC MDCC; UFC PPGETI; UECE PPGCC |
| **Maio** | IFCE PPGCC; IFCE PPGET |
| **Junho** | IFCE PPGCC; IFCE PPGET; UFC MDCC; UFC PPGETI |
| **Julho** | UFC PPGETI (continuação) |

> ⚠️ Calendários variam a cada ano. Este quadro serve para **programar verificações**, não como garantia de datas.

## ✅ Próximas ações

- [x] Verificar página de seleção do **UFC PCOMP** (Edital 01/2026 em análise; ver [editais/2026-09-ufc-pcomp.md](editais/2026-09-ufc-pcomp.md)).
- [x] Verificar página de seleção do **UECE PPGCC** (ciclo 2026.1 encerrado; próxima janela histórica em set e dez/jan).
- [ ] Acompanhar resultado do **UFC PCOMP** 2027.1 até publicação no site do programa.
- [ ] **IFCE PPGCC:** inscrições do Edital 43/2026 até 2026-11-21; ler retificação da prova escrita (2026-10-29).
- [ ] **UFC PPGETI:** inscrições do Edital 06/2026 até 2026-11-13; homologação prevista em 2026-11-18.
- [ ] **IFCE PPGET:** resultado preliminar da análise em 2026-11-26; resultado final em 2026-12-10.
- [ ] Checagem semanal da página de processo seletivo do **UFC MDCC** até surgir o edital 2027.1.
- [ ] Confirmar se **UECE/IFCE MPCOMP** ainda existe e se abrirá turma no próximo ciclo.
- [x] Primeira carga de `docentes/orientadores-potenciais.md` (temas públicos; completar Lattes/contatos ao longo do ciclo).
- [ ] Revisar este README ao final de cada ciclo de editais.

## 🔄 Rotina de monitoramento sugerida

1. **Mensal (fixo):** abrir a página de processos seletivos de cada programa e conferir se há edital novo ou retificação.
2. **Nas janelas do calendário acima:** checagem semanal.
3. **Ao encontrar edital:** criar arquivo em `editais/`, preencher cronograma, atualizar status no painel e registrar a próxima ação.
4. **Após resultado:** atualizar o arquivo do edital com o desfecho e mover o status para `encerrado`.

## 🧭 Escopo e critérios de inclusão

Um programa entra neste repositório se atender a **pelo menos um** dos critérios:

- Possui linha de pesquisa explícita em **Engenharia de Software**, desenvolvimento de sistemas ou metodologias;
- Tem grupos/projetos que desenvolvem **software, ferramentas ou arquiteturas**;
- Aplica **IA ou outras técnicas computacionais à construção de sistemas ou soluções de software**.

Programas com foco exclusivo em áreas distantes (ex.: processamento de imagens sem relação com software, redes sem componente de desenvolvimento) são registrados apenas se houver um docente ou projeto específico que justifique a inclusão.

## 📌 Observações

- Este repositório é de **uso pessoal** e não substitui a leitura dos editais oficiais.
- Todas as informações devem ser conferidas na fonte primária (páginas oficiais dos programas) antes de qualquer decisão.
- Links, contatos e cronogramas mudam com frequência; a data da última verificação deve constar em cada arquivo.

## 🔗 Fontes principais

- IFCE — Portal de Seleções: https://portal.ifce.edu.br
- UFC — Pró-Reitoria de Pesquisa e Pós-Graduação: https://propeg.ufc.br
- UECE — Pró-Reitoria de Pós-Graduação: https://www.uece.br/propgpq

---

*Última atualização do README: 2026-11-04*
