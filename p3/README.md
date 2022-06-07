# Apresentação

O presente projeto foi originado no contexto das atividades da disciplina de pós-graduação [*Ciência e Visualização de Dados em Saúde*](https://ds4h.org), oferecida no primeiro semestre de 2022, na Unicamp.

> |Nome  | RA | Especialização|
> |--|--|--|
> | Rebeca Padovani Ederli  | 201482  | Ciência da Computação|


# Referência bibliográfica do artigo lido
> G. Scardoni, M. Petterlini, & C. Laudanna, "Analyzing biological network parameters with CentiScaPe." Bioinformatics 25(21), 2857–2859 (2009) https://doi.org/10.1093/bioinformatics/btp517.

# Resumo
> O artigo tem como objetivo mostrar como a ferramenta CentiScape é versátil e fácil de utilizar em bioinformática quando a análise de rede é baseada em centralidade, tanto para realização de cálculos e plot de resultados quanto para análise das saídas obtidas. Os autores demonstram a partir de experimentos realizados com dados de kino-phosphatome humano, que são um compilado de bancos de dados públicos (HPRD, BIND, DIP, IntAct, MINT e BioGRID). O artigo contém os resultados dos cáluclos de várias centralidades de rede, como Distância Média, Diâmetro, Grau, Tensão, Intermediação, Radialidade, Proximidade, Valor Centroide e Excentricidade, e análises biológicas provenientes dos resultados gerados.

# Breve descrição do experimento/análise do artigo que foi replicado
> Os dados fornecidos pelos autores são uma rede global de interatores de proteínas humanas, incluindo 11.120 nós e 84.776 interações não direcionadas únicas. Esses dados foram coletados das bases públicas HPRD, BIND, DIP, IntAct, MINT e BioGRID. Todas as reproduções realizadas foram feitas a partir da entrada de um subconjunto desta rede, que foi extraído e consiste apenas de interações conhecidas entre proteínas quinases e fosfatases humanas incluindo 543 nós e 3776 interações (os autores também realizam essa etapa, porém são obtidos 549 nós e 3844 interações da extração). 

> Por meio dessa entrada foram calculados os valores mínimo, máximo e médio de todas as centralidades computadas juntamente com o diâmetro e a distância média da rede para se ter uma visão geral das propriedades topológicas globais da rede kino-phosphatome. As centralidades computadas estão descritas a seguir:

> 1. Grau, ou *degree*, que permite uma avaliação imediata da relevância do nó. Proteínas com grau muito alto estão interagindo com várias outras proteínas.
> 2. Diâmetro, ou *diameter*, é a compacidade de uma rede biológica, pode ser interpretado como a facilidade de comunicação entre as proteínas;
> 3. Distância média, ou *distance average*, também representa a compacidade de uma rede biológica, embora os índices de centralidade devam ser calculados para apoiar essa indicação.
> 4. Excentricidade, ou *eccentricity*, pode ser interpretada como a facilidade de uma proteína ser alcançada por todas as outras proteínas da rede;
> 5. Proximidade, ou *closeness*, é probabilidade de uma proteína ser relevante para várias outras proteínas, mas com a possibilidade de ser irrelevante para algumas outras proteínas. Ou seja, uma proteína com alta proximidade, comparada à média de proximidade da rede, será facilmente central para outras proteínas;
> 6. Radialidade, ou *radiality*, também pode ser interpretada como a probabilidade de uma proteína ser relevante para várias outras proteínas, mas com a possibilidade de ser irrelevante para algumas outras proteínas;
> 7. Centralidade, ou *centrality*, sigifica a probabilidade de uma proteína ser capaz de organizar agrupamentos de proteínas. Uma proteína com alto valor de centroide, possivelmente estará envolvida na coordenação da atividade de outras proteínas altamente conectadas;
> 8. Estresse, ou *stress*, pode indicar a relevância de uma proteína como capaz de manter nós comunicantes juntos;
> 9. Intermediação, ou *Betweenness*, indica a capacidade de uma proteína de trazer em comunicação proteínas distantes.

> As outras reproduções realizadas estão listadas a seguir:

> 1. Cálculo de centralidades de cada nó;
> 2. 'plot by centrality', plotando grau sobre grau;
> 3. plot para análise de quantidade de nós com graus acima da média;
> 4. plot das centralidades da proteína quinase MAPK1;
> 5. plot das centralidades da proteína fosfatase PTPN1;
> 6. plot de centroide sobre centroide;
> 7. plot de grau sobre o centroide;
> 8. filtragem de nós com todos os valores de centralidade acima da média (geração de nova sub-rede).

## Dados usados como entrada
Dataset | Endereço na Web | Resumo descritivo
----- | ----- | -----
 GLOBAL-HGNC | https://academic.oup.com/bioinformatics/article/25/21/2857/227713#supplementary-data | Uma rede bipartida de proteínas quinases humanas conhecidas e as fosfatases com as quais elas interagem. É um compilado de conjuntos de dados públicos (HPRD, BIND, DIP, IntAct, MINT e BioGRID) de interatividade de proteínas humanas. O tipo de aresta é Vinculativo e os nós são Proteínas quinases e fosfatases (bipartido, não direcionado, não ponderado).

# Método
> Método usado para a análise -- adaptações feitas, ferramentas utilizadas, abordagens de análise adotadas e respectivos algoritmos.
> Etapas do processo reproduzido.

# Resultados
> Apresente os resultados obtidos pela sua adaptação.
> Confronte os seus resultados com aqueles do artigo.
> Esta seção opcionalmente pode ser apresentada em conjunto com o método.
