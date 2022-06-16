# Guia de comandos Git/GitHub - Desafio Bootcamp Impulso

# Sobre o Git
Git é um sistema livre de controle de versão criado por Linus Torvalds em 2005 como uma alternativa ao CVS no desenvolvimento do Kernel Linux;

Por ser um sistema seguro e distribuído o Git foi adotado por muitos outros projetos;

## Instalando 
O Git pode ser instalado em Linux, OSx e Windows;

No site oficial https://git-scm.com/ está detalhado a instalação para cada sistema operacional, aqui será o Linux Debian 11;

No terminal digite:# apt-get install git;

## git init
Tudo começa com esse comando, ele cria um repositório no Git com uma pasta oculta .git/;

Repositório é a como o Git chama os diretórios, dentro do Git: repositório, fora: diretório;

Após o comando o git init o Git começa a verificar as alterações no diretório em que o comando foi dado;

O Git trabalha com 3 repositório áreass: Working Area, Stangig Area e Repositório Local;

## git status
Com esse comando podemos verificar o status do Git no projeto;

Criamos o arquivo NovoArquivo.md e digitamos git status;

Ele irá mostrar que um NovoArquivo.md foi criado e sugerir o comando git add;

## git add
Esse comando move as alterações que foram identificadas em Working Area para Stanging Area;

Novamente com o comando git status podemos ver que o Git identificou que as alterações agora estão adicionadas na Stanging Area e sugere um commit delas;

## git commit
Com esse comando as alterações foram movidas da Stangig Area para Local Repository;

Usamos o comando git status para verificar o status do git no diretório;

O Git irá informar que não há alterações a serem adicionadas com o comando git add (Recomeça o ciclo);


# Sobre o GitHub
GitHub é uma plataforma de hospedagem de código-fonte e arquivos com controle de versão usando o Git;

Foi criado em 2008 e adquirido pela Microsoft em 2018;

## git remote add origin 
Com esse comando adicionamos o nosso respositório do remoto do GitHub ao nosso repositório local;

Esse comando precisa do link do repositório que foi criado no GitHub;

Origin é um alias para o link;

## git remote -v
Esse comando verifica os repositórios remoto, no caso o GitHub;

## git push
Esse comando empurra as alterações que estão no diretório local para o diretório remoto;


