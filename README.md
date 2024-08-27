# Modelo Série temporal WGG Digital

[![GPLv3 License](https://img.shields.io/badge/License-GPL%20v3-yellow.svg)](https://opensource.org/licenses/)
[![AGPL License](https://img.shields.io/badge/license-AGPL-blue.svg)](http://www.gnu.org/licenses/agpl-3.0)
[![author](https://img.shields.io/badge/author-RafaelGallo-red.svg)](https://github.com/RafaelGallo?tab=repositories) 
[![](https://img.shields.io/badge/python-3.7+-blue.svg)](https://www.python.org/downloads/release/python-374/) 
[![](https://img.shields.io/badge/R-3.6.0-red.svg)](https://www.r-project.org/)
[![](https://img.shields.io/badge/ggplot2-white.svg)](https://ggplot2.tidyverse.org/)
[![](https://img.shields.io/badge/transformers-white.svg)](https://huggingface.co/docs/transformers)
[![](https://img.shields.io/badge/Google_Cloud-white.svg)](https://huggingface.co/docs/transformers)
[![](https://img.shields.io/badge/dplyr-blue.svg)](https://dplyr.tidyverse.org/)
[![](https://img.shields.io/badge/readr-green.svg)](https://readr.tidyverse.org/)
[![](https://img.shields.io/badge/ggvis-black.svg)](https://ggvis.tidyverse.org/)
[![](https://img.shields.io/badge/Shiny-red.svg)](https://shiny.tidyverse.org/)
[![](https://img.shields.io/badge/plotly-green.svg)](https://plotly.com/)
[![](https://img.shields.io/badge/XGBoost-red.svg)](https://xgboost.readthedocs.io/en/stable/#)
[![](https://img.shields.io/badge/Tensorflow-orange.svg)](https://powerbi.microsoft.com/pt-br/)
[![](https://img.shields.io/badge/Keras-red.svg)](https://powerbi.microsoft.com/pt-br/)
[![](https://img.shields.io/badge/CUDA-gree.svg)](https://powerbi.microsoft.com/pt-br/)
[![](https://img.shields.io/badge/Caret-orange.svg)](https://caret.tidyverse.org/)
[![](https://img.shields.io/badge/Pandas-blue.svg)](https://pandas.pydata.org/) 
[![](https://img.shields.io/badge/Matplotlib-blue.svg)](https://matplotlib.org/)
[![](https://img.shields.io/badge/Seaborn-green.svg)](https://seaborn.pydata.org/)
[![](https://img.shields.io/badge/Matplotlib-orange.svg)](https://scikit-learn.org/stable/) 
[![](https://img.shields.io/badge/Scikit_Learn-green.svg)](https://scikit-learn.org/stable/)
[![](https://img.shields.io/badge/Numpy-white.svg)](https://numpy.org/) 

![cap](https://github.com/RafaelGallo/ML_Churn_Prediction_card/blob/main/imgs/buildings-fog.jpg)

Uma empresa global de vendas está monitorando o desempenho de suas metas de vendas em diferentes países ao longo do tempo. Os dados históricos mostram o percentual de atingimento das metas mensais de fevereiro de 2022 a dezembro de 2023 para cada país onde a empresa opera. O desafio é prever o percentual de atingimento das metas para janeiro de 2024, com o objetivo de ajustar e otimizar as estratégias de vendas e marketing para o próximo ano.

## Desafio
Prever o valor de atingimento de metas de vendas para janeiro de 2024 em cada país com base nos dados históricos. A empresa deseja utilizar essas previsões para:
Ajustar as Metas e Recursos: Identificar quais países podem precisar de ajustes nas metas ou de alocação adicional de recursos, como campanhas de marketing, para melhorar o desempenho de vendas. Planejamento de Estoque: Prever os níveis de demanda em diferentes países para otimizar o planejamento de estoque e evitar tanto excesso quanto falta de produtos. Otimização de Campanhas de Marketing: Desenvolver campanhas de marketing mais eficazes, direcionadas aos países com maior necessidade de suporte para atingir as metas de vendas. Gerenciamento de Riscos: Identificar potenciais riscos de não atingimento das metas em determinados países, permitindo à empresa implementar estratégias de mitigação de forma proativa.

## Problema negócio
Desenvolver um modelo preditivo que forneça estimativas precisas dos percentuais de atingimento das metas de vendas para janeiro de 2024 em cada país. O modelo deve ser capaz de capturar tendências, sazonalidades e outras variáveis temporais presentes nos dados históricos, proporcionando insights valiosos para as equipes de vendas e marketing.

## Indicadores de Sucesso
Precisão das Previsões: Avaliar o desempenho do modelo preditivo utilizando métricas como MAE ou RMSE.
Impacto nas Vendas: Medir o impacto das ações tomadas com base nas previsões, como a melhoria nas taxas de atingimento das metas em comparação com os meses anteriores.
Eficiência Operacional: Avaliar a redução de custos operacionais e de marketing como resultado de um planejamento mais preciso e otimizado.

## Abordagem:
Análise de Séries Temporais: Usar técnicas de análise de séries temporais para modelar e prever os valores futuros de atingimento de metas.
Ajustes Dinâmicos: Implementar um sistema que permita ajustes contínuos nas estratégias com base nas previsões geradas.

# Análise de dados

1.Gráfico Histrograma - Distribuição dos valores de atingimento de metas.

![](![image](https://github.com/user-attachments/assets/b50fb61a-2ffe-462b-a184-635872b07cab)

Este histograma mostra a distribuição dos valores de atingimento de metas, representando como as metas de vendas foram cumpridas ao longo do tempo ou entre diferentes países/regiões.

A maior parte dos registros está concentrada na faixa de 0,6 a 0,75. Isso indica que a maioria dos países ou regiões conseguiu atingir entre 60% e 75% das metas estabelecidas. Este resultado sugere um desempenho consistente em torno de 70% de atingimento das metas. Há relativamente poucos casos em que o atingimento de metas foi inferior a 50%, indicando que a maioria dos países ou regiões evitou quedas acentuadas no desempenho. Esses poucos casos de baixo desempenho (na faixa de 0,3 a 0,5) podem representar áreas ou períodos que necessitam de maior atenção ou investigação. A distribuição é levemente assimétrica para a esquerda, o que significa que os casos de baixo atingimento são menos frequentes, enquanto a maioria se encontra em torno de 0,7. Para o time de negócios, esses resultados indicam uma necessidade de reforçar estratégias para mover o desempenho geral para mais perto de 100%, buscando melhorias nas áreas que consistentemente ficam abaixo das metas. A análise pode ser segmentada por país ou período para identificar onde estão os maiores desafios e onde as estratégias bem-sucedidas podem ser replicadas.

2. Gráfico linhas de linhas mostra a evolução dos valores de atingimento de metas ao longo do tempo em três regiões: Colômbia/Equador, Peru e Brasil.

![image](https://github.com/user-attachments/assets/7d9880ab-e20f-45c5-b25b-98cd241eb694)

Colômbia/Equador: Esta região mostra uma tendência de altos e baixos acentuados, sugerindo uma volatilidade significativa no atingimento de metas. Há períodos de recuperação, seguidos por quedas abruptas. Peru: O Peru exibe uma curva mais estável no início de 2022, mas também passa por flutuações notáveis, especialmente no final de 2022 e 2023. No entanto, o aumento acentuado no final de 2023 pode indicar uma melhoria significativa no desempenho. Brasil: A linha do Brasil é a mais consistente entre as três regiões, embora também apresente algumas flutuações, especialmente no segundo semestre de 2022 e ao longo de 2023. No entanto, as variações não são tão acentuadas quanto nas outras regiões. Peru: Ao longo do tempo, o Peru parece estar recuperando terreno, especialmente no final de 2023, onde atinge o valor mais alto de atingimento de metas em comparação com as outras regiões. Brasil: Mantém uma posição relativamente estável, com uma leve tendência de aumento no final de 2023, indicando um desempenho mais previsível. Colômbia/Equador: Apesar de alguns períodos de bom desempenho, a região parece ter dificuldades para manter um crescimento consistente, com várias quedas notáveis ao longo do tempo. Volatilidade na Colômbia/Equador: A alta volatilidade sugere que pode haver fatores externos significativos ou desafios internos que precisam ser endereçados para estabilizar o desempenho. Esta região pode necessitar de uma análise detalhada para identificar as causas dessas flutuações e desenvolver estratégias para mitigar esses impactos. Recuperação no Peru: O aumento acentuado no final de 2023 no Peru é um sinal positivo. Isso pode indicar que as iniciativas recentes estão surtindo efeito, mas será importante continuar monitorando para garantir que essa melhoria seja sustentável. Consistência no Brasil: O Brasil, apesar de algumas variações, mostra um desempenho mais consistente ao longo do tempo. Esta estabilidade pode ser explorada para replicar as boas práticas em outras regiões. Análise das Causas: Investigar os fatores que contribuem para as flutuações, especialmente nas regiões de Colômbia/Equador e Peru, para entender melhor as influências externas e internas no atingimento de metas. Monitoramento Contínuo: Continuar monitorando as tendências ao longo do tempo para detectar mudanças emergentes no desempenho e ajustar as estratégias conforme necessário. Compartilhamento de Melhores Práticas: O Brasil pode servir como modelo para práticas estáveis que poderiam ser implementadas em outras regiões para melhorar a consistência no atingimento de metas.

3. Média móveis meta - Brasil

![image](https://github.com/RafaelGallo/ML_Serie_temporal_WGG_Digital/blob/main/img/005.png?raw=true)

Este gráfico ilustra as tendências dos valores de atingimento de metas para o Brasil ao longo do tempo, utilizando a série original (linha azul) e duas médias móveis (de 3 meses e 6 meses) para suavizar as flutuações de curto prazo e identificar tendências mais duradouras.

Insights importantes
Série Original (Linha Azul):

A linha azul representa os valores reais do atingimento de metas mês a mês. Podemos observar que há várias flutuações ao longo do tempo, com alguns picos e vales acentuados.
No entanto, há uma tendência geral de recuperação no final do período analisado, com os valores de atingimento de metas crescendo consistentemente após um período de baixa significativa.

Média Móvel de 3 Meses (Linha Vermelha):

A linha vermelha suaviza as flutuações de curto prazo, mostrando uma versão mais estabilizada da série temporal.
Ela reage mais rapidamente às mudanças na série original, mas ainda captura as principais tendências. Podemos observar que, mesmo com as flutuações, a média móvel de 3 meses acompanha bem a recuperação do desempenho, indicando que, apesar das variações, o Brasil tem mantido um crescimento sustentável ao longo do tempo.
Média Móvel de 6 Meses (Linha Verde):

A linha verde, representando a média móvel de 6 meses, é ainda mais suave e captura as tendências de longo prazo.

Essa linha mostra que, apesar das flutuações mensais, a tendência de longo prazo para o Brasil é positiva, com um crescimento gradual e mais consistente no atingimento de metas ao longo do tempo.

Este gráfico fornece uma visão clara de como o desempenho de vendas no Brasil evoluiu ao longo do tempo e como as médias móveis podem ser usadas para entender e prever melhor as tendências futuras. Ele é uma ferramenta valiosa para o time de negócios no processo de tomada de decisão e ajuste de estratégias.

4. Modelo ARIMA
   
![image](https://github.com/user-attachments/assets/8041797c-0e16-40d7-92a6-a6529bb93c97)

Este gráfico apresenta a evolução das metas de vendas para Colômbia/Equador ao longo do tempo, mostrando tanto os dados históricos de treino e teste (linha azul) quanto as previsões futuras (linha vermelha). Vamos analisar os principais pontos relevantes para o time de negócios:

Estabilidade e Crescimento: O período final de 2023 mostra que as metas de vendas alcançaram um pico, sugerindo que as estratégias adotadas estão dando certo. No entanto, é importante considerar que esse crescimento pode estar se estabilizando, o que indica a necessidade de continuar inovando para manter o desempenho ou encontrar novas oportunidades de crescimento.

Preocupação com o Declínio: A previsão de queda nas metas de vendas a partir de meados de 2024 pode ser um sinal de alerta para o time de negócios. É essencial investigar as causas potenciais dessa queda projetada. Fatores como mudanças de mercado, sazonalidade, ou possíveis desafios operacionais devem ser analisados para evitar que essa previsão se concretize.

Planejamento Proativo: Com base nessas previsões, o time de negócios deve considerar ajustes estratégicos, como campanhas de marketing direcionadas, ajustes na política de preços, ou expansão em novos mercados, para mitigar a possível queda nas metas e garantir que a empresa mantenha seu desempenho positivo.

# Avaliação modelos

O resultado que você obteve apresenta as métricas de avaliação para três modelos diferentes (ARIMA, SARIMA e Prophet) com base nos valores de MAE (Mean Absolute Error) e RMSE (Root Mean Squared Error). Aqui está uma interpretação dos resultados:

1. ARIMA

MAE: 0.061828
RMSE: 0.061828
Interpretação: O modelo ARIMA tem um erro absoluto médio e um erro quadrático médio em torno de 0.0618, o que indica que, em média, as previsões do modelo estão desviando dos valores reais por esse montante.

2. SARIMA

MAE: 0.015966
RMSE: 0.015966
Interpretação: O modelo SARIMA mostra um desempenho significativamente melhor do que o ARIMA, com erros médios (MAE e RMSE) menores, sugerindo que o SARIMA está conseguindo capturar melhor a sazonalidade e outras características dos dados.

3. Prophet

MAE: 0.000005
RMSE: 0.000005
Interpretação: O modelo Prophet apresenta os menores valores de erro, indicando que este modelo tem o melhor desempenho entre os três, com as previsões mais próximas dos valores reais.

Considerações Finais:
Melhor Modelo: Com base nos valores de MAE e RMSE, o modelo Prophet é o que apresenta o melhor desempenho, seguido pelo SARIMA e, por último, o ARIMA. Isso sugere que o Prophet é o mais adequado para capturar as dinâmicas presentes nos seus dados. Adoção do Modelo: Dado o excelente desempenho do Prophet, ele seria a escolha mais lógica para fazer previsões de metas de vendas. No entanto, como sempre, é importante considerar o contexto de negócios e a aplicabilidade do modelo em cenários específicos.

# Conclusão

Para desenvolver um modelo preditivo capaz de fornecer estimativas precisas dos percentuais de atingimento das metas de vendas para janeiro de 2024 em cada país (Colômbia/Equador, Peru e Brasil), foram aplicados os modelos ARIMA, SARIMA e Prophet. Esses modelos foram escolhidos por suas capacidades de capturar tendências, sazonalidades e outras variáveis temporais presentes nos dados históricos.

Análise dos Modelos:

1. Modelo ARIMA

O modelo ARIMA foi aplicado com parâmetros definidos para capturar a natureza não estacionária dos dados.
Ele mostrou resultados moderados em termos de precisão, com um erro absoluto médio (MAE) de 0.061828, e RMSE de 0.061828.
Apesar de ter capturado bem as tendências, o ARIMA teve dificuldades em capturar todas as nuances sazonais, como é observado em comparações com os outros modelos.

2. Modelo SARIMA

O SARIMA estendeu o ARIMA, incorporando componentes sazonais (com parâmetros sazonais), permitindo uma modelagem mais precisa das variações sazonais.
Este modelo apresentou uma precisão superior ao ARIMA, com um MAE de 0.015966 e RMSE de 0.015966, indicando uma melhor performance na previsão de padrões sazonais e tendências.
Nos gráficos, podemos ver que o SARIMA captura tanto a tendência quanto as variações sazonais, oferecendo previsões mais ajustadas para os meses seguintes.

3. Modelo Prophet

O Prophet foi escolhido por sua robustez e facilidade em modelar dados com forte sazonalidade e efeitos de feriados.
Incrivelmente, apresentou o menor erro absoluto médio (MAE de 0.000005) e RMSE (0.000005), o que indica uma excelente capacidade de previsão.
No entanto, ao avaliar o comportamento visual do modelo, ele parece ser muito sensível a outliers, mostrando grandes flutuações na previsão para o período futuro. Isso pode indicar uma necessidade de ajuste ou de revisão dos hiperparâmetros utilizados.

Os modelos SARIMA e Prophet se destacaram como os mais adequados para prever os percentuais de atingimento de metas de vendas. Enquanto o Prophet apresentou o menor erro de previsão, ele pode ser sensível a outliers, e o SARIMA oferece um balanço entre precisão e estabilidade das previsões.
Para as equipes de vendas e marketing, os resultados sugerem que o SARIMA pode fornecer estimativas mais consistentes para o planejamento estratégico, capturando as tendências e sazonalidades específicas de cada país. O Prophet, embora preciso, deve ser aplicado com cautela, especialmente se os dados contiverem outliers significativos. Em síntese, ambos os modelos podem fornecer insights valiosos, mas a escolha final dependerá da robustez necessária nas previsões e da natureza dos dados históricos disponíveis.
