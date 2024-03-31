# Guias Extras

## Estrutura de pastas do projeto

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

- __build:__ Alterações que afetam o sistema de construção ou dependências externas (escopos de exemplo: gulp, broccoli, npm),
- __ci:__ Changes to our CI configuration files and scripts (example scopes: Travis, Circle, BrowserStack, SauceLabs);
- __docs:__ referem-se a inclusão ou alteração somente de arquivos de documentação;
- __feat:__ Tratam adições de novas funcionalidades ou de quaisquer outras novas implantações ao código;
- __fix:__ Essencialmente definem o tratamento de correções de bugs;
- __perf:__ Uma alteração de código que melhora o desempenho;
- __refactor:__ Tipo utilizado em quaisquer mudanças que sejam executados no código, porém não alterem a funcionalidade final da tarefa impactada;
style: Alterações referentes a formatações na apresentação do código que não afetam o significado do código, como por exemplo: espaço em branco, formatação, ponto e vírgula ausente etc.;
- __test:__ Adicionando testes ausentes ou corrigindo testes existentes nos processos de testes automatizados (TDD);
- __chore:__ Atualização de tarefas que não ocasionam alteração no código de produção, mas mudanças de ferramentas, mudanças de configuração e bibliotecas que realmente não entram em produção;
- __env:__ basicamente utilizado na descrição de modificações ou adições em arquivos de configuração em processos e métodos de integração contínua (CI), como parâmetros em arquivos de configuração de containers.