---
title: Interface do usuário indutivo
description: Este tópico descreve o modelo de interface do usuário conhecido como IUI (interface do usuário indutivo).
ms.assetid: d99dc30a-68e5-4b7a-8cbd-0ac77a90a354
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 632e16191b7103cbf6be9fe209ada78781d4a53c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159293"
---
# <a name="inductive-user-interface"></a>Interface do usuário indutivo

Este tópico descreve o modelo de interface do usuário conhecido como IUI (interface do usuário indutivo). Também chamada de navegação indutivo, o modelo IUI sugere como tornar os aplicativos de software mais simples, dividindo os recursos em telas ou páginas que são fáceis de explicar e entender. Esse modelo de IUI é evidente em vários projetos da Microsoft, como o Microsoft Money 2000, os miniaplicativos do painel de controle do Windows, várias telas e caixas de diálogo no Microsoft Visual Studio 2010 e os painéis de tarefas em Microsoft Office.

-   [Introdução](#introduction)
-   [IUI em ação: resolvendo um problema de design comum](#iui-in-action-solving-a-common-design-problem)
    -   [O problema: o software é difícil de usar](#the-problem-software-is-hard-to-use)
    -   [Interface do usuário dedutivo](#deductive-user-interface)
    -   [Uma solução: interface do usuário indutivo](#a-solution-inductive-user-interface)
-   [Etapas para criar uma interface do usuário indutivo](#steps-for-creating-an-inductive-user-interface)
    -   [Etapa 1: concentrar cada página em uma única tarefa](#step-one-focus-each-page-on-a-single-task)
    -   [Etapa dois: declarar a tarefa](#step-two-state-the-task)
    -   [Etapa três: fazer o conteúdo da página se adequar à tarefa](#step-three-make-the-pages-contents-suit-the-task)
    -   [Etapa quatro: oferecer links para tarefas secundárias](#step-four-offer-links-to-secondary-tasks)
-   [Diretrizes adicionais](#additional-guidelines)
    -   [Usar modelos de tela consistentes](#use-consistent-screen-templates)
    -   [Torne-o óbvio como executar a tarefa com os controles na tela](#make-it-obvious-how-to-carry-out-the-task-with-the-controls-on-the-screen)
    -   [Fornecer uma maneira fácil de concluir uma tarefa e iniciar uma nova](#provide-screens-for-starting-tasks)
    -   [Torne a próxima etapa de navegação óbvia](#make-the-next-navigational-step-obvious)
-   [Assistência ao usuário](#user-assistance)
    -   [Assistência principal](#primary-assistance)
    -   [Assistência secundária](#secondary-assistance)
-   [Apêndice: projetando e testando o Microsoft Money 2000](#appendix-designing-and-testing-microsoft-money-2000)
    -   [Projetando e testando o Money 2000](#designing-and-testing-money-2000)
    -   [Testes de usabilidade](#usability-tests)
    -   [Comparação com sites da Web](#comparison-with-web-sites)

## <a name="introduction"></a>Introdução

O IUI é um modelo de interface do usuário que sugere como tornar os aplicativos de software mais simples, dividindo os recursos em telas ou páginas que são fáceis de explicar e entender. A Microsoft implementou esse modelo no Money 2000, um grande aplicativo de software comercial. Os testes informais sugerem que os usuários podem executar tarefas mais rapidamente neste modelo como nas interfaces tradicionais e podem encontrar coisas com mais facilidade.

Muitos aplicativos de software comercial incluem interfaces de usuário nas quais uma tela apresenta um conjunto de controles, mas deixa-o para o usuário para deduzir a finalidade da página e como usar os controles para realizar essa finalidade.

Os princípios descritos neste documento não exigem nem implicam nenhum conjunto rígido específico de designs, controles ou elementos visuais. Como as interfaces gráficas do usuário em geral, os princípios deste documento deixam muito espaço para a flexibilidade e a criatividade no design.

Os princípios gerais da interface do usuário indutivo são demonstrados com exemplos extraídos do Money 2000.

> [!IMPORTANT]
> O conceito geral de IUI está em sua insofisticada. Os designers que empregam essas técnicas estão aprendendo e descobrindo mais sobre ela, pois elas as utilizam para o software. As informações neste documento evoluem ao longo do tempo conforme a pesquisa e o conhecimento nessa área aumentam. Este tópico fornece uma introdução ao IUI, em vez de uma firme, um conjunto abrangente de diretrizes.

 

## <a name="iui-in-action-solving-a-common-design-problem"></a>IUI em ação: resolvendo um problema de design comum

Esta seção aborda um problema de design comum com os produtos de software atuais e apresenta o IUI como uma técnica para superar o problema.

### <a name="the-problem-software-is-hard-to-use"></a>O problema: o software é difícil de usar

A maioria dos softwares é muito difícil de usar. Essa conclusão é desenhada de teste de usabilidade, evidências curiosas e experiências pessoais de designers de software. O conceito de IUI foi criado por meio da condução de pesquisa, fazendo palpites sobre o que torna o software atual difícil de usar e, em seguida, proposta de soluções. Os designers que usam o IUI devem contar com a satisfação do cliente para determinar o sucesso final do design.

A maioria dos produtos de software atuais é difícil de usar pelos seguintes motivos gerais:

-   Os usuários não parecem construir um modelo mental adequado do produto.

    O design da interface para a maioria dos produtos de software atuais pressupõe que os usuários compreendam um modelo conceitual que os designers criaram com cuidado. Infelizmente, a maioria dos usuários não parece adquirir um modelo mental que seja completo e preciso o suficiente para orientar sua navegação. Esses usuários provavelmente estão muito ocupados e sobrecarregados com informações. Eles não têm tempo, energia ou desejo de estudar um modelo conceitual para seu software.

-   Até mesmo muitos usuários de tempo demorado nunca são os procedimentos comuns.

    Os designers sabem que novos usuários podem ter problemas a princípio, mas esperam que esses problemas desapareçam à medida que os usuários aprendem tarefas comuns. Os dados de usabilidade indicam que isso geralmente não acontece. Em um estudo, os pesquisadores configuram equipamentos automatizados para usuários de vídeo em casa. As fitas mostraram que os usuários que se concentram na tarefa em questão não observam necessariamente o procedimento que eles estão seguindo e não aprendem com a experiência. Na próxima vez que os usuários executam a mesma operação, eles podem se deparar com ele exatamente da mesma maneira.

-   Os usuários devem trabalhar de difícil para descobrir cada recurso ou tela.

    A maioria dos produtos de software são projetados para (os poucos) usuários que entendem seu modelo conceitual e têm procedimentos comuns. Para a maioria dos clientes, cada recurso ou procedimento é um quebra-cabeça frustrante e indesejado. Os usuários podem assumir que esses quebra-cabeças são um custo inevitável de usar computadores, mas eles certamente ficarão mais felizes sem essa carga.

A melhor solução para esses problemas é encontrar uma estratégia geral para tornar os recursos dos produtos de software mais evidentes e auto-explicativos. Os usuários devem ser capazes de encontrar um recurso toda vez que precisarem dele e devem ser capazes de usar esse recurso sempre que desejarem usá-lo.

### <a name="deductive-user-interface"></a>Interface do usuário dedutivo

A maioria dos elementos no software atualmente exige que o usuário os estude e deforneça seu comportamento, conforme demonstrado pela captura de tela a seguir.

![captura de tela de uma caixa de diálogo Propriedades de exemplo.](images/iuiguidelines01.png)

Os usuários experientes do computador, incluindo os designers de software, reconhecem rapidamente que essa caixa de diálogo permite que eles gerenciem uma lista de coisas. Eles entendem os botões abaixo que a lista pode adicionar, remover e fornecer informações sobre itens de lista. No entanto, observe que nenhum desse comportamento é explicitamente declarado na própria caixa de diálogo.

Agora, dê uma olhada na caixa de diálogo do ponto de vista de um usuário casual. Muitos usuários, quando você enfrentou essa caixa de diálogo, perguntarão "o que eu devo fazer com isso?" Quando a caixa de diálogo for exibida, o usuário deverá parar e descobrir o que fazer em seguida. Primeiro, o usuário deve deduzir o fato de que o grande retângulo branco é uma caixa de listagem vazia a ser preenchida com itens. O pequeno rótulo de texto da caixa, "coisas", oferece uma dica vaga. Alguns usuários tentariam digitar na caixa de listagem, pois ela se parece com uma caixa de texto de edição.

Em seguida, o usuário deve deduzir que os botões abaixo da lista afetam seu conteúdo. Alguns dos botões estão inicialmente desabilitados, o que é outra fonte potencial de confusão do usuário. O usuário deve experimentar os controles para saber como a caixa de diálogo funciona.

O usuário também pode fazer outras perguntas: "quantos itens devo colocar na lista? Devo inserir itens em uma ordem específica? Por que eu recebi essa caixa de diálogo em primeiro lugar? O que é isso? "

Os usuários são distraídos de suas metas sempre que precisam descobrir a finalidade de uma tela e como usá-la. Isso, por fim, representa um custo em tempo e satisfação do usuário. Ainda pior, os usuários pagam esse custo repetidamente à medida que eles usam um quebra-cabeça sobre a interface toda vez que usarem um recurso.

Uma tela deve ter um título que explique claramente sua finalidade. Quando os designers criam uma tela, eles raramente exigem que ele tenha uma finalidade claramente expresso. Em vez disso, ele pode simplesmente ser parte de um modelo conceitual maior que o usuário deve deduzir.

Estudos mostram que muitos usuários são confundidos até mesmo por operações básicas no software. Eles têm dificuldade em entender o que o produto pode fazer para eles, onde ir para executar uma operação e como executar essa operação depois de encontrá-la. A simplificação do software fazendo alterações fundamentais é uma maneira eficiente de atender aos clientes existentes de forma mais completa e atrair novos usuários.

### <a name="a-solution-inductive-user-interface"></a>Uma solução: interface do usuário indutivo

Como uma nova maneira de criar software, a meta do IUI é reduzir a quantidade de idéias irrelevantes que os usuários devem fazer para se moverem com êxito entre partes de um produto e usar seus recursos. A palavra indutivo vem da induzição de verbo, o que significa liderar ou mover por influência ou persuasão.

IUI é uma extensão da interface de estilo da Web comum. No ambiente da Web, as páginas precisam ser simples e baseadas em tarefas porque cada informação deve ser enviada a um servidor por uma conexão relativamente lenta. Em seguida, o servidor responde com a próxima etapa e assim por diante. Um bom design da Web significa focar em uma única tarefa por página e fornecer navegação por meio de páginas. Da mesma forma, a navegação indutivo começa com o foco da atividade em cada página para uma única tarefa principal.

Uma interface indutivo bem projetada ajuda os usuários a responder a duas questões fundamentais que eles enfrentam ao examinar uma tela:

-   O que eu deveria fazer agora?
-   Por onde vou ir aqui para realizar minha próxima tarefa?

O software criado de acordo com esses princípios responde a essas perguntas, começando com uma premissa fundamental: uma tela com uma finalidade única, claramente declarada e explícita é mais fácil de entender do que uma página sem tal finalidade. Se a tela for mais fácil de entender, será mais fácil para o usuário saber o que fazer e onde ir em seguida.

Essa premissa fundamental pode ser expandida em uma série de quatro etapas para criar software que usa IUI:

-   Concentre cada tela em uma única tarefa.
-   Declare a tarefa.
-   Faça o conteúdo da tela se ajustar à tarefa.
-   Oferecer links para tarefas secundárias.

Embora este documento descreva os princípios gerais do IUI, ele também demonstra esses princípios em ação mostrando exemplos do Money 2000 e de outros softwares. Você deve considerar esses exemplos como expressões específicas de IUI, não um modelo estrito de implementação.

Além das quatro etapas listadas acima, você pode fortalecer sua interface seguindo estas cinco diretrizes:

-   Use modelos de tela consistentes.
-   Forneça telas para iniciar tarefas.
-   Torne-o óbvio como executar a tarefa com os controles na tela.
-   Forneça uma maneira fácil de concluir uma tarefa e iniciar uma nova.
-   Torne a próxima etapa de navegação óbvia.

### <a name="processes"></a>Processos

Muitas tarefas exigem que os usuários naveguem por uma série de telas. Um usuário que executa uma tarefa pode clicar em um link para uma tarefa secundária que se afasta da sequência de telas que compõe a tarefa principal. Quando o usuário conclui a tarefa secundária, deve haver uma maneira fácil de retornar o usuário diretamente para o ponto de ramificação na tarefa original. Os usuários provavelmente terão problemas para usar controles de navegação convencionais, como botões **voltar** e **Avançar** , para retornar para onde eles começaram.

Para fornecer essa capacidade, o IUI define um conceito de navegação chamado processo, uma tela ou uma série de telas que executam uma tarefa. Um processo atua como um tipo de sub-rotina de navegação. Os usuários podem iniciar um processo, trabalhar com sua série de telas e, na última página, clicar no botão "concluído" para retornar rapidamente à página em que o processo começou.

## <a name="steps-for-creating-an-inductive-user-interface"></a>Etapas para criar uma interface do usuário indutivo

Esta seção descreve detalhadamente as quatro etapas que você pode usar para criar um IUI.

### <a name="step-one-focus-each-page-on-a-single-task"></a>Etapa 1: concentrar cada página em uma única tarefa

A primeira etapa na criação de um IUI é usar um recurso ou um conjunto de recursos e dividi-lo em telas separadas. Cada tela deve ser focada em uma única tarefa, chamada de tarefa principal da tela.

Essa ideia parece simples, mas poucos aplicativos o seguem. A maioria dos aplicativos apresenta uma tela da qual todos os recursos relacionados são realizados. Esse design exige que os usuários descubram (deduzim) o que pode ser feito e como fazê-lo.

A tarefa principal pode ser específica ou aberta finalizada. Por exemplo, em um programa de finanças pessoais, uma tarefa específica pode ser "selecionar a cobrança que você deseja pagar", enquanto uma tarefa aberta pode ser "revisar o desempenho de seus investimentos".

A tarefa principal deve ser algo que faça sentido para o usuário, em vez de uma reflexão de um detalhe de implementação ou outro conceito abstrato. A tarefa deve ser algo que os usuários possam considerar, de preferência, descritos em suas próprias palavras.

### <a name="example"></a>Exemplo

Esta seção compara duas versões diferentes do Money. Os exemplos mostram recursos muito semelhantes que permitem que os usuários exibam e gerenciem contas financeiras.

O modelo IUI foi desenvolvido durante a criação do Money 2000, um aplicativo para gerenciar finanças pessoais. O Money 2000 é a oitava versão principal do produto. O Money 2000 é um grande programa do Windows com muito mais de 1 milhão linhas de código.

O Money 2000 é um aplicativo de estilo da Web. Ele não é um site da Web, mas compartilha muitos atributos com sites da Web. Sua interface do usuário consiste em páginas de tela inteira mostradas em um quadro compartilhado, com ferramentas para voltar e avançar por meio de uma pilha de navegação. Nessa base, o Money 2000 adiciona um conjunto de novas convenções de interface do usuário que criam uma experiência de usuário mais estruturada.

Embora IUI tenha sido usado pela primeira vez no design de estilo da Web do Money 2000, ele também pode ser usado com elementos de interface tradicionais, como janelas e caixas de diálogo.

No Money 99, os usuários geralmente executavam uma grande variedade de tarefas em uma única tela. Por exemplo, a captura de tela a seguir mostra o **gerente de conta** que apresentou todos os recursos relacionados à conta no Money 99 em uma única tela.

![captura de tela do gerente de contas no Money 99.](images/iuiguidelines02.png)

Essa tela agrupa uma tarefa comum, navegando para uma conta, bem como tarefas pouco frequentes, como criar e excluir contas. Nenhuma dessas tarefas específicas é diretamente expressa no título da tela, gerente de **conta**. Muitos usuários podem encontrar essa tela como desafiadora como a caixa de diálogo de exemplo na Figura 1. Em ambos os casos, o usuário deve deduzir a finalidade da tela e como usá-la.

O Money 2000, que segue o IUI, oferece um conjunto praticamente idêntico de recursos relacionados à conta, mas os fornece em duas telas separadas. A captura de tela a seguir mostra a primeira dessas telas, que se concentra inteiramente em fazer com que o usuário escolha uma conta.

![captura de tela da tela de seleção de conta no Money 2000.](images/iuiguidelines03.png)

A tela Money 2000 contém aproximadamente o mesmo número de elementos visuais que a tela anterior do Money 99, mas a página agora se concentra inteiramente em fazer com que o usuário escolha uma conta. Por exemplo, na versão do Money 99, um usuário tinha que fazer dois cliques para abrir uma conta: um para selecioná-lo e outro para selecionar a operação de abertura. Na versão do Money 2000, o único motivo pelo qual um usuário clica em uma conta é abri-lo e, portanto, um único clique pode ser suficiente. Dessa forma, embora o número de telas possa aumentar, o número de cliques necessários para executar uma tarefa comum geralmente é reduzido.

Ocasionalmente, os usuários desejarão adicionar ou remover uma conta. Para executar essa tarefa no Money 2000, os usuários navegam para uma segunda tela (mostrada na captura de tela a seguir) que se concentra na configuração de contas.

![captura de tela da tela de configuração da conta no Money 2000.](images/iuiguidelines04.png)

A finalidade de cada tela é mais clara na versão IUI do Money 2000. Além disso, cada tela tem mais espaço para dedicar ao cumprimento de sua finalidade. Por exemplo, o gerente de **contas** do Money 99 poderia dar pouco espaço ao botão **Excluir conta** , pois ele raramente era usado em comparação com os outros comandos na tela. Por outro lado, a tela de configuração da conta no Money 2000 pode apresentar esse comando de forma mais proeminente, tornando-o mais detectável e auto-explicativo.

### <a name="what-is-a-single-task"></a>O que é uma tarefa única?

Como saber se uma tela está realmente focada em apenas uma tarefa? Uma tela com suporte a várias tarefas pode ser explicada como tendo apenas uma finalidade se essa finalidade for abstrata o suficiente. Aqui está uma regra geral: uma tela se concentra em uma finalidade se o designer puder expressar essa finalidade com um título de tela conciso, significativo e natural.

Os designers do Money 2000 consideraram a interrupção dessas telas (**escolha uma conta para usar** e **configurar suas contas em dinheiro**) em mais telas. No entanto, como cada tela já tem um título conciso, significativo e de som natural, os designers acreditaram que as telas estavam concentradas o suficiente. Ao criar uma tela, se não for possível considerar um título claro e simples, provavelmente você está tentando fazer muito na tela.

### <a name="step-two-state-the-task"></a>Etapa dois: declarar a tarefa

Cada tela deve ser intitulada com uma instrução concisa e explícita de sua tarefa principal. Isso pode ser uma instrução direta ("Selecione a conta que você deseja balancear") ou uma pergunta que você deseja que o usuário responda ("qual conta você deseja balancear?").

Esse é outro princípio simples de soar, que geralmente não é praticado. Por exemplo, versões anteriores do Money tinham telas com títulos como **gerente de serviços financeiros online** e **conta de saldo**. Os usuários tinham que deduzir a finalidade e o comportamento dessas telas da organização e dos rótulos de seus controles.

O título da tela ou da página é muito importante. Se o produto usa janelas, páginas de estilo da Web, caixas de diálogo ou outro design, o título não deve ter permissão para rolar.

### <a name="usable-screens-have-clear-titles"></a>As telas utilizáveis têm títulos claros

As telas que executam muitas tarefas exigem títulos abstratos ou complexos. Por exemplo, a tela Money 99 mostrada na Figura 2 permitia ao usuário navegar para contas e configurar contas. O título abstrato "gerente de contas" foi dado a esta página em uma tentativa de capturar essas duas finalidades. Embora os usuários possam ter algumas ideias sobre o que uma página de "gerente de contas" pode fazer, talvez não percebam que a tarefa mais comum para essa tela era simplesmente escolher uma conta.

Algumas telas ou comandos têm finalidades abstratas que não sugerem prontamente títulos claros. Para essas telas, os designers podem escolher nomes que sejam deliberadamente vagos, como "configurações", jargões cunhado, como "QuickStep;" ou jargão que revela detalhes de implementação ("compactação de banco de dados"). Esses tipos de nomes geralmente são confusos ou enganosos para os usuários. Além disso, esses nomes geralmente são nomes que não expressam a ação que o usuário deseja realizar, o que aumenta a confusão.

Os títulos de tela e outros nomes geralmente não são determinados até o final do processo de design. Os designers geralmente solicitam que os gravadores surjam um nome adequado para uma tela depois de serem projetados e codificados. Nesse ponto, não há nenhum recurso se um bom nome não puder ser encontrado e, portanto, a equipe pode precisar se liquidar por nomes que não estão claros. A solução para essa falha é que os designers pensem em termos de clareza em funções e títulos de tela logo no início do processo de design.

As funções e títulos de tela devem se concentrar nas tarefas mais comuns executadas pelos clientes. Os designers geralmente são tentados a fornecer enormes quantidades de funcionalidade em uma tentativa de atender ao maior número de clientes, juntamente com os desejos da própria equipe de design. No entanto, os recursos adicionais sempre adicionam complexidade e outros custos.

### <a name="screen-title-indicates-design-clarity"></a>Título da tela indica clareza do design

No modelo IUI, os designers escolhem os títulos de tela nos primeiros estágios do processo de design. Em vez de escolher um título para justificar a maneira como a tela funciona, o título é usado para determinar se a tela faz sentido. Se nenhum título adequado puder ser encontrado, o recurso será reprojetado. Se nenhum design permitir um título claro e conciso (ou seja, se não houver nenhuma maneira de explicar o recurso), os designers poderão abandonar o recurso. Nas capturas de tela a seguir, compare a tela pagamento da fatura do Money 99 à esquerda, que fornece um rótulo estático para a página ("próximas listas & depósitos") e a tela do Money 2000 correspondente à direita, que tem um título explícito ("clique na cobrança que você gostaria de pagar"):

![captura de tela que mostra um título estático no Money 99 e um título ativo no Money 2000.](images/iuiguidelines05.png)

Um título de tela, que é naturalmente apenas uma frase ou frase, é mais fácil de ser alterado do que um design ou código. Apesar desse fato, a experiência com o IUI mostrou que insistir em um título de tela claro produz designs melhores. Os títulos devem ser escolhidos com a entrada dos membros da equipe de educação e uso do usuário, bem como os designers de produto.

Às vezes, os integrantes da equipe podem tentar adiar essa decisão, supondo que os clientes compartilhem sua compreensão da finalidade de uma tela. Quando forçada a oferecer uma declaração clara e concisa dessa finalidade, no entanto, as diferenças de opinião são geralmente reveladas. Ao resolver essas diferenças e escolher um título antecipadamente, as discussões de design podem continuar mais suavemente.

Depois que um título é escolhido, você não deve considerá-lo inalterado. Os designers provavelmente refinarão títulos de tela ao longo do tempo, como em qualquer design. No entanto, o primeiro título escolhido deve ser tão forte quanto possível nesse estágio de desenvolvimento.

### <a name="guidelines-for-choosing-screen-titles&quot;></a>Diretrizes para escolher títulos de tela

Esta seção descreve uma técnica simples para escolher bons títulos de tela. Para usar essa técnica, os designers Imaginem um amigo perguntando, &quot;Qual é essa tela?&quot; e, em seguida, surgiram uma resposta clara e útil que conclui a frase &quot;esta é a tela onde você?.&quot; As palavras que completam a sentença se tornam o título da tela.

Durante o desenvolvimento do Money 2000, os gravadores de documentação da equipe criaram diretrizes de título de tela para garantir a qualidade e a consistência. Por exemplo, essas diretrizes sugeriam títulos que usaram verbos e foram frases como perguntas ou instruções diretas. Os designers impediam nomes estáticos que permitiam mais abstração e podem ser vagas.

Para simplificar os títulos, os designers evitaram frases compostas e tentaram usar a linguagem de conversação, evitando termos inconvenientes e jargão. Se os designers não conseguirem descrever a tarefa sem recorrer a conjunção (&quot;and&quot;, &quot;or"), a tela provavelmente está tentando fazer mais de uma tarefa e será menos provável que o usuário possa entender imediatamente o que fazer.

Mesmo quando um título é escolhido com cuidado, a região do título pode ser muito pequena para explicar adequadamente uma tarefa complexa. Para aliviar esse problema, você pode incluir um breve parágrafo descritivo na parte superior da área de conteúdo da tela que elabora a tarefa.

A tabela a seguir contém alguns exemplos de títulos de tela no Money 99 e títulos para as mesmas ou as telas relacionadas no Money 2000.



| Títulos de tela no Money 99             | Novos títulos de tela no Money 2000                         | Comentário                                         |
|---------------------------------------|---------------------------------------------------------|-------------------------------------------------|
| **Gerente de contas**                   | **Escolha uma conta** **configurar suas contas**<br/> | Título estático alterado para títulos ativos.          |
| **Detalhes da Conta**                   | **Alterar a configuração da conta**                                | Título estático alterado para ativo, título específico. |
| **Calendário de pagamentos**                  | **Pagar uma fatura**                                          | Título vagado que se tornou descritivo.                   |
| **Gerenciador de serviços financeiros online** |                                                         | Página não necessária após o redesign.                 |



 

### <a name="making-the-screen-title-prominent"></a>Destacando o título da tela

Depois de liquidar um título de tela útil, é importante garantir que a atenção do usuário seja desenhada para ele. Alguns estudos mostraram que os usuários raramente lêem texto instrutivo. Para ajudar a superar esse problema, os títulos de tela devem ser projetados para serem proeminentes e atraentes a fim de atrair a atenção do usuário. O Design Visual da tela deve informar ao usuário que o título é a coisa mais importante a ser lida.

### <a name="step-three-make-the-pages-contents-suit-the-task"></a>Etapa três: fazer o conteúdo da página se adequar à tarefa

Ao criar software que siga as diretrizes do IUI, o trabalho de design mais rígido geralmente envolve a quebra de recursos em telas ou páginas. A próxima etapa é determinar quais controles serão usados em cada tela para realizar sua tarefa principal. Esses controles compõem o conteúdo da página, onde o usuário faz o trabalho. O título e o conteúdo da tela são duas metades de uma caixa de diálogo entre o programa e o usuário. O título representa a pergunta do programa ou fornece uma instrução, e o usuário responde pela interface da tela.

Se o título da tela for claro e simples, criar a tela será normalmente simples. Por exemplo, uma das telas do Money 2000 mostradas anteriormente é intitulada "escolher uma conta a ser usada". Dado esse título, a tela obviamente deve conter uma lista simples de contas das quais o usuário pode escolher. Outra tela do Money 2000 tem o título "verificar os itens a serem incluídos em seus impostos". Naturalmente, essa tela contém uma lista de verificação de itens.

Os usuários devem ser capazes de descobrir facilmente como usar controles para obter a tarefa principal da tela. Quando os usuários são instruídos a selecionar uma conta e podem procurar na tela para localizar uma lista de contas, eles confirmam sua compreensão da tarefa. Isso aumenta a chance de que os usuários sejam bem-sucedidos, o que também aumenta sua confiança na execução de outras tarefas.

### <a name="screen-content-areas"></a>Áreas de conteúdo da tela

O local exato e a forma das áreas de conteúdo da tela dependem do design do software. No Money 2000, a região de conteúdo da tela é tudo abaixo do título da tela e à direita da lista de tarefas. Essa região pode rolar por telas longas. Alguns conteúdos não essenciais também podem aparecer na área de status abaixo da lista de tarefas.

Os designers podem optar por elaborar a tarefa principal da tela em um parágrafo na parte superior da região de conteúdo. Os usuários nunca precisam ler esse texto, mas podem achar útil. Muitos usuários podem ignorá-lo e ainda usar a tela com êxito. Ao contrário do título, essa descrição pode rolar para fora se a tela for rolável. Para obter mais detalhes, consulte [diretrizes para escolher títulos de tela](#guidelines-for-choosing-screen-titles).

Se os designers desejarem uma página para exibir lembretes não essenciais, alertas ou outras informações de status, ele poderá ser mostrado à esquerda da área de conteúdo principal, na lista de tarefas no lado esquerdo da tela. Funcionalmente, essa área de status é uma região adicional para o conteúdo da tela. Essa área não é proeminente o suficiente para conter controles essenciais.

### <a name="provide-a-clear-exit-from-the-page"></a>Fornecer uma saída clara da página

Depois de concluir uma tarefa com êxito, o usuário enfrenta outro problema: quando e como sair da tela. Para telas cuja tarefa principal é navegação, executar a própria tarefa move o usuário para a próxima tela. Em outras telas, pode ser mais difícil para o usuário saber como proceder. Por exemplo, em uma tela que solicita que o usuário digite informações em campos, o usuário pode precisar de ajuda para descobrir quando e como continuar. Nessas páginas, muitas vezes é útil oferecer um botão limpar **próximo** ou **concluído** em um local consistente.

Estudos de usabilidade mostraram que os usuários preferem usar esses botões mesmo quando botões de navegação globais, como botões de **fundo** ou **página inicial** em uma barra de ferramentas, estão disponíveis. Os usuários geralmente ficam desagradáveis em telas sem uma saída clara, até mesmo as telas cujo único propósito é fornecer informações a serem lidas.

Para obter mais informações sobre esse assunto, consulte [fornecer uma maneira fácil de concluir uma tarefa e iniciar uma nova](#provide-screens-for-starting-tasks) na seção de diretrizes adicionais.

### <a name="step-four-offer-links-to-secondary-tasks"></a>Etapa quatro: oferecer links para tarefas secundárias

A última etapa na criação de uma tela é fornecer links para tarefas secundárias, que são recursos que não realizam diretamente a tarefa principal, mas estão relacionados à tela. Por exemplo, se a tarefa principal em uma tela for escrever uma carta, as tarefas secundárias nessa tela poderão ser Pesquisar um endereço de correspondência ou imprimir um envelope.

As tarefas secundárias podem abrir caixas de diálogo, alterar a apresentação visual do conteúdo da tela ou navegar pelo usuário para uma tela diferente. Uma tarefa secundária pode realizar indiretamente a tarefa principal ou pode redirecionar os usuários perdidos para o local que eles estão procurando.

Se uma página for uma conversa entre o computador e o usuário, uma tarefa secundária permitirá que o usuário ignore a pergunta atual do computador e peça que o computador faça outra coisa em vez disso. Por exemplo, imagine esta caixa de diálogo: computador: "qual fatura você deseja pagar?" Usuário: "na verdade, o que eu realmente quero fazer é encontrar uma fatura que paguei um pouco."

Algumas telas em seu produto não terão tarefas secundárias, enquanto outras terão várias. Você deve evitar a criação de uma longa lista de tarefas que provavelmente serão difíceis de serem verificadas pelo usuário. Se uma tela tiver uma lista relativamente longa de tarefas secundárias, as tarefas mais comuns deverão ser posicionadas primeiro, agrupadas em uma seção separada ou, de outra forma, enfatizadas visualmente.

A lista não deve incluir todas as tarefas secundárias concebível, desde que ela torne a próxima etapa de navegação óbvia. Em vez de oferecer muitas tarefas secundárias, uma tela pode fornecer tarefas secundárias que navegam para páginas subsidiárias que listam mais tarefas.

### <a name="visual-design-of-secondary-tasks"></a>Design Visual de tarefas secundárias

As tarefas secundárias devem ser listadas em uma posição subordinada na tela, onde são acessíveis, se necessário, mas não distraiam o usuário da tarefa principal. Colocar essa lista em uma posição consistente em cada tela ajuda os usuários a localizar a lista rapidamente quando precisarem dela.

Se você exibir a lista de tarefas secundárias no lado esquerdo da tela, a lista em si não deverá ser rolável, nem sempre deverá rolar com a página, conforme mostrado na captura de tela a seguir da tela de **pagamento de cobrança** do Money 2000.

![captura de tela da tela de pagamento de cobrança no Money 2000.](images/iuiguidelines07.png)

## <a name="additional-guidelines"></a>Diretrizes adicionais

Esta seção descreve cinco diretrizes úteis para criar um IUI de acordo com as quatro etapas descritas na seção anterior.

### <a name="use-consistent-screen-templates"></a>Usar modelos de tela consistentes

Ao criar um software que siga o modelo IUI, você deve criar um modelo para usar como um guia para cada tela. O modelo indutivo não determina que você use qualquer modelo específico. Há muitas variações possíveis que podem atender a um design indutivo. Seu produto pode precisar apenas de um modelo para todas as suas telas, ou você pode criar vários modelos diferentes para várias finalidades.

Um bom modelo permite que um novo usuário entenda rapidamente como as telas do produto funcionam. O uso consistente do modelo nas telas do produto fornece um bom fluxo de interface do usuário da tela para a tela. Como os usuários aprendem a esperar que os mesmos elementos apareçam nos mesmos locais, eles podem digitalizar e começar a usar cada nova tela mais rapidamente.

### <a name="provide-screens-for-starting-tasks"></a>Fornecer telas para iniciar tarefas

Os produtos criados com o IUI geralmente usam telas especiais projetadas para iniciar usuários em conjuntos de tarefas. Essas telas são chamadas de páginas de atividades porque organizam grupos relacionados de tarefas comuns. As páginas de atividade fornecem um ponto de partida para os usuários. Uma página de atividade normalmente apresenta links para outras páginas em que o usuário realmente trabalha. As páginas de atividade perguntam ao usuário "o que você deseja fazer agora?" e apresentar uma lista de possíveis respostas. As páginas de atividade podem seguir um modelo especial para ajudar os usuários a reconhecê-las.

Uma página de atividade faz uma boa página inicial padrão para um produto. Quando os usuários iniciam um aplicativo, eles geralmente têm uma ideia em mente sobre a tarefa que desejam realizar. Normalmente, o motivo para iniciar o produto é um de um pequeno número de tarefas muito comuns. A página inicial padrão do produto reconhece isso tornando-o óbvio como iniciar tarefas comuns.

A **Home** Page do Money 2000 é um exemplo de uma página de atividade. Por padrão, os usuários veem essa tela, onde é exibido o acesso a tarefas financeiras comuns, como o pagamento de uma fatura e o balanceamento de uma conta, quando elas iniciam o aplicativo.

A captura de tela a seguir mostra a **Home** Page do Money 2000.

![captura de tela do home page do Money 2000. uma página de atividade que lista algumas tarefas comuns e fornece links para conjuntos de tarefas em outras páginas.](images/iuiguidelines08.png)

Como o Money fornece muitos recursos financeiros, apenas as tarefas financeiras mais comuns se ajustam à **Home** Page. Para todas as outras tarefas, a **Home** Page é vinculada a um conjunto de páginas de atividades da subsidiária chamado centros financeiros. Cada área principal do Money fornece um centro financeiro. Essas telas apresentam a próxima camada de tarefas, servindo como um ponto de salto para todos os recursos de cada área.

Por exemplo, a área de **impostos** sobre dinheiro contém os recursos relacionados a impostos do produto. A área de **impostos** oferece links para esses recursos em uma página do **centro de impostos** , conforme mostrado na captura de tela a seguir.

![captura de tela da página do centro de impostos do Money 2000. ](images/iuiguidelines09.png)

Uma página de atividade também pode ser muito mais simples se houver menos opções disponíveis. A captura de tela a seguir mostra como uma página de atividade pode ser usada para gerenciar contas de usuário do Windows.

![captura de tela de uma página de atividade do Money 2000 para gerenciar contas de usuário do Windows. ](images/iuiguidelines10.png)

### <a name="make-it-obvious-how-to-carry-out-the-task-with-the-controls-on-the-screen"></a>Torne-o óbvio como executar a tarefa com os controles na tela

A melhor maneira de seguir essa diretriz é escolher um título de tela apropriado e limitar o escopo de tarefas primárias apenas ao mais comum. Depois de ter chegado a um título e uma finalidade claros para a página, escolher o conjunto certo de controles será simples.

### <a name="provide-an-easy-way-to-complete-a-task-and-start-a-new-one"></a>Fornecer uma maneira fácil de concluir uma tarefa e iniciar uma nova

O último obstáculo que um usuário enfrenta em uma tela é descobrir quando e como sair. O usuário normalmente deixa a tela clicando em um link ou executando um comando que navega para outra tela. Esses links podem aparecer na área de conteúdo da tela, na lista de tarefas ou nas barras de ferramentas de navegação. Os usuários também podem deixar uma tela fechando o arquivo atual ou o próprio aplicativo.

A tarefa em algumas telas é preparar para uma operação que o usuário deve confirmar ou cancelar. Essas telas geralmente oferecem um link que executa e confirma a operação e outro link que cancela. Se o usuário ignorar essas opções e clicar em outro link, o programa deverá executar a opção menos destrutiva. As telas devem indicar o que acontecerá se o usuário usar esse caminho. Você pode formular os links para tornar isso mais óbvio. Por exemplo, um botão de confirmação rotulado como "salvar alterações" implica que as alterações feitas na tela não terão efeito até que esse botão seja clicado.

Mesmo que os usuários possam sair sempre que desejarem, você ainda poderá oferecer um link que sugira uma saída óbvia da página. O mesmo é verdadeiro para páginas que simplesmente exibem informações estáticas. Para obter mais informações sobre esse assunto, consulte a seção [fornecer uma saída clara da página](#provide-a-clear-exit-from-the-page).

### <a name="starting-and-completing-processes"></a>Iniciando e concluindo processos

Para os fins deste artigo, os processos são técnicas para lidar com tarefas que levam o usuário a mais de uma tela.

Suponha que um usuário clique em um link no conteúdo da tela ou na lista de tarefas e seja levado para outra tela. Essa página, por sua vez, pode ser a primeira de uma série de telas que realiza algum resultado geral. No final desta série de telas, o usuário deseja retornar à tela que precedeu o processo. Há pelo menos duas maneiras de retornar o usuário? clicar no botão voltar repetidamente ou retornar à home page e navegar a partir daí? Mas nenhum desses métodos é óbvio ou natural. A maioria dos usuários espera encontrar um botão na tela final que os retorna diretamente para a tela original.

O modelo IUI dá suporte a esse cenário por meio do conceito de um processo, uma tela ou uma série de telas tratadas como uma unidade de navegação. Os usuários podem inserir o processo, trabalhar em suas telas e, na última tela, encontrar um botão que os retorna para onde eles começaram. É importante que o usuário possa iniciar o processo de vários locais do produto. Os usuários são sempre devolvidos ao local onde começaram, independentemente de onde eles fossem quando iniciaram o processo.

### <a name="process-name"></a>Nome do processo

Cada processo deve receber um nome e o nome deve aparecer em algum lugar em cada tela do processo. O Money 2000 usa essa abordagem. Cada tela que faz parte de um processo geral inclui o nome desse processo ao longo da parte superior. Esse nome de processo é exibido menos proeminente do que o título exclusivo da tela, pois é menos importante. O nome do processo lembra os usuários qual processo está realizando e reforça a noção de que todas as telas no processo fazem parte de um único recurso. Por exemplo, a área de **impostos sobre dinheiro** inclui um processo de **avaliador de impostos** que abrange várias telas. Cada tela nesse processo exibe o nome do processo coletivo e seu título de tela exclusivo.

### <a name="implementation-of-processes"></a>Implementação de processos

O mesmo processo pode ser iniciado de vários links em telas diferentes, e os usuários sempre serão retornados para a página inicial correta. Esse comportamento não pode ser obtido por meio de um link embutido em código na tela final do processo, pois o destino do link variará. Em vez disso, o aplicativo pode implementar esse comportamento mantendo uma pilha de processos ativos, independentemente da pilha de navegação normal usada pelos comandos **voltar** e **Avançar** . Quando o usuário inicia um processo, a tela de inicialização é enviada por push na pilha de processo. Quando o usuário clica no botão **Done** na tela final do processo, o aplicativo abre a tela de inicialização mais recente fora da pilha e retorna o usuário para essa tela.

Quando os usuários navegam para fora de uma tela em um processo, o processo permanece ativo na pilha de processos. Os usuários podem concluir o processo de backup na tela em que o deixou e depois continuar. Isso permite que os usuários façam um desvio, faça backup e continue com o processo. Para ver como esse comportamento funciona, inicie qualquer processo de compra online no World Wide Web, deixe o site e, em seguida, pressione o botão **voltar** . Em geral, você poderá escolher de onde parou.

### <a name="done-button"></a>Botão Concluído

Para concluir uma tela e passar para a próxima tela no processo, as telas podem exibir um botão próximo à parte inferior da página. O rótulo desse botão é "próximo", "concluído" ou algo semelhante. Se o botão finalizar o processo e o processo puder ser chamado de vários locais, a legenda do botão **Done** poderá incluir o nome do local de chamada.

### <a name="navigation-bar"></a>Barra de navegação

Em qualquer tela, os usuários podem decidir que concluíram a área atual do produto e que desejam iniciar outra coisa. Eles talvez não queiram concluir explicitamente a tela atual antes de passar para outra parte do produto. Uma barra de ferramentas de navegação pode oferecer ao usuário um conjunto de links para iniciar novas tarefas. Assim como acontece com outras listas de links de tarefas, eles devem seguir o princípio de tornar a próxima etapa de navegação óbvia, discutida em detalhes na seção a seguir.

### <a name="make-the-next-navigational-step-obvious"></a>Torne a próxima etapa de navegação óbvia

Poucos programas podem disponibilizar todos os seus recursos ao mesmo tempo. Os usuários geralmente devem navegar por um programa para encontrar um recurso específico. Os usuários serão mais bem-sucedidos na navegação se puderem ver com facilidade como obter pelo menos uma etapa mais próxima do resultado desejado. As telas que usam IUI são projetadas com esse princípio em mente.

Por exemplo, as páginas de atividade não exibem necessariamente todas as tarefas ou destinos que o usuário pode querer alcançar a partir desse ponto. Em vez disso, as páginas de atividade fornecem uma lista de tarefas que são concluídas o suficiente para que os usuários possam determinar facilmente o link apropriado para clicar, mesmo que apenas as leve para outra página de links. As tarefas mais frequentes devem ser mais proeminentes e exigem a menor quantidade de navegação. Tarefas menos frequentes podem exigir mais etapas.

Veja um exemplo do Money 2000. Suponha que os usuários desejam executar uma operação apenas ocasionalmente, como verificar o valor estimado do pagamento de imposto de renda do ano seguinte. Primeiro, os usuários começam a procurar esse recurso na home page do Money 2000. Como o recurso não aparece na lista de tarefas comuns, ele deve verificar a lista de áreas financeiras. A área de **impostos** parece comprometer, então clique nela. A página do **centro de impostos** contém um link para o recurso de estimativa de imposto que eles estão procurando, para que eles cliquem e concluam sua tarefa. Ao aplicar os princípios de IUI, o Money 2000 permite que os usuários encontrem intuitivamente o que estão procurando.

## <a name="user-assistance"></a>Assistência ao usuário

Esta seção descreve um conjunto de diretrizes sugeridas para integrar o texto de assistência do usuário em um produto que usa o IUI.

A assistência principal refere-se a todo o texto visível na tela (conforme mostrado na captura de tela a seguir). A assistência principal fornece pistas textuais e focadas em tarefas para que os usuários possam entender facilmente todas as informações apresentadas na tela. Eles entendem a finalidade da página e a maneira como os objetos se relacionam entre si para ajudar a realizar tarefas. Como o texto está diretamente na tela, as informações que respondem a perguntas sobre iniciantes como "o que devo fazer?" é fácil de acessar e altamente visível sem que o usuário precise realizar qualquer ação.

![captura de tela da tela de configuração da conta do Money 2000.](images/iuiguidelines11.png)

A assistência secundária consiste em todo o texto que não está visível na tela e requer que alguma interação do usuário seja acessada, como clicar ou passar o mouse sobre um elemento da interface do usuário. Esse conteúdo não é essencial para realizar a tarefa em questão, mas ainda está diretamente relacionado.

### <a name="primary-assistance"></a>Assistência principal

A assistência principal pode incluir alguns ou todos os seguintes componentes:

-   Título da tela

    Exemplo: alterar sua imagem

    O título da tela é o primeiro e mais importante item que aparece na tela. Seu objetivo é descrever na própria linguagem do usuário a tarefa que pode ser concluída nesta página. O título da tela deve evitar descrever os detalhes de como concluir a tarefa. O texto no título da tela deve se referir apenas à tarefa principal da tela. Como regra prática, mais simples e curta a descrição da tarefa, o melhor definido para a tarefa é provavelmente. Para obter informações mais detalhadas sobre este tópico, consulte Etapa dois: [declarar a tarefa](#step-two-state-the-task).

-   Subtítulo da tela

    Exemplo: você também pode baixar uma nova imagem da Internet.

    Mesmo com um esforço cuidadoso, o título da tela pode não ser suficiente para explicar adequadamente uma tarefa complexa. O subtítulo permite elaborar a finalidade da tela. Você pode usar um subtítulo para ajudar a esclarecer a finalidade da página, fornecer descrição de tarefa adicional ou ajudar a definir expectativas. Os usuários que não lêem o subtítulo devem ser capazes de usar a página com êxito. Assim como o título, o subtítulo deve evitar descrever detalhes para concluir a tarefa.

-   Tarefas

    Exemplo: alterar a proteção de tela

    As tarefas podem ser apresentadas como links de texto ou imagens gráficas que exigem interação do usuário. Comandos que são apresentados como links de texto devem ser baseados em verbo e escritos como tarefas claras e concisas.

-   Rótulos para botões de comando

    Exemplo: criar senha

    Há três tipos de botões de comando:

    -   Cancelar
    -   Concluído
    -   Commit

    Os botões cancelar e concluídos simplesmente usam "Cancelar" e "concluído" como seus rótulos. Os botões de confirmação devem usar rótulos de texto ativos em vez de "OK". Por exemplo, use "criar senha" em vez de "OK".

-   Rótulos para outros controles

    Exemplo: digite sua senha

    Os rótulos para controles como botões de opção, caixas de seleção e caixas de texto devem ser escritos de forma clara e concisa para que os usuários saibam exatamente quais são os controles, quais serão usados e quais informações precisam ser fornecidas para realizar sua tarefa.

-   Links de "tarefas relacionadas"

    Exemplo: tarefas relacionadas-alterar outra conta

    Links de "tarefas relacionadas" são pontos de entrada explícitos para outras tarefas relacionadas ao recurso atual. Eles devem ser escritos como links baseados em tarefas.

-   Links "Veja também"

    Exemplo: Consulte também-alterar seu tema

    Os links "Veja também" são tarefas secundárias. Eles estão relacionados à tarefa principal, mas levarão o usuário para fora do contexto atual. Eles devem aparecer como links de tarefas regulares. Para obter mais informações sobre tarefas secundárias, consulte [Design Visual de tarefas secundárias](#visual-design-of-secondary-tasks).

### <a name="secondary-assistance"></a>Assistência secundária

A assistência secundária pode incluir alguns ou todos os seguintes componentes:

-   InfoTips

    Você pode usar um InfoTip para fornecer ao usuário informações adicionais sobre um link de tarefa ou um botão de comando. Por exemplo, um InfoTip em um link de tarefa pode ler "exibe uma página onde você pode escolher uma imagem para usar com sua conta". A InfoTip aparece quando o usuário passa o mouse sobre o objeto associado. Você deve criar InfoTips para todos os elementos da interface do usuário que o usuário pode clicar.

-   Tópicos de ajuda sobre "Saiba mais sobre"

    Exemplo: Saiba mais sobre o download de um arquivo

    "Saiba mais sobre" links para abrir tópicos de ajuda, como visões gerais de recursos, informações conceituais, informações de suporte e informações de procedimento. Para reduzir a desordem, você deve minimizar o número de tópicos de ajuda "Saiba mais sobre" na tela.

## <a name="appendix-designing-and-testing-microsoft-money-2000"></a>Apêndice: projetando e testando o Microsoft Money 2000

Esta seção foi adaptada das próprias descrições de primeira mão dos designers. Ele discute como a equipe do Money 2000 modificou o processo de design e teste para acomodar o modelo IUI.

### <a name="designing-and-testing-money-2000"></a>Projetando e testando o Money 2000

Projetar dinheiro 2000 usando o modelo de navegação indutivo levou a equipe a questionar os designs que estavam no produto há muito tempo. Como os princípios do modelo são simples, era fácil adotar o modelo no processo de design e permanecer com ele. No final, os designers acreditam que o modelo ajudou a fazer designs melhores do que poderiam ter produzido sem ele.

### <a name="clearer-titles-and-designs"></a>Títulos e designs mais claros

Os designers do Money 2000 perceberam que geralmente descreveriam os recursos usando palavras que realmente não apareceram na tela. No modelo IUI, as telas devem se explicar. Por exemplo, a equipe explicou que a tela rotulada **calendário de pagamento** foi destinada a pagar faturas. No Money 2000, essa tela é chamada **Pay Bills**. Todos os elementos que não estão relacionados a essa finalidade foram movidos para telas de subsidiárias, resultando em um design mais claro.

Outro exemplo envolve uma tela chamada **Gerenciador de serviços financeiros online**. A equipe se esforçau para surgir uma explicação simples da finalidade dessa tela. Quando não puderam chegar a uma, eles removeram essa tela e distribuíram seus recursos entre páginas mais logicamente definidas.

### <a name="helping-new-designers"></a>Ajudando novos designers

A equipe descobriu que é mais fácil ensinar técnicas de design de IUI a designers de software novos e inexperientes. As técnicas permitiam que os designers de todos os níveis de experiência avaliem seus designs usando títulos de tela como um teste de clareza. Quando forçado a colocar um título claro e conciso em uma tela mal projetada, os designers reconheceram rapidamente que nenhum título era bom o suficiente para a página. Eles perceberam que o problema não estava na escolha de palavras para um título, mas sim em um design de tela com falha. Com esse entendimento, eles poderiam recriar a tela para dar suporte a uma interação de usuário mais clara e, portanto, um título mais claro.

### <a name="including-writers"></a>Incluindo gravadores

À medida que o projeto progrediu, a equipe percebeu que os autores e editores de documentação devem estar envolvidos na criação de títulos de tela. Os gravadores eram limitados em sua capacidade de escolher bons títulos em versões anteriores porque estavam envolvidos apenas em um estágio posterior. As telas normalmente eram dadas títulos de trabalho temporários por designers ou programadores. Esses títulos foram usados até o final do ciclo do produto quando os gravadores eram solicitados a surgir com os títulos finais da tela. Nesse ponto, era tarde demais para retrabalhar com telas mal projetadas.

Por outro lado, a equipe do Money 2000 envolvia escritores nos primeiros estágios do processo de design. Isso trouxe uma valiosa entrada nos títulos de tela quando ainda poderia ajudar o design. Se uma tela era muito complexa para permitir um título claro, os gravadores podem sugerir que a página fosse reprojetada.

Ao final do projeto, os gravadores e designers acreditaram que os títulos de tela estavam mais claros e mais seguros do que nas versões anteriores. Os gravadores também acharam mais fácil explicar as novas páginas, tornando o trabalho de documentação do produto mais simples. Todos os membros da equipe pensaram que envolver todas as disciplinas na fase de design tornaram o produto melhor e mais fácil de usar.

### <a name="usability-tests"></a>Testes de usabilidade

Ao desenvolver o Money 2000, a equipe conduziu vários testes de usabilidade para examinar as diferenças entre a antiga estrutura de navegação do Money 99 e as alterações que foram feitas como resultado da aplicação do modelo IUI.

### <a name="prototype-testing"></a>Teste de protótipo

No início do processo de desenvolvimento do produto, os designers criaram um protótipo para explorar como os usuários reagirão ao IUI. Esse trabalho foi feito logo no início do processo de desenvolvimento para dar tempo para refinar os princípios do modelo antes de os programadores começarem a revisar o produto em si.

A equipe criou um protótipo no Microsoft Visual Basic e HTML que simulava atividades de finanças pessoais normalmente executadas no Money. No protótipo, os usuários podem navegar para mais de 50 páginas que representam as principais áreas do produto. Nessas áreas, eles podiam configurar contas financeiras, pagar faturas, exibir relatórios e trabalhar com seus investimentos.

Onze participantes executaram o mesmo conjunto de tarefas no Money 99 e no protótipo do IUI. Eles foram atribuídos aleatoriamente para usar um dos produtos primeiro. Quatro participantes foram os usuários atuais do Money, quatro eram usuários atuais de um produto concorrente e três nunca usaram um produto financeiro pessoal antes.

As preferências gerais indicaram que os quatro usuários atuais do Money preferidos Money 99 (a versão que estavam usando em casa), enquanto os sete usuários restantes preferem o novo protótipo para a versão atual. Para todas as outras medidas, não havia nenhuma diferença entre os usuários dos três grupos. Em termos de desempenho geral, os usuários estavam na área errada do produto duas vezes quantas vezes usar o Money 99 (2,82 vezes por tarefa), como no protótipo (1,45 vezes por tarefa). Outros dados de preferência e medidas de desempenho, embora não sejam significativos, apareciam para favorecer o protótipo. Com base nesses dados e em outros testes, a equipe de produto do Money decidiu incorporar os princípios de IUI no Money 2000.

### <a name="product-testing"></a>Teste de produto

Depois que a maioria do código para o produto foi concluída, a equipe realizou outro estudo de usabilidade para examinar a implementação final do IUI. Neste teste, 10 participantes que nunca usaram um produto de finanças pessoal antes foram selecionados para usar o Money 99 ou o Money 2000. Todos os usuários executaram as mesmas tarefas.

Os usuários do Money 2000 concluíram com êxito 89% das tarefas, enquanto os usuários do Money 99 concluíram com êxito apenas 74% das tarefas. Assim como acontece com o protótipo, os usuários também parecem ser mais rápidos, mas não significativamente diferentes, ao navegar no Money 2000 em comparação com o Money 99. Além disso, as medidas gerais de satisfação subjetiva para a navegação também tendiamm mais para o dinheiro 2000 do que para o Money 99.

### <a name="controlled-testing"></a>Teste controlado

Como o Money 2000 é enorme e complexo, não é adequado realizar experimentos controlados quanto aos efeitos da aplicação de IUI. Em vez disso, a equipe criou um ambiente mais restrito para o teste.

O teste envolvia um aplicativo de "Visualizador de mercado de ações" que permitia aos usuários modificar a exibição de um relatório de mercado de ações mostrado na tela. Os usuários podem alterar quais colunas de dados foram incluídas no relatório, a ordem das colunas do relatório, seu alinhamento e o número de casas decimais usadas. Os designers queriam ver como uma abordagem de IUI para essa tarefa seria executada em comparação com uma interface gráfica do usuário convencional.

A captura de tela a seguir mostra a interface de usuário convencional usada no teste. Uma única caixa de diálogo executa todas as tarefas de personalização de relatório. Muitos aplicativos fornecem uma caixa de diálogo semelhante para selecionar um subconjunto de uma lista de itens. A caixa de diálogo contém duas listas: a lista à esquerda exibe todas as colunas de relatório disponíveis e a direita mostra o subconjunto de colunas que o usuário selecionou para o relatório. Controles adicionais modificam os atributos Order e Formatting para colunas de relatório selecionadas na lista à direita.

![captura de tela de uma caixa de diálogo convencional.](images/iuiguidelines12.png)

Para a versão IUI desta tarefa, a equipe criou um aplicativo estilo da Web. Cada tarefa de personalização foi colocada em uma página separada. O aplicativo também incluiu uma página principal, mostrada na captura de tela a seguir, que pergunta aos usuários como eles desejam personalizar o relatório.

![captura de tela de uma tela de teste do IUI.](images/iuiguidelines13.png)

Clicar em links nesta página principal leva o usuário a páginas adicionais para executar tarefas de personalização específicas. Por exemplo, a captura de tela a seguir mostra a página usada para selecionar colunas de relatório.

![captura de tela de uma tela de teste do IUI para selecionar colunas de relatório.](images/iuiguidelines14.png)

Em testes de ambas as versões, os assuntos foram solicitados a personalizar relatórios de um determinado estado inicial (mostrado na tela) para um estado de meta especificado (mostrado em um folheto em papel). O computador mantém o controle da quantidade de tempo e o número de tentativas que os assuntos fizeram para personalizar o relatório. O computador informou aos usuários quando ele personalizou o relatório com êxito.

O teste incluía 88 participantes. Cada participante foi solicitado a personalizar um conjunto de 11 relatórios com uma das duas versões do aplicativo. Além disso, 72 desses participantes retornaram uma semana mais tarde para personalizar outro conjunto de 11 relatórios usando a mesma versão da primeira sessão. Cada assunto foi classificado como um usuário de computador principiante, principalmente usando o computador para email, jogando paciência e navegando na Web.

Não havia nenhuma diferença significativa entre os usuários das duas versões ou qualquer uma das outras variáveis de interesse. Os usuários executaram tarefas na mesma velocidade, iteraram na tarefa o mesmo número de vezes e tiveram as mesmas classificações de satisfação subjetiva geral para as duas versões. Esse teste, portanto, falhou em mostrar todas as medidas nas quais o IUI resultou em uma melhoria ou degradação no desempenho ou em classificações subjetivas.

Pode ser argumentado que, se o usuário precisar navegar mais para executar a tarefa, a quantidade de tempo para executar a tarefa deverá ser maior. Embora esse experimento não sugira esse resultado, é importante observar que o tempo médio de desempenho e seus desvios padrão associados para as duas abordagens diferentes para essa tarefa eram quase idênticos.

Pesquisa adicional será necessária para determinar se há aprimoramentos mensuráveis do uso de IUI. Na pior das hipóteses, esse teste não forneceu nenhuma evidência que IUI danifique o desempenho ou o uso do produto.

### <a name="comparison-with-web-sites"></a>Comparação com sites da Web

Muitos sites bem projetados usam princípios semelhantes ao modelo IUI descrito neste documento. Isso é provavelmente um efeito colateral da maneira como a Web funciona. Como é difícil implementar interações complexas entre controles em uma única página da Web, os designers geralmente dividem tarefas em partes que envolvem mais de uma viagem ao servidor para obter uma nova página. Alguns sites incluem, inclusive, títulos de página que informam claramente a finalidade da página.

Os designers de aplicativos tradicionais têm um conjunto muito mais rico de ferramentas disponíveis. Isso proporciona mais flexibilidade, mas também oferece mais oportunidades para criar páginas complexas e confusas. Ao criar interfaces de usuário indutivos, os designers devem usar esse poder com critério e se lembrar da clareza e da simplicidade do valor.

 

 





