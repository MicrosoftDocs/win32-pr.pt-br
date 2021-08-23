---
title: Usabilidade no design de software
description: Este tópico apresenta o conceito de usabilidade e por que ele deve ser uma parte importante de qualquer projeto de design de software.
ms.assetid: 912b3224-e36d-44d6-98fa-a7f28e68a2d0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 482fd749a797c58656d987e1bde9e995ac58b8fdf98a6c056cd327e846665749
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589126"
---
# <a name="usability-in-software-design"></a>Usabilidade no design de software

Este tópico apresenta o conceito de usabilidade e por que ele deve ser uma parte importante de qualquer projeto de design de software.

-   [Introdução](#introduction)
-   [Definindo usabilidade](#defining-usability)
    -   [Facilidade de uso](#ease-of-use)
    -   [Usabilidade versus Utilitário](#usability-vs-utility)
    -   [Curtindo-o versus usando-o](#liking-it-vs-using-it)
    -   [Descoberta versus Learning versus eficiência](#discovery-vs-learning-vs-efficiency)
    -   [Os trabalhos não funcionam](#slogans-do-not-work)
-   [Por que a usabilidade é importante?](#why-is-usability-important)
    -   [Por que você deve se importar?](#why-should-you-care)
    -   [Quanto custa?](#what-does-it-cost)
    -   [Como aumentar a usabilidade?](#how-do-i-increase-usability)
    -   [Por que devo envolver usuários?](#why-should-i-involve-users)
    -   [Não é possível seguir apenas as diretrizes?](#cant-i-just-follow-guidelines)
    -   [Preciso criar um laboratório de usabilidade?](#do-i-need-to-build-a-usability-lab)
    -   [Como fazer para Introdução?](#how-do-i-get-started)

## <a name="introduction"></a>Introdução

O termo "usabilidade" no contexto de criação de software representa uma abordagem que coloca o usuário, em vez do sistema, no centro do processo. Essa filosofia, conhecida como design centrado no usuário, incorpora preocupações do usuário e a defesa desde o início do processo de design e determina que as necessidades do usuário devem ser as mais importantes de qualquer decisão de design.

O aspecto mais visível dessa abordagem é o teste de usabilidade, no qual os usuários trabalham e interagem com a interface do produto e compartilham suas exibições e preocupações com os designers e desenvolvedores.

## <a name="defining-usability"></a>Definindo usabilidade

A seção define o que significa usabilidade no contexto do desenvolvimento de software e como ela se relaciona com outros aspectos do processo de desenvolvimento.

### <a name="ease-of-use"></a>Facilidade de uso

Usabilidade é uma medida de como é fácil usar um produto para executar tarefas prescritas. Isso é diferente dos conceitos relacionados de utilitário e de likeability.

### <a name="usability-vs-utility"></a>Usabilidade versus Utilitário

Um atributo central que determina a qualidade de um produto é útil. Isso mede se os usos reais de um produto podem atingir as metas que os designers pretendem atingir. O conceito de utilidade se ramifica ainda mais no utilitário e na usabilidade. Embora esses termos sejam relacionados, eles não são intercambiáveis.

Utilitário refere-se à capacidade do produto de executar uma tarefa ou tarefas. Quanto mais tarefas o produto for projetado para executar, mais utilitário ele terá.

Considere processadores de palavras típicos do Microsoft MS-DOS do final dos anos 1980. Esses programas forneceam muitos recursos poderosos de edição e manipulação de texto, mas exigiam que os usuários aprendem e se lembrarem de dezenas de teclas desastráveis para executar esses programas. Aplicativos como esses podem ser ditos com alto utilitário (eles dão aos usuários a funcionalidade necessária), mas baixa usabilidade (os usuários devem gastar muito tempo e esforço para aprender e usá-los). Por outro lado, um aplicativo simples e bem projetado, como uma calculadora, pode ser muito fácil de usar, mas não oferece muito utilitário.

Ambas as qualidades são necessárias para aceitação do mercado e ambas fazem parte do conceito geral de utilidade. Obviamente, se um programa for altamente usável, mas não fizer nada de valor, ninguém o usará. E os usuários que receberem um programa poderoso que é difícil de usar provavelmente o resistem ou buscarão alternativas.

O teste de usabilidade ajuda a determinar como é fácil para os usuários executarem tarefas específicas. No entanto, ele não ajuda diretamente a determinar se o produto em si tem valor ou utilitário. (Os usuários podem oferecer comentários relacionados ao utilitário durante o teste de usabilidade, mas qualquer comentário deve ser verificado com outros métodos de pesquisa mais robustos.)

### <a name="liking-it-vs-using-it"></a>Curtindo-o versus usando-o

A capacidade de likeability é sempre uma característica desejável em um produto. Se pessoas como o produto, têm maior probabilidade de usá-lo e recomendá-lo a outras pessoas. Mas, assim como com o utilitário , você deve ter cuidado para não confundir a capacidade de likeability com a usabilidade.

As pessoas geralmente gostam de um produto por motivos não relacionados ao utilitário e à usabilidade. Eles podem ser atraindo-se para seu estilo ou para o status que eles acredita que o produto confere a eles. As pessoas normalmente gostam de produtos altamente usáveis, mas você não deve supor que isso significa que um produto bem-parecido é acessível.

Usabilidade é sobre se uma pessoa pode usar o produto para executar as tarefas de que precisa executar. O teste de usabilidade mede principalmente o desempenho, não a preferência. No entanto, os questionários padronizados podem ser usados para medir preferências entre produtos.

### <a name="discovery-vs-learning-vs-efficiency"></a>Descoberta versus Learning versus eficiência

Há muitos aspectos para a usabilidade, mas tradicionalmente o termo se refere especificamente aos atributos de descoberta, aprendizado e eficiência.

-   A descoberta envolve procurar e localizar o recurso de um produto em resposta a uma necessidade específica. O teste de usabilidade pode determinar quanto tempo um usuário leva para encontrar um recurso e quantos erros (opções erradas sobre a localização) o usuário faz ao longo do caminho.
-   Learning refere-se ao processo pelo qual o usuário entende como usar um recurso descoberto para concluir uma tarefa. O teste de usabilidade pode determinar quanto tempo esse processo leva e também quantos erros o usuário faz ao aprender o recurso.
-   Eficiência refere-se ao ponto em que o usuário "doou" o recurso e usa-o sem exigir mais aprendizado. O teste de usabilidade pode determinar quanto tempo leva para o usuário experiente executar as etapas necessárias para usar o recurso.

Esses três aspectos básicos da usabilidade são fortemente influenciados pela natureza da tarefa em questão e pela frequência com que o usuário a executa. Alguns recursos são usados raramente ou são tão complexos que o usuário essencialmente os reaprende toda vez; para esses recursos, a Microsoft geralmente desenvolve assistentes para orientar o usuário durante o processo.

### <a name="slogans-do-not-work"></a>Os trabalhos não funcionam

Os desenvolvedores de software às vezes pensam que simples, como "tornar o produto mais acessível", ajudarão a resolver problemas de usabilidade. Embora uma postura positiva em relação à usabilidade seja importante, somente o teste de usabilidade adequado com usuários comuns, no contexto do produto específico que está sendo criado, pode fornecer aos desenvolvedores as informações necessárias para criar um produto que atenderá às necessidades dos usuários. "Tornar o produto mais acessível" deve ser o lema de todos os desenvolvedores de software, mas só fará sentido se o desenvolvedor souber o que significa usabilidade. Testar com usuários comuns é a maneira mais confiável de descobrir.

## <a name="why-is-usability-important"></a>Por que a usabilidade é importante?

A seção responde a algumas perguntas comuns sobre por que a usabilidade é importante e como incorporar princípios de design centrados no usuário no processo de desenvolvimento.

### <a name="why-should-you-care"></a>Por que você deve se importar?

Se as considerações de usabilidade ainda não foram incorporadas ao processo de design do produto, você pode se perguntar por que isso é necessário ou desejável. No fim das contas, certamente é possível lançar um produto funcionando e sem bugs sem executar nenhum trabalho de usabilidade. Mas incorporar princípios de design centrados no usuário pode levar a um produto muito aprimorado em várias áreas.

O melhor motivo para executar testes de usabilidade é reduzir o número de chamadas de suporte dos usuários. A baixa usabilidade é um dos principais motivos pelos quais os usuários chamam linhas de suporte técnico de software, e cada executivo da empresa de software e gerente de Serviços de Informações sabe o quanto o suporte a produtos pode ser caro. Além disso, cobrar usuários por suporte aumenta a possível insatisfação com o produto. Se os usuários acharem fácil usar seu produto, eles não precisarão chamar suporte técnico com a mesma frequência.

Para software produzido para uso interno, o próximo melhor motivo para tornar a usabilidade uma parte importante do processo de desenvolvimento é reduzir os custos de treinamento. Um produto altamente usável é muito mais fácil para os usuários aprenderem do que um para o qual a usabilidade não era uma prioridade alta. Os usuários aprendem recursos mais rapidamente e mantêm seu conhecimento por mais tempo, o que se correlaciona diretamente à redução dos custos e do tempo de treinamento.

O teste de usabilidade ajuda a melhorar a aceitação do usuário. A aceitação resulta de vários fatores, incluindo usabilidade, utilitário e capacidade de similaridade. Para produtos de varejo, a aceitação do usuário geralmente se correlaciona diretamente à repetição da compra ou à fidelidade, o que significa que é provável que o usuário recomende o produto para outras pessoas. Para aplicativos internos, a aceitação do usuário está relacionada à disposição de usar o software para executar as tarefas para as quais ele foi projetado, o que ajuda a aumentar a produtividade. Aumentar a usabilidade é um dos fatores que podem contribuir para maior aceitação do usuário.

A usabilidade pode ajudar a diferenciar seus produtos daqueles de seus concorrentes. Se dois produtos são substancialmente iguais no utilitário , o produto com melhor usabilidade provavelmente será considerado superior. Além disso, Windows diretrizes de programação de aparência e acompanhamento nivelou o campo de reprodução para a interface básica do usuário, de modo que muitos programas que atendem a funções semelhantes pareçam e atuem um pouco parecidos. Essas semelhanças significam que pequenas diferenças na usabilidade podem ter um grande efeito na preferência do usuário.

Por fim, todos os produtos são testados para usabilidade eventualmente. Os usuários executam testes de usabilidade no produto sempre que o usam e renderizam seus respectivos julgamentos por meio do uso contínuo ou da falta dele. Testar o produto antes de liberá-lo no mercado pode ajudar a garantir que as experiências dos usuários com o produto sejam positivas.

### <a name="what-does-it-cost"></a>Quanto custa?

Desenvolvedores de software e gerentes de projeto geralmente se preocupam que iniciar um processo de design centralizado pelo usuário e executar um teste de usabilidade adequado exigirá quantidades inaceitáveis de tempo e dinheiro. A realidade é que o custo no tempo e o dinheiro gastos concentrando-se no usuário geralmente são relativamente pequenos e, certamente, quando comparados ao custo de não fazer isso.

Considere, por exemplo, o custo no tempo e o dinheiro de fazer revisões de design no final do ciclo de desenvolvimento, em vez de anteriormente, quando o produto ainda está no quadro de desenho. Aguardar até o período beta para expor os usuários ao produto para fins de teste de usabilidade pode resultar na desalocar partes do programa que levaram muito tempo para desenvolver. E esperar até que o produto seja realmente liberado e, em seguida, fazer alterações com base em comentários negativos ou dar suporte a um design ruim pode aumentar o custo de maneira imenssurável devido a altos custos de suporte a produtos ou recepção ruim dos usuários.

Um estudo de usabilidade razoável normalmente pode ser executado em cerca de duas semanas ou menos e pode reduzir consideravelmente o tempo e o custo de fazer alterações tardiamente no ciclo de desenvolvimento. O custo da execução do teste varia dependendo da natureza do produto e das partes da interface que são testadas.

Pense no teste de usabilidade como semelhante ao teste de código. Gerenciadores de projetos bem-sucedidos são responsáveis pelo teste de código ao planejar um projeto de desenvolvimento. Eles não o veem como algo extra que deve ser feito ao agendamento e ao orçamento do projeto. Em vez disso, os gerentes de projeto aceitam o teste de código como um custo de fazer negócios porque a alternativa é muito mais cara. O mesmo se aplica ao teste de usabilidade.

### <a name="how-do-i-increase-usability"></a>Como aumentar a usabilidade?

Ao ler e entender a importância da usabilidade, os desenvolvedores de software às vezes ficam tentados a adicionar usabilidade, como se fosse um ingredientes que pode simplesmente ser adicionado a um produto para torná-lo mais acessível. Em vez disso, a usabilidade deve fazer parte do processo de design em si, em vez de uma "coisa" adicionada ao processo aqui ou ali. O motivo pelo qual os especialistas em usabilidade se referem ao "foco do usuário" e ao "design centrado no usuário" é que a usabilidade depende de manter as necessidades dos usuários centrais para o processo de design. O design centralizado pelo usuário por necessidade envolve mais do que apenas seguir um conjunto de regras que regem o posicionamento do botão e do menu em uma interface. O teste de usabilidade é uma oportunidade para verificar o trabalho de design. Não é uma maneira de "adicionar" usabilidade a um produto.

Gould, Semprees e Lewis (1991) identificam quatro princípios importantes de design centralizado pelo usuário:

-   Foco antecipado nos usuários.

    Os desenvolvedores devem se concentrar em entender as necessidades dos usuários no início do processo de design.

-   Design integrado.

    Todos os aspectos do design devem evoluir em paralelo, em vez de em sequência. Mantenha o design interno do produto consistente com as necessidades da interface do usuário.

-   Teste antecipado e contínuo.

    A única abordagem atualmente viável para o design de software é empírica: o design funcionará se os usuários reais decidirem que ele funciona. Incorporar testes de usabilidade em todo o processo de desenvolvimento oferece aos usuários a oportunidade de fornecer comentários sobre o design antes que o produto seja lançado.

-   Design iterativo.

    Grandes problemas geralmente mascaram pequenos problemas. Designers e desenvolvedores devem revisar o design iterativamente por meio de rodadas de teste.

### <a name="why-should-i-involve-users"></a>Por que devo envolver usuários?

Os desenvolvedores devem reconhecer que eles não são usuários típicos. Eles têm mais conhecimento e compreensão sobre o sistema que estão desenvolvendo do que a média de usuários. Aspectos da interface que não são claros ou confusos para a maioria dos usuários podem, portanto, ser perfeitamente claros para alguém que trabalhou no projeto. Alguns desenvolvedores de software podem se empatia com o usuário médio até certo ponto, mas não há substituto para as interações reais de usuários reais com o produto.

Da mesma forma, ao se concentrar nas necessidades típicas dos usuários no início e revisar o design com base no teste do usuário com frequência, os desenvolvedores de software voltados para o usuário produzem designs melhores e, como resultado, produtos melhores.

Com um design melhor, vem uma melhor aceitação dos usuários. O benefício com o software de varejo é óbvio: aumento das vendas. A aceitação também é importante com o software desenvolvido para uso interno: o aumento do foco no design centralizado pelo usuário leva ao aumento da produtividade e à menor necessidade de suporte. Envolver usuários visivelmente desde o início do desenvolvimento também demonstra interesse em suas preocupações e necessidades, o que aumenta sua disposição para ajudar no esforço de desenvolvimento.

### <a name="cant-i-just-follow-guidelines"></a>Não é possível seguir apenas as diretrizes?

A Microsoft desenvolveu um conjunto de diretrizes de interface para a plataforma Windows de computação para garantir que Windows programas tenham uma aparência consistente. Outras empresas desenvolveram diretrizes semelhantes para outras plataformas de computação, e especialistas em usabilidade, como o Sempre, escreveram extensivamente sobre a criação de páginas da Web usáveis. Com a grande quantidade de informações disponíveis nesses tópicos, os designers às vezes acredita que a adesão rigorosa às diretrizes e padrões é tudo o que é necessário para produzir produtos que podem ser usáveis.

O problema com essa abordagem é que as diretrizes são inerentemente gerais. As diretrizes devem se aplicar a uma ampla variedade de casos e, portanto, nem sempre preveem o melhor curso de ação para o aplicativo específico que está sendo desenvolvido. A aderindo a um conjunto bem escrito de diretrizes pode ajudar no design de uma interface consistente, mas eles não podem garantir sua responsabilidade, a menos que ele seja testado com usuários reais. Ao usar diretrizes, não as use como um guia em que as diretrizes apontam para o melhor de todos os resultados. Dois desenvolvedores podem implementar a mesma diretriz de duas maneiras diferentes, e ambas as implementações podem não ser igualmente apropriadas para a situação. Ocasionalmente, a adesão rigorosa às diretrizes pode levar a resultados ruins ou a conflitos entre diretrizes. Somente o design centralizado pelo usuário pode ajudar a liberar esses problemas antes que eles se tornem problemas.

Outra maneira de pensar sobre isso é: Permitir que o design centralizado pelo usuário seja o arbitr de decisões de design, não as diretrizes de interface do usuário.

### <a name="do-i-need-to-build-a-usability-lab"></a>Preciso criar um laboratório de usabilidade?

Não suponha que o teste de usabilidade significa se comprometer com um laboratório caro, com câmeras montadas no limite, espelhos de ida e outras interceptações de grupo de foco. Para ter certeza, as empresas que fazem muitos testes geralmente acham conveniente criar laboratórios dedicados, e consultores de usabilidade geralmente têm uma ampla variedade de instalações e equipamentos para oferecer aos clientes. Porém, testes de usabilidade válidos e úteis podem ser executados em uma variedade de configurações e circunstâncias.

Uma abordagem é simplesmente ter um testador?, alguém verificado na execução de estudos de participante humanos e na coleta de dados?, ficar atrás de um usuário enquanto trabalha e observar o usuário executando tarefas. Isso pode ser feito facilmente em uma sala de conferência ou em um escritório. Para obter mais informações sobre como testar por observação, consulte a entrada Dumas e Redish em [Outros Recursos](other-resources.md).

À medida que o teste de usabilidade se desenvolve e se torna mais envolvido, equipamentos como uma câmera de vídeo, um espelho único ou ferramentas que permitem que você veja e grave o monitor de um usuário em tempo real podem ser adicionados.

Como alternativa, o teste pode ser terceirizado para consultores de usabilidade. A seção a seguir contém dicas sobre como encontrar os consultores certos.

### <a name="how-do-i-get-started"></a>Como fazer para Introdução?

Depois de decidir incorporar princípios de design centrados no usuário no processo de desenvolvimento, você precisará decidir se contrata profissionais de usabilidade ou terceirizar os testes de usabilidade para um fornecedor.

A UPA (Associação de Profissionais de Usabilidade) tem um guia de fornecedor que pode ajudar a encontrar consultores de usabilidade.

Alguns grupos de consultoria também podem ajudar a configurar laboratórios de usabilidade ou desenvolver um programa de usabilidade interno para incorporar princípios de usabilidade ao processo de design.

Se você contrata profissionais de usabilidade, a Human Factors e a Society Demónomics têm um serviço de posicionamento que pode ajudar a encontrar possíveis funcionários. Muitos profissionais de usabilidade também pertencem ao Grupo de Interesse Especial do ACM no SIGCHI (Interação Computer-Human) e UPA. Coloque anúncios de emprego em suas publicações ou em suas conferências.

Seja qual for a rota que for tomada, lembre-se de que esses são serviços de teste. O princípio de que os designers não são usuários típicos também é verdadeiro para profissionais de usabilidade.

Para obter mais informações sobre essas empresas e organizações e para saber mais sobre o teste de usabilidade e o design centrado no usuário, consulte [Outros recursos.](other-resources.md)

 

 




