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





Defini��es
Ambiente
O t�xi inteligente opera em uma cidade ideal, em forma de malha (similar � cidade de Nova Iorque), com ruas indo nas dire��es Norte-Sul e Leste-Oeste. Outros ve�culos certamente estar�o presentes na cidade, mas n�o haver� pedestres para se preocupar. A cada intersec��o h� um sem�foro que permite tr�fego tanto na dire��o Norte-Sul como na Leste-Oeste. A cidade segue as regras norte-americanas de tr�nsito:

No sinal verde, � permitido virar � esquerda se n�o houver nenhum tr�fego no sentido contr�rio fazendo curva � direita ou indo reto pela intersec��o.
No sinal vermelho, curva � direita � permitido se n�o houver nenhum tr�fego no sentido contr�rio se aproximando � sua esquerda, pela intersec��o. Para entender como conduzir corretamente o tr�fego de sentido contr�rio ao virar � esquerda, voc� pode assistir a este v�deo oficial sobre educa��o de condutores ou esta palestra animada.
Entradas e sa�das
Suponha que � atribu�do ao t�xi inteligente um plano de rota baseado na localiza��o inicial e no destino do passageiro. A rota � dividida a cada intersec��o em um ponto de navega��o, e voc� pode assumir que o t�xi inteligente, a qualquer instante, est� em alguma interse��o no mundo. Portanto, o pr�ximo ponto de navega��o para o destino, assumindo que o destino ainda n�o foi alcan�ado, � uma interse��o distante em uma dire��o (Norte, Sul, Leste ou Oeste). O t�xi inteligente tem apenas uma vis�o egoc�ntrica da interse��o, que �: ele pode determinar o estado do sem�foro adequado � sua dire��o, e se h� um ve�culo na interse��o para cada uma das dire��es contr�rias. Para cada a��o, o t�xi inteligente pode ficar ocioso na interse��o ou dirigir para a pr�xima interse��o � esquerda, � direita ou em frente. Por �ltimo, cada viagem tem um tempo para alcan�ar o destino que diminui a cada a��o tomada (os passageiros querem chegar a seu destino rapidamente). Se o tempo atribu�do torna-se zero antes de alcan�ar o destino, a viagem falhou.

Recompensas e objetivos
O t�xi inteligente recebe uma recompensa a cada viagem bem-sucedida e tamb�m recebe recompensas menores por cada a��o que ele executa com sucesso e obedecendo �s leis de tr�nsito. O t�xi inteligente recebe pequenas penalidade para cada a��o incorreta, e grandes penalidades para cada a��o que viole as leis de tr�nsito ou que cause um acidente com outro ve�culo. Baseado nas recompensas e penalidade que o t�xi inteligente recebe, a implementa��o do agente autocondutor dever� aprender um pol�tica �tima para dirigir nas estradas da cidade enquanto obedece �s leis de tr�nsito, evitando acidentes e alcan�ando o destino dos passageiros no tempo determinado.


Arquivos para envio
Quando estiver pronto para enviar seu projeto, re�na os arquivos abaixo e os comprima em um �nico arquivo para upload. Outra maneira seria fornec�-los em seu reposit�rio do GitHub, em uma pasta chamada smartcab, para facilitar o acesso.

Um arquivo Python agent.py com todo o c�digo implementado conforme as instru��es.
Uma pasta /logs/ com cinco registros produzidos pela sua simula��o e utilizados na an�lise.
O arquivo do Notebook smartcab.ipynb com todas as perguntas respondidas e todos os blocos de c�digo executados e exibindo a sa�da.
Um arquivo em HTML com o nome report.html exportado do notebook do projeto. Esse arquivo deve estar presente para que seu projeto seja avaliado.
Ap�s reunir esses arquivos e ler a rubrica do projeto, v� at� a p�gina de envio de projeto.