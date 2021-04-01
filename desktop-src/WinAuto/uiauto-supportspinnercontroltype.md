---
title: Tipo de controle Spinner
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle Spinner.
ms.assetid: 28673ad5-645d-4314-96c4-81a951226256
keywords:
- Automação da interface do usuário, suporte para tipo de controle Spinner
- Automação da interface do usuário, tipo de controle Spinner
- Automação da interface do usuário, estrutura de árvore para tipo de controle Spinner
- Automação da interface do usuário, propriedades para tipo de controle Spinner
- Automação da interface do usuário, padrões de controle para tipo de controle Spinner
- Automação da interface do usuário, eventos para tipo de controle Spinner
- estruturas de árvore, tipo de controle Spinner
- Propriedades, tipo de controle Spinner
- padrões de controle, tipo de controle Spinner
- eventos, tipo de controle Spinner
- suporte para tipo de controle Spinner
- tipo de controle Controle giratório
- tipos de controle, estrutura de árvore para tipo de controle Spinner
- tipos de controle, padrões de controle para tipo de controle Spinner
- tipos de controle, suporte para controle giratório
- tipos de controle, controle giratório
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9681160bf82c9a541412bb6dde8958c603fcfe22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636635"
---
# <a name="spinner-control-type"></a><span data-ttu-id="d72d4-119">Tipo de controle Spinner</span><span class="sxs-lookup"><span data-stu-id="d72d4-119">Spinner Control Type</span></span>

<span data-ttu-id="d72d4-120">Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle **Spinner** .</span><span class="sxs-lookup"><span data-stu-id="d72d4-120">This topic provides information about Microsoft UI Automation support for the **Spinner** control type.</span></span>

<span data-ttu-id="d72d4-121">Os controles Spinner são usados para selecionar de um domínio de itens ou um intervalo de números.</span><span class="sxs-lookup"><span data-stu-id="d72d4-121">Spinner controls are used to select from a domain of items or a range of numbers.</span></span>

<span data-ttu-id="d72d4-122">As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle **Spinner** .</span><span class="sxs-lookup"><span data-stu-id="d72d4-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Spinner** control type.</span></span> <span data-ttu-id="d72d4-123">Os requisitos de automação da interface do usuário se aplicam a todos os controles Spinner onde a plataforma/estrutura de interface do usuário integra o suporte de automação da interface do usuário para tipos de controle e padrões</span><span class="sxs-lookup"><span data-stu-id="d72d4-123">The UI Automation requirements apply to all spinner controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="d72d4-124">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="d72d4-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="d72d4-125">Estrutura de árvore típica</span><span class="sxs-lookup"><span data-stu-id="d72d4-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="d72d4-126">Propriedades relevantes</span><span class="sxs-lookup"><span data-stu-id="d72d4-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="d72d4-127">Padrões de controle necessários</span><span class="sxs-lookup"><span data-stu-id="d72d4-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="d72d4-128">Eventos necessários</span><span class="sxs-lookup"><span data-stu-id="d72d4-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="d72d4-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d72d4-129">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="d72d4-130">Estrutura de árvore típica</span><span class="sxs-lookup"><span data-stu-id="d72d4-130">Typical Tree Structure</span></span>

<span data-ttu-id="d72d4-131">A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence aos controles Spinner quando eles dão suporte aos padrões de controle **RangeValue** e **Selection** e descreve o que pode ser contido em cada exibição.</span><span class="sxs-lookup"><span data-stu-id="d72d4-131">The following table depicts a typical control and content view of the UI Automation tree that pertain to spinner controls when they support the **RangeValue** and **Selection** control patterns and describes what can be contained in each view.</span></span> <span data-ttu-id="d72d4-132">Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="d72d4-132">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>

<span data-ttu-id="d72d4-133">**Padrão de controle RangeValue**</span><span class="sxs-lookup"><span data-stu-id="d72d4-133">**RangeValue control pattern**</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d72d4-134">Exibição de controle</span><span class="sxs-lookup"><span data-stu-id="d72d4-134">Control View</span></span></th>
<th><span data-ttu-id="d72d4-135">Exibição de conteúdo</span><span class="sxs-lookup"><span data-stu-id="d72d4-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="d72d4-136">Controle giratório</span><span class="sxs-lookup"><span data-stu-id="d72d4-136">Spinner</span></span>
<ul>
<li><span data-ttu-id="d72d4-137">Editar (0 ou 1)</span><span class="sxs-lookup"><span data-stu-id="d72d4-137">Edit (0 or 1)</span></span></li>
<li><span data-ttu-id="d72d4-138">Botão (2)</span><span class="sxs-lookup"><span data-stu-id="d72d4-138">Button (2)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="d72d4-139">Controle giratório</span><span class="sxs-lookup"><span data-stu-id="d72d4-139">Spinner</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d72d4-140">**padrão de controle Seleção**</span><span class="sxs-lookup"><span data-stu-id="d72d4-140">**Selection control pattern**</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d72d4-141">Exibição de controle</span><span class="sxs-lookup"><span data-stu-id="d72d4-141">Control View</span></span></th>
<th><span data-ttu-id="d72d4-142">Exibição de conteúdo</span><span class="sxs-lookup"><span data-stu-id="d72d4-142">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="d72d4-143">Controle giratório</span><span class="sxs-lookup"><span data-stu-id="d72d4-143">Spinner</span></span>
<ul>
<li><span data-ttu-id="d72d4-144">Editar (0 ou 1)</span><span class="sxs-lookup"><span data-stu-id="d72d4-144">Edit (0 or 1)</span></span></li>
<li><span data-ttu-id="d72d4-145">Botão (2)</span><span class="sxs-lookup"><span data-stu-id="d72d4-145">Button (2)</span></span></li>
<li><span data-ttu-id="d72d4-146">Item de lista (0 ou mais)</span><span class="sxs-lookup"><span data-stu-id="d72d4-146">List Item (0 or more)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="d72d4-147">Controle giratório</span><span class="sxs-lookup"><span data-stu-id="d72d4-147">Spinner</span></span>
<ul>
<li><span data-ttu-id="d72d4-148">ListItem (0 ou mais)</span><span class="sxs-lookup"><span data-stu-id="d72d4-148">ListItem (0 or more)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d72d4-149">Para garantir que os dois botões na subárvore de exibição de controle possam ser diferenciados por ferramentas de teste automatizadas, atribua o valor **ScrollAmount \_ SmallIncrement** ou [**ScrollAmount \_ SmallDecrement**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-scrollamount) à propriedade **AutomationId** , conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="d72d4-149">To ensure that the two buttons in the control view subtree can be distinguished by automated test tools, assign the **ScrollAmount\_SmallIncrement** or [**ScrollAmount\_SmallDecrement**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-scrollamount) value to the **AutomationId** property as appropriate.</span></span> <span data-ttu-id="d72d4-150">Para algumas implementações, o controle de edição associado pode ser um par do controle Spinner.</span><span class="sxs-lookup"><span data-stu-id="d72d4-150">For some implementations, the associated edit control may be a peer of the spinner control.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="d72d4-151">Propriedades relevantes</span><span class="sxs-lookup"><span data-stu-id="d72d4-151">Relevant Properties</span></span>

<span data-ttu-id="d72d4-152">A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para controles Spinner.</span><span class="sxs-lookup"><span data-stu-id="d72d4-152">The following table lists the UI Automation properties whose value or definition is especially relevant to spinner controls.</span></span> <span data-ttu-id="d72d4-153">Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="d72d4-153">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="d72d4-154">Propriedade de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="d72d4-154">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="d72d4-155">Valor</span><span class="sxs-lookup"><span data-stu-id="d72d4-155">Value</span></span>       | <span data-ttu-id="d72d4-156">Observações</span><span class="sxs-lookup"><span data-stu-id="d72d4-156">Notes</span></span>                                                                                                                                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d72d4-157">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="d72d4-157">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="d72d4-158">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="d72d4-158">See notes.</span></span>  | <span data-ttu-id="d72d4-159">O valor dessa propriedade deve ser exclusivo entre todos os elementos de mesmo nível na exibição bruta da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="d72d4-159">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                                                                                                               |
| [<span data-ttu-id="d72d4-160">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="d72d4-160">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="d72d4-161">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="d72d4-161">See notes.</span></span>  | <span data-ttu-id="d72d4-162">O retângulo mais externo que contém o controle inteiro.</span><span class="sxs-lookup"><span data-stu-id="d72d4-162">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="d72d4-163">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="d72d4-163">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="d72d4-164">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="d72d4-164">See notes.</span></span>  | <span data-ttu-id="d72d4-165">O ponto clicável do controle Spinner dá enfoque à parte de edição do controle.</span><span class="sxs-lookup"><span data-stu-id="d72d4-165">The spinner control's clickable point gives focus to the edit portion of the control.</span></span>                                                                                                                                                                                                                                      |
| [<span data-ttu-id="d72d4-166">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="d72d4-166">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="d72d4-167">**Controle giratório**</span><span class="sxs-lookup"><span data-stu-id="d72d4-167">**Spinner**</span></span> | <span data-ttu-id="d72d4-168">Esse valor é o mesmo para todas as estruturas.</span><span class="sxs-lookup"><span data-stu-id="d72d4-168">This value is the same for all frameworks.</span></span>                                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="d72d4-169">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="d72d4-169">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="d72d4-170">TRUE</span><span class="sxs-lookup"><span data-stu-id="d72d4-170">TRUE</span></span>        | <span data-ttu-id="d72d4-171">O controle Spinner sempre deve ser conteúdo.</span><span class="sxs-lookup"><span data-stu-id="d72d4-171">The spinner control must always be content.</span></span>                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="d72d4-172">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="d72d4-172">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="d72d4-173">TRUE</span><span class="sxs-lookup"><span data-stu-id="d72d4-173">TRUE</span></span>        | <span data-ttu-id="d72d4-174">O controle Spinner sempre deve ser um controle.</span><span class="sxs-lookup"><span data-stu-id="d72d4-174">The spinner control must always be a control.</span></span>                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="d72d4-175">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="d72d4-175">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="d72d4-176">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="d72d4-176">See notes.</span></span>  | <span data-ttu-id="d72d4-177">Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="d72d4-177">If the control can receive keyboard focus, it must support this property.</span></span> <span data-ttu-id="d72d4-178">Um controle giratório raramente leva o foco, mas quando ele faz, o foco deve permanecer no controle Spinner em si, não nos botões filho.</span><span class="sxs-lookup"><span data-stu-id="d72d4-178">A spinner control rarely takes the focus, but when it does, the focus should remain on the spinner control itself, not on the child buttons.</span></span> <span data-ttu-id="d72d4-179">O usuário deve ser capaz de executar todas as ações de rolagem usando as teclas seta para cima e seta para baixo.</span><span class="sxs-lookup"><span data-stu-id="d72d4-179">The user should be able to perform all scrolling actions by using the UP ARROW and DOWN ARROW keys.</span></span> |
| [<span data-ttu-id="d72d4-180">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="d72d4-180">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="d72d4-181">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="d72d4-181">See notes.</span></span>  | <span data-ttu-id="d72d4-182">Os controles Spinner têm um rótulo de texto estático.</span><span class="sxs-lookup"><span data-stu-id="d72d4-182">Spinner controls have a static text label.</span></span>                                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="d72d4-183">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="d72d4-183">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="d72d4-184">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="d72d4-184">See notes.</span></span>  | <span data-ttu-id="d72d4-185">Cadeia de caracteres localizada correspondente ao tipo de controle **Spinner** .</span><span class="sxs-lookup"><span data-stu-id="d72d4-185">Localized string corresponding to the **Spinner** control type.</span></span> <span data-ttu-id="d72d4-186">O valor padrão é "Spinner" para en-US ou inglês (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="d72d4-186">The default value is "spinner" for en-US or English (United States).</span></span>                                                                                                                                                                                       |
| [<span data-ttu-id="d72d4-187">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="d72d4-187">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="d72d4-188">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="d72d4-188">See notes.</span></span>  | <span data-ttu-id="d72d4-189">O controle Spinner normalmente obtém seu nome de um rótulo de texto estático.</span><span class="sxs-lookup"><span data-stu-id="d72d4-189">The spinner control typically gets its name from a static text label.</span></span>                                                                                                                                                                                                                                                      |



 

## <a name="required-control-patterns"></a><span data-ttu-id="d72d4-190">Padrões de controle necessários</span><span class="sxs-lookup"><span data-stu-id="d72d4-190">Required Control Patterns</span></span>

<span data-ttu-id="d72d4-191">A tabela a seguir lista os padrões de controle de automação da interface do usuário que devem ter suporte em todos os controles Spinner.</span><span class="sxs-lookup"><span data-stu-id="d72d4-191">The following table lists the UI Automation control patterns required to be supported by all spinner controls.</span></span> <span data-ttu-id="d72d4-192">Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="d72d4-192">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="d72d4-193">Propriedade padrão de controle/padrão</span><span class="sxs-lookup"><span data-stu-id="d72d4-193">Control Pattern/Pattern Property</span></span>                                         | <span data-ttu-id="d72d4-194">Suporte/valor</span><span class="sxs-lookup"><span data-stu-id="d72d4-194">Support/Value</span></span> | <span data-ttu-id="d72d4-195">Observações</span><span class="sxs-lookup"><span data-stu-id="d72d4-195">Notes</span></span>                                                                                                                                     |
|--------------------------------------------------------------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d72d4-196">**IRangeValueProvider**</span><span class="sxs-lookup"><span data-stu-id="d72d4-196">**IRangeValueProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider)                | <span data-ttu-id="d72d4-197">Depende</span><span class="sxs-lookup"><span data-stu-id="d72d4-197">Depends</span></span>       | <span data-ttu-id="d72d4-198">Os controles Spinner que abrangem um intervalo numérico podem dar suporte ao padrão de controle [RangeValue](uiauto-implementingrangevalue.md) .</span><span class="sxs-lookup"><span data-stu-id="d72d4-198">Spinner controls that span a numeric range can support the [RangeValue](uiauto-implementingrangevalue.md) control pattern.</span></span>               |
| [<span data-ttu-id="d72d4-199">**ISelectionProvider**</span><span class="sxs-lookup"><span data-stu-id="d72d4-199">**ISelectionProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)                  | <span data-ttu-id="d72d4-200">Depende</span><span class="sxs-lookup"><span data-stu-id="d72d4-200">Depends</span></span>       | <span data-ttu-id="d72d4-201">Controles Spinner que têm uma lista de itens a serem selecionados devem oferecer suporte ao padrão de controle [Selection](uiauto-implementingselection.md) .</span><span class="sxs-lookup"><span data-stu-id="d72d4-201">Spinner controls that have a list of items to be selected must support the [Selection](uiauto-implementingselection.md) control pattern.</span></span> |
| [<span data-ttu-id="d72d4-202">**CanSelectMultiple**</span><span class="sxs-lookup"><span data-stu-id="d72d4-202">**CanSelectMultiple**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple) | <span data-ttu-id="d72d4-203">FALSE</span><span class="sxs-lookup"><span data-stu-id="d72d4-203">FALSE</span></span>         | <span data-ttu-id="d72d4-204">Os controles Spinner são sempre contêineres de seleção única.</span><span class="sxs-lookup"><span data-stu-id="d72d4-204">Spinner controls are always single selection containers.</span></span>                                                                                  |
| [<span data-ttu-id="d72d4-205">**IValueProvider**</span><span class="sxs-lookup"><span data-stu-id="d72d4-205">**IValueProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)                          | <span data-ttu-id="d72d4-206">Depende</span><span class="sxs-lookup"><span data-stu-id="d72d4-206">Depends</span></span>       | <span data-ttu-id="d72d4-207">Controles Spinner que abrangem um conjunto descrete de opções ou números podem dar suporte ao padrão de controle de [valor](uiauto-implementingvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="d72d4-207">Spinner controls that span a descrete set of options or numbers can support the [Value](uiauto-implementingvalue.md) control pattern.</span></span>    |



 

## <a name="required-events"></a><span data-ttu-id="d72d4-208">Eventos necessários</span><span class="sxs-lookup"><span data-stu-id="d72d4-208">Required Events</span></span>

<span data-ttu-id="d72d4-209">A tabela a seguir lista os eventos de automação da interface do usuário que são necessários para dar suporte a controles Spinner.</span><span class="sxs-lookup"><span data-stu-id="d72d4-209">The following table lists the UI Automation events that spinner controls are required to support.</span></span> <span data-ttu-id="d72d4-210">Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="d72d4-210">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="d72d4-211">Evento de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="d72d4-211">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="d72d4-212">Observações</span><span class="sxs-lookup"><span data-stu-id="d72d4-212">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d72d4-213">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="d72d4-213">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="d72d4-214">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="d72d4-214">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="d72d4-215">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="d72d4-215">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="d72d4-216">Se o controle oferecer suporte à propriedade [**IsEnabled**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="d72d4-216">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="d72d4-217">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="d72d4-217">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="d72d4-218">Se o controle oferecer suporte à propriedade [**IsOffscreen**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="d72d4-218">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| <span data-ttu-id="d72d4-219">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade RangeValueValuePropertyId.</span><span class="sxs-lookup"><span data-stu-id="d72d4-219">[**UIA\_RangeValueValuePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>        | <span data-ttu-id="d72d4-220">Se o controle der suporte ao padrão de controle [RangeValue](uiauto-implementingrangevalue.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="d72d4-220">If the control supports the [RangeValue](uiauto-implementingrangevalue.md) control pattern, it must support this event.</span></span>   |
| <span data-ttu-id="d72d4-221">[**UIA \_ Propriedade \_ InvalidatedEventId de seleção**](uiauto-event-ids.md) – evento alterado.</span><span class="sxs-lookup"><span data-stu-id="d72d4-221">[**UIA\_Selection\_InvalidatedEventId**](uiauto-event-ids.md) property-changed event.</span></span>               | <span data-ttu-id="d72d4-222">Se o controle der suporte ao padrão de controle [Selection](uiauto-implementingselection.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="d72d4-222">If the control supports the [Selection](uiauto-implementingselection.md) control pattern, it must support this event.</span></span>     |
| [<span data-ttu-id="d72d4-223">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="d72d4-223">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |
| <span data-ttu-id="d72d4-224">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ValueValuePropertyId.</span><span class="sxs-lookup"><span data-stu-id="d72d4-224">[**UIA\_ValueValuePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>                  | <span data-ttu-id="d72d4-225">Se o controle der suporte ao padrão de controle de [valor](uiauto-implementingvalue.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="d72d4-225">If the control supports the [Value](uiauto-implementingvalue.md) control pattern, it must support this event.</span></span>             |



 

## <a name="related-topics"></a><span data-ttu-id="d72d4-226">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d72d4-226">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="d72d4-227">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="d72d4-227">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d72d4-228">Visão Geral dos Tipos de Controle de Automação de Interface do Usuário</span><span class="sxs-lookup"><span data-stu-id="d72d4-228">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="d72d4-229">Visão geral de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="d72d4-229">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




