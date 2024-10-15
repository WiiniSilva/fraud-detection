# Case Fraude

Este projeto tem como objetivo detectar fraudes em transações financeiras utilizando técnicas de aprendizado de máquina. O notebook `Case Fraude.ipynb` contém todo o fluxo de trabalho do projeto, incluindo a preparação dos dados, modelagem e avaliação dos modelos.

## Conteúdo

1. [Introdução](#introdução)
2. [Carregamento e Pré-processamento dos Dados](#carregamento-e-pré-processamento-dos-dados)
3. [Análise Exploratória dos Dados](#análise-exploratória-dos-dados)
4. [Engenharia de Features](#engenharia-de-features)
5. [Modelagem](#modelagem)
6. [Avaliação dos Modelos](#avaliação-dos-modelos)
7. [Conclusão](#conclusão)
8. [Referências](#referências)

## Introdução

As fraudes financeiras representam um desafio significativo para instituições financeiras e empresas em todo o mundo. Elas podem resultar em enormes perdas financeiras, danos à reputação e desconfiança dos clientes. Com o aumento das transações digitais, detectar e prevenir fraudes tornou-se ainda mais crucial. Utilizar técnicas de aprendizado de máquina para identificar padrões anômalos em transações pode fornecer uma defesa eficaz contra fraudes. Este projeto visa explorar e aplicar essas técnicas para melhorar a detecção de atividades fraudulentas, protegendo tanto as organizações quanto seus clientes. 

## Pré-processamento dos Dados

* Filtragem Geográfica: Foram selecionadas apenas transações realizadas no Brasil.

* Entrega de Documentos: Foram considerados como fraudes os casos em que os valores estavam ausentes na entrega dos documentos de 1 a 3.

* Transformação da Data da Transação: A data da transação foi desmembrada em três variáveis distintas: Hora da Compra, Dia do Mês e Dia da Semana. Essa separação foi feita para melhor compreender o comportamento dos fraudadores.

* Redução de Dimensionalidade: As variáveis Produto e Categoria Produto continham uma grande variedade de informações. Para reduzir a dimensionalidade e melhorar a análise, foi utilizado o método Target Encoder.

* Substituição de Valores Ausentes: Para as variáveis de score de 2 a 10, os valores ausentes foram substituídos pela mediana. Essa abordagem foi adotada devido à grande quantidade de outliers presentes nessas variáveis.

## Análise Exploratória dos Dados

* Distribuição de Fraudes: Apenas 5% dos dados representam transações fraudulentas.

* Score 1: Transações fraudulentas tendem a apresentar valores mais baixos para o score_1, indicando que um score_1 baixo pode ser um bom indicador de maior probabilidade de fraude.

* Score 2: Apesar de apresentar valores altos, o score_2 sozinho não é capaz de prever fraudes com precisão. Portanto, será necessário utilizar múltiplos scores e outros fatores no modelo de detecção de fraudes.

* Score 3: A média do score_3 é praticamente a mesma para fraudes e não fraudes, sugerindo que esta variável, isoladamente, pode não ser um forte discriminador entre as duas classes.

* Score 4: Quanto menor o score_4, maior a probabilidade de fraude, tornando-se um bom discriminador entre transações fraudulentas e não fraudulentas.

* Score 5: As diferenças nas distribuições (fraudulentas e não fraudulentas) sugerem que o score_5 tem um comportamento distinto nas fraudes, tornando-se uma variável importante para o modelo de detecção de fraudes.

* Score 6: A diferença nas distribuições sugere que o score_6 pode ser um bom discriminador entre transações fraudulentas e não fraudulentas, com pontuações mais baixas associadas a um risco maior de fraude.

* Score 7: A maioria dos valores de score_7 está concentrada nos intervalos mais baixos, com a cauda se estendendo para valores mais altos.

* Score 8: O score_8 apresenta uma distribuição aproximadamente uniforme, com frequências relativamente constantes ao longo da faixa de valores.

* Score 9: A tendência de fraudes apresentarem scores_9 mais baixos pode ser explorada no modelo de detecção, ajudando a identificar transações suspeitas.

* Score 10: A presença de picos em 0 e a ligeira diferença na média entre fraudes e não fraudes indicam que quanto menor o score_10, maior a probabilidade de fraude.

D* ocumentos Não Entregues: Transações onde o documento 1 não foi entregue (0) apresentam uma taxa de fraude significativamente maior (16.16%) em comparação às transações onde o documento foi entregue (1), com uma taxa de fraude de apenas 4.30%. Quando o documento 3 não é entregue (0), a taxa de fraude é de 8.18%, enquanto a entrega do documento 3 (1) reduz a taxa de fraude para 3.28%.

* Horário da Transação: Entre 0h e 4h, as fraudes são significativamente mais altas, com picos às 2h (19.65%) e 3h (15.68%), sugerindo que a madrugada é um horário de maior risco para fraudes.

## Engenharia de Features

Explique as técnicas de engenharia de features utilizadas, como a criação de variáveis lag, transformação de variáveis e uso de técnicas de oversampling como SMOTE.

## Modelagem

Detalhe os modelos de aprendizado de máquina utilizados, como `XGBClassifier`, `RandomForestClassifier` e `SARIMA`. Inclua a definição dos hiperparâmetros e a otimização utilizando técnicas como `RandomizedSearchCV` e `GridSearchCV`.

## Avaliação dos Modelos

Descreva as métricas de avaliação utilizadas para comparar os modelos, como AUC-ROC, accuracy, precision, recall e f1-score. Inclua uma comparação dos resultados dos modelos e gráficos como curvas ROC e matrizes de confusão.

## Conclusão

Resuma as principais conclusões do projeto, destacando o melhor modelo e as métricas de desempenho. Discuta possíveis melhorias futuras e próximos passos.

## Referências

Liste as principais referências utilizadas no projeto, incluindo artigos, documentação de bibliotecas e outros recursos relevantes.


