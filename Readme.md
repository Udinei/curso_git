## Git e Github 

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

`git checkout ` - Pode ser utilizado de varias formas ver sessão Git Checkout

`git show <hash>` - Exibe as alterações do commit informado no hash

`git diff` - Exibe por linha todas as alterações executadas nos arquivos

`git diff --name-only` - exibe somente os nomes dos arquivos que foram modificados

`git reset --soft <hash>` - apaga do repositorio e do historico todos commits acima das hash e volta as alterações anteriormente feitas para o stage

`git reset --mixed <hash>` - apaga do repositorio e do historico todos commits acima das hash e volta os arquivos para unstage 

`git reset --hard <hash>` -  apaga do repositorio e do historico todos commits acima das hash e as alterações feitas nos arquivos

`git revert <hash>` - vai para um commit informado assumindo-o como o atual, sem pagar os commits já feitos


`git config credential.helper store` - Armazena suas credenciais do git no disk, evitando ter que digitar login e senha toda vez que fizer commit no github



### Comando Git Checkout
`git checkout -b nome-branch` - Cria uma nova branch em seguida o checkout é feito

`git checkout nova-branch` - Cria localmente a branch master (remota)

`git checkout <hash>` - posiciona o cursor do git num commit especifico


### Comandos para conectar repositorio local ao repositorio remoto (github)

`git remote add origin https://github.com/OWNER/REPOSITORY.git` - Adiciona (conecta) pasta local ao repositorio remoto em seguida o comando abaixo deve ser executado.

`git push -u origin master` - Seta repositorio origin como repositorio master de versionamento (-u somente a primeira vez que fizer o push)

### Comandos para desconectar repositorio local do repositorio remoto (github)
`git remote -v` - Exibe o nome e endereço dos repositorios remotos, os quais a pasta local versionada pelo git esta conectada

`git remote rm <nameRepository>` - Desconecta a pasta local versionada pelo git do repositorio remotos informado
