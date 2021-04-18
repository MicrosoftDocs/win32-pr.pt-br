---
title: Suporte à automação da interface do usuário para arrastar e soltar
description: Este tópico descreve os padrões de controle que expõem informações sobre a funcionalidade de arrastar e soltar de um elemento.
ms.assetid: FFF5A296-C9FF-4B47-AAF8-A9DD581D9DBE
keywords:
- Automação da interface do usuário, suporte a arrastar e soltar
- Automação da interface do usuário, arrastar visão geral do padrão
- Automação da interface do usuário, visão geral do padrão DropTarget
- Visão geral da automação da interface do usuário, arrastar e soltar
- padrões de arrastar e soltar, sobre
- Arrastar padrão de controle
- Padrão de controle DropTarget
- padrões de controle, arraste
- padrões de controle, DropTarget
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4194613d15aadac4a925303ef2322d4cf53c341c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105810543"
---
# <a name="ui-automation-support-for-drag-and-drop"></a>Suporte à automação da interface do usuário para arrastar e soltar

A automação da interface do usuário da Microsoft define dois padrões de controle para dar suporte a cenários de arrastar e soltar, o padrão de controle de [arrastar](/windows/desktop/WinAuto/uiauto-implementingdrag) e o padrão de controle [DropTarget](/windows/desktop/WinAuto/uiauto-implementingdroptarget) . Você implementa o padrão de controle de arrastar para um elemento que pode ser arrastado e o padrão de controle DropTarget para um elemento que pode receber um elemento arrastado; ou seja, um destino de soltura. Os dois padrões de controle expõem informações que uma tecnologia assistencial pode usar para ajudar um usuário de acessibilidade a concluir uma operação de arrastar e soltar.

-   [Arrastando estilos](#dragging-styles)
    -   [Estilo de origem/destino](#sourcetarget-style)
    -   [Estilo somente origem](#source-only-style)
-   [Arrastando vários itens](#dragging-multiple-items)
-   [Interfaces de cliente para arrastar e soltar](#client-interfaces-for-drag-and-drop)

## <a name="dragging-styles"></a>Arrastando estilos

Ao implementar o padrão de controle de [arrastar](/windows/desktop/WinAuto/uiauto-implementingdrag) para um elemento arrastável, você precisa decidir se deseja implementar o estilo de arrastar de *origem/destino* ou o estilo de arrastar *somente origem* .

### <a name="sourcetarget-style"></a>Estilo de origem/destino

No estilo de origem/destino de arrastar e soltar, o elemento arrastado (a "origem") e o elemento de destino (o "destino") são distintos e cada um gera um conjunto distinto de eventos. Este é o ciclo de vida de uma operação de arrastar que usa o estilo de origem/destino: <dl> Quando o usuário inicia uma operação de arrastar:

-   A origem gera o evento DragStart ([**UIA \_ Drag \_ DragStartEventId**](uiauto-event-ids.md)).
-   A fonte define a propriedade [**IDragProvider:: iscapturado**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) como **true**.
-   Os destinos atualizam suas propriedades [**DropTargetEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) .

  
Quando a operação de arrastar entra em uma região de destino:

-   O destino gera o evento DragEnter ([**UIA \_ DropTarget \_ DragEnterEventId**](uiauto-event-ids.md)).

  
Quando a operação de arrastar sair de uma região de destino:

-   O destino gera o evento DragLeave ([**UIA \_ DropTarget \_ DragLeaveEventId**](uiauto-event-ids.md)).

  
Quando o usuário libera o item arrastado em um não destino:

-   A origem gera o evento DragCancel ([**UIA \_ Drag \_ DragCancelEventId**](uiauto-event-ids.md)).
-   A fonte define a propriedade [**IDragProvider:: iscapturado**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) como **false**.

  
Quando o usuário libera o item arrastado sobre um destino:

-   A origem gera o evento DragComplete ([**UIA \_ Drag \_ DragCompleteEventId**](uiauto-event-ids.md)).
-   A fonte define a propriedade [**IDragProvider:: iscapturado**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) como **false**.
-   O destino define a propriedade [**IDropTargetProvider::D roptargeteffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) para indicar o efeito que ocorreu.
-   O destino gera o evento solto ([**UIA \_ DropTarget \_ DroppedEventId**](uiauto-event-ids.md)).

  
</dl>

Os eventos dos objetos de origem e de destino estão fortemente relacionados, mas distintos. Os dados sobre o que está sendo arrastado vêm da origem, enquanto os dados sobre "o que poderia acontecer" e "o que aconteceu" vêm do destino.

Quando uma operação de arrastar está em andamento, o item arrastado pode ser arrastado para dentro e para fora das regiões de destino quantas vezes a operação for concluída.

Qualquer destino de soltura que precise atualizar sua propriedade [**IDropTargetProvider::D roptargeteffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) de forma dinâmica deve gerar um evento de alteração de propriedade adicional nessa propriedade.

### <a name="source-only-style"></a>Estilo somente origem

O estilo de arrastar somente origem permite que um provedor Evite implementar destinos de destino. Não implementar destinos de destino ajuda a reduzir o custo de implementação, mas não dá aos aplicativos cliente de acessibilidade informações sobre o objeto que recebeu a queda. Este é o ciclo de vida de uma operação de arrastar que usa o estilo somente origem: <dl> Quando o usuário inicia uma operação de arrastar:

-   A origem gera o evento DragStart ([**UIA \_ Drag \_ DragStartEventId**](uiauto-event-ids.md)).
-   A fonte define a propriedade [**IDragProvider:: iscapturado**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) como **true**.

  
Quando a operação de arrastar entra em uma região de destino:

-   A fonte define a propriedade [**IDragProvider::D ropeffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) como o valor apropriado.

  
Quando a operação de arrastar sair de uma região de destino:

-   A fonte define a propriedade [**IDragProvider::D ropeffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) como o valor apropriado.

  
Quando o usuário libera o item arrastado em um não destino:

-   A origem gera o evento DragCancel ([**UIA \_ Drag \_ DragCancelEventId**](uiauto-event-ids.md)).
-   A fonte define a propriedade [**IDragProvider:: iscapturado**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) como **false**.

  
Quando o usuário libera o item arrastado sobre um destino:

-   A origem gera o evento DragComplete ([**UIA \_ Drag \_ DragCompleteEventId**](uiauto-event-ids.md)).
-   A fonte define a propriedade [**IDragProvider::D ropeffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) para indicar o efeito que ocorreu quando o item foi Descartado.

  
</dl>

## <a name="dragging-multiple-items"></a>Arrastando vários itens

Se um provedor implementar operações de arrastar e soltar em que o usuário pode arrastar vários objetos ao mesmo tempo, o provedor usará os estilos de origem/destino ou somente origem, conforme descrito na seção anterior, mas com uma pequena diferença. Quando o usuário inicia a operação de arrastar, o provedor cria um elemento de origem mestre que representa o conjunto completo de itens que estão sendo arrastados. O elemento de origem mestre gera todos os eventos em nome do conjunto de itens arrastados; os itens não geram nenhum evento próprio.<dl> Quando o usuário inicia uma operação de arrastar:

-   O provedor cria o elemento de origem mestre.
-   O elemento Source mestre gera o evento DragStart ([**UIA \_ Drag \_ DragStartEventId**](uiauto-event-ids.md)).
-   O elemento de origem mestre define a propriedade [**IDragProvider:: iscapturado**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) como **true**.
-   O elemento de origem mestre atualiza a lista de itens capturados para incluir todos os itens que estão sendo arrastados para que o método [**GetGrabbedItems**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-getgrabbeditems) possa recuperar a lista.

  
</dl>

Para esse ponto, o elemento de origem mestre executa a mesma função que o elemento de origem, conforme descrito na seção anterior.

## <a name="client-interfaces-for-drag-and-drop"></a>Interfaces de cliente para arrastar e soltar

Os aplicativos cliente de automação da interface do usuário usam as interfaces [**IUIAutomationDragPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) e [**IUIAutomationDropTargetPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern) para acessar informações do tipo "arrastar e soltar" de elementos da interface do usuário.

 

 