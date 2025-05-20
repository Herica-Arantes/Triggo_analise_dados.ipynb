# Triggo_analise_dados.ipynb

Com base nos resultados obtidos pela execução do código:

a) Volume de pedidos por mês e sazonalidade: O volume de pedidos por mês varia ao longo do tempo, apresentando um padrão sazonal perceptível, com um aumento significativo de pedidos no final de cada ano. Há uma tendência geral de crescimento no volume de pedidos ao longo dos meses analisados.

b) Distribuição do tempo de entrega dos pedidos: A maioria dos pedidos é entregue dentro de um período de 25 a 30 dias. No entanto, a distribuição do tempo de entrega é assimétrica, com a presença de alguns pedidos que levam consideravelmente mais tempo para serem entregues (outliers).

c) Relação entre o valor do frete e a distância de entrega: Embora uma análise precisa exija o cálculo direto da distância entre CEPs, a análise exploratória do frete médio por par de estados do vendedor e do cliente sugere que a distância regional impacta o valor do frete, com fretes mais altos tendendo a ocorrer entre estados mais distantes.

d) Categorias de produtos mais vendidas em termos de faturamento: As categorias de produtos que geram maior faturamento total são 'bed_bath_table', 'health_beauty' e 'sports_leisure'.

e) Estados brasileiros com maior valor médio de pedido: Os estados brasileiros com maior valor médio de pedido são:

RR
AP
AM
BA
PI
MT
RO
SE
PB
TO


# Análise de Dados de E-commerce Brasileiro

Este projeto realiza uma análise exploratória e modelagem básica em um conjunto de dados de e-commerce brasileiro, utilizando Google Colab, Python, Pandas, Matplotlib, Seaborn, Plotly e SQLite.

## Como Executar o Projeto

1.  **Abra o Notebook no Google Colab:**
    *   Certifique-se de que você tem acesso ao notebook `seu_notebook_nome.ipynb` (substitua pelo nome real do seu arquivo) no GitHub.
    *   No GitHub, navegue até o arquivo do notebook (`.ipynb`).
    *   Clique no botão "Open in Colab" (se disponível) ou copie a URL do arquivo `.ipynb`.
    *   Vá para o Google Colab ([https://colab.research.google.com/](https://colab.research.google.com/)) e abra o notebook usando a URL ou navegando pelo GitHub.

2.  **Certifique-se de ter os dados:**
    *   Os arquivos CSV necessários para a análise devem estar presentes no ambiente do Colab. Se você estiver rodando a partir do seu drive, certifique-se de que os arquivos estão na pasta correta. Se os dados não estiverem incluídos no repositório GitHub, você precisará fazer o upload manual dos arquivos CSV para o ambiente de execução do Colab ou conectá-lo ao seu Google Drive onde os dados estão armazenados. O código atual assume que os arquivos CSV estão no mesmo diretório que o notebook ou foram carregados para o ambiente.

3.  **Execute as Células:**
    *   Execute as células do notebook sequencialmente. O notebook é projetado para ser executado de cima para baixo.
    *   Você pode executar cada célula individualmente clicando no ícone de "Play" ao lado da célula ou executar todas as células clicando em "Runtime" -> "Run all" no menu superior.
    *   O código realizará a importação de bibliotecas, carregamento dos dados, tratamento (remoção de duplicatas, preenchimento de nulos, tradução de categorias), criação de um DataFrame unificado, análise exploratória usando Python (Pandas) e SQL (SQLite), modelagem de classificação (previsão de atraso) e análise de segmentação de clientes (RFM + Clustering). As visualizações interativas serão geradas usando Plotly.

## Principais Resultados Encontrados

A análise revelou insights importantes sobre o comportamento de compra, logística e satisfação do cliente:

*   **Volume de Pedidos:** O volume de pedidos por mês mostra uma clara sazonalidade, com picos observados no final do ano. Houve também um crescimento geral no volume de pedidos ao longo do tempo no período analisado.
*   **Tempo de Entrega:** A maioria dos pedidos é entregue em até 25-30 dias. No entanto, existem outliers que representam entregas significativamente mais longas.
*   **Frete:** A distribuição do valor do frete foi analisada. A análise simplificada por par de estados sugere que a distância geográfica impacta o valor do frete, como esperado.
*   **Faturamento por Categoria de Produto:** As categorias de produtos com maior faturamento total incluem 'bed_bath_table', 'health_beauty' e 'sports_leisure'.
*   **Valor Médio de Pedido por Estado:** Foram identificados os estados brasileiros com maior valor médio de pedido.
*   **Taxa de Recorrência:** Uma análise inicial mostrou a taxa de clientes recorrentes no conjunto de dados.
*   **Previsão de Atraso:** Foi construído um modelo de Regressão Logística para prever se um pedido será entregue com atraso, utilizando features como preço, frete e tempo de envio estimado. As métricas de avaliação (Precision, Recall, F1-Score, AUC) indicam o desempenho do modelo nesta tarefa.
*   **Segmentação de Clientes:** A segmentação de clientes foi realizada utilizando RFM (Recência, Frequência, Valor Monetário) e métricas adicionais como Nota Média de Avaliação e Tempo Médio de Entrega. O método K-Means foi aplicado para agrupar clientes com comportamentos semelhantes. Os perfis de cluster revelam características distintas para cada segmento de cliente.
*   **Visualizações:** Foram geradas diversas visualizações (gráficos de linha, barras, scatter plots, box plots) para ilustrar a evolução das vendas, concentração por estado, relação entre tempo de entrega e satisfação, e métricas de desempenho de vendedores.

## Ferramentas e Bibliotecas Utilizadas

*   Google Colab
*   Python
*   Pandas
*   NumPy
*   Matplotlib
*   Seaborn
*   Plotly
*   SQLite
*   Scikit-learn
