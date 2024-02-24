
# LAB IA-900
#### PROJETO PARA CERTIFICAÇÃO MICROSOFT IA-900 DA DIO

![Azure](https://img.shields.io/badge/azure-%230072C6.svg?style=for-the-badge&logo=microsoftazure&logoColor=white)

> ## Dados sobre o projeto:

- _Crie um novo repositório no github com um nome a sua preferência;_
- _Crie um modelo de previsão com seus devidos pontos de extremidade configurados;_
- _Escreva o passo a passo desse processo em um readme.md de como você chegou nessa etapa;_
- _Salve nesse repositório o readme.md e o arquivo .json de pontos de extremidade;_
- _Compartilhe conosco o link desse repositório através do botão 'entregar projeto'._

##
### Segundo a documentação devemos seguir essa sequência:
##

> ## Criar um espaço de trabalho do Aprendizado de Máquina do Azure
  1. Acesso ao portal da Azure <pre>https://portal.azure.com</pre>
  2. Criar um Grupo (Create a resource) seguindo os passos:
  3. Em Create a resource no menu lateral aparecera um Dashboard e seu campo de busca então digite (Azure Machine Learning) depois clicar em (Create)
     
     ![image](https://github.com/vinicius-campelo/lab-ia900/assets/74797865/7d21adca-3e5e-4f55-8455-b16ee5968d1a)

      - Subscription (deixa como esta) pois essa e a assinatura da plataforma;
      - Resource group (se não existir) create new (nome de grupo desejado sem espaços);
      - Workspace details
        - Name (nome exclusivo);
        - region (Selecione a região geográfica mais próxima);
        - Storage account (deixa como esta) pois ele foi preenchido ao informar o Name);
        - Key vault (deixa como esta) pois ele foi preenchido ao informar o Name);
        - Application insights (deixa como esta) pois ele foi preenchido ao informar o Name);
        - Os outros links (Networking, Encryption, Identity, Tags, Review + create) não e necessário preencher;
        - Após o procedimento selecione o botão (Revisar + criar) ou (Review + create) esse processo demora alguns minutos.

 
  4. Selecione Iniciar estúdio (ou abra uma nova guia do navegador e navegue até <pre>https://ml.azure.com</pre> Feche todas as mensagens exibidas.
  5. No estúdio de Aprendizado de Máquina do Azure, você deve ver seu espaço de trabalho recém-criado. Caso contrário, selecione Todos os espaços de trabalho no menu à esquerda e, em seguida, selecione o espaço de trabalho que você acabou de criar.

     ![image](https://github.com/vinicius-campelo/lab-ia900/assets/74797865/4f417994-716a-4e74-8ccc-669216b545cb)





> ## Usar o aprendizado de máquina automatizado para treinar um modelo
  No estúdio de Aprendizado de Máquina do Azure, exiba a página ML automatizada (em Criação).

  Crie um novo trabalho de ML automatizado com as seguintes configurações, usando Avançar conforme necessário para progredir pela interface do usuário:

  #### Configurações básicas:
  - Nome do trabalho: mslearn-bike-automl
  - Novo nome do experimento: mslearn-bike-rental
  - Descrição: Aprendizado de máquina automatizado para previsão de aluguel de bicicletas
  - Tags: nenhuma

  #### Tipo de tarefa & data:

  - Selecionar tipo de tarefa: Regressão
  - Selecionar conjunto de dados: crie um novo conjunto de dados com as seguintes configurações:
  - Tipo de dados:
  - Nome: bike-rentals
  - Descrição: Dados históricos de aluguer de bicicletas
  - Tipo: Tabular
      - Fonte de dados:
      - Selecionar de arquivos da Web
  - URL da Web:
      - URL da Web: https://aka.ms/bike-rentals
      - Ignorar validação de dados: não selecione
  - Configurações:
      - Formato de arquivo: Delimitado
      - Delimitador: Vírgula
      - Codificação: UTF-8
      - Cabeçalhos de coluna: Somente o primeiro arquivo tem cabeçalhos
      - Pular linhas: Nenhum
      - O conjunto de dados contém dados de várias linhas: não selecione
  - Esquema:
      - Incluir todas as colunas diferentes de Caminho
      - Revisar os tipos detectados automaticamente
    Selecione Criar. Depois que o conjunto de dados for criado, selecione o conjunto de dados de aluguel de bicicletas para continuar a enviar o trabalho de ML automatizado.

  #### Configurações da tarefa:

  - Tipo de tarefa: Regressão
  - Conjunto de dados: aluguel de bicicletas
  - Coluna de destino: Aluguéis (inteiro)
  - Definições de configuração adicionais:
    - Métrica primária: Erro quadrático médio da raiz normalizada
    - Explicar melhor modelo: Não selecionado
    - Use todos os modelos suportados: Nãoselecionado. Você restringirá o trabalho para tentar apenas alguns algoritmos específicos.
    - Modelos permitidos: selecione apenas RandomForest e LightGBM — normalmente você gostaria de tentar o maior número possível, mas cada modelo adicionado aumenta o tempo necessário     para executar o trabalho.
  - Limites: expanda esta seção
     - Máximo de tentativas: 3
     - Máximo de tentativas simultâneas: 3
     - Nós máximos: 3
     - Limiar de pontuação métrica: 0,085 (de modo que, se um modelo atingir uma pontuação métrica quadrática média normalizada de 0,085 ou menos, o trabalho termina.)
     - Tempo limite: 15
     - Tempo limite de iteração: 15
     - Habilitar rescisão antecipada: Selecionado
  - Validação e teste:
     - Tipo de validação: Divisão de validação de trem
     - Porcentagem de dados de validação: 10
     - Conjunto de dados de teste: Nenhum
     
  - Computação:
     - Selecione o tipo de computação: Serverless
     - Tipo de máquina virtual: CPU
     - Camada de máquina virtual: Dedicado
     - Tamanho da máquina virtual: Standard_DS3_V2*
     - Número de instâncias: 1
  * Se sua assinatura restringir os tamanhos de VM disponíveis para você, escolha qualquer tamanho disponível.

  3. Envie o trabalho de treinamento. Ele começa automaticamente.

  4. Aguarde a conclusão do trabalho. Pode demorar um pouco – agora pode ser um bom momento para uma pausa para o café!
   ##
   ![image](https://github.com/vinicius-campelo/lab-ia900/assets/74797865/7b725ca2-4d43-40e8-a29f-18945a0b7330)
   ##
   ![image](https://github.com/vinicius-campelo/lab-ia900/assets/74797865/cd448180-d599-4a77-948f-3cbe99d8539f)
   ##
   ![image](https://github.com/vinicius-campelo/lab-ia900/assets/74797865/e031f2e7-0816-49c8-a855-6f8c9364597f)
   ##
   ![image](https://github.com/vinicius-campelo/lab-ia900/assets/74797865/1b131ce1-7431-49b3-bc48-42f384393bd2)
   ##
   ![image](https://github.com/vinicius-campelo/lab-ia900/assets/74797865/4ada8fe1-a626-4ca7-86cd-5a3d5c252987)
   ##
   ![image](https://github.com/vinicius-campelo/lab-ia900/assets/74797865/d258d996-186f-4023-b905-c8bf363091b1)
   ##
   ![image](https://github.com/vinicius-campelo/lab-ia900/assets/74797865/5d4a65f5-c66f-40b1-944c-2e9953896d73)
   ##
   ![image](https://github.com/vinicius-campelo/lab-ia900/assets/74797865/45863a01-5f8d-47d5-90fa-1f4798426feb)
   ##
   ![image](https://github.com/vinicius-campelo/lab-ia900/assets/74797865/6283fdf9-8b02-4d12-87b4-ff8d75bf8398)
   ##
   ![image](https://github.com/vinicius-campelo/lab-ia900/assets/74797865/7ffc2711-8348-494f-b026-bcafa5a93b32)
   ##
   Na mesma tela descendo
   ![image](https://github.com/vinicius-campelo/lab-ia900/assets/74797865/c4c67449-b5a7-4d06-962a-ee863c18a9cf)
   ##
   ![image](https://github.com/vinicius-campelo/lab-ia900/assets/74797865/60ece7e0-ed8f-4703-838c-4f7ae82a6c61)
   ##
   ![image](https://github.com/vinicius-campelo/lab-ia900/assets/74797865/10e4cf79-98ef-4ae3-9b6d-8d847c80f71c)
   ##
   ![image](https://github.com/vinicius-campelo/lab-ia900/assets/74797865/a08eedeb-52b3-44f5-b440-621491bb365a)
   ##
   ![image](https://github.com/vinicius-campelo/lab-ia900/assets/74797865/44d3475d-6f72-469b-859a-377977f8b238)
   ##
   ![image](https://github.com/vinicius-campelo/lab-ia900/assets/74797865/c4c10d2a-3e87-45c2-8c98-c04f73dd8909)
   ##
  2. Selecione o texto em Nome do algoritmo para o melhor modelo para exibir seus detalhes.

  3. Selecione a guia Métricas e selecione os gráficos de resíduos e predicted_true se ainda não estiverem selecionados.

     Analise os gráficos que mostram o desempenho do modelo. O gráfico de resíduos mostra os resíduos (as diferenças entre os valores previstos e reais) como um histograma. O gráfico     predicted_true compara os valores previstos com os valores verdadeiros.
  ![image](https://github.com/vinicius-campelo/lab-ia900/assets/74797865/416fe842-e860-41f3-94f0-a3900e52d3b6)


> ## Implantar e testar o modelo

  1. Na guia Modelo para obter o melhor modelo treinado pelo seu trabalho de aprendizado de máquina automatizado, selecione Implantar e usar a opção Serviço Web para implantar o modelo      com as seguintes configurações:
        - Nome: predict-rentals
        - Descrição: Prever aluguéis de ciclos
        - Tipo de computação: Instância de Contêiner do Azure
        - Habilitar autenticação: Selecionado
  ##
  ![image](https://github.com/vinicius-campelo/lab-ia900/assets/74797865/81b18663-47ce-45fb-8717-9a5c65a867dc)
  ##
  ![image](https://github.com/vinicius-campelo/lab-ia900/assets/74797865/8386f29c-2291-4c10-8235-2f7b70a4cd70)


  2. Aguarde o início da implantação - isso pode levar alguns segundos. O status de implantação para o ponto de extremidade de aluguel de previsão será indicado na parte principal da 
     página como Em execução.
  3. Aguarde até que o status Implantar seja alterado para Bem-sucedido. Isso pode levar de 5 a 10 minutos.
  ##
  ![image](https://github.com/vinicius-campelo/lab-ia900/assets/74797865/b21492a8-c445-4b97-9306-187c42c2da14)




> ## Testar o serviço implantado
  1. No estúdio do Aprendizado de Máquina do Azure, no menu à esquerda, selecione Pontos de extremidade e abra o ponto de extremidade em tempo real de aluguéis de previsão.

  2. Na página de ponto de extremidade em tempo real de aluguéis de previsão, exiba a guia Teste.
    ##
    ![image](https://github.com/vinicius-campelo/lab-ia900/assets/74797865/fa3962b1-7f4d-4bd8-b55f-f6b27d6a67fe)

  4. No painel Dados de entrada para testar o ponto de extremidade, substitua o modelo JSON pelos seguintes dados de entrada:
     ##
     ![image](https://github.com/vinicius-campelo/lab-ia900/assets/74797865/210d34d7-df2d-4123-9f6a-65d38bd07a6b)


   ## Entrada teste e saida:
   > [!IMPORTANT]
   Testando ponto de extremidade parametros

  ```json
   {
     "Inputs": { 
       "data": [
         {
           "day": 1,
           "mnth": 1,   
           "year": 2022,
           "season": 2,
           "holiday": 0,
           "weekday": 1,
           "workingday": 1,
           "weathersit": 2, 
           "temp": 0.3, 
           "atemp": 0.3,
           "hum": 0.3,
           "windspeed": 0.3 
         }
       ]    
     },   
     "GlobalParameters": 1.0
   }
  ```
  ## 
  Resultado do teste
  
  ```json
   {
     "Results": [
       444.27799000000000
     ]
   }
  ```

> ## Limpeza

  1. No estúdio do Aprendizado de Máquina do Azure, na guia Pontos de extremidade, selecione o ponto de extremidade de aluguel de previsão. Em seguida, selecione Excluir e confirme que      deseja excluir o ponto de extremidade.

  2. A exclusão da computação garante que sua assinatura não será cobrada por recursos de computação. No entanto, será cobrado um pequeno valor pelo armazenamento de dados, desde que o      espaço de trabalho do Aprendizado de Máquina do Azure exista em sua assinatura. Se você tiver terminado de explorar o Aprendizado de Máquina do Azure, poderá excluir o espaço de 
     trabalho do Aprendizado de Máquina do Azure e os recursos associados.

  Para excluir seu espaço de trabalho:

  1. No portal do Azure, na página Grupos de recursos, abra o grupo de recursos especificado ao criar seu espaço de trabalho do Aprendizado de Máquina do Azure.
  2. Clique em Excluir grupo de recursos, digite o nome do grupo de recursos para confirmar que deseja excluí-lo e selecione Excluir.



  
## Referência:

 - [Explore Azure AI Services](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/02-content-safety.html)
 - [Explore Automated Machine Learning in Azure Machine Learning](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/01-machine-learning.html)
 - [SprintAI900: Azure Machine Learning](https://www.youtube.com/watch?v=PzdYcJ1pRPI&t=18s)
 - [IA para Quem não é Cientista de Dados](https://www.youtube.com/watch?v=a4_7HdJ1cys&t=1918s)

  



