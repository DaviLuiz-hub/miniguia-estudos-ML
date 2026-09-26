# miniguia-estudos-ML-nootbookLM

# Mini Guia de Machine Learning com NotebookLM
## 1. Contexto e Objetivos
Nesse mini-gua de estudos vou criar um guia simples e facil de maneira compreesivel para qualquer pessoa conseguir entender um modelo de Machine Learning

## 2. Curadoria de Fontes
Eu ultilizei 3 fontes para o meu projeto: 
### [Fonte 1 Passo a passo de como criar o seu modelo de ML](https://www.insightlab.ufc.br/6-passos-para-criar-seu-primeiro-projeto-de-machine-learning/)
° essa fonte foi muito util para ampliar e ratificar questões importantes no ínicio de um Modelo, questões como EDA, armazenamento de dados, reutilização de dados, divisão de treinamento de modelo e entre outros. 


### [Fonte 2 Oque um Modelo de Machine Learning?](https://www.alura.com.br/formacao-machine-learning?utm_term=&utm_campaign=&utm_source=google&utm_medium=cpc&campaign_id=24055440457_201432283351_817743049139&utm_id=24055440457_201432283351_817743049139&hsa_acc=7964138385&hsa_cam=&hsa_grp=201432283351&hsa_ad=817743049139&hsa_src=g&hsa_tgt=kwl-3500001&hsa_kw=&hsa_mt=a&hsa_net=google&hsa_ver=3&gad_source=1&gad_campaignid=24055440457&gbraid=0AAAAADpqZIAktaNR8zHPmPUYZuz0EXWZ5&gclid=Cj0KCQjw2t3VBhD8ARIsAK0F6qxVAF13aMtiLkrQ_ifP5a0d8PlRP-TjCCNPUNFbb2K1kwttDOp9HqQaAgsiEALw_wcB)
° Muito útil para realmente saber o que é um modelo de Machine Learning 


### [Fonte 3 Oque é Overfitting e Underfitting?](https://www.ibm.com/br-pt/think/topics/overfitting-vs-underfitting)
°Responsável por explicar questões importantes dentro de um modelo, como a ilusão de uma alta acúracia de um modelo ou o erro de um underfitting e busca pelo o equilibrio de um modelo

## 3. Engenharia de Prompts

### Explique o que é Machine Learning para uma pessoa que está começando a estudar programação. Use exemplos simples e baseie a resposta nas fontes disponíveis neste notebook.


### Explique o que são dados de treinamento e dados de teste e por que devemos separar esses dados.


### Faça um resumo estruturado dos principais conceitos de Machine Learning presentes nas fontes deste notebook.

## 4. Cicatrizes 

### Problema encontrado: Durante os testes com o NotebookLM, algumas respostas apresentaram uma linguagem muito técnica para o nível introdutório pretendido.
### Exemplo: Explique overfitting.
ele deu uma resposta muito complexa e dificil de entender para alguém que é iniciante dentro desse aprendizado de maquina
### Como resolvi: Explique overfitting para uma pessoa que está começando a estudar Machine Learning. Utilize uma linguagem simples, um exemplo do cotidiano e explique como esse problema pode ser evitado.

### Resultado:
A resposta ficou mais clara e adequada ao objetivo do Mini Guia.

## 5. Mini Guia de Machine Learning
### 5.1 O que é Machine Learning?
O **Machine Learning** (Aprendizado de Máquina) é um ramo da inteligência artificial focado em criar sistemas capazes de aprender e evoluir automaticamente a partir da experiência com dados.

Em vez de escrever códigos com regras explícitas para cada cenário, o algoritmo analisa conjuntos de dados para reconhecer padrões por conta própria e, a partir disso, tomar decisões ou fazer previsões diante de novas situações
### 5.2 Como funciona?
* **Preparação dos Dados:** Coletamos as informações necessárias e as limpamos, corrigindo erros e transformando os dados em formato numérico para que o algoritmo consiga processá-los.
* **Divisão em Treino e Teste:** Separamos os dados em um conjunto de **treinamento** (usado para o modelo aprender) e um conjunto de **teste** (guardado para avaliar o modelo com dados inéditos).
* **Identificação de Padrões:** O algoritmo analisa as variáveis de entrada (*features*) para encontrar relações com o resultado desejado (*target*). Isso pode ser feito usando dados rotulados (aprendizado supervisionado) ou dados sem rótulos (não supervisionado).
* **Avaliação e Ajuste:** Testamos o algoritmo com os dados reservados para garantir que ele aprendeu o padrão geral do problema, evitando que ele apenas decore os exemplos do treinamento (*overfitting*).
* **Aplicação Prática:** Com o aprendizado validado, o modelo é implantado em produção para fazer previsões e tomar decisões automáticas diante de novos dados do mundo real
### 5.3 Tipos de Machine Learning
O aprendizado de máquina é dividido principalmente pelo tipo de dado e pela forma como o modelo aprende:

* **Aprendizado Supervisionado:** O modelo é treinado com **dados rotulados**, ou seja, exemplos que já possuem a resposta correta ("gabarito").
  * **Classificação:** Prevê categorias ou rótulos (por exemplo, identificar se um e-mail é spam ou classificar uma imagem médica como "saudável" ou "doente").
  * **Regressão:** Prevê valores numéricos contínuos (por exemplo, estimar o preço de venda de um imóvel).
* **Aprendizado Não Supervisionado:** O modelo analisa **dados sem rótulos** e descobre padrões ou estruturas ocultas por conta própria.
  * **Clusterização (Agrupamento):** Agrupa dados semelhantes sem orientação prévia (como o algoritmo K-means).
  * **Redução de Dimensionalidade:** Simplifica dados complexos reduzindo o número de variáveis sem perder as informações essenciais (como o PCA)
### 5.4 Overfitting e Underfitting
Representam os dois lados do grande desafio de aprendizado do modelo[10]:

* **Underfitting (Subajuste):** Acontece quando o modelo é **simples demais** para capturar as relações nos dados, apresentando um desempenho fraco tanto no treinamento quanto nos testes. *Exemplo:* Tentar prever o preço de uma casa olhando apenas para a metragem e ignorando a localização.
* **Overfitting (Sobreajuste):** Acontece quando o modelo é **complexo demais e memoriza** os detalhes e ruídos do treinamento. Ele tem excelente precisão nos dados conhecidos, mas falha ao receber dados novos. É o equivalente a memorizar o gabarito de uma lista de exercícios em vez de entender a matéria para a prova.

### 5.5 Avaliação
Indica como medir se o algoritmo realmente aprendeu e se vai funcionar bem no mundo real1516:Divisão dos Dados: Os dados são separados em três partes para garantir um teste justo: Treinamento (70-80% para o modelo aprender), Validação (10-15% para calibrar o modelo) e Teste (10-15% para avaliar o desempenho final com dados inéditos).Métricas de Desempenho:Para Classificação: Acurácia, precisão, recall, pontuação F1 e matriz de confusão.Para Regressão: Erro Quadrático Médio (MSE), Erro Absoluto Médio (MAE) 

## 6. Glossário

* **Overfitting (Sobreajuste):** Ocorre quando o modelo memoriza os detalhes e ruídos dos dados de treino em vez de aprender os padrões gerais, falhando ao lidar com novos dados.
* **Underfitting (Subajuste):** Ocorre quando o modelo é simples demais para capturar os padrões dos dados, apresentando alto erro tanto no treinamento quanto nos testes.
* **Viés (** **Bias** **):** Suposições simplificadas que o modelo faz sobre os dados; um viés muito alto ignora a complexidade do problema e leva ao *underfitting*.
* **Variância (** **Variance** **):** Sensibilidade do modelo às flutuações e ruídos do conjunto de treino; uma variância muito alta faz o modelo memorizar detalhes e causa *overfitting*.
* **Hiperparâmetros:** Configurações externas do algoritmo que são ajustadas por meio de experimentos para otimizar seu aprendizado.
* **Regularização:** Conjunto de técnicas (como L1, L2 ou *Dropout*) aplicadas para restringir a complexidade do modelo e evitar o *overfitting*.
* **Clusterização (** **Clustering** **):** Técnica de aprendizado não supervisionado usada para agrupar pontos de dados semelhantes sem o uso de rótulos prévios.
* **Engenharia de Recursos (** **Feature Engineering** ): Criação ou transformação de variáveis para representar as informações do conjunto de dados de forma mais significativa para o algoritmo.
* **Análise Exploratória de Dados (EDA):** Etapa de investigação inicial para compreender as variáveis de entrada e saída, além de identificar *outliers* e dados ausentes.
## 7. Prompts Reutilizáveis
1-Para aprender um novo conceito
Explique [CONCEITO] para alguém que está começando em Machine Learning. Utilize linguagem simples e apresente um exemplo prático.

2-Para comparar conceitos
Compare [CONCEITO A] e [CONCEITO B]. Explique as principais diferenças, semelhanças e situações em que cada um pode ser utilizado.

3-Para revisar
Faça um resumo dos principais pontos sobre [CONCEITO]. Destaque os conceitos mais importantes que devo memorizar.

4-Para praticar
Crie 5 questões sobre [CONCEITO], começando pelo nível básico e aumentando gradualmente a dificuldade. Não apresente as respostas inicialmente.

5-Para identificar dificuldades
Faça 5 perguntas sobre [CONCEITO] para avaliar se eu realmente compreendi o assunto. Após minhas respostas, identifique quais conceitos preciso revisar.

## 8. Conclusão
Com este projeto, consegui entender melhor os conceitos básicos de Machine Learning e organizar os conteúdos de uma forma mais fácil para estudar. O NotebookLM ajudou na pesquisa e na revisão dos assuntos.

Também aprendi a criar prompts mais específicos para conseguir respostas mais úteis. Pretendo continuar estudando Machine Learning e colocar o que aprendi em prática.
