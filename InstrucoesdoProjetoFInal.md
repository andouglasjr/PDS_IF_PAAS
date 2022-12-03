# Instruções do Projeto Final

Este documento apresenta as instruções de como o projeto final da disciplina de PDS deve ser desenvolvido. 

## Como o projeto deve ser desenvolvido?

O projeto final consiste no desenvolvimento de um software seguindos as etapas estudadas durante a disciplina. 

### Requisitos

* O projeto deve ser desenvolvido por no máximo 4 integrantes.
* O Github deve ser usado como SCV do projeto de vocês. É necessário me incluir entre os colaboradores (_AndouglasSilva_) para que eu possa visualizar as alterações realizadas.
* A documentação deve ser feita no próprio Git, abrindo uma pasta para cada ponto das etapas do desenvolvimento do projeto.


### Avaliação

A avaliação do projeto se dará baseado nos seguintes pontos:

1. Necessidades do Cliente (10 pontos)

Apresentar em um relatório (pode ser um arquivo .md como este, organizado, armazenado no git) quais as possíveis necessidades do cliente baseado na visita e nas propostas apresentadas abaixo. Lembrando que nem tudo que é necessidade será desenvolvido. Isso será avaliado nos requitos.

2. Requisitos (10 Pontos)

Baseado nas necessidades do cliente, apresentar quais são os requisitos funcionais e não-funcionais do sistema. É interessante classificar os requisitos como: desejável, essencial ou opcional. Essa classificação permite definir aquilo que de fato será implementado nos próximos passos. Pesquise sobre relatórios de requisitos funcionais de sistemas para vocês terem uma ideia de como esse ponto é documentado. Essa documentação pode ser feita em um outro arquivo .md (como este), organizado e armazenado no git.

3. Análise dos Requisitos e Projeto (35 Pontos)

Baseado no documento dos Requisitos, apresentar aquilo que será realmente desenvolvido (considerando o tempo que vocês tem para implementar). Além disso, criar diagramas que apresentem o fluxo desses requisitos. Por exemplo, utilizar o Diagrama de Caso de Uso para cada requisito funcional listado anteriormente e que será implementado. Também criar o projeto do BD.

4. Implementação (35 Pontos)

Implementar o sistema. A linguagem deve ser escolhida pelo grupo. Tudo que for realizado deve ser enviado ao github.

5. Teste (10 Pontos)

Testar a implementação usando teste unitário, integração ou de sistema. (Pelo menos um desses deve ser realizado)

## Qual será o projeto?

Durante a visita ao CT do Queijo, foram apresentados alguns processos que são realizados na produção dos diferentes tipos de produtos, geralmente de forma manual. Como falado anteriormente, vocês podem pensar, basicamente, em dois tipos de sistemas: (1) um que vocês já estão familiarizados voltado ao desenvolvimento de sistema web e (2) um outro tipo que entraria mais na área de automação industrial com a ideia do **supervisório**. 

Um supervisório é um software com interface gráfica que recebe informações de sensores e apresenta, em forma de desenho, essas informações ao usuário. Dito isto, listarei algumas demandas que foram apresentadas no CT.

### Controle de Inventário 

Este projeto consiste no controle de material que é adquirido e consumido pelo CT do Queijo para realizar a produção, além de um controle para cada tipo dessa produção. Por exemplo, se será produzido Queijo, é necessário que a produção seja inserida no sistema, com os dados de quantidade de queijo que será produzido, assim como todo o material utilizado e para onde será destinado. Para este projeto será necessário pesquisar como é realizado a produção de cada produto, baseado no que foi visto durante a visita. 

### Controle de Acesso de Funcionários

Na visita foi falado que diferentes profissionais participam, de diferentes formas, da produção no ambiente: coordenadores, professores, técnicos e bolsitas. Neste projeto será desenvolvido um sistema que armazene os funcionários do CT do Queijo, dando-lhes as devidas permissões para acessar o ambiente de trabalho, assim como um controle de acesso para cada usuário. O sistema também deve permitir que produções ou visitas sejam marcadas de forma a facilitar o fluxo de trabalho dentro do CT.

### Controle de Máquinas e Equipamento 

Este projeto consiste no armazenamento de informações relacionadas as máquinas utilizadas no CT do Queijo. Neste sistema, o usuário poderá cadastrar novas máquinas adquiridas, visualizar o estado das máquinas instaladas, deletar máquinas que não estão mais em uso e atualizar o status dessas máquinas. Além disso, as máquinas devem ser cadastradas baseadas nos produtos que elas fazem parte do processo. Por exemplo, uma caldeira X é usada no processo de Pasteurização. Um sensor de temperatura Y é usado para produção do queijo, etc. 

### Controle de Pedidos

Este projeto consiste no desenvolvimento de um sistema que facilite os pedidos solicitados ao CT do Queijo. Usuários externos poderão solicitar a produção de um determinado produto, inserindo a quantidade desejada. O sistema apresenta ao CT uma interface de pedidos, organizada por data e hora de solicitação. O CT pode aceitar a solicitação ou recusar (enviando ao usuário externo uma justificativa, por exemplo, falta de insumos ou agenda cheia). O sistema gera a agenda de entrega desses produtos. 

### Supervisório do Processo de Pasteurização 

A pasteurização foi um dos processos apresentados no dia da visita. Basicamente, esse processo consiste no aumento e diminuição da temperatura do leite de forma controlada. Neste projeto, uma interface gráfica do processo deve ser desenvolvida, para apresentar ao cliente de forma remota todo o caminho percorrido pelo leito, assim como o aumento e diminuição da temperatura e a saída da máquina. Neste processo, sensores de temperatura são utilizados, além de bombas pra fazer o fluxo do leite, da chegada até a saída. Logs de ocorrências precisam ser apresentados e armazenados (por exemplo, bomba ligada, sensor de nível máximo atingido, sensor de nível mínimo atingido, máquina desligada, etc.). Deve ser permitido ao cliente iniciar e parar o processo de forma remota. Dica: O react é uma ótima ferramenta para criação de telas deste tipo, pois é simples criar cada um dos componentes e animá-los.

### Supervisório da Produção da Iogurteira 

Neste processo, o ingredientes são misturados em um recipiente utilizando-se de um misturador (uma pá que gira no interior desse recipiente) com temperatura controlada pelo usuário. Neste processo válvulas são acionadas para trazer o leite até o recipiente e depois para retirá-lo. Um sensor de temperatura é utilizado para indicar o valor de medição ao cliente que produz o iogurte. Logs de ocorrências precisam ser apresentados e armazenados (por exemplo, bomba ligada, sensor de nível máximo atingido, sensor de nível mínimo atingido, máquina desligada, etc.). Deve ser permitido ao cliente iniciar e parar o processo de forma remota. Dica: O react é uma ótima ferramenta para criação de telas deste tipo, pois é simples criar cada um dos componentes e animá-los.

### Supervisório das Câmaras Frias 

Neste processo, a câmara fria que vocês entraram precisa ter sua temperatura indicada externamente ao cliente. Neste caso, o sistema deve armazenar (a cada tempo pré-definido) medições da temperatura interna da câmara de forma que seja possível acompanhar todo o processo, mesmo que a energia do ambiente acabe. Alarmes precisam ser acionados pelo sistema (alguma mensagem na tela deve aparecer), caso a temperatura esteja fora do intervalo correto para mantêr os produtos armazenados na câmara. Deve ser permitido ao cliente iniciar e parar o funcionamento da câmara de forma remota. Dica: O react é uma ótima ferramenta para criação de telas deste tipo, pois é simples criar cada um dos componentes e animá-los.

## Exemplo do que seria um Supervisório

![Exemplo de Supervisório](https://www.rtautomacao.com.br/imagens/informacoes/sistema-supervisorio-industrial-01.jpg)

## Considerações Finais

1. Qualquer dúvida entrar em contato comigo (**andouglas.silva@escolar.ifrn.edu.br**).
2. Usaremos as aulas que ainda teremos de forma presencial (turno e contra turno) para desenvolvimento do projeto.
3. A aula da próxima semana (que não teremos por causa do jogo) e um sábado letivo serão utilizados para leitura de dois assuntos que faltam para fechar a ementa: Implantação e Custo de Software.

