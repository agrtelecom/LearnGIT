# GIT E GITHUB
Baseado no vídeo (muito bom) https://www.youtube.com/watch?v=2alg7MQ6_sI

### Instalação
Visite o site oficial e instale o git na sua máquina

### Utilização
Vá para o diretório do projeto e inicie um repositório
git init

Configure seu nome e email
git config --local user.name "Seu_Nome_Aqui"
git config --local user.email "seuemail@exemplo.com"


Edite ao menos um arquivo e crie um ponto no tempo (para posterior recuperação)
git add nomedoarquivo
git commit -m "Digite uma mensagem que descreva esse ponto na história do arquivo/projeto"

Mudei o autor e verifiquei a mudança com ...
git log

Verifique que o git só faz "track" de arquivos explicitamente adicionados...

Após as mudanças realizadas, precisamos usar novamente a sequencia de comandos add + commit
git add nomedoarquivo
git commit -m "Digite uma mensagem que descreva esse ponto na história do arquivo/projeto"

Para verificar as modificações
git log
E para detalhes da última modificação 
git show

Para verificar uma modificação específica
git show IDENTIFICAÇÃO DO COMMIT

Até aqui, tudo OK.
Agora vamos começar a criar branches, por exemplo, para adicionar novas funcionalidades sem alterar a brach Master.
git branch nomeDaBranch
git checkout nomeDaBranch

Além da modificação deste arquivo readme, também criei novo arquivo NovoArquivo.txt, com uma linha de texto.

LEMBRE-SE que é necessário adicionar os dois arquivos modificados para fazer um commit!

git add README.md
git add NovoArquivo.txt
git commit -m "atualização do antigo e criação do novo"

DICA: para adicionar todos os arquivos do diretório use
git add .

Se voltarmos para a master
git checkout master
vamos notar que o novo arquivo não existe lá. Experimente o comando 'ls'! O arquivo não existe.
e quando voltamos para a primeiraBranche, verificamos que o arquivo volta a ser exibido.

Após analisar os códigos, queremos trazer as modificações da branch de edição para o master.

Voltamos para a master..
git checkout master

E fazemos o merge...
git merge  nomeDaBranch


Depois de usada, a primeiraBranch pode ser apagada
git branch (lista as branches)

git branch -D primeiraBranch

git branch (lista as branches)

### Como colocar seu projeto na nuvem?

Primeiro, abra uma conta no github.
TAmbém existem outros repositórios git na nuvem. bitbucket

Depois crie um repositório e conecte o git local ao git remoto
git remote add origin https://github.com/agrtelecom/LearnGIT.git

Verifique com 
git remote -v

Para "empurrar" seu conteúdo para o repositório na nuvem
git push

Como é a prmeira vez, é preciso criar a branch master ...
git push -u origin master


ATENÇÃO
git add e git commit irão salvar localmente.
Para as mudanças refletirem na nuvem é necessário também o 
git push


O que é isso?
  git push --set-upstream origin master

### Como trazr um projeto da nuvem para trabalhar localmente?

Você precisa clonar o repositório
git clone http://ENDEREÇO.git


Ainda tem mais instruções a partir deste ponto que eu não coloquei aqui.. 
Assista ao vídeo novamente.