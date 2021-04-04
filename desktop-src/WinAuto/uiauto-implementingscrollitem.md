---
title: Padrão de controle ScrollItem
description: Descreve as diretrizes e convenções para implementar o IScrollItemProvider, incluindo informações sobre métodos.
ms.assetid: ea0d7438-218c-4925-b24c-a8011f305b9d
keywords:
- Automação da interface do usuário, implementando o padrão de controle ScrollItem
- Automação da interface do usuário, padrão de controle ScrollItem
- Automação da interface do usuário, IScrollItemProvider
- IScrollItemProvider
- Implementando padrões de controle ScrollItem de automação da interface do usuário
- Padrões de controle ScrollItem
- padrões de controle, IScrollItemProvider
- padrões de controle, implementando a automação da interface do usuário ScrollItem
- padrões de controle, ScrollItem
- interfaces, IScrollItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7233dfe649d166a3172ff2dda3122895f259abcc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159951"
---
# <a name="scrollitem-control-pattern"></a>Padrão de controle ScrollItem

Descreve as diretrizes e convenções para implementar o [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider), incluindo informações sobre métodos. O padrão de controle **ScrollItem** é usado para dar suporte a controles filho individuais de contêineres que implementam [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider). A existência do padrão de controle **ScrollItem** em um controle não significa que seu contêiner ou qualquer ancestral deve implementar o padrão de controle **Scroll** .

Quando o contêiner implementa o padrão de controle **Scroll** , o padrão de controle **ScrollItem** atua como um canal de comunicação entre um controle filho e seu contêiner para garantir que o contêiner possa alterar o conteúdo visível no momento (ou região) dentro de seu visor para exibir o controle filho. Para obter exemplos de controles que implementam esse padrão de controle, consulte [tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md).

Este tópico inclui as seções a seguir.

-   [Diretrizes e convenções de implementação](#implementation-guidelines-and-conventions)
-   [Membros necessários para **IScrollItemProvider**](#required-members-for-iscrollitemprovider)
-   [Tópicos relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Diretrizes e convenções de implementação

Ao implementar o padrão de controle **ScrollItem** , observe as seguintes diretrizes e convenções:

-   Os itens contidos em um controle de [janela](uiauto-supportwindowcontroltype.md) ou **Canvas** não são necessários para implementar a interface [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider) . No entanto, como alternativa, eles devem expor um local válido para a propriedade [**IUIAutomationElement:: CurrentBoundingRectangle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentboundingrectangle) (ou [**CachedBoundingRectangle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedboundingrectangle)). Isso permitirá que um aplicativo cliente de automação da interface do usuário da Microsoft use os métodos de padrão de controle [**IUIAutomationScrollPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationscrollpattern) no contêiner para exibir o item filho.

## <a name="required-members-for-iscrollitemprovider"></a>Membros necessários para **IScrollItemProvider**

O método a seguir é necessário para implementar a interface [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider) .



| Membros necessários                                                    | Tipo de membro | Observações |
|---------------------------------------------------------------------|-------------|-------|
| [**ScrollIntoView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollitemprovider-scrollintoview) | Método      | Nenhum  |



 

Este padrão de controle não tem propriedades ou eventos associados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md)
</dt> <dt>

[Padrão de controle de seleção](uiauto-implementingselection.md)
</dt> <dt>

[Visão Geral de Padrões de Controle de Automação de Interface de Usuário](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Visão geral da árvore de automação de interface do usuário](uiauto-treeoverview.md)
</dt> </dl>

 

 




