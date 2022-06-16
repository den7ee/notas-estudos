# Guia de comandos básicos Git/GitHub - Desafio Bootcamp Impulso

# Sobre
Esse guia de comandos básicos tem como objetivo facilitar a execução de comandos necessários para:
- Criar um par de chaves ssh ed25519;
- 
- Instalar o Git no Debian;
- Iniciar um repositório Git em um diretório local;
- Verificar status de alterações do respositório;
- Adicionar as alterações de Working Area para Staging Area;
- Comitar as alterações de Staging Area para Local Repository;
- Empurar as alterações de Local Repository para Remote Repository(GitHub);

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

## chave ssh
Para empurrar as alterações do repositório local (Local Repository no Git) para o repositório local no GitHub é necessário uma conexão ssh;

Essa foi uma alteração feita no GitHub em 2021, antes disso era possível o push apenas com username e senha do GitHub;

Para criar a chave ssh do GitHub vai em Settings no seu perfil/SSH and GPG keys.

## ssh-keygen -t ed25519 -C
Esse comando precisa do e-mail de login do GitHub para funcionar;

Ele gera um par de chaves, uma pública e outra privada com o nome: ed25519 com tipo de criptografia SHA256;

Após o comando é informado o local onde as chaves foram criadas;

Depois disso será solicitado uma senha 2x;

## cat id_
Esse comando deve ser feito no diretório que foi informado no comando ssh-keygen;

Ele deve ser completado com o arquivo nomedachave.pub;

Esse comando irá exibir token da chave gerada;


## SSH and GPG keys
É nesse local onde vai ficar a chave SSH no GitHub;

Uma nova chave é criada clicando na opção: New SSH key;

Digite o nome para identificar a chave e cole o token de ssh gerado com o comando cat id_;


## git remote add origin 
Com esse comando adicionamos o nosso respositório do remoto do GitHub ao nosso repositório local;

Esse comando precisa do link do repositório que foi criado no GitHub;

Origin é um alias para o link;

## git remote -v
Esse comando verifica os repositórios remoto, no caso o GitHub;

## git push
Esse comando empurra as alterações que estão no diretório local para o diretório remoto;

## git pull
Esse comando puxa o diretório remoto para o diretório local;
