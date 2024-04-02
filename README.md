# Trabalhando com Machine Learning na Prática no Azure ML


## 1: Criando recurso do Azure Machine Learning

##### Primeiro precisei criar um recurso de Machine Learning. Para isso, cliquei em "Criar recurso" e depois pesquisei por Azure Machine Learning no marketplace. Após encontrar o recurso, crie ele.


## 2: Configurando o recurso do Azure Machine Learning

##### Na aba de Noções básica, Detalhes do recurso, é informei a assinatura para cobrança no campo Assinatura e depois informei o Grupo de recursos que vai englobar o recurso que será criado.

##### Após, em Detalhes da área de trabalho, é informei os detalhes do workspace que será criado. Como foi um laboratório, as configurações foram mínimas. Por fim, criei o recurso clicando em Consultar + criar. Após a validação ser aprovada, cliquei em "Criar".

## 3: Criando o modelo

##### No estúdio, na página do workspace criado anteriormente, acessei a opção do menu ML automatizado e na página aberto, cliquei em "Novo trabalho de ML automatizado".

##### Em "Configurações básicas", preenchi os campos "Nome do trabalho", "Novo nome do experimento" e "Descrição". Após cliquei em "Avançar".

##### No passo "Tipo de tarefa e dados", selecionei o tipo de tarefa como Regressão e em seguida, em "Selecionar dados", cliquei em "Criar". No modal aberto, em "Tipos de dados", preenchi os campos "Nome", "Descrição" e escolhi "Tipo" como Tabular. Cliquei em "Avançar" e no passo "Fonte de dados", escolhi "De arquivos da Web" e cliquei em avançar novamente.

##### No passo "URL da Web", informei a URL https://aka.ms/bike-rentals do conjunto de dados. Algumas vezes tive problemas com a validação dos dados, então usei essa URL: https://raw.githubusercontent.com/MicrosoftLearning/mslearn-ai-fundamentals/main/data/ml/daily-bike-share.csv. No passo "Configurações", preenchi as configurações do conjunto e após avançar para "Esquema", verifiquei os tipos de dados. Finalmente, ao avançar, verifiquei as configurações criadas para o ativo de dados e cliquei em criar.

##### Em "Configurações de tarefas", escolhi o conjunto de dados importado. Após, em "Coluna de destino" escolhi a coluna rentals como target.

##### Nos campos de "Limite", preenchi com os valores e marquei "Habilitar encerramento antecipado".

##### Em "Validar e testar", em "Tipo de validação" escolhi "Divisão de validação de treinamento".

##### Após avançar e examinar as configurações do trabalho, cliquei em "Enviar trabalho de treinamento".

##### Após finalizar o trabalho de treinamento, precisei criar o modelo. Para isso, acessei a página do trabalho realizado e cliquei em "Modelo de registro". Deixei as opções padrões para "Selecionar saída". Em "Configurações do modelo", somente preenchi o nome e a versão. Após isso, cliquei em criar o modelo.

#####  Po fim, o modelo fica acessível na opção de menu "Modelo".

## 5: Teste do modelo

##### Na página do modelo, acessei a aba "Pontos de extremidade" e em seguida cliquei em "Implantar". Porém, por algum motivo o botão não funcionou. Então, para criar o ponto de extremidade para esse modelo, acessei "Pontos de extremidade" no menu lateral, e cliquei em "Criar". Em seguida marquei o modelo e deixei todos os campos seguintes como os valores padrões, exceto "Contagem de instâncias" que deixei como 1. Então cliquei em "Implantar".


##### Logo após a implantação, que demora bastante, acessei a aba "Testar" do ponto de extremidade criado para o meu modelo.

##### Para o teste, utilizei o json