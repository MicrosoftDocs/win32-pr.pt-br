---
title: Padrão de controle DropTarget
description: Fornece diretrizes e convenções para implementar o padrão de controle DropTarget usando IDropTargetProvider, incluindo informações sobre propriedades e métodos.
ms.assetid: DD5EE4A0-E6C0-4657-A60F-7F59FC569E04
keywords:
- Automação da Interface do Usuário, implementando o padrão de controle DropTarget
- Automação da Interface do Usuário, padrão de controle DropTarget
- Automação da Interface do Usuário,IDropTargetProvider
- IDropTargetProvider
- implementando Automação da Interface do Usuário de controle DropTarget
- Padrões de controle DropTarget
- padrões de controle, IDropTargetProvider
- padrões de controle, implementando Automação da Interface do Usuário DropTarget
- padrões de controle, DropTarget
- interfaces, IDropTargetProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03cc425c9d41a70150eba2431c6fd317f2f8c23f878f7a0615025aec25b85b68
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098306"
---
# <a name="droptarget-control-pattern"></a>Padrão de controle DropTarget

Fornece diretrizes e convenções para implementar o padrão de controle **DropTarget** usando [**IDropTargetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-idroptargetprovider), incluindo informações sobre propriedades e métodos. O **padrão de controle DropTarget** é usado para dar suporte a controles que podem ser o destino de uma operação do tipo "arrastar e soltar".

## <a name="implementation-guidelines-and-conventions"></a>Diretrizes e convenções de implementação

Ao implementar o padrão **de controle DropTarget,** use as seguintes diretrizes e convenções:

-   O **padrão DropTarget** deve ter suporte enquanto uma operação de arrastar está em andamento. Ele pode ser suportado mesmo quando uma operação de arrastar não está em andamento.
-   A [**propriedade IDropTargetProvider::D ropTargetEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) é necessária.
-   A [**propriedade IDropTargetProvider::D ropTargetEffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffects) é necessária quando há mais de um possível efeito de soltar para o destino.
-   O elemento deve gerar eventos alterados de propriedade para as propriedades **DropTargetEffect** ([**UIA \_ DropTargetDropTargetEffectPropertyId**](uiauto-control-pattern-propids.md)) e **DropTargetEffects** ([**UIA \_ DropTargetDropTargetEffectsPropertyId**](uiauto-control-pattern-propids.md)) quando elas são alteradas.

## <a name="required-members-for-idroptargetprovider"></a>Membros necessários para **IDropTargetProvider**

As seguintes propriedades e métodos são necessários para implementar a interface [**IDropTargetProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idroptargetprovider)



| Membros necessários                                                                              | Tipo de membro | Observações                                                                    |
|-----------------------------------------------------------------------------------------------|-------------|--------------------------------------------------------------------------|
| [**DropTargetEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect)                       | Propriedade    | Nenhum                                                                     |
| [**DropTargetEffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffects)                     | Propriedade    | Necessário se o destino de soltar for compatível com mais de um possível efeito de soltar. |
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

[Automação da Interface do Usuário suporte para arrastar e soltar](ui-automation-support-for-drag-and-drop.md)
</dt> </dl>

 

 