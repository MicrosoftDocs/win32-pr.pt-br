---
title: Tipo de controle Thumb
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle Thumb.
ms.assetid: 3b1d6802-cfd4-4b07-80a0-2950ca7f4e96
keywords:
- Automação da interface do usuário, suporte para tipo de controle Thumb
- Automação da interface do usuário, tipo de controle Thumb
- Automação da interface do usuário, estrutura de árvore para o tipo de controle Thumb
- Automação da interface do usuário, propriedades para tipo de controle Thumb
- Automação da interface do usuário, padrões de controle para o tipo de controle Thumb
- Automação da interface do usuário, eventos para tipo de controle Thumb
- estruturas de árvore, tipo de controle Thumb
- Propriedades, tipo de controle Thumb
- padrões de controle, tipo de controle Thumb
- eventos, tipo de controle Thumb
- suporte para o tipo de controle Thumb
- tipo de controle Posição
- tipos de controle, estrutura de árvore para o tipo de controle Thumb
- tipos de controle, padrões de controle para o tipo de controle Thumb
- tipos de controle, suporte para Thumb
- tipos de controle, Thumb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8faf60fab30f54d3ed3e4b5a9f49628a3a35be5b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364380"
---
# <a name="thumb-control-type"></a><span data-ttu-id="fc77d-119">Tipo de controle Thumb</span><span class="sxs-lookup"><span data-stu-id="fc77d-119">Thumb Control Type</span></span>

<span data-ttu-id="fc77d-120">Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle **Thumb** .</span><span class="sxs-lookup"><span data-stu-id="fc77d-120">This topic provides information about Microsoft UI Automation support for the **Thumb** control type.</span></span>

<span data-ttu-id="fc77d-121">Os controles Thumb fornecem a funcionalidade que permite que um controle seja movido (ou arrastado), como um botão de barra de rolagem ou redimensionado, como um widget de redimensionamento de janela.</span><span class="sxs-lookup"><span data-stu-id="fc77d-121">Thumb controls provide the functionality that enables a control to be moved (or dragged), such as a scroll bar button, or resized, such as a window resizing widget.</span></span> <span data-ttu-id="fc77d-122">Observe que um controle Thumb não fornece funcionalidade de arrastar e soltar.</span><span class="sxs-lookup"><span data-stu-id="fc77d-122">Note that a thumb control does not provide drag-and-drop functionality.</span></span> <span data-ttu-id="fc77d-123">Os controles Thumb podem receber o foco do mouse, mas não o foco do teclado.</span><span class="sxs-lookup"><span data-stu-id="fc77d-123">Thumb controls can receive mouse focus but not keyboard focus.</span></span> <span data-ttu-id="fc77d-124">O desenvolvedor de controle deve implementar o controle para que ele atue adequadamente (pode ser arrastado ou redimensionado).</span><span class="sxs-lookup"><span data-stu-id="fc77d-124">The control developer must implement the control so that it acts appropriately (can be dragged or resized).</span></span>

<span data-ttu-id="fc77d-125">As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle **Thumb** .</span><span class="sxs-lookup"><span data-stu-id="fc77d-125">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Thumb** control type.</span></span> <span data-ttu-id="fc77d-126">Os requisitos de automação da interface do usuário aplicam todos os controles Thumb nos quais a plataforma/estrutura da interface do usuário integra o suporte à automação da interface do usuário para tipos de controle e</span><span class="sxs-lookup"><span data-stu-id="fc77d-126">The UI Automation requirements apply all thumb controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="fc77d-127">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="fc77d-127">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="fc77d-128">Estrutura de árvore típica</span><span class="sxs-lookup"><span data-stu-id="fc77d-128">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="fc77d-129">Propriedades relevantes</span><span class="sxs-lookup"><span data-stu-id="fc77d-129">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="fc77d-130">Padrões de controle necessários</span><span class="sxs-lookup"><span data-stu-id="fc77d-130">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="fc77d-131">Eventos necessários</span><span class="sxs-lookup"><span data-stu-id="fc77d-131">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="fc77d-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fc77d-132">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="fc77d-133">Estrutura de árvore típica</span><span class="sxs-lookup"><span data-stu-id="fc77d-133">Typical Tree Structure</span></span>

<span data-ttu-id="fc77d-134">A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence a controles Thumb e descreve o que pode ser contido em cada exibição.</span><span class="sxs-lookup"><span data-stu-id="fc77d-134">The following table depicts a typical control and content view of the UI Automation tree that pertains to thumb controls and describes what can be contained in each view.</span></span> <span data-ttu-id="fc77d-135">Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="fc77d-135">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fc77d-136">Exibição de controle</span><span class="sxs-lookup"><span data-stu-id="fc77d-136">Control View</span></span></th>
<th><span data-ttu-id="fc77d-137">Exibição de conteúdo</span><span class="sxs-lookup"><span data-stu-id="fc77d-137">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="fc77d-138">Posição</span><span class="sxs-lookup"><span data-stu-id="fc77d-138">Thumb</span></span></li>
</ul></td>
<td><span data-ttu-id="fc77d-139">(Não aplicável)</span><span class="sxs-lookup"><span data-stu-id="fc77d-139">(Not applicable)</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="fc77d-140">Os controles Thumb nunca aparecem no modo de exibição de conteúdo porque existem apenas para serem manipulados com um mouse.</span><span class="sxs-lookup"><span data-stu-id="fc77d-140">Thumb controls never appear in the content view because they exist only to be manipulated with a mouse.</span></span> <span data-ttu-id="fc77d-141">Eles são expostos embora outro padrão de controle, como o padrão de controle [Scroll](uiauto-implementingscroll.md) , o padrão de controle [Transform](uiauto-implementingtransform.md) ou o padrão de controle [RangeValue](uiauto-implementingrangevalue.md) , tenha suporte no contêiner do controle Thumb.</span><span class="sxs-lookup"><span data-stu-id="fc77d-141">They are exposed though another control pattern, such as the [Scroll](uiauto-implementingscroll.md) control pattern, [Transform](uiauto-implementingtransform.md) control pattern, or [RangeValue](uiauto-implementingrangevalue.md) control pattern, being supported on the thumb control's container.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="fc77d-142">Propriedades relevantes</span><span class="sxs-lookup"><span data-stu-id="fc77d-142">Relevant Properties</span></span>

<span data-ttu-id="fc77d-143">A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para os controles de Thumb.</span><span class="sxs-lookup"><span data-stu-id="fc77d-143">The following table lists the UI Automation properties whose value or definition is especially relevant to thumb controls.</span></span> <span data-ttu-id="fc77d-144">Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="fc77d-144">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="fc77d-145">Propriedade de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="fc77d-145">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="fc77d-146">Valor</span><span class="sxs-lookup"><span data-stu-id="fc77d-146">Value</span></span>      | <span data-ttu-id="fc77d-147">Observações</span><span class="sxs-lookup"><span data-stu-id="fc77d-147">Notes</span></span>                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fc77d-148">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="fc77d-148">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="fc77d-149">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="fc77d-149">See notes.</span></span> | <span data-ttu-id="fc77d-150">O valor dessa propriedade deve ser exclusivo entre todos os elementos de mesmo nível na exibição bruta da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fc77d-150">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="fc77d-151">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="fc77d-151">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="fc77d-152">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="fc77d-152">See notes.</span></span> | <span data-ttu-id="fc77d-153">O retângulo mais externo que contém o controle inteiro.</span><span class="sxs-lookup"><span data-stu-id="fc77d-153">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                                                     |
| [<span data-ttu-id="fc77d-154">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="fc77d-154">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="fc77d-155">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="fc77d-155">See notes.</span></span> | <span data-ttu-id="fc77d-156">Um ponto dentro da área visível do cliente do controle Thumb.</span><span class="sxs-lookup"><span data-stu-id="fc77d-156">A point within the visible client area of the thumb control.</span></span>                                                                                                                                                                                                 |
| [<span data-ttu-id="fc77d-157">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="fc77d-157">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="fc77d-158">**Comum**</span><span class="sxs-lookup"><span data-stu-id="fc77d-158">**Thumb**</span></span>  |                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="fc77d-159">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="fc77d-159">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="fc77d-160">FALSE</span><span class="sxs-lookup"><span data-stu-id="fc77d-160">FALSE</span></span>      | <span data-ttu-id="fc77d-161">O controle Thumb nunca é incluído na exibição de conteúdo da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fc77d-161">The thumb control is never included in the content view of the UI Automation tree.</span></span>                                                                                                                                                                           |
| [<span data-ttu-id="fc77d-162">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="fc77d-162">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="fc77d-163">TRUE</span><span class="sxs-lookup"><span data-stu-id="fc77d-163">TRUE</span></span>       | <span data-ttu-id="fc77d-164">O controle Thumb sempre é incluído na exibição de controle da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fc77d-164">The thumb control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                                                                          |
| [<span data-ttu-id="fc77d-165">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="fc77d-165">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="fc77d-166">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="fc77d-166">See notes.</span></span> | <span data-ttu-id="fc77d-167">Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="fc77d-167">If the control can receive keyboard focus, it must support this property.</span></span> <span data-ttu-id="fc77d-168">Um controle Thumb pode receber o foco se for usado como um objeto "garra" para dimensionar uma janela ou um painel.</span><span class="sxs-lookup"><span data-stu-id="fc77d-168">A thumb control can receive the focus if it is used as a "gripper" object for sizing a window or a pane.</span></span> <span data-ttu-id="fc77d-169">Um controle Thumb em um controle deslizante ou barra de rolagem nunca deve receber o foco.</span><span class="sxs-lookup"><span data-stu-id="fc77d-169">A thumb control in a slider or scroll bar should never receive the focus.</span></span> |
| [<span data-ttu-id="fc77d-170">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="fc77d-170">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="fc77d-171">NULO</span><span class="sxs-lookup"><span data-stu-id="fc77d-171">NULL</span></span>       | <span data-ttu-id="fc77d-172">Controles Thumb nunca têm um rótulo.</span><span class="sxs-lookup"><span data-stu-id="fc77d-172">Thumb controls never have a label.</span></span>                                                                                                                                                                                                                           |
| [<span data-ttu-id="fc77d-173">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="fc77d-173">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="fc77d-174">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="fc77d-174">See notes.</span></span> | <span data-ttu-id="fc77d-175">Cadeia de caracteres localizada correspondente ao tipo de controle **Thumb** .</span><span class="sxs-lookup"><span data-stu-id="fc77d-175">Localized string corresponding to the **Thumb** control type.</span></span> <span data-ttu-id="fc77d-176">O valor padrão é "Thumb" para en-US ou inglês (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="fc77d-176">The default value is "thumb" for en-US or English (United States).</span></span>                                                                                                                             |
| [<span data-ttu-id="fc77d-177">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="fc77d-177">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="fc77d-178">NULO</span><span class="sxs-lookup"><span data-stu-id="fc77d-178">NULL</span></span>       | <span data-ttu-id="fc77d-179">Como o controle Thumb não está disponível na exibição de conteúdo da árvore de automação da interface do usuário, ele não requer um nome.</span><span class="sxs-lookup"><span data-stu-id="fc77d-179">Because the thumb control is not available in the content view of the UI Automation tree, it does not require a name.</span></span>                                                                                                                                        |



 

## <a name="required-control-patterns"></a><span data-ttu-id="fc77d-180">Padrões de controle necessários</span><span class="sxs-lookup"><span data-stu-id="fc77d-180">Required Control Patterns</span></span>

<span data-ttu-id="fc77d-181">A tabela a seguir lista os padrões de controle de automação da interface do usuário necessários para serem suportados pelos controles Thumb.</span><span class="sxs-lookup"><span data-stu-id="fc77d-181">The following table lists the UI Automation control patterns required to be supported by thumb controls.</span></span> <span data-ttu-id="fc77d-182">Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="fc77d-182">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="fc77d-183">Padrão de controle</span><span class="sxs-lookup"><span data-stu-id="fc77d-183">Control Pattern</span></span>                                         | <span data-ttu-id="fc77d-184">Suporte</span><span class="sxs-lookup"><span data-stu-id="fc77d-184">Support</span></span>  | <span data-ttu-id="fc77d-185">Observações</span><span class="sxs-lookup"><span data-stu-id="fc77d-185">Notes</span></span>                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fc77d-186">**ITransformProvider**</span><span class="sxs-lookup"><span data-stu-id="fc77d-186">**ITransformProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | <span data-ttu-id="fc77d-187">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="fc77d-187">Required</span></span> | <span data-ttu-id="fc77d-188">Permite que o controle Thumb seja movido na tela.</span><span class="sxs-lookup"><span data-stu-id="fc77d-188">Enables the thumb control to be moved on the screen.</span></span> <span data-ttu-id="fc77d-189">Como o controle Thumb normalmente não pode ser redimensionado ou girado, o padrão de controle [Transform](uiauto-implementingtransform.md) dá suporte principalmente à função [**move**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-move) .</span><span class="sxs-lookup"><span data-stu-id="fc77d-189">Because the thumb control typically cannot be resized or rotated, the [Transform](uiauto-implementingtransform.md) control pattern primarily supports the [**Move**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-move) function.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="fc77d-190">Eventos necessários</span><span class="sxs-lookup"><span data-stu-id="fc77d-190">Required Events</span></span>

<span data-ttu-id="fc77d-191">A tabela a seguir lista os eventos de automação da interface do usuário aos quais os controles Thumb são necessários para dar suporte.</span><span class="sxs-lookup"><span data-stu-id="fc77d-191">The following table lists the UI Automation events that thumb controls are required to support.</span></span> <span data-ttu-id="fc77d-192">Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="fc77d-192">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="fc77d-193">Evento de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="fc77d-193">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="fc77d-194">Observações</span><span class="sxs-lookup"><span data-stu-id="fc77d-194">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fc77d-195">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="fc77d-195">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="fc77d-196">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="fc77d-196">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="fc77d-197">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="fc77d-197">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="fc77d-198">Se o controle oferecer suporte à propriedade [**IsEnabled**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="fc77d-198">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="fc77d-199">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="fc77d-199">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="fc77d-200">Se o controle oferecer suporte à propriedade [**IsOffscreen**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="fc77d-200">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="fc77d-201">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="fc77d-201">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="fc77d-202">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fc77d-202">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="fc77d-203">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="fc77d-203">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="fc77d-204">Visão Geral dos Tipos de Controle de Automação de Interface do Usuário</span><span class="sxs-lookup"><span data-stu-id="fc77d-204">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="fc77d-205">Visão geral de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="fc77d-205">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




