---
title: Trabalhando com itens virtualizados
description: Este tópico descreve como usar a funcionalidade fornecida pelos padrões de controle ItemContainer e VirtualizedItem para encontrar e recuperar informações sobre itens virtualizados.
ms.assetid: e1898ba0-5ffa-4c61-b378-c7ef7c4a2c52
keywords:
- clientes, Automação da Interface do Usuário virtualizados
- clientes, itens virtualizados
- clientes, padrões de controle
- clientes, padrões de controle VirtualizedItem
- clientes, padrões de controle ItemContainer
- clientes, Automação da Interface do Usuário de controle VirtualizedItem
- clientes, Automação da Interface do Usuário de controle
- clientes, Automação da Interface do Usuário de controle ItemContainer
- Automação da Interface do Usuário, itens virtualizados
- Automação da Interface do Usuário, padrões de controle
- Automação da Interface do Usuário,padrões de controle VirtualizedItem
- Automação da Interface do Usuário,padrões de controle ItemContainer
- Padrões de controle VirtualizedItem
- Padrões de controle ItemContainer
- padrões de controle, VirtualizedItem
- padrões de controle, ItemContainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e2c0e84f91af6bcaadef5af373b73057fb4a137480255f3ee1af4456e45eaf1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119570366"
---
# <a name="working-with-virtualized-items"></a>Trabalhando com itens virtualizados

Este tópico descreve como usar a funcionalidade fornecida pelos padrões de controle [ItemContainer](uiauto-implementingitemcontainer.md) e [VirtualizedItem](uiauto-implementingvirtualizeditem.md) para encontrar e recuperar informações sobre itens virtualizados.

-   [Visão geral da virtualização](#overview-of-virtualization)
-   [Como um controle dá suporte à virtualização](#how-a-control-supports-virtualization)
-   [Como os clientes encontram e realizam itens virtualizados](#how-clients-find-and-realize-virtualized-items)
-   [Exemplo](#example)
-   [Tópicos relacionados](#related-topics)

## <a name="overview-of-virtualization"></a>Visão geral da virtualização

Controles que contêm um grande número de itens filho podem usar a virtualização para gerenciar os itens com eficiência. Com a virtualização, o controle mantém informações completas na memória apenas para um subconjunto de itens em um determinado momento. Normalmente, o subconjunto inclui apenas os itens que estão visíveis no momento para o usuário. As informações completas sobre os itens virtualizados restantes são mantidas no armazenamento e carregadas na memória ou realizadas, pois o controle precisa dele, por exemplo, à medida que novos itens se tornam visíveis para o usuário.

Os controles que usam a virtualização representam um desafio porque somente itens realizados estão totalmente disponíveis como elementos Automação da Interface do Usuário Microsoft na árvore Automação da Interface do Usuário dados. Itens virtualizados não existem na árvore, portanto, as informações sobre eles não estão disponíveis para os clientes. Para recuperar informações sobre itens virtualizados, os clientes precisam de uma maneira de forçar Automação da Interface do Usuário para passar a solicitação para realizar os itens para o controle. Depois que os itens foram realizados, Automação da Interface do Usuário pode criar Automação da Interface do Usuário para eles. Automação da Interface do Usuário inclui dois padrões de controle para permitir que os clientes trabalhem com itens virtualizados: [ItemContainer](uiauto-implementingitemcontainer.md) e [VirtualizedItem](uiauto-implementingvirtualizeditem.md).

## <a name="how-a-control-supports-virtualization"></a>Como um controle dá suporte à virtualização

Qualquer controle que possa conter itens virtualizados deve dar suporte ao [padrão de controle ItemContainer.](uiauto-implementingitemcontainer.md) Além disso, qualquer item que possa ser virtualizado deve dar suporte ao [padrão de controle VirtualizedItem.](uiauto-implementingvirtualizeditem.md) A funcionalidade exposta pelos padrões de controle ItemContainer e VirtualizedItem é acessível aos clientes por meio das interfaces [**IUIAutomationItemContainerPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationitemcontainerpattern) e [**IUIAutomationVirtualizedItemPattern.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvirtualizeditempattern)

## <a name="how-clients-find-and-realize-virtualized-items"></a>Como os clientes encontram e realizam itens virtualizados

Os clientes podem usar o método [**IUIAutomationItemContainerPattern::FindItemByProperty**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationitemcontainerpattern-finditembyproperty) para pesquisar itens filho no contêiner com base no valor de uma propriedade específica. O método também pode recuperar o primeiro item no contêiner ou o item que segue o item especificado. Se um item filho correspondente for encontrado, **FindItemByProperty** recuperará uma interface [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) para o item. No entanto, se o item filho for virtualizado, a interface **IUIAutomationElement** será um espaço reservado. O [**erro UIA \_ E \_ ELEMENTNOTAVAILABLE**](uiauto-error-codes.md) ocorre quando o cliente tenta usar a interface **IUIAutomationElement** para recuperar valores de propriedade ou métodos de chamada que ainda não estão disponíveis. Quais propriedades ou métodos estão disponíveis por meio de um espaço reservado depende da implementação do controle. O único requisito para um espaço reservado é dar suporte à interface [**IUIAutomationVirtualizedItemPattern.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvirtualizeditempattern)

O [**erro UIA \_ E \_ ELEMENTNOTAVAILABLE**](uiauto-error-codes.md) é uma indicação para o cliente de que um item pode ser virtualizado. O cliente deve responder recuperando a interface [**IUIAutomationVirtualizedItemPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvirtualizeditempattern) para o item e, em seguida, realizando o item chamando o método [**IUIAutomationVirtualizedItemPattern::Realize.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationvirtualizeditempattern-realize) Se isso for bem-sucedido, a interface [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) será totalmente funcional com todas as propriedades apropriadas disponíveis.

Dependendo da implementação do controle, chamar [**IUIAutomationVirtualizedItemPattern::Realize**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationvirtualizeditempattern-realize) pode fazer com que o controle role o item para a exibição. No entanto, um cliente não deve depender do item que rola para a exibição ou se tornou visível. Para garantir que o item está visível, o cliente pode usar o [**método IUIAutomationScrollItemPattern::ScrollIntoView.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationscrollitempattern-scrollintoview)

## <a name="example"></a>Exemplo

Para obter um código de exemplo que mostra como usar o Automação da Interface do Usuário para virtualização, consulte [How to Retrieve a Virtualized Item](uiauto-howto-retrieve-virtualized-item.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão Geral de Padrões de Controle de Automação de Interface de Usuário](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




