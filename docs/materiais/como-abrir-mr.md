# Como abrir um Merge Request (MR) no Kdenlive

Esta página descreve como criar **Merge Request (MR)** no repositório do Kdenlive, hospedado no [KDE GitLab (invent.kde.org)](https://invent.kde.org/multimedia/kdenlive). No GitLab, o equivalente ao Pull Request do GitHub é chamado de **Merge Request**.

> **Nota:** O Kdenlive utiliza a plataforma [invent.kde.org](https://invent.kde.org/multimedia/kdenlive) (GitLab) como repositório oficial. Não são aceitas contribuições via GitHub.

---

## Pré-requisitos

Antes de abrir um MR, você precisará:

1. **Criar uma conta KDE Identity** em [identity.kde.org](https://identity.kde.org) — ela é usada para acessar o invent.kde.org e todos os serviços da KDE.
2. **Fazer um fork** do repositório em [invent.kde.org/multimedia/kdenlive](https://invent.kde.org/multimedia/kdenlive) para a sua conta pessoal.
3. **Clonar o seu fork** localmente:
   ```bash
   git clone https://invent.kde.org/SEU_USUARIO/kdenlive.git
   cd kdenlive
   ```
4. **Adicionar o upstream** como remote:
   ```bash
   git remote add upstream https://invent.kde.org/multimedia/kdenlive.git
   ```
5. Consultar as instruções de compilação na [Wiki do projeto](https://invent.kde.org/multimedia/kdenlive/-/wikis/home).

---

## Antes de começar a trabalhar

- **Verifique se já existe uma issue** relacionada ao que você quer corrigir ou implementar. Use o rastreador de bugs oficial: [bugs.kde.org – Kdenlive](https://bugs.kde.org/buglist.cgi?product=kdenlive&resolution=---).
- **Se não houver uma issue**, crie uma no Bugzilla do KDE ou abra uma discussão no grupo oficial Matrix [kdenlive dev](https://matrix.to/#/%23kdenlive-dev:kde.org) ou no [Fórum Kdenlive](https://discuss.kde.org/tag/kdenlive) antes de começar a codificar.
- **Sincronize sempre com o upstream** antes de criar um branch novo:
  ```bash
  git fetch upstream
  git checkout master
  git merge upstream/master
  ```

---

## Criando o Branch e Desenvolvendo

1. Crie um branch a partir do `master`:
   ```bash
   git checkout -b minha-correcao upstream/master
   ```
2. Faça suas alterações com commits pequenos e descritivos.
3. Escreva **mensagens de commit em inglês**, seguindo o padrão convencional:
   ```
   fix(timeline): correct clip snapping at boundaries
   ```
   ou
   ```
   feat(effects): add new color grading filter
   ```

---

## O que torna um MR de qualidade

> **Regra:** Todo o conteúdo do MR (título, descrição, commits e comentários no código) deve estar em **inglês**, pois a equipe e os revisores são internacionais.

### 1. Título claro

Use o formato: `Fixes #NUMERO: Breve descrição do que foi feito`

**Bom:** `Fixes #1234: Fix crash when opening project with missing clips`
**Ruim:** `Fixed a bug`

### 2. Descrição completa

Ao abrir o MR, preencha:

- **O que foi alterado?**
- **Por que a mudança é necessária?**
- **Como testar a mudança?**
- **Capturas de tela** (para mudanças visuais na interface).

### 3. Escopo focado

- Cada MR deve resolver **apenas uma issue ou problema**.
- Não misture correções de bugs, refatorações e novas funcionalidades no mesmo MR.

### 4. Testes passando

- Certifique-se de que o código **compila sem erros** antes de abrir o MR.
- Se houver testes automatizados, execute-os localmente.
- O CI/CD do KDE GitLab será executado automaticamente; o MR só será revisado se os pipelines passarem.

### 5. Siga o estilo de código do Kdenlive

- O Kdenlive é escrito em **C++ e QML**.
- Siga o **KDE Coding Style**: [api.kde.org/guidelines-and-tips](https://api.kde.org/guidelines-and-tips.html).
- Use o `clang-format` para garantir a formatação correta.

---

## Abrindo o Merge Request

1. Envie seu branch para o seu fork:
   ```bash
   git push origin minha-correcao
   ```
2. Acesse [invent.kde.org/multimedia/kdenlive/-/merge_requests](https://invent.kde.org/multimedia/kdenlive/-/merge_requests) e clique em **New merge request**.
3. Selecione o seu fork e branch como origem, e o repositório oficial `multimedia/kdenlive` (branch `master`) como destino.
4. Preencha o título e a descrição completos.
5. Marque o MR como **Draft** (rascunho) se ainda não estiver pronto para revisão.

---

## Checklist Final

Antes de marcar o MR como pronto para revisão:

  - [ ] Meu MR resolve **apenas um problema** (issue)
  - [ ] O título e a descrição estão em **inglês**
  - [ ] Segui o **KDE Coding Style**
  - [ ] O código **compila sem erros**
  - [ ] Os **pipelines do CI** estão passando
  - [ ] Incluí **capturas de tela** (se houver mudanças visuais)
  - [ ] A mensagem de commit está clara e descritiva
  - [ ] Estou pronto para **responder às revisões** prontamente

---

## Após abrir o MR

- **Participe ativamente da revisão**: responda os comentários dos mantenedores e faça as alterações solicitadas.
- **Não force-push** no branch enquanto houver revisão em andamento.
- Quando o MR estiver aprovado, um mantenedor irá fazer o merge.

---

## Links Úteis

| Recurso | Link |
| ------- | ---- |
| Repositório oficial | [invent.kde.org/multimedia/kdenlive](https://invent.kde.org/multimedia/kdenlive) |
| Merge Requests abertos | [invent.kde.org/multimedia/kdenlive/-/merge_requests](https://invent.kde.org/multimedia/kdenlive/-/merge_requests) |
| Rastreador de bugs (Bugzilla) | [bugs.kde.org – Kdenlive](https://bugs.kde.org/buglist.cgi?product=kdenlive) |
| Fórum da comunidade | [discuss.kde.org/tag/kdenlive](https://discuss.kde.org/tag/kdenlive) |
| KDE Coding Style | [api.kde.org/guidelines-and-tips](https://api.kde.org/guidelines-and-tips.html) |
| Wiki do projeto | [invent.kde.org/multimedia/kdenlive/-/wikis](https://invent.kde.org/multimedia/kdenlive/-/wikis/home) |
| KDE Identity (conta) | [identity.kde.org](https://identity.kde.org) |
| Código de Conduta KDE | [kde.org/code-of-conduct](https://kde.org/code-of-conduct/) |

---

## Histórico de Versão

- **v1.0 (14/04/2026):** Documento criado para o projeto GCES – Kdenlive.