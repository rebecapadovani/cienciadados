# Apresentação

O presente projeto foi originado no contexto das atividades da disciplina de pós-graduação [*Ciência e Visualização de Dados em Saúde*](https://ds4h.org), oferecida no primeiro semestre de 2022, na Unicamp.

> |Nome  | RA | Especialização|
> |--|--|--|
> | Rebeca Padovani Ederli  | 201482  | Ciência da Computação|


# Referência bibliográfica do artigo lido
> Giovanni Scardoni, Michele Petterlini, Carlo Laudanna, Analyzing biologic network parameters with CentiScaPe, Bioinformatics , Volume 25, Issue 21, 1 November 2009, Pages 2857–2859, https://doi.org/10.1093/bioinformatics/btp517.

# Resumo
> O artigo tem como objetivo mostrar como a ferramenta CentiScape é versátil e fácil de utilizar em bioinformática quando a análise de rede é baseada em centralidade, tanto para realização de cálculos e plot de resultados quanto para análise das saídas obtidas. Os autores demonstram a partir de experimentos realizados com dados de kino-phosphatome humano, que são um compilado de bancos de dados públicos (HPRD, BIND, DIP, IntAct, MINT e BioGRID). O artigo contém os resultados dos cáluclos de várias centralidades de rede, como Distância Média, Diâmetro, Grau, Tensão, Intermediação, Radialidade, Proximidade, Valor Centroide e Excentricidade, e análises biológicas provenientes dos resultados gerados.

# Breve descrição do experimento/análise do artigo que foi replicado
> Os dados fornecidos pelos autores são uma rede global de interatores de proteínas humanas, incluindo 11.120 nós e 84.776 interações não direcionadas únicas. Esses dados foram coletados das bases públicas HPRD, BIND, DIP, IntAct, MINT e BioGRID. Todas as reproduções realizadas foram feitas a partir da entrada de um subconjunto desta rede, que foi extraído e consiste apenas de interações conhecidas entre proteínas quinases e fosfatases humanas incluindo 543 nós e 3776 interações (os autores também realizam essa etapa, porém são obtidos 549 nós e 3844 interações da extração). 

Por meio dessa entrada foram calculados os valores mínimo, máximo e médio de todas as centralidades computadas juntamente com o diâmetro e a distância média da rede para se ter uma visão geral das propriedades topológicas globais da rede kino-phosphatome. As centralidades computadas são:

1.
2.
3.
4.
5.
6.
7.
8.
9.
As outras reproduções realizadas são listadas a seguir:

1. Cálculo de centralidades de cada nó;
2. 'plot by centrality', plotando grau sobre grau;
3. plot para análise de quantidade de nós com graus acima da média;
4. plot das centralidades da proteína quinase MAPK1;
5. plot das centralidades da proteína fosfatase PTPN1;
6. plot de centroide sobre centroide;
7. plot de grau sobre o centroide;
8. filtragem de nós com todos os valores de centralidade acima da média (geração de nova sub-rede).

## Dados usados como entrada
Dataset | Endereço na Web | Resumo descritivo
----- | ----- | -----
Título do Dataset | http://base1.org/ | Breve resumo (duas ou três linhas) sobre o dataset.

# Método
> Método usado para a análise -- adaptações feitas, ferramentas utilizadas, abordagens de análise adotadas e respectivos algoritmos.
> Etapas do processo reproduzido.

# Resultados
> Apresente os resultados obtidos pela sua adaptação.
> Confronte os seus resultados com aqueles do artigo.
> Esta seção opcionalmente pode ser apresentada em conjunto com o método.
