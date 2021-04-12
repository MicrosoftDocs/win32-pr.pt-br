---
title: Padrão de controle DropTarget
description: Fornece diretrizes e convenções para implementar o padrão de controle DropTarget usando IDropTargetProvider, incluindo informações sobre propriedades e métodos.
ms.assetid: DD5EE4A0-E6C0-4657-A60F-7F59FC569E04
keywords:
- Automação da interface do usuário, implementando o padrão de controle DropTarget
- Automação da interface do usuário, padrão de controle DropTarget
- Automação da interface do usuário, IDropTargetProvider
- IDropTargetProvider
- Implementando padrões de controle DropTarget de automação da interface do usuário
- Padrões de controle DropTarget
- padrões de controle, IDropTargetProvider
- padrões de controle, implementando a automação da interface do usuário DropTarget
- padrões de controle, DropTarget
- interfaces, IDropTargetProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd03d219ce8b26a0ac01806ebab09892a027fbd1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294238"
---
# <a name="droptarget-control-pattern"></a>Padrão de controle DropTarget

Fornece diretrizes e convenções para implementar o padrão de controle **DropTarget** usando [**IDropTargetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-idroptargetprovider), incluindo informações sobre propriedades e métodos. O padrão de controle **DropTarget** é usado para dar suporte a controles que podem ser o destino de uma operação de arrastar e soltar.

## <a name="implementation-guidelines-and-conventions"></a>Diretrizes e convenções de implementação

Ao implementar o padrão de controle **DropTarget** , use as seguintes diretrizes e convenções:

-   O padrão **DropTarget** deve ter suporte enquanto uma operação de arrastar estiver em andamento. Ele pode ter suporte mesmo quando uma operação de arrastar não está em andamento.
-   A propriedade [**IDropTargetProvider::D roptargeteffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) é necessária.
-   A propriedade [**IDropTargetProvider::D roptargeteffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffects) é necessária quando há mais de um possível efeito de soltar para o destino.
-   O elemento deve gerar eventos de propriedade alterada para as propriedades **DropTargetEffect** ([**UIA \_ DropTargetDropTargetEffectPropertyId**](uiauto-control-pattern-propids.md)) e **DropTargetEffects** ([**UIA \_ DropTargetDropTargetEffectsPropertyId**](uiauto-control-pattern-propids.md)) quando elas forem alteradas.

## <a name="required-members-for-idroptargetprovider"></a>Membros necessários para **IDropTargetProvider**

As propriedades e os métodos a seguir são necessários para implementar a interface [**IDropTargetProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idroptargetprovider) .



| Membros necessários                                                                              | Tipo de membro | Observações                                                                    |
|-----------------------------------------------------------------------------------------------|-------------|--------------------------------------------------------------------------|
| [**DropTargetEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect)                       | Propriedade    | Nenhum                                                                     |
| [**DropTargetEffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffects)                     | Propriedade    | Necessário se a interface "soltar" oferecer suporte a mais de um possível efeito de soltar. |
| [**UIA \_ DropTarget \_ DragEnterEventId**](uiauto-event-ids.md) | Evento       | Nenhum                                                                     |
| [**UIA \_ DropTarget \_ DragLeaveEventId**](uiauto-event-ids.md) | Evento       | Nenhum                                                                     |
| [**UIA \_ DropTarget \_ DroppedEventId**](uiauto-event-ids.md)     | Evento       | Nenhum                                                                     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md)
</dt> <dt>

[Arrastar padrão de controle](/windows/desktop/WinAuto/uiauto-implementingdrag)
</dt> <dt>

[Visão Geral de Padrões de Controle de Automação de Interface de Usuário](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Visão geral da árvore de automação de interface do usuário](uiauto-treeoverview.md)
</dt> <dt>

[Suporte à automação da interface do usuário para arrastar e soltar](ui-automation-support-for-drag-and-drop.md)
</dt> </dl>

 

 