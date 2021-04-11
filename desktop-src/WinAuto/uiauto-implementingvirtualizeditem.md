---
title: Padrão de controle VirtualizedItem
description: Descreve as diretrizes e convenções para implementar o IVirtualizedItemProvider, incluindo informações sobre propriedades e métodos.
ms.assetid: 7a95e92f-7ccb-4c9b-8986-1d2de7038e47
keywords:
- Automação da interface do usuário, implementando o padrão de controle VirtualizedItem
- Automação da interface do usuário, padrão de controle VirtualizedItem
- Automação da interface do usuário, IVirtualizedItemProvider
- IVirtualizedItemProvider
- Implementando padrões de controle VirtualizedItem de automação da interface do usuário
- Padrões de controle VirtualizedItem
- padrões de controle, IVirtualizedItemProvider
- padrões de controle, implementando a automação da interface do usuário VirtualizedItem
- padrões de controle, VirtualizedItem
- interfaces, IVirtualizedItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8dac9e34dd9bff5d0ba2d245aa2fb8de621f40a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160480"
---
# <a name="virtualizeditem-control-pattern"></a>Padrão de controle VirtualizedItem

Descreve as diretrizes e convenções para implementar o [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider), incluindo informações sobre propriedades e métodos. O padrão de controle **VirtualizedItem** é usado para dar suporte a itens virtualizados, que são itens representados por elementos de automação de espaço reservado na árvore de automação da interface do usuário da Microsoft.

Itens virtualizados podem incluir itens recuperados de um controle que dá suporte ao padrão de controle de item [contido](uiauto-implementingitemcontainer.md) ou um objeto incorporado virtualizado recuperado de um controle que dá suporte ao padrão de controle de [texto](uiauto-implementingtextandtextrange.md) . O espaço reservado para um item virtualizado pode não ter dados carregados para todas as propriedades de automação da interface do usuário e pode retornar [**UIA \_ E \_ ELEMENTNOTAVAILABLE**](uiauto-error-codes.md) em resposta a consultas de propriedades que não estão disponíveis. O padrão de controle **VirtualizedItem** fornece um método para concretizar um item virtual para que as informações completas sejam disponibilizadas para o item e um elemento de automação completa possa ser criado para o item na árvore de automação da interface do usuário.

Este tópico inclui as seções a seguir.

-   [Diretrizes e convenções de implementação](#implementation-guidelines-and-conventions)
-   [Membros necessários para **IVirtualizedItemProvider**](#required-members-for-ivirtualizeditemprovider)
-   [Tópicos relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Diretrizes e convenções de implementação

Ao implementar o padrão de controle **VirtualizedItem** , observe as seguintes diretrizes e convenções:

-   Qualquer elemento de espaço reservado de automação da interface do usuário que pode ser virtualizado deve dar suporte ao padrão de controle **VirtualizedItem** expondo a interface [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider) .
-   Quando [**IVirtualizedItemProvider:: perceba**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) é chamado, o objeto de espaço reservado deve ser atualizado com implementações completas de suas propriedades e padrões de controle.
-   Quando [**IVirtualizedItemProvider:: perceba**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) é chamado, o provedor pode alterar o visor para que o item virtualizado venha a ser exibido. Não é necessário colocar o item na exibição; no entanto, itens fora da tela, não virtualizados, devem dar suporte ao método [**IScrollItemProvider:: ScrollIntoView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollitemprovider-scrollintoview) .

## <a name="required-members-for-ivirtualizeditemprovider"></a>Membros necessários para **IVirtualizedItemProvider**

As propriedades e os métodos a seguir são necessários para implementar a interface [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider) .



| Membros necessários                                           | Tipo de membro | Observações |
|------------------------------------------------------------|-------------|-------|
| [**State**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) | Método      | Nenhum  |



 

Este padrão de controle não tem eventos associados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Implementando o padrão de controle do contêiner de automação da interface do usuário](uiauto-implementingitemcontainer.md)
</dt> <dt>

[Visão Geral de Padrões de Controle de Automação de Interface de Usuário](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Visão geral da árvore de automação de interface do usuário](uiauto-treeoverview.md)
</dt> <dt>

[Trabalhando com itens virtualizados](uiauto-workingwithvirtualizeditems.md)
</dt> </dl>

 

 




