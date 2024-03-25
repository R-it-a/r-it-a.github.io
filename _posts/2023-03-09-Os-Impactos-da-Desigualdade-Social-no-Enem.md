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

Neste contexto, uma análise abrangente das notas do Exame Nacional do Ensino Médio (Enem) emerge como uma ferramenta interessante para compreender a fundo essas disparidades e direcionar ações transformadoras. O Enem tornou-se um instrumento crucial para avaliar a qualidade da educação no país e, consequentemente, para refletir as desigualdades educacionais e sociais existentes. Compreender como as políticas afirmativas, como as cotas, afetaram as desigualdades na educação e como essas desigualdades estão interligadas com fatores como cor de pele, gênero e formação dos pais é uma abordagem necessária para orientar políticas inclusivas e justas.

A análise das notas do Enem revela desigualdades marcantes relacionadas a fatores como cor de pele, gênero e nível de formação dos pais. Participantes negros, pardos e indígenas tendem a apresentar médias de notas inferiores em compacor de peleo com participantes brancos. Além disso, mulheres têm notas significativamente mais baixas que homens, destacando a interseccionalidade entre desigualdades de gênero e cor de pele, corroborando os estudos de Sueli Carneiro (1999).

Essa análise, embora exploratória, enfatiza a urgência contínua de abordagens inclusivas nas universidades e a importância de políticas afirmativas que abordem as opressões de cor de pele e gênero. Cabe ressaltar que esse estudo é um ponto de partida e análises mais aprofundadas são necessárias para compreender essas diferenças em sua totalidade.

Ao explorar essas questões, fica claro que a busca por igualdade de acesso à educação é um processo multifacetado e em constante evolução. A promoção da diversidade e a construção de uma sociedade mais justa e inclusiva requerem um compromisso conjunto de toda a sociedade, com especial atenção às necessidades das mulheres pretas e indígenas, grupos que há muito foram marginalizados em seu acesso à educação e oportunidades.

## Material e Métodos
	
Para realizar a análise dos dados do Exame Nacional do Ensino Médio (Enem) dos anos de 2011, 2018 e 2020, a autora deste trabalho coletou os microdados disponibilizados pelo Instituto Nacional de Estudos e Pesquisas Educacionais Anísio Teixeira (INEP), que é o órgão responsável pela organização e aplicação do exame no Brasil. Esses dados foram obtidos em formato CSV (comma-separated value) e importados para um dataframe pandas utilizando a função read_csv(). Todos os códigos usados para análise, explocor de peleo de gráfico e gecor de peleo de gráficos foram implementados na linguagem Python. Mais especificamente, as análises estatísticas foram feitas por meio da biblioteca pandas, a gecor de peleo dos gráficos por meio das bibliotecas matplotlib e seaborn e os métodos de regressão estatística por meio da biblioteca scikit-learn.

Após a importação dos dados, foi realizada uma etapa de pré-processamento, onde as colunas relevantes para a análise foram selecionadas, referentes às notas de matemática, linguagem e código, ciências humanas, ciências da natureza, sexo, cor de pele e nível de formação da mãe e do pai. Os valores ausentes foram removidos.

Para calcular a desigualdade entre as notas dos diferentes grupos raciais e de gênero, utilizou-se a diferença entre as medianas das notas. A mediana é um valor que divide um conjunto de dados em duas partes iguais e é menos sensível a valores discrepantes em relação à média. Já a média é um valor que representa a tendência central de um conjunto de dados e pode ser influenciada por valores discrepantes. Foram plotados boxplots, para melhor visualizar a distribuição do conjunto de dados. Composto por uma caixa que representa o intervalo interquartil (50% dos dados), o boxplot possui uma linha mediana que divide a caixa em duas partes iguais e dois segmentos chamados de bigodes, que representam a dispersão dos dados dentro do intervalo interquartil, e possíveis pontos ou valores discrepantes.  Em seguida, foram plotados gráficos que mostram essa desigualdade de notas por grupos raciais e de gênero, utilizando a biblioteca seaborn.

Também foi criado um modelo de regressão linear usando a classe LinearRegression do scikit-learn e treinado no conjunto de treinamento usando a função fit. Em seguida, a previsão das notas foi feita no conjunto de teste usando a função predict. O erro RMSE foi calculado usando a função mean_squared_error da biblioteca sklearn.metrics.

Por fim, foi realizada a análise estatística dos resultados obtidos, utilizando técnicas como regressão linear e cálculo de medianas, além da explocor de peleo e visualização das relações entre as variáveis disponíveis por meio de gráficos gerados.

Em resumo, este trabalho utilizou dados do Enem disponibilizados pelo INEP para avaliar a relação entre a formação acadêmica dos pais, a cor de pele e o gênero dos estudantes e seu desempenho no exame. A partir da análise dos dados, foram identificadas possíveis disparidades que precisam ser abordadas por políticas públicas de inclusão nas universidades. Além disso, foram desenvolvidos modelos preditivos que podem ser utilizados para orientar essas políticas e melhorar a inclusão de grupos historicamente marginalizados na educação superior.

## Resultados e Discussão 

Quando foi realizada uma análise inicial dos dados do Enem, observou-se conforme demonstrado na figura1, que as mulheres constituem aproximadamente 20% a mais dos participantes no ENEM em comparação aos homens. Contudo, as notas obtidas pelos homens superam significativamente as das mulheres. Tal discrepância não apenas reflete diferenças no acesso à educação entre gêneros, mas também evidencia um desencorajamento persistente que afeta as mulheres no que tange aos estudos nas áreas de exatas. Essa situação sublinha a necessidade de abordar tanto as barreiras estruturais quanto os estereótipos de gênero que limitam o pleno potencial acadêmico feminino, especialmente nas ciências, tecnologia, engenharia e matemática (STEM).

![image](https://github.com/R-it-a/r-it-a.github.io/assets/75498905/e1583114-4cbc-40cc-9fbb-3e408bf3c8e4)
Fig.1

![image](https://github.com/R-it-a/r-it-a.github.io/assets/75498905/e4c91255-8b5f-4085-8b11-987d6c32a537)
Fig.2

A análise dos resultados obtidos no Exame Nacional do Ensino Médio (ENEM) revela uma discrepância significativa nas pontuações de matemática entre gêneros, com uma diferença média de 60 unidades a favor dos candidatos masculinos no ano de 2011, com uma ligeira melhora em 2018 e uma piora novamente em 2020.

Consoante com estudos recentes sobre autodeclaração, observa-se que ao longo do período de 2011 à 2018, temos um movimento decrescente de autoidentificação enquanto branco, e cada vez mais pessoas se entendendo como pretas e pardas.

![image](https://github.com/R-it-a/r-it-a.github.io/assets/75498905/58ac762a-7e3e-42a8-9e94-72bbe733fe08)
Fig 3


O teste de Tukey HSD (Diferença Honesta Significativa) demosntado abaixo é um método estatístico utilizado para realizar comparações múltiplas entre as médias de diferentes grupos, após a realização de uma ANOVA (Análise de Variância). Se a ANOVA indica que há diferenças significativas entre as médias dos grupos, o teste de Tukey HSD pode ser aplicado para determinar especificamente quais pares de grupos diferem entre si. Aqui está um resumo de como ele funciona. 
A análise apresentada acima utiliza o teste de Tukey HSD (Diferença Honesta Significativa) para explorar diferenças estatísticas nas notas médias de matemática entre diversos grupos de identidade racial de participantes do ENEM. Este teste compara as médias de todos os pares de grupos, ajustando para múltiplas comparações e fornecendo uma medida robusta de diferenças significativas entre eles. Os resultados revelam variações substanciais nas notas médias, indicando que alguns grupos raciais, especificamente os identificados como amarelos e brancos, tendem a ter desempenhos superiores comparados a outros grupos, como os indígenas. Ao destacar essas disparidades, a análise aponta para a importância de investigar as causas subjacentes e desenvolver intervenções educacionais que promovam a equidade no acesso e na qualidade da educação matemática para todos os estudantes, independentemente de sua identidade racial.

  Multiple Comparison of Means - Tukey HSD, FWER=0.05        
===================================================================
    group1        group2    meandiff p-adj  lower    upper   reject
-------------------------------------------------------------------
      amarelo        branco  35.1398   0.0  33.7452  36.5345   True
      amarelo      indigena  -59.964   0.0 -63.0284 -56.8997   True
      amarelo nao_declarado   7.9741   0.0   5.9863   9.9618   True
      amarelo         pardo -23.9514   0.0   -25.34 -22.5628   True
      amarelo         preto -36.3929   0.0 -37.8676 -34.9181   True
       branco      indigena -95.1039   0.0 -97.8715 -92.3363   True
       branco nao_declarado -27.1658   0.0 -28.6558 -25.6758   True
       branco         pardo -59.0912   0.0 -59.5354  -58.647   True
       branco         preto -71.5327   0.0 -72.1991 -70.8664   True
     indigena nao_declarado  67.9381   0.0  64.8292   71.047   True
     indigena         pardo  36.0127   0.0  33.2482  38.7772   True
     indigena         preto  23.5712   0.0  20.7624    26.38   True
nao_declarado         pardo -31.9254   0.0 -33.4098 -30.4411   True
nao_declarado         preto -44.3669   0.0 -45.9321 -42.8017   True
        pardo         preto -12.4415   0.0  -13.095  -11.788   True

-------------------------------------------------------------------

Na Figura 4, 5 e 6, a disparidade nas notas médias, organizadas por grupo racial, é notavelmente evidenciada. A análise revela que indivíduos identificados como brancos apresentam médias superiores em comparação aos demais grupos raciais. Especial atenção é direcionada à situação dos povos indígenas, cujas médias são as mais baixas dentre os grupos analisados. Este cenário sublinha a urgente necessidade de expandir o acesso à educação de qualidade em todo o território nacional, garantindo que políticas educacionais inclusivas e respeitosas sejam implementadas, com foco especial na realidade e nas demandas dos povos indígenas. Este passo é fundamental para a construção de uma sociedade mais justa e igualitária, onde as oportunidades educacionais não sejam limitadas por barreiras raciais.


![image](https://github.com/R-it-a/r-it-a.github.io/assets/75498905/3bdf07cb-609d-4ac7-bc3f-73aeca24d977)
Fig4

![image](https://github.com/R-it-a/r-it-a.github.io/assets/75498905/a917a8c7-5645-4669-b605-bf9faf611ea7)
Fig5

Ao analisar o gráfico da Fig 7, fica evidente que as mulheres brancas têm, em média, notas mais altas em Matemática do que mulheres indígenas, pretas e pardas. Isso sugere que as mulheres brancas apresentam um desempenho acadêmico superior nessa disciplina em comparação com mulheres desses grupos étnicos. Além disso, é importante ressaltar que ser mulher dentro desses grupos amplifica as disparidades educacionais existentes. As mulheres enfrentam desafios específicos relacionados ao acesso à educação, discriminação de gênero, expectativas sociais e oportunidades limitadas de desenvolvimento acadêmico e profissional. Essas disparidades de gênero, combinadas com as raciais, aprofundam ainda mais as desigualdades no desempenho acadêmico. Portanto, compreender a interseccionalidade de gênero e cor de pele é crucial para entender as complexas dinâmicas que afetam o acesso à educação e o desempenho acadêmico das mulheres pertencentes a grupos étnicos minoritários. Isso destaca a urgência de políticas educacionais inclusivas que abordem essas desigualdades interseccionais, promovendo equidade e oportunidades iguais para todas as mulheres, independentemente de sua origem étnica.

![image](https://github.com/R-it-a/r-it-a.github.io/assets/75498905/c7f1543a-9522-46f4-99d7-aa9bfbe4d615)
Fig 6

A fugura 8 eo gráfico "Notas Médias de Matemática por Nível de Formação da Mãe (2020)" apresenta uma análise sobre a relação entre o desempenho acadêmico em matemática dos estudantes e o nível de formação educacional de suas mães. Os eixos do gráfico representam, respectivamente, os diferentes níveis de formação da mãe e as notas médias de matemática dos estudantes. As barras coloridas indicam as médias das notas para cada categoria de formação da mãe, enquanto a linha de regressão linear, destacada em laranja, mostra a tendência geral nos dados.

![image](https://github.com/R-it-a/r-it-a.github.io/assets/75498905/1f778b05-d471-4877-b038-4d6bc4a1b83e)
Fig 7

Observa-se uma clara associação entre o nível de formação da mãe e as notas médias de matemática dos estudantes. Quanto mais elevado o nível educacional da mãe, maior tende a ser o desempenho acadêmico de seus filhos em matemática. Os estudantes cujas mães concluíram a faculdade ou a pós-graduação apresentam notas médias mais altas em matemática em comparação com aqueles cujas mães possuem um nível de formação mais baixo, como nunca ter estudado ou não completar a 4ª série.

A linha de regressão linear reforça essa tendência, indicando uma relação positiva entre o nível de formação da mãe e as notas médias de matemática dos estudantes. O valor de R² da regressão linear, que expressa a proporção da variação nas notas explicada pelo nível de formação da mãe, sugere uma adequação satisfatória do modelo à tendência dos dados.
![image](https://github.com/R-it-a/r-it-a.github.io/assets/75498905/7cc972ac-6599-4dfb-8873-735aa30a9f30)
Fig 8

Esses resultados ressaltam a importância do papel da educação materna no desempenho acadêmico dos filhos, destacando a necessidade de estratégias voltadas para o aprimoramento do acesso e da qualidade da educação para as mães. Investimentos nessa área podem contribuir significativamente para a promoção da igualdade de oportunidades educacionais e para a melhoria do desempenho escolar das futuras gerações.
Os gráficos evidenciam que, mesmo entre mães pretas, pardas e indígenas, um maior nível de escolaridade está associado a notas mais altas de suas filhas em matemática. Isso ressalta a importância crucial da educação materna nessas comunidades, mostrando que quando mães desses grupos étnico-raciais têm acesso à educação de qualidade, suas filhas também se beneficiam, obtendo melhores resultados acadêmicos. Portanto, investir na educação das mães pretas, pardas e indígenas não só promove a equidade e a inclusão, mas também é uma estratégia eficaz para melhorar o desempenho escolar de suas filhas e quebrar ciclos de desigualdade.
Os gráficos destacam que as alunas que se beneficiam das políticas de cotas, especialmente aquelas provenientes de famílias pretas, pardas e indígenas, têm o potencial de transformar significativamente o futuro. Ao terem acesso à educação superior por meio dessas políticas inclusivas, essas jovens não apenas têm a oportunidade de romper com as barreiras socioeconômicas e raciais que historicamente as têm prejudicado, mas também se tornam agentes de mudança em suas comunidades. Ao conquistarem suas formações acadêmicas, elas se capacitam para contribuir de maneira significativa para a construção de uma sociedade mais justa e igualitária, promovendo a diversidade e a inclusão em todos os aspectos da vida social, econômica e política.

## Conclusão(ões) ou Considerações Finais

A análise dos dados do Enem revelou desigualdades significativas nas notas em relação a fatores como cor de pele, gênero e nível de formação dos pais, com participantes negros, pardos e indígenas tendo medianas e distribuições de notas mais baixas do que participantes brancos. As participantes femininas têm notas significativamente mais baixas do que os participantes masculinos, embora muito mais mulheres do que homens se inscrevam para o Enem. Isso sugere que há uma interseccionalidade entre as desigualdades de gênero e de cor de pele, consoante com o que é apontado por Sueli Carneiro (1999). As conclusões ressaltam a urgência e continuidade de abordagens inclusivas nas universidades e políticas afirmativas que reconheçam e mitiguem as opressões de cor de pele e gênero para que o passado não seja projetado no futuro de maneira injusta e violenta. Por fim, é importante ressaltar que essa é uma análise exploratória e que outras análises mais sofisticadas podem ser realizadas para investigar essas diferenças com mais profundidade.

## Agradecimento 
Agradeço aos meus pais, que com sua força me inspiram todos os dias. Agradeço a Giovana, sem a qual nada disso seria possível, e ao Felipe, cujas referências antirracistas são sempre indicações certeiras.  

## Referências

Carneiro, S. "Racismo, Sexismo e Desigualdade no Brasil." Revista de Estudos Avançados, vol. 13, no. 35, 1999, pp. 117-136.

Cathy O’Neil. Algoritmos de Destruição em Massa. 2021

Gonzalez, L.. "Racismo e Sexismo na Cultura Brasileira." Cadernos do Terceiro Mundo, vol. 46, 1984, pp. 27-31.

Kambeba, Márica. "Cotas Raciais e o Acesso dos Povos Indígenas ao Ensino Superior". Publicado na Revista Brasileira de Estudos Pedagógicos, vol. 97, no. 246, jan./abr. 2016, pp. 217-234.

Kayapó et al. “O acesso dos povos indígenas ao ensino superior.” Publicado na Revista Le Monde Diplomatique, jul.2022.

Silva, Sônia e Carvalho, Marília. "Cotas Raciais e o Acesso ao Ensino Superior pelos Indígenas Brasileiros". Publicado na Revista Brasileira de Política e Administcor de peleo da Educação, vol. 29, no. 1, jan./abr. 2013, pp. 135-149.
