# <div align="start"><img src="https://img.icons8.com/?size=512&id=20906&format=png" width=30 align="center" /> git </div>


<div align="center"> <img src=https://geps.dev/progress/80 align="center"> Completed! </div>

## Principais comandos

# BRANCHES:

```bash
$ git checkout [-b | -a | -c] <arguments>
```
→ `-b` cria uma nova branch e alterna para a mesma.

→ `-a` lista as branchs locais e a de rastreamento.

→ `-c` cria uma branch a partir de outra
</br>
- Para alterar o nome da branch criada:
```bash
$ git branch -m "<antigo>" "<novo>"
```

- Para deletar a branch:
```bash
$ git push <remote> :"<branch>"
```
</br>
→ Utilizado para alternar entre versões. 

→ É possível utilizar referências com a opção ~n, sendo n um inteiro qualquer. Retrocedendo n commits da branch atual.

# TAGS:

- Tags anotadas:

```bash
$ git tag -a "<tag>" -m "<commit>"
```

- Tags leves:

```bash
$ git tag [-d] <tag>
```

- Para empurrar as tags:

```bash
$ git push --tags
```

→ `-a` adiciona uma tag anotada.

→ `-m` adiciona uma mensagem como o commit.

→ `-d` para deletar uma tag.

# STATUS:

```bash
$ git status
```

→ Para visualizar as alterações feitas no diretório de trabalho.

```bash
$ git restore <file>
```

→ Para descartar mudanças locais.

```bash
$ git add <file>
```

→ Para adicionar e atualizar o que será commitado.

```bash
$ git clean <file> [-f | -n]
```

→ Para descartar mudanças no estado untracked.

→ `-f` força a remoção dos arquivos.

→ `-n` mostra todos os arquivos que serão apagados e pedirá confirmação.

# REVERT | RESET:

```bash
$ git revert <commit> [--no-edit]
```

→ `—no-edit` mantém a mensagem padrão ao reverter um commit.

```bash
$ git reset [--soft | --mixed<default> | --hard]
```

→ `—soft` preserva a área de staging.

→ `—mixed` não preserva a área de staging, mas mantém o arquivo na área de trabalho.

→ `—hard` não preserva a área do staging e não mantém o arquivo.

```bash
$ git reflog
```

→ Pegamos a referência do commit.

```bash
$ git checkout <hash>
```

→ Trazemos a branch do commit de volta

# MERGE:

```bash
git merge [--no-ff]
```

→ `—no-ff` indica para o git a não utilizar o fast forward.

\# FETCH:

```bash
$ git fetch
```

→ O fetch fará download do conteúdo remoto, ma não atualizará o estado de funcionamento do repositório local.

# PULL:

```bash
$ git pull
```

→ Baixa alterações do repositório remoto e mescla com sua área de trabalho

# FETCH x PULL:

→ O fetch irá baixar os git objects sem afetar o código local

→ O pull executa um git fetch seguido de um git merge origin/<current_branch>
