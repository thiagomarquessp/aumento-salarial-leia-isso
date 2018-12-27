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

Para calcular é bem simples: 

```shell
SD = Start Date
FD = Finish Date

Lead Time = FD - SD 

Cycle Time = FD - SD 
```
Só para lembrar, no caso do Lead Time, lembrem-se que o Start Date é no momento em que a task entra em Backlog e o Finish Date é o momento em que entra em Done e o Cycle Time tem o Start Date no momento em que sai de Backlog e entra em WIP e o Finish Date é o momento que a task entra em Done.

**Obs.:** Marque a data no post it de inicio e utilize o horário tanto no Start Date, quanto no Finish Date.

## Quando queremos pontuar com Fibonacci

 Uma das coisas mais comuns em times distribuídos é utilizar fibonacci para estimar user stories e praticamente todos os times que eu já trabalhei utilizam a sequência 1,2,3,5,8,13,21 de uma maneira muito abstrata, muitas vezes fazendo apenas por fazer, ou seja, não colocam critérios para nada.

 Nesse tópico vou falar sobre como utilizar essa sequência com um pouco de critério, ou seja, levar um pouquinho a sério essa estimativa. 

 Bem, não encarem isso como uma verdade absoluta, até porque eu não conheço todos os contextos do mundo, então estou passando um pouco de conhecimento que vi dando certo em pelo menos 2 lugares que apliquei essa forma de pensar. 

 Algo que observei em todos os times que trabalhei foi a rapidez que o time respondia as seguintes questões: 

 1. Nesse útimo mês (ou qualquer medida de tempo), qual feature foi considerada a mais **fácil** que se lembram?
 2. Nesse útimo mês (ou qualquer medida de tempo), qual feature foi considerada a mais **difícil** que se lembram?

 Normalmente temos na cabeça as coisas que são extremamente complicadas e também sabemos aquelas que foram muito fáceis de fazer, e se fizermos essa pergunta pra nós mesmos, sobre qualquer assunto, vamos saber responder.

 Sabendo dos dois extremos, vamos definir em Fibonacci o **mais fácil (1)** e o **mais difícil (8)**. Geralmente utilizo apenas essas duas medidas porque eu considero que uma user story de 13 pontos não cabe em um sprint, mas pronto, essa é uma visão que eu tenho, e como geralmente os times são imaturos, assumo aquilo que julgo ser importante e começo da seguinte maneira: 

 1. Num quadro físico, defino os dois extremos (1 e 8) e coloco as informações de tarefas/user story mais fácil e a mais difícil apenas e defino aquilo como o que eu chamo de VMA (Verdade Momentânea Absoluta), pois confio no que o time me fala sobre exatamente o que eles fizeram nessas condições. 

 2. Definido os extremos, na hora do planning, começo o trabalho comparativo, ou seja, pego uma user story e de bate pronto pergunto ao time se está **mais próximo** do 1 ou **mais próximo** do 8 e de onde estiver mais próxima, eu assumo também apenas esses extremos, ou seja, se está próxima do 1, assumo como 1, se estiver próximo do 8, assumo como 8. 

 3. Depois de definido uma pontuação máxima para o time informe a área de produto sobre essa decisão e vamos rodar o primeiro sprint.
 A psicologia explica que quando temos algo inovador em um contexto "crítico", as pessoas tendem a trabalhar com mais empenho e entusiasmo as primeiras semanas. Então sugiro levar a sério os números a partir do terceiro sprint (minha opinião).

 4. Nas retrospectivas levem os números do sprint, por exemplo: 
Previsão: 40 pontos
Entregues: 40 pontos
Não entregues: N/A
Expedites: N/A
Em desenvolvimento: 0

Esse é um sprint lindo, onde prometemos e entregamos, não tivemos expedites ou outras coisitas a mais (BUG FIX por exemplo).

Mas tem casos como: 

Previsão: 40 pontos
Entregues: 35 pontos
Não entregues: 5
Expedites: 0
Em desenvolvimento: 3
Sprint Backlog: 2

Esse foi um sprint um pouco problemático porque não entregamos o prometido, e justamente na **retrospectiva** que temos que ver o que foi que aconteceu e vou dar um exemplo macro das user stories para ilustrar o exemplo acima: 

```ruby
US1  - 8
US2  - 8
US3  - 8
US4  - 8
US5  - 1
US5  - 1
US6  - 1
US7  - 1
US8  - 1
US9  - 1
US10 - 1
US11 - 1
Total: 40 pontos
```
Levar na retrospectiva as US com suas pontuações e como foi a saúde do nosso sprint pode resultar na **Melhora Contínua**, pois justamente na retrospectiva sabemos o que de fato ocorreu para que nesse caso não conseguissemos entregar o sprint (caso seja Scrum) e então nesse primeiro momento, abstrair do padrão **coisas positivas, negativas, o que temos que melhorar** como ocorrem na maioria das retrospectivas e sim trazer valores reais de como nós trabalhamos e ver onde foi que erramos e acreditem que muitas coisas passam por nós na hora do planning que esquecemos de mencionar, por exemplo ***férias**, **ausência por doença**, **acidentes**, **mau humor** (acreditem, é normal acontecer porque ninguém é de ferro), etc. ou então, o claro problema de planejamento, onde normalmente subestimamos ou superestimamos, mas nesse contexto, onde tenho duas faixas apenas (1 e 8), é totalmente aceitável, inclusive o desafio é exatamente esse, criar um "caos" a médio prazo.

4. Planning pós "caos" vamos seguir da mesma maneira, porém dessa vez vamos olhar para os itens que não entregamos, e vamos avaliar com as mesmas perguntas: Mais perto do 1 ou Mais perto do 8? Porém agora vem a pergunta complementar: 

1. Mais perto do 1, mas é igual ao 1?

Se a resposta for não, vem a seguinte:

2. Se não é igual ao 1, é igual ao 8?

Se a resposta for **SIM**, assuma como 8, caso contrário, **abrimos a terceira faixa** (5) e assumimos aquilo como 5 e deixamos aquela User Story nessa régua padrão, ou seja, temos a **mais fácil**, a **mais difícil** e agora o grupo das **medianas**.

E esse exercício será sempre feito até abrir a faixa 13, que no meu caso, quando chegamos em 13 é hora de transformar essa user story em várias outras pequenas. 

## Mas isso é realmente importante? 

Sim, porque dessa maneira conseguimos aos poucos passar confiança aos nossos stakeholders, evitamos falar prazos por falar e usamos um pouco de estatística para comprovar o trabalho feito, negociar prazos, dividir o risco. 

## Tamanhos de camisa 

Há pessoas que estimam por tamanhos de camisa (P, M, G, GG), que a dinâmica é a mesma, cria régua, tira conclusões, apresente na retrospectiva, bla bla bla .... porém, queria deixar uma dica de ouro sobre esse tipo de medida, que é tirar das user stories e colocar em **épicos**, ou seja, defino um épico qualquer, planejo, quebro em várias user stories, faço aquele trabalho que citei acima, **PORÉM**, ai que entra a mágica, imagine que esse épico teve seus 40 pontos e dentre todos os épicos já feitos nos ultimos X tempos, foi o mais díficil, podemos assumir esse épico com o **tamanho G** e podemos afirmar com mais precisão, ao bater o olho em um novo épico, que se ele for **G**, terá pelo menos **40 pontos**, faz sentido? E o exercício de replanejar, repontuar e criar novas réguas, também serve para os épicos e quanto mais acertivos formos, melhor será e se eu for abrir as métricas a um nível mais diversificado, veremos que um **épico tamanho G** com **40 pontos** será entregue em **X sprints**, e em números fictícios, se meu time entrega 10 pontos por sprint, esse épico estará em produção no máximo em **4 semanas**. 

A importância dessas medidas são justamente para conseguirmos (vou repetir isso exaustivamente) dar previsibilidade e confiança aos nossos stakeholders, e sim, **ÓBVIO** que vamos errar, mas erraremos por pouco, a variação é muito baixa, e quando há, é geralmente porque esquecemos de considerar alguma variável (férias, médico, faltas, humor, ressaca, etc.).