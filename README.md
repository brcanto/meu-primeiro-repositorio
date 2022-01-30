## Desafio - Meu primeiro repositório

### Criando um repositorio no Github para praticar o que foi visto no curso da DIO Introdução do Git e ao GItlab.

Agradecimentos aos professores pela excelente aula!

Rodrigo L. Canto (rodrigocanto@gmail.com)

**Comandos básicos:**

Dentro do Git Bash

**Gerando uma chave no diretorio do usuario**:

#ssh-keygen -t ed25519 -C rodrigocanto@gmail.com

um par de chaves (1 publica e 1 privada) será gerada dentro do diretorio do %users%/.ssh

**Enviando a chave publica para o Github:**

copie o conteúdo da chave publica (%user%/.ssh/chave.pub)

No Github clique no icone redondo no canto superior direito, depois em **Settings**. No menu esquerdo, clique em **SSH e GPG Keys**. Clique então em **New SSH Key**. Coloque o nome para identificar o dispositivo que acessará o repositório remoto e em **key** cole a chave publica.

**Iniciando o agente ssh:**

#eval $(ssh-agent -s)

#ssh-add \<caminho_e_nome_da_chave_privada\>

OBS: pode deixar a senha em branco (apenas para repositorio publico)

**Para testar, abra um repositorio no Github e no botão Code (em verde) copie o codigo para acesso ssh. No Git Bash da maquina local, use o seguinte comando para clonar o repositorio remoto para o local:**

git clone \<codigo_ssh>

**Para inicializar um repositorio localmente, entre na pasta onde sera o repositório e digite o comando:**

#git init

**Configurando o repositorio:**

#git config --global user. email \<rodrigocanto@gmail.com\>

#git config --global user.name \<brcanto\>

**Para visualizar os parâmetros de configuração:**

#git config --list

**Alterando os parametros de configurações (unset):**

#git config --global --unset user. email \<rodrigocanto@gmail.com\>

#git config --global --unset user.name \<brcanto\>

OBS: onde rcanto é o mesmo usuário no Github.

A fim de facilitar a edição do arquivo **index.md**, é interessante utilizar um **editor de markdown. Dica, o Mark Text é free.

**Para inserir todos arquivos da pasta corrente em Staged:**

#git add *

**Para efetivar o commit na pasta:**

#git commit -m "mensagem que identifica o commit"

**Para empurrar as alterações dos repositorios locais para os repositorios remoto:**

#git push origin master

ou

#git push origin main

**Para consultar o estado dos arquivos do repositorio localmente:**

#git status

**Para incluir um repositorio remoto no github copie o Code https do repositorio e no Git bash execute o comando:**

#git remote add origin \<code https\>

**Para visualizar os repositorios remotos configurados:**

#git remote -v


