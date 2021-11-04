# MD-ATS
Código-fonte e outros arquivos utilizado no desenvolvimento do artigo "A Comparative Study of Automatic Text Summarization Algorithms"

## Autores
- Alysson Cristiano Estevam de Moura 
- Luciana Santos de Assis
- Olival Gomes Barboza Júnior

## Professor
- Dr. Marcelo Ladeira

## Contexto
Este trabalho referencia o artigo "A Comparative Study of Automatic Text Summarization Algorithms" desenvolvido na disciplina de Mineração de Dados do curso de Pós-Graduação em Computação Aplicada da Universidade de Brasília. Trata-se de um estudo comparativo de três algoritmos extrativos de sumarização de textos, utilizando métricas ROUGE:
- Algoritmo baseado em frequência de palavras
- Algoritmo clássico de Luhn
- Algoritmo TextRank baseada na similaridade do cosseno

## Base de dados

A base de dados utilizada para o desenvolvimento deste trabalho foi recuperada do repositório: https://github.com/sunnysai12345/News_Summary Trata-se de um conjunto de 4.515 textos de notícias e os respectivos sumários de referência. No desenvolvimento deste trabalho foi realizado um estudo comparativo dos sumários gerados automaticamente pelos três algoritmos e os sumários gerados manualmente e disponibilizados da base de dados.

Inicialmente, decidimos pela exclusão de alguns registros da base pelo fato de possírem um número de caracteres baixo e consequentemente, não terem condições de gerar resultados interessantes para este trabalho. Após a limpeza desses registros, a base de dados ficou com 3965 registros.

## Arquivos de dados
- news_summary_original.xlsx (Base de dados original com 4515 registros)
- news_summary.xlsx (Base de dados utilizada para o desenvolvimento do trabalho com 3965 registros)

## Arquivos - Código-Fonte
A implementação dos algoritmos foi realizada na linguagem de programação Python e o ambiente de desenvolvimento utilizado foi o Jupyter Notebook. No total, foram gerados 5 arquivos de código-fonte:
1. Importação Notícias.ipynb
2. Algoritmo de Frequencia.ipynb
3. Algoritmo de Luhn.ipynb
4. Algoritmo Similaridade Cosseno.ipynb
5. Métricas Rouge.ipynb

Na primeira etapa da implementação, basicamente, é realizada a leitura do arquivo "news_summary.xlsx" e a geração do arquivo "news.json" com uma limpeza dos registros e seleção apenas das colunas que serão utilizadas na análise dos algoritmos.

Na segunda etapa de processamento, o "Algoritmo baseado em frequência de palavras" é aplicado ao conjunto das 3965 notícias para a geração do sumário automático. No final da execução, os arquivos "algoritmo_frequencia.json" e "processamento_frequencia.json" são gerados respectivamente com os sumários automáticos e tempo de processamento do conjunto completo dos dados.

A terceira etapa de processamento consiste na execução do "Algoritmo de Luhn". No final da execução, os arquivos "algoritmo_luhn.json" e "processamento_luhn.json" são gerados respectivamente com os sumários automáticos e tempo de processamento do conjunto completo dos dados.

A quarta etapa de processamento consiste na execução do "Algoritmo TextRank com similaridade de cosseno". No final da execução, os arquivos "algoritmo_cosseno.json" e "processamento_cosseno.json" são gerados respectivamente com os sumários automáticos e tempo de processamento do conjunto completo dos dados.

Finalmente, a última etapa de processamento consite na aplicação das métricas Rouge (ROUGE-1, ROUGE-2 e ROUGE-L) para os três algoritmos em comparação aos sumários gerados manualmente e disponibilizados no dataset. Além disso, foram gerados alguns gráficos para melhor visualização dos resultados apresentados nos experimentos. Três arquivos são gerados durante a execução deste programa: rouge_frequencia.xlsx, rouge_luhn.xlsx e rouge_cosseno.xlsx. Esses arquivos possuem as métricas rouge para cada registro.

