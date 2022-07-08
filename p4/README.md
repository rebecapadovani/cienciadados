# Projeto 4 – Classificação de lesões de substância branca no Lúpus
# Project 4 - Classification of white matter lesions in Lupus.

# Apresentação

O presente projeto foi originado no contexto das atividades da disciplina de pós-graduação [*Ciência e Visualização de Dados em Saúde*](https://ds4h.org), oferecida no primeiro semestre de 2022, na Unicamp.

> |Nome  | RA | Especialização|
> |--|--|--|
> | Rebeca Padovani Ederli | 201482  | Ciência da Computação|


# Introdução
> O objetivo principal do projeto é diferenciar lesões isquêmicas e desmielinizantes por meio de um classificador e, assim, identificar qual a etiologia mais provável das lesões presentes em pacientes de Lúpus Eritematoso Sistêmico (SLE).
> A etiologia da lesão é importante para o tratamento adequado e um método que distingue lesões desmielinizantes de isquêmicas e pode ser usado para caracterizar lesões de etiologia desconhecida. As estiologias são isquêmica e desmielinizante e as lesões da substância branca apresentam-se brilhante em T2w e FLAIR (hiperintensidades de substância branca).

## Ferramentas
> * Linguagem de programação Python;
> * Jupyter Notebook;
> * Google Colaboratory.

## Preparo e uso dos dados
> Os dados utilizados correspondem aos dados separados para a tarefa de Deep Learning ("Data_P4_DL"). Não foram utilizadas as máscaras para nenhum tipo de processo neste trabalho.

> * Todas as imagens foram redimensionadas para 170x170.
> * *Data augmentation*: foi aplicada a técnica de *data augmentation* nas imagens dos conjuntos de treinamento e validação. As transformações realizadas com *data augmentation* incluem:
> 1. Flip horizontal: as inversões de imagem são realizadas ao longo de um eixo de simetria. Para aprimoramento de imagens médicas, elas podem ser realizadas tanto na vertical quanto na horizontal;
> 2. Flip Vertical;
> 3. Rotação em 45 graus;
> 4. Rotação em 90 graus;
> 5. Brilho variando entre 0.5 e 1.2: quanto menor o valor, mais escura é a imagem;
> 6. Contraste variando entre 0.8 e 1.2: quando o contraste é aumentado, o número de pixels brancos e pretos na imagem também aumenta;
> 7. Afiação (ou *sharpening*), com fator 2: transformação que aumenta o contraste nas bordas da imagem, dando uma aparência mais nítida.

> As transformações para gerar novos dados foram realizadas de forma aleatória.
> Algumas imagens geradas com *data augmentation* no conjunto de treinamento podem ser observadas na Figura 1.

> ![Figura 1](assets/data-augmentation.png)
 
> Figura 1 - Algumas imagens geradas com *data augmentation* por meio do conjunto de treinamento.

# Metodologia
> Foi utilizado um classificador baseado em Deep Learning, a arquitetura ResNet-18. A ResNet-18 possui 18 camadas de profundidade. É possível carregar uma versão pré-treinada da rede treinada em mais de um milhão de imagens do banco de dados ImageNet [1]. A rede pré-treinada pode classificar imagens em 1000 categorias de objetos e muitos animais. Como resultado, a rede aprendeu representações ricas de recursos para uma ampla variedade de imagens. Por esse motivo, essa arquitetura foi escolhida neste trabalho. Foi utilizada a versão não pré-treinada desta rede. Uma camada NN linear foi adicionada à arquitetura com 2 neurônios de saída.
> Os dados foram dividos em aproximadamente 90% para o conjunto de treinamento e 10% para o conjunto de teste. O conjunto de validação correspode a aproximadamente 26% do conjunto de treinamento. Resultando em 507 imagens para treinamento, 182 para validação e 78 para teste.
> Os parâmetros do modelo foram adotados com base na atividade realizada em aula: *taxa de aprendizado = 0.00005* e otimizador SGD. *Cross Entropy Loss* foi utilizada para calcular a perda de entropia cruzada entre a entrada e o alvo.
> As métricas calculadas a partir dos resultados foram especificidade, sensibilidade, acurácia e matriz de confusão. Os testes foram realizados no conjunto de teste estabelecido e no conjunto de teste apresentado na atividade em aula para verificar como o modelo está atuando. Em seguida, foram realizadas as predições no conjunto SLE.

* resultados do treinamento do classificador usando tabelas e gráficos
>
> Justificar as escolhas.
> Esta parte do relatório pode ser copiada da Atividade 11, caso o grupo opte por usar o SVM já treinado.

# Resultados Obtidos e Discussão
> Esta seção deve apresentar o resultado de predição das lesões de LES usando o classificador treinado. Também deve tentar explicar quais os atributos relevantes usados na classificação obtida
> * apresente os resultados de forma quantitativa e qualitativa
> * tenha em mente que quem irá ler o relatório é uma equipe multidisciplinar. Descreva questões técnicas, mas também a intuição por trás delas.

# Conclusão
> Destacar as principais conclusões obtidas no desenvolvimento do projeto.
>
> Destacar os principais desafios enfrentados.
>
> Principais lições aprendidas.
>
> Trabalhos Futuros:
> * o que poderia ser melhorado se houvesse mais tempo?

# Referências Bibliográficas
> Lista de artigos, links e referências bibliográficas (se houver).
>
> Fiquem à vontade para escolher o padrão de referenciamento preferido pelo grupo.
> [1] ImageNet . http://www.image-net.org