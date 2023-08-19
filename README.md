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

### `git init`

Agora é preciso tornar essa pasta um projeto git, para isso você pode executar esse comando já dentro da pasta ou fora, expecificando o nome.

`$ git init <O nome do seu repositório>`

- Esse comando cria a pasta `.git`.

### `git add`

Logo em seguida vamos adicionar nossas alterações na área de staging, para isso usamos o comando que adiciona os arquivos criados e alterados em uma área de preparação para o próximos passos, que é unir esses arquivos ao repositório remoto.

`$ git add <O nome do arquivo criado ou modificado>`  // Adiciona o arquivo para a área de stagging.

`$ git add .` // Adiciona todos os arquivos modificado/criados para a área de stagging.

### `git commit`

Depois disso, vamos realizar o commit, ele captura as mudanças que foram adicionadas no stagging, além disso eles representam os pontos na linha do tempo do seu projeto.

`$ git commit -a`  // Une o `add .` ao commit. 

`$ git commit -m "Mensagem do commit"`  // Com o -m é possível adicionar mensagens sobre o commit.

### Criando repositório remoto:

Para dar continuidade é preciso linkar nosso repositório local ao remoto, para isto, precisamos criar o repositório no github.

![image](https://github.com/Brunalu28/RepoGit/assets/44930475/8cea635c-8127-4a48-b590-f0a6f2972e84)

- Adicione um título e uma descrição ao repositório;
- Você pode deixar público ou privado;
- Adicionar o README.md, .gitgnore e a licensa se preferir.

### `git remote`

Depois do repositório local e remoto criados, é preciso estabelecer uma conexão entre eles, para isso utilizamos o seguinte comando:

`$ git remote add origin <url>`

- `origin` referencia o nosso repositório remoto.

![image](https://github.com/Brunalu28/RepoGit/assets/44930475/9e6d4929-dcce-42ca-90b1-b07c96242cad)

- A url está disponível nesse botão, vamos utilizar o ssh.

### `git branch`

Depois de fazer o link, você pode observar que a ramificação principal do seu projeto remoto é a `main`, portanto é importante sincronizar com a branch local.

`$ git branch -M "main"`  // Esse comando modifica o nome da branch atual.

Mas o que seria uma branch? Ela é basicamente um ramo independente que surge do seu projeto, em cada branch que você criar é possível desenvolver algo diferente, adicionar alguma funcionalidade que posteriormente pode ser unida ao caminho principal do seu projeto.

`$ git branch` (lista todas as ramificações existentes)

`$ git branch <nome_da_branch>` (cria uma nova branch)

`$ git branch -d <nome_da_branch>` (deleta a branch)

### `git checkout`

Esse comando é muito útil para quando se está trabalhando com muitas branchs, com ele é possível mudar de branch a qualquer momento.

`$ git checkout <nome_da_branch>`

`$ git checkout -b <nome_da_branch>`  // Esse comando cria e já entra na nova branch.

### `git pull`

Você criou o README.md ou algum arquivo logo quando estava criando o repositório no github? É importante você puxar essas alterações para o repositorio local antes de fazer o próximo comando, evitando conflitos.

`$ git pull` // Pega as alterações do remoto para o local da branch que você se encontra.

`$ git pull --rebase ou -r` // Ele aplica seus commits locais as atualizações remotas.

### `git push`

Tudo certo? vamos para a parte final, que é subir as alterações commitadas para nosso repositório remoto, para isso usamos o `push`.

`$ git push -u origin main`  //  É importante adicionar o nome da branch para o push e se for o primeiro, usar o -u.

`$ git push <nome_da_branch>`

### 2. Remotamente:

Se você quiser iniciar seu ambiente de desenvolvimento já sincronizado com o git, você precisa primeiro criar o repositório remoto e logo em seguida usar um comando para adicionar esse repositorio remoto a sua máquina.

### `git clone`

Esse comando cria uma cópia do repositório na sua máquina, com ele você não precisa realizar o `git init`, pois ele já realiza esse comando internamente.

`$ git clone <url_do_repo>`

- Depois disso você já pode começar a trabalhar no seu projeto normalmente, e commitar as atualizações, só se atente a estar com o nome das branchs sincronizados e as atualizações também, para caso esteja trabalhando em equipe.
