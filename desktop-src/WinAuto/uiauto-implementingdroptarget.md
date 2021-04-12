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
# <a name="droptarget-control-pattern"></a><span data-ttu-id="88f0f-113">Padrão de controle DropTarget</span><span class="sxs-lookup"><span data-stu-id="88f0f-113">DropTarget Control Pattern</span></span>

<span data-ttu-id="88f0f-114">Fornece diretrizes e convenções para implementar o padrão de controle **DropTarget** usando [**IDropTargetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-idroptargetprovider), incluindo informações sobre propriedades e métodos.</span><span class="sxs-lookup"><span data-stu-id="88f0f-114">Provides guidelines and conventions for implementing the **DropTarget** control pattern by using [**IDropTargetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-idroptargetprovider), including information about properties and methods.</span></span> <span data-ttu-id="88f0f-115">O padrão de controle **DropTarget** é usado para dar suporte a controles que podem ser o destino de uma operação de arrastar e soltar.</span><span class="sxs-lookup"><span data-stu-id="88f0f-115">The **DropTarget** control pattern is used to support controls that can be the target of a drag-and-drop operation.</span></span>

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="88f0f-116">Diretrizes e convenções de implementação</span><span class="sxs-lookup"><span data-stu-id="88f0f-116">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="88f0f-117">Ao implementar o padrão de controle **DropTarget** , use as seguintes diretrizes e convenções:</span><span class="sxs-lookup"><span data-stu-id="88f0f-117">When implementing the **DropTarget** control pattern, use the following guidelines and conventions:</span></span>

-   <span data-ttu-id="88f0f-118">O padrão **DropTarget** deve ter suporte enquanto uma operação de arrastar estiver em andamento.</span><span class="sxs-lookup"><span data-stu-id="88f0f-118">The **DropTarget** pattern must be supported while a drag operation is in progress.</span></span> <span data-ttu-id="88f0f-119">Ele pode ter suporte mesmo quando uma operação de arrastar não está em andamento.</span><span class="sxs-lookup"><span data-stu-id="88f0f-119">It can be supported even when a drag operation is not in progress.</span></span>
-   <span data-ttu-id="88f0f-120">A propriedade [**IDropTargetProvider::D roptargeteffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) é necessária.</span><span class="sxs-lookup"><span data-stu-id="88f0f-120">The [**IDropTargetProvider::DropTargetEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) property is required.</span></span>
-   <span data-ttu-id="88f0f-121">A propriedade [**IDropTargetProvider::D roptargeteffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffects) é necessária quando há mais de um possível efeito de soltar para o destino.</span><span class="sxs-lookup"><span data-stu-id="88f0f-121">The [**IDropTargetProvider::DropTargetEffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffects) property is required when there is more than one possible drop effect for the target.</span></span>
-   <span data-ttu-id="88f0f-122">O elemento deve gerar eventos de propriedade alterada para as propriedades **DropTargetEffect** ([**UIA \_ DropTargetDropTargetEffectPropertyId**](uiauto-control-pattern-propids.md)) e **DropTargetEffects** ([**UIA \_ DropTargetDropTargetEffectsPropertyId**](uiauto-control-pattern-propids.md)) quando elas forem alteradas.</span><span class="sxs-lookup"><span data-stu-id="88f0f-122">The element must raise property changed events for the **DropTargetEffect** ([**UIA\_DropTargetDropTargetEffectPropertyId**](uiauto-control-pattern-propids.md)) and **DropTargetEffects** ([**UIA\_DropTargetDropTargetEffectsPropertyId**](uiauto-control-pattern-propids.md)) properties when they change.</span></span>

## <a name="required-members-for-idroptargetprovider"></a><span data-ttu-id="88f0f-123">Membros necessários para **IDropTargetProvider**</span><span class="sxs-lookup"><span data-stu-id="88f0f-123">Required Members for **IDropTargetProvider**</span></span>

<span data-ttu-id="88f0f-124">As propriedades e os métodos a seguir são necessários para implementar a interface [**IDropTargetProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idroptargetprovider) .</span><span class="sxs-lookup"><span data-stu-id="88f0f-124">The following properties and methods are required for implementing the [**IDropTargetProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idroptargetprovider) interface.</span></span>



| <span data-ttu-id="88f0f-125">Membros necessários</span><span class="sxs-lookup"><span data-stu-id="88f0f-125">Required members</span></span>                                                                              | <span data-ttu-id="88f0f-126">Tipo de membro</span><span class="sxs-lookup"><span data-stu-id="88f0f-126">Member type</span></span> | <span data-ttu-id="88f0f-127">Observações</span><span class="sxs-lookup"><span data-stu-id="88f0f-127">Notes</span></span>                                                                    |
|-----------------------------------------------------------------------------------------------|-------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="88f0f-128">**DropTargetEffect**</span><span class="sxs-lookup"><span data-stu-id="88f0f-128">**DropTargetEffect**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect)                       | <span data-ttu-id="88f0f-129">Propriedade</span><span class="sxs-lookup"><span data-stu-id="88f0f-129">Property</span></span>    | <span data-ttu-id="88f0f-130">Nenhum</span><span class="sxs-lookup"><span data-stu-id="88f0f-130">None</span></span>                                                                     |
| [<span data-ttu-id="88f0f-131">**DropTargetEffects**</span><span class="sxs-lookup"><span data-stu-id="88f0f-131">**DropTargetEffects**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffects)                     | <span data-ttu-id="88f0f-132">Propriedade</span><span class="sxs-lookup"><span data-stu-id="88f0f-132">Property</span></span>    | <span data-ttu-id="88f0f-133">Necessário se a interface "soltar" oferecer suporte a mais de um possível efeito de soltar.</span><span class="sxs-lookup"><span data-stu-id="88f0f-133">Required if the drop target supports more than one possible drop effect.</span></span> |
| [<span data-ttu-id="88f0f-134">**UIA \_ DropTarget \_ DragEnterEventId**</span><span class="sxs-lookup"><span data-stu-id="88f0f-134">**UIA\_DropTarget\_DragEnterEventId**</span></span>](uiauto-event-ids.md) | <span data-ttu-id="88f0f-135">Evento</span><span class="sxs-lookup"><span data-stu-id="88f0f-135">Event</span></span>       | <span data-ttu-id="88f0f-136">Nenhum</span><span class="sxs-lookup"><span data-stu-id="88f0f-136">None</span></span>                                                                     |
| [<span data-ttu-id="88f0f-137">**UIA \_ DropTarget \_ DragLeaveEventId**</span><span class="sxs-lookup"><span data-stu-id="88f0f-137">**UIA\_DropTarget\_DragLeaveEventId**</span></span>](uiauto-event-ids.md) | <span data-ttu-id="88f0f-138">Evento</span><span class="sxs-lookup"><span data-stu-id="88f0f-138">Event</span></span>       | <span data-ttu-id="88f0f-139">Nenhum</span><span class="sxs-lookup"><span data-stu-id="88f0f-139">None</span></span>                                                                     |
| [<span data-ttu-id="88f0f-140">**UIA \_ DropTarget \_ DroppedEventId**</span><span class="sxs-lookup"><span data-stu-id="88f0f-140">**UIA\_DropTarget\_DroppedEventId**</span></span>](uiauto-event-ids.md)     | <span data-ttu-id="88f0f-141">Evento</span><span class="sxs-lookup"><span data-stu-id="88f0f-141">Event</span></span>       | <span data-ttu-id="88f0f-142">Nenhum</span><span class="sxs-lookup"><span data-stu-id="88f0f-142">None</span></span>                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="88f0f-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="88f0f-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88f0f-144">Tipos de controle e seus padrões de controle com suporte</span><span class="sxs-lookup"><span data-stu-id="88f0f-144">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="88f0f-145">Arrastar padrão de controle</span><span class="sxs-lookup"><span data-stu-id="88f0f-145">Drag Control Pattern</span></span>](/windows/desktop/WinAuto/uiauto-implementingdrag)
</dt> <dt>

[<span data-ttu-id="88f0f-146">Visão Geral de Padrões de Controle de Automação de Interface de Usuário</span><span class="sxs-lookup"><span data-stu-id="88f0f-146">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="88f0f-147">Visão geral da árvore de automação de interface do usuário</span><span class="sxs-lookup"><span data-stu-id="88f0f-147">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> <dt>

[<span data-ttu-id="88f0f-148">Suporte à automação da interface do usuário para arrastar e soltar</span><span class="sxs-lookup"><span data-stu-id="88f0f-148">UI Automation Support for Drag-and-Drop</span></span>](ui-automation-support-for-drag-and-drop.md)
</dt> </dl>

 

 