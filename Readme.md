### Git e Github 

## Comandos básicos do git
`git init` - Sinaliza que a pasta atual e os arquivos criados nela serão versionados pelo git. Esse comando cria uma pasta oculta chamada .git

`git add` - Adiciona arquivos ou pastas ao controle do git

`git commit` - Adiciona um ponto na linha do tempo de controle do git

`git log` - Exibe os pontos de controle da linha do tempo

`git status` - Exibe o estado das alterações enviadas ao git

`git config credential.helper store` - Armazena suas credenciais do git no disk, evitando ter que digitar login e senha toda vez que fizer commit no github


## Comandos para conectar repositorio local ao repositorio remoto (github)

`git remote add origin https://github.com/OWNER/REPOSITORY.git` - Adiciona (conecta) pasta local ao repositorio remoto em seguida o comando abaixo deve ser executado.

`git push -u origin master` - Seta repositorio origin como repositorio master de versionamento

## Comandos para desconectar repositorio local do repositorio remoto (github)
`git remote -v` - Exibe o nome e endereço dos repositorios remotos, os quais a pasta local versionada pelo git esta conectada
`git remote rm <nameRepository>` - Desconecta a pasta local versionada pelo git do repositorio remotos informado
