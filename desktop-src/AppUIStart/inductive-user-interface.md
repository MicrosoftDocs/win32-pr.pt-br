---
title: Inativar Interface do Usuário
description: Este tópico descreve o modelo de interface do usuário conhecido como IUI (interface do usuário inativa).
ms.assetid: d99dc30a-68e5-4b7a-8cbd-0ac77a90a354
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a16282248e1942070f5dc3e1418016657de2e84f39e1f8473eaedcbc0eeccbf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589333"
---
# <a name="inductive-user-interface"></a>Inativar Interface do Usuário

Este tópico descreve o modelo de interface do usuário conhecido como IUI (interface do usuário inativa). Também chamado de navegação inativa, o modelo de IUI sugere como simplificar os aplicativos de software por meio da quebra de recursos em telas ou páginas fáceis de explicar e entender. Esse modelo de IUI é evidente em vários projetos da Microsoft, como o Microsoft Money 2000, os applets do painel de controle do Windows, várias telas e caixas de diálogo no Microsoft Visual Studio 2010 e os painéis de tarefas no Microsoft Office.

-   [Introdução](#introduction)
-   [IUI em ação: resolvendo um problema de design comum](#iui-in-action-solving-a-common-design-problem)
    -   [O problema: o software é difícil de usar](#the-problem-software-is-hard-to-use)
    -   [Interface do usuário de desaconsução](#deductive-user-interface)
    -   [Uma solução: inativar Interface do Usuário](#a-solution-inductive-user-interface)
-   [Etapas para criar um Interface do Usuário](#steps-for-creating-an-inductive-user-interface)
    -   [Etapa 1: Concentrar cada página em uma única tarefa](#step-one-focus-each-page-on-a-single-task)
    -   [Etapa dois: Estado da tarefa](#step-two-state-the-task)
    -   [Etapa três: Fazer com que o conteúdo da página se adequa à tarefa](#step-three-make-the-pages-contents-suit-the-task)
    -   [Etapa quatro: Oferecer links para tarefas secundárias](#step-four-offer-links-to-secondary-tasks)
-   [Diretrizes adicionais](#additional-guidelines)
    -   [Usar modelos de tela consistentes](#use-consistent-screen-templates)
    -   [Tornar óbvio como executar a tarefa com os controles na tela](#make-it-obvious-how-to-carry-out-the-task-with-the-controls-on-the-screen)
    -   [Fornecer uma maneira fácil de concluir uma tarefa e iniciar uma nova](#provide-screens-for-starting-tasks)
    -   [Tornar a próxima etapa de navegação óbvia](#make-the-next-navigational-step-obvious)
-   [Assistência do usuário](#user-assistance)
    -   [Assistência primária](#primary-assistance)
    -   [Assistência secundária](#secondary-assistance)
-   [Apêndice: Projetando e testando o Microsoft Money 2000](#appendix-designing-and-testing-microsoft-money-2000)
    -   [Projetando e testando o Money 2000](#designing-and-testing-money-2000)
    -   [Testes de usabilidade](#usability-tests)
    -   [Comparação com sites](#comparison-with-web-sites)

## <a name="introduction"></a>Introdução

A IUI é um modelo de interface do usuário que sugere como simplificar os aplicativos de software por meio da quebra de recursos em telas ou páginas fáceis de explicar e entender. A Microsoft implementou esse modelo no Money 2000, um aplicativo de software comercial grande. Testes informais sugerem que os usuários podem executar tarefas tão rapidamente nesse modelo quanto em interfaces tradicionais e podem encontrar coisas mais facilmente.

Muitos aplicativos de software comercial incluem interfaces do usuário nas quais uma tela apresenta um conjunto de controles, mas deixa para o usuário deduzir a finalidade da página e como usar os controles para realizar essa finalidade.

Os princípios descritos neste documento não exigem nem implicam nenhum conjunto rígido específico de designs, controles ou elementos visuais. Assim como as interfaces gráficas do usuário em geral, os princípios neste documento deixam muito espaço para flexibilidade e criatividade no design.

Os princípios gerais da interface do usuário inativa são demonstrados com exemplos extraídos do Money 2000.

> [!IMPORTANT]
> O conceito geral de IUI está em sua infaência. Os designers que empregam essas técnicas estão aprendendo e descobrindo mais sobre ela à medida que a usam para seu software. As informações neste documento evoluirão ao longo do tempo à medida que a pesquisa e o conhecimento nessa área aumentarem. Este tópico fornece uma introdução à IUI, em vez de um conjunto de diretrizes forte e abrangente.

 

## <a name="iui-in-action-solving-a-common-design-problem"></a>IUI em ação: resolvendo um problema de design comum

Esta seção aborda um problema de design comum com os produtos de software atuais e apresenta a IUI como uma técnica para superar o problema.

### <a name="the-problem-software-is-hard-to-use"></a>O problema: o software é difícil de usar

A maioria dos softwares é muito difícil de usar. Essa conclusão é retirada de testes de usabilidade, evidência anedótal e experiências pessoais de designers de software. O conceito de IUI foi criado realizando pesquisas, fazendo suposições instrutivas sobre o que torna o software atual difícil de usar e, em seguida, propondo soluções. Os designers que usam a IUI devem depender da satisfação do cliente para determinar o sucesso final do design.

A maioria dos produtos de software atuais é difícil de usar pelos seguintes motivos gerais:

-   Os usuários parecem não construir um modelo mental adequado do produto.

    O design de interface para a maioria dos produtos de software atuais pressu que os usuários entenderão um modelo conceitual que os designers criaram cuidadosamente. Infelizmente, a maioria dos usuários parece não adquirir um modelo mental completo e preciso o suficiente para orientar sua navegação. Esses usuários provavelmente estão muito ocupados e sobrecarregados com informações. Eles não têm o tempo, a energia ou o desejo de estudar um modelo conceitual para seu software.

-   Até mesmo muitos usuários de muito tempo nunca dominam procedimentos comuns.

    Os designers sabem que os novos usuários podem ter problemas a princípio, mas esperam que esses problemas sejam resfriados à medida que os usuários aprendem tarefas comuns. Os dados de usabilidade indicam que isso geralmente não acontece. Em um estudo, os pesquisadores configuram equipamentos automatizados para ajudar os usuários em casa. As fitas mostraram que os usuários que se concentram na tarefa em mãos não necessariamente notam o procedimento que estão seguindo e não aprendem com a experiência. Na próxima vez que os usuários executarem a mesma operação, eles poderão passar por ela exatamente da mesma maneira.

-   Os usuários devem trabalhar muito para descobrir cada recurso ou tela.

    A maioria dos produtos de software é projetada para (poucos) usuários que entendem seu modelo conceitual e têm procedimentos comuns mestres. Para a maioria dos clientes, cada recurso ou procedimento é um quebra-cabeça frustrante e indesejado. Os usuários podem presumir que esses quebra-cabeças são um custo inevitável de usar computadores, mas certamente seriam felizes sem essa carga.

A melhor solução para esses problemas é encontrar uma estratégia geral para tornar os recursos de produtos de software mais autoexplicativos e autoexplicativos. Os usuários devem ser capazes de encontrar um recurso sempre que precisam dele e devem ser capazes de usar esse recurso sempre que quiserem usá-lo.

### <a name="deductive-user-interface"></a>Interface do usuário de desaconsução

A maioria dos elementos no software hoje exige que o usuário os estudar e deduzir seu comportamento, conforme demonstrado pela captura de tela a seguir.

![captura de tela de uma caixa de diálogo de propriedades de exemplo.](images/iuiguidelines01.png)

Usuários de computador experientes, incluindo designers de software, reconhecem rapidamente que essa caixa de diálogo permite que eles gerenciem uma lista de coisas. Eles entendem que os botões abaixo da lista podem adicionar, remover e fornecer informações sobre itens de lista. No entanto, observe que nenhum desse comportamento é explicitamente declarado na própria caixa de diálogo.

Agora, dê outra olhada na caixa de diálogo do ponto de vista de um usuário ocasional. Muitos usuários, ao se deparar com essa caixa de diálogo, perguntarão: "O que devo fazer com isso?" Quando a caixa de diálogo for exibida, o usuário deverá parar e descobrir o que fazer em seguida. Primeiro, o usuário deve deduzir o fato de que o retângulo branco grande é uma caixa de listagem vazia a ser preenchida com itens. O rótulo de texto pequeno da caixa, "Coisas", oferece uma dica indefinição. Alguns usuários tentariam digitar na caixa de listagem, pois ele se parece com uma caixa de texto de edição.

Em seguida, o usuário deve deduzir que os botões abaixo da lista afetam seu conteúdo. Alguns dos botões são inicialmente desabilitados, que é outra possível fonte de confusão do usuário. O usuário deve experimentar os controles para saber como a caixa de diálogo funciona.

O usuário também pode fazer outras perguntas: "Quantos itens devo colocar na lista? Devo inserir itens em uma ordem específica? Por que eu fiz essa caixa de diálogo em primeiro lugar? Para que isso se trata?"

Os usuários não têm suas metas sempre que precisam descobrir a finalidade de uma tela e como usá-la. Isso, em última análise, representa um custo no tempo e a satisfação do usuário. Pior ainda, os usuários pagam esse custo uma e outra vez à medida que se sobrecarram pela interface sempre que usam um recurso.

Uma tela deve ter um título que explique claramente sua finalidade. Quando os designers criam uma tela, raramente exigem que ela tenha uma finalidade claramente expressável. Em vez disso, ele pode simplesmente fazer parte de um modelo conceitual maior que o usuário deve deduzir.

Os estudos mostram que muitos usuários estão confusos até mesmo por operações básicas no software. Eles têm dificuldade para entender o que o produto pode fazer por eles, onde ir para executar uma operação e como executar essa operação depois de a encontrar. Simplificar o software fazendo alterações fundamentais é uma maneira eficiente de atender melhor aos clientes existentes e atrair novos usuários.

### <a name="a-solution-inductive-user-interface"></a>Uma solução: inativar Interface do Usuário

Como uma nova maneira de criar software, a meta da IUI é reduzir a quantidade de raciocínios que os usuários devem fazer para se mover com êxito entre partes de um produto e usar seus recursos. A palavra indução vem do verbo induzir, o que significa levar ou mover por influência ou pela indução.

A IUI é uma extensão da interface de estilo Web comum. No ambiente Web, as páginas devem ser simples e baseadas em tarefas, pois cada informação deve ser enviada a um servidor por uma conexão relativamente lenta. Em seguida, o servidor responde com a próxima etapa e assim por diante. Um bom design para a Web significa concentrar-se em uma única tarefa por página e fornecer navegação por meio de páginas. Da mesma forma, a navegação indutivo começa com o foco da atividade em cada página para uma única tarefa principal.

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

O modelo IUI foi desenvolvido durante a criação do Money 2000, um aplicativo para gerenciar finanças pessoais. O Money 2000 é a oitava versão principal do produto. o Money 2000 é um grande programa de Windows com muito mais de 1 milhão linhas de código.

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

Algumas telas ou comandos têm finalidades abstratas que não sugerem prontamente títulos claros. para essas telas, os designers podem escolher nomes que sejam deliberadamente vagas, como "Configurações;" jargões cunhado, como "QuickStep;" ou jargão que revela detalhes de implementação ("compactação de banco de dados"). Esses tipos de nomes geralmente são confusos ou enganosos para os usuários. Além disso, esses nomes geralmente são nomes que não expressam a ação que o usuário deseja realizar, o que aumenta a confusão.

Os títulos de tela e outros nomes geralmente não são determinados até o final do processo de design. Os designers geralmente solicitam que os gravadores surjam um nome adequado para uma tela depois de serem projetados e codificados. Nesse ponto, não há nenhum recurso se um bom nome não puder ser encontrado e, portanto, a equipe pode precisar se liquidar por nomes que não estão claros. A solução para essa falha é que os designers pensem em termos de clareza em funções e títulos de tela logo no início do processo de design.

As funções e títulos de tela devem se concentrar nas tarefas mais comuns executadas pelos clientes. Os designers geralmente ficam tentados a fornecer enormes quantidades de funcionalidade em uma tentativa de atender ao maior número de clientes, juntamente com o desejo da própria equipe de design. No entanto, recursos adicionais sempre adicionam complexidade e outros custos.

### <a name="screen-title-indicates-design-clarity"></a>Título da tela indica clareza de design

No modelo de IUI, os designers escolhem os títulos da tela nos estágios mais antigos do processo de design. Em vez de escolher um título para justificar o modo como a tela funciona, o título é usado para determinar se a tela faz sentido. Se nenhum título adequado puder ser encontrado, o recurso será reprojetado. Se nenhum design permitir um título claro e conciso (ou seja, se não houver nenhuma maneira de explicar o recurso), os designers poderão abandonar o recurso. Nas capturas de tela a seguir, compare a tela de pagamento de fatura do Money 99 à esquerda, que fornece um rótulo estático para a página ("Contas futuras & Depósitos") e a tela money 2000 correspondente à direita, que tem um título explícito ("Clique na fatura que você gostaria de pagar"):

![captura de tela que mostra um título estático em money 99 e um título ativo em money 2000.](images/iuiguidelines05.png)

Um título de tela, que é obviamente apenas uma frase ou frase, é mais fácil de alterar do que um design ou código. Apesar desse fato, a experiência com a IUI mostrou que a depuração em um título de tela clara no início produz designs melhores. Os títulos devem ser escolhidos com a entrada dos membros da equipe de educação e usabilidade do usuário, bem como dos designers de produtos.

Às vezes, os membros da equipe podem tentar adiar essa decisão, supondo que os clientes compartilhem sua compreensão da finalidade de uma tela. No entanto, quando forçada a oferecer uma instrução clara e concisa dessa finalidade, as diferenças de opiniões geralmente são reveladas. Ao resolver essas diferenças e escolher um título no início, as discussões de design podem continuar mais suavemente.

Depois que um título for escolhido, você não deverá considerá-lo inalterável. Os designers provavelmente refinarão títulos de tela ao longo do tempo, assim como qualquer design. No entanto, o primeiro título escolhido deve ser o mais forte possível nesse estágio de desenvolvimento.

### <a name="guidelines-for-choosing-screen-titles&quot;></a>Diretrizes para escolher títulos de tela

Esta seção descreve uma técnica simples para escolher bons títulos de tela. Para usar essa técnica, os designers imaginem um amigo perguntando: &quot;Para que se trata esta tela?&quot; e, em seguida, vêm com uma resposta clara e útil que conclui a frase &quot;Esta é a tela em que você?&quot;. As palavras que concluem a frase se tornam o título da tela.

Durante o desenvolvimento do Money 2000, os autores de documentação da equipe criaram diretrizes de título da tela para garantir a qualidade e a consistência. Por exemplo, essas diretrizes sugeriram títulos que usavam verbos e foram formulados como perguntas ou instruções diretas. Os designers evitaram nomes estáticos que permitiam mais abstração e podem ser vaga.

Para simplificar os títulos, os designers evitaram frases compostas e tentaram usar a linguagem de conversação, evitando termos e jargões complicados. Se os designers não puderem descrever a tarefa sem recorrer a conjunções (&quot;e&quot;, &quot;ou"), a tela provavelmente está tentando fazer mais de uma tarefa e é menos provável que o usuário possa entender imediatamente o que fazer.

Mesmo quando um título é escolhido cuidadosamente, a região de título pode ser muito pequena para explicar adequadamente uma tarefa complexa. Para atenuar esse problema, você pode incluir um breve parágrafo descritivo na parte superior da área de conteúdo da tela que detalha a tarefa.

A tabela a seguir contém alguns exemplos de títulos de tela no Money 99 e títulos para as mesmas telas ou relacionadas no Money 2000.



| Títulos de tela no Money 99             | Novos títulos de tela no Money 2000                         | Comentário                                         |
|---------------------------------------|---------------------------------------------------------|-------------------------------------------------|
| **Gerente de contas**                   | **Escolher uma conta** **Configurar suas contas**<br/> | Título estático alterado para títulos ativos.          |
| **Detalhes da Conta**                   | **Alterar a configuração da conta**                                | Título estático alterado para título ativo e específico. |
| **Calendário de pagamento**                  | **Pagar uma fatura**                                          | Título de cargo descritivo.                   |
| **Gerente de Serviços Financeiros Online** |                                                         | Página não necessária após a reprojeto.                 |



 

### <a name="making-the-screen-title-prominent"></a>Tornando o título da tela proeminente

Depois de liquidar em um título de tela útil, é importante garantir que a atenção do usuário seja desenhada para ele. Alguns estudos mostraram que os usuários raramente leem textos instrucionais. Para ajudar a superar esse problema, os títulos de tela devem ser projetados para serem proeminentes e atraentes para chamar a atenção do usuário. O design visual da tela deve informar ao usuário que o título é a coisa mais importante a ser lida.

### <a name="step-three-make-the-pages-contents-suit-the-task"></a>Etapa três: Fazer com que o conteúdo da página se adequa à tarefa

Ao criar um software que segue as diretrizes da IUI, o trabalho de design mais difícil geralmente envolve a quebra de recursos em telas ou páginas. A próxima etapa é determinar quais controles serão usados em cada tela para realizar sua tarefa principal. Esses controles comem o conteúdo da página, em que o usuário faz o trabalho. O título e o conteúdo da tela são duas metades de um diálogo entre o programa e o usuário. O título apresenta a pergunta do programa ou fornece uma instrução e o usuário responde por meio da interface da tela.

Se o título da tela for claro e simples, a criação da tela geralmente será simples. Por exemplo, uma das telas do Money 2000 mostradas anteriormente é intitucada "Escolher uma conta a ser usada". Considerando esse título, a tela obviamente deve conter uma lista simples de contas que o usuário pode escolher. Outra tela do Money 2000 tem o título "Verificar os itens a incluir em seus impostos". Naturalmente, essa tela contém uma lista de verificação de itens.

Os usuários devem ser capazes de descobrir facilmente como usar controles para atingir a tarefa principal da tela. Quando os usuários são informado a selecionar uma conta e podem procurar na tela para encontrar uma lista de contas, eles confirmam sua compreensão da tarefa. Isso aumenta a chance de que os usuários sejam bem-sucedidos, o que também aumenta sua confiança na execução de outras tarefas.

### <a name="screen-content-areas"></a>Áreas de conteúdo da tela

A localização exata e a forma das áreas de conteúdo da tela dependem do design do software. No Money 2000, a região de conteúdo da tela é tudo abaixo do título da tela e à direita da lista de tarefas. Essa região pode rolar em telas longas. Alguns conteúdos não essenciais também podem aparecer na área de status abaixo da lista de tarefas.

Os designers podem optar por elaborar a tarefa principal da tela em um parágrafo na parte superior da região de conteúdo. Os usuários nunca precisam ler este texto, mas podem achar útil. Muitos usuários podem ignorar e ainda usar a tela com êxito. Ao contrário do título, essa descrição poderá rolar para fora se a tela for rolável. Para obter mais detalhes, consulte [Diretrizes para escolher títulos de tela.](#guidelines-for-choosing-screen-titles)

Se os designers quiserem uma página para exibir lembretes não essenciais, alertas ou outras informações de status, ela poderá ser mostrada à esquerda da área de conteúdo principal, na lista de tarefas no lado esquerdo da tela. Funcionalmente, essa área de status é uma região adicional para o conteúdo da tela. Essa área não é proeminente o suficiente para conter controles essenciais.

### <a name="provide-a-clear-exit-from-the-page"></a>Fornecer uma saída clara da página

Depois de concluir uma tarefa com êxito, o usuário enfrenta outro problema: quando e como sair da tela. Para telas cuja tarefa principal é a navegação, executar a própria tarefa move o usuário para a próxima tela. Em outras telas, pode ser mais difícil para o usuário saber como continuar. Por exemplo, em uma tela que solicita ao usuário para digitar informações em campos, o usuário pode precisar de ajuda para descobrir quando e como seguir em frente. Em tais páginas, geralmente é útil oferecer um botão **Next** ou **Done** claro em um local consistente.

Os estudos de usabilidade mostraram que os usuários preferem usar esses  botões  mesmo quando os botões de navegação globais, como Voltar ou Início em uma barra de ferramentas, estão disponíveis. Os usuários geralmente ficam desamudos em telas sem saída clara, até mesmo em telas cuja única finalidade é fornecer informações a serem lidas.

Para obter mais informações sobre esse assunto, consulte Fornecer uma [maneira](#provide-screens-for-starting-tasks) fácil de concluir uma tarefa e iniciar uma nova na seção Diretrizes Adicionais.

### <a name="step-four-offer-links-to-secondary-tasks"></a>Etapa quatro: Oferecer links para tarefas secundárias

A última etapa na criação de uma tela é fornecer links para tarefas secundárias, que são recursos que não realizam diretamente a tarefa primária, mas estão relacionados à tela. Por exemplo, se a tarefa principal em uma tela for escrever uma letra, as tarefas secundárias nessa tela poderão ser procurar um endereço de email ou imprimir um envelope.

As tarefas secundárias podem abrir caixas de diálogo, alterar a apresentação visual do conteúdo da tela ou navegar pelo usuário para uma tela diferente. Uma tarefa secundária pode realizar indiretamente a tarefa primária ou redirecionar usuários perdidos para o local que eles estão procurando.

Se uma página for uma conversa entre o computador e o usuário, uma tarefa secundária permitirá que o usuário ignore a pergunta atual do computador e peça ao computador para fazer outra coisa. Por exemplo, imagine esta caixa de diálogo: Computador: "Qual fatura você deseja pagar?" Usuário: "Na verdade, o que eu realmente quero fazer é encontrar uma fatura que eu pago um tempo atrás."

Algumas telas em seu produto não terão tarefas secundárias, enquanto outras terão várias. Você deve evitar criar uma longa lista de tarefas que provavelmente serão difíceis para o usuário verificar. Se uma tela tiver uma lista relativamente longa de tarefas secundárias, as tarefas mais comuns deverão ser colocadas primeiro, agrupadas em uma seção separada ou enfatizadas visualmente.

A lista não deve incluir todas as tarefas secundárias concebíveis, desde que ela torna a próxima etapa de navegação óbvia. Em vez de oferecer muitas tarefas secundárias, uma tela pode fornecer tarefas secundárias que navegam para páginas subsidiárias listando mais tarefas.

### <a name="visual-design-of-secondary-tasks"></a>Design visual de tarefas secundárias

As tarefas secundárias devem ser listadas em uma posição subordinada na tela, em que elas podem ser acessadas, se necessário, mas não desviam o usuário da tarefa primária. Colocar essa lista em uma posição consistente em cada tela ajuda os usuários a encontrar a lista rapidamente quando precisam dela.

Se você exibir a lista de tarefas secundárias no lado esquerdo da tela, a lista em si não deverá ser rolável, nem deverá rolar com a página, conforme mostrado na captura de tela a seguir da tela Pagamento da Fatura do Money 2000. 

![captura de tela da tela de pagamento da fatura em money 2000.](images/iuiguidelines07.png)

## <a name="additional-guidelines"></a>Diretrizes adicionais

Esta seção descreve cinco diretrizes úteis para criar uma IUI de acordo com as quatro etapas descritas na seção anterior.

### <a name="use-consistent-screen-templates"></a>Usar modelos de tela consistentes

Ao criar um software que segue o modelo de IUI, você deve criar um modelo para usar como um guia para cada tela. O modelo de indução não determina que você use qualquer modelo específico. Há muitas variações possíveis que podem atender a um design indução. Seu produto pode precisar de apenas um modelo para todas as suas telas ou você pode criar vários modelos diferentes para várias finalidades.

Um bom modelo permite que um novo usuário entenda rapidamente como as telas do produto funcionam. O uso consistente do modelo nas telas do produto fornece um bom fluxo de interface do usuário da tela para a tela. À medida que os usuários aprendem a esperar que os mesmos elementos apareçam nos mesmos locais, eles podem verificar e começar a usar cada nova tela mais rapidamente.

### <a name="provide-screens-for-starting-tasks"></a>Fornecer telas para iniciar tarefas

Produtos projetados com IUI geralmente usam telas especiais projetadas para iniciar usuários em conjuntos de tarefas. Essas telas são chamadas de páginas de atividade porque organizam grupos relacionados de tarefas comuns. As páginas de atividade fornecem um ponto de partida para os usuários. Uma página de atividade normalmente apresenta links para outras páginas em que o usuário realmente faz o trabalho. As páginas de atividades perguntem ao usuário "O que você deseja fazer agora?" e apresentam uma lista de respostas possíveis. As páginas de atividades podem seguir um modelo especial para ajudar os usuários a reconhecê-las.

Uma página de atividade torna uma boa página inicial padrão para um produto. Quando os usuários iniciam um aplicativo, eles geralmente têm uma ideia em mente sobre a tarefa que eles querem realizar. Normalmente, o motivo para iniciar o produto é uma das tarefas muito comuns. A página inicial padrão do produto reconhece isso, tornando óbvio como iniciar tarefas comuns.

A Home **page** do Money 2000 é um exemplo de uma página de atividade. Por padrão, os usuários veem essa tela, em que o acesso a tarefas financeiras comuns, como pagar uma fatura e balancear uma conta, é exibido quando eles iniciam o aplicativo.

A captura de tela a seguir mostra a Home **page** do Money 2000.

![captura de tela do money 2000 home page. uma página de atividade que lista algumas tarefas comuns e fornece links para conjuntos de tarefas em outras páginas.](images/iuiguidelines08.png)

Como Money fornece muitos recursos financeiros, somente as tarefas financeiras mais comuns se encaixam na **Home** page. Para todas as outras tarefas, a **Home** page vincula-se a um conjunto subsidiária de páginas de atividades chamadas centros financeiros. Cada área principal do Money fornece um centro financeiro. Essas telas apresentam a próxima camada de tarefas, que serve como um ponto de partida para todos os recursos em cada área.

Por exemplo, a área Impostos **sobre** Dinheiro contém os recursos relacionados a impostos do produto. A **área** Impostos oferece links para esses recursos em uma **página do Tax Center,** conforme mostrado na captura de tela a seguir.

![captura de tela da página do centro de impostos money 2000. ](images/iuiguidelines09.png)

Uma página de atividade também pode ser muito mais simples se menos opções estão disponíveis. A captura de tela a seguir mostra como uma página de atividade pode ser usada para gerenciar Windows de usuário.

![captura de tela de uma página de atividades money 2000 para gerenciar contas de usuário do Windows. ](images/iuiguidelines10.png)

### <a name="make-it-obvious-how-to-carry-out-the-task-with-the-controls-on-the-screen"></a>Tornar óbvio como executar a tarefa com os controles na tela

A melhor maneira de seguir essa diretriz é escolher um título de tela apropriado e limitar o escopo das tarefas primárias apenas às mais comuns. Depois de chegar a um título claro e uma finalidade para a página, escolher o conjunto certo de controles será simples.

### <a name="provide-an-easy-way-to-complete-a-task-and-start-a-new-one"></a>Fornecer uma maneira fácil de concluir uma tarefa e iniciar uma nova

O último obstáculo que um usuário enfrenta em uma tela é descobrir quando e como sair. O usuário normalmente sai da tela clicando em um link ou executando um comando que navega para outra tela. Esses links podem aparecer na área de conteúdo da tela, na lista de tarefas ou nas barras de ferramentas de navegação. Os usuários também podem sair de uma tela fechando o arquivo atual ou o próprio aplicativo.

A tarefa em algumas telas é preparar para uma operação que o usuário deve confirmar ou cancelar. Essas telas geralmente oferecem um link que executa e confirma a operação e outro link que cancela. Se o usuário ignorar essas opções e clicar em outro link, o programa deverá executar a opção menos destrutiva. As telas devem indicar o que acontecerá se o usuário seguir esse caminho. Você pode formular os links para tornar isso mais óbvio. Por exemplo, um botão de confirmação rotulado "Salvar Alterações" implica que as alterações feitas na tela não terão efeito até que esse botão seja clicado.

Mesmo que os usuários possam sair sempre que quiserem, você ainda poderá oferecer um link que sugere uma saída óbvia da página. O mesmo é verdadeiro para páginas que simplesmente exibem informações estáticas. Para obter mais informações sobre esse assunto, consulte a seção [Fornecer uma saída clara da página](#provide-a-clear-exit-from-the-page).

### <a name="starting-and-completing-processes"></a>Iniciando e concluindo processos

Para os fins deste artigo, os processos são técnicas para lidar com tarefas que levam o usuário a mais de uma tela.

Suponha que um usuário clique em um link no conteúdo ou na lista de tarefas de uma tela e seja levado para outra tela. Essa página, por sua vez, pode ser a primeira de uma série de telas que realiza algum resultado geral. No final desta série de telas, o usuário deseja retornar à tela que precedeu o processo. Há pelo menos duas maneiras pelas quais o usuário pode voltar? clicando no botão Voltar repetidamente ou retornando para o home page e navegando de lá? mas nenhum desses métodos é óbvio ou natural. A maioria dos usuários espera encontrar um botão na tela final que os retorna diretamente para a tela original.

O modelo de IUI dá suporte a esse cenário por meio do conceito de um processo, uma tela ou uma série de telas tratadas como uma unidade de navegação. Os usuários podem entrar no processo, trabalhar em suas telas e, na última tela, encontrar um botão que os retorne ao local em que foram iniciados. É importante que o usuário possa iniciar o processo de vários locais no produto. Os usuários sempre são retornados para o local em que foram iniciados, independentemente de onde estavam quando iniciaram o processo.

### <a name="process-name"></a>Nome do processo

Cada processo deve receber um nome e o nome deve aparecer em algum lugar em cada tela no processo. O Money 2000 usa essa abordagem. Cada tela que faz parte de um processo geral inclui o nome desse processo na parte superior. Esse nome de processo é exibido com menos destaque do que o título exclusivo da tela porque é menos importante. O nome do processo lembra aos usuários qual processo eles estão realizando e reforça a noção de que todas as telas no processo fazem parte de um único recurso. Por exemplo, a **área Impostos sobre** Dinheiro inclui um processo de **Estimador** de Imposto que abrange várias telas. Cada tela nesse processo exibe o nome do processo coletivo e seu título de tela exclusivo.

### <a name="implementation-of-processes"></a>Implementação de processos

O mesmo processo pode ser lançado de vários links em telas diferentes e os usuários sempre serão retornados para a página inicial correta. Esse comportamento não pode ser obtido por meio de um link codificado na tela final do processo, pois o destino do link variará. Em vez disso, o aplicativo pode implementar esse comportamento mantendo uma pilha de processos ativos, independentemente da pilha de navegação normal usada pelos comandos **Voltar** **e** Encaminhar. Quando o usuário inicia um processo, a tela de lançamento é pressionada na pilha de processo. Quando o usuário clica no **botão Done** na tela final do processo, o aplicativo exibe a tela de início mais recente da pilha e retorna o usuário para essa tela.

Quando os usuários navegam para fora de uma tela em um processo, o processo permanece ativo na pilha de processo. Os usuários podem concluir o processo fazendo o back-up na tela em que o deixou e, em seguida, continuar. Isso permite que os usuários façam um desvio, façam o back-up e, em seguida, façam o processo. Para ver como esse comportamento funciona, inicie qualquer processo de compra online no World Wide Web, deixe o site e pressione o **botão** Voltar. Em geral, você poderá continuar de onde paramos.

### <a name="done-button"></a>Botão Concluído

Para concluir uma tela e passar para a próxima tela no processo, as telas podem exibir um botão próximo à parte inferior da página. O rótulo desse botão é "Próximo", "Pronto" ou algo semelhante. Se o botão terminar o processo e o processo  puder ser chamado de vários locais, a legenda do botão Done poderá incluir o nome do local de chamada.

### <a name="navigation-bar"></a>Barra de navegação

Em qualquer tela, os usuários podem decidir que estão concluídos com a área atual do produto e querem iniciar outra coisa. Talvez eles não queiram concluir explicitamente a tela atual antes de passar para outra parte do produto. Uma barra de ferramentas de navegação pode oferecer ao usuário um conjunto de links para iniciar novas tarefas. Assim como com outras listas de links de tarefa, eles devem seguir o princípio de tornar a próxima etapa de navegação óbvia, discutida em detalhes na seção a seguir.

### <a name="make-the-next-navigational-step-obvious"></a>Tornar a próxima etapa de navegação óbvia

Alguns programas podem disponibilizar todos os recursos ao mesmo tempo. Os usuários geralmente devem navegar por um programa para encontrar um recurso específico. Os usuários serão mais bem-sucedidos na navegação se puderem ver facilmente como obter pelo menos uma etapa mais próxima do resultado desejado. As telas que usam a IUI são projetadas com esse princípio em mente.

Por exemplo, as páginas de atividade não exibem necessariamente todas as tarefas concebíveis ou destinos que o usuário talvez queira atingir a partir desse ponto. Em vez disso, as páginas de atividades fornece uma lista de tarefas que são concluídas o suficiente para que os usuários possam determinar facilmente o link apropriado para clicar, mesmo que ele as leva apenas para outra página de links. As tarefas mais frequentes devem ser mais proeminentes e exigir a menor quantidade de navegação. Tarefas menos frequentes podem exigir mais etapas.

Veja um exemplo de Money 2000. Suponha que os usuários querem executar uma operação que só fazem ocasionalmente, como verificar o valor estimado do pagamento do imposto de renda do próximo ano. Os usuários começam a pesquisar esse recurso na Home page do Money 2000. Como o recurso não aparece na lista de tarefas comuns, eles devem verificar a lista de áreas financeiras. A **área Impostos** parece ser uma promessa, portanto, eles clicam nele. A **página Central de** Impostos contém um link para o recurso de estimativa de imposto que eles estão procurando, para que eles cliquem nele e concluam sua tarefa. Aplicando princípios de IUI, o Money 2000 permite que os usuários encontrem intuitivamente o que estão procurando.

## <a name="user-assistance"></a>Assistência do usuário

Esta seção descreve um conjunto de diretrizes sugeridas para integrar o texto de assistência do usuário em um produto que usa a IUI.

A assistência primária refere-se a todo o texto visível na tela (conforme mostrado na captura de tela a seguir). A assistência primária fornece dicas textuais e voltadas para tarefas para que os usuários possam entender facilmente todas as informações apresentadas na tela. Eles entendem a finalidade da página e a maneira como os objetos se relacionam entre si para ajudar a realizar tarefas. Como o texto está diretamente na tela, as informações que responde a perguntas de iniciantes como "O que devo fazer?" é fácil de acessar e altamente visível sem que o usuário tenha que tomar nenhuma ação.

![captura de tela da tela de instalação da conta do money 2000.](images/iuiguidelines11.png)

A assistência secundária consiste em todo o texto que não está visível na tela e requer alguma interação do usuário para acessar, como clicar ou passar o mouse sobre um elemento de interface do usuário. Esse conteúdo não é essencial para realizar a tarefa em questão, mas ainda está diretamente relacionado.

### <a name="primary-assistance"></a>Assistência primária

A assistência primária pode incluir alguns ou todos os seguintes componentes:

-   Título da tela

    Exemplo: Alterar sua imagem

    O título da tela é o primeiro e mais importante item que aparece na tela. Sua finalidade é descrever no próprio idioma do usuário a tarefa que pode ser concluída nesta página. O título da tela deve evitar descrever os detalhes de como concluir a tarefa. O texto no título da tela só deve se referir à tarefa principal da tela. Como regra geral, quanto mais simples e menor for a descrição da tarefa, melhor será a definição da tarefa. Para obter informações mais detalhadas sobre este tópico, consulte Etapa dois: [Estado da tarefa](#step-two-state-the-task).

-   Subtítulo de tela

    Exemplo: você também pode baixar uma nova imagem da Internet.

    Mesmo com um esforço cuidadoso, o título da tela pode não ser suficiente para explicar adequadamente uma tarefa complexa. O subtítulo permite que você elabore sobre a finalidade da tela. Você pode usar um subtítulo para ajudar a esclarecer a finalidade da página, fornecer uma descrição adicional da tarefa ou ajudar a definir as expectativas. Os usuários que não leem o subtítulo devem ser capazes de usar a página com êxito. Assim como o título, o subtítulo deve evitar descrever detalhes para concluir a tarefa.

-   Tarefas

    Exemplo: alterar a economia de tela

    As tarefas podem ser apresentadas como links de texto ou imagens gráficas que exigem interação do usuário. Os comandos apresentados como links de texto devem ser baseados em verbo e gravados como tarefas claras e concisas.

-   Rótulos para botões de comando

    Exemplo: Criar Senha

    Há três tipos de botões de comando:

    -   Cancelar
    -   Concluído
    -   Commit

    Os botões Cancel e Done simplesmente usam "Cancelar" e "Done" como seus rótulos. Os botões de commit devem usar rótulos de texto ativos em vez de "OK". Por exemplo, use "Criar Senha" em vez de "OK".

-   Rótulos para outros controles

    Exemplo: digite sua senha

    Rótulos para controles como botões de rádio, caixas de seleção e caixas de texto devem ser escritos de forma clara e concisa para que os usuários saibam exatamente para que são os controles, para quais deles usar e quais informações precisam ser fornecidas para realizar sua tarefa.

-   Links de "Tarefas relacionadas"

    Exemplo: Tarefas relacionadas – Alterar outra conta

    Links de "Tarefas relacionadas" são pontos de entrada explícitos para outras tarefas relacionadas ao recurso atual. Eles devem ser gravados como links baseados em tarefas.

-   Links "Consulte também"

    Exemplo: consulte também – Alterar seu tema

    Os links "Consulte também" são tarefas secundárias. Eles estão relacionados à tarefa primária, mas tirarão o usuário do contexto atual. Eles devem aparecer como links de tarefa regulares. Para obter mais informações sobre tarefas secundárias, consulte [Design visual de tarefas secundárias.](#visual-design-of-secondary-tasks)

### <a name="secondary-assistance"></a>Assistência secundária

A assistência secundária pode incluir alguns ou todos os seguintes componentes:

-   InfoTips

    Você pode usar um InfoTip para fornecer ao usuário informações adicionais sobre um link de tarefa ou um botão de comando. Por exemplo, uma InfoTip em um link de tarefa pode ler "Exibe uma página em que você pode escolher uma imagem para usar com sua conta". O InfoTip aparece quando o usuário passar o mouse sobre o objeto associado. Você deve criar InfoTips para todos os elementos de interface do usuário que o usuário pode clicar.

-   Tópicos de ajuda "Saiba mais sobre"

    Exemplo: Saiba mais sobre – Baixando um arquivo

    Os links "Saiba mais" abrem tópicos da Ajuda, como visão geral de recursos, informações conceituais, informações de suporte e informações de procedimento. Para reduzir a confusão, você deve minimizar o número de tópicos de ajuda "Saiba mais" na tela.

## <a name="appendix-designing-and-testing-microsoft-money-2000"></a>Apêndice: Projetando e testando o Microsoft Money 2000

Esta seção foi adaptada das próprias descrições em primeira mão dos designers. Ele discute como a equipe do Money 2000 modificou o processo de design e teste para acomodar o modelo de IUI.

### <a name="designing-and-testing-money-2000"></a>Projetando e testando o Money 2000

A criação do Money 2000 usando o modelo de navegação inativa levou a equipe a questionar designs que estavam no produto há muito tempo. Como os princípios do modelo são simples, foi fácil adotar o modelo no processo de design e permanecer com ele. No final, os designers acreditaram que o modelo os ajudou a criar designs melhores do que poderiam ter produzido sem ele.

### <a name="clearer-titles-and-designs"></a>Títulos e designs mais claros

Os designers do Money 2000 notaram que geralmente descrevem recursos usando palavras que não eram realmente exibidas na tela. No modelo de IUI, as telas devem se explicar. Por exemplo, a equipe explicou que a tela rotulada **Calendário de** Pagamento foi destinada ao pagamento de faturas. No Money 2000, essa tela é chamada **de Pagar Faturas.** Todos os elementos que não estão relacionados a essa finalidade foram movidos para telas subsidiárias, resultando em um design mais claro.

Outro exemplo envolve uma tela chamada **Gerenciador de Serviços Financeiros Online**. A equipe se esforçou para chegar a uma explicação simples da finalidade dessa tela. Quando não puderam chegar a uma, removeram essa tela e distribuíram seus recursos entre páginas definidas logicamente.

### <a name="helping-new-designers"></a>Ajudando novos designers

A equipe descobriu que é fácil ensinar técnicas de design de IU a designers de software novos e insensidores. As técnicas permitiam que designers em todos os níveis de experiência avaliam seus designs usando títulos de tela como um teste de clareza. Quando forçados a colocar um título claro e conciso em uma tela mal projetada, os designers reconheceram rapidamente que nenhum título era bom o suficiente para a página. Eles percebidoam que o problema não era escolher palavras para um título, mas sim em um design de tela com falhas. Com esse entendimento, eles poderiam recriar a tela para dar suporte a uma interação de usuário mais clara e, portanto, um título mais claro.

### <a name="including-writers"></a>Incluindo gravadores

À medida que o projeto progrediu, a equipe percebeu que os autores e editores de documentação devem estar envolvidos na criação de títulos de tela. Os gravadores eram limitados em sua capacidade de escolher bons títulos em versões anteriores porque estavam envolvidos apenas em um estágio posterior. As telas normalmente eram dadas títulos de trabalho temporários por designers ou programadores. Esses títulos foram usados até o final do ciclo do produto quando os gravadores eram solicitados a surgir com os títulos finais da tela. Nesse ponto, era tarde demais para retrabalhar com telas mal projetadas.

Por outro lado, a equipe do Money 2000 envolvia escritores nos primeiros estágios do processo de design. Isso trouxe uma valiosa entrada nos títulos de tela quando ainda poderia ajudar o design. Se uma tela era muito complexa para permitir um título claro, os gravadores podem sugerir que a página fosse reprojetada.

Ao final do projeto, os gravadores e designers acreditaram que os títulos de tela estavam mais claros e mais seguros do que nas versões anteriores. Os gravadores também acharam mais fácil explicar as novas páginas, tornando o trabalho de documentação do produto mais simples. Todos os membros da equipe pensaram que envolver todas as disciplinas na fase de design tornaram o produto melhor e mais fácil de usar.

### <a name="usability-tests"></a>Testes de usabilidade

Ao desenvolver o Money 2000, a equipe conduziu vários testes de usabilidade para examinar as diferenças entre a antiga estrutura de navegação do Money 99 e as alterações que foram feitas como resultado da aplicação do modelo IUI.

### <a name="prototype-testing"></a>Teste de protótipo

No início do processo de desenvolvimento do produto, os designers criaram um protótipo para explorar como os usuários reagirão ao IUI. Esse trabalho foi feito logo no início do processo de desenvolvimento para dar tempo para refinar os princípios do modelo antes de os programadores começarem a revisar o produto em si.

a equipe criou um protótipo no Microsoft Visual Basic e HTML que simulava atividades de finanças pessoais normalmente executadas no Money. No protótipo, os usuários podem navegar para mais de 50 páginas que representam as principais áreas do produto. Nessas áreas, eles podiam configurar contas financeiras, pagar faturas, exibir relatórios e trabalhar com seus investimentos.

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

 

 





