# MPE -  Métrica do próprio esforço

Já se perguntou o tamanho do seu esforço relacionado a testes manuais ou automatizados? Já se perguntou quanto tempo você leva para realizar uma tarefa? Pois bem, esse é um exercício que te faz ter pequenos objetivos, desde objetivos diários até anuais, que carinhosamente chamei de MPE (Métrica do próprio esforço), ou seja, começar a medir o próprio trabalho, como por exemplo, começar a fazer o track de quantas tarefas são automatizadas por dia/semana e para começar a colher isso, será necessário haver planejamento, quebra de task, etc., e podemos usar por exemplo uma medida básica chamada ***LEAD TIME***, que é o cálculo do momento em que a task é criada e colocada em **backlog** até o momento em que ela vai para **done** ou o ***CYCLE TIME***, que é medido desde o momento em que a task é colocada em **To Do** até **Done**. Lembrem-se de considerar dias úteis, fins de semana e horas úteis. 

Eu acho legal ter esse controle para tentar dar uma informação o mais próxima do "real", ou seja, estimamos com base matemática, mas para que isso seja bom, precisamos ter o hábito de **planejar as tarefas**, **quebrar as maiores** etc. Eu costuomo rodar a seguinte receita: 

1. Olhar o que tem que ser feito;
2. Planejar os testes;
3. Quebrar em micro tasks;
4. Montar o Backlog de Tasks; 
5. Rodar o processo.

Essa é a base, mas para se ter ***confiança*** em algum número, precisamos "forçar" para que ele seja confiável, e quando eu digo "forçar", quero dizer que nos esforçar para que a métrica entre no **eixo** para poder dar uma previsão das coisas.

Geralmente eu crio um quadro físico com **TO DO**, **WIP** e **DONE** e rodo a primeira semana, colho os dados necessários, e continuo por mais uma semana, e depois a terceira e por fim a quarta semana, porque eu acredito que seja um tempo relativamente bom para percebermos que podemos melhorar no planejamento e na execução e no meu caso, eu pego confiança depois de um mês nos cálculos e diante disso consigo, após o meu planejamento, dizer quanto tempo aquilo ficará pronto. É uma estimativa, e assim como toda e qualquer estimativa, ela é falha, mas quanto mais eu passar confiança, melhor será. 

Na minha última experiência, cheguei a um número de 5 tasks por dia automatizadas, não estou colocando grau de dificuldade, e sim o tempo que eu levava 5 tasks do TO DO para DONE, porém, fiquei fora por quase um mês do projeto, e quando voltei, tive que ***recomeçar*** tudo de novo, porque aqueles números já não faziam mais sentido, tanto que eu aumentei depois de um mês a taxa de entrega, chegando em 5.45 tasks por dia e nessa ocasião foi interessante porque estava em um projeto em que havia uma data de entrega ousada inclusive, porém todos os testes estavam **planejados e splitados**, e quando me perguntaram sobre o tempo de teste, mostrei as métricas, que de acordo com elas, levariam 30 dias para terminar os testes de forma automatizadas, sendo que o nosso Tech Lead deu um prazo pra ficar pronto (sem base matemática) de 7 dias, ou seja, chutou uma data e mentiu sobre ela.

Indo nessa direção, quando alguém vem com alguma coisa que está fora do fluxo (expedites), informo que vai haver impacto nas métricas, negocio, e o mais importante, **divido o RISCO** com todos os envolvidos, e assim não serei o único cobrado (lembrem-se disso). 

Usar esse tipo de medida para **projetos de automação** (odeio esse nome), onde sou condicionado a automatizar todo o core da aplicação é fundamental para negociar prazos, pois todos os dias surgem novos testes a serem feitos em bug fixes ou features.

Encontre um mecanismo para alinhar seus números com o processo do time, e se o time não estiver utilizando um processo saudável, tente levar seu nível de entendimento para dentro do time, até mesmo para que o time tenha blindagem suficiente sobre as previsões e se o time tiver um nível de maturidade legal, use isso a seu favor. 

Não é necessário fazer uma auto retrospectiva, mas esteja sempre atento aos seus números, **SEMPRE** colha as métricas semanalmente (eu costumo tirar na sexta-feira), um erro comum é procrastinar essa colheita, e fazemos isso depois de 15, 20 dias. Eu não gosto dessa prática porque eu perco o contexto do planejamento e da execução, ou seja, pode ser que em uma semana eu tenha entregado 2 por dia ao invés de 5, então se eu esperar 20 dias para colher essas métricas, pode ser que eu me esqueça o que levou a diminuir em um pouco mais de 50% a minha taxa de entrega e assim entrar numa esfera de "Ah, isso não serve pra nada mesmo.", porque tirar métricas é uma tarefa muito muito **CHATA**, mas a longo prazo, faz todo sentido, principalmente quando vierem te perguntar quando as coisas vão ficar prontas.