---
title: Padrão de controle ScrollItem
description: Descreve diretrizes e convenções para implementar IScrollItemProvider, incluindo informações sobre métodos.
ms.assetid: ea0d7438-218c-4925-b24c-a8011f305b9d
keywords:
- Automação da Interface do Usuário, implementando o padrão de controle ScrollItem
- Automação da Interface do Usuário, padrão de controle ScrollItem
- Automação da Interface do Usuário,IScrollItemProvider
- IScrollItemProvider
- implementando padrões Automação da Interface do Usuário controle ScrollItem
- Padrões de controle ScrollItem
- padrões de controle, IScrollItemProvider
- padrões de controle, implementando Automação da Interface do Usuário ScrollItem
- padrões de controle, ScrollItem
- interfaces,IScrollItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a677a761c01afb5ad6feaf04df0197299a528a22741c0bd8ff72c02f45c74b0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118826886"
---
# <a name="scrollitem-control-pattern"></a>Padrão de controle ScrollItem

Descreve diretrizes e convenções para implementar [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider), incluindo informações sobre métodos. O **padrão de controle ScrollItem** é usado para dar suporte a controles filho individuais de contêineres que implementam [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider). A existência do padrão **de controle ScrollItem** em um controle não implica que seu contêiner ou qualquer ancestral deve implementar o padrão **de controle Scroll.**

Quando o contêiner  implementa o padrão de controle Scroll, o padrão de controle **ScrollItem** atua como um canal de comunicação entre um controle filho e seu contêiner para garantir que o contêiner possa alterar o conteúdo visível no momento (ou região) em seu visor para exibir o controle filho. Para exemplos de controles que implementam esse padrão de controle, consulte [Tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md).

Este tópico inclui as seções a seguir.

-   [Diretrizes e convenções de implementação](#implementation-guidelines-and-conventions)
-   [Membros necessários para **IScrollItemProvider**](#required-members-for-iscrollitemprovider)
-   [Tópicos relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Diretrizes e convenções de implementação

Ao implementar o padrão **de controle ScrollItem,** observe as seguintes diretrizes e convenções:

-   Itens contidos em [um controle Janela](uiauto-supportwindowcontroltype.md) ou **Tela** não são necessários para implementar a interface [**IScrollItemProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider) Como alternativa, no entanto, eles devem expor um local válido para a propriedade [**IUIAutomationElement::CurrentBoundingRectangle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentboundingrectangle) (ou [**CachedBoundingRectangle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedboundingrectangle)). Isso permitirá que um aplicativo cliente microsoft Automação da Interface do Usuário use os métodos de padrão de controle [**IUIAutomationScrollPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationscrollpattern) no contêiner para exibir o item filho.

## <a name="required-members-for-iscrollitemprovider"></a>Membros necessários para **IScrollItemProvider**

O método a seguir é necessário para implementar a interface [**IScrollItemProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider)



| Membros necessários                                                    | Tipo de membro | Observações |
|---------------------------------------------------------------------|-------------|-------|
| [**ScrollIntoView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollitemprovider-scrollintoview) | Método      | Nenhum  |



 

Esse padrão de controle não tem propriedades ou eventos associados.

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

 

 




