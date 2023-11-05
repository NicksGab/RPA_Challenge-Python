# RPA_Challenge em Python

## Onde foi utilizado?
O site que foi utilizado para este projeto se chama RPA Challenge (rpachallenge.com/), que é um desafio para os desenvolvedores RPA e tem como finalidade, além de ser desafiador, ser um teste de velocidade de seus RPAs.

## O que preciso para reproduzir?
Primeiramente precisamos ter em mente que este RPA foi desenvolvido em Python, então a primeira coisa que precisamos ter em nossa máquina instalado é o Python 3.11 ou superior.

Para isso iremos acessar o site de download do Python (https://www.python.org/downloads/) e concluir sua instalação normalmente.

Agora que já temos o Python instalado precisamos das bibliotecas usadas nesse projeto.
Presumindo que tenha alguma IDE instalada (VSCode, PyCharm) abra o terminal e digite os seguintes comandos.

**pip install selenium**
(Biblioteca de automação em Browser utilizada para a manipulação de DOM nesse projeto)

**pip install openpyxl**
(Biblioteca responsável pela leitura do arquivo .xlsx que contém os dados necessários para o desafio do site)

Pronto, seu ambiente está pronto para rodar seu projeto RPA.

Lembrando que esse RPA utiliza o WebDriver do Google Chrome na versão 118.0.
Caso o webdriver não funcione abra seu Chrome pela url "chrome://settings/help" anote a versão do seu Chrome.
Em seguida acesse "https://chromedriver.chromium.org/downloads" faça o download do arquivo .rar do WebDriver para sua versão e extraia na pasta do projeto substituindo o atual. 

Lembre-se que é importante manter o mesmo nome do arquivo anterior.

## Como reproduzir esse projeto?
A reprodução é bastante simples, presumindo que tenha todas as dependências devidamente instaladas em seu ambiente, vá na pasta do projeto em seu computador (Caso não tenha, faça o download por este repositório) e execute o arquivo "main.py".

Pronto, simples assim, logo em seguida verá seu Chrome abrir na página do RPA Challenge e toda execução automática do projeto.

## Desafios que enfrentei durante o processo.
Apesar de ser um projeto bem simples eu tinha o objetivo de concluir o desafio o mais rápido possível, o Python com Selenium por si só já era rápido.

Em minha primeira tentativa conclui o 100% na marca de 0.5 segundos no desafio, mas ainda estava lento pra mim.

Então pensei que possivelmente poderia se dar ao tempo que o Selenium leva para identificar os elementos HTML, e para mim uma ótima solução para isso seria executar o JavaScript na página, afinal se o objetivo é o DOM quem melhor para essa tarefa do que o próprio JavaScript?

E realmente foi uma ótima solução, de 0.5 caiu para 0.184 segundos, um salto enorme na minha opinião, mas ainda poderia melhorar, e já que o JavaScript tinha funcionado muito bem, a página não trocava de aba e não via nenhum update na página além do próprio Form, pensei comigo mesmo, por que não utilizar ainda mais o JavaScript? Extrair o máximo possível dele por meio do Selenium?

Foi exatamente o que tentei fazer, coletei todos os dados do arquivo .xlsx com python e os coloquei em um Array Multidimensional. A partir daí utilizei de puro JavaScript deixando-o com a responsabilidade de inserir os dados no campo correto e passar para a próxima página do formulário.

E não muito surpreendentemente mas de um modo extremamente empolgante essa solução deu muito certo! O que inicialmente para mim demorava 0.5s agora estava sendo finalizado em 0.053 segundos, quase 10x mais rápido! 


## Notas finais
Esse foi um projeto que criei depois que descobri esse site, pois fiquei extremamente animado com o desafio, afinal quem não gosta do sentimento de ser desafiado em algo que ama e colocar em prática tudo que vinha em mente?

Inicialmente tinha feito esse desafio em Power Automate puro, que levou 2 minutos para concluir toda execução, isso foi um tanto quanto... decepcionante na hora... mas bom, é claro que utiliza-lo para isso não daria certo, até porque não é realmente a finalidade dele. Mas consegui fazer esse tempo cair para 2 segundos usando o javaScript no Power Automate e isso foi muito empolgante! 

Mas bem isso é história pra outro repositório, se você leu até aqui, lhe agradeço imensamente pela atenção e espero que executando o projeto ou tentando otimizar ainda mais esse projeto você sinta a mesma sensação que eu senti, porque é simplesmente incrível!
