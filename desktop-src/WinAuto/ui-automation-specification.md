---
title: Especificação Automação da Interface do Usuário dados
description: Este tópico fornece uma visão geral da Especificação Automação da Interface do Usuário Microsoft, que forma a base da implementação Windows de Automação da Interface do Usuário.
ms.assetid: 45160767-09b0-4fd1-bd73-bc5ac0e6f75e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fc07b70128a401d48813ded68c31dfcfca5bb5a49d2ca46683e9a902af003ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118325088"
---
# <a name="ui-automation-specification"></a>Especificação Automação da Interface do Usuário dados

Este tópico fornece uma visão geral da Especificação Automação da Interface do Usuário Microsoft, que forma a base da implementação Windows de Automação da Interface do Usuário. A especificação Automação da Interface do Usuário pode ser suportada em plataformas diferentes do Microsoft Windows. Para obter mais informações, consulte [Automação da Interface do Usuário Especificação](./uiauto-specandcommunitypromise.md)

Este tópico contém as seguintes seções:

-   [Introducton](#introducton)
-   [Automação da Interface do Usuário elementos](#ui-automation-elements)
-   [Automação da Interface do Usuário árvore](#ui-automation-tree)
-   [Automação da Interface do Usuário propriedades](#ui-automation-properties)
-   [Padrões de controle da automação da interface do usuário](#ui-automation-control-patterns)
-   [Tipos de controle da automação da interface do usuário](#ui-automation-control-types)
-   [Automação da Interface do Usuário eventos](#ui-automation-events)
-   [Tópicos relacionados](#related-topics)

## <a name="introducton"></a>Introducton

A Especificação Automação da Interface do Usuário fornece acesso programático flexível aos elementos da interface do usuário na área de trabalho do Windows, permitindo que produtos de tecnologia adaptativa, como leitores de tela, forneçam informações sobre a interface do usuário para os usuários finais e manipulem a interface do usuário por meios diferentes da entrada padrão.

Automação da Interface do Usuário é mais amplo no escopo do que apenas uma definição de interface. Ele fornece:

-   Um modelo de objeto e funções que facilitam para aplicativos cliente receber eventos, recuperar valores de propriedade e manipular elementos da interface do usuário.
-   Uma infraestrutura principal para localizar e buscar entre limites de processo.
-   Um conjunto de interfaces para provedores expressarem a estrutura de árvore, as propriedades gerais e a funcionalidade dos elementos da interface do usuário.
-   Uma propriedade de "tipo de controle" que permite que clientes e provedores indiquem claramente as propriedades comuns, a funcionalidade e a estrutura de um objeto de interface do usuário.

Automação da Interface do Usuário aprimora o Microsoft Active Accessibility por:

-   Habilitando clientes fora do processo eficientes, continuando a permitir o acesso em processo.
-   Expor mais informações sobre a interface do usuário de uma maneira que permita que os clientes sejam fora do processo.
-   Coexistir com e aproveitar Microsoft Active Accessibility sem herdar suas limitações. Para obter mais informações, [consulte Microsoft Active Accessibility e Automação da Interface do Usuário comparados.](microsoft-active-accessibility-and-ui-automation-compared.md)
-   Fornecendo uma alternativa ao [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) que é simples de implementar.

A implementação da especificação Automação da Interface do Usuário em Windows recursos Component Object Model interfaces baseadas em COM (interfaces gerenciadas).

## <a name="ui-automation-elements"></a>Automação da Interface do Usuário elementos

Automação da Interface do Usuário expõe cada parte da interface do usuário para aplicativos cliente como um elemento *de automação*. Os provedores fornecem valores de propriedade para cada elemento. Os elementos são expostos como uma estrutura de árvore, com a área de trabalho como o elemento raiz.

Os elementos de automação expõem propriedades comuns dos elementos de interface do usuário que eles representam. Uma dessas propriedades é o tipo de controle, que descreve sua aparência e funcionalidade básicas (por exemplo, um botão ou uma caixa de seleção).

## <a name="ui-automation-tree"></a>Automação da Interface do Usuário árvore

A Automação da Interface do Usuário de dados representa toda a interface do usuário: o elemento raiz é a área de trabalho atual e os elementos filho são janelas de aplicativo. Cada um desses elementos filho pode conter elementos que representam menus, botões, barras de ferramentas e assim por diante. Esses elementos, por sua vez, podem conter elementos como itens de lista, como mostra a ilustração a seguir.

![captura de tela mostrando a árvore de automação da interface do usuário](images/uiatree.gif)

Esteja ciente de que a ordem dos irmãos na árvore Automação da Interface do Usuário é muito importante. Os objetos que estão ao lado uns dos outros visualmente também devem estar próximos uns dos outros na árvore Automação da Interface do Usuário dados.

Automação da Interface do Usuário provedores para um controle específico suportam a navegação entre os elementos filho desse controle. No entanto, os provedores não estão preocupados com a navegação entre essas subá árvores de controle. Isso é gerenciado pelo núcleo Automação da Interface do Usuário, usando informações dos provedores de janela padrão.

Para ajudar os clientes a processar informações de interface do usuário com mais eficiência, a estrutura dá suporte a exibições alternativas da árvore de automação: exibição bruta, exibição de controle e exibição de conteúdo. Como mostra a tabela a seguir, o tipo de filtragem determina as exibições e o cliente define o escopo de uma exibição.



| Árvore de Automação | Descrição                                                                                                             |
|-----------------|-------------------------------------------------------------------------------------------------------------------------|
| Exibição bruta        | A árvore completa de objetos de elemento de automação para os quais a área de trabalho é a raiz.                                          |
| Exibição de controle    | Um subconjunto da exibição bruta que é mapeada de perto para a estrutura da interface do usuário conforme o usuário a percebe.                                |
| Exibição de conteúdo    | Um subconjunto da exibição de controle que contém o conteúdo mais relevante para o usuário, como os valores em uma caixa de combinação listada. |



 

Para obter mais informações, consulte [Visão geral Automação da Interface do Usuário árvore.](uiauto-treeoverview.md)

## <a name="ui-automation-properties"></a>Automação da Interface do Usuário propriedades

A Automação da Interface do Usuário especificação define dois tipos de propriedades: propriedades do elemento de automação e propriedades de padrão de controle. As propriedades do elemento de automação se aplicam à maioria dos controles, fornecendo informações fundamentais sobre o elemento, como seu nome. As propriedades do padrão de controle se aplicam aos padrões de controle, que são descritos a seguir.

Ao contrário Microsoft Active Accessibility, cada Automação da Interface do Usuário é identificada por um GUID e um nome programático, o que facilita a introdução de novas propriedades.

Para obter mais informações, consulte [Visão geral Automação da Interface do Usuário propriedades do](uiauto-propertiesoverview.md).

## <a name="ui-automation-control-patterns"></a>Padrões de controle de automação da interface do usuário

Um padrão de controle descreve um aspecto específico da funcionalidade de um elemento de automação. Por exemplo, um controle simples "com clique", como um botão ou hiperlink, deve dar suporte ao padrão de controle Invocar para representar a ação de "clique".

Cada padrão de controle é uma representação canônica de possíveis recursos e funções da interface do usuário. A implementação atual do Automação da Interface do Usuário define 22 padrões de controle. A API Windows automação do Windows também pode dar suporte a padrões de controle personalizados. Ao contrário Microsoft Active Accessibility propriedades de estado ou função, um elemento de automação pode dar suporte a vários Automação da Interface do Usuário de controle.

Para obter mais informações, consulte [Visão geral Automação da Interface do Usuário padrões de controle.](uiauto-controlpatternsoverview.md)

## <a name="ui-automation-control-types"></a>Tipos de controle de automação de interface do usuário

Um tipo de controle é uma propriedade de elemento de automação que especifica um controle conhecido que o elemento representa. Atualmente, o Automação da Interface do Usuário define 38 tipos de controle, incluindo Button, CheckBox, ComboBox, DataGrid, Document, Hyperlink, Image, ToolTip, Tree e Window.

Antes de atribuir um tipo de controle a um elemento, o elemento precisa atender a determinadas condições, incluindo uma estrutura de árvore de automação específica, valores de propriedade, padrões de controle e eventos. No entanto, você não está limitado a eles. Você pode estender um controle com padrões e propriedades personalizados, bem como com os predefinidos.

O número total de tipos de controle predefinidos é significativamente menor do que Microsoft Active Accessibility funções de objeto [,](object-roles.md)porque os tipos de controle Automação da Interface do Usuário podem ser combinados para expressar um conjunto maior de recursos, enquanto Microsoft Active Accessibility funções não podem.

Para obter mais informações, consulte [Visão geral Automação da Interface do Usuário tipos de controle .](uiauto-controltypesoverview.md)

## <a name="ui-automation-events"></a>Automação da Interface do Usuário eventos

Automação da Interface do Usuário eventos notificam aplicativos de alterações e ações realizadas com elementos de automação. Há quatro tipos diferentes de Automação da Interface do Usuário eventos e eles não significam necessariamente que o estado visual da interface do usuário foi alterado. O modelo de evento Automação da Interface do Usuário é independente da estrutura [WinEvent](winevents-infrastructure.md) no Windows, embora a API de Automação do Windows torna Automação da Interface do Usuário eventos interoperáveis com a estrutura Microsoft Active Accessibility.

Para obter mais informações, consulte [Visão geral Automação da Interface do Usuário eventos do .](uiauto-eventsoverview.md)

## <a name="related-topics"></a>Tópicos relacionados

[Especificação Automação da Interface do Usuário ,](./uiauto-specandcommunitypromise.md)visão [geral Windows API de Automação do Windows](windows-automation-api-overview.md)