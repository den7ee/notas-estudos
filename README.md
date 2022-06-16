# Guia de comandos básicos Git/GitHub + Extra - Desafio Bootcamp Impulso

## Sobre
Esse guia de comandos básicos tem como objetivo facilitar a execução de comandos necessários para:
- Gerar um par de chaves ssh ed25519;
- Exibir o valor da chave pública para colar no GitHub;
- Inicilizar ssh-agent para admistrar as chaves geradas;
- Instalar o Git no Debian;
- Iniciar um repositório Git em um diretório local;
- Verificar status de alterações do respositório;
- Adicionar as alterações de 'Working Area' para 'Staging Area' do Git;
- Comitar as alterações de 'Staging Area' para 'Local Repository' do Git;
- Adicionar respositório remoto do GitHub ao nosso repositório local do Git;
- Verificar repositórios remotos do Git;
- Empurar as alterações de 'Local Repository' do Git para 'Remote Repository' (GitHub);
- Puxar do 'Remote Repository' (GitHub) para 'Local Repository' do Git;
- Extra;

## Sobre o Git
Git é um sistema livre de controle de versão criado por Linus Torvalds em 2005 como uma alternativa ao CVS no desenvolvimento do Kernel Linux;

Por ser um sistema seguro e distribuído o Git foi adotado por muitos outros projetos;

## Sobre o GitHub
GitHub é uma plataforma de hospedagem de código-fonte e arquivos com controle de versão usando o Git;

Foi criado em 2008 e adquirido pela Microsoft em 2018;

## Sobre a chave ssh
Para empurrar as alterações do repositório local (Local Repository no Git) para o repositório local no GitHub é necessário uma conexão ssh;

Essa foi uma alteração feita no GitHub em 2021, antes disso era possível o push apenas com username e senha do GitHub;

Para criar a chave ssh do GitHub vai em Settings no seu perfil/SSH and GPG keys.

# Gerar um par de chaves ssh ed25519;
## ssh-keygen -t ed25519 -C
Esse comando precisa do e-mail de login do GitHub para funcionar;

Ele gera um par de chaves, uma pública e outra privada com o nome: ed25519 com tipo de criptografia SHA256;

Após o comando é informado o local onde as chaves foram criadas;

Depois disso será solicitado uma senha 2x;

# Exibir o valor da chave pública para colar no GitHub;
## cat id_
Esse comando deve ser feito no diretório que foi informado no comando ssh-keygen;

Ele deve ser completado com o arquivo nomedachave.pub;

Esse comando irá exibir token da chave gerada;

Cole em: Settings/SSH and GPG keys no GitHub após clicar em: New SSH key e dar um nome para identificar a sua chave ssh; 

# Inicilizar ssh-agent para admistrar as chaves geradas
## $(ssh-agent -s)
O comando irá retornar o pid de números de um Agent;

Ele deve ser executado no diretório onde está o par de chaves ssh;

# Instalar o Git no Debian;
## apt-get install git
O Git pode ser instalado em Linux, OSx e Windows;

No site oficial https://git-scm.com/ está detalhado a instalação para cada sistema operacional;

# Iniciar um repositório Git em um diretório local
## git init
Tudo começa com esse comando, ele cria um repositório no Git com uma pasta oculta .git/;

Repositório é a como o Git chama os diretórios, dentro do Git: repositório, fora: diretório;

Após o comando o git init o Git começa a verificar as alterações no diretório em que o comando foi dado;

O Git trabalha com 3 repositório áreass: Working Area, Stangig Area e Repositório Local;

# Verificar status de alterações do respositório
## git status
Com esse comando podemos verificar o status do Git no projeto;

Criamos o arquivo NovoArquivo.md e digitamos git status;

Ele irá mostrar que um NovoArquivo.md foi criado e sugerir o comando git add;

# Adicionar as alterações de Working Area para Staging Area
## git add
Esse comando move as alterações que foram identificadas em Working Area para Stanging Area;

Novamente com o comando git status podemos ver que o Git identificou que as alterações agora estão adicionadas na Stanging Area e sugere um commit delas;

# Comitar as alterações de Staging Area para Local Repository
## git commit
Com esse comando as alterações foram movidas da Stangig Area para Local Repository;

Usamos o comando git status para verificar o status do git no diretório;

O Git irá informar que não há alterações a serem adicionadas com o comando git add (Recomeça o ciclo);

# Adicionar respositório do remoto do GitHub ao nosso repositório local
## git remote add origin 
Com esse comando adicionamos o nosso respositório do remoto do GitHub ao nosso repositório local;

Esse comando precisa do link do repositório que foi criado no GitHub;

Origin é um alias para o link;

## Verificar repositórios remotos;
## git remote -v
Esse comando verifica os repositórios remoto, no caso o GitHub;

# Empurar as alterações de Local Repository para Remote Repository (GitHub)
## git push
Esse comando empurra as alterações que estão no diretório local para o diretório remoto;

# Puxar do Remote Repository (GitHub) para Local Repository  
# git pull
Esse comando puxa o diretório remoto para o diretório local;

# Extra
## Como o Git identifica as alterações?
Após o comando git init o SHA1 (Secure Hash Algorithms), produz um número hexadecimal de 40 dígitos;

Cada alteração feita no diretório altera também o número hexadecimal, dessa forma o Git consegue identificar uma alteração;

O começo de cada código hexadecimal do arquivo pode ser visto no GitHub próximo ao botão Code;

Esse código hexadecimal é único para cada ojeto dentro do Git (Blobs, Trees e Commits);

Commits são um conjunto de Trees que são um conjunto de Blobs;

