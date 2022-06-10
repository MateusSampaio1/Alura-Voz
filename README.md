# Alura Voz - 1° Challenge de DataScience.

A Alura voz é uma empresa fictícia que atua no ramo das telecomunicações, e depois de identificar que estava tendo um problema com a taxa de rotatividade dos clientes, resolveu me contratar para atuar como cientista de dados, trabalhando em conjunto com a equipe de vendas. Vale evidenciar que esse problema de saída dos cliente é mensurado por uma métrica conhecida como Churn Rate, essa métrica irá mostrar basicamente a quantidade de pessoas que resolveram deixar de ser clientes em um determinado período de tempo.

Diante disso e, temendo maiores prejuízos na receita da empresa, fui informado de que teríamos algo em torno de um mês para analisarmos um conjunto de dados disponibilizados por eles, com o intuito de encontrar alternativas que venham a retardar e/ou diminuir ao máximo essa debandada dos clientes.

Como nosso prazo é de aproximadamente quatro semanas, acredito que seja interessante para manter a organização, dividir essa missão em etapas da seguinte forma:

# Tratamento dos dados.

Essa etapa tem o intuito de preparar os dados para garantir que as próximas etapas sejam realizadas sem maiores problemas. Para que isso seja factível, é necessário que consigamos compreender qual é o tipo de dados que estamos trabalhando e quais informações são possíveis de extrair deles, e com esse fim, também nos foi disponibilizado um dicionário dos dados.

**Dicionário de dados**
- **CustomerID**: número de identificação único de cada cliente
- **Churn**: se o cliente deixou ou não a empresa
- **Gender**: gênero (masculino e feminino)
- **SeniorCitizen**: informação sobre um cliente ter ou não idade igual ou maior que 65 anos
- **Partner**: se o cliente possui ou não um parceiro ou parceira
- **Dependents**: se o cliente possui ou não dependentes
- **Tenure**: meses de contrato do cliente
- **PhoneService**: assinatura de serviço telefônico
- **MultipleLines**: assisnatura de mais de uma linha de telefone
- **InternetService**: assinatura de um provedor internet
- **OnlineSecurity**: assinatura adicional de segurança online
- **OnlineBackup**: assinatura adicional de backup online
- **DeviceProtection**: assinatura adicional de proteção no dispositivo
- **TechSupport**: assinatura adicional de suporte técnico, menos tempo de espera
- **StreamingTV**: assinatura de TV a cabo
- **StreamingMovies**: assinatura de streaming de filmes
- **Contract**: tipo de contrato
- **PaperlessBilling**: se o cliente prefere receber online a fatura
- **PaymentMethod**: forma de pagamento
- **Charges.Monthly**: total de todos os serviços do cliente por mês
- **Charges.Total**: total gasto pelo cliente

Uma vez tratados, podemos seguir para a próxima etapa do processo.

# Análise exploratória.

Depois de conhecer e tratar os dados, devemos seguir adiante e ivestigarmos os dados com maior afinco. Essa análise será feita com o auxílio de técnicas estatíticas e por meio de visualizações gráficas.

Inicialmente procurou-se observar de que maneira a varíavel alvo (Evasão/Churn) se dividia e constatou-se que pouco mais de um quarto do total de clientes, registrados no conjunto de dados, resolveu deixar a Alura voz.

Posteriormente buscou-se verificar como era a relação da nossa variável alvo com as demais variáveis contidas no DataFrame. Após vislumbrar a interação entre a variável Cobrança_mensal e a varialvel alvo, achei que também seria relevante considerá-la nas demais visualizações.

Por fim, a última parte realizada nessa etapa foi a criação de uma matriz de correlação entre as variáveis. E foi possível identificar que não existia uma correlação muito forte entre a nossa variável target e as demais variáveis presentes no df.

# Modelagem dos dados.

O passo seguinte desse projeto, após todas as análises realizadas, é a etapa de modelagem dos dados. No entanto, como a natureza dos dados é, em sua maioria, qualitativa e do tipo object, será necessário realizar uma codficação no mesmo, para que consigamos utilizar modelos matemáticos e assim tentar prever potenciais clientes que poderiam vir a deixar a empresa.

As etapas para criação deste modelo de classificação consistem basicamente na identificação de quais são as variáveis relevantes para a aprendizagem do modelo, a separação destas variáveis entre as características ou features e os rótulos ou labels, a separação entre dados de treino e teste do modelo, o treinamento do modelo escolhido, a predição desse modelo e por fim a mensuração das métricas para esse modelo gerado.

Nesse trabalho em específico foram utilizados os modelo **Dummy** e **DecisionTree** como linha de base e os modelos **RandomForest** e **AdaBoost** na tentativa de encontrar métricas melhores que os anteriores. Como os dados possuiam um desbalanceamento entre as duas classes, decidi testar os modelos em três cenários diferentes, para só então decidir qual foi o melhor.

Os três cenários são contituídos por uma tentativa realizada mantendo o desbalanceamento das clases, uma utilizando o médodo de **OverSampling** como meio de equilibrar as variáveis e uma utilizando o método de **UnderSampling** também como o propósito de equilibrar as variáveis.

Todo o desenvolvimento desse projeto e sua conclusão podem ser vistos no Notebook [Desafio_alura](https://github.com/MateusSampaio1/Alura-Voz/blob/main/Notebooks/Desafio_Alura.ipynb).

#alura #alurachallengedatascience1



