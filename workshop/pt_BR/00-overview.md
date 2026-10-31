<!-- l10n-sync: source-file="workshop/00-overview.md" -->
# 🎮 Mona Mayhem — Workshop de GitHub Copilot

---

> **Duração:** ~1 hora  
> **Nível:** Intermediário  
> **Stack:** Astro / Node.js / TypeScript

Construa um aplicativo retrô estilo arcade para comparar contribuições do GitHub — **Mona Mayhem** — enquanto aprende todo o espectro de fluxos de trabalho do GitHub Copilot. O workshop oferece **duas trilhas**: uma experiência no VS Code e outra com GitHub Copilot CLI.

---

## 🎯 Escolha sua trilha

- **Trilha do VS Code** — fique dentro do editor e pratique Chat, Plan Mode, Agent Mode, agentes em segundo plano e o ciclo de revisão integrado.
- **Trilha do CLI** — fique no terminal e pratique `copilot`, contexto com `@file`, `/plan`, edições automáticas, `/fleet`, `/delegate` e `/review`.

Siga a trilha que melhor combina com seu fluxo de trabalho.

---

## 📋 Lista rápida de verificação

Antes de começar, verifique:

- [ ] GitHub Copilot está habilitado para sua conta
- [ ] Node.js instalado
- [ ] Git instalado e configurado
- [ ] Seu navegador e terminal estão prontos

<!-- track:vscode:start -->
- [ ] VS Code **v1.107+** (sem atualizações pendentes)
- [ ] Conectado à extensão do **GitHub Copilot**
- [ ] Painel de Chat aberto e Agent pronto
<!-- track:vscode:end -->

<!-- track:cli:start -->
- [ ] GitHub Copilot CLI instalado e disponível como `copilot`
- [ ] Autenticado no CLI com `/login`
- [ ] Confortável usando comandos de barra como `/help`, `/plan` e `/review`
<!-- track:cli:end -->

> 💡 **Dica:** Use o DevContainer para um ambiente pré-configurado se quiser começar rapidamente no VS Code.

---

## 🧠 O que você vai aprender

| # | Habilidade | Descrição |
|---|------------|-----------|
| 1 | **Context Engineering** | Ensine o Copilot sobre seu código com instruções, referências e restrições claras |
| 2 | **Plan First** | Escreva a arquitetura antes de implementar |
| 3 | **Implementação agêntica** | Deixe o Copilot realizar trabalho de codificação em vários passos com sua supervisão |
| 4 | **Design iterativo** | Use o Copilot para transformar elementos visuais e refinar detalhes de interação |
| 5 | **Fluxos de trabalho paralelos** | Divida o trabalho entre agentes, sessões ou tarefas delegadas |

<!-- track:vscode:start -->
### Foco das funcionalidades do VS Code

- **Chat + modo Ask** para exploração
- **Plan Mode** para arquitetura e prompts de design
- **Agent Mode** para implementação em vários arquivos
- **Agentes locais e em nuvem** para acabamento em paralelo
<!-- track:vscode:end -->

<!-- track:cli:start -->
### Foco das funcionalidades do Copilot CLI

- **Sessões interativas de CLI** com `copilot`
- **`/plan` e Shift+Tab** para planejamento estruturado
- **Edições autônomas** com aprovações inline e `/diff`
- **`/fleet`, `/delegate` e `/review`** para paralelismo e controles de qualidade
<!-- track:cli:end -->

---

## 📚 Partes do workshop

| Parte | Título | Descrição |
|------|--------|-----------|
| [**01**](01-setup.md) | Configuração e contexto | Crie seu repositório, prepare o ambiente e dê ao Copilot o contexto adequado |
| [**02**](02-plan-and-scaffold.md) | Planejar e estruturar | Projete a API e a arquitetura da página antes de implementar |
| [**03**](03-agent-mode.md) | Construir o jogo | Conecte a página de batalha e os gráficos de contribuição com ajuda agêntica |
| [**04**](04-design-vibes.md) | Tematização orientada por design | Transforme o esqueleto em uma experiência retro arcade |
| [**05**](05-polish.md) | Acabamento e trabalho paralelo | Use fluxos multiagente para melhorar UX, robustez e qualidade |
| [**06**](06-bonus.md) | Bônus e extensões | Explore recursos abertos, fluxos de compartilhamento e experimentos extras |

---

## 💡 Dicas profissionais

1. **Mantenha o navegador aberto** — acompanhe as atualizações em tempo real enquanto codifica.
2. **Faça commits com frequência** — salve checkpoints limpos enquanto itera.
3. **Ajuste o plano antes de implementar** — melhores planos levam a melhores resultados.
4. **Revise as mudanças do Copilot** — use a visualização de diff ou as ferramentas de revisão do CLI em vez de aceitar às cegas.

<!-- track:vscode:start -->
5. **Use checkpoints e desfazer** no chat se uma iteração sair do foco.
<!-- track:vscode:end -->

<!-- track:cli:start -->
5. **Use `/session`, `/context` e `/share file`** quando quiser inspecionar ou preservar seu trabalho.
<!-- track:cli:end -->
