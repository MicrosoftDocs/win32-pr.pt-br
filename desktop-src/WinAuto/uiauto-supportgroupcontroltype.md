---
title: Tipo de controle de grupo
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle grupo.
ms.assetid: f8363c2f-dbff-43a3-831f-d30151829ef9
keywords:
- Automação da interface do usuário, suporte para tipo de controle de grupo
- Automação da interface do usuário, tipo de controle de grupo
- Automação da interface do usuário, estrutura de árvore para tipo de controle de grupo
- Automação da interface do usuário, propriedades para tipo de controle de grupo
- Automação da interface do usuário, padrões de controle para tipo de controle de grupo
- Automação da interface do usuário, eventos para tipo de controle de grupo
- estruturas de árvore, tipo de controle de grupo
- Propriedades, tipo de controle de grupo
- padrões de controle, tipo de controle de grupo
- eventos, tipo de controle de grupo
- suporte para tipo de controle de grupo
- tipo de controle Grupo
- tipos de controle, estrutura de árvore para tipo de controle de grupo
- tipos de controle, padrões de controle para tipo de controle de grupo
- tipos de controle, suporte para grupo
- tipos de controle, grupo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44b630d0ef736d937e4f024c8131adc4c843b6e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363937"
---
# <a name="group-control-type"></a><span data-ttu-id="e95d2-119">Tipo de controle de grupo</span><span class="sxs-lookup"><span data-stu-id="e95d2-119">Group Control Type</span></span>

<span data-ttu-id="e95d2-120">Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle **grupo** .</span><span class="sxs-lookup"><span data-stu-id="e95d2-120">This topic provides information about Microsoft UI Automation support for the **Group** control type.</span></span>

<span data-ttu-id="e95d2-121">Um controle de grupo representa um nó dentro de uma hierarquia.</span><span class="sxs-lookup"><span data-stu-id="e95d2-121">A group control represents a node within a hierarchy.</span></span> <span data-ttu-id="e95d2-122">O tipo de controle **grupo** cria uma separação na árvore de automação da interface do usuário para que os itens agrupados tenham uma divisão lógica dentro da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="e95d2-122">The **Group** control type creates a separation in the UI Automation tree so items that are grouped together have a logical division within the UI Automation tree.</span></span>

<span data-ttu-id="e95d2-123">As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle **grupo** .</span><span class="sxs-lookup"><span data-stu-id="e95d2-123">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Group** control type.</span></span> <span data-ttu-id="e95d2-124">Os requisitos de automação da interface do usuário se aplicam a todos os controles de grupo nos quais a plataforma/estrutura da interface do usuário integra o suporte à automação da interface do usuário para tipos de controle</span><span class="sxs-lookup"><span data-stu-id="e95d2-124">The UI Automation requirements apply to all group controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="e95d2-125">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="e95d2-125">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="e95d2-126">Estrutura de árvore típica</span><span class="sxs-lookup"><span data-stu-id="e95d2-126">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="e95d2-127">Propriedades relevantes</span><span class="sxs-lookup"><span data-stu-id="e95d2-127">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="e95d2-128">Padrões de controle necessários</span><span class="sxs-lookup"><span data-stu-id="e95d2-128">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="e95d2-129">Eventos necessários</span><span class="sxs-lookup"><span data-stu-id="e95d2-129">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="e95d2-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e95d2-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="e95d2-131">Estrutura de árvore típica</span><span class="sxs-lookup"><span data-stu-id="e95d2-131">Typical Tree Structure</span></span>

<span data-ttu-id="e95d2-132">A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence a controles de grupo e descreve o que pode ser contido em cada exibição.</span><span class="sxs-lookup"><span data-stu-id="e95d2-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to group controls and describes what can be contained in each view.</span></span> <span data-ttu-id="e95d2-133">Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="e95d2-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e95d2-134">Exibição de controle</span><span class="sxs-lookup"><span data-stu-id="e95d2-134">Control View</span></span></th>
<th><span data-ttu-id="e95d2-135">Exibição de conteúdo</span><span class="sxs-lookup"><span data-stu-id="e95d2-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="e95d2-136">Agrupar</span><span class="sxs-lookup"><span data-stu-id="e95d2-136">Group</span></span>
<ul>
<li><span data-ttu-id="e95d2-137">0 ou muitos controles</span><span class="sxs-lookup"><span data-stu-id="e95d2-137">0 or many controls</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="e95d2-138">Agrupar</span><span class="sxs-lookup"><span data-stu-id="e95d2-138">Group</span></span>
<ul>
<li><span data-ttu-id="e95d2-139">0 ou muitos controles</span><span class="sxs-lookup"><span data-stu-id="e95d2-139">0 or many controls</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="e95d2-140">Os controles de grupo normalmente incluem o suporte de automação da interface do usuário para tipos de controle encontrados abaixo deles na subárvore, incluindo os tipos de controle [ListItem](uiauto-supportlistitemcontroltype.md), [TreeItem](uiauto-supporttreeitemcontroltype.md)e [DataItem](uiauto-supportdataitemcontroltype.md) .</span><span class="sxs-lookup"><span data-stu-id="e95d2-140">Group controls typically include UI Automation support for control types found below them in the subtree, including the [ListItem](uiauto-supportlistitemcontroltype.md), [TreeItem](uiauto-supporttreeitemcontroltype.md), and [DataItem](uiauto-supportdataitemcontroltype.md) control types.</span></span> <span data-ttu-id="e95d2-141">Como um controle de grupo é um contêiner genérico, é possível que qualquer tipo de controle esteja sob o controle de grupo na árvore.</span><span class="sxs-lookup"><span data-stu-id="e95d2-141">Because a group control is a generic container, it is possible for any type of control to be under the group control in the tree.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="e95d2-142">Propriedades relevantes</span><span class="sxs-lookup"><span data-stu-id="e95d2-142">Relevant Properties</span></span>

<span data-ttu-id="e95d2-143">A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para os controles de grupo.</span><span class="sxs-lookup"><span data-stu-id="e95d2-143">The following table lists the UI Automation properties whose value or definition is especially relevant to the group controls.</span></span> <span data-ttu-id="e95d2-144">Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="e95d2-144">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="e95d2-145">Propriedade de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="e95d2-145">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="e95d2-146">Valor</span><span class="sxs-lookup"><span data-stu-id="e95d2-146">Value</span></span>      | <span data-ttu-id="e95d2-147">Observações</span><span class="sxs-lookup"><span data-stu-id="e95d2-147">Notes</span></span>                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e95d2-148">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="e95d2-148">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="e95d2-149">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="e95d2-149">See notes.</span></span> | <span data-ttu-id="e95d2-150">O valor dessa propriedade deve ser exclusivo entre todos os elementos de mesmo nível na exibição bruta da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="e95d2-150">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                         |
| [<span data-ttu-id="e95d2-151">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="e95d2-151">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="e95d2-152">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="e95d2-152">See notes.</span></span> | <span data-ttu-id="e95d2-153">O retângulo mais externo que contém o controle inteiro.</span><span class="sxs-lookup"><span data-stu-id="e95d2-153">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                             |
| [<span data-ttu-id="e95d2-154">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="e95d2-154">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="e95d2-155">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="e95d2-155">See notes.</span></span> | <span data-ttu-id="e95d2-156">Com suporte se houver um retângulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="e95d2-156">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="e95d2-157">Se nem todos os pontos dentro do retângulo delimitador forem clicáveis, o elemento executará testes de clique especializados, substituirá e fornecerá um ponto clicável.</span><span class="sxs-lookup"><span data-stu-id="e95d2-157">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span> |
| [<span data-ttu-id="e95d2-158">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="e95d2-158">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="e95d2-159">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="e95d2-159">**Group**</span></span>  |                                                                                                                                                                                                      |
| [<span data-ttu-id="e95d2-160">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="e95d2-160">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="e95d2-161">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="e95d2-161">**TRUE**</span></span>   | <span data-ttu-id="e95d2-162">O controle de grupo é sempre incluído na exibição de conteúdo da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="e95d2-162">The group control is always included in the content view of the UI Automation tree.</span></span>                                                                                                                  |
| [<span data-ttu-id="e95d2-163">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="e95d2-163">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="e95d2-164">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="e95d2-164">**TRUE**</span></span>   | <span data-ttu-id="e95d2-165">O controle de grupo é sempre incluído no modo de exibição de controle da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="e95d2-165">The group control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                  |
| [<span data-ttu-id="e95d2-166">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="e95d2-166">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="e95d2-167">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="e95d2-167">See notes.</span></span> | <span data-ttu-id="e95d2-168">Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="e95d2-168">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                            |
| [<span data-ttu-id="e95d2-169">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="e95d2-169">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="e95d2-170">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="e95d2-170">See notes.</span></span> | <span data-ttu-id="e95d2-171">Os controles de grupo normalmente são autorotulados.</span><span class="sxs-lookup"><span data-stu-id="e95d2-171">Group controls are typically self-labeling.</span></span> <span data-ttu-id="e95d2-172">Nesses casos, retorna **NULL**.</span><span class="sxs-lookup"><span data-stu-id="e95d2-172">In these cases, return **NULL**.</span></span> <span data-ttu-id="e95d2-173">Se o grupo tiver um rótulo de texto estático, retorne o rótulo como o valor da propriedade **LabeledBy** .</span><span class="sxs-lookup"><span data-stu-id="e95d2-173">If the group has a static text label, return the label as the value of the **LabeledBy** property.</span></span>                      |
| [<span data-ttu-id="e95d2-174">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="e95d2-174">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="e95d2-175">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="e95d2-175">See notes.</span></span> | <span data-ttu-id="e95d2-176">Cadeia de caracteres localizada correspondente ao tipo de controle de **grupo** .</span><span class="sxs-lookup"><span data-stu-id="e95d2-176">Localized string corresponding to the **Group** control type.</span></span> <span data-ttu-id="e95d2-177">O valor padrão é "Group" para en-US ou inglês (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="e95d2-177">The default value is "group" for en-US or English (United States).</span></span>                                                                     |
| [<span data-ttu-id="e95d2-178">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="e95d2-178">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="e95d2-179">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="e95d2-179">See notes.</span></span> | <span data-ttu-id="e95d2-180">O controle de grupo normalmente obtém seu nome do texto que rotula o controle.</span><span class="sxs-lookup"><span data-stu-id="e95d2-180">The group control typically gets its name from the text that labels the control.</span></span>                                                                                                                     |



 

## <a name="required-control-patterns"></a><span data-ttu-id="e95d2-181">Padrões de controle necessários</span><span class="sxs-lookup"><span data-stu-id="e95d2-181">Required Control Patterns</span></span>

<span data-ttu-id="e95d2-182">A tabela a seguir lista os padrões de controle de automação da interface do usuário que devem ter suporte para o tipo de controle **grupo** .</span><span class="sxs-lookup"><span data-stu-id="e95d2-182">The following table lists the UI Automation control patterns required to be supported for the **Group** control type.</span></span> <span data-ttu-id="e95d2-183">Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="e95d2-183">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="e95d2-184">Padrão de controle</span><span class="sxs-lookup"><span data-stu-id="e95d2-184">Control Pattern</span></span>                                                   | <span data-ttu-id="e95d2-185">Suporte</span><span class="sxs-lookup"><span data-stu-id="e95d2-185">Support</span></span> | <span data-ttu-id="e95d2-186">Observações</span><span class="sxs-lookup"><span data-stu-id="e95d2-186">Notes</span></span>                                                                                                                                                 |
|-------------------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e95d2-187">**IExpandCollapseProvider**</span><span class="sxs-lookup"><span data-stu-id="e95d2-187">**IExpandCollapseProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | <span data-ttu-id="e95d2-188">Depende</span><span class="sxs-lookup"><span data-stu-id="e95d2-188">Depends</span></span> | <span data-ttu-id="e95d2-189">Os controles de grupo que podem ser usados para mostrar ou ocultar informações devem oferecer suporte ao padrão de controle [ExpandCollapse](uiauto-implementingexpandcollapse.md) .</span><span class="sxs-lookup"><span data-stu-id="e95d2-189">Group controls that can be used to show or hide information must support the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="e95d2-190">Eventos necessários</span><span class="sxs-lookup"><span data-stu-id="e95d2-190">Required Events</span></span>

<span data-ttu-id="e95d2-191">A tabela a seguir lista os eventos de automação da interface do usuário aos quais os controles de grupo precisam dar suporte.</span><span class="sxs-lookup"><span data-stu-id="e95d2-191">The following table lists the UI Automation events that group controls are required to support.</span></span> <span data-ttu-id="e95d2-192">Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="e95d2-192">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="e95d2-193">Evento de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="e95d2-193">UI Automation Event</span></span>                                                                                                                                                | <span data-ttu-id="e95d2-194">Observações</span><span class="sxs-lookup"><span data-stu-id="e95d2-194">Notes</span></span>                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e95d2-195">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="e95d2-195">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                                   |                                                                                                                                                  |
| <span data-ttu-id="e95d2-196">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="e95d2-196">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                              |                                                                                                                                                  |
| <span data-ttu-id="e95d2-197">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ExpandCollapseExpandCollapseStatePropertyId.</span><span class="sxs-lookup"><span data-stu-id="e95d2-197">[**UIA\_ExpandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="e95d2-198">Se o controle oferecer suporte ao padrão de controle de padrão de controle [ExpandCollapse](uiauto-implementingexpandcollapse.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="e95d2-198">If the control supports the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern control pattern, it must support this event.</span></span> |
| <span data-ttu-id="e95d2-199">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="e95d2-199">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                              | <span data-ttu-id="e95d2-200">Se o controle oferecer suporte à propriedade [**IsEnabled**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="e95d2-200">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>                         |
| <span data-ttu-id="e95d2-201">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="e95d2-201">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                          | <span data-ttu-id="e95d2-202">Se o controle oferecer suporte à propriedade [**IsOffscreen**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="e95d2-202">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>                       |
| <span data-ttu-id="e95d2-203">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ToggleToggleStatePropertyId.</span><span class="sxs-lookup"><span data-stu-id="e95d2-203">[**UIA\_ToggleToggleStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>                                 | <span data-ttu-id="e95d2-204">Se o controle der suporte ao padrão de controle [Toggle](uiauto-implementingtoggle.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="e95d2-204">If the control supports the [Toggle](uiauto-implementingtoggle.md) control pattern, it must support this event.</span></span>                                 |
| [<span data-ttu-id="e95d2-205">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="e95d2-205">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                               |                                                                                                                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="e95d2-206">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e95d2-206">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="e95d2-207">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="e95d2-207">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e95d2-208">Visão Geral dos Tipos de Controle de Automação de Interface do Usuário</span><span class="sxs-lookup"><span data-stu-id="e95d2-208">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="e95d2-209">Visão geral de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="e95d2-209">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




