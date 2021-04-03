---
title: Tipo de controle SplitButton
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle SplitButton.
ms.assetid: ca4f8e45-7487-4a8b-9df5-edc2b0e56663
keywords:
- Automação da interface do usuário, suporte para tipo de controle SplitButton
- Automação da interface do usuário, tipo de controle SplitButton
- Automação da interface do usuário, estrutura de árvore para tipo de controle SplitButton
- Automação da interface do usuário, propriedades para tipo de controle SplitButton
- Automação da interface do usuário, padrões de controle para tipo de controle SplitButton
- Automação da interface do usuário, eventos para tipo de controle SplitButton
- estruturas de árvore, tipo de controle SplitButton
- Propriedades, tipo de controle SplitButton
- padrões de controle, tipo de controle SplitButton
- eventos, tipo de controle SplitButton
- suporte para tipo de controle SplitButton
- Tipo de controle SplitButton
- tipos de controle, estrutura de árvore para tipo de controle SplitButton
- tipos de controle, padrões de controle para tipo de controle SplitButton
- tipos de controle, suporte para SplitButton
- tipos de controle, SplitButton
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c56cd6b22838dfa92ba25ce05e74d228f4173ac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636634"
---
# <a name="splitbutton-control-type"></a><span data-ttu-id="29e26-119">Tipo de controle SplitButton</span><span class="sxs-lookup"><span data-stu-id="29e26-119">SplitButton Control Type</span></span>

<span data-ttu-id="29e26-120">Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle **SplitButton** .</span><span class="sxs-lookup"><span data-stu-id="29e26-120">This topic provides information about Microsoft UI Automation support for the **SplitButton** control type.</span></span>

<span data-ttu-id="29e26-121">O controle botão de divisão permite que uma ação seja executada em um controle e expanda o controle para ver uma lista de outras ações possíveis que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="29e26-121">The split button control enables an action to be performed on a control, and to expand the control to see a list of other possible actions that can be performed.</span></span>

<span data-ttu-id="29e26-122">As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle **SplitButton** .</span><span class="sxs-lookup"><span data-stu-id="29e26-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **SplitButton** control type.</span></span> <span data-ttu-id="29e26-123">Os requisitos de automação da interface do usuário se aplicam a todos os controles do botão de divisão onde a plataforma/estrutura da interface do usuário integra o suporte de automação da interface do usuário para tipos de controle</span><span class="sxs-lookup"><span data-stu-id="29e26-123">The UI Automation requirements apply to all split button controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="29e26-124">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="29e26-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="29e26-125">Estrutura de árvore típica</span><span class="sxs-lookup"><span data-stu-id="29e26-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="29e26-126">Propriedades relevantes</span><span class="sxs-lookup"><span data-stu-id="29e26-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="29e26-127">Padrões de controle necessários</span><span class="sxs-lookup"><span data-stu-id="29e26-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="29e26-128">Eventos necessários</span><span class="sxs-lookup"><span data-stu-id="29e26-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="29e26-129">Exemplo do tipo de controle SplitButton</span><span class="sxs-lookup"><span data-stu-id="29e26-129">SplitButton Control Type Example</span></span>](#splitbutton-control-type-example)
-   [<span data-ttu-id="29e26-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="29e26-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="29e26-131">Estrutura de árvore típica</span><span class="sxs-lookup"><span data-stu-id="29e26-131">Typical Tree Structure</span></span>

<span data-ttu-id="29e26-132">A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence aos controles de botão de divisão e descreve o que pode ser contido em cada exibição.</span><span class="sxs-lookup"><span data-stu-id="29e26-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to split button controls and describes what can be contained in each view.</span></span> <span data-ttu-id="29e26-133">Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="29e26-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="29e26-134">Exibição de controle</span><span class="sxs-lookup"><span data-stu-id="29e26-134">Control View</span></span></th>
<th><span data-ttu-id="29e26-135">Exibição de conteúdo</span><span class="sxs-lookup"><span data-stu-id="29e26-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="29e26-136">SplitButton</span><span class="sxs-lookup"><span data-stu-id="29e26-136">SplitButton</span></span>
<ul>
<li><span data-ttu-id="29e26-137">Imagem (0 ou 1)</span><span class="sxs-lookup"><span data-stu-id="29e26-137">Image (0 or 1)</span></span></li>
<li><span data-ttu-id="29e26-138">Texto (0 ou 1)</span><span class="sxs-lookup"><span data-stu-id="29e26-138">Text (0 or 1)</span></span></li>
<li><span data-ttu-id="29e26-139">Botão (1 ou 2)</span><span class="sxs-lookup"><span data-stu-id="29e26-139">Button (1 or 2)</span></span>
<ul>
<li><span data-ttu-id="29e26-140">O menu (0 ou 1; é exibido como um filho de um subbotão que dá suporte ao padrão ExpandCollapse)</span><span class="sxs-lookup"><span data-stu-id="29e26-140">Menu (0 or 1; appears as a child of a sub-button that supports the ExpandCollapse pattern)</span></span>
<ul>
<li><span data-ttu-id="29e26-141">MenuItem (1 para muitos)</span><span class="sxs-lookup"><span data-stu-id="29e26-141">MenuItem (1 to many)</span></span></li>
</ul></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="29e26-142">SplitButton</span><span class="sxs-lookup"><span data-stu-id="29e26-142">SplitButton</span></span>
<ul>
<li><span data-ttu-id="29e26-143">Botão (1 ou 2)</span><span class="sxs-lookup"><span data-stu-id="29e26-143">Button (1 or 2)</span></span>
<ul>
<li><span data-ttu-id="29e26-144">MenuItem (1 para muitos)</span><span class="sxs-lookup"><span data-stu-id="29e26-144">MenuItem (1 to many)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="29e26-145">Propriedades relevantes</span><span class="sxs-lookup"><span data-stu-id="29e26-145">Relevant Properties</span></span>

<span data-ttu-id="29e26-146">A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para o tipo de controle **SplitButton** .</span><span class="sxs-lookup"><span data-stu-id="29e26-146">The following table lists the UI Automation properties whose value or definition is especially relevant to the **SplitButton** control type.</span></span> <span data-ttu-id="29e26-147">Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="29e26-147">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="29e26-148">Propriedade de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="29e26-148">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="29e26-149">Valor</span><span class="sxs-lookup"><span data-stu-id="29e26-149">Value</span></span>           | <span data-ttu-id="29e26-150">Observações</span><span class="sxs-lookup"><span data-stu-id="29e26-150">Notes</span></span>                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="29e26-151">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="29e26-151">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="29e26-152">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="29e26-152">See notes.</span></span>      | <span data-ttu-id="29e26-153">O valor dessa propriedade deve ser exclusivo entre todos os elementos de mesmo nível na exibição bruta da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="29e26-153">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                         |
| [<span data-ttu-id="29e26-154">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="29e26-154">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="29e26-155">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="29e26-155">See notes.</span></span>      | <span data-ttu-id="29e26-156">O retângulo mais externo que contém o controle inteiro.</span><span class="sxs-lookup"><span data-stu-id="29e26-156">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                             |
| [<span data-ttu-id="29e26-157">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="29e26-157">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="29e26-158">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="29e26-158">See notes.</span></span>      | <span data-ttu-id="29e26-159">Com suporte se houver um retângulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="29e26-159">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="29e26-160">Se nem todos os pontos dentro do retângulo delimitador forem clicáveis, o elemento executará testes de clique especializados, substituirá e fornecerá um ponto clicável.</span><span class="sxs-lookup"><span data-stu-id="29e26-160">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span> |
| [<span data-ttu-id="29e26-161">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="29e26-161">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="29e26-162">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="29e26-162">**SplitButton**</span></span> | <span data-ttu-id="29e26-163">Esse valor é o mesmo para todas as estruturas de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="29e26-163">This value is the same for all UI frameworks.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="29e26-164">**UIA \_ HelpTextPropertyId**</span><span class="sxs-lookup"><span data-stu-id="29e26-164">**UIA\_HelpTextPropertyId**</span></span>](uiauto-automation-element-propids.md)                         | <span data-ttu-id="29e26-165">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="29e26-165">See notes.</span></span>      | <span data-ttu-id="29e26-166">O texto de ajuda pode indicar o resultado da ativação do botão de divisão, que geralmente é o mesmo tipo de informações apresentadas por meio de uma dica de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="29e26-166">The help text can indicate the result of activating the split button, which is typically the same type of information presented through a tooltip.</span></span>                                                   |
| [<span data-ttu-id="29e26-167">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="29e26-167">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="29e26-168">TRUE</span><span class="sxs-lookup"><span data-stu-id="29e26-168">TRUE</span></span>            | <span data-ttu-id="29e26-169">O controle de botão de divisão contém informações para o usuário final.</span><span class="sxs-lookup"><span data-stu-id="29e26-169">The split button control contains information for the end user.</span></span>                                                                                                                                      |
| [<span data-ttu-id="29e26-170">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="29e26-170">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="29e26-171">TRUE</span><span class="sxs-lookup"><span data-stu-id="29e26-171">TRUE</span></span>            | <span data-ttu-id="29e26-172">O controle do botão de divisão é visível para o usuário final.</span><span class="sxs-lookup"><span data-stu-id="29e26-172">The split button control is visible to the end user.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="29e26-173">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="29e26-173">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="29e26-174">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="29e26-174">See notes.</span></span>      | <span data-ttu-id="29e26-175">Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="29e26-175">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                            |
| [<span data-ttu-id="29e26-176">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="29e26-176">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="29e26-177">NULO</span><span class="sxs-lookup"><span data-stu-id="29e26-177">NULL</span></span>            | <span data-ttu-id="29e26-178">Os controles do botão de divisão não têm um rótulo de texto estático.</span><span class="sxs-lookup"><span data-stu-id="29e26-178">Split button controls do not have a static text label.</span></span>                                                                                                                                               |
| [<span data-ttu-id="29e26-179">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="29e26-179">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="29e26-180">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="29e26-180">See notes.</span></span>      | <span data-ttu-id="29e26-181">Cadeia de caracteres localizada correspondente ao tipo de controle **SplitButton** .</span><span class="sxs-lookup"><span data-stu-id="29e26-181">Localized string corresponding to the **SplitButton** control type.</span></span> <span data-ttu-id="29e26-182">O valor padrão é "botão de divisão" para en-US ou inglês (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="29e26-182">The default value is "split button" for en-US or English (United States).</span></span>                                                        |
| [<span data-ttu-id="29e26-183">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="29e26-183">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="29e26-184">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="29e26-184">See notes.</span></span>      | <span data-ttu-id="29e26-185">O texto que é usado para rotular o botão de divisão.</span><span class="sxs-lookup"><span data-stu-id="29e26-185">The text that is used to label the split button.</span></span> <span data-ttu-id="29e26-186">Sempre que uma imagem é usada para rotular um botão de divisão, o texto alternativo deve ser fornecido para a propriedade nome do botão de divisão.</span><span class="sxs-lookup"><span data-stu-id="29e26-186">Whenever an image is used to label a split button, alternate text must be supplied for the split button Name property.</span></span>                              |



 

## <a name="required-control-patterns"></a><span data-ttu-id="29e26-187">Padrões de controle necessários</span><span class="sxs-lookup"><span data-stu-id="29e26-187">Required Control Patterns</span></span>

<span data-ttu-id="29e26-188">A tabela a seguir lista os padrões de controle de automação da interface do usuário que devem ser suportados por todos os controles de botão de divisão.</span><span class="sxs-lookup"><span data-stu-id="29e26-188">The following table lists the UI Automation control patterns required to be supported by all split button controls.</span></span> <span data-ttu-id="29e26-189">Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="29e26-189">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="29e26-190">Padrão de controle</span><span class="sxs-lookup"><span data-stu-id="29e26-190">Control Pattern</span></span>                                                   | <span data-ttu-id="29e26-191">Suporte</span><span class="sxs-lookup"><span data-stu-id="29e26-191">Support</span></span>  | <span data-ttu-id="29e26-192">Observações</span><span class="sxs-lookup"><span data-stu-id="29e26-192">Notes</span></span>                                                                                                                                                                                                                          |
|-------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="29e26-193">**IExpandCollapseProvider**</span><span class="sxs-lookup"><span data-stu-id="29e26-193">**IExpandCollapseProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | <span data-ttu-id="29e26-194">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="29e26-194">Required</span></span> | <span data-ttu-id="29e26-195">Como os botões de divisão sempre têm a capacidade de expandir uma lista de opções, eles devem dar suporte ao padrão de controle [ExpandCollapse](uiauto-implementingexpandcollapse.md) .</span><span class="sxs-lookup"><span data-stu-id="29e26-195">Because split buttons always have the ability to expand a list of options, they must support the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern.</span></span>                                                      |
| [<span data-ttu-id="29e26-196">**IInvokeProvider**</span><span class="sxs-lookup"><span data-stu-id="29e26-196">**IInvokeProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                 | <span data-ttu-id="29e26-197">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="29e26-197">Required</span></span> | <span data-ttu-id="29e26-198">Como os botões de divisão sempre têm uma ação padrão associada ao método [**IInvokeProvider:: Invoke**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iinvokeprovider-invoke) , eles devem oferecer suporte ao padrão de controle [Invoke](uiauto-implementinginvoke.md) .</span><span class="sxs-lookup"><span data-stu-id="29e26-198">Because split buttons always have a default action associated with the [**IInvokeProvider::Invoke**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iinvokeprovider-invoke) method, they must support the [Invoke](uiauto-implementinginvoke.md) control pattern.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="29e26-199">Eventos necessários</span><span class="sxs-lookup"><span data-stu-id="29e26-199">Required Events</span></span>

<span data-ttu-id="29e26-200">A tabela a seguir lista os eventos de automação da interface do usuário que são necessários para dar suporte aos controles de botão Split.</span><span class="sxs-lookup"><span data-stu-id="29e26-200">The following table lists the UI Automation events that split button controls are required to support.</span></span> <span data-ttu-id="29e26-201">Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="29e26-201">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="29e26-202">Evento de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="29e26-202">UI Automation Event</span></span>                                                                                                                                                | <span data-ttu-id="29e26-203">Observações</span><span class="sxs-lookup"><span data-stu-id="29e26-203">Notes</span></span>                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="29e26-204">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="29e26-204">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                                   |                                                                                                                            |
| <span data-ttu-id="29e26-205">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="29e26-205">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                              |                                                                                                                            |
| <span data-ttu-id="29e26-206">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ExpandCollapseExpandCollapseStatePropertyId.</span><span class="sxs-lookup"><span data-stu-id="29e26-206">[**UIA\_ExpandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> |                                                                                                                            |
| [<span data-ttu-id="29e26-207">**UIA \_ invocar \_ InvokedEventId**</span><span class="sxs-lookup"><span data-stu-id="29e26-207">**UIA\_Invoke\_InvokedEventId**</span></span>](uiauto-event-ids.md)                                                                                  |                                                                                                                            |
| <span data-ttu-id="29e26-208">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="29e26-208">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                              | <span data-ttu-id="29e26-209">Se o controle oferecer suporte à propriedade [**IsEnabled**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="29e26-209">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="29e26-210">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="29e26-210">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                          | <span data-ttu-id="29e26-211">Se o controle oferecer suporte à propriedade [**IsOffscreen**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="29e26-211">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="29e26-212">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="29e26-212">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                               |                                                                                                                            |



 

## <a name="splitbutton-control-type-example"></a><span data-ttu-id="29e26-213">Exemplo do tipo de controle SplitButton</span><span class="sxs-lookup"><span data-stu-id="29e26-213">SplitButton Control Type Example</span></span>

<span data-ttu-id="29e26-214">A imagem a seguir ilustra um controle que implementa o tipo de controle **SplitButton** .</span><span class="sxs-lookup"><span data-stu-id="29e26-214">The following image illustrates a control that implements the **SplitButton** control type.</span></span>

![captura de tela mostrando exemplo de um controle SplitButton](images/splitbuttonxmpl.jpg)



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="29e26-216">Árvore de automação da interface do usuário – exibição de controle</span><span class="sxs-lookup"><span data-stu-id="29e26-216">UI Automation Tree—Control View</span></span></th>
<th><span data-ttu-id="29e26-217">Árvore de automação da interface do usuário – exibição de conteúdo</span><span class="sxs-lookup"><span data-stu-id="29e26-217">UI Automation Tree—Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="29e26-218">&quot;Nome &quot; do SplitButton (invocar, ExpandCollapse)</span><span class="sxs-lookup"><span data-stu-id="29e26-218">SplitButton &quot;Name&quot; (Invoke, ExpandCollapse)</span></span>
<ul>
<li><span data-ttu-id="29e26-219">&quot;Opção de botão mais &quot; (Invoke)</span><span class="sxs-lookup"><span data-stu-id="29e26-219">Button &quot;More option&quot; (Invoke)</span></span>
<ul>
<li><span data-ttu-id="29e26-220">Menu</span><span class="sxs-lookup"><span data-stu-id="29e26-220">Menu</span></span>
<ul>
<li><span data-ttu-id="29e26-221">MenuItem</span><span class="sxs-lookup"><span data-stu-id="29e26-221">MenuItem</span></span></li>
<li><span data-ttu-id="29e26-222">...</span><span class="sxs-lookup"><span data-stu-id="29e26-222">...</span></span></li>
</ul></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="29e26-223">&quot;Nome &quot; do SplitButton (invocar, ExpandCollapse)</span><span class="sxs-lookup"><span data-stu-id="29e26-223">SplitButton &quot;Name&quot; (Invoke, ExpandCollapse)</span></span>
<ul>
<li><span data-ttu-id="29e26-224">&quot;Opção de botão mais &quot; (Invoke)</span><span class="sxs-lookup"><span data-stu-id="29e26-224">Button &quot;More option&quot; (Invoke)</span></span>
<ul>
<li><span data-ttu-id="29e26-225">Menu</span><span class="sxs-lookup"><span data-stu-id="29e26-225">Menu</span></span>
<ul>
<li><span data-ttu-id="29e26-226">MenuItem</span><span class="sxs-lookup"><span data-stu-id="29e26-226">MenuItem</span></span></li>
<li><span data-ttu-id="29e26-227">...</span><span class="sxs-lookup"><span data-stu-id="29e26-227">...</span></span></li>
</ul></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="29e26-228">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="29e26-228">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="29e26-229">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="29e26-229">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="29e26-230">Visão Geral dos Tipos de Controle de Automação de Interface do Usuário</span><span class="sxs-lookup"><span data-stu-id="29e26-230">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="29e26-231">Visão geral de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="29e26-231">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




