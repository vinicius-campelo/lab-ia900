
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


> ## Implantar e testar o modelo
> ## Testar o serviço implantado
> ## Limpeza


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

  
## Referência:

 - [Explore Azure AI Services](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/02-content-safety.html)
 - [Explore Automated Machine Learning in Azure Machine Learning](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/01-machine-learning.html)
 - [SprintAI900: Azure Machine Learning](https://www.youtube.com/watch?v=PzdYcJ1pRPI&t=18s)
 - [IA para Quem não é Cientista de Dados](https://www.youtube.com/watch?v=a4_7HdJ1cys&t=1918s)

  



