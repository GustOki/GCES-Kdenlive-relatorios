# Regras para Merge Requests no Kdenlive

Esta página descreve as **regras obrigatórias** para abrir Merge Requests (MRs) no repositório do Kdenlive em [invent.kde.org](https://invent.kde.org/multimedia/kdenlive). Seguir estas regras aumenta as chances do seu MR ser revisado e integrado rapidamente.

> **Nota:** O Kdenlive usa o **KDE GitLab** (`invent.kde.org`), não o GitHub. O equivalente ao Pull Request (PR) é chamado de **Merge Request (MR)**.

---

## Regras

### 1. Tenha uma issue (ou bug) associada

- Todo MR deve estar vinculado a uma **issue existente** no [Bugzilla do KDE](https://bugs.kde.org/buglist.cgi?product=kdenlive&resolution=---) ou a uma issue/discussão no GitLab.
- Referencie a issue na descrição do MR com `Fixes #NUMERO` ou `Closes BUG:NUMERO` (para Bugzilla).
- Se não houver uma issue, **crie uma primeiro** e aguarde a confirmação dos mantenedores antes de começar a implementação.

### 2. Mantenha o MR pequeno e focado

- Cada MR deve tratar de **apenas um problema ou funcionalidade**.
- Não misture correções de bugs não relacionadas, refatorações e novas funcionalidades.
- MRs menores são mais fáceis de revisar e têm feedback mais rápido.

### 3. Escreva um título claro e em inglês

Siga o formato: `Fixes #NUMERO: Breve descrição do que foi feito`

- **Bom:** `Fixes #4567: Fix crash when importing MKV with missing audio stream`
- **Ruim:** `Consertei um bug`

Todo o conteúdo do MR (título, descrição, commits e comentários) **deve estar em inglês**.

### 4. Preencha a descrição do MR completamente

A descrição deve conter:

- **O que foi alterado?** – Descreva claramente a mudança.
- **Por que a mudança é necessária?** – Explique o problema ou a motivação.
- **Como testar?** – Liste os passos para o revisor verificar a correção.
- **Capturas de tela** – Obrigatórias para alterações visuais na interface.

### 5. Certifique-se de que o código compila e os pipelines passam

- O MR **não será revisado** enquanto houver falha no CI/CD do [KDE GitLab](https://invent.kde.org).
- Compile o Kdenlive localmente antes de enviar.
- Verifique se os testes automatizados passam.

### 6. Siga o estilo de código da KDE

- O Kdenlive é escrito em **C++ e QML**.
- Siga o [KDE Coding Style](https://api.kde.org/guidelines-and-tips.html).
- Use o **clang-format** para garantir a formatação correta do código C++.
- Não deixe código comentado, prints de debug ou arquivos desnecessários no MR.

### 7. Atualize a documentação se necessário

- Se sua mudança altera o comportamento do software, atualize a documentação relevante.
- A documentação do usuário está em [docs.kdenlive.org](https://docs.kdenlive.org) e é mantida em [invent.kde.org/documentation/docs-kdenlive-org](https://invent.kde.org/documentation/docs-kdenlive-org).

### 8. Use commits limpos e descritivos

- Escreva mensagens de commit claras em **inglês**.
- Prefira commits atômicos (um commit por mudança lógica).
- Antes de solicitar revisão, considere fazer `rebase` ou `squash` em commits pequenos e desnecessários.

### 9. Solicite a revisão das pessoas certas

- Use a função **Reviewers** do GitLab para marcar mantenedores relevantes.
- Caso não saiba quem marcar, deixe o campo em branco — os mantenedores serão notificados automaticamente.
- Você pode mencionar alguém nos comentários com `@username`.

### 10. Responda ao feedback prontamente

- Participe ativamente da revisão do seu MR.
- Responda aos comentários, faça as alterações solicitadas e avise quando o MR estiver pronto para nova rodada de revisão.
- Não faça force-push enquanto a revisão estiver em andamento, pois isso pode apagar o contexto dos comentários.

---

## Fluxo Resumido de Contribuição

```
1. Conta KDE Identity → identity.kde.org
2. Fork do repositório → invent.kde.org/multimedia/kdenlive
3. Clone do fork e configuração do upstream
4. Criação de branch a partir do master
5. Desenvolvimento + commits em inglês
6. Push para o fork
7. Abertura do MR no invent.kde.org
8. Pipelines passando → revisão dos mantenedores
9. Correções de acordo com o feedback
10. Merge
```

---

## Links Úteis

| Recurso | Link |
| ------- | ---- |
| Repositório oficial | [invent.kde.org/multimedia/kdenlive](https://invent.kde.org/multimedia/kdenlive) |
| Merge Requests abertos | [invent.kde.org/multimedia/kdenlive/-/merge_requests](https://invent.kde.org/multimedia/kdenlive/-/merge_requests) |
| Rastreador de bugs (Bugzilla) | [bugs.kde.org – Kdenlive](https://bugs.kde.org/buglist.cgi?product=kdenlive) |
| Abrir novo bug | [bugs.kde.org – Reportar bug](https://bugs.kde.org/enter_bug.cgi?product=kdenlive) |
| Wiki de desenvolvimento | [invent.kde.org/multimedia/kdenlive/-/wikis](https://invent.kde.org/multimedia/kdenlive/-/wikis/home) |
| KDE Coding Style | [api.kde.org/guidelines-and-tips](https://api.kde.org/guidelines-and-tips.html) |
| KDE Identity (conta) | [identity.kde.org](https://identity.kde.org) |
| Código de Conduta KDE | [kde.org/code-of-conduct](https://kde.org/code-of-conduct/) |
| Fórum da comunidade | [discuss.kde.org/tag/kdenlive](https://discuss.kde.org/tag/kdenlive) |
| Documentação do usuário | [docs.kdenlive.org](https://docs.kdenlive.org) |

---

## Histórico de Versão

- **v1.0 (14/04/2026):** Documento criado para o projeto GCES – Kdenlive.