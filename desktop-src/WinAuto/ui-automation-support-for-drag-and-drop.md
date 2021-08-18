---
title: Automação da Interface do Usuário suporte para arrastar e soltar
description: Este tópico descreve os padrões de controle que expõem informações sobre a funcionalidade do tipo "arrastar e soltar" de um elemento.
ms.assetid: FFF5A296-C9FF-4B47-AAF8-A9DD581D9DBE
keywords:
- Automação da Interface do Usuário, suporte para arrastar e soltar
- Automação da Interface do Usuário,Visão geral do padrão de arrastar
- Automação da Interface do Usuário,visão geral do padrão DropTarget
- Automação da Interface do Usuário visão geral do "arrastar e soltar"
- padrões do "arrastar e soltar", sobre
- Arrastar padrão de controle
- Padrão de controle DropTarget
- padrões de controle, Arrastar
- padrões de controle, DropTarget
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eab48f4319c51a5ccbbaadae22f1ae337740df5b6d0fdf325a01ba1323f8630
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133559"
---
# <a name="ui-automation-support-for-drag-and-drop"></a>Automação da Interface do Usuário suporte para arrastar e soltar

O Microsoft Automação da Interface do Usuário define dois padrões de controle para dar suporte a cenários de arrastar e soltar, o padrão de controle [Arrastar](/windows/desktop/WinAuto/uiauto-implementingdrag) e o [padrão de controle DropTarget.](/windows/desktop/WinAuto/uiauto-implementingdroptarget) Você implementa o padrão de controle Arrastar para um elemento que pode ser arrastado e o padrão de controle DropTarget para um elemento que pode receber um elemento arrastado; ou seja, um destino de soltar. Os dois padrões de controle expõem informações que uma tecnologia adaptativa pode usar para ajudar um usuário de acessibilidade a concluir uma operação do tipo "arrastar e soltar".

-   [Arrastando estilos](#dragging-styles)
    -   [Estilo de origem/destino](#sourcetarget-style)
    -   [Estilo somente de origem](#source-only-style)
-   [Arrastando vários itens](#dragging-multiple-items)
-   [Interfaces de cliente para arrastar e soltar](#client-interfaces-for-drag-and-drop)

## <a name="dragging-styles"></a>Arrastando estilos

Ao implementar o [padrão](/windows/desktop/WinAuto/uiauto-implementingdrag) de controle Arrastar para um elemento que pode ser arrastado, você  precisa decidir se deve implementar o estilo de arrastar de *origem/destino* ou o estilo de arrastar somente origem.

### <a name="sourcetarget-style"></a>Estilo de origem/destino

No estilo de origem/destino do tipo "arrastar e soltar", o elemento arrastado (a "origem") e o elemento drop-target (o "destino") são distintos e cada um gera um conjunto distinto de eventos. Este é o ciclo de vida de uma operação de arrastar que usa o estilo de origem/destino: <dl> Quando o usuário inicia uma operação de arrastar:

-   A origem gera o evento DragStart ([**UIA \_ \_ DragStartEventId**](uiauto-event-ids.md)).
-   A origem define [**a propriedade IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) como **TRUE.**
-   Os destinos atualizam [**suas propriedades DropTargetEffect.**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect)

  
Quando a operação de arrastar entra em uma região de destino:

-   O destino gera o evento DragEnter ([**UIA \_ DropTarget \_ DragEnterEventId**](uiauto-event-ids.md)).

  
Quando a operação de arrastar sai de uma região de destino:

-   O destino gera o evento DragLeave ([**UIA \_ DropTarget \_ DragLeaveEventId**](uiauto-event-ids.md)).

  
Quando o usuário libera o item arrastado sobre um não destino:

-   A origem gera o evento DragCancel ([**UIA \_ \_ DragCancelEventId**](uiauto-event-ids.md)).
-   A origem define [**a propriedade IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) como **FALSE.**

  
Quando o usuário libera o item arrastado sobre um destino:

-   A origem gera o evento DragComplete ([**UIA \_ \_ DragCompleteEventId**](uiauto-event-ids.md)).
-   A origem define [**a propriedade IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) como **FALSE.**
-   O destino define a [**propriedade IDropTargetProvider::D ropTargetEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) para indicar o efeito que ocorreu.
-   O destino gera o evento Dropped ([**UIA \_ DropTarget \_ DroppedEventId**](uiauto-event-ids.md)).

  
</dl>

Os eventos dos objetos de origem e destino estão intimamente relacionados, mas distintos. Os dados sobre o que está sendo arrastado vêm da origem, enquanto os dados sobre "o que poderia acontecer" e "o que aconteceu" vêm do destino.

Quando uma operação de arrastar está em andamento, o item arrastado pode ser arrastado para dentro e para fora das regiões de destino qualquer número de vezes antes que a operação seja concluída.

Qualquer destino de soltar que precise atualizar sua propriedade [**IDropTargetProvider::D ropTargetEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) em tempo real deverá gerar um evento de propriedade adicional alterado nessa propriedade.

### <a name="source-only-style"></a>Estilo somente de origem

O estilo de arrastar somente origem permite que um provedor evite implementar destinos de soltar. Não implementar destinos de soltar ajuda a reduzir o custo de implementação, mas não oferece aos aplicativos cliente de acessibilidade nenhuma informação sobre o objeto que recebeu a queda. Este é o ciclo de vida de uma operação de arrastar que usa o estilo somente de origem: <dl> Quando o usuário inicia uma operação de arrastar:

-   A origem gera o evento DragStart ([**UIA \_ \_ DragStartEventId**](uiauto-event-ids.md)).
-   A origem define [**a propriedade IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) como **TRUE.**

  
Quando a operação de arrastar entra em uma região de destino:

-   A origem define [**a propriedade IDragProvider::D ropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) como o valor apropriado.

  
Quando a operação de arrastar sai de uma região de destino:

-   A origem define [**a propriedade IDragProvider::D ropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) como o valor apropriado.

  
Quando o usuário libera o item arrastado sobre um não destino:

-   A origem gera o evento DragCancel ([**UIA \_ \_ DragCancelEventId**](uiauto-event-ids.md)).
-   A origem define [**a propriedade IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) como **FALSE.**

  
Quando o usuário libera o item arrastado sobre um destino:

-   A origem gera o evento DragComplete ([**UIA \_ \_ DragCompleteEventId**](uiauto-event-ids.md)).
-   A origem define [**a propriedade IDragProvider::D ropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) para indicar o efeito que ocorreu quando o item foi descartado.

  
</dl>

## <a name="dragging-multiple-items"></a>Arrastando vários itens

Se um provedor implementar operações do tipo "arrastar e soltar", em que o usuário possa arrastar vários objetos ao mesmo tempo, o provedor usará os estilos de origem/destino ou somente origem, conforme descrito na seção anterior, mas com uma pequena diferença. Quando o usuário inicia a operação de arrastar, o provedor cria um elemento de origem mestre que representa o conjunto completo de itens que estão sendo arrastados. O elemento de origem mestre gera todos os eventos em nome do conjunto de itens arrastados; os itens não adem eventos próprios.<dl> Quando o usuário inicia uma operação de arrastar:

-   O provedor cria o elemento de origem mestre.
-   O elemento de origem mestre gera o evento DragStart ([**UIA \_ \_ DragStartEventId**](uiauto-event-ids.md)).
-   O elemento de origem mestre define [**a propriedade IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) como **TRUE.**
-   O elemento de origem mestre atualiza a lista de itens capturados para incluir todos os itens que estão sendo arrastados para que o [**método GetGrabbedItems**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-getgrabbeditems) possa recuperar a lista.

  
</dl>

Para esse ponto em diante, o elemento de origem mestre executa a mesma função que a do elemento de origem, conforme descrito na seção anterior.

## <a name="client-interfaces-for-drag-and-drop"></a>Interfaces de cliente para arrastar e soltar

Automação da Interface do Usuário aplicativos cliente usam as interfaces [**IUIAutomationDragPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) e [**IUIAutomationDropTargetPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern) para acessar informações do arrastar e soltar de elementos da interface do usuário.

 

 