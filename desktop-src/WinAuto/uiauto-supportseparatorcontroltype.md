---
title: Tipo de controle Separator
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle Separator.
ms.assetid: 4987b05a-101e-48b1-aed2-bd7206146f70
keywords:
- Automação da interface do usuário, suporte para tipo de controle Separator
- Automação da interface do usuário, tipo de controle Separator
- Automação da interface do usuário, estrutura de árvore para tipo de controle Separator
- Automação da interface do usuário, propriedades para tipo de controle Separator
- Automação da interface do usuário, padrões de controle para tipo de controle Separator
- Automação da interface do usuário, eventos para tipo de controle Separator
- estruturas de árvore, tipo de controle Separator
- Propriedades, tipo de controle Separator
- padrões de controle, tipo de controle Separator
- eventos, tipo de controle Separator
- suporte para tipo de controle Separator
- tipo de controle Separador
- tipos de controle, estrutura de árvore para tipo de controle Separator
- tipos de controle, padrões de controle para o tipo de controle Separator
- tipos de controle, suporte para separador
- tipos de controle, separador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92cdf6c15dbe461e78877c6b93f0ff4b52f67fc8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498758"
---
# <a name="separator-control-type"></a><span data-ttu-id="9a666-119">Tipo de controle Separator</span><span class="sxs-lookup"><span data-stu-id="9a666-119">Separator Control Type</span></span>

<span data-ttu-id="9a666-120">Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle **Separator** .</span><span class="sxs-lookup"><span data-stu-id="9a666-120">This topic provides information about Microsoft UI Automation support for the **Separator** control type.</span></span>

<span data-ttu-id="9a666-121">Os controles separadores são usados para dividir visualmente um espaço em duas regiões.</span><span class="sxs-lookup"><span data-stu-id="9a666-121">Separator controls are used to visually divide a space into two regions.</span></span> <span data-ttu-id="9a666-122">Por exemplo, um controle Separator pode ser uma barra que define dois painéis em uma janela.</span><span class="sxs-lookup"><span data-stu-id="9a666-122">For example, a separator control can be a bar that defines two panes in a window.</span></span> <span data-ttu-id="9a666-123">Se o separador puder ser movido, o controle deverá ser exposto como Thumb no tipo de controle.</span><span class="sxs-lookup"><span data-stu-id="9a666-123">If the separator can be moved, the control should be exposed as Thumb in control type.</span></span>

<span data-ttu-id="9a666-124">As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle **Separator** .</span><span class="sxs-lookup"><span data-stu-id="9a666-124">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Separator** control type.</span></span> <span data-ttu-id="9a666-125">Os requisitos de automação da interface do usuário se aplicam a todos os controles de separador onde a estrutura/plataforma da interface do usuário integra o suporte à automação da interface do usuário para tipos de</span><span class="sxs-lookup"><span data-stu-id="9a666-125">The UI Automation requirements apply to all separator controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="9a666-126">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="9a666-126">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="9a666-127">Estrutura de árvore típica</span><span class="sxs-lookup"><span data-stu-id="9a666-127">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="9a666-128">Propriedades relevantes</span><span class="sxs-lookup"><span data-stu-id="9a666-128">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="9a666-129">Padrões de controle necessários</span><span class="sxs-lookup"><span data-stu-id="9a666-129">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="9a666-130">Eventos necessários</span><span class="sxs-lookup"><span data-stu-id="9a666-130">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="9a666-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9a666-131">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="9a666-132">Estrutura de árvore típica</span><span class="sxs-lookup"><span data-stu-id="9a666-132">Typical Tree Structure</span></span>

<span data-ttu-id="9a666-133">A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence a controles separadores e descreve o que pode ser contido em cada exibição.</span><span class="sxs-lookup"><span data-stu-id="9a666-133">The following table depicts a typical control and content view of the UI Automation tree that pertains to separator controls and describes what can be contained in each view.</span></span> <span data-ttu-id="9a666-134">Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="9a666-134">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9a666-135">Exibição de controle</span><span class="sxs-lookup"><span data-stu-id="9a666-135">Control View</span></span></th>
<th><span data-ttu-id="9a666-136">Exibição de conteúdo</span><span class="sxs-lookup"><span data-stu-id="9a666-136">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="9a666-137">Separador</span><span class="sxs-lookup"><span data-stu-id="9a666-137">Separator</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="9a666-138">O tipo de controle <strong>Separator</strong> nunca tem conteúdo.</span><span class="sxs-lookup"><span data-stu-id="9a666-138">The <strong>Separator</strong> control type never has content.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="9a666-139">Propriedades relevantes</span><span class="sxs-lookup"><span data-stu-id="9a666-139">Relevant Properties</span></span>

<span data-ttu-id="9a666-140">A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para controles de separadores.</span><span class="sxs-lookup"><span data-stu-id="9a666-140">The following table lists the UI Automation properties whose value or definition is especially relevant to separator controls.</span></span> <span data-ttu-id="9a666-141">Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="9a666-141">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="9a666-142">Propriedade de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="9a666-142">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="9a666-143">Valor</span><span class="sxs-lookup"><span data-stu-id="9a666-143">Value</span></span>         | <span data-ttu-id="9a666-144">Observações</span><span class="sxs-lookup"><span data-stu-id="9a666-144">Notes</span></span>                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9a666-145">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="9a666-145">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="9a666-146">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="9a666-146">See notes.</span></span>    | <span data-ttu-id="9a666-147">O valor dessa propriedade deve ser exclusivo entre todos os elementos de mesmo nível na exibição bruta da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="9a666-147">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                         |
| [<span data-ttu-id="9a666-148">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="9a666-148">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="9a666-149">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="9a666-149">See notes.</span></span>    | <span data-ttu-id="9a666-150">O retângulo mais externo que contém o controle inteiro.</span><span class="sxs-lookup"><span data-stu-id="9a666-150">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                             |
| [<span data-ttu-id="9a666-151">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="9a666-151">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="9a666-152">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="9a666-152">See notes.</span></span>    | <span data-ttu-id="9a666-153">Com suporte se houver um retângulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="9a666-153">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="9a666-154">Se nem todos os pontos dentro do retângulo delimitador forem clicáveis, o elemento executará testes de clique especializados, substituirá e fornecerá um ponto clicável.</span><span class="sxs-lookup"><span data-stu-id="9a666-154">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span> |
| [<span data-ttu-id="9a666-155">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="9a666-155">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="9a666-156">**Separador**</span><span class="sxs-lookup"><span data-stu-id="9a666-156">**Separator**</span></span> |                                                                                                                                                                                                      |
| [<span data-ttu-id="9a666-157">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="9a666-157">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="9a666-158">FALSE</span><span class="sxs-lookup"><span data-stu-id="9a666-158">FALSE</span></span>         | <span data-ttu-id="9a666-159">O controle Separator nunca tem conteúdo.</span><span class="sxs-lookup"><span data-stu-id="9a666-159">The separator control is never content.</span></span>                                                                                                                                                              |
| [<span data-ttu-id="9a666-160">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="9a666-160">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="9a666-161">TRUE</span><span class="sxs-lookup"><span data-stu-id="9a666-161">TRUE</span></span>          | <span data-ttu-id="9a666-162">O controle Separator sempre deve ser um controle.</span><span class="sxs-lookup"><span data-stu-id="9a666-162">The separator control must always be a control.</span></span>                                                                                                                                                      |
| [<span data-ttu-id="9a666-163">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="9a666-163">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="9a666-164">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="9a666-164">See notes.</span></span>    | <span data-ttu-id="9a666-165">Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="9a666-165">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                            |
| [<span data-ttu-id="9a666-166">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="9a666-166">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="9a666-167">NULO</span><span class="sxs-lookup"><span data-stu-id="9a666-167">NULL</span></span>          | <span data-ttu-id="9a666-168">O controle Separator não tem um rótulo estático.</span><span class="sxs-lookup"><span data-stu-id="9a666-168">The separator control does not have a static label.</span></span>                                                                                                                                                  |
| [<span data-ttu-id="9a666-169">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="9a666-169">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="9a666-170">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="9a666-170">See notes.</span></span>    | <span data-ttu-id="9a666-171">Cadeia de caracteres localizada correspondente ao tipo de controle **Separator** .</span><span class="sxs-lookup"><span data-stu-id="9a666-171">Localized string corresponding to the **Separator** control type.</span></span> <span data-ttu-id="9a666-172">O valor padrão é "separador" para en-US ou inglês (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="9a666-172">The default value is "Separator" for en-US or English (United States).</span></span>                                                             |
| [<span data-ttu-id="9a666-173">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="9a666-173">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="9a666-174">""</span><span class="sxs-lookup"><span data-stu-id="9a666-174">""</span></span>            | <span data-ttu-id="9a666-175">O controle Separator não requer uma propriedade **Name** .</span><span class="sxs-lookup"><span data-stu-id="9a666-175">The separator control does not require a **Name** property.</span></span>                                                                                                                                          |



 

## <a name="required-control-patterns"></a><span data-ttu-id="9a666-176">Padrões de controle necessários</span><span class="sxs-lookup"><span data-stu-id="9a666-176">Required Control Patterns</span></span>

<span data-ttu-id="9a666-177">O controle Separator não é necessário para dar suporte a nenhum padrão de controle.</span><span class="sxs-lookup"><span data-stu-id="9a666-177">The separator control is not required to support any control patterns.</span></span> <span data-ttu-id="9a666-178">Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="9a666-178">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>

## <a name="required-events"></a><span data-ttu-id="9a666-179">Eventos necessários</span><span class="sxs-lookup"><span data-stu-id="9a666-179">Required Events</span></span>

<span data-ttu-id="9a666-180">A tabela a seguir lista os eventos de automação da interface do usuário aos quais os controles separadores são necessários para dar suporte.</span><span class="sxs-lookup"><span data-stu-id="9a666-180">The following table lists the UI Automation events that separator controls are required to support.</span></span> <span data-ttu-id="9a666-181">Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="9a666-181">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="9a666-182">Evento de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="9a666-182">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="9a666-183">Observações</span><span class="sxs-lookup"><span data-stu-id="9a666-183">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9a666-184">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="9a666-184">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="9a666-185">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="9a666-185">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="9a666-186">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="9a666-186">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="9a666-187">Se o controle oferecer suporte à propriedade [**IsEnabled**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="9a666-187">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="9a666-188">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="9a666-188">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="9a666-189">Se o controle oferecer suporte à propriedade [**IsOffscreen**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="9a666-189">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="9a666-190">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="9a666-190">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="9a666-191">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9a666-191">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="9a666-192">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="9a666-192">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9a666-193">Visão Geral dos Tipos de Controle de Automação de Interface do Usuário</span><span class="sxs-lookup"><span data-stu-id="9a666-193">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="9a666-194">Visão geral de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="9a666-194">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




