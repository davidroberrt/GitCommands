# Comandos Git

## Configuração Inicial

- `git config`: Configura opções do Git no nível do sistema, usuário ou repositório.
   - Exemplo: `git config --global user.name "Seu Nome"`

## Inicialização e Clonagem de Repositórios

- `git init`: Inicia um novo repositório Git.
   - Exemplo: `git init nome-do-repositorio`

- `git clone`: Clona um repositório existente.
   - Exemplo: `git clone https://github.com/usuario/nome-do-repositorio.git`

## Estágio e Compromisso

- `git add`: Adiciona alterações ao índice (staging area).
   - Exemplo: `git add nome-do-arquivo`

- `git commit`: Registra alterações no repositório.
   - Exemplo: `git commit -m "Mensagem do commit"`

## Ramificação e Fusão

- `git branch`: Lista, cria ou exclui ramificações.
   - Exemplo: `git branch nome-da-ramificacao`

- `git checkout`: Muda para uma ramificação específica.
   - Exemplo: `git checkout nome-da-ramificacao`

- `git merge`: Funde alterações de uma ramificação em outra.
   - Exemplo: `git merge nome-da-outra-ramificacao`

## Atualização e Envio

- `git pull`: Atualiza o repositório local com as alterações do remoto.
   - Exemplo: `git pull origin nome-da-ramificacao`

- `git push`: Envia alterações locais para o repositório remoto.
   - Exemplo: `git push origin nome-da-ramificacao`

## Submódulos

- `git submodule`: Gerencia submódulos dentro do repositório.

## Rastreamento de Arquivos

- `git rm`: Remove arquivos do índice e do diretório de trabalho.
   - Exemplo: `git rm nome-do-arquivo`

## Ignorando Arquivos

- `.gitignore`: Arquivo que lista padrões de arquivos/diretórios a serem ignorados.

## Alterações Temporárias

- `git stash`: Salva alterações temporárias que não são para serem commitadas.

## Rebase

- `git rebase`: Altera a base de uma ramificação.
   - Exemplo: `git rebase ramificacao-destino`

## Amend

- `git commit --amend`: Modifica o último commit.
   - Exemplo: `git commit --amend`

## Logs Decorados

- `git log --decorate`: Exibe informações sobre referências ao lado dos commits.

## Atribuição de Autoria

- `git commit --author`: Atribui um autor específico a um commit.
   - Exemplo: `git commit --author="Nome <email@exemplo.com>"`

## Contribuição

- `git shortlog`: Gera um resumo de contribuições para o repositório.

## Anotação de Linha

- `git blame`: Mostra quem modificou cada linha de um arquivo e em qual commit.

## Armazenamento Temporário de Alterações

- `git worktree`: Permite trabalhar com várias cópias de trabalho separadas.

... (continuação)

## Reflog

- `git reflog`: Mostra um log de referências, útil para recuperar commits perdidos.

## Configuração Global

- `git config --global`: Configurações globais do usuário.
   - Exemplo: `git config --global core.autocrlf true`

## Cherry-pick

- `git cherry-pick`: Aplica um commit específico em uma ramificação.
   - Exemplo: `git cherry-pick commit-hash`

## Bisect

- `git bisect`: Ajuda na busca do commit que introduziu um bug.
   - Exemplo: `git bisect start` e `git bisect bad`/`git bisect good`

## Logs Detalhados

- `git log --graph --oneline --all`: Visualiza o histórico de commits de forma gráfica e resumida.

## Limpeza

- `git clean`: Remove arquivos não rastreados no diretório de trabalho.

## Busca em Logs

- `git grep`: Procura por padrões em qualquer árvore de trabalho e exibe os resultados.


## Configuração de Difftool e Mergetool

- `git difftool`: Configura e executa ferramentas de diff externas.
   - Exemplo: `git difftool --tool=meld`

- `git mergetool`: Configura e executa ferramentas de merge externas.
   - Exemplo: `git mergetool --tool=kdiff3`

## Stash

- `git stash`: Armazena temporariamente alterações não comprometidas.
   - Exemplo: `git stash save "Nome do Stash"`

- `git stash pop`: Aplica as alterações do último stash e remove o stash.

## Configuração Avançada de Remotos

- `git remote`: Mostra os repositórios remotos conectados.
   - Exemplo: `git remote -v`

- `git remote add`: Adiciona um novo repositório remoto.
   - Exemplo: `git remote add nome-remoto URL-do-remoto`

## Fetch e Pull Detalhados

- `git fetch`: Busca todas as alterações de um repositório remoto.
   - Exemplo: `git fetch origin`

- `git pull --rebase`: Atualiza o repositório local rebaseando em vez de mesclar.

## Trabalhando com Tags

- `git tag`: Lista, cria ou exclui tags.
   - Exemplo: `git tag -a v1.0 -m "Versão 1.0"`

- `git tag -d`: Exclui uma tag existente.
   - Exemplo: `git tag -d nome-da-tag`

## Desfazendo Alterações

- `git reset`: Desfaz alterações específicas do commit.
   - Exemplo: `git reset commit-hash`

- `git revert`: Desfaz um commit, criando um novo commit.
   - Exemplo: `git revert commit-hash`

## Trabalhando com Submódulos

- `git submodule`: Gerencia submódulos dentro do repositório.

## Busca e Substituição em Commits

- `git filter-branch`: Filtra branches em uma reescrita completa do histórico.
   - **Cuidado:** Uso avançado e pode alterar o histórico de forma significativa.

... (continuação)

## Interatividade e Seleção de Linhas

- `git add -p`: Permite a interatividade na adição de mudanças, linha por linha.
   - Útil para selecionar alterações específicas a serem comprometidas.

## Aliases

- `git config --global alias.nome-do-alias comando-git`: Cria alias para comandos frequentemente usados.
   - Exemplo: `git config --global alias.s status`

- `git alias`: Exibe a lista de aliases configurados.

## Hooks

- Hooks são scripts que você pode executar automaticamente em resposta a eventos específicos no Git.
  - Exemplo: `.git/hooks/pre-commit` para executar ações antes de um commit.

## Desfazendo Múltiplos Commits

- `git reset --soft HEAD~n`: Desfaz os últimos n commits, mantendo as alterações no diretório de trabalho.

- `git reset --hard HEAD~n`: Desfaz os últimos n commits e descarta as alterações no diretório de trabalho.

## Exibir Informações Detalhadas

- `git show`: Exibe informações detalhadas sobre um commit, diff incluído.
   - Exemplo: `git show commit-hash`

## Desfazendo e Modificando Commits

- `git revert -n`: Reverte commits sem criar um novo commit imediatamente.
   - Útil para realizar várias reversões antes de consolidar.

- `git commit --fixup` e `git rebase -i --autosquash`: Facilita a consolidação de correções com commits anteriores.

## Refatoração de Histórico

- `git rebase -i`: Permite reescrever e reorganizar commits interativamente.

## Comandos para Trabalho em Equipe

- `git fetch --prune`: Remove automaticamente referências remotas que não existem mais no repositório remoto.

- `git cherry`: Mostra commits que existem em um branch, mas não em outro.
   - Exemplo: `git cherry branch-local branch-remoto`

## Trabalho com Divergências

- `git log --merges`: Exibe logs apenas para commits de merge.

## Gerenciamento de Ramificações Remotas

- `git push --delete origin nome-da-ramificacao`: Exclui uma ramificação remota.
   - Exemplo: `git push --delete origin minha-ramificacao`

- `git remote prune origin`: Remove ramificações remotas que foram excluídas no repositório remoto.

## Subcomandos de Git Remote

- `git remote -v`: Exibe URLs dos repositórios remotos configurados.

- `git remote show nome-remoto`: Exibe informações detalhadas sobre um repositório remoto.

## Trabalho com Refspecs

- `git push origin local-ramificacao:ramificacao-remota`: Envia uma ramificação local para uma remota.
   - Exemplo: `git push origin minha-ramificacao:feature/minha-ramificacao`

- `git fetch origin local-ramificacao:ramificacao-remota`: Obtém uma ramificação remota sem fazer merge.
   - Exemplo: `git fetch origin feature/outra-ramificacao:feature/outra-ramificacao`

## Configuração do Git

- `git config --get-regexp alias`: Exibe todos os aliases configurados.

- `git config --global core.editor nome-do-editor`: Define o editor padrão para mensagens de commit.

## Git Workflows

- Git Flow, GitHub Flow, GitLab Flow: Diferentes abordagens para fluxos de trabalho Git.

## Git Bisect Automatizado

- `git bisect start`: Inicia o processo de bisect.
   - Exemplo: `git bisect start`

- `git bisect good` e `git bisect bad`: Ajuda a identificar automaticamente o commit problemático.

## Alias para Comandos Comuns

- `git config --global alias.st status`: Cria um alias para o comando `git status`.
   - Exemplo: `git st`

- `git config --global alias.ci commit`: Cria um alias para o comando `git commit`.
   - Exemplo: `git ci -m "Mensagem do commit"`

## Configuração de Endereços SSH

- `ssh-keygen`: Gera uma chave SSH para autenticação com o servidor remoto.

- Adicionando chave SSH ao agente SSH: `ssh-add ~/.ssh/sua-chave-privada`

## Git Subtree

- `git subtree`: Permite trabalhar com subárvores Git dentro de um repositório Git.

- Exemplo de adição de um subprojeto: `git subtree add --prefix pasta-subprojeto https://github.com/exemplo/repo-subprojeto.git master`

## Hooks Personalizados

- Criar scripts executáveis em `.git/hooks` para hooks personalizados.

## Trabalhando com Submódulos

- `git submodule init`: Inicializa submódulos após clonar um repositório.

- `git submodule update`: Atualiza submódulos para as versões configuradas.

- `git submodule foreach`: Executa um comando em cada submódulo.

## Modificação de Histórico por Autor

- `git log --author="Nome do Autor"`: Exibe logs filtrados por autor.

- `git log --grep="Mensagem"`: Filtra logs por mensagens de commit.

## Desfazendo Commit Localmente

- `git reset HEAD~n`: Desfaz os últimos n commits, mantendo alterações no diretório de trabalho.

- `git revert -n HEAD~n`: Reverte os últimos n commits, permitindo edições antes de confirmar.

## Utilizando Git Rerere

- `git config --global rerere.enabled true`: Ativa o Rerere (Reuse Recorded Resolution).

- Ajuda a reutilizar resoluções de conflitos anteriores automaticamente.


## Worktree

- `git worktree`: Permite trabalhar com cópias de trabalho adicionais em diferentes locais.

- `git worktree add nome-da-pasta branch`: Cria uma nova cópia de trabalho associada a uma branch específica.

## Alterações Locais e Stash

- `git stash list`: Lista todos os stashes disponíveis.

- `git stash apply`: Aplica o último stash.

- `git stash drop`: Remove o último stash.

## Ignorar Alterações Locais

- `git update-index --assume-unchanged arquivo`: Ignora alterações locais no arquivo.

- `git update-index --no-assume-unchanged arquivo`: Para de ignorar alterações locais no arquivo.

## Alterações Interativas

- `git add -i`: Modo interativo para adicionar alterações.

- `git commit --amend -m "Nova mensagem"`: Modifica a mensagem do último commit.

## Comparação Avançada

- `git difftool`: Abre uma ferramenta de diff externa para visualização interativa.

- `git difftool branch1..branch2`: Compara duas branches usando uma ferramenta externa.

## Trabalhando com Submódulos

- `git submodule init`: Inicializa submódulos após clonar um repositório.

- `git submodule update`: Atualiza submódulos para as versões configuradas.

- `git submodule foreach`: Executa um comando em cada submódulo.

## Modificação de Histórico por Autor

- `git log --author="Nome do Autor"`: Exibe logs filtrados por autor.

- `git log --grep="Mensagem"`: Filtra logs por mensagens de commit.

## Desfazendo Commit Localmente

- `git reset HEAD~n`: Desfaz os últimos n commits, mantendo alterações no diretório de trabalho.

- `git revert -n HEAD~n`: Reverte os últimos n commits, permitindo edições antes de confirmar.

## Utilizando Git Rerere

- `git config --global rerere.enabled true`: Ativa o Rerere (Reuse Recorded Resolution).

- Ajuda a reutilizar resoluções de conflitos anteriores automaticamente.


## Arquivos Binários e LFS (Large File Storage)

- `git lfs`: Extensão do Git para gerenciar grandes arquivos binários.

- `git lfs install`: Configura o repositório para usar o Git LFS.

- `git lfs track "*.extensao"`: Rastreia arquivos específicos para o LFS.

## Merge e Diff Avançados

- `git mergetool`: Abre uma ferramenta externa para resolver conflitos de merge.

- `git merge-base branch1 branch2`: Encontra o commit base comum de duas branches.

## Visualização Gráfica do Histórico

- `git log --graph --all --oneline --decorate`: Visualiza o histórico de forma gráfica.

## Condições de Trabalho

- `git bisect`: Ajuda na busca do commit que introduziu um bug.

- `git bisect start` e `git bisect bad`/`git bisect good`: Utilizado durante o processo de bisect.

## Desabilitar o Uso do Fast Forward no Merge

- `git merge --no-ff branch`: Força a criação de um commit de merge, mesmo se não houver conflitos.

## Trabalhando com Reflogs

- `git reflog`: Exibe o log de referências, permitindo recuperar commits perdidos.

- `git reflog show nome-da-ramificacao`: Mostra o histórico de uma ramificação específica no reflog.

## Customizando Hooks Git

- Hooks são scripts executados automaticamente em resposta a eventos do Git.
   - Exemplo: `.git/hooks/pre-push` para executar ações antes do push.

## Ignorando Mudanças em Arquivos Rastreados

- `git update-index --skip-worktree arquivo`: Ignora mudanças locais em um arquivo rastreado.

- `git update-index --no-skip-worktree arquivo`: Para de ignorar alterações locais em um arquivo rastreado.

## Trabalhando com Configurações Locais

- `git config --local`: Configurações específicas do repositório.
   - Exemplo: `git config --local core.ignorecase true`

## Git Grep em Todo o Histórico

- `git grep "padrao" $(git rev-list --all)`: Procura por um padrão em todo o histórico.

## Desfazendo Mudanças Interativamente

- `git restore -p`: Permite descartar alterações interativamente.
   - Útil para selecionar partes específicas das mudanças a serem descartadas.

## Comandos Relacionados a Submódulos

- `git submodule sync`: Sincroniza submódulos para refletir as alterações no repositório pai.

- `git submodule update --remote`: Atualiza submódulos para as versões mais recentes configuradas.

## Desfazendo Alterações em um Único Arquivo

- `git checkout -- nome-do-arquivo`: Descarta alterações não commitadas em um arquivo específico.

## Recriando o Último Commit

- `git commit --amend --no-edit`: Adiciona alterações ao último commit sem modificar a mensagem.

## Estratégia de Merge Ours

- `git merge -s ours branch`: Realiza um merge considerando as alterações da branch atual como corretas.

## Restaurando um Arquivo de um Commit Anterior

- `git checkout commit-hash -- nome-do-arquivo`: Restaura um arquivo específico de um commit anterior.

## Utilizando Git Workflows Populares

- Git Flow: `git flow feature start nome-da-feature` para iniciar uma nova feature.

- GitHub Flow: Uso de branches principais, comumente `main` ou `master`, e pull requests.

## Análise de Alterações

- `git diff branch1..branch2`: Exibe as diferenças entre duas branches.

- `git diff --stat branch1..branch2`: Mostra estatísticas de alterações entre duas branches.

## Remover Alterações não Commitadas

- `git restore --source=HEAD --staged --worktree nome-do-arquivo`: Remove alterações do índice e do diretório de trabalho.

## Conflitos de Merge

- `git checkout --ours nome-do-arquivo` e `git checkout --theirs nome-do-arquivo`: Resolve conflitos de merge, escolhendo alterações da branch atual ou da branch sendo mesclada.

## Configurações Customizadas de Merge

- `git merge -X theirs branch`: Realiza um merge, priorizando as alterações da branch sendo mesclada em caso de conflito.

## Trabalhando com Shallow Clone

- `git clone --depth 1 URL-do-repositorio`: Cria um clone superficial, baixando apenas a última revisão.

## Mostrar Alterações em um Período Específico

- `git log --since="data" --until="data"`: Exibe os commits feitos em um período de tempo específico.

## Trabalhando com Subárvores

- `git subtree add --prefix pasta-subprojeto URL-do-repo-subprojeto branch`: Adiciona um subprojeto como uma subárvore.

- `git subtree pull --prefix pasta-subprojeto URL-do-repo-subprojeto branch`: Atualiza uma subárvore.

## Alterações Temporárias e Stash

- `git stash apply --index`: Aplica um stash, incluindo as alterações no índice.

- `git stash drop stash@{2}`: Remove um stash específico.

## Renomeando Arquivos

- `git mv arquivo-atual novo-nome`: Renomeia um arquivo no Git.

## Trabalhando com Refs Locais

- `git update-ref refs/heads/branch commit-hash`: Atualiza uma referência de branch localmente.

## Extraindo Patches

- `git format-patch -n HEAD~3`: Gera patches para os últimos 3 commits.

- `git apply --check meu-patch.patch`: Verifica se um patch pode ser aplicado com segurança.

## Desfazendo Rebase Interativo

- `git reflog expire --expire=now --all`: Limpa o reflog para evitar vazamento de objetos.

- `git reset --hard ORIG_HEAD`: Desfaz o último rebase interativo.

## Identificando Alterações Introduzidas por um Commit

- `git diff commit-hash^!`: Exibe as alterações introduzidas por um commit específico.

## Modificando a Mensagem de Vários Commits

- `git rebase -i HEAD~n`: Permite reescrever mensagens de commit em um rebase interativo.

## Ignorando Mudanças em um Arquivo Rastreado

- `git update-index --skip-worktree nome-do-arquivo`: Ignora alterações locais em um arquivo rastreado.

## Revertendo um Merge

- `git revert -m 1 commit-hash`: Reverte um commit de merge, mantendo uma das branches.

## Estratégias de Merge Personalizadas

- `git merge -s recursive -X ours branch`: Utiliza a estratégia recursiva com marcação de "ours" durante um merge.

## Corrigindo Commits na Branch Atual

- `git commit --fixup commit-hash`: Cria um commit de correção referente a um commit anterior.

- `git rebase -i --autosquash HEAD~n`: Consolida commits de correção durante um rebase interativo.

## Análise Estatística de Alterações

- `git log --stat`: Exibe estatísticas resumidas de alterações em cada commit.

## Desfazendo Alterações e Mantendo os Commits

- `git revert --no-commit commit-hash`: Desfaz um commit sem criar um novo commit imediatamente.

- `git cherry-pick -n commit-hash`: Aplica um commit sem realizar o commit imediatamente.

## Exibindo o Histórico em Formato Resumido

- `git log --pretty=oneline`: Exibe o histórico em uma linha por commit.

## Desfazendo o Último Commit sem Perder as Alterações

- `git reset --soft HEAD^`: Desfaz o último commit mantendo as alterações no diretório de trabalho.

## Corrigindo Erros em Commits Anteriores

- `git commit --amend --no-edit`: Adiciona alterações ao último commit sem modificar a mensagem.

## Trabalhando com Históricos Orfanados

- `git checkout --orphan nova-branch`: Cria uma nova branch com um histórico "órfão".

## Visualizando Diferenças com um Antigo Estado

- `git difftool HEAD~3..HEAD~1`: Abre uma ferramenta de diff para visualizar diferenças entre dois commits.

## Visualizando Commits que Afetam um Arquivo

- `git log -- nome-do-arquivo`: Exibe commits que alteraram um arquivo específico.

## Desfazendo um Commit e Mantendo as Alterações

- `git reset --soft HEAD~1`: Desfaz o último commit mantendo as alterações no índice.

## Refazendo o Histórico com Filtros

- `git filter-branch --commit-filter 'COMANDOS'`: Permite reescrever completamente o histórico.

## Desfazendo Todas as Alterações Locais

- `git reset --hard HEAD`: Descarta todas as alterações locais e sincroniza com o último commit.

## Comandos para Trabalho Remoto

- `git remote add nome-remoto URL-do-repo-remoto`: Adiciona um repositório remoto.
  - Exemplo: `git remote add origin https://github.com/seu-usuario/seu-repositorio.git`

- `git remote -v`: Exibe URLs dos repositórios remotos configurados.

- `git push -u origin branch`: Define a branch padrão para push.
  - Exemplo: `git push -u origin main`

- `git pull origin branch`: Atualiza o repositório local com as alterações do repositório remoto.

## Trabalhando com Tags

- `git tag nome-da-tag`: Cria uma tag leve (apontador para um commit).
  - Exemplo: `git tag v1.0.0`

- `git tag -a nome-da-tag -m "Mensagem da Tag"`: Cria uma tag anotada (commit identificado por uma tag).
  - Exemplo: `git tag -a v1.0.0 -m "Versão 1.0.0"`

- `git push origin nome-da-tag`: Envia uma tag para o repositório remoto.

## Visualizando Diferenças entre Dois Commits

- `git diff commit1 commit2`: Exibe as diferenças entre dois commits.
  - Exemplo: `git diff HEAD~3 HEAD~1`

## Desfazendo Mudanças no Staging Area

- `git restore --staged nome-do-arquivo`: Remove um arquivo do staging area, mantendo as alterações no diretório de trabalho.

## Removendo Arquivos do Repositório

- `git rm nome-do-arquivo`: Remove um arquivo do repositório e do diretório de trabalho.

- `git rm --cached nome-do-arquivo`: Remove um arquivo do repositório, mas mantém no diretório de trabalho.

## Anexando Mensagens Adicionais ao Último Commit

- `git commit --amend -m "Nova mensagem"`: Adiciona mensagens ao último commit sem criar um novo commit.

## Listando Todas as Tags com Anotações

- `git show-ref --tags`: Lista todas as tags com anotações no repositório.
- 

## Trabalhando com Refs Remotas

- `git ls-remote`: Lista refs remotas.

- `git fetch --prune origin`: Atualiza e remove refs remotas obsoletas.

## Configurando Variáveis de Ambiente

- `GIT_COMMITTER_DATE="data" git commit --amend --no-edit`: Modifica a data do commit durante um amend.

## Trabalhando com Submódulos e Commits Específicos

- `git submodule update --remote`: Atualiza submódulos para a versão mais recente.

- `git submodule update --checkout`: Garante que os submódulos estejam no commit correto.

## Visualizando o Histórico de um Arquivo

- `git log -p nome-do-arquivo`: Exibe o histórico de alterações de um arquivo.

## Trabalhando com Hooks de Servidor Git

- Hooks no lado do servidor podem ser usados para automatizar ações em um repositório central.

## Forçando o Push

- `git push --force origin branch`: Força o push de uma branch, substituindo a versão remota.

## Comandos Avançados de Busca em Logs

- `git log --grep="padrao" --author="autor"`: Filtra logs por mensagem e autor.

- `git log -S"texto"`: Procura por mudanças que introduzem ou removem uma determinada string.

## Anexando Mensagens a Commits Anteriores

- `git notes add -m "Nota para commit" commit-hash`: Adiciona notas a commits.

- `git show --show-notes`: Exibe notas anexadas a commits.

## Desfazendo Alterações Locais e Resetando Commits

- `git reset --hard HEAD`: Descarta todas as alterações locais e reseta para o último commit.

- `git reset --soft HEAD~n`: Desfaz os últimos n commits, mantendo as alterações no diretório de trabalho.

- `git revert commit-hash`: Cria um novo commit que reverte as alterações de um commit específico.

## Trabalhando com Submódulos

- `git submodule add URL-do-repo`: Adiciona um submódulo ao seu repositório.

- `git submodule init`: Inicializa submódulos após clonar um repositório.

- `git submodule update`: Atualiza submódulos para as versões configuradas.

## Alterando a Origem do Repositório Remoto

- `git remote set-url origin nova-URL`: Altera a URL do repositório remoto.

## Utilizando Hooks

- Hooks são scripts que são executados automaticamente em determinados eventos do Git.

- Exemplo de um hook pós-commit: `.git/hooks/post-commit`

## Git Workflows Populares

- **Gitflow Workflow**: Um modelo de branch que define um rigoroso processo de branch para cada tipo de funcionalidade.

- **GitHub Flow**: Um modelo mais simples com uma única branch principal, geralmente chamada de `main` ou `master`, e o uso de pull requests.

- **GitLab Flow**: Similar ao GitHub Flow, mas inclui ambientes de deploy para cada branch.

## Revertendo para um Estado Específico

- `git checkout commit-hash -- .`: Restaura o estado de todos os arquivos para um commit específico.

- `git reset --hard commit-hash`: Reseta para um commit específico, descartando todas as alterações locais.

## Trabalhando com Stashes

- `git stash list`: Lista todos os stashes disponíveis.

- `git stash apply`: Aplica o último stash.

- `git stash drop`: Remove o último stash.

- `git stash pop`: Aplica e remove o último stash.

## Trabalhando com Históricos Específicos

- `git log --since="YYYY-MM-DD" --until="YYYY-MM-DD"`: Exibe os commits feitos em um período de tempo específico.

- `git log nome-do-arquivo`: Exibe o histórico de um arquivo específico.

## Desfazendo Alterações Locais de Forma Seletiva

- `git restore -p`: Permite descartar alterações interativamente, selecionando partes específicas das mudanças a serem descartadas.

## Trabalhando com Variáveis de Ambiente

- `GIT_COMMITTER_DATE="YYYY-MM-DDTHH:MM:SS" git commit --amend --no-edit`: Modifica a data do commit durante um amend.

## Personalizando a Mensagem de Confirmação de Merge

- `git merge --no-edit -m "Nova mensagem" branch`: Realiza um merge e altera a mensagem de commit padrão.

## Utilizando Git Bisect Automatizado

- `git bisect start`: Inicia o processo de bisect.

- `git bisect bad` e `git bisect good`: Marca pontos ruins e bons durante a bisect.

- `git bisect reset`: Conclui o processo de bisect.

## Exibindo Alterações com Números de Linhas

- `git log -p -U0`: Exibe alterações com números de linha em vez de contexto.

- `git blame -L10,20 nome-do-arquivo`: Exibe quem modificou as linhas 10 a 20 de um arquivo.


## Visualizando Arquivos Não Rastreados

- `git ls-files --others --exclude-standard`: Lista arquivos não rastreados no diretório de trabalho.

## Listando Tags Ordenadas por Data

- `git tag --sort=-committerdate`: Lista tags ordenadas por data de commit.

## Utilizando Git para Download de Arquivos

- `git archive --remote=URL-do-repo --format=tar branch | tar -xf -`: Baixa um arquivo específico de um repositório Git.

## Ignorando Alterações em um Arquivo Já Rastreado

- `git update-index --assume-unchanged nome-do-arquivo`: Ignora alterações futuras em um arquivo já rastreado.

## Visualizando Diferenças com Arquivos Binários

- `git diff --binary commit1 commit2`: Exibe as diferenças entre dois commits, incluindo arquivos binários.


## Trabalhando com Refs

- `git tag -d nome-da-tag`: Exclui uma tag localmente.

- `git push origin --delete nome-da-tag`: Remove uma tag de um repositório remoto.

- `git show-ref`: Exibe referências no formato longo.

## Encontrando o Commit que Introduziu uma Determinada Linha

- `git blame -Llinha,linha nome-do-arquivo`: Exibe quem modificou uma linha específica de um arquivo e em qual commit.

- `git bisect run comando`: Automatiza o processo de bisect.

## Trabalhando com Submódulos Git

- `git submodule status`: Exibe o status dos submódulos.

- `git submodule foreach 'comando'`: Executa um comando em cada submódulo.

## Mostrando Alterações sem Confusão

- `git log --graph --oneline --all`: Exibe o histórico em um formato gráfico mais compacto.

## Utilizando Alias Avançados

- `git config --global alias.nome-do-alias 'comando-git'`: Cria alias para comandos frequentemente usados.

## Desfazendo um Rebase Interativo

- `git rebase --abort`: Abandona um rebase interativo em andamento.

- `git rebase --continue` e `git rebase --skip`: Continua ou pula commits durante um rebase interativo.

## Criando um Patch de Stash

- `git stash show -p stash@{2} > nome-do-arquivo.patch`: Cria um patch a partir de um stash específico.

- `git apply < nome-do-arquivo.patch`: Aplica um patch gerado pelo stash.


