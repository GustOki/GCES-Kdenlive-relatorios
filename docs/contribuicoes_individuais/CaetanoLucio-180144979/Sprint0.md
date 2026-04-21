# Diário de Bordo – Caetano Santos Lucio

**Disciplina:** Gestão da Configuração e Evolução de Software (GCES)  
**Equipe:** GCES 2026.1 – Kdenlive  
**Comunidade/Projeto de Software Livre:** [Kdenlive](https://invent.kde.org/multimedia/kdenlive)  
**Matrícula:** 180144979  
**GitHub:** [@caeslucio](https://github.com/caeslucio)  
**KDE Invent:** [@caeslucio](https://invent.kde.org/caeslucio)

---

## Sprint 0 – 01/04/2026 – 14/04/2026

### Resumo da Sprint

Sprint 0 foi dedicada inteiramente ao planejamento e à configuração do repositório de documentação do grupo para a disciplina GCES. A principal responsabilidade desta sprint foi criar do zero a infraestrutura de documentação do projeto, baseada no modelo utilizado pela turma anterior (GCES-OPPIA), porém adaptada para o novo projeto escolhido pela equipe: o **Kdenlive**, um editor de vídeo não-linear de código aberto mantido pela comunidade KDE.

O trabalho envolveu a adaptação de todos os guias de contribuição ao ecossistema real do Kdenlive (que usa o KDE GitLab — `invent.kde.org` — em vez do GitHub), a criação de materiais de apoio e a configuração do pipeline de CI/CD para publicação automática via GitHub Pages com MkDocs Material.

---

### Atividades Realizadas

| Data  | Atividade                                                    | Tipo   | Link/Referência                                                                                            | Status    |
| ----- | ------------------------------------------------------------ | ------ | ---------------------------------------------------------------------------------------------------------- | --------- |
| 13/04 | Análise do repositório modelo (GCES-OPPIA-relatorios)        | Estudo | [GCES-OPPIA-relatorios](https://github.com/LuizaMaluf/GCES-OPPIA-relatorios)                               | Concluído |
| 13/04 | Criação da estrutura de pastas do novo repositório           | Doc    | `GCES-Kdenlive-relatorios/`                                                                                | Concluído |
| 13/04 | Configuração do `mkdocs.yml`                                 | Doc    | [mkdocs.yml](https://github.com/caeslucio/GCES-Kdenlive-relatorios/blob/main/mkdocs.yml)                   | Concluído |
| 13/04 | Criação do `README.md` e `docs/index.md`                     | Doc    | [README.md](https://github.com/caeslucio/GCES-Kdenlive-relatorios/blob/main/README.md)                     | Concluído |
| 13/04 | Criação dos templates de diário de bordo e relatório         | Doc    | [materiais/](../../materiais/)                                                                             | Concluído |
| 13/04 | Workflow de deploy automático (GitHub Actions + MkDocs)      | Outro  | [deploy.yml](https://github.com/caeslucio/GCES-Kdenlive-relatorios/blob/main/.github/workflows/deploy.yml) | Concluído |
| 14/04 | Preenchimento da Sprint 0 com as atividades realizadas       | Doc    | [Sprint0.md](Sprint0.md)                                                                                   | Concluído |
| 14/04 | Pesquisa na documentação oficial de contribuição do Kdenlive | Estudo | [kdenlive.org/get-involved](https://kdenlive.org/get-involved/)                                            | Concluído |
| 14/04 | Pesquisa no repositório oficial do Kdenlive no KDE GitLab    | Estudo | [invent.kde.org/multimedia/kdenlive](https://invent.kde.org/multimedia/kdenlive)                           | Concluído |
| 14/04 | Escrita do guia "Como abrir um MR" com fluxo do KDE GitLab   | Doc    | [como-abrir-mr.md](../../materiais/como-abrir-mr.md)                                                       | Concluído |
| 14/04 | Escrita do guia "Regras para MRs" com regras do Kdenlive     | Doc    | [regras-para-mr.md](../../materiais/regras-para-mr.md)                                                     | Concluído |
| 14/04 | Escrita do diário de bordo da Sprint 0                       | Doc    | Este arquivo                                                                                               | Concluído |
| 21/04 | Implantação e espelhamento dinâmico via PyMdownx Snippets    | Dev    | [index.md](../../index.md)                                                                                 | Concluído |
| 21/04 | Refatoração visual (paleta Indigo) e custom tasklists        | UX     | [mkdocs.yml](https://github.com/caeslucio/GCES-Kdenlive-relatorios/blob/main/mkdocs.yml)                   | Concluído |
| 21/04 | Inclusão vetorial SVG da Logo Oficial nas rootpages          | UX     | [README.md](https://github.com/caeslucio/GCES-Kdenlive-relatorios/blob/main/README.md)                     | Concluído |
| 21/04 | Revisão e fix de warnings estruturais de relinking no MkDocs | QA     | [Sprint0.md](Sprint0.md)                                                                                   | Concluído |

---

### Maiores Avanços

- **Infraestrutura de documentação completa**: o repositório foi criado com estrutura MkDocs Material, menu de navegação configurado, modo escuro/claro, busca integrada e CI/CD funcional. Qualquer push na branch `main` publicará automaticamente o site.
- **Refinamento da interface Mkdocs (UX/UI)**: adoção da paleta *Indigo* para corresponder à marcação visual do projeto Kdenlive real, implantação de *custom tasklists* renderizadas e de espelhamentos dinâmicos via *Snippets* que evitam duplicação de tabelas (ex: puxar os membros dinamicamente do README para o index.md final).
- **Guias de contribuição reais**: os guias de abertura e regras de MR foram escritos com base na documentação oficial do Kdenlive. O projeto usa o KDE GitLab (`invent.kde.org`), o Bugzilla do KDE para rastreamento de bugs e requer conta KDE Identity.
- **Pesquisa do ecossistema KDE**: entendi como funciona o fluxo de contribuição da KDE — criação de conta no [identity.kde.org](https://identity.kde.org), fork no GitLab, abertura de Merge Requests (não Pull Requests), uso do Bugzilla como rastreador de bugs e do fórum [discuss.kde.org](https://discuss.kde.org/tag/kdenlive) como canal de comunicação.

---

### Maiores Dificuldades

- **Diferença de plataforma**: o Kdenlive não usa o GitHub para contribuições de código — usa o KDE GitLab (`invent.kde.org`). Isso exige adaptar todos os guias e terminologia (Pull Request → Merge Request, GitHub Issues → Bugzilla KDE).
- **Ausência de dados de parte da equipe**: matrículas, usuários do GitHub e do KDE de vários integrantes ainda não foram fornecidos, deixando parte das tabelas com campos em branco.
- **Conteúdo de projetos anteriores**: alguns arquivos copiados do projeto modelo tinham referências profundas ao Oppia (comandos Docker específicos, links para wikis do Oppia, nomes de mantenedores), exigindo uma revisão detalhada arquivo por arquivo.

---

### Aprendizados

- O ecossistema KDE tem sua própria infraestrutura de identidade (`identity.kde.org`) e rastreamento de bugs (`bugs.kde.org/bugzilla`), separada do GitHub/GitLab público.
- No Kdenlive, as contribuições de código acontecem via **Merge Requests** no [invent.kde.org](https://invent.kde.org/multimedia/kdenlive), seguindo o **KDE Coding Style** para C++ e QML.
- O MkDocs Material permite publicar sites de documentação completos com CI/CD via GitHub Actions, sem necessidade de infraestrutura externa.
- A importância de documentar desde o início: um repositório de documentação bem estruturado facilita a colaboração de todos os membros do grupo ao longo do semestre.

---

### Plano Pessoal para a Próxima Sprint (Sprint 1)

- [ ] Criar conta no [KDE Identity](https://identity.kde.org) e no [invent.kde.org](https://invent.kde.org).
- [ ] Fazer o fork do repositório do Kdenlive e configurar o ambiente de compilação local.
- [ ] Ler a [Wiki de desenvolvimento do Kdenlive](https://invent.kde.org/multimedia/kdenlive/-/wikis/home).
- [ ] Identificar ao menos 1 issue ou bug aberto no [Bugzilla do KDE](https://bugs.kde.org/buglist.cgi?product=kdenlive&resolution=---) para trabalhar.
- [ ] Abrir ou comentar em ao menos 1 issue ou MR no repositório oficial.
- [ ] Escrever o diário de bordo da Sprint 1.
