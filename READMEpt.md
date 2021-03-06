Comandos Git
============

## Versões traduzidas
- [English version (original)](README.md)

___

_Uma lista dos comandos Git mais usados_

*Se você está interessado em meus aliases do Git, dê uma olhada no meu `.bash_profile`, encontrado aqui: https://github.com/joshnh/bash_profile/blob/master/.bash_profile*

--

### Obtendo & Criação de Projetos

| Comando | Descrição |
| ------- | --------- |
| `git init` | Inicializa um repositório Git local |
| `git clone ssh://git@github.com/[usuario]/[nome-repositorio].git` | Cria uma cópia local de um repositório remoto |

### Básicos

| Comando | Descrição |
| ------- | --------- |
| `git status` | Checa o status |
| `git add [nome-arquivo.txt]` | Adiciona um arquivo para área de stage |
| `git add -A` | Adiciona todos os arquivos novos ou modificados para a área de stage |
| `git commit -m "[Mensagem de Commit]"` | Comita as alterações |
| `git rm -r [nome-arquivo.txt]` | Remove um arquivo (ou pasta) |

### Branching & Merging

| Comando | Descrição |
| ------- | --------- |
| `git branch` | Lista as branches (o asterisco denota a branch atual) |
| `git branch -a` | Lista todas as branches (local e remoto) |
| `git branch [nome da branch]` | Cria uma nova branch |
| `git branch -d [nome da branch]` | Deleta uma branch |
| `git push origin --delete [nome da branch]` | Deleta uma branch remota |
| `git checkout -b [nome da branch]` | Cria uma nova branch e muda para ela |
| `git checkout -b [nome da branch] origin/[nome da branch]` | Clona uma branch remota e muda para ela |
| `git checkout [nome da branch]` | Seleciona uma branch |
| `git checkout -` | Muda para a última branch |
| `git checkout -- [nome-arquivo.txt]` | Descarta modificações de um arquivo |
| `git merge [nome da branch]` | Faz um merge de uma branch na branch atual |
| `git merge [source branch] [branch alvo]` | Faz um merge de uma branch em outra branch |

### Stashing

| Comando | Descrição |
| ------- | --------- |
| `git stash` | cria uma branch temporária contendo a versão atual do seu projeto |
| `git stash list` | Lista todos os stash’s criados  |
| `git stash apply` | Restaurar todas as modificações da ultima entrada stash |
| `git stash apply @{id}` | Restaurar todas as modificações da entrada id |
| `git stash branch <nome-da-branch>` | Criar uma branch a partir do ultimo stash |
| `git stash branch <nome-da-branch> stash@{id}` | Criar uma branch a partir do stash ID |
| `git stash clear` | Remove todas as entradas 'stash' |
| `git stash show` | Lista todos os arquivos modificados no ultimo stash |
| `git stash create <mensagem> OU git stash save <mensagem>` | Cria um stash com uma mensagem personalizada |

### Sharing & Updating Projects

| Comando | Descrição |
| ------- | --------- |
| `git push origin [nome da branch]` | Enviar uma branch para seu repositório remoto |
| `git push -u origin [nome da branch]` | Envia as alterações da branch informada para um repositório remoto (and selecionar a branch) |
| `git push` | Envia as alterações para o repositório remoto (branch atual) |
| `git push origin --delete [nome da branch]` | Deletar uma branch remota |
| `git pull` | Atualiza o repositório local para o último commit |
| `git pull origin [nome da branch]` | Recebe alterações do repositório remoto |
| `git remote add origin ssh://git@github.com/[usuario]/[nome-repositorio].git` | Adicionar um repositório remoto |
| `git remote set-url origin ssh://git@github.com/[usuario]/[nome-repositorio].git` | Seta um repositório da origin branch para o SSH |

### Inspeção & Comparação

| Comando | Descrição |
| ------- | --------- |
| `git log` | Ver modificações |
| `git log --summary` | Ver modificações (detalhadas) |
| `git log --oneline` | Ver modificações linha a linha |
| `git log --branches` | Ver modificações de todas as branches |
| `git diff [branch original] [branch alvo]` | Visualizar alterações antes de mesclar |

