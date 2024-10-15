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

## Análise Exploratória dos Dados

Descreva as principais análises exploratórias realizadas, como a distribuição das variáveis, análise de correlação e identificação de outliers.

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


