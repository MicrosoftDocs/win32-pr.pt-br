---
title: Tipo de controle HeaderItem
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle HeaderItem.
ms.assetid: c70420d6-d9f3-47c8-a09f-35ed170f815f
keywords:
- Automação da interface do usuário, suporte para tipo de controle HeaderItem
- Automação da interface do usuário, tipo de controle HeaderItem
- Automação da interface do usuário, estrutura de árvore para tipo de controle HeaderItem
- Automação da interface do usuário, propriedades para tipo de controle HeaderItem
- Automação da interface do usuário, padrões de controle para o tipo de controle HeaderItem
- Automação da interface do usuário, eventos para tipo de controle HeaderItem
- estruturas de árvore, tipo de controle HeaderItem
- Propriedades, tipo de controle HeaderItem
- padrões de controle, tipo de controle HeaderItem
- eventos, tipo de controle HeaderItem
- suporte para tipo de controle HeaderItem
- Tipo de controle HeaderItem
- tipos de controle, estrutura de árvore para tipo de controle HeaderItem
- tipos de controle, padrões de controle para o tipo de controle HeaderItem
- tipos de controle, suporte para HeaderItem
- tipos de controle, HeaderItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bab61f92a6ab4db221810f9f083279ade4bf353
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105784540"
---
# <a name="headeritem-control-type"></a><span data-ttu-id="0fa4f-119">Tipo de controle HeaderItem</span><span class="sxs-lookup"><span data-stu-id="0fa4f-119">HeaderItem Control Type</span></span>

<span data-ttu-id="0fa4f-120">Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle **HeaderItem** .</span><span class="sxs-lookup"><span data-stu-id="0fa4f-120">This topic provides information about Microsoft UI Automation support for the **HeaderItem** control type.</span></span>

<span data-ttu-id="0fa4f-121">O tipo de controle **HeaderItem** fornece um rótulo Visual para uma linha ou coluna de informações.</span><span class="sxs-lookup"><span data-stu-id="0fa4f-121">The **HeaderItem** control type provides a visual label for a row or column of information.</span></span>

<span data-ttu-id="0fa4f-122">As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle **HeaderItem** .</span><span class="sxs-lookup"><span data-stu-id="0fa4f-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **HeaderItem** control type.</span></span> <span data-ttu-id="0fa4f-123">Os requisitos de automação da interface do usuário se aplicam a todos os controles de item de cabeçalho onde a estrutura/plataforma da interface do usuário integra o suporte de automação da interface do usuário para tipos de controle</span><span class="sxs-lookup"><span data-stu-id="0fa4f-123">The UI Automation requirements apply to all header item controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="0fa4f-124">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="0fa4f-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="0fa4f-125">Estrutura de árvore típica</span><span class="sxs-lookup"><span data-stu-id="0fa4f-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="0fa4f-126">Propriedades relevantes</span><span class="sxs-lookup"><span data-stu-id="0fa4f-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="0fa4f-127">Padrões de controle necessários</span><span class="sxs-lookup"><span data-stu-id="0fa4f-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="0fa4f-128">Eventos necessários</span><span class="sxs-lookup"><span data-stu-id="0fa4f-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="0fa4f-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0fa4f-129">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="0fa4f-130">Estrutura de árvore típica</span><span class="sxs-lookup"><span data-stu-id="0fa4f-130">Typical Tree Structure</span></span>

<span data-ttu-id="0fa4f-131">A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence a controles de item de cabeçalho e descreve o que pode ser contido em cada exibição.</span><span class="sxs-lookup"><span data-stu-id="0fa4f-131">The following table depicts a typical control and content view of the UI Automation tree that pertains to header item controls and describes what can be contained in each view.</span></span> <span data-ttu-id="0fa4f-132">Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="0fa4f-132">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0fa4f-133">Exibição de controle</span><span class="sxs-lookup"><span data-stu-id="0fa4f-133">Control View</span></span></th>
<th><span data-ttu-id="0fa4f-134">Exibição de conteúdo</span><span class="sxs-lookup"><span data-stu-id="0fa4f-134">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="0fa4f-135">HeaderItem</span><span class="sxs-lookup"><span data-stu-id="0fa4f-135">HeaderItem</span></span></li>
</ul></td>
<td><span data-ttu-id="0fa4f-136">(Não aplicável)</span><span class="sxs-lookup"><span data-stu-id="0fa4f-136">(Not applicable)</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="0fa4f-137">Propriedades relevantes</span><span class="sxs-lookup"><span data-stu-id="0fa4f-137">Relevant Properties</span></span>

<span data-ttu-id="0fa4f-138">A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para o tipo de controle **HeaderItem** .</span><span class="sxs-lookup"><span data-stu-id="0fa4f-138">The following table lists the UI Automation properties whose value or definition is especially relevant to the **HeaderItem** control type.</span></span> <span data-ttu-id="0fa4f-139">Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="0fa4f-139">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="0fa4f-140">Propriedade de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="0fa4f-140">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="0fa4f-141">Valor</span><span class="sxs-lookup"><span data-stu-id="0fa4f-141">Value</span></span>          | <span data-ttu-id="0fa4f-142">Observações</span><span class="sxs-lookup"><span data-stu-id="0fa4f-142">Notes</span></span>                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0fa4f-143">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="0fa4f-143">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="0fa4f-144">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="0fa4f-144">See notes.</span></span>     | <span data-ttu-id="0fa4f-145">O valor dessa propriedade deve ser exclusivo entre todos os elementos de mesmo nível na exibição bruta da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="0fa4f-145">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                         |
| [<span data-ttu-id="0fa4f-146">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="0fa4f-146">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="0fa4f-147">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="0fa4f-147">See notes.</span></span>     | <span data-ttu-id="0fa4f-148">O retângulo mais externo que contém o controle inteiro.</span><span class="sxs-lookup"><span data-stu-id="0fa4f-148">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                             |
| [<span data-ttu-id="0fa4f-149">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="0fa4f-149">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="0fa4f-150">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="0fa4f-150">See notes.</span></span>     | <span data-ttu-id="0fa4f-151">Com suporte se houver um retângulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="0fa4f-151">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="0fa4f-152">Se nem todos os pontos dentro do retângulo delimitador forem clicáveis, o elemento executará testes de clique especializados, substituirá e fornecerá um ponto clicável.</span><span class="sxs-lookup"><span data-stu-id="0fa4f-152">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span> |
| [<span data-ttu-id="0fa4f-153">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="0fa4f-153">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="0fa4f-154">**HeaderItem**</span><span class="sxs-lookup"><span data-stu-id="0fa4f-154">**HeaderItem**</span></span> | <span data-ttu-id="0fa4f-155">Esse valor é o mesmo para todas as estruturas de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="0fa4f-155">This value is the same for all UI frameworks.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="0fa4f-156">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="0fa4f-156">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="0fa4f-157">FALSE</span><span class="sxs-lookup"><span data-stu-id="0fa4f-157">FALSE</span></span>          | <span data-ttu-id="0fa4f-158">O controle de item de cabeçalho não está incluído na exibição de conteúdo da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="0fa4f-158">The header item control is not included in the content view of the UI Automation tree.</span></span>                                                                                                               |
| [<span data-ttu-id="0fa4f-159">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="0fa4f-159">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="0fa4f-160">TRUE</span><span class="sxs-lookup"><span data-stu-id="0fa4f-160">TRUE</span></span>           | <span data-ttu-id="0fa4f-161">O controle item de cabeçalho é sempre incluído na exibição de controle da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="0fa4f-161">The header item control is always included in the control view of the UI Automation tree.</span></span>                                                                                                            |
| [<span data-ttu-id="0fa4f-162">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="0fa4f-162">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="0fa4f-163">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="0fa4f-163">See notes.</span></span>     | <span data-ttu-id="0fa4f-164">Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="0fa4f-164">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                            |
| [<span data-ttu-id="0fa4f-165">**UIA \_ ItemStatusPropertyId**</span><span class="sxs-lookup"><span data-stu-id="0fa4f-165">**UIA\_ItemStatusPropertyId**</span></span>](uiauto-automation-element-propids.md)                     | <span data-ttu-id="0fa4f-166">Consulte as observações</span><span class="sxs-lookup"><span data-stu-id="0fa4f-166">See notes</span></span>      | <span data-ttu-id="0fa4f-167">Essa propriedade fornece informações para ordens de classificação pelo item de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="0fa4f-167">This property provides information for sort orders by the header item.</span></span>                                                                                                                               |
| [<span data-ttu-id="0fa4f-168">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="0fa4f-168">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="0fa4f-169">NULO</span><span class="sxs-lookup"><span data-stu-id="0fa4f-169">NULL</span></span>           | <span data-ttu-id="0fa4f-170">Os controles de item de cabeçalho não têm um rótulo de texto estático.</span><span class="sxs-lookup"><span data-stu-id="0fa4f-170">Header item controls do not have a static text label.</span></span>                                                                                                                                                |
| [<span data-ttu-id="0fa4f-171">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="0fa4f-171">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="0fa4f-172">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="0fa4f-172">See notes.</span></span>     | <span data-ttu-id="0fa4f-173">Cadeia de caracteres localizada correspondente ao tipo de controle **HeaderItem** .</span><span class="sxs-lookup"><span data-stu-id="0fa4f-173">Localized string corresponding to the **HeaderItem** control type.</span></span> <span data-ttu-id="0fa4f-174">O valor padrão é "item de cabeçalho" para en-US ou inglês (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="0fa4f-174">The default value is "header item" for en-US or English (United States).</span></span>                                                          |
| [<span data-ttu-id="0fa4f-175">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="0fa4f-175">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="0fa4f-176">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="0fa4f-176">See notes.</span></span>     | <span data-ttu-id="0fa4f-177">O controle de item de cabeçalho é sempre autorotulado.</span><span class="sxs-lookup"><span data-stu-id="0fa4f-177">The header item control is always self-labeling.</span></span>                                                                                                                                                     |



 

## <a name="required-control-patterns"></a><span data-ttu-id="0fa4f-178">Padrões de controle necessários</span><span class="sxs-lookup"><span data-stu-id="0fa4f-178">Required Control Patterns</span></span>

<span data-ttu-id="0fa4f-179">A tabela a seguir lista os padrões de controle de automação da interface do usuário que devem ter suporte de todos os controles de item de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="0fa4f-179">The following table lists the UI Automation control patterns required to be supported by all header item controls.</span></span> <span data-ttu-id="0fa4f-180">Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="0fa4f-180">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="0fa4f-181">Padrão de controle</span><span class="sxs-lookup"><span data-stu-id="0fa4f-181">Control Pattern</span></span>                                         | <span data-ttu-id="0fa4f-182">Suporte</span><span class="sxs-lookup"><span data-stu-id="0fa4f-182">Support</span></span> | <span data-ttu-id="0fa4f-183">Observações</span><span class="sxs-lookup"><span data-stu-id="0fa4f-183">Notes</span></span>                                                                                                                             |
|---------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0fa4f-184">**IInvokeProvider**</span><span class="sxs-lookup"><span data-stu-id="0fa4f-184">**IInvokeProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)       | <span data-ttu-id="0fa4f-185">Depende</span><span class="sxs-lookup"><span data-stu-id="0fa4f-185">Depends</span></span> | <span data-ttu-id="0fa4f-186">Implemente o padrão de controle [Invoke](uiauto-implementinginvoke.md) se o controle de item de cabeçalho puder ser clicado para classificar os dados.</span><span class="sxs-lookup"><span data-stu-id="0fa4f-186">Implement the [Invoke](uiauto-implementinginvoke.md) control pattern if the header item control can be clicked to sort the data.</span></span> |
| [<span data-ttu-id="0fa4f-187">**ITransformProvider**</span><span class="sxs-lookup"><span data-stu-id="0fa4f-187">**ITransformProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | <span data-ttu-id="0fa4f-188">Depende</span><span class="sxs-lookup"><span data-stu-id="0fa4f-188">Depends</span></span> | <span data-ttu-id="0fa4f-189">Implemente o padrão de controle [Transform](uiauto-implementingtransform.md) se o controle de item de cabeçalho puder ser redimensionado.</span><span class="sxs-lookup"><span data-stu-id="0fa4f-189">Implement the [Transform](uiauto-implementingtransform.md) control pattern if the header item control can be resized.</span></span>            |



 

## <a name="required-events"></a><span data-ttu-id="0fa4f-190">Eventos necessários</span><span class="sxs-lookup"><span data-stu-id="0fa4f-190">Required Events</span></span>

<span data-ttu-id="0fa4f-191">A tabela a seguir lista os eventos de automação da interface do usuário aos quais os controles de item de cabeçalho são necessários para dar suporte.</span><span class="sxs-lookup"><span data-stu-id="0fa4f-191">The following table lists the UI Automation events that header item controls are required to support.</span></span> <span data-ttu-id="0fa4f-192">Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="0fa4f-192">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="0fa4f-193">Evento de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="0fa4f-193">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="0fa4f-194">Observações</span><span class="sxs-lookup"><span data-stu-id="0fa4f-194">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0fa4f-195">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="0fa4f-195">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="0fa4f-196">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="0fa4f-196">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| [<span data-ttu-id="0fa4f-197">**UIA \_ invocar \_ InvokedEventId**</span><span class="sxs-lookup"><span data-stu-id="0fa4f-197">**UIA\_Invoke\_InvokedEventId**</span></span>](uiauto-event-ids.md)                                                     | <span data-ttu-id="0fa4f-198">Se o controle der suporte ao padrão de controle [Invoke](uiauto-implementinginvoke.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="0fa4f-198">If the control supports the [Invoke](uiauto-implementinginvoke.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="0fa4f-199">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="0fa4f-199">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="0fa4f-200">Se o controle oferecer suporte à propriedade [**IsEnabled**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="0fa4f-200">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="0fa4f-201">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="0fa4f-201">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="0fa4f-202">Se o controle oferecer suporte à propriedade [**IsOffscreen**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="0fa4f-202">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="0fa4f-203">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="0fa4f-203">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="0fa4f-204">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0fa4f-204">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="0fa4f-205">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="0fa4f-205">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0fa4f-206">Visão Geral dos Tipos de Controle de Automação de Interface do Usuário</span><span class="sxs-lookup"><span data-stu-id="0fa4f-206">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="0fa4f-207">Visão geral de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="0fa4f-207">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




