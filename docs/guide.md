# Guias Extras

## Estrutura de pastas do projeto

A estrutura de pastas do projeto é uma organização hierárquica das diferentes partes e recursos do projeto. Cada pasta tem uma função específica e contém tipos específicos de arquivos relacionados ao desenvolvimento, configuração, dados e documentação do projeto. Aqui está uma explicação detalhada de cada pasta:


[Guia de Markdown](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)

<div style="text-align: center;">

  | Nome da pasta | Descrição |
  |---|---|
  | assets | Armazena recursos estáticos como imagens, CSS e JavaScript. |
  | bin | Armazena os arquivos executáveis do projeto. |
  | build | Armazena os arquivos compilados do projeto. |
  | config | Armazena arquivos de configuração do projeto. |
  | data | Armazena dados usados pelo projeto. |
  | docs | Armazena a documentação do projeto. |
  | lib | Armazena bibliotecas de terceiros usadas pelo projeto. |
  | logs | Armazena os logs do projeto. |
  | src | Armazena o código-fonte do projeto. |
  | temp | Armazena arquivos temporários do projeto. |
</div>

## Commits Semânticos

O Git Semântico é uma abordagem para nomear e versionar commits de uma forma padronizada e significativa. Ele segue uma convenção de nomenclatura que atribui significado semântico aos commits, permitindo aos desenvolvedores entender facilmente o propósito e o impacto de uma alteração.

- __build:__ Alterações que afetam o sistema de construção ou dependências externas (escopos de exemplo: gulp, broccoli, npm),
- __ci:__ Changes to our CI configuration files and scripts (example scopes: Travis, Circle, BrowserStack, SauceLabs);
- __docs:__ referem-se a inclusão ou alteração somente de arquivos de documentação;
- __feat:__ Tratam adições de novas funcionalidades ou de quaisquer outras novas implantações ao código;
- __fix:__ Essencialmente definem o tratamento de correções de bugs;
- __perf:__ Uma alteração de código que melhora o desempenho;
- __refactor:__ Tipo utilizado em quaisquer mudanças que sejam executados no código, porém não alterem a funcionalidade final da tarefa impactada;
- __style:__ Alterações referentes a formatações na apresentação do código que não afetam o significado do código, como por exemplo: espaço em branco, formatação, ponto e vírgula ausente etc.;
- __test:__ Adicionando testes ausentes ou corrigindo testes existentes nos processos de testes automatizados (TDD);
- __chore:__ Atualização de tarefas que não ocasionam alteração no código de produção, mas mudanças de ferramentas, mudanças de configuração e bibliotecas que realmente não entram em produção;
- __env:__ basicamente utilizado na descrição de modificações ou adições em arquivos de configuração em processos e métodos de integração contínua (CI), como parâmetros em arquivos de configuração de containers.

## Projeto com Estrutura MVC em Node.js

Este projeto segue a arquitetura MVC (Model, View, Controller) para organizar e modularizar o código, tornando-o mais fácil de entender, manter e escalar. A estrutura de diretórios é projetada de acordo com as melhores práticas de desenvolvimento.

| Diretório   | Descrição  | 
|-------------- | ----------------------------------------------------------------------------------------------------------- |
| controllers | Gerenciam o fluxo de informações entre o frontend e o backend, realizando chamadas aos serviços.           |
| models      | Responsáveis pela construção dos objetos que representam os dados manipulados pela aplicação.             |
| routes      | Definem as rotas da aplicação, especificando como as requisições HTTP são tratadas e direcionadas.       |
| services    | Encapsulam a lógica de negócios da aplicação, realizando operações específicas nos dados.                |
| views       | Contêm as páginas do frontend que consomem os dados fornecidos pelo backend, apresentando-os ao usuário. |

