# Relatório de Contribuição – Sprint 0
 
**Disciplina:** Gestão de Configuração e Evolução de Software  
**Equipe:** GCES 2026.1 – Kdenlive  
**Comunidade/Projeto:** [KDE / Kdenlive](https://invent.kde.org/multimedia/kdenlive)  
**Matrícula:** 232014413  
**GitHub:** [@davirnunes](https://github.com/davirnunes)  
**KDE Invent:** [@davirnunes](https://invent.kde.org/davirnunes)  
**Período:** 01/04/2026 – 21/04/2026
 
---
 
## 1. Resumo da Sprint
 
Esta Sprint 0 foi o *bootstrap* da nossa operação. O foco dividiu-se em duas frentes críticas: a **Engenharia de Documentação**, onde estabelecemos um portal robusto via MkDocs Material para centralizar o conhecimento da equipe, e o **Setup de Ambiente no Windows**, utilizando o Craft para domar a árvore de dependências do Kdenlive. Consolidamos nossa presença na infraestrutura do KDE (Identity/Invent) e mapeamos o fluxo de contribuição que ditará o ritmo das próximas semanas.
 
---
 
## 2. Objetivos da Sprint
 
- **Padronização:** Criar um repositório de relatórios com CI/CD funcional e UI/UX otimizada.
- **Acreditação:** Obter as credenciais necessárias no KDE Identity e validar o acesso ao Invent.
- **Configuração de Ambiente:** Superar as barreiras de compilação no Windows (Craft/Compiler setup).
- **Mapeamento:** Entender a fundo as regras de submissão e o *Coding Style* da comunidade KDE.
---
 
## 3. Entregas Coletivas
 
| Entrega | Status | Link/Referência | Observações |
| :--- | :--- | :--- | :--- |
| **Portal MkDocs** | ✅ Concluído | [Link do Repo/Pages] | Estrutura com modo dark, busca e templates. |
| **Fork & Clone** | ✅ Concluído | [invent.kde.org/davirnunes/kdenlive] | Base de código sincronizada localmente. |
| **Guia de Contribuição** | ✅ Concluído | [/materiais/guia_contribuicao.md] | Baseado nas normas oficiais do Kdenlive. |
 
---
 
## 4. Log de Atividades
 
| Data | Atividade | Tipo | Status |
| :--- | :--- | :--- | :--- |
| 15/04 | Estudo de arquitetura do repositório exemplo | Estudo | ✅ |
| 18/04 | Setup inicial do MkDocs Material e CI/CD para deploy | Doc/Infra | ✅ |
| 19/04 | Instalação do **Craft** e configuração de dependências no Windows | Ambiente | ✅ |
| 19/04 | Criação de conta KDE Identity e validação no Bugzilla | Outro | ✅ |

---
 
## 5. Maiores Avanços
 
- **Ecossistema KDE dominado:** diferente do GitHub comum, o KDE exige um fluxo próprio (Identity → Invent → Bugzilla). O sucesso na navegação dessas ferramentas é um marco para a equipe.
- **Infraestrutura "As a Service":** a documentação não é apenas texto — o MkDocs configurado com CI/CD garante que cada log de membro seja publicado automaticamente, reduzindo o trabalho manual.
- **Build no Windows:** conseguir configurar o Craft e as variáveis de ambiente multimídia no Windows sem conflitos críticos de DLLs.
---
 
## 6. Maiores Dificuldades
 
- **Dívida de tempo na estruturação:** a dedicação minuciosa à arquitetura do MkDocs consumiu uma janela de tempo que comprimiu o prazo de preenchimento dos diários do restante da equipe.
- **Complexidade do Craft:** lidar com caminhos longos (`MAX_PATH`) e a instalação silenciosa de dependências pesadas no Windows exigiu múltiplas tentativas de configuração.
!!! warning "Nota de Responsabilidade"
    Como arquiteto da documentação, assumo que a priorização da infraestrutura central atrasou a integração dos dados individuais da equipe nesta sprint, ponto que será normalizado na Sprint 1.
 
---
 
## 7. Lições Aprendidas
 
- **Gestão de Configuração:** o Craft não é apenas um instalador, mas uma ferramenta de gestão de configuração essencial para manter a paridade entre ambientes de desenvolvimento distintos.
- **Cultura Open Source:** no Kdenlive, a conversa no Matrix/Fórum é tão importante quanto o código. A proatividade em canais como o [discuss.kde.org](https://discuss.kde.org/tag/kdenlive) é vital.
---
 
## 8. Plano Pessoal para a Próxima Sprint (Sprint 1)
 
- [ ] Realizar um teste de estabilidade no windows no Kdenlive.
- [ ] Submeter o primeiro Merge Request no KDE Invent.
- [ ] Iniciar o estudo da estrutura de classes do projeto (C++/Qt).