<h1 align="center">Modelo de Clusterização por RFM</h1>

<p align="center">
 <a href="#entendimento-do-negócio">Entendimento do negócio</a> •
 <a href="#tecnologias-utilizadas">Tecnologias utilizadas</a> •
 <a href="#tratamento-dos-dados">Tratamento dos dados</a> • 
 <a href="#entendimento-dos-dados">Entendimento dos dados</a> • 
 <a href="#perguntas-de-negócio">Perguntas de negócios</a
</p>

## Entendimento do negócio
<p align="justify">
Esta é uma proposta de resolução para um desafio da Formação em Dados da Escola DNC. Trata-se da criação de um modelo de clusterização para criar um sistema de agrupamento de perfis de clientes para um e-commerce com base nas métricas RFM.
  
<p align="justify">
Os dados fornecidos possuem informações sobre clientes, produtos e transações da loja realizadas entre os anos de 2010 e 2011. Os dados estão disponíveis no Kaggle, em https://www.kaggle.com/datasets/carrie1/ecommerce-data.

## Tecnologias utilizadas
- Google Colab
- Python
- Pandas
- Numpy
- Matplotlib
- Seaborn
- Scikit-learn
- Yellowbrick

## Tratamento dos dados
<p align="justify">
Para utilizarmos as informações de maneira ideal, foi necessário remover linhas duplicadas, linhas com valores nulos, linhas com valores negativos em determindas variáveis, transformar os tipos de variáveis e remover outliers.

## Entendimento dos dados
<p align="justify">
Foi feita uma análise univariada para visualizar a distribuição dos dados afim de procurar por padrões ou tendências relevantes para o negócio.

<p align="justify">
Para a fazer a modelagem dos dados, foi necessário fazer uma manipulação para obter as métricas RFM (ressalta-se que foi considerado o ticket médio de cada cliente) para em seguida utilizar o PowerTransformer para normalizar os dados. O modelo escolhido foi o KMeans, que foi implementado utilizando o scikit-learn. O número de cluster escolhido através dos métodos de Elbow e Silhouette foi 4.

## Perguntas de negócio
<p align="justify">
O modelo criado gerou um gráfico 3D para melhor visualização dos clusters, assim como um gráfico e uma tabela comparando os centroides dos clusters com base no RFM. Isso permitiu identificar as características mais proeminentes de cada cluster, ou seja, de cada perfil de cliente. Dessa forma, definimos 4 perfis distintos de clientes, sendo eles: churn, clientes novos, clientes fiéis e clientes gastadores. 

<div align='center'>

| Perfil | Recência | Frequência | Valor |
| ----------- | ----------- | ----------- | ----------- |
| Churn | Alta | Baixa | Baixa-Média
| Clientes novos | Baixa | Baixa | Baixa-Média
| Clientes gastadores | Variável | Variável | Alta
| Clietes fiéis | Baixa | Alta | Baixa-Média

</div>

<p align="justify">
Essa segmentação pode ser utilizada, por exemplo, em campanhas de marketing personalizadas e em recomendação de determinados tipos de produtos.
