# GIT E GITHUB

Aprendendo ...

### Instalação
Visite o site oficial e instale o git na sua máquina

### Utilização

- Vá para o diretório do projeto e inicie um repositório
> git init

- Edite ao menos um arquivo e crie um ponto no tempo (para posterior recuperação)
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