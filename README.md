# Analysis-of-Brazilian-Cancer-Data
This repository was created for the final project of a Data Science course at UNESP Botucatu. 
All data were extracted from: https://www.kaggle.com/joaopedromedeiros/cancer-data-brazil

O banco de dados escolhido foi fornecido pelo INCA (Instituto Nacional de Câncer) e adequado (alguns termos foram traduzidos e algumas strings substituídas) e disponibilizado por João Pedro Medeiros na plataforma Kaggle. Os dados mostram a realidade brasileira em termos de câncer, já que mostra dados relacionados diretamente ao paciente (como tipo de câncer, morfologia do mesmo e se o indíviduo faleceu ou não, e caso tenha, os dados também mostram se a causa da morte foi por câncer ou não) e dados relativos à localidade, como estado de origem do paciente e estado de tratamento. Além disso, os dados fornecem informações de gênero e idade dos pacientes, permitindo o cruzamento dessas informações com o tipo do câncer e a mortalidade. 

E quando encontramos esse conjunto de dados, nos chamou muita atenção essa amplitude de informações nos dados e boas ideias surgiram na discussão inicial. Com isso, nossa motivação para utilizar esse conjunto foi tentar obter maiores informações relacionadas à incidência de câncer e/ou suas morfologias em diferentes sub-populações e questões similares relacionadas à mortalidade em pessoas com câncer. 

Com isso, esperamos responder e observar a incidência de câncer por idade, realizar uma análise exploratória sobre as incidências de cada morfologia de câncer em relação aos gêneros masculino e feminino, também esperamos mostrar as morfologias mais letais e a distribuição dessas mortes por tipo de câncer. Também tentaremos observar a taxa de mortalidade por outras causas em indivíduos com câncer, além das frequências de mortes por câncer em diferentes centros de tratamento e sua análise exploratória. Por fim, realizaremos a implementação de machine learning, através das ferramentas de train, test e árvore de decisão para prever a mortalidade por câncer em função da idade do indivíduo. 

# Discussão dos Dados e Resultados: observando os resultados obtidos.
Inicialmente, na sessão "Incidência de câncer por idade", retiramos as idades acima de 122 anos e obtivemos um gráfico adequado, mostrando as maiores incidências da doença na faixa etária entre 60 e 70 anos. 

Em seguida, realizamos a análise exploratória para as incidências de diferentes morfologias nos indivíduos com diferentes gêneros. Tivemos que adicionar um terceiro gênero "IGNORADO" devido à falta de registro de alguns indivíduos no conjunto de dados. Isso ocorre devido à escolha do indivíduo preferir não informar seu gênero ou não ter ocorrido a coleta dessa informação ao admitir o paciente. Com isso, obtivemos que ADENOCARCINOMA é a morfologia mais comum no sexo masculino, CARCINOMA DUCTAL INFILTRANTE é a mais comum no sexo feminino e CARCINOMA BASOCELULAR no gênero ignorado (o que não é um dado estatísticamente significativo). 

Na sequência, fizemos a análise das cinco morfologias de câncer com maior incidência de morte, de acordo com os valores absolutos de morte por câncer em todos os centros de tratamento analisados, e a representação gráfica dessa análise, sendo NEOPLASIA MALIGNA a que mais causou mortes.

Desse modo, fizemos uma análise exploratória das causas de morte de pessoas diagnosticadas com câncer, obtendo que 6,6% delas falecem de causas diferentes do próprio câncer e 3,3% não possuem a causa da morte registrada. De forma complementar, foi feita e graficamente representada uma comparação entre a frequência de morte por câncer e alguma causa diferente nos diferentes centros de tratamento, juntamente com uma tabela mostrando as taxas de morte por câncer por centro de tratamento em pacientes com a doença.

Por fim, os dados foram separados em train e test, o score foi analisado e o modelo de árvore de decisão foi criado. 

  # Discussão sobre os problemas relacionados à árvore de decisões e modelo de predição: 
  Após o treino do modelo, verificamos o score pelo método de Hold-out. Ao analisar o score, foi possível constatar que o mesmo não se mostra satisfatório, uma vez que   esse valor está muito distante do ideal (65,5%). Mesmo após realizar um OverSampling ou um UnderSampling, não são encontrados resultados satisfatórios, o que nos       leva a concluir que o DataFrame não é bem estruturado para o modelo de predição, uma vez que apresenta uma pobreza de dados quantitativos, bem como um grande           desbalanceamento nos dados alvo. Desta forma, não foi encontrado um resultado adequado e, portanto, o modelo implementado não é confiável para predizer a causa da     morte dos pacientes diagnosticados com câncer. 
   



Vitor Melo Brandão
