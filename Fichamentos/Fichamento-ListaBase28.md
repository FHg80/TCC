# Towards Automating Code Review Activities

TUFANO, R. et al. "Towards Automating Code Review Activities," in: 2021 IEEE/ACM 43rd International Conference on Software Engineering (ICSE). [s.l.] IEEE, 2021. p. 163–174. doi: [10.1109/ICSE43902.2021.00027](https://doi.org/10.1109/ICSE43902.2021.00027).

## 1. Fichamento de Conteúdo

O artigo explora a automação parcial do processo de revisão de código (_code review_), que, apesar de reduzir bugs, aplicar refatorações, tornar a legibilidade melhor (removendo declarações de variáveis desnecessárias por exemplo) e identificar soluções alternativas para problemas no _software_, é uma atividade manual e dispendiosa em termos de tempo para os desenvolvedores. O objetivo do estudo não é propor uma substituição dos desenvolvedores, mas assisti-los, automatizando algumas tarefas repetitivas como refatorações de código e correção de _bugs_ menores. Para isso, os autores propõem duas arquiteturas de _Deep Learning_ baseadas em _Transformers_, focando em dois cenários distintos: a do contribuidor e a do revisor. No cenário do contribuidor, um modelo (com 1 codificador) foi ensinado com um _data set_ de 17.194 pares de código, em que cada par de código representa uma transformação de código diferente, para sugerir automaticamente alterações no código antes mesmo que ele seja submetido, antecipando o _feedback_ de um revisor. No cenário do revisor, um segundo modelo (com 2 codificadores) foi treinado com um _data set_ de 17.194 _triplets_ para receber como entrada o código submetido e um comentário em linguagem natural do revisor e gerar automaticamente a versão revisada do código que implementa tal comentário. A avaliação empírica mostrou que o modelo do contribuidor conseguiu replicar as transformações de código exatas em até 16% dos casos , enquanto o modelo do revisor, beneficiado pelo contexto do comentário, atingiu uma precisão de até 31%. Os autores concluem que os resultados são promissores, mas que mais pesquisa é necessária para tornar os modelos utilizáveis na prática.

## 2. Fichamento Bibliográfico

* _Contributor (contribuidor)_ o desenvolvedor que submete o código para ser revisado (página 1).

* _Reviewer (revisor)_ o desenvolvedor que comenta e avalia as mudanças de código submetidas por um contribuidor (página 1).

* _Deep Learning (DL) Models_ o estudo utiliza modelos de aprendizado profundo, especificamente a arquitetura Transformer, para aprender e automatizar tarefas de revisão de código (página 1).

* _Transformers (transformadores)_ um modelo de DL que consiste em um codificador e um decodificador para processar uma sequência de _tokens_ e gerar outra como saída (página 1).

* _Contributor Model (1-encoder)_ um modelo de DL com um codificador, que recebe como entrada o código submetido (CS) e gera uma versão revisada (CR), tentando antecipar as sugestões que um revisor faria (página 2).

* _Reviewer Model (2-encoder)_ um modelo de DL com dois codificadores, que recebe como entrada tanto o CS quanto o comentário do revisor em linguagem natural (Rnl) para gerar a CR (página 2).

* _Triplets (tripletos)_ um tripleto é uma estrutura de dados que consiste em três partes: um código original (submetido para uma revisão), um comentário em linguagem natural (feito pelo revisor) e um código revisado (implementando a sugestão feita pelo revisor) (página 2).

* _Code Abstraction (abstração de Código)_ um passo de pré-processamento para reduzir o tamanho do vocabulário do código-fonte, substituindo identificadores e literais por IDs genéricos (ex: VAR_1, TYPE_1), o que melhora o desempenho dos modelos de DL (página 2).

* _Perfect Prediction (predição Perfeita)_ uma métrica de avaliação usada no estudo que considera uma predição como correta se o código gerado pelo modelo for idêntico ao código que foi escrito manualmente pelo desenvolvedor após a rodada de revisão (página 3).

## 3. Fichamento de Citações

* _"However, since code review is a manual activity it comes at the cost of spending developers time on reviewing their teammates' code."_
* _"Our goal is to make the first step towards partially automating the code review process, thus, possibly reducing the manual costs associated with it."_
* _"The final goal is not to replace developers during code reviews but work with them in tandem by automatically solving (or suggesting) code quality issues that developers would manually catch and fix in their final checks."_
* _"The first one learns code changes performed by developers during real code review activities, thus providing the contributor with a revised version of her code implementing code transformations usually recommended during code review before the code is even submitted for review."_
* _"The second one automatically provides the reviewer commenting on a submitted code with the revised code implementing her comments expressed in natural language."_
* _"On the contributor side, the trained model succeeds in replicating the code transformations applied during code reviews in up to 16% of cases."_
* _"On the reviewer side, the model can correctly implement a comment provided in natural language in up to 31% of cases."_