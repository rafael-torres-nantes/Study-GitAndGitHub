# Comandos Básicos do Git
O Git oferece uma ampla gama de comandos para gerenciar o controle de versão de seus projetos. Aqui estão alguns dos comandos básicos mais comumente usados:

## 1. Configuração do usuário

Define o nome de usuário e o email global para ser usado em todos os seus commits.

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seu_email@example.com"
```

Mostra o o nome de usuário e email global, além de todas as configurações Git globais e locais:
```bash
git config --global user.name
git config --global user.email
git config --list
```

### Editor de texto

Define o [editor de texto](https://docs.github.com/en/get-started/getting-started-with-git/associating-text-editors-with-git) padrão para ser usado ao escrever mensagens de commit:
```bash
git config --global core.editor "code --wait"
```

## 2. Criando repositório local

Para começar a rastrear as alterações em um projeto existente ou iniciar um novo projeto com o Git, você precisa inicializar um repositório local. Você pode fazer isso executando:
```bash
git init
```

Cria um novo repositório Git no diretório atual e configura a branch principal como __main__ em vez de __master__:
```bash
git config --global init.defaultBranch main
```

Mostra todos os arquivos e pastas no diretório atual, incluindo arquivos ocultos:
```bash
ls -a
```

## 3. Adicionando mudanças

Mostra o status do repositório Git atual, incluindo arquivos modificados, não rastreados e staged:
```bash
git status
```

Após fazer alterações nos arquivos do seu projeto, você precisa adicioná-las ao índice do Git antes de confirmá-las em um commit. Isso é feito com o comando:
```bash
git add .
```

Adiciona um arquivo específico à área de preparação para o próximo commit:
```bash
git add nome_do_arquivo
```

## 4. Removendo arquivos adicionados

Remove todos os arquivos da área de preparação:
```bash
git rm --cached -r .
```

Remove um arquivo específico da área de preparação:
```bash
git rm --cached nome_do_arquivo
```

## 5. Salvando mudanças

Salva as alterações na área de preparação como um novo commit com a mensagem especificada:
```bash
git commit -m "Mensagem do commit"
```
É recomendável usar uma mensagem clara e concisa que descreva o propósito das alterações.

### Gits Semânticos

Os commits podem seguir uma abordagem semântica, comunicando a intenção da alteração:

- __build:__ Mudanças relacionadas ao sistema de construção ou dependências externas (exemplos: gulp, npm).

- __ci:__ Alterações nos arquivos e scripts de configuração de integração contínua (exemplos: Travis, CircleCI).

- __docs:__ Inclusões ou modificações apenas em arquivos de documentação.

- __feat:__ Adições de novas funcionalidades ou implementações ao código.

- __fix:__ Correções de bugs.

- __perf:__ Alterações de código que melhoram o desempenho.

- __refactor:__ Refatorações de código que não alteram a funcionalidade final.

- __style:__ Alterações na formatação do código que não afetam seu significado (exemplos: espaços em branco, formatação).

- __test:__ Adições ou correções de testes automatizados (TDD).

- __chore:__ Atualizações de tarefas que não afetam o código de produção, como mudanças de ferramentas ou configurações.

- __env:__ Modificações ou adições em arquivos de configuração para integração contínua (CI), como parâmetros de configuração de containers.

## 6. Quatro estados

No Git, existem quatro estados principais de um arquivo: untracked, unmodified, modified e staged.

- __Untracked (Não rastreado)__: Arquivos não monitorados pelo Git, geralmente novos arquivos no diretório de trabalho.

- __Staged (Preparado)__: Alterações marcadas para o próximo commit usando `git add`.

- __Unmodified (Não modificado)__: Arquivos monitorados sem alterações desde o último commit.

- __Modified (Modificado)__: Arquivos alterados no diretório de trabalho após serem adicionados ao Git, mas não preparados para commit.

## 7. Visualizando alterações

Mostra as diferenças entre o diretório de trabalho e a área de preparação:
```bash
git diff
```

Mostra as diferenças entre a área de preparação e o último commit:
```bash
git diff --cached
```

Mostra as diferenças entre o diretório de trabalho e o último commit:
```bash
git diff --staged
```

## 8. Histórico de commits

Visualizar o histórico de commits do repositório Git:
```bash
git log
```
> Este comando mostrará informações sobre cada commit, incluindo o hash, autor, data e mensagem de commit.


Visualiza apenas as mensagens de commit:
```bash
git log --oneline
```

Visualiza _n números_ de commits:
```bash
git log -1
```

Visualiza as diferenças entre os commits de forma ampla:
```bash
git log --p
```

Visualiza as diferenças entre os commits de forma resumida:
```bash
git log --stat
```

## 9. Alterando um commit

Se você precisar modificar a mensagem do commit mais recente ou adicionar alterações esquecidas, pode fazer isso com o comando:
```bash
git commit --amend -m "Nova mensagem de commit"
```
> Se não utilizar o -m, acessará o VIM como editor de texto e deverá clickar "ESC > Digite: "WQ" > "ENTER"

Altera o conteúdo do commit mais recente sem modificar a mensagem:
```bash
git commit --amend --no-edit
```

## 10. Acessar versões anteriores

Altera o diretório de trabalho para a versão específica do projeto:
```bash
git checkout numero_versao
```
>Isso alterará seu diretório de trabalho para a versão específica do projeto.

Limpa arquivos não rastreados do diretório de trabalho:
```bash
git clean -f
```

## 11. Ignorando arquivos

Cria um arquivo `.gitignore` para listar os arquivos que o Git deve ignorar:
```bash
touch .gitignore
```

Em seguida, edite o `.gitignore` e adicione os padrões de arquivos que deseja ignorar.

## 12. Parar de rastrear um arquivo

Marca um arquivo como "pular a árvore de trabalho". Isso significa que o Git irá ignorar as alterações nesse arquivo, mesmo que ele tenha sido modificado:
```bash
git updata--index --skip-worktree nome_do_arquivo
```

Caso deseje reverter essa configuração:
```bash
git updata--index --no-skip-worktree nome_do_arquivo
```

## 13. Clonando repositório

Clonar um repositório Git existente para um novo diretório local:
```bash
git clone URL_do_repositório
```