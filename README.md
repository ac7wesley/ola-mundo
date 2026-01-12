# Como trabalhar com Git.
```bash
Versão Simplificada,S2, para mais informações consulte git-scm.com
```
[**Link diretor para o site do Git** ](https://git-scm.com/docs)

## Git e GitHub

Ferramentas indispensáveis para trabalhar com programação.

#### Clona um repositório.

```bash
git clone <url_do_projeto>

# Exemplo
git clone https://github.com/ac7wesley/ola-mundo.git

```
#### Inicia um arquivo git/repositórios.

```bash
git init
```

#### Adiciona arquivos na stage para serem enviados ao Github

```bash
# Adiciona todos os arquivo de uma só vez.
git add .

# Adicionando um arquivo
git add index.html

# Adicionando uma pasta
git add assets

```
## Status

Para ver o Status "stage” de um arquivo e se ele arquivo será adicionado ou deletado. Assim fica mais claro entender o que vai para o commit e o que não vai para o seu commit.

### Como utilizar

```bash
git status
```
## Push

Esse comando faz com que todos os nossos commits sejam empurrados (tipo um upload) na origem do repositório, poe exemplo, dentro do GitHub. Ao executar com o `-u` você está dizendo que essa branch faz parte de um repositório remoto, o `-u` é uma abreviação para o `--set-upstream`.

Não será necessário utilizar o `-u` o tempo todo, apenas quando novas branches forem criadas para joga-las no provedor Git.

Caso o `git push` seja executado sem o `-u` será necessário sempre informar a origem e o nome da branch para que as alterações sejam levadas ao provedor Git.

### Como utilizar

```bash
# Na primeira vez
git push -u origin <nome_da_branch>

# Nas outras vezes
git push

# Quando executado sem -u
git push origin <nome_da_branch>
```
Obs.: [branch] **É a branch que você esta trabalhando**, evitar trabalhar na branch main, sempre criar as branch para cada alteração no seu projeto.

```bash
# Commit simplificado.
git commit -m "mensagem do commit" 

atributo: -a = pula stage do git add.
atributo: -m = adiciona uma mensagem no commit tem que usar "".
        
```
Obs.: Sempre que possível usar a [*Conventional Commits Pattern* aqui neste link](https://www.conventionalcommits.org/en/v1.0.0/), ou pesquise o google.

 ## Pull

Com este comando você consegue pegar a última versão atualizada que está na origem remota, ou seja, todos os novos commits das pessoas que trabalharam no projeto vai diretamente para a branch que você pretende trabalhar. 

IMPORTANTE: se você fez um push com `-u` em algum momento, apenas um `git pull` dentro da branch será necessário, mas caso você não tenha feito isso, para baixar as atualizações será necessário rodar um git pull com `origin <nome_da_branch>`.

### Como utilizar

```bash
git pull

# Se precisar buscar na origin, quando não foi feito `git push -u`
git pull origin <nome_da_branch>
```

## Checkout

O git checkout acessa branches, ou seja, ramificações existentes (locais ou remotas) e também cria uma nova branch a partir de outra que você já esteja, quando acompanhado do `-b` em sua execução.

As branches normalmente são utilizadas para criar novas features sem precisar afetar a principal, ou seja, a branch `main` (na maior parte dos casos).

### Como utilizar

```bash
git checkout <nome_da_branch>

# Para criar uma nova branch
git checkout -b <nome_da_branch>
```

## Branch

Lista todas as branches locais ou remotas, também delete branches locais, importante para saber em qual branch você esta trabalhando.

### Como utilizar

```bash
git branch

# Para deletar uma branch local
git branch -D <nome_da_branch>

# Para deletar uma branch remota
git push --delete origin <nome_da_branch>
```



Obrigado por **você** esta aqui, Acesse meu [GitHub Click Aqui](https://github.com/ac7wesley), _ac7wesley_.
