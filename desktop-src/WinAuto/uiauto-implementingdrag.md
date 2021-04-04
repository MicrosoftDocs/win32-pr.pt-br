---
title: Arrastar padrão de controle
description: Fornece diretrizes e convenções para implementar o padrão de controle de arrastar usando IDragProvider, incluindo informações sobre propriedades e métodos. O padrão de controle de arrastar é usado para dar suporte a controles arrastáveis ou controles com itens arrastáveis.
ms.assetid: 9853E9CB-D04B-4F67-8E9E-7F1F99BACEA7
keywords:
- Automação da interface do usuário, implementando o padrão de controle de arrastar
- Automação da interface do usuário, arrastar padrão de controle
- Automação da interface do usuário, IDragProvider
- IDragProvider
- implementação da automação da interface do usuário arrastar padrões de controle
- Arrastar padrões de controle
- padrões de controle, IDragProvider
- padrões de controle, implementação da automação da interface do usuário
- padrões de controle, arraste
- interfaces, IDragProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 548f0212eca37e1890596143f27e9af70e1fb19a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007769"
---
# <a name="drag-control-pattern"></a>Arrastar padrão de controle

Fornece diretrizes e convenções para implementar o padrão de controle de **arrastar** usando [**IDragProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-idragprovider), incluindo informações sobre propriedades e métodos. O padrão de controle de **arrastar** é usado para dar suporte a controles arrastáveis ou controles com itens arrastáveis.

## <a name="implementation-guidelines-and-conventions"></a>Diretrizes e convenções de implementação

Ao implementar o padrão de controle de **arrastar** , use estas diretrizes e convenções:

-   A interface [**IDragProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idragprovider) dá suporte a dois estilos de arrastar diferentes: o estilo de origem/destino e o estilo somente origem. Você precisa escolher o estilo que funciona melhor para seus cenários de arrastar e soltar:
    -   **Estilo de origem/destino:** Cada destino possível drop é representado por um elemento que implementa a interface [**IDropTargetProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idroptargetprovider) . Durante uma operação de arrastar, os eventos de automação da interface do usuário da Microsoft originam-se do elemento que está sendo arrastado e dos elementos de destino.
    -   **Estilo somente de origem:** Os destinos de destino não são representados pelos elementos de automação da interface do usuário. Durante uma operação de arrastar, os eventos se originam apenas do elemento que está sendo arrastado.
-   [**IDragProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idragprovider) é uma interface somente leitura destinada ao monitoramento de operações de arrastar. Você não pode usá-lo para controlar uma operação de arrastar. Você pode automatizar operações de arrastar enviando a entrada do mouse para um controle.
-   A propriedade [**IDragProvider:: iscapturado**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) é necessária.
-   As propriedades [**IDragProvider::D ropeffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) e [**IDragProvider::D ropeffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffects) são necessárias para uma implementação de estilo somente de origem e são proibidas para uma implementação de estilo de origem/destino. Em uma implementação de estilo de origem/destino, elementos de destino podem ser consultados para seus efeitos de soltar.
-   A propriedade [**IDragProvider:: GrabbedItems**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-getgrabbeditems) representa o arrasto de vários itens. Quando o usuário inicia a operação de arrastar, você precisa criar um novo elemento de automação de interface do usuário para servir como o elemento de origem do evento. Esse novo elemento dispara todos os eventos que o elemento de origem teria acionado no modo de origem/destino ou somente de origem, enquanto nenhum dos elementos que realmente estão sendo arrastados aciona qualquer evento. Quando a operação de arrastar for concluída, destrua o elemento de origem do evento.
-   O elemento deve acionar eventos de propriedade alterada para as propriedades **DropEffect** ([**UIA \_ DragDropEffectPropertyId**](uiauto-control-pattern-propids.md)) e **DropEffects** ([**UIA \_ DragDropEffectsPropertyId**](uiauto-control-pattern-propids.md)) quando elas forem alteradas. Eventos de propriedade alterada para as outras propriedades são permitidos, mas podem ser inferidos dos eventos obrigatórios **DragStart** ([**UIA \_ Drag \_ DragStartEventId**](uiauto-event-ids.md)), **DragCancel** ([**UIA \_ Arraste \_ DragCancelEventId**](uiauto-event-ids.md)) e **DragComplete** ([**UIA \_ Drag \_ DragCompleteEventId**](uiauto-event-ids.md)).
-   

## <a name="required-members-for-idragprovider"></a>Membros necessários para **IDragProvider**

As propriedades e os métodos a seguir são necessários para implementar a interface [**IDragProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-idragprovider) .



| Membros necessários                                                                        | Tipo de membro | Observações                                                                         |
|-----------------------------------------------------------------------------------------|-------------|-------------------------------------------------------------------------------|
| [**Iscapturado**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed)                                     | Propriedade    | Nenhum                                                                          |
| [**DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect)                                   | Propriedade    | Necessário para uma implementação do estilo somente origem.                      |
| [**DropEffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffects)                                 | Propriedade    | Necessário se houver mais de um possível efeito de soltar para o item capturado. |
| [**GetGrabbedItems**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-getgrabbeditems)                         | Método      | Necessário para uma operação de arrastar com vários itens.                                  |
| [**UIA \_ arrastar \_ DragStartEventId**](uiauto-event-ids.md)       | Evento       | Nenhum                                                                          |
| [**UIA \_ arrastar \_ DragCancelEventId**](uiauto-event-ids.md)     | Evento       | Nenhum                                                                          |
| [**UIA \_ arrastar \_ DragCompleteEventId**](uiauto-event-ids.md) | Evento       | Nenhum                                                                          |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md)
</dt> <dt>

[Padrão de controle DropTarget](/windows/desktop/WinAuto/uiauto-implementingdroptarget)
</dt> <dt>

[Visão Geral de Padrões de Controle de Automação de Interface de Usuário](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Visão geral da árvore de automação de interface do usuário](uiauto-treeoverview.md)
</dt> <dt>

[Suporte à automação da interface do usuário para arrastar e soltar](ui-automation-support-for-drag-and-drop.md)
</dt> </dl>

 

 