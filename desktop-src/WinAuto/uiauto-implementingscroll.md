---
title: Padrão de controle Scroll
description: Descreve as diretrizes e convenções para implementar o IScrollProvider, incluindo informações sobre propriedades e métodos. O padrão de controle Scroll é usado para dar suporte a um controle que atua como um contêiner rolável para uma coleção de objetos filho.
ms.assetid: baf8012a-52d5-4465-b26d-aa3d7f550b54
keywords:
- Automação da interface do usuário, implementando o padrão de controle Scroll
- Automação da interface do usuário, padrão de controle de rolagem
- Automação da interface do usuário, IScrollProvider
- IScrollProvider
- Implementando padrões de controle de rolagem da automação da IU
- Padrões de controle de rolagem
- padrões de controle, IScrollProvider
- padrões de controle, implementação da rolagem da automação da interface do usuário
- padrões de controle, rolagem
- interfaces, IScrollProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b525c77a7f89f7adc95a3d90d999f8b243cfcdb6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636459"
---
# <a name="scroll-control-pattern"></a>Padrão de controle Scroll

Descreve as diretrizes e convenções para implementar o [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider), incluindo informações sobre propriedades e métodos. O padrão de controle **Scroll** é usado para dar suporte a um controle que atua como um contêiner rolável para uma coleção de objetos filho.

O controle não é necessário para usar barras de rolagem para dar suporte à funcionalidade de rolagem, embora normalmente faça isso. A imagem a seguir mostra um controle de rolagem que não usa barras de rolagem. Para obter exemplos de controles que implementam esse padrão de controle, consulte [tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md).

![captura de tela mostrando um controle de rolagem sem barras de rolagem](images/uia-scrollpattern-without-scrollbars.jpg)

Este tópico inclui as seções a seguir.

-   [Diretrizes e convenções de implementação](#implementation-guidelines-and-conventions)
-   [Membros necessários para **IScrollProvider**](#required-members-for-iscrollprovider)
-   [Tópicos relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Diretrizes e convenções de implementação

Ao implementar o padrão de controle de **rolagem** , observe as seguintes diretrizes e convenções:

-   Os filhos desse controle devem implementar [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider).
-   As barras de rolagem de um controle de contêiner não dão suporte ao padrão de controle **Scroll** . Em vez disso, eles devem oferecer suporte ao padrão de controle [RangeValue](uiauto-implementingrangevalue.md) .
-   Quando a rolagem é medida em percentuais, todos os valores ou quantidades relacionados à formatura de rolagem devem ser normalizados para um intervalo de 0 a 100.
-   A propriedade [**IScrollProvider:: HorizontallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable) e a propriedade [**VerticallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable) são independentes da propriedade **IsEnabled** .
-   Se a propriedade [**IScrollProvider:: HorizontallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable) for **false**, a propriedade [**HorizontalViewSize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalviewsize) deverá ser definida como 100 (100%) e a propriedade [**HorizontalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent) deve ser definida como **UIA \_ ScrollPatternNoScroll** (-1). Da mesma forma, se a propriedade [**VerticallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable) for **false**, a propriedade [**VerticalViewSize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalviewsize) deverá ser definida como 100 (100%) e a propriedade [**VerticalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalscrollpercent) deve ser definida como **UIA \_ ScrollPatternNoScroll** (-1). Isso permite que um cliente de automação da interface do usuário da Microsoft use esses valores de propriedade dentro do método [**SetScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-setscrollpercent) enquanto evita uma condição de corrida se uma direção na qual o cliente não está interessado em rolar é ativada.
-   A propriedade [**IScrollProvider:: HorizontalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent) é específica à localidade. Definir **HorizontalScrollPercent** como 100 deve definir o local de rolagem do controle para o equivalente de sua posição mais à direita para idiomas como o inglês que são lidos da esquerda para a direita. Como alternativa, para idiomas como árabe que são lidos da direita para a esquerda, definir **HorizontalScrollPercent** como 100 deve definir o local de rolagem para a posição mais à esquerda.

## <a name="required-members-for-iscrollprovider"></a>Membros necessários para **IScrollProvider**

As propriedades e os métodos a seguir são necessários para implementar a interface [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider) .



| Membros necessários                                                                  | Tipo de membro | Observações |
|-----------------------------------------------------------------------------------|-------------|-------|
| [**HorizontalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent) | Propriedade    | Nenhum  |
| [**VerticalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalscrollpercent)     | Propriedade    | Nenhum  |
| [**HorizontalViewSize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalviewsize)           | Propriedade    | Nenhum  |
| [**VerticalViewSize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalviewsize)               | Propriedade    | Nenhum  |
| [**HorizontallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable)   | Propriedade    | Nenhum  |
| [**VerticallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable)       | Propriedade    | Nenhum  |
| [**Rolagem**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-scroll)                                   | Método      | Nenhum  |
| [**SetScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-setscrollpercent)               | Método      | Nenhum  |



 

Este padrão de controle não tem eventos associados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md)
</dt> <dt>

[Visão Geral de Padrões de Controle de Automação de Interface de Usuário](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Visão geral da árvore de automação de interface do usuário](uiauto-treeoverview.md)
</dt> </dl>

 

 




