
# Explorando o Machine Learning do Azure

Usando o recurso de aprendizado de máquina automatizado do Azure Machine Learning para treinar e avaliar um modelo de aprendizado de máquina.

## 🛠 Habilidades
Machine Learning, Azure, Endpoints...

## Configurando o aprendizado de máquina automatizado para treinar um modelo

O aprendizado de máquina automatizado permite experimentar diversos algoritmos e parâmetros para treinar diversos modelos e identificar o melhor para os dados. 

Utilizei um conjunto de dados com detalhes históricos de aluguel de bicicletas para treinar um modelo que prevê o número de aluguéis de bicicletas esperados em um determinado dia, com base em características sazonais e meteorológicas.

### Passo a Passo resumido

- Criar Workspace de Machine Learning
- Gerar um Automated ML
- Upload do arquivo csv no Blob Storage
- Criar uma task de regressão
- Gerar o deploy do modelo
- Testar uma previsão com o enpoint do modelo

## Screenshots
Upload dos dados
![Upload dos dados](https://i.ibb.co/9HzjPF17/Captura-de-Tela-2025-04-11-a-s-18-13-50.png)

Criando a task de regressão
![Criando a task de regressão](https://i.ibb.co/ZRmnHNpm/Captura-de-Tela-2025-04-11-a-s-18-17-13.png)

Modelo concluído
![Modelo concluído](https://i.ibb.co/HfGQpNDx/Captura-de-Tela-2025-04-11-a-s-18-31-35.png)

Criando o endpoint do modelo
![Criando o endpoint do modelo](https://i.ibb.co/XZyBtsym/Captura-de-Tela-2025-04-11-a-s-18-36-44.png)



## Microsoft Learn

[Documentação Lab 01 - Automated Machine Learning](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/01-machine-learning.html)


## Aprendizados

É muito bom ver na prática os conceitos do Machine Learning, ainda mais, poder utilizar o Azure para isso. Inicialmente tive alguns problemas com o Azure, configurando as máquinas e tentando executar o laboratório dentro dos resources gratis e sim, é possivel.

O resultado final, um json contendo um array com apenas uma posição pode não parecer muito significativo se estiver fora do contexto, mas muita coisa aconteceu para chegarmos nesse resultado, e já foi possivel pensar em algumas possibilidades e não vejo a hora de integrar um outro automated ML em alguma plataforma.

## Feedback

Se você tiver algum feedback, por favor me deixe saber por meio de thiagodebia@gmail.com


## FAQ

#### O que fazer ao receber o erro de resource não registrado ao criar o endpoint do modelo?

Fiz alguns testes seguindo a documentção do Azure, resultando sempre no mesmo erro. Como estou usando o bonus de avaliação da Azure, mudei a configuração dos servidores, sobrando assim, máquinas para criar o endpoint, e ai sim funcionou.

#### O que fazer se não conseguir configurar o datasource com a url da documentação?

A url contendo o arquivo da documentação aponta para um .zip com isso, ao configurar o datasource o azure não consegue mapear as colunas. Fiz o download do arquivo e fiz o upload apenas do csv, mudando o tipo de MLTable para tabulate. O Azure reconheceu o csv e configurou automaticamente a primeira linha e as colunas.




## Demonstração
Métricas do modelo
![Métricas do modelo](https://i.ibb.co/W4xFSGF6/Captura-de-Tela-2025-04-12-a-s-12-54-09.png)

Testando o modelo
![Testando o modelo](https://i.ibb.co/v4ZpptPZ/Captura-de-Tela-2025-04-12-a-s-13-10-31.png)



## Resultado

Json Output

```bash
[ 
  309.194476306583 
]
```
    
