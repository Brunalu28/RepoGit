# *Bem vindo ao RepoGit!* 📝
Esse repositório é dedicado a ensinar como usar o git e github de forma prática desde o básico ao avançado.

- O `git` é um sistema open source de versionameto de código, ele cria uma linha do tempo com base nas alterações que forem feitas em um projeto, é possível ter o controle de cada alteração. Utilizar o git é a melhor forma de gerernciar código, principalmente se estiver sendo desenvolvido por mais de uma pessoa. 

- Já o `github` é o serviço que hospeda os repositórios git que você desenvolveu, além dele também temos o `gitlab`que tem o mesmo objetivo, só que possui algumas ferramentas extras como suporte para a criação de Wikis de projetos e plataforma para gerenciamento de tarefas (Passagem de issues para os membros de um projeto, boards para atualizar o andamento das demandas).

## Instalando o git 📥: 
- O primeiro passo para usar essas ferramentas é a instalação do git na sua máquina, esse passo pode ser feito através do link a seguir:
  
    - [link de Instalação](https://git-scm.com/downloads)

## Configurando seu usuário 💁🏻‍♀️:

Logo depois de fazer a instalação é importante fazer a configuração do seu usuário, para isso use o comando `git config`, adicionando seu nome e email que serão empregados a cada commit.

- Use esses comandos no git bash ou em algum terminal.

`$ git config –global user.name “Seu nome”`

`$ git config –global user.email “Seu email”`
      
## Criando um projeto ▶️:

Temos duas opções, a primeira é de criar primeiro o repositório na sua máquina e depois adicionar ao github, a segunda é criar o repositório no github antes.

### 1. Localmente:

- Inicialmente crie uma pasta em seu notebook;
- Entre nessa pasta e crie algum arquivo, adicione alguma coisa para testar;
- Salve as alterações.

Agora é preciso tornar essa pasta um projeto git, pra isso usamos o `git init`, você pode executar esse comando já dentro da pasta ou fora, expecificando o nome.

`$ git init <O nome do seu repositório>`

- Esse comando cria a pasta `.git`.

Logo em seguida vamos adicionar nossas alterações na área de staging, para isso usamos o comando `git add` que adiciona os arquivos criados e alterados em uma área de preparação para o próximos passos, que é unir esses arquivos ao repositório remoto.

`$ git add <O nome do arquivo criado ou modificado>`  // Adiciona o arquivo para a área de stagging.

`$ git add .` // Adiciona todos os arquivos modificado/criados para a área de stagging.

Depois disso, vamos realizar o commit, ele captura as mudanças que foram adicionadas no stagging, além disso eles representam os pontos na linha do tempo do seu projeto.

`$ git commit -a`  // Une o `add .` ao commit. 

`$ git commit -m "Mensagem do commit"`  // Com o -m é possível adicionar mensagens sobre o commit.

