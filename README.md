
# LAB IA-900
#### PROJETO PARA CERTIFICAÇÃO MICROSOFT IA-900 DA DIO

![Azure](https://img.shields.io/badge/azure-%230072C6.svg?style=for-the-badge&logo=microsoftazure&logoColor=white)

## Dados sobre o projeto:

- Crie um novo repositório no github com um nome a sua preferência;
- Crie um modelo de previsão com seus devidos pontos de extremidade configurados;
- Escreva o passo a passo desse processo em um readme.md de como você chegou nessa etapa;
- Salve nesse repositório o readme.md e o arquivo .json de pontos de extremidade;
- Compartilhe conosco o link desse repositório através do botão 'entregar projeto'.


## Entrada teste:
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

  



