---
title: Padrão de controle SelectionItem
description: Descreve as diretrizes e convenções para implementar o ISelectionItemProvider, incluindo informações sobre propriedades, métodos e eventos.
ms.assetid: 9314547f-7062-42db-b6a7-8a8eaef21d4e
keywords:
- Automação da interface do usuário, implementando o padrão de controle SelectionItem
- Automação da interface do usuário, padrão de controle SelectionItem
- Automação da interface do usuário, ISelectionItemProvider
- ISelectionItemProvider
- Implementando padrões de controle SelectionItem de automação da interface do usuário
- Padrões de controle SelectionItem
- padrões de controle, ISelectionItemProvider
- padrões de controle, implementando a automação da interface do usuário SelectionItem
- padrões de controle, SelectionItem
- interfaces, ISelectionItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 912be363ea8228d905a600de091d6cbe12b925fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105796163"
---
# <a name="selectionitem-control-pattern"></a><span data-ttu-id="fdf17-113">Padrão de controle SelectionItem</span><span class="sxs-lookup"><span data-stu-id="fdf17-113">SelectionItem Control Pattern</span></span>

<span data-ttu-id="fdf17-114">Descreve as diretrizes e convenções para implementar o [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider), incluindo informações sobre propriedades, métodos e eventos.</span><span class="sxs-lookup"><span data-stu-id="fdf17-114">Describes guidelines and conventions for implementing [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider), including information about properties, methods, and events.</span></span> <span data-ttu-id="fdf17-115">O padrão de controle **SelectionItem** é usado para dar suporte a controles que atuam como itens filho individuais selecionáveis de controles de contêiner que implementam [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider).</span><span class="sxs-lookup"><span data-stu-id="fdf17-115">The **SelectionItem** control pattern is used to support controls that act as individual, selectable child items of container controls that implement [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider).</span></span>

<span data-ttu-id="fdf17-116">Para obter exemplos de controles que implementam esse padrão de controle, consulte [tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="fdf17-116">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="fdf17-117">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="fdf17-117">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="fdf17-118">Diretrizes e convenções de implementação</span><span class="sxs-lookup"><span data-stu-id="fdf17-118">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="fdf17-119">Membros necessários para **ISelectionItemProvider**</span><span class="sxs-lookup"><span data-stu-id="fdf17-119">Required Members for **ISelectionItemProvider**</span></span>](#required-members-for-iselectionitemprovider)
-   [<span data-ttu-id="fdf17-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fdf17-120">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="fdf17-121">Diretrizes e convenções de implementação</span><span class="sxs-lookup"><span data-stu-id="fdf17-121">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="fdf17-122">Ao implementar o padrão de controle **SelectionItem** , observe as seguintes diretrizes e convenções:</span><span class="sxs-lookup"><span data-stu-id="fdf17-122">When implementing the **SelectionItem** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="fdf17-123">Controles de seleção única que gerenciam controles filho que implementam [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot), como o controle deslizante de **resolução de tela** na caixa de diálogo **Propriedades de exibição** para Windows, devem implementar [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider); seus filhos devem implementar [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) e [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider).</span><span class="sxs-lookup"><span data-stu-id="fdf17-123">Single-selection controls that manage child controls that implement [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot), such as the **Screen Resolution** slider in the **Display Properties** dialog for Windows, should implement [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider); their children should implement both [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) and [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider).</span></span>

## <a name="required-members-for-iselectionitemprovider"></a><span data-ttu-id="fdf17-124">Membros necessários para **ISelectionItemProvider**</span><span class="sxs-lookup"><span data-stu-id="fdf17-124">Required Members for **ISelectionItemProvider**</span></span>

<span data-ttu-id="fdf17-125">As propriedades, os métodos e os eventos a seguir são necessários para implementar a interface [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider) .</span><span class="sxs-lookup"><span data-stu-id="fdf17-125">The following properties, methods, and events are required for implementing the [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider) interface.</span></span>



| <span data-ttu-id="fdf17-126">Membros necessários</span><span class="sxs-lookup"><span data-stu-id="fdf17-126">Required members</span></span>                                                                                                                        | <span data-ttu-id="fdf17-127">Tipo de membro</span><span class="sxs-lookup"><span data-stu-id="fdf17-127">Member type</span></span> | <span data-ttu-id="fdf17-128">Observações</span><span class="sxs-lookup"><span data-stu-id="fdf17-128">Notes</span></span> |
|-----------------------------------------------------------------------------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="fdf17-129">**AddToSelection**</span><span class="sxs-lookup"><span data-stu-id="fdf17-129">**AddToSelection**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-addtoselection)                                                                  | <span data-ttu-id="fdf17-130">Método</span><span class="sxs-lookup"><span data-stu-id="fdf17-130">Method</span></span>      | <span data-ttu-id="fdf17-131">Nenhum</span><span class="sxs-lookup"><span data-stu-id="fdf17-131">None</span></span>  |
| [<span data-ttu-id="fdf17-132">**IsSelected**</span><span class="sxs-lookup"><span data-stu-id="fdf17-132">**IsSelected**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_isselected)                                                                          | <span data-ttu-id="fdf17-133">Propriedade</span><span class="sxs-lookup"><span data-stu-id="fdf17-133">Property</span></span>    | <span data-ttu-id="fdf17-134">Nenhum</span><span class="sxs-lookup"><span data-stu-id="fdf17-134">None</span></span>  |
| [<span data-ttu-id="fdf17-135">**RemoveFromSelection**</span><span class="sxs-lookup"><span data-stu-id="fdf17-135">**RemoveFromSelection**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-removefromselection)                                                        | <span data-ttu-id="fdf17-136">Método</span><span class="sxs-lookup"><span data-stu-id="fdf17-136">Method</span></span>      | <span data-ttu-id="fdf17-137">Nenhum</span><span class="sxs-lookup"><span data-stu-id="fdf17-137">None</span></span>  |
| [<span data-ttu-id="fdf17-138">**Não**</span><span class="sxs-lookup"><span data-stu-id="fdf17-138">**Select**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-select)                                                                                  | <span data-ttu-id="fdf17-139">Método</span><span class="sxs-lookup"><span data-stu-id="fdf17-139">Method</span></span>      | <span data-ttu-id="fdf17-140">Nenhum</span><span class="sxs-lookup"><span data-stu-id="fdf17-140">None</span></span>  |
| [<span data-ttu-id="fdf17-141">**SelectionContainer**</span><span class="sxs-lookup"><span data-stu-id="fdf17-141">**SelectionContainer**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer)                                                          | <span data-ttu-id="fdf17-142">Propriedade</span><span class="sxs-lookup"><span data-stu-id="fdf17-142">Property</span></span>    | <span data-ttu-id="fdf17-143">Nenhum</span><span class="sxs-lookup"><span data-stu-id="fdf17-143">None</span></span>  |
| [<span data-ttu-id="fdf17-144">**UIA \_ SelectionItem \_ ElementAddedToSelectionEventId**</span><span class="sxs-lookup"><span data-stu-id="fdf17-144">**UIA\_SelectionItem\_ElementAddedToSelectionEventId**</span></span>](uiauto-event-ids.md)         | <span data-ttu-id="fdf17-145">Evento</span><span class="sxs-lookup"><span data-stu-id="fdf17-145">Event</span></span>       | <span data-ttu-id="fdf17-146">Nenhum</span><span class="sxs-lookup"><span data-stu-id="fdf17-146">None</span></span>  |
| [<span data-ttu-id="fdf17-147">**UIA \_ SelectionItem \_ ElementRemovedFromSelectionEventId**</span><span class="sxs-lookup"><span data-stu-id="fdf17-147">**UIA\_SelectionItem\_ElementRemovedFromSelectionEventId**</span></span>](uiauto-event-ids.md) | <span data-ttu-id="fdf17-148">Evento</span><span class="sxs-lookup"><span data-stu-id="fdf17-148">Event</span></span>       | <span data-ttu-id="fdf17-149">Nenhum</span><span class="sxs-lookup"><span data-stu-id="fdf17-149">None</span></span>  |
| [<span data-ttu-id="fdf17-150">**UIA \_ SelectionItem \_ ElementSelectedEventId**</span><span class="sxs-lookup"><span data-stu-id="fdf17-150">**UIA\_SelectionItem\_ElementSelectedEventId**</span></span>](uiauto-event-ids.md)                         | <span data-ttu-id="fdf17-151">Evento</span><span class="sxs-lookup"><span data-stu-id="fdf17-151">Event</span></span>       | <span data-ttu-id="fdf17-152">Nenhum</span><span class="sxs-lookup"><span data-stu-id="fdf17-152">None</span></span>  |



 

<span data-ttu-id="fdf17-153">Se o resultado de um [**Select**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-select), um [**AddToSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-addtoselection)ou um [**RemoveFromSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-removefromselection) for um único item selecionado, um evento **ElementSelected** ([**UIA \_ SelectionItem \_ ElementSelectedEventId**](uiauto-event-ids.md)) deverá ser gerado; caso contrário, gerará eventos **ElementAddedToSelection** ([**UIA \_ SelectionItem \_ ElementAddedToSelectionEventId**](uiauto-event-ids.md)) ou **ElementRemovedFromSelection** ([**UIA \_ SelectionItem \_ ElementRemovedFromSelectionEventId**](uiauto-event-ids.md)) conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="fdf17-153">If the result of a [**Select**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-select), an [**AddToSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-addtoselection), or a [**RemoveFromSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-removefromselection) is a single selected item, an **ElementSelected** event ([**UIA\_SelectionItem\_ElementSelectedEventId**](uiauto-event-ids.md)) should be raised; otherwise raise **ElementAddedToSelection** ([**UIA\_SelectionItem\_ElementAddedToSelectionEventId**](uiauto-event-ids.md)) or **ElementRemovedFromSelection** ([**UIA\_SelectionItem\_ElementRemovedFromSelectionEventId**](uiauto-event-ids.md)) events as appropriate.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fdf17-154">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fdf17-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fdf17-155">Tipos de controle e seus padrões de controle com suporte</span><span class="sxs-lookup"><span data-stu-id="fdf17-155">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="fdf17-156">Visão Geral de Padrões de Controle de Automação de Interface de Usuário</span><span class="sxs-lookup"><span data-stu-id="fdf17-156">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="fdf17-157">Visão geral da árvore de automação de interface do usuário</span><span class="sxs-lookup"><span data-stu-id="fdf17-157">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




