# Diretivas para revisão de código
Discussão entre o revisor e o codificador é sadio, favorece troca de idéias e a aquisição de novo conhecimento.

## Padronização ##
Padronização devem ser seguidos para manter organização, diminuir a curvatura de aprendizagem e legibilidade, seguem os padrões para cada tecnologia utilizada na stack.

### Padrão Angular 1.x ###
https://github.com/johnpapa/angular-styleguide/blob/master/a1/i18n/pt-BR.md
### Padrão JavaScript ###
https://github.com/airbnb/javascript/tree/es5-deprecated/es5
### Padrão Java ###
https://google.github.io/styleguide/javaguide.html

## Modularização ##
1. Regras de negócio não devem encontrar na camada de controle, e sim na camada de domínio (Considerando aqui uma arquitetura multi camadas).

## Nomeclaturas ##

### Nomes que fazem sentido ao negócio e que seja claro. ###
### Variáveis abreviadas apenas quando é amplamente conhecido o seu signficado.###
1. Exceções que podem ser utilizadas mas obrigatoriamente se enquadra no "amplamente conhecido":
 - Índices = i, j, k, ...
 - Amplamente conhecida: HTML, XML, ...
 - Siglas do domínio da aplicação: FPO, PPI, SADT, SUS, ...

## Complexidade ##
1. Principal item a ser considerado é o SRP (Single Responsability Principle), porém alguns itens secundários são recomendáveis:
2. Complexidade ciclomática <= 10.
3. Métodos menores que 30 linhas, geralmente métodos grandes violam o SRP devem ser quebrados por subtarefas, manter o mesmo nível de abstração é algo a ser considerado.
4. Estruturas de controle aninhada acima de 3.

## Desenvolvimento defensivo ##
1. Validar dados de entrada, checando se o comportamento do input é o esperado para a execução da tarefa (Mesmo as entradas do tipo "impossível de acontecer").
2. Evite retornar null, se retornar, a avaliação do null deve ser checado como retorno.
3. Caso necessário, valide a pós condição.

## Principios S.O.L.I.D. ##
1. Single responsibility principle
2. Open/closed principle
3. Liskov substitution principle
4. Interface segregation principle
5. Dependency inversion principle
