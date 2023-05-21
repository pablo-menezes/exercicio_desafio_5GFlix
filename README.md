## Pablo Menezes

# exercicio_desafio_5GFlix
Pós Graduação Cesar School - Cadeira Computação em Nuvem 

# Projeto Final 2022.2


| **Tipo de Projeto**                                                 | **Ferramental**               | **Linguagem**        |  **Data Entrega** |
| ----------------------------                                        | ----------------------        | -------------        | -------------     |
|Responder Perguntas a partir de base de dados                       | Google Colab                  | Python With Pandas   | 21/05/2023        |



# Documentação código Colab
| **id**  | **Pergunta** |
| ------  | -----------  |
| 1.1.    | Quantos filmes estão disponíveis no dataset?  |
| 1.2.	  | Qual é o nome dos 5 filmes com melhor média de avaliação? |
| 1.3.	  | Quais os 9 anos com menos lançamentos de filmes?  |
| 1.4.	  | Quantos filmes que possuem avaliação maior ou igual a 4.7, considerando apenas os filmes avaliados na última data de avaliação do dataset?  |
| 1.5.	  | Dos filmes encontrados na questão anterior, quais são os 10 filmes com as piores notas ?  |
| 1.6.	  | Quais os id's dos 5 customers que mais avaliaram filmes e quantas avaliações cada um fez?   |


# 1.1.	Quantos filmes estão disponíveis no dataset?
| **Função Utilizda** | **Link Documentação** | **Explicação de uso na atividade**|
| -----               | -----                 | ------ |
| value_counts()      | [pandas.Series.value_counts](https://pandas.pydata.org/docs/reference/api/pandas.Series.value_counts.html). | O objetivo de utilizar o value_counts() é realizar a contagem dos valores contidos em uma Data Series ou seja uma coluna especifica, a artir de uma primary_key, como é o caso da coluna Movie_Id, foi possivél contar a quantidade de valores nessa coluna e retornar |
| sum()               | [pandas.DataFrame.sum](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.sum.html)  | A sum() soma todos os valores, com isso, primeira função é verificada a quantidade de primary_key, e a função sum() soma elas para retornar um valor total.|


# 1.2.	Qual é o nome dos 5 filmes com melhor média de avaliação?
| **Função Utilizda** | **Link Documentação** | **Explicação de uso na atividade**|
| -----               | -----                 | ------ |
| Groupby()           | [pandas.DataFrame.groupby](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.groupby.html)  | A função group By do pandas vai ajudar agrupando os valores por grupo ou categoria de valores, retornando o count, uma média, uma agregação. No caso da atividade foi utilizada para realizar a média de Rantings|


# 1.3.	Quais os 9 anos com menos lançamentos de filmes?
| **Função Utilizda** | **Link Documentação** | **Explicação de uso na atividade**|
| -----               | -----                 | ------ |
| Value_counts()      | [pandas.Series.value_counts](https://pandas.pydata.org/docs/reference/api/pandas.Series.value_counts.html). | Foi contada a quantidade de filmes com a coluna ano e retornada as ultimas linhas do DataFrame  |
| tail()              | [pandas.DataFrame.tail](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.tail.html)  | Retorna as ultimas linhas do dataFrame, utilizamos para retornar as ultimas 9 linhas do dataframe  |

# 1.4.	Quantos filmes que possuem avaliação maior ou igual a 4.7, considerando apenas os filmes avaliados na última data de avaliação do dataset?
| **Função Utilizda** | **Link Documentação** | **Explicação de uso na atividade**|
| -----               | -----                 | ------ |
| max()               | [pandas.Series.max](https://pandas.pydata.org/docs/reference/api/pandas.Series.max.html#pandas.Series.max)  | Retornando o valor maximo de um DataFrame ou Data Series, no caso das notas da última data de avaliação do dataset, a função max() foi usada para retornar a última data de avaliação do dataset.  |
| loc()               | [pandas.DataFrame.loc](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.loc.html)  | A função loc do DataFrame realiza um filtro nas condições colocada dentro da função, como a condição para a nossa resposta é que a avaliação seja na última data do dataframe usamos esses valor com a max(), e em seguida definimos a segunda condição como os ratings => (Igual ou Maior) que 4,7. |
| unique()            | [pandas.unique](https://pandas.pydata.org/docs/reference/api/pandas.unique.html)  | A função unique(), nos trás os valores que são únicos de cada coluna, então utilizamos para no final das contas ter a quantidade de filmes que passaram na nossa condição do loc().  |

# 1.5.	Dos filmes encontrados na questão anterior, quais são os 10 filmes com as piores notas ?
| **Função Utilizda** | **Link Documentação** | **Explicação de uso na atividade**|
| -----               | -----                 | ------ |
| min()               | [pandas.DataFrame.min](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.min.html)  | A função min retorna os menores valores de um DataFrame ou DataSeries, utilizamos ele para retornar os filmes com os melhores valores de avaliação. |
| merge()             | [pandas.DataFrame.merge](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.merge.html)  | O merge de Dataframes, realiza uma junção deles, utilizando uma tabela em comum entre os dois, e definimos o tipo da junção que é LEFT ou seja pega os valores do primeiro dataframe  e depois o do Segundo, Right Pegar os dados em comum do Segundo com o Primeiro, ou Inner que junta os dois dataframes, para o nosso problema precisamos dos 10 filmes que consta no dataframe 1, junto com as menores notas contidas no dataframe 2.

# 1.6.	Quais os id's dos 5 customers que mais avaliaram filmes e quantas avaliações cada um fez?
| **Função Utilizda** | **Link Documentação** | **Explicação de uso na atividade**|
| -----               | -----                 | ------ |
| value_counts()      | [pandas.Series.value_counts](https://pandas.pydata.org/docs/reference/api/pandas.Series.value_counts.html)  | Foi usado o Value_counts para contar a quantidade que cada Customers ID votou na tabela de Rating. |
| head()              | [pandas.DataFrame.head](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.head.html)  | Foi usado para retorna os valores do topo de um data frame, com o head(5), para retornar as 5 linhas do topo do dataframe.
