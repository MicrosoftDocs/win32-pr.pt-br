---
title: Criando uma interface do usuário
description: Esta seção descreve detalhadamente algumas das tarefas associadas à criação de uma interface do usuário para um aplicativo do Windows.
ms.assetid: 22deda0c-bf03-4fcd-9cc9-6381b601c152
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97d5027baf7276b1353e03254478545e554daa5e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454218"
---
# <a name="designing-a-user-interface"></a>Criando uma interface do usuário

Esta seção descreve detalhadamente algumas das tarefas associadas à criação de uma interface do usuário para um aplicativo do Windows.

-   [Introdução](#introduction)
-   [Requisitos funcionais](#functional-requirements)
-   [Análise do usuário](#user-analysis)
    -   [Instruções do problema](#problem-statements)
    -   [Suas](#priorities)
-   [Design conceitual](#conceptual-design)
-   [Design lógico](#logical-design)
-   [Design físico](#physical-design)

## <a name="introduction"></a>Introdução

O design da interface do usuário pode ser dividido em três elementos essenciais: funcionalidade, estética e desempenho.

Com mais frequência do que não, o foco principal durante o desenvolvimento de aplicativos é a funcionalidade. O aplicativo pode ser usado? Ele permite que os usuários concluam tarefas? No entanto, a funcionalidade é apenas uma parte da história.

Estética descrevem como as coisas são mostradas e apresentadas, o estilo no qual as coisas são comunicadas ao usuário. As estética são muito subjetivas e muito mais difíceis de quantificar do que os requisitos funcionais e as métricas de desempenho. As estética normalmente se destinam a escolhas simples, como as cores se complementam ou como os elementos da interface do usuário transmitem seu significado – isso geralmente afeta a maneira como uma pessoa se sente sobre algo e influencia o quão bem-sucedido eles estão usando.

O desempenho é medido não apenas na velocidade, mas também na confiabilidade. Se um aplicativo parecer bem, for fácil de usar, mas falhar repetidamente, provavelmente não será muito bem sucedido. O aplicativo precisa fornecer ao usuário total confiança em sua confiabilidade.

Veja a seguir algumas tarefas da fase de design que podem contribuir com uma interface do usuário bem-sucedida para um aplicativo do Windows.

## <a name="functional-requirements"></a>Requisitos funcionais

Considere as seguintes sugestões no início da fase de design para otimizar a experiência do usuário em todo o público mais amplo possível:

-   Siga as diretrizes de design da interface do usuário.

    Familiarizar-se com as [diretrizes de interação da experiência do usuário do Windows](../uxguide/guidelines.md) e se referir a elas com frequência à medida que o design, a implementação e o teste da interface do usuário do aplicativo progride.

-   Verifique se a interface do usuário está acessível.

    Não se esqueça de integrar a acessibilidade ao design da interface do usuário desde o início do ciclo de vida do produto. A acessibilidade modernização pode ser extremamente dispendiosa porque parte do desenvolvimento de acessibilidade requer atenção no nível de arquitetura. Para obter mais informações, baixe o [software de engenharia para o ebook de acessibilidade](https://www.microsoft.com/download/details.aspx?id=19262).

-   Suporte ao Marketplace internacional.

    O Windows inclui tecnologias que habilitam o suporte para várias culturas e linguagens escritas em um aplicativo do Windows. Se o aplicativo estiver direcionando para o Marketplace internacional, é importante incluir o suporte à internacionalização no design da interface do usuário desde o início do projeto. Para obter mais informações, consulte [internacionalização para aplicativos do Windows](../intl/international-support.md).

## <a name="user-analysis"></a>Análise do usuário

Uma etapa crítica na criação de uma interface bem-sucedida é obter um entendimento básico do que os usuários precisam e desejarem de um aplicativo antes de escrever qualquer código. Lembre-se de que os usuários potenciais de um aplicativo já estão fazendo seu trabalho de alguma forma, e as ferramentas e os processos existentes devem ser compreendidos o máximo possível. Não projete sem considerar completamente esses problemas.

A abordagem mais simples e informal é conversar com os usuários pretendidos do produto. Obtenha informações diretamente da fonte – Evite usar gerentes ou executivos como proxies para os consumidores reais. Considere que os pequenos grupos de desenvolvedores e gerentes de programas paguem visitas informais aos usuários em seus locais de trabalho em que há uma oportunidade de discutir como eles funcionam e reunir detalhes dos problemas que enfrentam com suas ferramentas atuais.

Lembre-se, não faça perguntas de entrelinha ou tendência, pois isso afetará diretamente a qualidade e a validade dos comentários do usuário. Tenha em mente o seguinte ao redigir perguntas durante esta fase:

-   Quem são nossos usuários? Quais habilidades e conhecimento eles têm?
-   Quais fontes de dados diferentes podemos usar para entender sua experiência?
-   Quais metas e tarefas usarão nosso produto para serem concluídas?
-   Quais são as suposições que estamos fazendo e como podemos verificá-las?
-   Quais fontes de dados temos? (Estudos de usabilidade e avaliações heurísticas são bons lugares para começar.)

### <a name="problem-statements"></a>Instruções do problema

Depois que todos os comentários do usuário forem coletados, analise-os e excole-os em problemas e requisitos relacionados. Tente evitar pensar em soluções neste ponto. Verifique se os problemas estão totalmente identificados, não apenas os sintomas.

Geralmente, é útil compor uma lista de instruções de problema de uma frase (da perspectiva dos usuários) para cada problema ou requisito. Por exemplo, "redimensionar largura da caixa de edição para 15 caracteres" não é um problema. Mas "é muito difícil digitar em termos de pesquisa longos" é uma declaração de problema válida. A diferença é dramática. Tente não definir a solução e o problema ao mesmo tempo: geralmente o problema real é perdido. Neste exemplo, pode haver muitas outras maneiras de resolver o problema de termos de pesquisa, incluindo a alteração do tamanho da caixa de edição. Sempre mantenha as soluções alternativas em mente.

A seguir estão exemplos adicionais de instruções de problema:

-   É difícil navegar de uma seção do site para outra.
-   Os usuários precisam esperar muito tempo para que o software seja carregado.
-   Nossas mensagens de erro de segurança são difíceis de entender.
-   A página de registro tem muitas perguntas e os usuários costumam abandonar isso.
-   Encontrar um produto específico no índice do site é muito difícil de ser concluído.

Se as instruções do problema forem amplas o suficiente, provavelmente haverá muitas maneiras inovadoras e criativas de solucioná-las.

### <a name="priorities"></a>Prioridades

O ato de fazer uma lista de itens e classificar por prioridade, define uma versão. Sem prioridades claras, as equipes podem combater e argumentar sobre as coisas que devem ser feitas e quais coisas devem ser recortadas. O trabalho envolvido na definição de prioridades deve ser mais fácil com a pesquisa concluída, mas é sempre um desafio.

A definição de prioridades requer a capacidade de avaliar pelo menos três critérios: agenda, equipe e negócios. Pode haver um conjunto de agendamento predefinido para o projeto, o que limita o tamanho e a escala do trabalho que pode ser feito. Um problema que provavelmente exigirá a regravação da metade da base de código não deve ser tentado durante um pequeno ciclo de lançamento.

A composição e a natureza de uma equipe definem que tipos de trabalho podem ser feitos. Que outros compromissos a equipe tem? Há um designer ou engenheiro de usabilidade na equipe? Que habilidades com o design da Web ou da interface do usuário a equipe tem? Por fim, e o mais importante são as considerações de negócios. Quais são as metas de receita para este projeto? Quem são os concorrentes? Quais são as vantagens de resolver determinados problemas? Quais parcerias podem ser forjadas? Quaisquer outras considerações também devem ser identificadas antes de priorizar a lista.

Uma vez priorizado, a lista de instruções de problema define a direção do produto e garante que o desenvolvimento seja direcionado nas áreas certas.

## <a name="conceptual-design"></a>Design conceitual

Normalmente, a interface do usuário não é abordada na fase de design conceitual. No entanto, essa fase requer um modelo de negócios completo com perfis de usuário e cenários de uso completos, que são imperativos para uma experiência de usuário bem-sucedida.

## <a name="logical-design"></a>Design lógico

A fase de design lógico é quando os protótipos iniciais que oferecem suporte ao design conceitual são desenvolvidos.

As tecnologias específicas de hardware e software a serem usadas durante o desenvolvimento também são identificadas nesta fase, o que pode determinar os recursos da interface do usuário no produto final. Para obter mais informações, consulte [tecnologias de interface do usuário](user-interface-technologies-for-windows-applications.md).

Além das ferramentas de desenvolvimento, os vários requisitos de hardware e os fatores forma que devem ser direcionados pelo aplicativo devem ser identificados.

## <a name="physical-design"></a>Design físico

A fase de design físico determina como um design de interface do usuário deve ser implementado para os fatores de forma e de hardware específicos que foram identificados no design lógico.

É nessa fase que limitações de fator de forma ou de hardware podem introduzir restrições inesperadas na interface do usuário que exigem refinamentos significativos no design.

 

 