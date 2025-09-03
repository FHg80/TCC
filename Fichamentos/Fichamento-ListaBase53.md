# On the efficiency of test suite based program repair: A systematic assessment of 16 automated repair systems for java programs

LIU, K. et al. "On the efficiency of test suite based program repair: A systematic
assessment of 16 automated repair systems for java programs," in: Proceedings of the
ACM/IEEE 42nd International Conference on Software Engineering. New
York, NY, USA: Association for Computing Machinery, 2020. (ICSE ’20), p. 615–627.
ISBN 9781450371216. doi: [10.1145/3377811.3380338](https://doi.org/10.1145/3377811.3380338).

## 1. Fichamento de Conteúdo

O artigo se concentra na questão dos reparos automatizados baseados em testes, que são reparos realizados automaticamente por algoritmos específicos de análise de códigos que são posteriormente validados (ou não) por uma (ou várias) suítes de testes. O estudo ressalta que além das suítes de testes não serem adequadas o suficiente para medir a aproximação ao comportamento desejado de um determinado software, os reparos realizados por estes algoritmos são quantitativos e frequentemente incorretos. O objetivo do estudo é o de medir a eficiência de algumas ferramentas de reparos automatizados de código, já que os autores identificaram uma carência sobre este tema na literatura. O artigo se concentra especificamente em 16 ferramentas para reparo de programas escritos em Java (a linguagem mais popular dentro deste tópico). São elas: jGenProg, GenProg-A, jMutRepair, kPAR, RSRepair-A, jKali, Kali-A, DynaMoth, Nopol, ACS, Cardumen, ARJA, SimFix, FixMiner, AVATAR e TBar. Todas elas são _open-source_. Além da definição das ferramentas e do contexto do estudo, o artigo faz uma importante distinção entre efetividade e eficiência, frisando que estudos prévios focaram na efetitividade destes algoritmos, enquanto a eficiência foi deixada de lado. Para medir a eficiência, o estudo utilizou como métrica principal o número de retalhos candidatos gerados (retalhos neste contexto seriam pequenas alterações no código defeitusoso). Para a realização do estudo, primeiramente a equipe mediu a efetividade das ferramentas, assim como estudos anteriores fizeram, para depois medir a eficiência das mesmas. O artigo conclui que a eficiência destas ferramentas não é ideal, e que a comunidade deveria focar em estratégias para produzir ferramentas de reparo automatizados eficientes.

## 2. Fichamento Bibliográfico 

* _State-of-the-art_ (estado da arte) é o termo utilizado para se referir às ferramentas mais avançadas e eficazes que existem atualmente para o reparo automatizado de programas (página 1).

* _Correctness_ é o termo utilizado pelo artigo para se referir ao quão correto é um reparo realizado por uma ferramenta de reparo automatizado de programas (página 1).

* _Patch_ (retalho) é uma pequena modificação de código proposta pelas ferramentas de reparo automatizado de programas para tentar corrigir defeitos em _softwares_ (página 1).

* _Efficiency_ (eficiência) conceito chave do artigo que se refere à qualidade e ao quão corretos são os retalhos propostos pelos algoritmos de reparos automatizados de programas (página 1).

* _Effectiveness_ (eficácia) é a capacidade de se atingir um objetivo, não importando como. Neste contexto se refere a quantidade de retalhos que uma ferramenta consegue produzir no menor tempo possível (página 2).

## 3. Fichamento de Citações 

* _"In the last decade, Automated Program Repair (APR) [10, 26, 41] has extensively grown as a prominent research topic in the software engineering community."_
* _"Patches are generated to be applied on a buggy program until the patched program meets the desired behaviour."_
* _"Test suite based program repair systems commonly implement a three-step pipeline as illustrated in Figure 2: fault localization, which produces a ranked list of suspicious code locations that should be modified to fix the bug; patch generation, which implements the change operators that are applied on the buggy code locations; and patch validation, which executes the test cases to check that the patched program meets the behaviour (approximatively) specified by the test suite."_
* _"If a patch candidate can pass all the given test cases (both previouslypassing and previously-failing test cases on the buggy version), it is been fixed by one tool because the time budget is sufficient while it cannot be fixed by the other due to lack of time."_
* _"Efficiency is defined based on the number of patch candidates that are generated before a repair system can hit a valid patch."_
* _"Beyond the statistical data, we call on the community to invest in strategies for making repair efficient in order to facilitate adoption in a software industry where computing resources are managed sometimes with parsimony."_
