---
title: Tipo de controle RadioButton
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle RadioButton.
ms.assetid: 6fc4a6a3-f5c0-402b-b9e7-870dfaa3370d
keywords:
- Automação da interface do usuário, suporte para tipo de controle RadioButton
- Automação da interface do usuário, tipo de controle RadioButton
- Automação da interface do usuário, estrutura de árvore para tipo de controle RadioButton
- Automação da interface do usuário, propriedades para tipo de controle RadioButton
- Automação da interface do usuário, padrões de controle para tipo de controle RadioButton
- Automação da interface do usuário, eventos para tipo de controle RadioButton
- estruturas de árvore, tipo de controle RadioButton
- Propriedades, tipo de controle RadioButton
- padrões de controle, tipo de controle RadioButton
- eventos, tipo de controle RadioButton
- suporte para tipo de controle RadioButton
- RadioButton (tipo de controle)
- tipos de controle, estrutura de árvore para tipo de controle RadioButton
- tipos de controle, padrões de controle para tipo de controle RadioButton
- tipos de controle, suporte para RadioButton
- tipos de controle, RadioButton
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4702a2227a5164ff694378c82fa3b7cde33f9823
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636636"
---
# <a name="radiobutton-control-type"></a><span data-ttu-id="b1974-119">Tipo de controle RadioButton</span><span class="sxs-lookup"><span data-stu-id="b1974-119">RadioButton Control Type</span></span>

<span data-ttu-id="b1974-120">Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle **RadioButton** .</span><span class="sxs-lookup"><span data-stu-id="b1974-120">This topic provides information about Microsoft UI Automation support for the **RadioButton** control type.</span></span>

<span data-ttu-id="b1974-121">Um botão de opção consiste em um botão redondo e um texto definido pelo aplicativo (um rótulo), um ícone ou um bitmap que indica uma opção que o usuário pode fazer selecionando o botão.</span><span class="sxs-lookup"><span data-stu-id="b1974-121">A radio button consists of a round button and application-defined text (a label), an icon, or a bitmap that indicates a choice the user can make by selecting the button.</span></span> <span data-ttu-id="b1974-122">Um aplicativo geralmente usa botões de opção em uma caixa de grupo para permitir que o usuário escolha entre um conjunto de opções relacionadas, mas mutuamente exclusivas.</span><span class="sxs-lookup"><span data-stu-id="b1974-122">An application typically uses radio buttons in a group box to permit the user to choose from a set of related, but mutually exclusive options.</span></span> <span data-ttu-id="b1974-123">Por exemplo, o aplicativo pode apresentar um grupo de botões de opção do qual o usuário pode selecionar uma preferência de formato para o texto selecionado na área cliente.</span><span class="sxs-lookup"><span data-stu-id="b1974-123">For example, the application might present a group of radio buttons from which the user can select a format preference for text selected in the client area.</span></span> <span data-ttu-id="b1974-124">O usuário pode selecionar um formato alinhado à esquerda, alinhado à direita ou centralizado selecionando o botão de opção correspondente.</span><span class="sxs-lookup"><span data-stu-id="b1974-124">The user could select a left-aligned, right-aligned, or centered format by selecting the corresponding radio button.</span></span> <span data-ttu-id="b1974-125">Normalmente, o usuário pode selecionar apenas uma opção por vez de um conjunto de botões de opção.</span><span class="sxs-lookup"><span data-stu-id="b1974-125">Typically, the user can select only one option at a time from a set of radio buttons.</span></span>

> [!Note]  
> <span data-ttu-id="b1974-126">Outra generalização de controle para botões em que apenas um em um grupo pode ser selecionado é o conteúdo de um botão de alternância.</span><span class="sxs-lookup"><span data-stu-id="b1974-126">Another control generalization for buttons where only one in a group can be selected is the content of a toggle button.</span></span> <span data-ttu-id="b1974-127">Algumas estruturas de interface do usuário consideram um botão de opção como um botão de alternância especializado.</span><span class="sxs-lookup"><span data-stu-id="b1974-127">Some UI frameworks consider a radio button to be a specialized toggle button.</span></span>

 

<span data-ttu-id="b1974-128">As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle **RadioButton** .</span><span class="sxs-lookup"><span data-stu-id="b1974-128">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **RadioButton** control type.</span></span> <span data-ttu-id="b1974-129">Os requisitos de automação da interface do usuário se aplicam a todos os controles de botão onde a estrutura/plataforma da interface do usuário integra o suporte à automação da interface do usuário para tipos de controle</span><span class="sxs-lookup"><span data-stu-id="b1974-129">The UI Automation requirements apply to all button controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="b1974-130">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="b1974-130">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="b1974-131">Estrutura de árvore típica</span><span class="sxs-lookup"><span data-stu-id="b1974-131">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="b1974-132">Propriedades relevantes</span><span class="sxs-lookup"><span data-stu-id="b1974-132">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="b1974-133">Padrões de controle necessários</span><span class="sxs-lookup"><span data-stu-id="b1974-133">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="b1974-134">Eventos necessários</span><span class="sxs-lookup"><span data-stu-id="b1974-134">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="b1974-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="b1974-135">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="b1974-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b1974-136">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="b1974-137">Estrutura de árvore típica</span><span class="sxs-lookup"><span data-stu-id="b1974-137">Typical Tree Structure</span></span>

<span data-ttu-id="b1974-138">A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence aos controles de botão de opção e descreve o que pode ser contido em cada exibição.</span><span class="sxs-lookup"><span data-stu-id="b1974-138">The following table depicts a typical control and content view of the UI Automation tree that pertains to radio button controls and describes what can be contained in each view.</span></span> <span data-ttu-id="b1974-139">Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="b1974-139">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b1974-140">Exibição de controle</span><span class="sxs-lookup"><span data-stu-id="b1974-140">Control View</span></span></th>
<th><span data-ttu-id="b1974-141">Exibição de conteúdo</span><span class="sxs-lookup"><span data-stu-id="b1974-141">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="b1974-142">RadioButton</span><span class="sxs-lookup"><span data-stu-id="b1974-142">RadioButton</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="b1974-143">RadioButton</span><span class="sxs-lookup"><span data-stu-id="b1974-143">RadioButton</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="b1974-144">Não há filhos na exibição de controle nem no modo de exibição de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="b1974-144">There are no children in the control view or the content view.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="b1974-145">Propriedades relevantes</span><span class="sxs-lookup"><span data-stu-id="b1974-145">Relevant Properties</span></span>

<span data-ttu-id="b1974-146">A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para os controles que implementam o tipo de controle **RadioButton** (como controles Button).</span><span class="sxs-lookup"><span data-stu-id="b1974-146">The following table lists the UI Automation properties whose value or definition is especially relevant to the controls that implement the **RadioButton** control type (such as button controls).</span></span> <span data-ttu-id="b1974-147">Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="b1974-147">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="b1974-148">Propriedade de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="b1974-148">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="b1974-149">Valor</span><span class="sxs-lookup"><span data-stu-id="b1974-149">Value</span></span>           | <span data-ttu-id="b1974-150">Observações</span><span class="sxs-lookup"><span data-stu-id="b1974-150">Notes</span></span>                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b1974-151">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="b1974-151">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="b1974-152">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="b1974-152">See notes.</span></span>      | <span data-ttu-id="b1974-153">O valor dessa propriedade deve ser exclusivo entre todos os elementos de mesmo nível na exibição bruta da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="b1974-153">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                  |
| [<span data-ttu-id="b1974-154">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="b1974-154">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="b1974-155">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="b1974-155">See notes.</span></span>      | <span data-ttu-id="b1974-156">O retângulo mais externo que contém o controle inteiro.</span><span class="sxs-lookup"><span data-stu-id="b1974-156">The outermost rectangle that contains the whole control.</span></span>                                                                                      |
| [<span data-ttu-id="b1974-157">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="b1974-157">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="b1974-158">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="b1974-158">See notes.</span></span>      | <span data-ttu-id="b1974-159">O ponto clicável deve ser um ponto que, quando clicado, seleciona o botão de opção.</span><span class="sxs-lookup"><span data-stu-id="b1974-159">The clickable point must be a point that, when clicked, selects the radio button.</span></span>                                                             |
| [<span data-ttu-id="b1974-160">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="b1974-160">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="b1974-161">**RadioButton**</span><span class="sxs-lookup"><span data-stu-id="b1974-161">**RadioButton**</span></span> |                                                                                                                                               |
| [<span data-ttu-id="b1974-162">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="b1974-162">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="b1974-163">TRUE</span><span class="sxs-lookup"><span data-stu-id="b1974-163">TRUE</span></span>            | <span data-ttu-id="b1974-164">O controle de botão de opção sempre é incluído na exibição de conteúdo da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="b1974-164">The radio button control is always included in the content view of the UI Automation tree.</span></span>                                                    |
| [<span data-ttu-id="b1974-165">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="b1974-165">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="b1974-166">TRUE</span><span class="sxs-lookup"><span data-stu-id="b1974-166">TRUE</span></span>            | <span data-ttu-id="b1974-167">O controle de botão de opção sempre é incluído no modo de exibição de controle da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="b1974-167">The radio button control is always included in the control view of the UI Automation tree.</span></span>                                                    |
| [<span data-ttu-id="b1974-168">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="b1974-168">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="b1974-169">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="b1974-169">See notes.</span></span>      | <span data-ttu-id="b1974-170">Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="b1974-170">If the control can receive keyboard focus, it must support this property.</span></span>                                                                     |
| [<span data-ttu-id="b1974-171">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="b1974-171">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="b1974-172">NULO</span><span class="sxs-lookup"><span data-stu-id="b1974-172">NULL</span></span>            | <span data-ttu-id="b1974-173">Os controles de botão de opção são rotulados automaticamente por seu conteúdo.</span><span class="sxs-lookup"><span data-stu-id="b1974-173">Radio button controls are self-labeled by their contents.</span></span>                                                                                     |
| [<span data-ttu-id="b1974-174">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="b1974-174">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="b1974-175">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="b1974-175">See notes.</span></span>      | <span data-ttu-id="b1974-176">Cadeia de caracteres localizada correspondente ao tipo de controle **RadioButton** .</span><span class="sxs-lookup"><span data-stu-id="b1974-176">Localized string corresponding to the **RadioButton** control type.</span></span> <span data-ttu-id="b1974-177">O valor padrão é "botão de opção" para en-US ou inglês (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="b1974-177">The default value is "radio button" for en-US or English (United States).</span></span> |
| [<span data-ttu-id="b1974-178">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="b1974-178">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="b1974-179">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="b1974-179">See notes.</span></span>      | <span data-ttu-id="b1974-180">O nome do controle de botão de opção é o texto exibido ao lado do botão que mantém o estado de seleção.</span><span class="sxs-lookup"><span data-stu-id="b1974-180">The name of the radio button control is the text that is displayed beside the button that maintains the selection state.</span></span>                      |



 

## <a name="required-control-patterns"></a><span data-ttu-id="b1974-181">Padrões de controle necessários</span><span class="sxs-lookup"><span data-stu-id="b1974-181">Required Control Patterns</span></span>

<span data-ttu-id="b1974-182">A tabela a seguir lista os padrões de controle de automação da interface do usuário que devem ter suporte de todos os controles de botão de opção.</span><span class="sxs-lookup"><span data-stu-id="b1974-182">The following table lists the UI Automation control patterns required to be supported by all radio button controls.</span></span> <span data-ttu-id="b1974-183">Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="b1974-183">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="b1974-184">Propriedade padrão de controle/padrão</span><span class="sxs-lookup"><span data-stu-id="b1974-184">Control Pattern/Pattern Property</span></span>                                               | <span data-ttu-id="b1974-185">Suporte/valor</span><span class="sxs-lookup"><span data-stu-id="b1974-185">Support/Value</span></span> | <span data-ttu-id="b1974-186">Observações</span><span class="sxs-lookup"><span data-stu-id="b1974-186">Notes</span></span>                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b1974-187">**ISelectionItemProvider**</span><span class="sxs-lookup"><span data-stu-id="b1974-187">**ISelectionItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)                | <span data-ttu-id="b1974-188">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="b1974-188">Required</span></span>      | <span data-ttu-id="b1974-189">Todos os controles de botão de opção devem dar suporte ao padrão de controle [SelectionItem](uiauto-implementingselectionitem.md) para permitir que eles sejam selecionados.</span><span class="sxs-lookup"><span data-stu-id="b1974-189">All radio button controls must support the [SelectionItem](uiauto-implementingselectionitem.md) control pattern to enable themselves to be selected.</span></span>                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="b1974-190">**SelectionContainer**</span><span class="sxs-lookup"><span data-stu-id="b1974-190">**SelectionContainer**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer) | <span data-ttu-id="b1974-191">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="b1974-191">See notes.</span></span>    | <span data-ttu-id="b1974-192">A propriedade [**SelectionContainer**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer) sempre deve ser concluída para que um cliente de automação de interface do usuário possa determinar quais outros botões de rádio dentro de um contexto específico se relacionam entre si.</span><span class="sxs-lookup"><span data-stu-id="b1974-192">The [**SelectionContainer**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer) property must always be completed so that a UI Automation client can determine what other radio buttons within a specific context relate to one another.</span></span> <span data-ttu-id="b1974-193">Para a versão Microsoft Win32 do botão de opção, essa propriedade não tem suporte porque não é possível obter essas informações dessa estrutura herdada.</span><span class="sxs-lookup"><span data-stu-id="b1974-193">For the Microsoft Win32 version of the radio button, this property is not supported because it is not possible to obtain this information from that legacy framework.</span></span> |
| [<span data-ttu-id="b1974-194">**IToggleProvider**</span><span class="sxs-lookup"><span data-stu-id="b1974-194">**IToggleProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                              | <span data-ttu-id="b1974-195">Nunca</span><span class="sxs-lookup"><span data-stu-id="b1974-195">Never</span></span>         | <span data-ttu-id="b1974-196">O botão de opção não pode percorrer seu estado depois de definido.</span><span class="sxs-lookup"><span data-stu-id="b1974-196">The radio button cannot cycle through its state once it has been set.</span></span> <span data-ttu-id="b1974-197">O padrão de controle de [alternância](uiauto-implementingtoggle.md) nunca deve ter suporte em um botão de opção.</span><span class="sxs-lookup"><span data-stu-id="b1974-197">The [Toggle](uiauto-implementingtoggle.md) control pattern must never be supported on a radio button.</span></span>                                                                                                                                                                                                                                      |



 

## <a name="required-events"></a><span data-ttu-id="b1974-198">Eventos necessários</span><span class="sxs-lookup"><span data-stu-id="b1974-198">Required Events</span></span>

<span data-ttu-id="b1974-199">A tabela a seguir lista os eventos de automação da interface do usuário aos quais os controles de botão são necessários para dar suporte.</span><span class="sxs-lookup"><span data-stu-id="b1974-199">The following table lists the UI Automation events that button controls are required to support.</span></span> <span data-ttu-id="b1974-200">Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="b1974-200">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="b1974-201">Evento de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="b1974-201">UI Automation Event</span></span>                                                                                                                     | <span data-ttu-id="b1974-202">Observações</span><span class="sxs-lookup"><span data-stu-id="b1974-202">Notes</span></span>                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b1974-203">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="b1974-203">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                        |                                                                                                                                |
| <span data-ttu-id="b1974-204">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="b1974-204">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>   |                                                                                                                                |
| <span data-ttu-id="b1974-205">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="b1974-205">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                   | <span data-ttu-id="b1974-206">Se o controle oferecer suporte à propriedade [**IsEnabled**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="b1974-206">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>       |
| <span data-ttu-id="b1974-207">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="b1974-207">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>               | <span data-ttu-id="b1974-208">Se o controle oferecer suporte à propriedade [**IsOffscreen**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="b1974-208">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>     |
| [<span data-ttu-id="b1974-209">**UIA \_ SelectionItem \_ ElementRemovedFromSelectionEventId**</span><span class="sxs-lookup"><span data-stu-id="b1974-209">**UIA\_SelectionItem\_ElementRemovedFromSelectionEventId**</span></span>](uiauto-event-ids.md) | <span data-ttu-id="b1974-210">Se o controle der suporte ao padrão de controle [SelectionItem](uiauto-implementingselectionitem.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="b1974-210">If the control supports the [SelectionItem](uiauto-implementingselectionitem.md) control pattern, it must support this event.</span></span> |
| [<span data-ttu-id="b1974-211">**UIA \_ SelectionItem \_ ElementSelectedEventId**</span><span class="sxs-lookup"><span data-stu-id="b1974-211">**UIA\_SelectionItem\_ElementSelectedEventId**</span></span>](uiauto-event-ids.md)                         | <span data-ttu-id="b1974-212">Se o controle der suporte ao padrão de controle [SelectionItem](uiauto-implementingselectionitem.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="b1974-212">If the control supports the [SelectionItem](uiauto-implementingselectionitem.md) control pattern, it must support this event.</span></span> |
| [<span data-ttu-id="b1974-213">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="b1974-213">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                    |                                                                                                                                |



 

## <a name="remarks"></a><span data-ttu-id="b1974-214">Comentários</span><span class="sxs-lookup"><span data-stu-id="b1974-214">Remarks</span></span>

<span data-ttu-id="b1974-215">Um botão de opção representa uma única opção selecionável entre um grupo de botões de opção de mesmo nível.</span><span class="sxs-lookup"><span data-stu-id="b1974-215">A radio button represents a single selectable option among a group of peer radio buttons.</span></span> <span data-ttu-id="b1974-216">O ideal é que os botões de rádio tenham um elemento de agrupamento que esclarece os limites dos botões de opção de pares.</span><span class="sxs-lookup"><span data-stu-id="b1974-216">Ideally, radio buttons should have a grouping element that clarifies the boundaries of the peer radio buttons.</span></span> <span data-ttu-id="b1974-217">Geralmente, no entanto, o limite é implícito pela estrutura do elemento da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="b1974-217">Often, however, the boundary is implied by the UI element structure.</span></span> <span data-ttu-id="b1974-218">Por exemplo, um menu pode conter um conjunto de botões de opção consecutivos em vez de itens de menu, ou um conjunto de botões de opção que ocorrem após um rótulo de grupo, mas antes de um elemento acionável, como Button.</span><span class="sxs-lookup"><span data-stu-id="b1974-218">For example, a menu might contain a set of consecutive radio buttons instead of menu items, or a set of radio buttons that occur after a group label, but before an actionable element such as button.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b1974-219">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b1974-219">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b1974-220">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="b1974-220">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b1974-221">Visão Geral dos Tipos de Controle de Automação de Interface do Usuário</span><span class="sxs-lookup"><span data-stu-id="b1974-221">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="b1974-222">Visão geral de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="b1974-222">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




