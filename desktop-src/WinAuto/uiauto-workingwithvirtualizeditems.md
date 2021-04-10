---
title: Trabalhando com itens virtualizados
description: Este tópico descreve como usar a funcionalidade fornecida pelos padrões de controle contido e VirtualizedItem para localizar e recuperar informações sobre itens virtualizados.
ms.assetid: e1898ba0-5ffa-4c61-b378-c7ef7c4a2c52
keywords:
- clientes, itens virtualizados de automação da interface do usuário
- clientes, itens virtualizados
- clientes, padrões de controle
- clientes, padrões de controle VirtualizedItem
- clientes, padrões de controle de IsContainer
- clientes, padrões de controle VirtualizedItem de automação da interface do usuário
- clientes, padrões de controle de automação da interface do usuário
- clientes, padrões de controle do contêiner de automação da interface do usuário
- Automação da interface do usuário, itens virtualizados
- Automação da interface do usuário, padrões de controle
- Automação da interface do usuário, padrões de controle VirtualizedItem
- Automação da interface do usuário, padrões de controle de IsContainer
- Padrões de controle VirtualizedItem
- Padrões de controle de IsContainer
- padrões de controle, VirtualizedItem
- padrões de controle, IsContainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb29232b06304079ad5b9dfdfb589ad510a5b51f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292540"
---
# <a name="working-with-virtualized-items"></a>Trabalhando com itens virtualizados

Este tópico descreve como usar a funcionalidade fornecida pelos padrões de controle [contido](uiauto-implementingitemcontainer.md) e [VirtualizedItem](uiauto-implementingvirtualizeditem.md) para localizar e recuperar informações sobre itens virtualizados.

-   [Visão geral da virtualização](#overview-of-virtualization)
-   [Como um controle dá suporte à virtualização](#how-a-control-supports-virtualization)
-   [Como os clientes encontram e percebem itens virtualizados](#how-clients-find-and-realize-virtualized-items)
-   [Exemplo](#example)
-   [Tópicos relacionados](#related-topics)

## <a name="overview-of-virtualization"></a>Visão geral da virtualização

Controles que contêm um grande número de itens filho podem usar a virtualização para gerenciar os itens com eficiência. Com a virtualização, o controle mantém informações completas na memória apenas para um subconjunto de itens em um determinado momento. Normalmente, o subconjunto inclui apenas os itens que estão visíveis para o usuário no momento. As informações completas sobre os itens virtualizados restantes são mantidas no armazenamento e são carregadas na memória ou realizadas, pois o controle precisa dele, por exemplo, à medida que novos itens se tornam visíveis para o usuário.

Os controles que usam a virtualização representam um desafio porque apenas itens percebidos estão totalmente disponíveis como elementos de automação da interface do usuário da Microsoft na árvore de automação da interface do usuário. Os itens virtualizados não existem na árvore, portanto, as informações sobre eles não estão disponíveis para os clientes. Para recuperar informações sobre itens virtualizados, os clientes precisam de uma maneira de forçar a automação da interface do usuário a passar a solicitação para obter os itens para o controle. Depois que os itens forem percebidos, a automação da interface do usuário poderá criar elementos de automação da interface do usuário para eles. A automação da interface do usuário inclui dois padrões de controle para permitir que os clientes trabalhem com itens virtualizados: [MyContainer](uiauto-implementingitemcontainer.md) e [VirtualizedItem](uiauto-implementingvirtualizeditem.md).

## <a name="how-a-control-supports-virtualization"></a>Como um controle dá suporte à virtualização

Qualquer controle que possa conter itens virtualizados deve dar suporte ao padrão de controle de [IsContainer](uiauto-implementingitemcontainer.md) . Além disso, qualquer item que possa ser virtualizado deve dar suporte ao padrão de controle [VirtualizedItem](uiauto-implementingvirtualizeditem.md) . A funcionalidade que é exposta pelos padrões de controle de contêiner e VirtualizedItem é acessível aos clientes por meio das interfaces [**IUIAutomationItemContainerPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationitemcontainerpattern) e [**IUIAutomationVirtualizedItemPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvirtualizeditempattern) .

## <a name="how-clients-find-and-realize-virtualized-items"></a>Como os clientes encontram e percebem itens virtualizados

Os clientes podem usar o método [**IUIAutomationItemContainerPattern:: FindItemByProperty**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationitemcontainerpattern-finditembyproperty) para pesquisar itens filho no contêiner com base no valor de uma determinada propriedade. O método também pode recuperar o primeiro item no contêiner ou o item que segue o item especificado. Se um item filho correspondente for encontrado, o **FindItemByProperty** recuperará uma interface [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) para o item. No entanto, se o item filho for virtualizado, a interface **IUIAutomationElement** será um espaço reservado. O erro [**UIA \_ E \_ ELEMENTNOTAVAILABLE**](uiauto-error-codes.md) ocorre quando o cliente tenta usar a interface **IUIAutomationElement** para recuperar valores de propriedade ou chamar métodos que ainda não estão disponíveis. Quais propriedades ou métodos estão disponíveis por meio de um espaço reservado depende da implementação do controle. O único requisito para um espaço reservado é dar suporte à interface [**IUIAutomationVirtualizedItemPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvirtualizeditempattern) .

O erro [**UIA \_ E \_ ELEMENTNOTAVAILABLE**](uiauto-error-codes.md) é uma indicação para o cliente que um item pode ser virtualizado. O cliente deve responder recuperando a interface [**IUIAutomationVirtualizedItemPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvirtualizeditempattern) para o item e, em seguida, obtendo o item chamando o método [**IUIAutomationVirtualizedItemPattern:: concretizar**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationvirtualizeditempattern-realize) . Se isso tiver sucesso, a interface [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) será totalmente funcional com todas as propriedades apropriadas disponíveis.

Dependendo da implementação do controle, chamar [**IUIAutomationVirtualizedItemPattern:: perceber**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationvirtualizeditempattern-realize) pode fazer com que o controle role o item para a exibição. No entanto, um cliente não deve confiar no item que rola para a exibição ou tornou-se visível. Para garantir que o item esteja visível, o cliente pode usar o método [**IUIAutomationScrollItemPattern:: ScrollIntoView**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationscrollitempattern-scrollintoview) .

## <a name="example"></a>Exemplo

Por exemplo, código que mostra como usar o suporte de automação da interface do usuário para virtualização, consulte [como recuperar um item virtualizado](uiauto-howto-retrieve-virtualized-item.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão Geral de Padrões de Controle de Automação de Interface de Usuário](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




