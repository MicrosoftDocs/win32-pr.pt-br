---
title: Usabilidade no design de software
description: Este tópico apresenta o conceito de usabilidade e por que ele deve ser uma parte importante de qualquer projeto de design de software.
ms.assetid: 912b3224-e36d-44d6-98fa-a7f28e68a2d0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b302e63a475d060748e896440b28915816d910e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005064"
---
# <a name="usability-in-software-design"></a>Usabilidade no design de software

Este tópico apresenta o conceito de usabilidade e por que ele deve ser uma parte importante de qualquer projeto de design de software.

-   [Introdução](#introduction)
-   [Definindo a usabilidade](#defining-usability)
    -   [Facilidade de uso](#ease-of-use)
    -   [Usabilidade versus utilitário](#usability-vs-utility)
    -   [Gosta-lo versus usá-lo](#liking-it-vs-using-it)
    -   [Descoberta versus aprendizado versus eficiência](#discovery-vs-learning-vs-efficiency)
    -   [Os slogans não funcionam](#slogans-do-not-work)
-   [Por que a usabilidade é importante?](#why-is-usability-important)
    -   [Por que você deve se importar?](#why-should-you-care)
    -   [O que ele custa?](#what-does-it-cost)
    -   [Como posso aumentar a usabilidade?](#how-do-i-increase-usability)
    -   [Por que devo envolver os usuários?](#why-should-i-involve-users)
    -   [Não consigo apenas seguir as diretrizes?](#cant-i-just-follow-guidelines)
    -   [É necessário criar um laboratório de usabilidade?](#do-i-need-to-build-a-usability-lab)
    -   [Como faço para começar?](#how-do-i-get-started)

## <a name="introduction"></a>Introdução

O termo "usabilidade" no contexto de criação de software representa uma abordagem que coloca o usuário, em vez do sistema, no centro do processo. Essa filosofia, conhecida como Design centralizado no usuário, incorpora preocupações do usuário e advocacy do início do processo de design e determina que as necessidades do usuário devem ser as mais importantes de qualquer decisão de design.

O aspecto mais visível dessa abordagem é o teste de usabilidade, no qual os usuários trabalham e interagem com a interface do produto e compartilham suas exibições e preocupações com os designers e desenvolvedores.

## <a name="defining-usability"></a>Definindo a usabilidade

A seção define o que a usabilidade significa no contexto do desenvolvimento de software e como ele se relaciona com outros aspectos do processo de desenvolvimento.

### <a name="ease-of-use"></a>Facilidade de uso

A usabilidade é uma medida de como é fácil usar um produto para executar tarefas prescritas. Isso é diferente dos conceitos relacionados do utilitário e da maneira mais conceitual.

### <a name="usability-vs-utility"></a>Usabilidade versus utilitário

Um atributo central que determina a qualidade de um produto é útil. Isso mede se os usos reais de um produto podem atingir as metas que os designers pretendem alcançar. O conceito de ramificações de utilidade ainda mais em utilidade e utilidade. Embora esses termos estejam relacionados, eles não são intercambiáveis.

O utilitário refere-se à capacidade do produto de executar uma tarefa ou tarefas. Quanto mais tarefas o produto foi projetado para ser executado, mais utilitário ele tem.

Considere os processadores de texto do Microsoft MS-DOS típicos do final da década de 1980. Esses programas forneciam muitos recursos poderosos de edição e manipulação de texto, mas os usuários precisavam aprender e lembrar dezenas de pressionamentos de teclas misteriosos para realizá-los. Aplicativos como esses podem ser considerados com um utilitário alto (eles fornecem aos usuários a funcionalidade necessária), mas com pouca usabilidade (os usuários devem gastar muito tempo e esforço para aprender e usá-los). Por outro lado, um aplicativo simples e bem projetado, como uma calculadora, pode ser muito fácil de usar, mas não oferecer muito utilidade.

Ambas as qualidades são necessárias para a aceitação do mercado e ambas fazem parte do conceito geral de utilidade. Obviamente, se um programa for altamente utilizável, mas não fizer nada de valor, ninguém irá usá-lo. E os usuários que são apresentados com um programa poderoso que é difícil de usar provavelmente irão resistir ou buscar alternativas.

O teste de usabilidade ajuda a determinar como é fácil para os usuários executarem tarefas específicas. No entanto, ele não ajuda diretamente a determinar se o próprio produto tem valor ou utilitário. (Os usuários podem voluntariará os comentários relacionados ao utilitário durante o teste de usabilidade, mas todos os comentários devem ser verificados com outros métodos de pesquisa mais robustos.)

### <a name="liking-it-vs-using-it"></a>Gosta-lo versus usá-lo

A maneira mais conveniente é sempre uma característica desejável em um produto. Se as pessoas gostam do produto, eles têm mais probabilidade de usá-lo e recomendar a ele para outras pessoas. Mas, como com o utilitário, você deve ter cuidado para não confundir a capacidade de uso.

As pessoas frequentemente gostam de um produto por motivos não relacionados ao utilitário e à usabilidade. Eles podem ser atraídos ao seu estilo ou ao status que acreditam que o produto os confere. Normalmente, as pessoas gostam de produtos altamente utilizáveis, mas você não deve pressupor que isso significa que um produto bem curtido é utilizável.

A usabilidade é sobre se uma pessoa pode usar o produto para executar as tarefas que precisam executar. O teste de usabilidade mede principalmente o desempenho, e não a preferência. No entanto, os questionários padronizados podem ser usados para medir as preferências entre os produtos.

### <a name="discovery-vs-learning-vs-efficiency"></a>Descoberta versus aprendizado versus eficiência

Há muitos aspectos na usabilidade, mas tradicionalmente o termo se refere especificamente aos atributos de descoberta, aprendizado e eficiência.

-   A descoberta envolve procurar e localizar o recurso de um produto em resposta a uma necessidade específica. O teste de usabilidade pode determinar quanto tempo leva um usuário para encontrar um recurso e quantos erros (escolhas erradas sobre o local) o usuário faz ao longo do caminho.
-   O aprendizado refere-se ao processo pelo qual o usuário sabe como usar um recurso descoberto para concluir uma tarefa. Os testes de usabilidade podem determinar quanto tempo esse processo leva e também quantos erros o usuário faz enquanto aprende o recurso.
-   A eficiência refere-se ao ponto em que o usuário tem "dominar" o recurso e o utiliza sem precisar de mais aprendizado. O teste de usabilidade pode determinar quanto tempo leva para o usuário experiente executar as etapas necessárias para usar o recurso.

Esses três aspectos básicos da usabilidade são altamente influenciados pela natureza da tarefa em questão e pela frequência com a qual o usuário o executa. Alguns recursos são usados raramente ou são tão complexos que o usuário os aprende basicamente a cada vez; para esses recursos, a Microsoft frequentemente desenvolve assistentes para orientar o usuário durante o processo.

### <a name="slogans-do-not-work"></a>Os slogans não funcionam

Os desenvolvedores de software às vezes acham que slogans simples, como "tornar o produto mais utilizável", ajudarão a resolver problemas de usabilidade. Embora uma atitude positiva em relação à usabilidade seja importante, somente o teste de usabilidade adequado com usuários comuns, no contexto do produto específico que está sendo criado, pode fornecer aos desenvolvedores as informações de que eles precisam para criar um produto que atenderá às necessidades dos usuários. "Tornar o produto mais utilizável" deve ser o slogan de todos os desenvolvedores de software, mas faz sentido apenas se o desenvolvedor sabe o que significa usabilidade. O teste com usuários comuns é a maneira mais confiável de descobrir.

## <a name="why-is-usability-important"></a>Por que a usabilidade é importante?

A seção responde a algumas perguntas comuns sobre por que a usabilidade é importante e como incorporar princípios de design centrados no usuário no processo de desenvolvimento.

### <a name="why-should-you-care"></a>Por que você deve se importar?

Se as considerações de usabilidade ainda não tiverem sido incorporadas ao processo de design do produto, talvez você se pergunte por que ela é necessária ou desejável. Afinal de tarefas, é certamente possível lançar um produto de trabalho com bug livre sem executar nenhum trabalho de usabilidade. Mas incorporar princípios de design centralizados pelo usuário pode levar a um produto muito aprimorado em várias áreas.

O melhor motivo para realizar o teste de usabilidade é reduzir o número de chamadas de suporte dos usuários. A má usabilidade é um dos principais motivos pelos quais os usuários chamam linhas de suporte técnico de software, e todos os executivos e gerentes de serviços de informações da empresa de software sabem como o suporte ao produto pode ser caro. Além disso, cobrar os usuários pelo suporte aumenta a insatisfação potencial com o produto. Se os usuários acharem fácil usar seu produto, eles não precisarão chamar o suporte técnico com frequência.

Para o software produzido para uso interno, o melhor motivo para tornar a usabilidade uma parte importante do processo de desenvolvimento é reduzir os custos de treinamento. Um produto altamente utilizável é muito mais fácil para os usuários aprenderem do que um para o qual a usabilidade não era uma prioridade alta. Os usuários aprendem os recursos mais rapidamente e mantêm seu conhecimento mais longo, o que se correlaciona diretamente com os custos e o tempo de treinamento reduzidos.

O teste de usabilidade ajuda a melhorar a aceitação do usuário. Os resultados da aceitação de vários fatores, incluindo a usabilidade, o utilitário e a capacidade de uso. Para produtos de varejo, a aceitação do usuário geralmente se correlaciona diretamente com a repetição da compra ou à lealdade, o que significa que o usuário provavelmente recomendará o produto para outras pessoas. Para aplicativos internos, a aceitação do usuário se correlaciona com uma disposição para usar o software para executar as tarefas para as quais ele foi projetado, o que ajuda a aumentar a produtividade. Aumentar a usabilidade é um dos fatores que podem contribuir para uma maior aceitação do usuário.

A usabilidade pode ajudar a diferenciar seus produtos dos seus concorrentes. Se dois produtos forem substancialmente iguais em Utility, o produto com melhor usabilidade provavelmente será considerado superior. Além disso, as diretrizes de programação de aparência e acompanhamento do Windows têm nivelado o campo de jogo para a interface do usuário básica, de forma que muitos programas que atendem funções semelhantes pareçam e atuem de um modo semelhante. Essas semelhanças significam que pequenas diferenças na usabilidade podem ter um grande efeito na preferência do usuário.

Por fim, cada produto é testado para ser utilizado eventualmente. Os usuários executam testes de usabilidade no produto sempre que o utilizam, e renderizam seus veredicto por meio de seu uso contínuo ou faltam deles. Testar o produto antes de liberá-lo para o mercado pode ajudar a garantir que as experiências dos usuários com o produto sejam positivas.

### <a name="what-does-it-cost"></a>O que ele custa?

Desenvolvedores de software e gerentes de projeto geralmente se preocupam com o início de um processo de Design centralizado pelo usuário e a realização de testes de usabilidade adequados exigirão quantidades inaceitáveis de tempo e dinheiro. A realidade é que o custo em tempo e dinheiro gasto com foco no usuário costuma ser relativamente pequeno e, certamente, quando comparado ao custo de não fazê-lo.

Considere, por exemplo, o custo em tempo e dinheiro de fazer revisões de design atrasadas no ciclo de desenvolvimento, em oposição ao anterior, quando o produto ainda está no quadro de desenho. Aguardar até o período beta para expor os usuários ao produto para fins de teste de usabilidade pode resultar na Dismantling de partes do programa que levaram muito tempo para serem desenvolvidas. E aguardando até que o produto seja realmente lançado e, em seguida, fazer alterações com base em comentários negativos ou dar suporte a um design ruim poderia tornar o custo muito mais alto devido a altos custos de suporte a produtos ou a uma recepção inadequada dos usuários.

Um estudo de usabilidade razoável normalmente pode ser executado em cerca de duas semanas ou menos e pode reduzir muito o tempo e o custo de fazer alterações no final do ciclo de desenvolvimento. O custo de execução de testes variará dependendo da natureza do produto e das partes da interface que são testadas.

Considere o teste de usabilidade como semelhante ao teste de código. Gerentes de projeto bem-sucedidos conta para teste de código ao planejar um projeto de desenvolvimento. Eles não o veem como algo extra que deve ser redirecionado para a agenda e o orçamento do projeto. Em vez disso, os gerentes de projeto aceitam o teste de código como um custo de fazer negócios, pois a alternativa é muito mais cara. O mesmo se aplica ao teste de usabilidade.

### <a name="how-do-i-increase-usability"></a>Como posso aumentar a usabilidade?

Ao ler e compreender a importância da usabilidade, os desenvolvedores de software às vezes são tentados a adicionar usabilidade, como se fosse um ingrediente que pode simplesmente ser adicionado a um produto para torná-lo mais utilizável. Em vez disso, a usabilidade deve fazer parte do próprio processo de design, em vez de uma "coisa" que é adicionada ao processo aqui ou lá. O motivo pelo qual os especialistas em usabilidade se referem ao "foco do usuário" e ao "design centrado no usuário" é que a usabilidade depende de manter as necessidades dos usuários centralizados no processo de design. O design centralizado pelo usuário por necessidade envolve mais do que apenas seguir um conjunto de regras que regem o posicionamento de botões e menus em uma interface. O teste de usabilidade é uma oportunidade de verificar o trabalho de design. Não é uma maneira de "Adicionar" usabilidade a um produto.

Goulden, Boies e Lewis (1991) identificam quatro filosofias importantes do Design centralizado no usuário:

-   Foco antecipado nos usuários.

    Os desenvolvedores devem se concentrar em entender as necessidades dos usuários no início do processo de design.

-   Design integrado.

    Todos os aspectos do design devem evoluir em paralelo, em vez de em sequência. Mantenha o design interno do produto consistente com as necessidades da interface do usuário.

-   Testes antecipados e contínuos.

    A única abordagem viável atualmente para o design de software é uma empírica: o design funciona se os usuários reais decidirem que funciona. A incorporação dos testes de usabilidade durante o processo de desenvolvimento dá aos usuários a oportunidade de fornecer comentários sobre o design antes do lançamento do produto.

-   Design iterativo.

    Grandes problemas geralmente mascaram problemas pequenos. Designers e desenvolvedores devem revisar o design iterativamente por meio de rodadas de teste.

### <a name="why-should-i-involve-users"></a>Por que devo envolver os usuários?

Os desenvolvedores devem reconhecer que não são usuários típicos. Eles têm um conhecimento mais profundo e uma compreensão do sistema que estão desenvolvendo do que o usuário médio já vai. Os aspectos da interface que são inclaros ou confusos para a maioria dos usuários podem, portanto, ser perfeitamente claros para alguém que trabalhou no projeto. Alguns desenvolvedores de software são capazes de entendar com o usuário médio a um certo grau, mas não há nenhum substituto das interações reais dos usuários reais com o produto.

Da mesma forma, concentrando-se nas necessidades típicas dos usuários antecipadamente e revisando o design com base no teste de usuário com frequência, os desenvolvedores de software voltados para o usuário produzem designs melhores e, como resultado, melhores produtos.

Com um design melhor, é melhor aceitar os usuários. O benefício com o software de varejo é óbvio: maior vendas. A aceitação também é importante com o software desenvolvido para uso interno: o maior foco no design centralizado pelo usuário leva a uma maior produtividade e uma necessidade reduzida de suporte. O envolvimento visivelmente dos usuários desde o início do desenvolvimento também demonstra um interesse em suas preocupações e necessidades, o que aumenta sua disposição para ajudar no esforço de desenvolvimento.

### <a name="cant-i-just-follow-guidelines"></a>Não consigo apenas seguir as diretrizes?

A Microsoft desenvolveu um conjunto de diretrizes de interface para a plataforma de computação do Windows para garantir que os programas do Windows tenham uma aparência consistente. Outras empresas desenvolveram diretrizes semelhantes para outras plataformas de computação e especialistas em usabilidade, como o Jakob Nielsen, foram escritos extensivamente na criação de páginas da Web utilizáveis. Com a riqueza de informações disponíveis sobre esses tópicos, às vezes os designers acreditam uma rigorosa adesão a diretrizes e padrões é tudo o que é necessário para produzir produtos utilizáveis.

O problema dessa abordagem é que as diretrizes são inerentemente gerais. As diretrizes devem se aplicar a uma ampla variedade de casos e, portanto, nem sempre prescrevem o melhor curso de ação para o aplicativo específico que está sendo desenvolvido. Aderir a um conjunto de diretrizes bem escrito pode ajudar no design de uma interface consistente, mas eles não podem garantir que ela seja usablility, a menos que seja testada com usuários reais. Ao usar as diretrizes, não as use como um manual, em que as diretrizes apontam o caminho para o melhor de todos os resultados. Dois desenvolvedores podem implementar a mesma diretriz de duas maneiras diferentes, e ambas as implementações podem não ser igualmente apropriadas para a situação. Ocasionalmente, a rigorosa conformidade com as diretrizes pode levar a resultados insatisfatórios ou a conflitos entre as diretrizes. Somente o design centralizado pelo usuário pode ajudar a liberar esses problemas antes que eles se tornem problemas.

Outra maneira de pensar nisso é: deixar o design centralizado pelo usuário ser o arbitrador das decisões de design, não as diretrizes de interface do usuário.

### <a name="do-i-need-to-build-a-usability-lab"></a>É necessário criar um laboratório de usabilidade?

Não presuma que o teste de usabilidade significa a confirmação para um laboratório caro, com câmeras com uso de teto, espelhos unidirecionais e outros ajustes no grupo de foco. Para ter certeza, as empresas que fazem muitos testes geralmente acham conveniente criar laboratórios dedicados, e os consultores de usabilidade geralmente têm uma ampla gama de instalações e equipamentos para oferecer seus clientes. Mas útil, o teste de usabilidade válido pode ser executado em uma variedade de configurações e circunstâncias.

Uma abordagem é simplesmente ter um testador? alguém se inscreveu na execução de estudos de participantes humanos e coletando dados? fique atrás de um usuário enquanto trabalha e observe o usuário executando tarefas. Isso pode ser facilmente executado em uma sala de conferência ou em um escritório. Para obter mais informações sobre o teste por observação, consulte a entrada Dumas e redish em [outros recursos](other-resources.md).

À medida que o teste de usabilidade desenvolve e se torna mais envolvido, equipamentos como uma câmera de vídeo, um espelho unidirecional ou ferramentas que permitem exibir e registrar um monitor de usuário em tempo real podem ser adicionados.

Como alternativa, os testes podem ser terceirizados para os consultores de usabilidade. A seção a seguir contém dicas sobre como encontrar os consultores certos.

### <a name="how-do-i-get-started"></a>Como faço para começar?

Depois de decidir incorporar os princípios de design centrados no usuário no processo de desenvolvimento, você precisará decidir se deseja contratar profissionais de usabilidade ou terceirizar o teste de usabilidade para um fornecedor.

A UPA (Associação de profissionais de usabilidade) tem um guia de fornecedor que pode ajudar a encontrar consultores de usabilidade.

Alguns grupos de consultoria também podem ajudar a configurar os laboratórios de usabilidade ou desenvolver um programa de usabilidade interno para incorporar princípios de usabilidade ao processo de design.

Se contratar profissionais de usabilidade, os fatores humanos e o Ergonomics Society têm um serviço de posicionamento que pode ajudar a encontrar possíveis funcionários. Muitos profissionais de usabilidade também pertencem ao grupo de interesse especial do ACM na interação Computer-Human (SIGCHI) e UPA. Coloque anúncios de emprego em suas publicações ou em suas conferências.

Seja qual for a rota, lembre-se de que esses são serviços de teste. O princípio de que os designers não são usuários típicos também é verdadeiro para profissionais de usabilidade.

Para obter mais informações sobre essas empresas e organizações e saber mais sobre os testes de usabilidade e o design centrado no usuário, consulte [outros recursos](other-resources.md).

 

 




