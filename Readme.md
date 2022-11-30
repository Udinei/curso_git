## Git e Github 

### Configuração inicial após instalação

git config --global user.name "Fulano de Tal"

git config --global user.email fulanodetal@exemplo.br


### Visualizando as configurações atuais

`git config --list` -  Lista todas as configurações atuais do Git, para sair do comando digite `q`

### Criando o .gitignore e README.md

`touch .gitignore` - Cria o arquivo .gitignore no diretorio corrente  
Possivel conteudo para .gitignore:   
`target/` 

`touch README.md` - Cria o arquivo README.md no diretorio corrente

Escrevendo no arquivo README.md   
echo "# groovy-introducao" >> README.md



### Comandos básicos do git

`git init` - Sinaliza que a pasta atual e os arquivos criados nela serão versionados pelo git. Esse comando cria uma pasta oculta chamada .git

`git add .` - Adiciona arquivos ou pastas(novos ou alterados) ao controle de versão do git

`git status` - Exibe a situação atual dos arquivos repositorio

`git log` - Exibe informações dos arquivos e pastas já versionados pelo git

`git log --decorate` - 

`git log --author="nomeAutor"` - Exibe o hash dos commits, data, nome do autor e comentários 

`git shortlog -sn` - Exibe quantidade de commits por autores

`git log --graph` - Exibe de forma gráfica o que aconteceu na branch (merge, add, branch criada, etc...)

`git commit -m "comentario"` - Adiciona um ponto de controle na linha do tempo do git

`git commit -am "comentario"` - (caso arquivos alterados já exista)

`git push` -- das proximas vez para subir as alterações basta digitar somente esse comando

`git pull` - incorpora mudanças de um repositório remoto para o branch local

`git checkout ` - Pode ser utilizado de varias formas ver sessão Git Checkout

`git show <hash>` - Exibe as alterações do commit informado no hash

`git diff` - Exibe por linha todas as alterações executadas nos arquivos

`git diff --name-only` - exibe somente os nomes dos arquivos que foram modificados

`git reset --soft <hash>` - apaga do repositorio e do historico todos commits acima das hash e volta as alterações anteriormente feitas para o stage

### Alterando coisas no Git
`git commit --amend`  - Para alterar a mensagem do ultimo commit. O Git vai abrir o editor, com o conteúdo da mensagem do último commit e você pode editar e salvar e executar o comando para atulizar remotamente  `git push --force` 

 `git push --force` - Força commit no repositorio remoto

`git reset --mixed <hash>` - apaga do repositorio e do historico todos commits acima das hash e volta os arquivos para unstage 

`git reset --hard <hash>` -  apaga do repositorio e do historico todos commits acima das hash e as alterações feitas nos arquivos

`git revert <hash>` - vai para um commit informado assumindo-o como o atual, sem pagar os commits já feitos


`git config credential.helper store` - Armazena suas credenciais do git no disk, evitando ter que digitar login e senha toda vez que fizer commit no github

`git rm nomefile` - Remove arquivo do controle de versão do git (O arquivo não é removido fisicamente)

`git check-ignore -v -n --no-index nomefile` - Excluir um arquivo de ser incluso no controle de versão do git

### Desfazendo alterações locais
`git restore .` - Para descartar as alterações em todos os arquivos no diretório atual

`git restore '.js'` - Para descartar as alterações em todos os arquivos *.js do diretório atual


### Comando Git Checkout
`git checkout -b <branch>` - Cria uma nova branch a partir da branch atual, e posicina na nova branch

`git checkout nova-branch` - Cria localmente a branch master (remota)

`git checkout <hash>` - posiciona o cursor do git num commit especifico

### Comando git push
`git push -u origin <branch>` - Envia nova branch local criada com o comando acima para o github

Nota: se o comando acima exibir a msg abaixo:
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. Integrate the remote changes (e.g.
hint: 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

Com cautela usar o comando abaixo, para forçar o commit, ter certeza de já ter feito o pull antes:
`git push -f origin main`


### Estratégia de merge fast-foward (quando não há conflitos entre os branches envolvidos)
No branch (feature) atualiza-o com o conteúdo de master
`git rebase master`
 
Posicionar no branch master 
`git checkout master` - indo para o branch do master
 
No branche master fazer merge com branche feature
`git merge feature`    - fazendo o merge entre o master e o feature

## Removendo branchs remota
`git push origin --delete <branch>`

## Removendo branchs local
`git branch -d <branch>`

### Comandos para conectar repositorio local ao repositorio remoto (github)

`git remote add origin https://github.com/OWNER/REPOSITORY.git` - Adiciona (conecta) pasta local ao repositorio remoto em seguida o comando abaixo deve ser executado.

`git push -u origin master` - Seta repositorio origin como repositorio master de versionamento (-u somente a primeira vez que fizer o push)

### Comandos para desconectar repositorio local do repositorio remoto (github)
`git remote -v` - Exibe o nome e endereço dos repositorios remotos, os quais a pasta local versionada pelo git esta conectada

`git remote rm <nameRepository>` - Desconecta a pasta local versionada pelo git do repositorio remotos informado



### Vim editor de textost 
O Vim possui dois modos de operação:

`i` - Entra em modo de edição, também pode ser usado `a` 

`Esc` - Entra em modo de comando

###  Vim salvando o arquivo
Entrar em modo de comando `Esc` e digitar dois pontos `:`

`:w` - Salva o arquivo, também pode ser usado `ZZ` 
       nos dois caso pode passar um argumento. Ex: :w nomeArq.txt

`:wq` - Salva o arquivo e sai do Vim

`:w!` - O arquivo será salvo mesmo se aberto no modo somente leitura 
        (readonly)

`:q` - Sai do Vim. Se o arquivo não foi salvo, o programa emitirá um 
       alerta.

`:q!` - Força a saída, mesmo que o arquivo tenha sido modificado e não 
        tenha sido salvo anteriormente

###  Vim editando textos (deve-se estar em modo de comando - Esc)

`dd` - Apaga a linha do cursor       

`dw` - Apaga a palavra que esta o cursor 

`y` - Copia a linha para a memoria

`yy` - Copia a linha para a área de transferência

`yw` - Copia a palavra a partir da posição do cursor para a memoria

`p` - Colar o texto da memoria ou da área de transferencia para posição do cursor 




