# Machine Learning Engineer Nanodegree
# Reinforcement Learning
## Project: Train a Smartcab How to Drive

### Install

This project requires **Python 2.7** with the [pygame](https://www.pygame.org/wiki/GettingStarted
) library installed

### Code

Template code is provided in the `smartcab/agent.py` python file. Additional supporting python code can be found in `smartcab/enviroment.py`, `smartcab/planner.py`, and `smartcab/simulator.py`. Supporting images for the graphical user interface can be found in the `images` folder. While some code has already been implemented to get you started, you will need to implement additional functionality for the `LearningAgent` class in `agent.py` when requested to successfully complete the project. 

### Run

In a terminal or command window, navigate to the top-level project directory `smartcab/` (that contains this README) and run one of the following commands:

```python smartcab/agent.py```  
```python -m smartcab.agent```

This will run the `agent.py` file and execute your agent code.





Definições
Ambiente
O táxi inteligente opera em uma cidade ideal, em forma de malha (similar à cidade de Nova Iorque), com ruas indo nas direções Norte-Sul e Leste-Oeste. Outros veículos certamente estarão presentes na cidade, mas não haverá pedestres para se preocupar. A cada intersecção há um semáforo que permite tráfego tanto na direção Norte-Sul como na Leste-Oeste. A cidade segue as regras norte-americanas de trânsito:

No sinal verde, é permitido virar à esquerda se não houver nenhum tráfego no sentido contrário fazendo curva à direita ou indo reto pela intersecção.
No sinal vermelho, curva à direita é permitido se não houver nenhum tráfego no sentido contrário se aproximando à sua esquerda, pela intersecção. Para entender como conduzir corretamente o tráfego de sentido contrário ao virar à esquerda, você pode assistir a este vídeo oficial sobre educação de condutores ou esta palestra animada.
Entradas e saídas
Suponha que é atribuído ao táxi inteligente um plano de rota baseado na localização inicial e no destino do passageiro. A rota é dividida a cada intersecção em um ponto de navegação, e você pode assumir que o táxi inteligente, a qualquer instante, está em alguma interseção no mundo. Portanto, o próximo ponto de navegação para o destino, assumindo que o destino ainda não foi alcançado, é uma interseção distante em uma direção (Norte, Sul, Leste ou Oeste). O táxi inteligente tem apenas uma visão egocêntrica da interseção, que é: ele pode determinar o estado do semáforo adequado à sua direção, e se há um veículo na interseção para cada uma das direções contrárias. Para cada ação, o táxi inteligente pode ficar ocioso na interseção ou dirigir para a próxima interseção à esquerda, à direita ou em frente. Por último, cada viagem tem um tempo para alcançar o destino que diminui a cada ação tomada (os passageiros querem chegar a seu destino rapidamente). Se o tempo atribuído torna-se zero antes de alcançar o destino, a viagem falhou.

Recompensas e objetivos
O táxi inteligente recebe uma recompensa a cada viagem bem-sucedida e também recebe recompensas menores por cada ação que ele executa com sucesso e obedecendo às leis de trânsito. O táxi inteligente recebe pequenas penalidade para cada ação incorreta, e grandes penalidades para cada ação que viole as leis de trânsito ou que cause um acidente com outro veículo. Baseado nas recompensas e penalidade que o táxi inteligente recebe, a implementação do agente autocondutor deverá aprender um política ótima para dirigir nas estradas da cidade enquanto obedece às leis de trânsito, evitando acidentes e alcançando o destino dos passageiros no tempo determinado.


Arquivos para envio
Quando estiver pronto para enviar seu projeto, reúna os arquivos abaixo e os comprima em um único arquivo para upload. Outra maneira seria fornecê-los em seu repositório do GitHub, em uma pasta chamada smartcab, para facilitar o acesso.

Um arquivo Python agent.py com todo o código implementado conforme as instruções.
Uma pasta /logs/ com cinco registros produzidos pela sua simulação e utilizados na análise.
O arquivo do Notebook smartcab.ipynb com todas as perguntas respondidas e todos os blocos de código executados e exibindo a saída.
Um arquivo em HTML com o nome report.html exportado do notebook do projeto. Esse arquivo deve estar presente para que seu projeto seja avaliado.
Após reunir esses arquivos e ler a rubrica do projeto, vá até a página de envio de projeto.