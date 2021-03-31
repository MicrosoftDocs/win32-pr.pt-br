---
title: Tipo de controle de caixa de seleção
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle CheckBox.
ms.assetid: 5a9061bc-2eac-4839-8f2c-32b9d58fe712
keywords:
- Automação da interface do usuário, suporte para tipo de controle de caixa de seleção
- Automação da interface do usuário, tipo de controle CheckBox
- Automação da interface do usuário, estrutura de árvore para tipo de controle de CheckBox
- Automação da interface do usuário, propriedades para tipo de controle de caixa de seleção
- Automação da interface do usuário, padrões de controle para tipo de controle CheckBox
- Automação da interface do usuário, eventos para tipo de controle de caixa de seleção
- estruturas de árvore, tipo de controle de caixa de seleção
- Propriedades, tipo de controle de caixa de seleção
- padrões de controle, tipo de controle de caixa de seleção
- tipo de controle eventos, CheckBox
- suporte para tipo de controle de caixa de seleção
- CheckBox (tipo de controle)
- tipos de controle, estrutura de árvore para tipo de controle de caixa de seleção
- tipos de controle, padrões de controle para tipo de controle de caixa de seleção
- tipos de controle, suporte para CheckBox
- tipos de controle, caixa de seleção
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8e5bac106c8ba3bbf58c7f5b06c087ceb7b3418
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822602"
---
# <a name="checkbox-control-type"></a><span data-ttu-id="07b11-119">Tipo de controle de caixa de seleção</span><span class="sxs-lookup"><span data-stu-id="07b11-119">CheckBox Control Type</span></span>

<span data-ttu-id="07b11-120">Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle **CheckBox** .</span><span class="sxs-lookup"><span data-stu-id="07b11-120">This topic provides information about Microsoft UI Automation support for the **CheckBox** control type.</span></span>

<span data-ttu-id="07b11-121">Uma caixa de seleção é um objeto usado para indicar um estado com o qual os usuários podem interagir para percorrer esse estado.</span><span class="sxs-lookup"><span data-stu-id="07b11-121">A check box is an object used to indicate a state that users can interact with to cycle through that state.</span></span> <span data-ttu-id="07b11-122">As caixas de seleção apresentam uma opção binary (Sim/não), (ligar/desligar) ou terciário (ativado, desativado, indeterminado) ao usuário.</span><span class="sxs-lookup"><span data-stu-id="07b11-122">Check boxes either present a binary (Yes/No), (On/Off), or tertiary (On, Off, Indeterminate) option to the user.</span></span>

<span data-ttu-id="07b11-123">As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle **CheckBox** .</span><span class="sxs-lookup"><span data-stu-id="07b11-123">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **CheckBox** control type.</span></span> <span data-ttu-id="07b11-124">Os requisitos de automação da interface do usuário se aplicam a todos os controles da caixa de seleção onde a estrutura/plataforma da interface do usuário integra o suporte à automação da interface do usuário para tipos de controle</span><span class="sxs-lookup"><span data-stu-id="07b11-124">The UI Automation requirements apply to all check box controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="07b11-125">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="07b11-125">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="07b11-126">Estrutura de árvore típica</span><span class="sxs-lookup"><span data-stu-id="07b11-126">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="07b11-127">Propriedades relevantes</span><span class="sxs-lookup"><span data-stu-id="07b11-127">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="07b11-128">Padrões de controle necessários</span><span class="sxs-lookup"><span data-stu-id="07b11-128">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="07b11-129">Eventos necessários</span><span class="sxs-lookup"><span data-stu-id="07b11-129">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="07b11-130">DefaultAction</span><span class="sxs-lookup"><span data-stu-id="07b11-130">DefaultAction</span></span>](#defaultaction)
-   [<span data-ttu-id="07b11-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="07b11-131">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="07b11-132">Estrutura de árvore típica</span><span class="sxs-lookup"><span data-stu-id="07b11-132">Typical Tree Structure</span></span>

<span data-ttu-id="07b11-133">A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence a controles de caixa de seleção e descreve o que pode ser contido em cada exibição.</span><span class="sxs-lookup"><span data-stu-id="07b11-133">The following table depicts a typical control and content view of the UI Automation tree that pertains to check box controls and describes what can be contained in each view.</span></span> <span data-ttu-id="07b11-134">Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="07b11-134">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="07b11-135">Exibição de controle</span><span class="sxs-lookup"><span data-stu-id="07b11-135">Control View</span></span></th>
<th><span data-ttu-id="07b11-136">Exibição de conteúdo</span><span class="sxs-lookup"><span data-stu-id="07b11-136">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="07b11-137">CheckBox</span><span class="sxs-lookup"><span data-stu-id="07b11-137">CheckBox</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="07b11-138">CheckBox</span><span class="sxs-lookup"><span data-stu-id="07b11-138">CheckBox</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="07b11-139">Propriedades relevantes</span><span class="sxs-lookup"><span data-stu-id="07b11-139">Relevant Properties</span></span>

<span data-ttu-id="07b11-140">A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para o tipo de controle de **caixa de seleção** .</span><span class="sxs-lookup"><span data-stu-id="07b11-140">The following table lists the UI Automation properties whose value or definition is especially relevant to the **CheckBox** control type.</span></span> <span data-ttu-id="07b11-141">Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="07b11-141">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="07b11-142">Propriedade de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="07b11-142">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="07b11-143">Valor</span><span class="sxs-lookup"><span data-stu-id="07b11-143">Value</span></span>        | <span data-ttu-id="07b11-144">Observações</span><span class="sxs-lookup"><span data-stu-id="07b11-144">Notes</span></span>                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="07b11-145">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="07b11-145">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="07b11-146">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="07b11-146">See notes.</span></span>   | <span data-ttu-id="07b11-147">O valor dessa propriedade deve ser exclusivo entre todos os elementos de mesmo nível na exibição bruta da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="07b11-147">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="07b11-148">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="07b11-148">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="07b11-149">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="07b11-149">See notes.</span></span>   | <span data-ttu-id="07b11-150">O retângulo mais externo que contém o controle inteiro.</span><span class="sxs-lookup"><span data-stu-id="07b11-150">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                                                                           |
| [<span data-ttu-id="07b11-151">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="07b11-151">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="07b11-152">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="07b11-152">See notes.</span></span>   | <span data-ttu-id="07b11-153">Com suporte se houver um retângulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="07b11-153">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="07b11-154">Se nem todos os pontos dentro do retângulo delimitador forem clicáveis, o elemento executará testes de clique especializados, substituirá e fornecerá um ponto clicável.</span><span class="sxs-lookup"><span data-stu-id="07b11-154">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span>                                                                               |
| [<span data-ttu-id="07b11-155">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="07b11-155">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="07b11-156">**CheckBox**</span><span class="sxs-lookup"><span data-stu-id="07b11-156">**CheckBox**</span></span> |                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="07b11-157">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="07b11-157">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="07b11-158">TRUE</span><span class="sxs-lookup"><span data-stu-id="07b11-158">TRUE</span></span>         | <span data-ttu-id="07b11-159">O valor dessa propriedade sempre deve ser **verdadeiro**.</span><span class="sxs-lookup"><span data-stu-id="07b11-159">The value of this property must always be **TRUE**.</span></span> <span data-ttu-id="07b11-160">Isso significa que o controle caixa de seleção sempre deve ser incluído na exibição de conteúdo da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="07b11-160">This means that the check box control must always be included in the content view of the UI Automation tree.</span></span>                                                                                                                   |
| [<span data-ttu-id="07b11-161">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="07b11-161">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="07b11-162">TRUE</span><span class="sxs-lookup"><span data-stu-id="07b11-162">TRUE</span></span>         | <span data-ttu-id="07b11-163">O valor dessa propriedade sempre deve ser **verdadeiro**.</span><span class="sxs-lookup"><span data-stu-id="07b11-163">The value of this property must always be **TRUE**.</span></span> <span data-ttu-id="07b11-164">Isso significa que o controle caixa de seleção sempre deve ser incluído na exibição de controle da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="07b11-164">This means that the check box control must always be included in the control view of the UI Automation tree.</span></span>                                                                                                                   |
| [<span data-ttu-id="07b11-165">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="07b11-165">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="07b11-166">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="07b11-166">See notes.</span></span>   | <span data-ttu-id="07b11-167">Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="07b11-167">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                                                                                                          |
| [<span data-ttu-id="07b11-168">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="07b11-168">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="07b11-169">Nulo</span><span class="sxs-lookup"><span data-stu-id="07b11-169">Null</span></span>         | <span data-ttu-id="07b11-170">Os controles da caixa de seleção são de autorotulação.</span><span class="sxs-lookup"><span data-stu-id="07b11-170">Check box controls are self-labeling.</span></span>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="07b11-171">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="07b11-171">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="07b11-172">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="07b11-172">See notes.</span></span>   | <span data-ttu-id="07b11-173">Cadeia de caracteres localizada correspondente ao tipo de controle de **caixa de seleção** .</span><span class="sxs-lookup"><span data-stu-id="07b11-173">Localized string corresponding to the **CheckBox** control type.</span></span> <span data-ttu-id="07b11-174">O valor padrão é "caixa de seleção" para en-US ou inglês (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="07b11-174">The default value is "check box" for en-US or English (United States).</span></span>                                                                                                                                            |
| [<span data-ttu-id="07b11-175">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="07b11-175">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="07b11-176">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="07b11-176">See notes.</span></span>   | <span data-ttu-id="07b11-177">O valor da propriedade [**IUIAutomationElement:: CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) (ou [**CachedName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedname)) do controle da caixa de seleção é o texto que é exibido ao lado da caixa que mantém o estado de alternância.</span><span class="sxs-lookup"><span data-stu-id="07b11-177">The value of the check box control's [**IUIAutomationElement::CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) (or [**CachedName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedname)) property is the text that is displayed beside the box that maintains the toggle state.</span></span> |



 

## <a name="required-control-patterns"></a><span data-ttu-id="07b11-178">Padrões de controle necessários</span><span class="sxs-lookup"><span data-stu-id="07b11-178">Required Control Patterns</span></span>

<span data-ttu-id="07b11-179">A tabela a seguir lista os padrões de controle de automação da interface do usuário que devem ser suportados por todos os controles da caixa de seleção.</span><span class="sxs-lookup"><span data-stu-id="07b11-179">The following table lists the UI Automation control patterns required to be supported by all check box controls.</span></span> <span data-ttu-id="07b11-180">Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="07b11-180">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="07b11-181">Propriedade padrão de controle/padrão</span><span class="sxs-lookup"><span data-stu-id="07b11-181">Control Pattern/Pattern Property</span></span>                  | <span data-ttu-id="07b11-182">Suporte/valor</span><span class="sxs-lookup"><span data-stu-id="07b11-182">Support/Value</span></span> | <span data-ttu-id="07b11-183">Observações</span><span class="sxs-lookup"><span data-stu-id="07b11-183">Notes</span></span>                                                                                                                                                             |
|---------------------------------------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="07b11-184">**IToggleProvider**</span><span class="sxs-lookup"><span data-stu-id="07b11-184">**IToggleProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) | <span data-ttu-id="07b11-185">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="07b11-185">Required</span></span>      | <span data-ttu-id="07b11-186">As caixas de seleção dão suporte ao padrão de controle de [alternância](uiauto-implementingtoggle.md) para permitir que a caixa de seleção seja programaticamente alternada pelos Estados internos.</span><span class="sxs-lookup"><span data-stu-id="07b11-186">Check boxes support the [Toggle](uiauto-implementingtoggle.md) control pattern to allow the check box to be programmatically cycled through its internal states.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="07b11-187">Eventos necessários</span><span class="sxs-lookup"><span data-stu-id="07b11-187">Required Events</span></span>

<span data-ttu-id="07b11-188">A tabela a seguir lista os eventos de automação da interface do usuário que são necessários para dar suporte aos controles de caixa de seleção.</span><span class="sxs-lookup"><span data-stu-id="07b11-188">The following table lists the UI Automation events that check box controls are required to support.</span></span> <span data-ttu-id="07b11-189">Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="07b11-189">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="07b11-190">Evento de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="07b11-190">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="07b11-191">Observações</span><span class="sxs-lookup"><span data-stu-id="07b11-191">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="07b11-192">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="07b11-192">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="07b11-193">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="07b11-193">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="07b11-194">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="07b11-194">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="07b11-195">Se o controle oferecer suporte à propriedade [**IsOffscreen**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="07b11-195">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| <span data-ttu-id="07b11-196">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="07b11-196">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="07b11-197">Se o controle oferecer suporte à propriedade [**IsEnabled**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="07b11-197">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| [<span data-ttu-id="07b11-198">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="07b11-198">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |
| <span data-ttu-id="07b11-199">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ToggleToggleStatePropertyId.</span><span class="sxs-lookup"><span data-stu-id="07b11-199">[**UIA\_ToggleToggleStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>    |                                                                                                                            |



 

## <a name="defaultaction"></a><span data-ttu-id="07b11-200">DefaultAction</span><span class="sxs-lookup"><span data-stu-id="07b11-200">DefaultAction</span></span>

<span data-ttu-id="07b11-201">A ação padrão da caixa de seleção é fazer com que um botão de opção se concentre e alterne seu estado atual.</span><span class="sxs-lookup"><span data-stu-id="07b11-201">The default action of the check box is to cause a radio button to become focused and toggle its current state.</span></span> <span data-ttu-id="07b11-202">Conforme mencionado anteriormente, as caixas de seleção apresentam uma decisão binária (Sim/não ou ativar/desativar) para o usuário ou um terciário (on, off, indeterminado).</span><span class="sxs-lookup"><span data-stu-id="07b11-202">As mentioned previously, check boxes either present a binary (Yes/No or On/Off) decision to the user or a tertiary (On, Off, Indeterminate).</span></span> <span data-ttu-id="07b11-203">Se a caixa de seleção for binária, a ação padrão fará com que o estado "ativado" se torne "desativado" ou "desativado" para se tornar "ligado".</span><span class="sxs-lookup"><span data-stu-id="07b11-203">If the check box is binary the default action causes the "on" state to become "off" or the "off" state to become "on".</span></span> <span data-ttu-id="07b11-204">Em uma caixa de seleção terciário, a ação padrão percorre os Estados da caixa de seleção na mesma ordem em que o usuário enviou cliques de mouse sucessivos para o controle.</span><span class="sxs-lookup"><span data-stu-id="07b11-204">In a tertiary check box the default action cycles through the states of the check box in the same order as if the user had sent successive mouse clicks to the control.</span></span>

## <a name="related-topics"></a><span data-ttu-id="07b11-205">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="07b11-205">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="07b11-206">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="07b11-206">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="07b11-207">Visão Geral dos Tipos de Controle de Automação de Interface do Usuário</span><span class="sxs-lookup"><span data-stu-id="07b11-207">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="07b11-208">Visão geral de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="07b11-208">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




