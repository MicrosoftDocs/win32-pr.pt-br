---
title: Tipo de controle TabItem
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle TabItem.
ms.assetid: 97b8c043-1ac5-4e14-be80-8687300a10a2
keywords:
- Automação da interface do usuário, suporte para tipo de controle TabItem
- Automação da interface do usuário, tipo de controle TabItem
- Automação da interface do usuário, estrutura de árvore para tipo de controle TabItem
- Automação da interface do usuário, propriedades para tipo de controle TabItem
- Automação da interface do usuário, padrões de controle para o tipo de controle TabItem
- Automação da interface do usuário, eventos para o tipo de controle TabItem
- estruturas de árvore, tipo de controle TabItem
- Propriedades, tipo de controle TabItem
- padrões de controle, tipo de controle TabItem
- eventos, tipo de controle TabItem
- suporte para tipo de controle TabItem
- Tipo de controle TabItem
- tipos de controle, estrutura de árvore para o tipo de controle TabItem
- tipos de controle, padrões de controle para o tipo de controle TabItem
- tipos de controle, suporte para TabItem
- tipos de controle, TabItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e8f9f900240318de8629048f242cd755994c78
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160246"
---
# <a name="tabitem-control-type"></a><span data-ttu-id="de9ae-119">Tipo de controle TabItem</span><span class="sxs-lookup"><span data-stu-id="de9ae-119">TabItem Control Type</span></span>

<span data-ttu-id="de9ae-120">Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle **TabItem** .</span><span class="sxs-lookup"><span data-stu-id="de9ae-120">This topic provides information about Microsoft UI Automation support for the **TabItem** control type.</span></span>

<span data-ttu-id="de9ae-121">Um controle de item de guia é usado como o controle dentro de um controle guia que seleciona uma página específica a ser mostrada em uma janela.</span><span class="sxs-lookup"><span data-stu-id="de9ae-121">A tab item control is used as the control within a tab control that selects a specific page to be shown in a window.</span></span>

<span data-ttu-id="de9ae-122">As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle **TabItem** .</span><span class="sxs-lookup"><span data-stu-id="de9ae-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **TabItem** control type.</span></span> <span data-ttu-id="de9ae-123">Os requisitos de automação da interface do usuário se aplicam a todos os controles de item de guia onde a estrutura/plataforma da interface do usuário integra o suporte à automação da interface do usuário para tipos de controle</span><span class="sxs-lookup"><span data-stu-id="de9ae-123">The UI Automation requirements apply to all tab item controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="de9ae-124">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="de9ae-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="de9ae-125">Estrutura de árvore típica</span><span class="sxs-lookup"><span data-stu-id="de9ae-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="de9ae-126">Propriedades relevantes</span><span class="sxs-lookup"><span data-stu-id="de9ae-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="de9ae-127">Padrões de controle necessários</span><span class="sxs-lookup"><span data-stu-id="de9ae-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="de9ae-128">Eventos necessários</span><span class="sxs-lookup"><span data-stu-id="de9ae-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="de9ae-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="de9ae-129">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="de9ae-130">Estrutura de árvore típica</span><span class="sxs-lookup"><span data-stu-id="de9ae-130">Typical Tree Structure</span></span>

<span data-ttu-id="de9ae-131">A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence a controles de item de guia e descreve o que pode ser contido em cada exibição.</span><span class="sxs-lookup"><span data-stu-id="de9ae-131">The following table depicts a typical control and content view of the UI Automation tree that pertains to tab item controls and describes what can be contained in each view.</span></span> <span data-ttu-id="de9ae-132">Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="de9ae-132">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="de9ae-133">Exibição de controle</span><span class="sxs-lookup"><span data-stu-id="de9ae-133">Control View</span></span></th>
<th><span data-ttu-id="de9ae-134">Exibição de conteúdo</span><span class="sxs-lookup"><span data-stu-id="de9ae-134">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="de9ae-135">TabItem</span><span class="sxs-lookup"><span data-stu-id="de9ae-135">TabItem</span></span>
<ul>
<li><span data-ttu-id="de9ae-136">Imagem (0 ou 1)</span><span class="sxs-lookup"><span data-stu-id="de9ae-136">Image (0 or 1)</span></span></li>
<li><span data-ttu-id="de9ae-137">Texto</span><span class="sxs-lookup"><span data-stu-id="de9ae-137">Text</span></span></li>
<li><span data-ttu-id="de9ae-138">Painel</span><span class="sxs-lookup"><span data-stu-id="de9ae-138">Pane</span></span>
<ul>
<li><span data-ttu-id="de9ae-139">Vários controles (0 ou mais)</span><span class="sxs-lookup"><span data-stu-id="de9ae-139">Various controls (0 or more)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="de9ae-140">TabItem</span><span class="sxs-lookup"><span data-stu-id="de9ae-140">TabItem</span></span>
<ul>
<li><span data-ttu-id="de9ae-141">Painel</span><span class="sxs-lookup"><span data-stu-id="de9ae-141">Pane</span></span>
<ul>
<li><span data-ttu-id="de9ae-142">Vários controles (0 ou mais)</span><span class="sxs-lookup"><span data-stu-id="de9ae-142">Various controls (0 or more)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="de9ae-143">Propriedades relevantes</span><span class="sxs-lookup"><span data-stu-id="de9ae-143">Relevant Properties</span></span>

<span data-ttu-id="de9ae-144">A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para o tipo de controle **TabItem** .</span><span class="sxs-lookup"><span data-stu-id="de9ae-144">The following table lists the UI Automation properties whose value or definition is especially relevant to the **TabItem** control type.</span></span> <span data-ttu-id="de9ae-145">Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="de9ae-145">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="de9ae-146">Propriedade de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="de9ae-146">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="de9ae-147">Valor</span><span class="sxs-lookup"><span data-stu-id="de9ae-147">Value</span></span>       | <span data-ttu-id="de9ae-148">Observações</span><span class="sxs-lookup"><span data-stu-id="de9ae-148">Notes</span></span>                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|-------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="de9ae-149">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="de9ae-149">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="de9ae-150">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="de9ae-150">See notes.</span></span>  | <span data-ttu-id="de9ae-151">O valor dessa propriedade deve ser exclusivo entre todos os elementos de mesmo nível na exibição bruta da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="de9ae-151">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                |
| [<span data-ttu-id="de9ae-152">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="de9ae-152">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="de9ae-153">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="de9ae-153">See notes.</span></span>  | <span data-ttu-id="de9ae-154">O retângulo mais externo que contém o controle inteiro.</span><span class="sxs-lookup"><span data-stu-id="de9ae-154">The outermost rectangle that contains the whole control.</span></span>                                                                                    |
| [<span data-ttu-id="de9ae-155">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="de9ae-155">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="de9ae-156">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="de9ae-156">See notes.</span></span>  | <span data-ttu-id="de9ae-157">O controle de item de guia deve ter um ponto clicável que faz com que o item se torne selecionado.</span><span class="sxs-lookup"><span data-stu-id="de9ae-157">The tab item control must have a clickable point that causes the item to become selected.</span></span>                                                   |
| [<span data-ttu-id="de9ae-158">**UIA \_ ControllerForPropertyId**</span><span class="sxs-lookup"><span data-stu-id="de9ae-158">**UIA\_ControllerForPropertyId**</span></span>](uiauto-automation-element-propids.md)               | <span data-ttu-id="de9ae-159">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="de9ae-159">See notes.</span></span>  | <span data-ttu-id="de9ae-160">Essa propriedade pode ser usada como ponteiro para o painel de guias associado.</span><span class="sxs-lookup"><span data-stu-id="de9ae-160">This property can be used as pointer to the associated tab pane.</span></span> <span data-ttu-id="de9ae-161">Isso é útil quando não pode hospedar um painel como filho do objeto de item de guia.</span><span class="sxs-lookup"><span data-stu-id="de9ae-161">This is useful when it cannot host a pane as child of the tab item object.</span></span> |
| [<span data-ttu-id="de9ae-162">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="de9ae-162">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="de9ae-163">**TabItem**</span><span class="sxs-lookup"><span data-stu-id="de9ae-163">**TabItem**</span></span> | <span data-ttu-id="de9ae-164">Esse valor é o mesmo para todas as estruturas de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="de9ae-164">This value is the same for all UI frameworks.</span></span>                                                                                               |
| [<span data-ttu-id="de9ae-165">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="de9ae-165">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="de9ae-166">TRUE</span><span class="sxs-lookup"><span data-stu-id="de9ae-166">TRUE</span></span>        | <span data-ttu-id="de9ae-167">O controle de item de guia é sempre incluído na exibição de conteúdo da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="de9ae-167">The tab item control is always included in the content view of the UI Automation tree.</span></span>                                                      |
| [<span data-ttu-id="de9ae-168">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="de9ae-168">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="de9ae-169">TRUE</span><span class="sxs-lookup"><span data-stu-id="de9ae-169">TRUE</span></span>        | <span data-ttu-id="de9ae-170">O controle de item de guia sempre é incluído no modo de exibição de controle da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="de9ae-170">The tab item control is always included in the control view of the UI Automation tree.</span></span>                                                      |
| [<span data-ttu-id="de9ae-171">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="de9ae-171">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="de9ae-172">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="de9ae-172">See notes.</span></span>  | <span data-ttu-id="de9ae-173">Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="de9ae-173">If the control can receive keyboard focus, it must support this property.</span></span>                                                                   |
| [<span data-ttu-id="de9ae-174">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="de9ae-174">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="de9ae-175">Nulo</span><span class="sxs-lookup"><span data-stu-id="de9ae-175">Null</span></span>        | <span data-ttu-id="de9ae-176">O controle de item de guia não tem um rótulo de texto estático.</span><span class="sxs-lookup"><span data-stu-id="de9ae-176">The tab item control does not have a static text label.</span></span>                                                                                     |
| [<span data-ttu-id="de9ae-177">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="de9ae-177">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="de9ae-178">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="de9ae-178">See notes.</span></span>  | <span data-ttu-id="de9ae-179">Cadeia de caracteres localizada correspondente ao tipo de controle **TabItem** .</span><span class="sxs-lookup"><span data-stu-id="de9ae-179">Localized string corresponding to the **TabItem** control type.</span></span> <span data-ttu-id="de9ae-180">O valor padrão é "item de guia" para en-US ou inglês (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="de9ae-180">The default value is "tab item" for en-US or English (United States).</span></span>       |
| [<span data-ttu-id="de9ae-181">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="de9ae-181">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="de9ae-182">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="de9ae-182">See notes.</span></span>  | <span data-ttu-id="de9ae-183">O controle de item de guia rotulado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="de9ae-183">The tab item control self-labeled.</span></span>                                                                                                          |



 

## <a name="required-control-patterns"></a><span data-ttu-id="de9ae-184">Padrões de controle necessários</span><span class="sxs-lookup"><span data-stu-id="de9ae-184">Required Control Patterns</span></span>

<span data-ttu-id="de9ae-185">A tabela a seguir lista os padrões de controle de automação da interface do usuário que devem ter suporte em todos os controles de item de guia.</span><span class="sxs-lookup"><span data-stu-id="de9ae-185">The following table lists the UI Automation control patterns required to be supported by all tab item controls.</span></span> <span data-ttu-id="de9ae-186">Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="de9ae-186">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="de9ae-187">Padrão de controle</span><span class="sxs-lookup"><span data-stu-id="de9ae-187">Control Pattern</span></span>                                                 | <span data-ttu-id="de9ae-188">Suporte</span><span class="sxs-lookup"><span data-stu-id="de9ae-188">Support</span></span>  | <span data-ttu-id="de9ae-189">Observações</span><span class="sxs-lookup"><span data-stu-id="de9ae-189">Notes</span></span>                                                                                                                    |
|-----------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="de9ae-190">**ISelectionItemProvider**</span><span class="sxs-lookup"><span data-stu-id="de9ae-190">**ISelectionItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider) | <span data-ttu-id="de9ae-191">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="de9ae-191">Required</span></span> | <span data-ttu-id="de9ae-192">O controle de item de guia deve dar suporte a [**IUIAutomationSelectionItemPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationselectionitempattern).</span><span class="sxs-lookup"><span data-stu-id="de9ae-192">The tab item control must support [**IUIAutomationSelectionItemPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationselectionitempattern).</span></span> |
| [<span data-ttu-id="de9ae-193">**IInvokeProvider**</span><span class="sxs-lookup"><span data-stu-id="de9ae-193">**IInvokeProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)               | <span data-ttu-id="de9ae-194">Nunca</span><span class="sxs-lookup"><span data-stu-id="de9ae-194">Never</span></span>    | <span data-ttu-id="de9ae-195">O controle de item de guia nunca dá suporte a [**IUIAutomationInvokePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationinvokepattern).</span><span class="sxs-lookup"><span data-stu-id="de9ae-195">The tab item control never supports [**IUIAutomationInvokePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationinvokepattern).</span></span>             |



 

## <a name="required-events"></a><span data-ttu-id="de9ae-196">Eventos necessários</span><span class="sxs-lookup"><span data-stu-id="de9ae-196">Required Events</span></span>

<span data-ttu-id="de9ae-197">A tabela a seguir lista os eventos de automação da interface do usuário aos quais os controles de item de guia são necessários para dar suporte.</span><span class="sxs-lookup"><span data-stu-id="de9ae-197">The following table lists the UI Automation events that tab item controls are required to support.</span></span> <span data-ttu-id="de9ae-198">Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="de9ae-198">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="de9ae-199">Evento de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="de9ae-199">UI Automation Event</span></span>                                                                                                                     | <span data-ttu-id="de9ae-200">Observações</span><span class="sxs-lookup"><span data-stu-id="de9ae-200">Notes</span></span>                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="de9ae-201">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="de9ae-201">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                        |                                                                                                                            |
| <span data-ttu-id="de9ae-202">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="de9ae-202">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>   |                                                                                                                            |
| <span data-ttu-id="de9ae-203">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="de9ae-203">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                   | <span data-ttu-id="de9ae-204">Se o controle oferecer suporte à propriedade [**IsEnabled**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="de9ae-204">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="de9ae-205">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="de9ae-205">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>               | <span data-ttu-id="de9ae-206">Se o controle oferecer suporte à propriedade [**IsOffscreen**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="de9ae-206">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="de9ae-207">**UIA \_ SelectionItem \_ ElementRemovedFromSelectionEventId**</span><span class="sxs-lookup"><span data-stu-id="de9ae-207">**UIA\_SelectionItem\_ElementRemovedFromSelectionEventId**</span></span>](uiauto-event-ids.md) |                                                                                                                            |
| [<span data-ttu-id="de9ae-208">**UIA \_ SelectionItem \_ ElementSelectedEventId**</span><span class="sxs-lookup"><span data-stu-id="de9ae-208">**UIA\_SelectionItem\_ElementSelectedEventId**</span></span>](uiauto-event-ids.md)                         |                                                                                                                            |
| [<span data-ttu-id="de9ae-209">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="de9ae-209">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                    |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="de9ae-210">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="de9ae-210">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="de9ae-211">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="de9ae-211">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="de9ae-212">Visão Geral dos Tipos de Controle de Automação de Interface do Usuário</span><span class="sxs-lookup"><span data-stu-id="de9ae-212">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="de9ae-213">Visão geral de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="de9ae-213">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




