# RPG Educativo para Aprender Git e GitHub

Olá, Mestre Dresch!

Este README apresenta visão geral, estrutura, instruções de instalação e descrição das fases do jogo educativo que ensina Git e GitHub através da metáfora de cultivar uma planta. Sinta-se à vontade para ajustar ou personalizar conforme necessário.

---

## Sumário

1. [Visão Geral](#visão-geral)
2. [Funcionalidades Principais](#funcionalidades-principais)
3. [Tecnologias Utilizadas](#tecnologias-utilizadas)
4. [Instalação e Configuração](#instalação-e-configuração)
5. [Como Jogar](#como-jogar)
6. [Estrutura de Fases](#estrutura-de-fases)

   * Fase 0 – Jardim Inicial
   * Fase 1 – Semeando o Repositório
   * Fase 2 – Primeiras Folhas (Adicionar e Commitar)
   * Fase 3 – Ramas do Bosque (Branches)
   * Fase 4 – Conflito na Floresta (Merge e Resolução)
   * Fase 5 – Ida ao Mundo Externo (Remoto)
   * Fase 6 – Colheita Colaborativa (Pull Requests)
   * Fase 7 – Desafio Final (Rebase e Tags)
   * Fase Bônus – GitHub Actions
   * Fase Bônus II – Colaboração Avançada
7. [Tela de Tutorial e Menu Principal](#tela-de-tutorial-e-menu-principal)
8. [Recompensas e Progressão Visual](#recompensas-e-progressão-visual)
9. [Contribuições](#contribuições)
10. [Licença](#licença)

---

## 1. Visão Geral

Este projeto é um jogo em estilo RPG que tem como objetivo ensinar conceitos fundamentais do Git e do GitHub de forma lúdica e interativa. A cada fase concluída pelo jogador, uma planta simbólica vai crescendo e evoluindo, representando o domínio dos comandos Git:

* **Metáfora**: Plantar uma semente e cultivá-la até se tornar uma árvore robusta.
* **Interação**: Quizzes, desafios práticos e pequenas simulações no terminal ou interface gráfica para fixar conceitos.
* **Narrativa**: Um ambiente de jardim encantado, com NPCs que servem como mentores e guardiões dos conhecimentos Git.

> **Opinião**: Em minha visão, a junção de narrativa e mecânicas práticas (mesmo que simuladas) reforça a memorização dos comandos e mantém o jogador engajado.

---

## 2. Funcionalidades Principais

* **Tutorial Inicial**: Guia rápido sobre controles e metáfora do jogo.
* **Quiz Interativos**: Múltipla escolha e atividades de arrastar/soltar para simular `git merge` e resolução de conflitos.
* **Simulação de Terminal (opcional)**: Para quem quiser digitar comandos de verdade e vê-los aplicados em um repositório local.
* **Integração com GitHub (opcional)**: Conexão real com um repositório remoto para `git push` e `pull`.
* **Sistema de Ramificações (Branches)**: Criação e alternância de branches, simulando “galhos” de uma planta.
* **Resolução de Conflitos**: Desafios onde o jogador edita manualmente trechos de texto para mesclar versões.
* **Pull Requests e Code Review**: Mecanismo que simula contribuições de NPCs ou de outros jogadores e a revisão de código.
* **Rebase Interativo e Tags/Releases**: Reescrever histórico, combinar commits e marcar versões estáveis.
* **Bônus de CI/CD**: Configuração básica do GitHub Actions para testes automáticos.
* **Colaboração Avançada**: Configuração de `CODEOWNERS` e organização via GitHub Projects.

> **Opinião**: Recomendo tornar algumas integrações (como GitHub real e GitHub Actions) opcionais, para que iniciantes não se sintam sobrecarregados. Elas podem ser desbloqueadas quando o jogador atinge determinados marcos.

---

## 3. Tecnologias Utilizadas

* **Linguagem de Programação**: JavaScript (para lógica de game engine) + HTML/CSS (para front-end). Opcionalmente, um framework como Phaser ou PixiJS para parte gráfica.
* **Ambiente de Simulação de Terminal**: Bibliotecas JavaScript (ex.: xterm.js) para emular um terminal dentro do jogo.
* **Gestão de Estado e Dados**: IndexedDB ou localStorage para salvar progresso, status dos branches e commits simulados.
* **Integração Git Real (opcional)**: Node.js + child\_process para executar comandos Git localmente, ou APIs do GitHub via GitHub CLI (`gh`) ou chamada REST.
* **Servidor de Desenvolvimento**: Node.js + Express (caso haja componentes de backend, como auto-gravação de dados em nuvem).
* **Controle de Versão do Próprio Jogo**: Este projeto usa Git para versionamento e GitHub para hospedagem do repositório.

> **Opinião**: Como é um jogo educativo, a simplicidade da stack facilita a manutenção. Sugiro usar vanilla JS ou uma biblioteca leve de jogos para manter o foco nos conceitos Git.

---

## 4. Instalação e Configuração

1. **Pré-requisitos**:

   * Node.js v14+ instalado.
   * Git instalado (caso queira usar o terminal integrado).
   * (Opcional) Conta no GitHub e [GitHub CLI](https://cli.github.com/) (`gh`) instalado para funcionalidades reais de push/pull.

2. **Clone do Repositório**:

   ```bash
   git clone https://github.com/seu-usuario/rpg-git-educativo.git
   cd rpg-git-educativo
   ```

3. **Instalar Dependências**:

   ```bash
   npm install
   ```

4. **Configuração Inicial**:

   * Crie um arquivo `.env` na raiz (caso haja variáveis de ambiente, como TOKEN\_GITHUB).
   * Exemplo de `.env` (opcional):

     ```env
     GITHUB_TOKEN=seu_token_aqui
     ```

5. **Rodar em Modo de Desenvolvimento**:

   ```bash
   npm run dev
   ```

   Isso iniciará um servidor local (por exemplo, `http://localhost:3000`) com hot-reload para desenvolvimento.

6. **Build para Produção**:

   ```bash
   npm run build
   npm start
   ```

---

## 5. Como Jogar

1. Abra o navegador em `http://localhost:3000`.
2. Na tela inicial, você verá o **Jardim Inicial** com duas opções: **Tutorial** e **Jogar**.

   * **Tutorial**: breve explicação sobre a metáfora e controles do jogo.
   * **Jogar**: inicia a Fase 1 diretamente.
3. A cada fase, o jogador receberá perguntas (quiz) ou desafios práticos. Ao responder corretamente, a planta avançará em seu estágio de crescimento.
4. Caso erre, receberá feedback imediato com dicas e poderá tentar novamente.
5. Ao final de cada fase, um resumo dos comandos aprendidos estará disponível no “Boletim de Jardinagem”.
6. Conforme seu progresso, desbloqueie funções avançadas, como integração real com GitHub e workflows de CI.

> **Opinião**: incluir uma opção de “Sair para salvar progresso” ajuda jogadores com TDAH a fazer pausas e retomar sem estresse.

---

## 6. Estrutura de Fases

A seguir, uma descrição detalhada de cada fase, seus objetivos e mecânicas.

### Fase 0 – Jardim Inicial

* **Objetivo**: Apresentar o enredo, tutorial e acessar o jogo.
* **Mecânica**: Tela de boas-vindas com opções: “Tutorial” e “Jogar”.
* **Narrativa**: Uma estufa acolhe a semente; o jogador escolhe se quer aprender como navegar ou ir direto para o desafio.

### Fase 1 – Semeando o Repositório

* **Conceito Git/GitHub**: `git init`.
* **Objetivo**: Preparar o solo (criar repositório local).
* **Desafio**:

  1. Quiz: selecionar o comando correto para iniciar um repositório (`git init`).
* **Recompensa Visual**: Semente plantada e uma animação inicial de terra fértil.

> **Opinião**: manter essa fase curta e clara, pois muitos iniciantes já ficam ansiosos ao ver termos como `.git`.

### Fase 2 – Primeiras Folhas (Adicionar e Commitar)

* **Conceito Git/GitHub**: `git add` + `git commit`.
* **Objetivo**: Entender a Staging Area e o processo de commit.
* **Desafio**:

  1. Quiz: escolher `git add <arquivo>` para preparar arquivo.
  2. Quiz: escolher `git commit -m 'mensagem'` para gravar no histórico.
* **Recompensa Visual**: Pequena muda com primeiras folhas brotando.

> **Opinião**: a diferença entre “adicionar” e “comitar” é crucial; uma animação mostrando folhas sendo colhidas e fixadas em um mural de progresso ajuda a fixar a ideia.

### Fase 3 – Ramas do Bosque (Branches)

* **Conceito Git/GitHub**: `git branch` + `git checkout` (ou `git switch`).
* **Objetivo**: Criar e alternar entre branches.
* **Desafio**:

  1. Quiz: `git branch <nome>` para criar branch.
  2. Quiz: `git checkout <nome>` ou `git switch <nome>` para alternar.
* **Recompensa Visual**: Galhos surgindo, representando caminhos distintos para a planta crescer.

> **Opinião**: apresentar um pequeno mapa visual de ramificações ajuda a entender que cada branch é um caminho paralelo de desenvolvimento.

### Fase 4 – Conflito na Floresta (Merge e Resolução de Conflitos)

* **Conceito Git/GitHub**: `git merge` e resolução de conflitos.
* **Objetivo**: Unir branches e lidar com conflitos.
* **Desafio**:

  1. Quiz: `git merge <branch>` para mesclar.
  2. Mini-atividade de edição: resolver um conflito simulado, escolhendo quais linhas manter ou mesclar manualmente.
* **Recompensa Visual**: Animação de galhos sendo entrelaçados e fortalecimento do tronco.

> **Opinião**: conflitos podem assustar; inserir dicas visuais (por exemplo, destacar as linhas conflitantes em vermelho) torna a atividade mais intuitiva.

### Fase 5 – Ida ao Mundo Externo (Remoto e GitHub)

* **Conceito Git/GitHub**: `git remote add origin`, `git push origin main`, `git pull origin main`.
* **Objetivo**: Conectar ao GitHub e sincronizar alterações.
* **Desafio**:

  1. Quiz: `git remote add origin <URL>`.
  2. Quiz: `git push origin main` para enviar commits.
  3. Quiz: `git pull origin main` para trazer atualizações.
* **Recompensa Visual**: A planta “teletransporta” sementes para uma biblioteca global (GitHub) e recebe reconhecimento (ícone de estrela ou carimbo “publicado”).

> **Opinião**: permitir modo simulado e modo real (com autenticação GitHub) serve diferentes públicos; quem nunca usou GitHub pode ficar receoso com tokens.

### Fase 6 – Colheita Colaborativa (Pull Requests e Revisão)

* **Conceito Git/GitHub**: Pull Requests, Code Review.
* **Objetivo**: Criar PRs e revisar contribuições de outros.
* **Desafio**:

  1. Quiz: identificar que PRs são criadas na interface do GitHub (ou via `gh pr create`).
  2. Atividade: avaliar dois trechos de código/README e decidir se aprova ou solicita mudanças, sugerindo melhorias.
* **Recompensa Visual**: Ícones de cartas entregues, selo de “Revisão Aprovada” e pequenos frutos surgindo na planta (representando features colaborativas).

> **Opinião**: incentivar feedback construtivo é fundamental; oferecer exemplos de boas práticas (mensagens claras, comentários educados) faz diferença no aprendizado colaborativo.

### Fase 7 – Desafio Final: Conflito Global (Rebase Interativo, Tags e Releases)

* **Conceito Git/GitHub**: Rebase interativo (`git rebase -i`), squash, `git tag`, criação de Releases.
* **Objetivo**: Consolidar histórico, marcar versões estáveis.
* **Desafio**:

  1. Quiz: identificar que `git rebase -i HEAD~3` e marcar “squash” combina commits.
  2. Quiz: `git tag v1.0` para criar tag.
  3. Atividade final: reescrever histórico (emulado), resolver conflitos múltiplos, criar tag e “lançar” Release (simulação ou real).
* **Recompensa Visual**: A planta floresce por completo, ganha uma coroa simbólica de “Árvore Mestra” e libera sementes-mãe para outros jardins.

> **Opinião**: se desejar, divida esse desafio em duas etapas (primeiro rebase, depois tag/release) para facilitar a compreensão. Usuários iniciantes podem se perder se receberem tudo junto.

### Fase Bônus – GitHub Actions

* **Conceito Git/GitHub**: Configuração de CI básico via GitHub Actions.
* **Objetivo**: Automatizar testes e builds a cada push.
* **Desafio**:

  1. Quiz: identificar que arquivo de workflow é `.github/workflows/ci.yml`.
  2. Atividade: selecionar etapas (jobs) como “Instalar Dependências”, “Rodar Testes”.
* **Recompensa Visual**: Um Elfo Automatizador aparece, regando a planta automaticamente e afastando pragas (bugs).

> **Opinião**: essa fase é opcional para quem busca aprofundar; foque no básico de Git primeiro, e desbloqueie CI somente após o jogador dominar merge e rebase.

### Fase Bônus II – Colaboração Avançada (CODEOWNERS e GitHub Projects)

* **Conceito Git/GitHub**: `CODEOWNERS` e GitHub Projects.
* **Objetivo**: Definir responsabilidades e organizar tarefas.
* **Desafio**:

  1. Quiz: `CODEOWNERS` identifica responsáveis por arquivos.
  2. Atividade: criar ou simular um quadro de projeto com colunas “To Do”, “In Progress” e “Done”, movendo issues fictícias.
* **Recompensa Visual**: Pequenos jardineiros NPCs aparecem para cuidar de seções específicas (folhas, flores, raízes).

> **Opinião**: perfeito para equipes de desenvolvimento, mas mantenha como módulo extra para não distrair aprendizes individuais.

---

## 7. Tela de Tutorial e Menu Principal

* **Tutorial**:

  * Explicação breve da metáfora (solo, semente, rega, fertilização).
  * Controles básicos: navegação, seleção de alternativas, como digitar comandos (quando aplicável).
  * Breve demonstração das fases, mostrando que cada comando Git representa um gesto de cuidado com a planta.
* **Menu Principal**:

  * Botões:

    * **Tutorial**
    * **Jogar**
    * **Configurações** (som, dicas visuais, modo real/simulado).
    * **Boletim de Jardinagem** (histórico de comandos aprendidos e progresso).
    * **Sair/Salvar Progresso**.

> **Opinião**: um botão de “Dicas” fixo, que abre o “Livro de Sabedoria” com exemplos de comandos, ajuda jogadores com TDAH a retomar conceitos rapidamente quando ficarem em dúvida.

---

## 8. Recompensas e Progressão Visual

* **Pontuação (Pontos de Cultivo)**:

  * Cada quiz respondeu corretamente: +10 pontos.
  * Desafios práticos concluídos: +20 pontos.
  * Sugestões bem fundamentadas em code review: +15 pontos.
* **Itens de Coleção**:

  * **Adubo Mágico**: desbloqueado ao alcançar 100 pontos; acelera crescimento da planta em fases seguintes.
  * **Anel de Flores**: ao concluir Fase 3 sem erros; decora a planta.
  * **Estrela do Jardim**: ao concluir todos os quizzes sem falha.
* **Skins de Planta**:

  * **Girassol Radiante**
  * **Rosa Encantada**
  * **Jardim Lunar**
  * (Desbloqueáveis conforme progresso acumulado)

> **Opinião**: recompensas visuais e cosméticas aumentam engajamento. Para quem gosta de personalizar, ver sua planta assumir cores diferentes traz sensação de conquista.

---

## 9. Contribuições

Este projeto está em constante evolução. Se quiser contribuir:

1. Faça um fork deste repositório.
2. Crie uma branch para sua feature ou correção:

   ```bash
   git checkout -b feature/nome-da-feature
   ```
3. Implemente suas mudanças e adicione testes (se aplicável).
4. Faça commit das suas alterações:

   ```bash
   git commit -m "Descrição das mudanças"
   ```
5. Envie para seu fork:

   ```bash
   git push origin feature/nome-da-feature
   ```
6. Abra um Pull Request neste repositório e descreva as mudanças de forma clara.

Leia o arquivo `CONTRIBUTING.md` para diretrizes mais detalhadas.

> **Opinião**: adicionar um modelo de issue e PR template pode padronizar contribuições e facilitar a revisão de código por outros desenvolvedores.

---

## 10. Licença

Este projeto está licenciado sob a [MIT License](LICENSE).

---

**Obrigado por explorar esta ideia de jogo, Mestre Dresch!** Se precisar de ajustes ou quiser discutir novas funcionalidades, estou à disposição para opinar e contribuir.

Boa codificação e bom cultivo! 🌱
