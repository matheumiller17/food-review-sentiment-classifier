# Análise de Sentimentos em Avaliações de Clientes Brasileiros Utilizando Machine Learning

**Autor:** Matheus Miller  
**Área:** Inteligência Artificial, Machine Learning e Processamento de Linguagem Natural (NLP)  
**Tecnologias:** Python, Scikit-learn, Pandas, TF-IDF e Logistic Regression

## 1. Introdução

A análise de sentimentos é uma aplicação de Processamento de Linguagem Natural (NLP) que permite identificar opiniões positivas e negativas em textos.

Em plataformas de comércio eletrônico, milhares de clientes compartilham experiências sobre produtos, entregas e atendimento. A análise automatizada desses comentários pode auxiliar empresas a identificar problemas e compreender a satisfação dos consumidores.

Este projeto investiga a aplicação de algoritmos de Machine Learning na classificação automática de avaliações de clientes brasileiros.

## 2. Objetivo

Desenvolver e avaliar um modelo de classificação binária capaz de identificar sentimentos positivos e negativos em avaliações textuais de consumidores.

O projeto busca demonstrar a aplicação de técnicas tradicionais de NLP em um problema relacionado à experiência do cliente.

## 3. Dataset e preparação dos dados

Foi utilizado o conjunto de dados público **Brazilian E-Commerce Public Dataset by Olist**, que contém informações de pedidos e avaliações de consumidores brasileiros.

Foram selecionadas duas variáveis principais:

- `review_comment_message`: comentário escrito pelo consumidor.
- `review_score`: nota atribuída pelo consumidor, de 1 a 5 estrelas.

As avaliações foram classificadas da seguinte maneira:

| Nota | Classificação |
|---|---|
| 1 e 2 estrelas | Negativa |
| 3 estrelas | Excluída |
| 4 e 5 estrelas | Positiva |

Registros sem comentários foram removidos.

As notas foram utilizadas como indicadores aproximados de sentimento, uma vez que não representam necessariamente uma interpretação linguística precisa de cada comentário.

## 4. Metodologia

O desenvolvimento foi realizado em Python, utilizando bibliotecas de Machine Learning.

Primeiramente, os dados foram divididos em dois conjuntos:

- 80% para treinamento.
- 20% para teste.

A divisão foi estratificada para preservar aproximadamente a proporção entre avaliações positivas e negativas.

Em seguida, foi aplicado o algoritmo **TF-IDF (Term Frequency–Inverse Document Frequency)**, responsável por transformar os comentários em representações numéricas.

Para a classificação, foi utilizado o algoritmo **Logistic Regression**, treinado para identificar padrões associados às duas classes.

O modelo foi avaliado utilizando acurácia, precisão, recall e F1-score.

## 5. Resultados

Os resultados informados após a execução do notebook no Kaggle foram:

| Métrica | Resultado |
|---|---|
| Acurácia | 92,9% |
| F1-score macro | 0,91 |
| F1-score ponderado | 0,93 |

A acurácia de aproximadamente 92,9% indica que o modelo classificou corretamente essa proporção das avaliações presentes no conjunto de teste.

O F1-score macro de 0,91 representa a média não ponderada dos F1-scores das duas classes, enquanto o F1-score ponderado de 0,93 considera a quantidade de exemplos de cada classe.

Os resultados sugerem que o modelo conseguiu identificar padrões relevantes nas avaliações utilizadas.

Entretanto, uma avaliação mais completa exigiria analisar também a matriz de confusão, os resultados individuais por classe e o desempenho em dados externos.

## 6. Limitações

Apesar dos resultados obtidos, existem limitações importantes:

- As notas dos consumidores foram utilizadas como aproximação dos sentimentos.
- Avaliações irônicas, ambíguas ou contraditórias podem gerar classificações incorretas.
- O desempenho pode diminuir em comentários provenientes de outras plataformas.
- Não foi realizada uma validação externa independente.
- O modelo não utiliza arquiteturas modernas de linguagem, como Transformers ou LLMs.

Portanto, os resultados devem ser interpretados como desempenho experimental no conjunto de teste utilizado, e não como garantia de precisão em produção.

## 7. Aplicações práticas

Soluções semelhantes podem ser utilizadas em plataformas digitais para identificar reclamações, analisar feedback de consumidores, acompanhar tendências de satisfação e auxiliar equipes de experiência do cliente.

O projeto demonstra como técnicas de Machine Learning podem apoiar a análise de grandes volumes de avaliações textuais.

## 8. Conclusão

O experimento demonstrou a viabilidade de utilizar TF-IDF e regressão logística para classificar sentimentos em avaliações de consumidores brasileiros.

O modelo alcançou aproximadamente 92,9% de acurácia no conjunto de teste, apresentando resultados promissores para um protótipo de classificação binária.

Como trabalhos futuros, recomenda-se ampliar a avaliação experimental, comparar diferentes algoritmos e investigar modelos baseados em Transformers.

Este projeto integra um portfólio de estudos em Inteligência Artificial e Machine Learning, com foco em aplicações práticas de NLP.

## 9. Referências

- Olist. *Brazilian E-Commerce Public Dataset by Olist*. Kaggle.
- Scikit-learn. *Machine Learning in Python*. https://scikit-learn.org/
- Hugging Face. *Model Hub*. https://huggingface.co/
