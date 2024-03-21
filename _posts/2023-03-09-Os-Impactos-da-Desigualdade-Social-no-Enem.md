---
layout: post
title:  "Os Impactos da Desigualdade no Enem"
date:   2023-09-02 23:28:15 -0300
categories: jekyll update
---


## Resumo
	
Este trabalho tem como objetivo explorar as desigualdades sociais de acesso à educação no Brasil. Serão utilizados dados das notas do Exame Nacional do Ensino Médio (Enem) antes e depois da implementação do sistema de cotas, a fim de investigar a relação entre nota, etnia, sexo e nível de formação dos pais dos estudantes. A variável preditora escolhida será a nota de matemática, devido às discrepâncias no acesso à educação neste campo no Brasil. Além disso, técnicas estatísticas serão aplicadas para avaliar a significância das diferenças nas notas dos alunos antes e depois da implementação das cotas, bem como para identificar as principais variáveis que afetam o desempenho acadêmico dos estudantes. O uso de técnicas de regressão linear também será explorado, a fim de desenvolver um modelo preditivo que possa ser usado para prever notas do Enem, e para orientar as políticas públicas de inclusão nas universidades.

Palavras-chave: desigualdades sociais, acesso à educação, análise de dados, políticas públicas.

---

## Introdução
A busca por igualdade de oportunidades no acesso à educação é uma pauta vigente há muito tempo e recentemente alguns passos importantes tem sido dados no que tange uma série de políticas afirmativas voltadas para a promoção da diversidade étnica e cultural, bem como para a equidade de gênero dentro das univesidades públicas brasileiras. Desde a implementação da Lei 12.711, em 2012, que introduziu o sistema de cotas no Exame Nacional do Ensino Médio (Enem), até a recente adoção de políticas afirmativas por universidades como a Universidade de São Paulo (USP) e a Universidade Estadual de Campinas (Unicamp), avanços significativos têm sido feitos no sentido de proporcionar acesso à educação superior a grupos historicamente marginalizados.

Essas iniciativas refletem a consciência crescente de que o Brasil carrega uma dívida histórica para com sua população indígena e preta. O racismo, como observado por Sueli Carneiro (1999), permeia as estruturas sociais brasileiras desde sua origem, impondo obstáculos persistentes ao acesso à educação. Ao longo dos séculos, esses grupos foram submetidos a opressões sistêmicas e violentas, moldando profundamente as experiências sociais e educacionais de milhares de brasileiros ao longo de gerações. 

Lélia Gonzalez (1984) expõe a existência entrelaçada do racismo e sexismo na cultura brasileira, cujas manifestações variam entre sutilezas veladas e violências explícitas. Essas formas de opressão encontram reflexo nas realidades das mulheres pretas e indígenas, que enfrentam barreiras múltiplas e complexas para acessar oportunidades educacionais de qualidade. Especialmente as mulheres indígenas se veem em um contexto de vulnerabilidade social, onde o acesso a escolas de qualidade em suas comunidades é frequentemente comprometido (Kayapó et al., 2022).

As universidades públicas, reconhecidas por sua excelência educacional e contribuições científicas, também reproduzem essas desigualdades. Os vestibulares, moldados por uma cultura acadêmica que muitas vezes reflete privilégios da elite branca, podem ser inacessíveis para grupos étnicos marginalizados. As cotas são um dos instrumentos para enfrentar essa desigualdade, porém, como ressaltado por Sueli Carneiro (1999), é necessário um esforço coletivo e abrangente de todos os segmentos da sociedade para combater o racismo e o sexismo sistêmicos.

Neste contexto, uma análise abrangente das notas do Exame Nacional do Ensino Médio (Enem) emerge como uma ferramenta interessante para compreender a fundo essas disparidades e direcionar ações transformadoras. O Enem tornou-se um instrumento crucial para avaliar a qualidade da educação no país e, consequentemente, para refletir as desigualdades educacionais e sociais existentes. Compreender como as políticas afirmativas, como as cotas, afetaram as desigualdades na educação e como essas desigualdades estão interligadas com fatores como raça, gênero e formação dos pais é uma abordagem necessária para orientar políticas inclusivas e justas.

A análise das notas do Enem revela desigualdades marcantes relacionadas a fatores como raça, gênero e nível de formação dos pais. Participantes negros, pardos e indígenas tendem a apresentar médias de notas inferiores em comparação com participantes brancos. Além disso, mulheres têm notas significativamente mais baixas que homens, destacando a interseccionalidade entre desigualdades de gênero e raça, corroborando os estudos de Sueli Carneiro (1999).

Essa análise, embora exploratória, enfatiza a urgência contínua de abordagens inclusivas nas universidades e a importância de políticas afirmativas que abordem as opressões de raça e gênero. Cabe ressaltar que esse estudo é um ponto de partida e análises mais aprofundadas são necessárias para compreender essas diferenças em sua totalidade.

Ao explorar essas questões, fica claro que a busca por igualdade de acesso à educação é um processo multifacetado e em constante evolução. A promoção da diversidade e a construção de uma sociedade mais justa e inclusiva requerem um compromisso conjunto de toda a sociedade, com especial atenção às necessidades das mulheres pretas e indígenas, grupos que há muito foram marginalizados em seu acesso à educação e oportunidades.

## Material e Métodos
	
Para realizar a análise dos dados do Exame Nacional do Ensino Médio (Enem) dos anos de 2011, 2018 e 2020, a autora deste trabalho coletou os microdados disponibilizados pelo Instituto Nacional de Estudos e Pesquisas Educacionais Anísio Teixeira (INEP), que é o órgão responsável pela organização e aplicação do exame no Brasil. Esses dados foram obtidos em formato CSV (comma-separated value) e importados para um dataframe pandas utilizando a função read_csv(). Todos os códigos usados para análise, exploração de gráfico e geração de gráficos foram implementados na linguagem Python. Mais especificamente, as análises estatísticas foram feitas por meio da biblioteca pandas, a geração dos gráficos por meio das bibliotecas matplotlib e seaborn e os métodos de regressão estatística por meio da biblioteca scikit-learn.

Após a importação dos dados, foi realizada uma etapa de pré-processamento, onde as colunas relevantes para a análise foram selecionadas, referentes às notas de matemática, linguagem e código, ciências humanas, ciências da natureza, sexo, raça e nível de formação da mãe e do pai. Os valores ausentes foram removidos.

Para calcular a desigualdade entre as notas dos diferentes grupos raciais e de gênero, utilizou-se a diferença entre as medianas das notas. A mediana é um valor que divide um conjunto de dados em duas partes iguais e é menos sensível a valores discrepantes em relação à média. Já a média é um valor que representa a tendência central de um conjunto de dados e pode ser influenciada por valores discrepantes. Foram plotados boxplots, para melhor visualizar a distribuição do conjunto de dados. Composto por uma caixa que representa o intervalo interquartil (50% dos dados), o boxplot possui uma linha mediana que divide a caixa em duas partes iguais e dois segmentos chamados de bigodes, que representam a dispersão dos dados dentro do intervalo interquartil, e possíveis pontos ou valores discrepantes.  Em seguida, foram plotados gráficos que mostram essa desigualdade de notas por grupos raciais e de gênero, utilizando a biblioteca seaborn.

Também foi criado um modelo de regressão linear usando a classe LinearRegression do scikit-learn e treinado no conjunto de treinamento usando a função fit. Em seguida, a previsão das notas foi feita no conjunto de teste usando a função predict. O erro RMSE foi calculado usando a função mean_squared_error da biblioteca sklearn.metrics.

Por fim, foi realizada a análise estatística dos resultados obtidos, utilizando técnicas como regressão linear e cálculo de medianas, além da exploração e visualização das relações entre as variáveis disponíveis por meio de gráficos gerados.

Em resumo, este trabalho utilizou dados do Enem disponibilizados pelo INEP para avaliar a relação entre a formação acadêmica dos pais, a raça e o gênero dos estudantes e seu desempenho no exame. A partir da análise dos dados, foram identificadas possíveis disparidades que precisam ser abordadas por políticas públicas de inclusão nas universidades. Além disso, foram desenvolvidos modelos preditivos que podem ser utilizados para orientar essas políticas e melhorar a inclusão de grupos historicamente marginalizados na educação superior.

## Resultados e Discussão 
![image](https://github.com/R-it-a/r-it-a.github.io/assets/75498905/e1583114-4cbc-40cc-9fbb-3e408bf3c8e4)

![Book quantidade](/r-it-a.github.io/assets/imgs/quantidade.png)


## Conclusão(ões) ou Considerações Finais

A análise dos dados do Enem revelou desigualdades significativas nas notas em relação a fatores como raça, gênero e nível de formação dos pais, com participantes negros, pardos e indígenas tendo medianas e distribuições de notas mais baixas do que participantes brancos. As participantes femininas têm notas significativamente mais baixas do que os participantes masculinos, embora muito mais mulheres do que homens se inscrevam para o Enem. Isso sugere que há uma interseccionalidade entre as desigualdades de gênero e de raça, consoante com o que é apontado por Sueli Carneiro (1999). As conclusões ressaltam a urgência e continuidade de abordagens inclusivas nas universidades e políticas afirmativas que reconheçam e mitiguem as opressões de raça e gênero para que o passado não seja projetado no futuro de maneira injusta e violenta. Por fim, é importante ressaltar que essa é uma análise exploratória e que outras análises mais sofisticadas podem ser realizadas para investigar essas diferenças com mais profundidade.

## Agradecimento 
Agradeço aos meus pais, que com sua força me inspiram todos os dias. Agradeço a Giovana, sem a qual nada disso seria possível, e ao Felipe, cujas referências antirracistas são sempre indicações certeiras.  

## Referências

Carneiro, S. "Racismo, Sexismo e Desigualdade no Brasil." Revista de Estudos Avançados, vol. 13, no. 35, 1999, pp. 117-136.

Cathy O’Neil. Algoritmos de Destruição em Massa. 2021

Gonzalez, L.. "Racismo e Sexismo na Cultura Brasileira." Cadernos do Terceiro Mundo, vol. 46, 1984, pp. 27-31.

Kambeba, Márica. "Cotas Raciais e o Acesso dos Povos Indígenas ao Ensino Superior". Publicado na Revista Brasileira de Estudos Pedagógicos, vol. 97, no. 246, jan./abr. 2016, pp. 217-234.

Kayapó et al. “O acesso dos povos indígenas ao ensino superior.” Publicado na Revista Le Monde Diplomatique, jul.2022.

Silva, Sônia e Carvalho, Marília. "Cotas Raciais e o Acesso ao Ensino Superior pelos Indígenas Brasileiros". Publicado na Revista Brasileira de Política e Administração da Educação, vol. 29, no. 1, jan./abr. 2013, pp. 135-149.
