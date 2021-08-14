---
title: Projetando um Interface do Usuário
description: Esta seção descreve detalhadamente algumas das tarefas associadas à criação de uma interface do usuário para um Windows aplicativo.
ms.assetid: 22deda0c-bf03-4fcd-9cc9-6381b601c152
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 914f8a2bf2afb532e3deed8876ce0ddea0fe71a0e8ad5457e5967e5f48eeb2c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119440306"
---
# <a name="designing-a-user-interface"></a>Projetando um Interface do Usuário

Esta seção descreve detalhadamente algumas das tarefas associadas à criação de uma interface do usuário para um Windows aplicativo.

-   [Introdução](#introduction)
-   [Requisitos funcionais](#functional-requirements)
-   [Análise de usuário](#user-analysis)
    -   [Instruções de problema](#problem-statements)
    -   [Prioridades](#priorities)
-   [Design conceitual](#conceptual-design)
-   [Design lógico](#logical-design)
-   [Design físico](#physical-design)

## <a name="introduction"></a>Introdução

O design da interface do usuário pode ser dividido em três elementos essenciais: funcionalidade, filosofia e desempenho.

Com mais frequência do que não, o foco principal durante o desenvolvimento de aplicativos é a funcionalidade. O aplicativo é acessível? Ele permite que os usuários concluam tarefas? No entanto, a funcionalidade é apenas uma parte da história.

Os padrões descrevem como as coisas são mostradas e apresentadas, o estilo no qual as coisas são comunicadas ao usuário. Os padrões são muito subjetivos e muito mais difíceis de quantificar do que os requisitos funcionais e as métricas de desempenho. Normalmente, as alternativas são voltadas para escolhas simples – como as cores se complementam ou como os elementos da interface do usuário transmitem seu significado – que geralmente afetam a maneira como uma pessoa se preocupa com algo e influenciam o quão bem-sucedida ela está usando.

O desempenho é medido não apenas pela velocidade, mas também pela confiabilidade. Se um aplicativo parecer ótimo, for fácil de usar, mas falhar repetidamente, provavelmente não será muito bem-sucedido. O aplicativo precisa fornecer a um usuário confiança total em sua confiabilidade.

A seguir estão algumas tarefas de fase de design que podem contribuir para uma interface do usuário bem-sucedida para um Windows aplicativo.

## <a name="functional-requirements"></a>Requisitos funcionais

Considere as seguintes sugestões no início da fase de design para otimizar a experiência do usuário em todo o público-alvo mais amplo possível:

-   Siga as diretrizes de design da interface do usuário.

    Familiarizar-se com as [Windows](../uxguide/guidelines.md) de Interação do Usuário e refere-se a elas com frequência à medida que o design, a implementação e o teste da interface do usuário do aplicativo progridem.

-   Verifique se a interface do usuário está acessível.

    Certifique-se de integrar a acessibilidade ao design da interface do usuário desde o início do ciclo de vida do produto. A retroajuste da acessibilidade pode ser extremamente cara porque parte do desenvolvimento de acessibilidade requer atenção no nível da arquitetura. Para obter mais informações, baixe o [eBook Software de Engenharia para Acessibilidade](https://www.microsoft.com/download/details.aspx?id=19262).

-   Dar suporte ao marketplace internacional.

    Windows inclui tecnologias que habilitam o suporte para muitas culturas e linguagens escritas em um Windows aplicativo. Se o aplicativo estiver direcionando o marketplace internacional, é importante incluir o suporte à internacionalização no design da interface do usuário desde o início do projeto. Para obter mais informações, consulte [Internationalization for Windows Applications](../intl/international-support.md).

## <a name="user-analysis"></a>Análise de usuário

Uma etapa crítica na criação de uma interface bem-sucedida é obter uma compreensão básica do que os usuários precisam e querem de um aplicativo antes de escrever qualquer código. Lembre-se de que os possíveis usuários de um aplicativo já estão fazendo seu trabalho de alguma forma e ferramentas e processos existentes devem ser compreendidos da maneira mais completa possível. Não projete sem considerar totalmente esses problemas.

A abordagem mais simples e informal é conversar com os usuários pretendido do produto. Obter informações diretamente da fonte – evite usar gerentes ou executivos como proxies para consumidores reais. Considere fazer com que pequenos grupos de desenvolvedores e gerentes de programas paguem visitas informais aos usuários em seus locais de trabalho, em que há uma oportunidade de discutir como eles funcionam e coletar detalhes dos problemas que eles enfrentam com suas ferramentas atuais.

Lembre-se de não fazer perguntas principais ou preconceituosas, pois isso afetará diretamente a qualidade e a validade dos comentários do usuário. Lembre-se do seguinte ao compor perguntas durante essa fase:

-   Who são nossos usuários? Quais habilidades e conhecimento eles têm?
-   Quais diferentes fontes de dados podemos usar para entender sua experiência?
-   Quais metas e tarefas eles usarão nosso produto para concluir?
-   Quais suposições estamos fazendo e como podemos verificá-las?
-   Quais fontes de dados temos? (Estudos de usabilidade e avaliações heurísticas são bons lugares para começar.)

### <a name="problem-statements"></a>Instruções de problema

Depois que todos os comentários do usuário foram coletados, analise-os e o esvaia em problemas e requisitos relacionados. Tente evitar pensar em soluções neste ponto. Certifique-se de que os problemas sejam totalmente identificados, não apenas os sintomas.

Geralmente, é útil compor uma lista de instruções de problema de uma frase (da perspectiva dos usuários) para cada problema ou requisito. Por exemplo, "Resize edit box width to 15 characters" não é um problema. Mas "É muito difícil digitar em termos de pesquisa longos" é uma instrução de problema válida. A diferença é significativa. Tente não definir a solução e o problema ao mesmo tempo: geralmente, o problema real é perdido. Neste exemplo, pode haver muitas outras maneiras de resolver o problema dos termos de pesquisa, incluindo a alteração do tamanho da caixa de edição. Sempre tenha em mente soluções alternativas.

Veja a seguir exemplos adicionais de instruções de problema:

-   É difícil navegar de uma seção do site para outra.
-   Os usuários têm que aguardar muito tempo para que o software seja carregado.
-   Nossas mensagens de erro de segurança são difíceis de entender.
-   A página de registro tem muitas perguntas e os usuários geralmente a abandonarão.
-   Encontrar um produto específico no índice do site é muito difícil de concluir.

Se as instruções do problema são amplas o suficiente, provavelmente haverá muitas maneiras inovadoras e inovadoras de resolvê-las.

### <a name="priorities"></a>Prioridades

O ato de pegar uma lista de itens e classifica-los por prioridade define uma versão. Sem prioridades claras, as equipes podem discutir e discutir o que deve ser feito e quais coisas devem ser cortadas. O trabalho envolvido na definição de prioridades deve ser mais fácil com a conclusão da pesquisa, mas é sempre um desafio.

Definir prioridades requer a capacidade de avaliar pelo menos três critérios: agendamento, equipe e negócios. Pode haver um conjunto de agendamento predefinido para o projeto, que limita o tamanho e a escala do trabalho que pode ser feito. Um problema que provavelmente exigirá a reescrita de metade da base de código não deve ser tentado durante um pequeno ciclo de lançamento.

A natureza e a natureza de uma equipe definem quais tipos de trabalho podem ser feitos. Quais outros compromissos a equipe tem? Há um designer ou engenheiro de usabilidade na equipe? Quais habilidades com design da Web ou da interface do usuário a equipe tem? Por fim, e o mais importante, são considerações de negócios. Quais são as metas de receita para este projeto? Who os concorrentes? Quais são as vantagens de resolver determinados problemas? Quais parcerias podem ser forjados? Outras considerações também devem ser identificadas antes de priorizar a lista.

Depois de priorizada, a lista de instruções de problema define a direção do produto e garante que o desenvolvimento seja direcionado às áreas certas.

## <a name="conceptual-design"></a>Design conceitual

Normalmente, a interface do usuário não é abordada na fase de design conceitual. No entanto, essa fase requer um modelo de negócios completo com perfis de usuário completos e cenários de uso que são imperativos para uma experiência de usuário bem-sucedida.

## <a name="logical-design"></a>Design lógico

A fase de design lógico é quando os protótipos iniciais que suportam o design conceitual são desenvolvidos.

As tecnologias de hardware e software específicas a serem usadas durante o desenvolvimento também são identificadas nesta fase, que pode determinar os recursos da interface do usuário no produto final. Para obter mais informações, consulte [Interface do Usuário Technologies](user-interface-technologies-for-windows-applications.md).

Além das ferramentas de desenvolvimento, os vários requisitos de hardware e fatores forma que devem ser direcionados pelo aplicativo devem ser identificados.

## <a name="physical-design"></a>Design físico

A fase de design físico determina como um design de interface do usuário deve ser implementado para os fatores de hardware e forma específicos que foram identificados no design lógico.

É durante essa fase que as limitações de fator de hardware ou forma podem introduzir restrições inesperadas na interface do usuário que exigem refinamentos significativos para o design.

 

 