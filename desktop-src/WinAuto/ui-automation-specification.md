---
title: Especificação de automação da interface do usuário
description: Este tópico fornece uma visão geral da especificação de automação da interface do usuário da Microsoft, que constitui a base da implementação do Windows da automação da interface do usuário.
ms.assetid: 45160767-09b0-4fd1-bd73-bc5ac0e6f75e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d3cbb7ed2caa49e855b25f749820de8cf24f1e9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007791"
---
# <a name="ui-automation-specification"></a>Especificação de automação da interface do usuário

Este tópico fornece uma visão geral da especificação de automação da interface do usuário da Microsoft, que constitui a base da implementação do Windows da automação da interface do usuário. A especificação de automação da interface do usuário pode ter suporte em outras plataformas que não sejam o Microsoft Windows. Para obter mais informações, consulte [especificação de automação da interface do usuário](./uiauto-specandcommunitypromise.md)

Este tópico contém as seguintes seções:

-   [Introducton](#introducton)
-   [Elementos de automação da interface do usuário](#ui-automation-elements)
-   [Árvore de automação da interface do usuário](#ui-automation-tree)
-   [Propriedades de automação da interface do usuário](#ui-automation-properties)
-   [Padrões de controle da automação da interface do usuário](#ui-automation-control-patterns)
-   [Tipos de controle da automação da interface do usuário](#ui-automation-control-types)
-   [Eventos de automação da interface do usuário](#ui-automation-events)
-   [Tópicos relacionados](#related-topics)

## <a name="introducton"></a>Introducton

A especificação de automação da interface do usuário fornece acesso de programação flexível aos elementos da interface do usuário do Windows, permitindo que os produtos de tecnologia assistencial, como leitores de tela, forneçam informações sobre a interface do usuário aos usuários finais e manipulem a interface do usuário por meio de uma entrada padrão.

A automação da interface do usuário é mais ampla no escopo do que apenas uma definição de interface. Ele fornece:

-   Um modelo de objeto e funções que tornam mais fácil para os aplicativos cliente receberem eventos, recuperarem valores de propriedade e manipular elementos da interface do usuário.
-   Uma infra-estrutura básica para localizar e buscar limites de processo.
-   Um conjunto de interfaces para provedores para expressar a estrutura de árvore, as propriedades gerais e a funcionalidade dos elementos da interface do usuário.
-   Uma propriedade de "tipo de controle" que permite que clientes e provedores indiquem claramente as propriedades, a funcionalidade e a estrutura comuns de um objeto de interface do usuário.

A automação da interface do usuário aprimora o Microsoft Acessibilidade Ativa:

-   Habilitando clientes de fora de processo eficientes, enquanto continua a permitir o acesso em processo.
-   Expor mais informações sobre a interface do usuário de forma a permitir que os clientes estejam fora do processo.
-   Coexistente com e aproveitando o Microsoft Acessibilidade Ativa sem herdar suas limitações. Para obter mais informações, consulte [Microsoft acessibilidade ativa e automação de interface do usuário em comparação](microsoft-active-accessibility-and-ui-automation-compared.md).
-   Fornecer uma alternativa ao [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) que seja simples de implementar.

A implementação da especificação de automação da interface do usuário no Windows apresenta recursos baseados em Component Object Model (COM) e interfaces gerenciadas.

## <a name="ui-automation-elements"></a>Elementos de automação da interface do usuário

A automação da interface do usuário expõe todas as partes da interface do usuário para aplicativos cliente como um *elemento de automação*. Os provedores fornecem valores de propriedade para cada elemento. Os elementos são expostos como uma estrutura de árvore, com a área de trabalho como o elemento raiz.

Elementos de automação expõem propriedades comuns dos elementos da interface do usuário que eles representam. Uma dessas propriedades é o tipo de controle, que descreve sua aparência e funcionalidade básicas (por exemplo, um botão ou uma caixa de seleção).

## <a name="ui-automation-tree"></a>Árvore de automação da interface do usuário

A árvore de automação da interface do usuário representa toda a interface do usuário: o elemento raiz é a área de trabalho atual e os elementos filho são janelas de aplicativo. Cada um desses elementos filho pode conter elementos que representam menus, botões, barras de ferramentas e assim por diante. Esses elementos, por sua vez, podem conter elementos como itens de lista, como mostra a ilustração a seguir.

![captura de tela mostrando a árvore de automação da interface do usuário](images/uiatree.gif)

Lembre-se de que a ordem dos irmãos na árvore de automação da interface do usuário é muito importante. Os objetos que estão próximos entre si também devem ser próximos um do outro na árvore de automação da interface do usuário.

Provedores de automação de interface do usuário para um controle específico dão suporte à navegação entre os elementos filho desse controle. No entanto, os provedores não se preocupam com a navegação entre essas subárvores de controle. Isso é gerenciado pelo núcleo de automação da interface do usuário, usando informações dos provedores de janela padrão.

Para ajudar os clientes a processar informações da interface do usuário com mais eficiência, a estrutura dá suporte a exibições alternativas da árvore de automação: exibição bruta, exibição de controle e exibição de conteúdo. Como mostra a tabela a seguir, o tipo de filtragem determina as exibições e o cliente define o escopo de uma exibição.



| Árvore de automação | Descrição                                                                                                             |
|-----------------|-------------------------------------------------------------------------------------------------------------------------|
| Exibição bruta        | A árvore completa de objetos de elementos de automação para os quais a área de trabalho é a raiz.                                          |
| Exibição de controle    | Um subconjunto do modo de exibição bruto que é mapeado de forma mais próxima à estrutura da interface do usuário quando ele a percebe.                                |
| Exibição de conteúdo    | Um subconjunto do modo de exibição de controle que contém o conteúdo mais relevante para o usuário, como os valores em uma caixa de combinação suspensa. |



 

Para obter mais informações, consulte [visão geral da árvore de automação da interface do usuário](uiauto-treeoverview.md).

## <a name="ui-automation-properties"></a>Propriedades de automação da interface do usuário

A especificação de automação da interface do usuário define dois tipos de propriedades: propriedades do elemento Automation e propriedades de padrão de controle. As propriedades do elemento Automation aplicam-se à maioria dos controles, fornecendo informações fundamentais sobre o elemento, como seu nome. As propriedades de padrão de controle se aplicam a padrões de controle, que são descritos a seguir.

Ao contrário do Microsoft Acessibilidade Ativa, cada propriedade de automação da interface do usuário é identificada por um GUID e um nome programático, o que torna as novas propriedades mais fáceis de introduzir.

Para obter mais informações, consulte [visão geral das propriedades de automação da interface do usuário](uiauto-propertiesoverview.md).

## <a name="ui-automation-control-patterns"></a>Padrões de controle de automação da interface do usuário

Um padrão de controle descreve um aspecto específico da funcionalidade de um elemento de automação. Por exemplo, um simples controle "clicável" como um botão ou hiperlink deve dar suporte ao padrão de controle Invoke para representar a ação "click".

Cada padrão de controle é uma representação canônica de possíveis recursos e funções da interface do usuário. A implementação atual da automação da interface do usuário define 22 padrões de controle. A API de automação do Windows também pode oferecer suporte a padrões de controle personalizados. Ao contrário das propriedades de função ou estado do Microsoft Acessibilidade Ativa, um elemento Automation pode dar suporte a vários padrões de controle de automação da interface do usuário.

Para obter mais informações, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).

## <a name="ui-automation-control-types"></a>Tipos de controle de automação de interface do usuário

Um tipo de controle é uma propriedade de elemento de automação que especifica um controle bem conhecido que o elemento representa. Atualmente, a automação da interface do usuário define 38 tipos de controle, incluindo botão, caixa de seleção, ComboBox, DataGrid, documento, hiperlink, imagem, dica de ferramenta, árvore e janela.

Antes de você poder atribuir um tipo de controle a um elemento, o elemento precisa atender a determinadas condições, incluindo uma estrutura de árvore de automação específica, valores de propriedade, padrões de controle e eventos. No entanto, você não está limitado a esses. Você pode estender um controle com padrões e propriedades personalizadas, bem como com os predefinidos.

O número total de tipos de controle predefinidos é significativamente menor do que as [funções de objeto](object-roles.md)do Microsoft acessibilidade ativa, pois os tipos de controle de automação da interface do usuário podem ser combinados para expressar um conjunto maior de recursos enquanto as funções do Microsoft acessibilidade ativa não podem.

Para obter mais informações, consulte [visão geral de tipos de controle de automação da interface do usuário](uiauto-controltypesoverview.md).

## <a name="ui-automation-events"></a>Eventos de automação da interface do usuário

Eventos de automação da interface do usuário notificam aplicativos sobre alterações e ações executadas com elementos de automação. Há quatro tipos diferentes de eventos de automação de interface do usuário, e eles não significam necessariamente que o estado visual da interface do usuário foi alterado. O modelo de evento de automação da interface do usuário é independente da estrutura [WinEvent](winevents-infrastructure.md) no Windows, embora a API de automação do Windows torne os eventos de automação da interface do usuário interoperáveis com o Microsoft acessibilidade ativa Framework.

Para obter mais informações, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).

## <a name="related-topics"></a>Tópicos relacionados

[Especificação de automação da IU](./uiauto-specandcommunitypromise.md), [visão geral da API de automação do Windows](windows-automation-api-overview.md)