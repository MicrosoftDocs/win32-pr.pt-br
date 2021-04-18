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
# <a name="ui-automation-support-for-drag-and-drop"></a><span data-ttu-id="30e89-112">Suporte à automação da interface do usuário para arrastar e soltar</span><span class="sxs-lookup"><span data-stu-id="30e89-112">UI Automation Support for Drag-and-Drop</span></span>

<span data-ttu-id="30e89-113">A automação da interface do usuário da Microsoft define dois padrões de controle para dar suporte a cenários de arrastar e soltar, o padrão de controle de [arrastar](/windows/desktop/WinAuto/uiauto-implementingdrag) e o padrão de controle [DropTarget](/windows/desktop/WinAuto/uiauto-implementingdroptarget) .</span><span class="sxs-lookup"><span data-stu-id="30e89-113">Microsoft UI Automation defines two control patterns for supporting drag-and-drop scenarios, the [Drag](/windows/desktop/WinAuto/uiauto-implementingdrag) control pattern, and the [DropTarget](/windows/desktop/WinAuto/uiauto-implementingdroptarget) control pattern.</span></span> <span data-ttu-id="30e89-114">Você implementa o padrão de controle de arrastar para um elemento que pode ser arrastado e o padrão de controle DropTarget para um elemento que pode receber um elemento arrastado; ou seja, um destino de soltura.</span><span class="sxs-lookup"><span data-stu-id="30e89-114">You implement the Drag control pattern for an element that can be dragged, and the DropTarget control pattern for an element that can receive a dragged element; that is, a drop target.</span></span> <span data-ttu-id="30e89-115">Os dois padrões de controle expõem informações que uma tecnologia assistencial pode usar para ajudar um usuário de acessibilidade a concluir uma operação de arrastar e soltar.</span><span class="sxs-lookup"><span data-stu-id="30e89-115">The two control patterns expose information that an assistive technology can use to help an accessibility user complete a drag-and-drop operation.</span></span>

-   [<span data-ttu-id="30e89-116">Arrastando estilos</span><span class="sxs-lookup"><span data-stu-id="30e89-116">Dragging Styles</span></span>](#dragging-styles)
    -   [<span data-ttu-id="30e89-117">Estilo de origem/destino</span><span class="sxs-lookup"><span data-stu-id="30e89-117">Source/target Style</span></span>](#sourcetarget-style)
    -   [<span data-ttu-id="30e89-118">Estilo somente origem</span><span class="sxs-lookup"><span data-stu-id="30e89-118">Source-only Style</span></span>](#source-only-style)
-   [<span data-ttu-id="30e89-119">Arrastando vários itens</span><span class="sxs-lookup"><span data-stu-id="30e89-119">Dragging Multiple Items</span></span>](#dragging-multiple-items)
-   [<span data-ttu-id="30e89-120">Interfaces de cliente para arrastar e soltar</span><span class="sxs-lookup"><span data-stu-id="30e89-120">Client Interfaces for Drag-and-Drop</span></span>](#client-interfaces-for-drag-and-drop)

## <a name="dragging-styles"></a><span data-ttu-id="30e89-121">Arrastando estilos</span><span class="sxs-lookup"><span data-stu-id="30e89-121">Dragging Styles</span></span>

<span data-ttu-id="30e89-122">Ao implementar o padrão de controle de [arrastar](/windows/desktop/WinAuto/uiauto-implementingdrag) para um elemento arrastável, você precisa decidir se deseja implementar o estilo de arrastar de *origem/destino* ou o estilo de arrastar *somente origem* .</span><span class="sxs-lookup"><span data-stu-id="30e89-122">When you implement the [Drag](/windows/desktop/WinAuto/uiauto-implementingdrag) control pattern for a draggable element, you need to decide whether to implement the *source/target* dragging style, or the *source-only* dragging style.</span></span>

### <a name="sourcetarget-style"></a><span data-ttu-id="30e89-123">Estilo de origem/destino</span><span class="sxs-lookup"><span data-stu-id="30e89-123">Source/target Style</span></span>

<span data-ttu-id="30e89-124">No estilo de origem/destino de arrastar e soltar, o elemento arrastado (a "origem") e o elemento de destino (o "destino") são distintos e cada um gera um conjunto distinto de eventos.</span><span class="sxs-lookup"><span data-stu-id="30e89-124">In the source/target style of drag-and-drop, the dragged element (the "source") and the drop-target element (the "target") are distinct, and each raises a distinct set of events.</span></span> <span data-ttu-id="30e89-125">Este é o ciclo de vida de uma operação de arrastar que usa o estilo de origem/destino:</span><span class="sxs-lookup"><span data-stu-id="30e89-125">Here's the life cycle for a drag operation that uses the source/target style:</span></span> <dl> <span data-ttu-id="30e89-126">Quando o usuário inicia uma operação de arrastar:</span><span class="sxs-lookup"><span data-stu-id="30e89-126">When the user starts a drag operation:</span></span>

-   <span data-ttu-id="30e89-127">A origem gera o evento DragStart ([**UIA \_ Drag \_ DragStartEventId**](uiauto-event-ids.md)).</span><span class="sxs-lookup"><span data-stu-id="30e89-127">The source raises the DragStart ([**UIA\_Drag\_DragStartEventId**](uiauto-event-ids.md)) event.</span></span>
-   <span data-ttu-id="30e89-128">A fonte define a propriedade [**IDragProvider:: iscapturado**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) como **true**.</span><span class="sxs-lookup"><span data-stu-id="30e89-128">The source sets the [**IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) property to **TRUE**.</span></span>
-   <span data-ttu-id="30e89-129">Os destinos atualizam suas propriedades [**DropTargetEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) .</span><span class="sxs-lookup"><span data-stu-id="30e89-129">Targets update their [**DropTargetEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) properties.</span></span>

  
<span data-ttu-id="30e89-130">Quando a operação de arrastar entra em uma região de destino:</span><span class="sxs-lookup"><span data-stu-id="30e89-130">When the drag operation enters a target region:</span></span>

-   <span data-ttu-id="30e89-131">O destino gera o evento DragEnter ([**UIA \_ DropTarget \_ DragEnterEventId**](uiauto-event-ids.md)).</span><span class="sxs-lookup"><span data-stu-id="30e89-131">The target raises the DragEnter ([**UIA\_DropTarget\_DragEnterEventId**](uiauto-event-ids.md)) event.</span></span>

  
<span data-ttu-id="30e89-132">Quando a operação de arrastar sair de uma região de destino:</span><span class="sxs-lookup"><span data-stu-id="30e89-132">When the drag operation leaves a target region:</span></span>

-   <span data-ttu-id="30e89-133">O destino gera o evento DragLeave ([**UIA \_ DropTarget \_ DragLeaveEventId**](uiauto-event-ids.md)).</span><span class="sxs-lookup"><span data-stu-id="30e89-133">The target raises the DragLeave ([**UIA\_DropTarget\_DragLeaveEventId**](uiauto-event-ids.md)) event.</span></span>

  
<span data-ttu-id="30e89-134">Quando o usuário libera o item arrastado em um não destino:</span><span class="sxs-lookup"><span data-stu-id="30e89-134">When the user releases the dragged item over a non-target:</span></span>

-   <span data-ttu-id="30e89-135">A origem gera o evento DragCancel ([**UIA \_ Drag \_ DragCancelEventId**](uiauto-event-ids.md)).</span><span class="sxs-lookup"><span data-stu-id="30e89-135">The source raises the DragCancel ([**UIA\_Drag\_DragCancelEventId**](uiauto-event-ids.md)) event.</span></span>
-   <span data-ttu-id="30e89-136">A fonte define a propriedade [**IDragProvider:: iscapturado**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) como **false**.</span><span class="sxs-lookup"><span data-stu-id="30e89-136">The source sets the [**IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) property to **FALSE**.</span></span>

  
<span data-ttu-id="30e89-137">Quando o usuário libera o item arrastado sobre um destino:</span><span class="sxs-lookup"><span data-stu-id="30e89-137">When the user releases the dragged item over a target:</span></span>

-   <span data-ttu-id="30e89-138">A origem gera o evento DragComplete ([**UIA \_ Drag \_ DragCompleteEventId**](uiauto-event-ids.md)).</span><span class="sxs-lookup"><span data-stu-id="30e89-138">The source raises the DragComplete ([**UIA\_Drag\_DragCompleteEventId**](uiauto-event-ids.md)) event.</span></span>
-   <span data-ttu-id="30e89-139">A fonte define a propriedade [**IDragProvider:: iscapturado**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) como **false**.</span><span class="sxs-lookup"><span data-stu-id="30e89-139">The source sets the [**IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) property to **FALSE**.</span></span>
-   <span data-ttu-id="30e89-140">O destino define a propriedade [**IDropTargetProvider::D roptargeteffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) para indicar o efeito que ocorreu.</span><span class="sxs-lookup"><span data-stu-id="30e89-140">The target sets the [**IDropTargetProvider::DropTargetEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) property to indicate the effect that occurred.</span></span>
-   <span data-ttu-id="30e89-141">O destino gera o evento solto ([**UIA \_ DropTarget \_ DroppedEventId**](uiauto-event-ids.md)).</span><span class="sxs-lookup"><span data-stu-id="30e89-141">The target raises the Dropped ([**UIA\_DropTarget\_DroppedEventId**](uiauto-event-ids.md)) event.</span></span>

  
</dl>

<span data-ttu-id="30e89-142">Os eventos dos objetos de origem e de destino estão fortemente relacionados, mas distintos.</span><span class="sxs-lookup"><span data-stu-id="30e89-142">The events from the source and target objects are closely related, but distinct.</span></span> <span data-ttu-id="30e89-143">Os dados sobre o que está sendo arrastado vêm da origem, enquanto os dados sobre "o que poderia acontecer" e "o que aconteceu" vêm do destino.</span><span class="sxs-lookup"><span data-stu-id="30e89-143">The data about what is being dragged comes from the source, while the data about "what could happen" and "what did happen" comes from the target.</span></span>

<span data-ttu-id="30e89-144">Quando uma operação de arrastar está em andamento, o item arrastado pode ser arrastado para dentro e para fora das regiões de destino quantas vezes a operação for concluída.</span><span class="sxs-lookup"><span data-stu-id="30e89-144">When a drag operation is in progress, the dragged item can be dragged in and out of target regions any number of times before the operation completes.</span></span>

<span data-ttu-id="30e89-145">Qualquer destino de soltura que precise atualizar sua propriedade [**IDropTargetProvider::D roptargeteffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) de forma dinâmica deve gerar um evento de alteração de propriedade adicional nessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="30e89-145">Any drop target that needs to update its [**IDropTargetProvider::DropTargetEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) property on the fly should raise an additional property changed event on that property.</span></span>

### <a name="source-only-style"></a><span data-ttu-id="30e89-146">Estilo somente origem</span><span class="sxs-lookup"><span data-stu-id="30e89-146">Source-only Style</span></span>

<span data-ttu-id="30e89-147">O estilo de arrastar somente origem permite que um provedor Evite implementar destinos de destino.</span><span class="sxs-lookup"><span data-stu-id="30e89-147">The source-only dragging style lets a provider avoid implementing drop targets.</span></span> <span data-ttu-id="30e89-148">Não implementar destinos de destino ajuda a reduzir o custo de implementação, mas não dá aos aplicativos cliente de acessibilidade informações sobre o objeto que recebeu a queda.</span><span class="sxs-lookup"><span data-stu-id="30e89-148">Not implementing drop targets helps lower the implementation cost, but does not give accessibility client applications any information about the object that received the drop.</span></span> <span data-ttu-id="30e89-149">Este é o ciclo de vida de uma operação de arrastar que usa o estilo somente origem:</span><span class="sxs-lookup"><span data-stu-id="30e89-149">Here's the life cycle for a drag operation that uses the source-only style:</span></span> <dl> <span data-ttu-id="30e89-150">Quando o usuário inicia uma operação de arrastar:</span><span class="sxs-lookup"><span data-stu-id="30e89-150">When the user starts a drag operation:</span></span>

-   <span data-ttu-id="30e89-151">A origem gera o evento DragStart ([**UIA \_ Drag \_ DragStartEventId**](uiauto-event-ids.md)).</span><span class="sxs-lookup"><span data-stu-id="30e89-151">The source raises the DragStart ([**UIA\_Drag\_DragStartEventId**](uiauto-event-ids.md)) event.</span></span>
-   <span data-ttu-id="30e89-152">A fonte define a propriedade [**IDragProvider:: iscapturado**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) como **true**.</span><span class="sxs-lookup"><span data-stu-id="30e89-152">The source sets the [**IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) property to **TRUE**.</span></span>

  
<span data-ttu-id="30e89-153">Quando a operação de arrastar entra em uma região de destino:</span><span class="sxs-lookup"><span data-stu-id="30e89-153">When the drag operation enters a target region:</span></span>

-   <span data-ttu-id="30e89-154">A fonte define a propriedade [**IDragProvider::D ropeffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) como o valor apropriado.</span><span class="sxs-lookup"><span data-stu-id="30e89-154">The source sets the [**IDragProvider::DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) property to the appropriate value.</span></span>

  
<span data-ttu-id="30e89-155">Quando a operação de arrastar sair de uma região de destino:</span><span class="sxs-lookup"><span data-stu-id="30e89-155">When the drag operation leaves a target region:</span></span>

-   <span data-ttu-id="30e89-156">A fonte define a propriedade [**IDragProvider::D ropeffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) como o valor apropriado.</span><span class="sxs-lookup"><span data-stu-id="30e89-156">The source sets the [**IDragProvider::DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) property to the appropriate value.</span></span>

  
<span data-ttu-id="30e89-157">Quando o usuário libera o item arrastado em um não destino:</span><span class="sxs-lookup"><span data-stu-id="30e89-157">When the user releases the dragged item over a non-target:</span></span>

-   <span data-ttu-id="30e89-158">A origem gera o evento DragCancel ([**UIA \_ Drag \_ DragCancelEventId**](uiauto-event-ids.md)).</span><span class="sxs-lookup"><span data-stu-id="30e89-158">The source raises the DragCancel ([**UIA\_Drag\_DragCancelEventId**](uiauto-event-ids.md)) event.</span></span>
-   <span data-ttu-id="30e89-159">A fonte define a propriedade [**IDragProvider:: iscapturado**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) como **false**.</span><span class="sxs-lookup"><span data-stu-id="30e89-159">The source sets the [**IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) property to **FALSE**.</span></span>

  
<span data-ttu-id="30e89-160">Quando o usuário libera o item arrastado sobre um destino:</span><span class="sxs-lookup"><span data-stu-id="30e89-160">When the user releases the dragged item over a target:</span></span>

-   <span data-ttu-id="30e89-161">A origem gera o evento DragComplete ([**UIA \_ Drag \_ DragCompleteEventId**](uiauto-event-ids.md)).</span><span class="sxs-lookup"><span data-stu-id="30e89-161">The source raises the DragComplete ([**UIA\_Drag\_DragCompleteEventId**](uiauto-event-ids.md)) event.</span></span>
-   <span data-ttu-id="30e89-162">A fonte define a propriedade [**IDragProvider::D ropeffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) para indicar o efeito que ocorreu quando o item foi Descartado.</span><span class="sxs-lookup"><span data-stu-id="30e89-162">The source sets the [**IDragProvider::DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) property to indicate the effect that took place when the item was dropped.</span></span>

  
</dl>

## <a name="dragging-multiple-items"></a><span data-ttu-id="30e89-163">Arrastando vários itens</span><span class="sxs-lookup"><span data-stu-id="30e89-163">Dragging Multiple Items</span></span>

<span data-ttu-id="30e89-164">Se um provedor implementar operações de arrastar e soltar em que o usuário pode arrastar vários objetos ao mesmo tempo, o provedor usará os estilos de origem/destino ou somente origem, conforme descrito na seção anterior, mas com uma pequena diferença.</span><span class="sxs-lookup"><span data-stu-id="30e89-164">If a provider implements drag-and-drop operations where the user can drag multiple objects at the same time, the provider uses the source/target or source-only styles as described in the previous section, but with a small difference.</span></span> <span data-ttu-id="30e89-165">Quando o usuário inicia a operação de arrastar, o provedor cria um elemento de origem mestre que representa o conjunto completo de itens que estão sendo arrastados.</span><span class="sxs-lookup"><span data-stu-id="30e89-165">When the user begins the drag operation, the provider creates a master source element that represents the full set of items that are being dragged.</span></span> <span data-ttu-id="30e89-166">O elemento de origem mestre gera todos os eventos em nome do conjunto de itens arrastados; os itens não geram nenhum evento próprio.</span><span class="sxs-lookup"><span data-stu-id="30e89-166">The master source element raises all events on behalf of the set of dragged items; the items don't raise any events of their own.</span></span><dl> <span data-ttu-id="30e89-167">Quando o usuário inicia uma operação de arrastar:</span><span class="sxs-lookup"><span data-stu-id="30e89-167">When the user starts a drag operation:</span></span>

-   <span data-ttu-id="30e89-168">O provedor cria o elemento de origem mestre.</span><span class="sxs-lookup"><span data-stu-id="30e89-168">The provider creates the master source element.</span></span>
-   <span data-ttu-id="30e89-169">O elemento Source mestre gera o evento DragStart ([**UIA \_ Drag \_ DragStartEventId**](uiauto-event-ids.md)).</span><span class="sxs-lookup"><span data-stu-id="30e89-169">The master source element raises the DragStart ([**UIA\_Drag\_DragStartEventId**](uiauto-event-ids.md)) event.</span></span>
-   <span data-ttu-id="30e89-170">O elemento de origem mestre define a propriedade [**IDragProvider:: iscapturado**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) como **true**.</span><span class="sxs-lookup"><span data-stu-id="30e89-170">The master source element sets the [**IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) property to **TRUE**.</span></span>
-   <span data-ttu-id="30e89-171">O elemento de origem mestre atualiza a lista de itens capturados para incluir todos os itens que estão sendo arrastados para que o método [**GetGrabbedItems**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-getgrabbeditems) possa recuperar a lista.</span><span class="sxs-lookup"><span data-stu-id="30e89-171">The master source element updates the list of grabbed items to include all items being dragged so that the [**GetGrabbedItems**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-getgrabbeditems) method can retrieve the list.</span></span>

  
</dl>

<span data-ttu-id="30e89-172">Para esse ponto, o elemento de origem mestre executa a mesma função que o elemento de origem, conforme descrito na seção anterior.</span><span class="sxs-lookup"><span data-stu-id="30e89-172">For that point on, the master source element performs the same role as that of the source element as described in the previous section.</span></span>

## <a name="client-interfaces-for-drag-and-drop"></a><span data-ttu-id="30e89-173">Interfaces de cliente para arrastar e soltar</span><span class="sxs-lookup"><span data-stu-id="30e89-173">Client Interfaces for Drag-and-Drop</span></span>

<span data-ttu-id="30e89-174">Os aplicativos cliente de automação da interface do usuário usam as interfaces [**IUIAutomationDragPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) e [**IUIAutomationDropTargetPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern) para acessar informações do tipo "arrastar e soltar" de elementos da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="30e89-174">UI Automation client applications use the [**IUIAutomationDragPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) and [**IUIAutomationDropTargetPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern) interfaces to access drag-and-drop information from UI elements.</span></span>

 

 