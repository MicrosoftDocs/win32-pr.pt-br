---
title: Tipo de controle de painel
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle de painel.
ms.assetid: 2a5d69dc-6880-4610-b481-4371637472ed
keywords:
- Automação da interface do usuário, suporte para tipo de controle de painel
- Automação da interface do usuário, tipo de controle de painel
- Automação da interface do usuário, estrutura de árvore para tipo de controle de painel
- Automação da interface do usuário, propriedades para tipo de controle de painel
- Automação da interface do usuário, padrões de controle para tipo de controle de painel
- Automação da interface do usuário, eventos para tipo de controle de painel
- estruturas de árvore, tipo de controle de painel
- Propriedades, tipo de controle de painel
- padrões de controle, tipo de controle de painel
- eventos, tipo de controle de painel
- suporte para tipo de controle de painel
- tipo de controle Painel
- tipos de controle, estrutura de árvore para tipo de controle de painel
- tipos de controle, padrões de controle para tipo de controle de painel
- tipos de controle, suporte para o painel
- tipos de controle, painel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51b7f22e6fb302ebb160a174c27c61119b8f09fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104561934"
---
# <a name="pane-control-type"></a><span data-ttu-id="f2076-119">Tipo de controle de painel</span><span class="sxs-lookup"><span data-stu-id="f2076-119">Pane Control Type</span></span>

<span data-ttu-id="f2076-120">Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle de **painel** .</span><span class="sxs-lookup"><span data-stu-id="f2076-120">This topic provides information about Microsoft UI Automation support for the **Pane** control type.</span></span>

<span data-ttu-id="f2076-121">O tipo de controle de **painel** é para regiões potencialmente roláveis que têm conteúdo distinto.</span><span class="sxs-lookup"><span data-stu-id="f2076-121">The **Pane** control type is for potentially scrollable regions that have disparate content.</span></span> <span data-ttu-id="f2076-122">Ele é usado para representar um objeto em uma janela de quadro ou de documento.</span><span class="sxs-lookup"><span data-stu-id="f2076-122">It is used to represent an object within a frame or document window.</span></span> <span data-ttu-id="f2076-123">Os usuários podem navegar entre controles de painel e dentro do conteúdo do painel atual.</span><span class="sxs-lookup"><span data-stu-id="f2076-123">Users can navigate between pane controls and within the contents of the current pane.</span></span> <span data-ttu-id="f2076-124">Os controles de painel representam um nível de agrupamento menor que o Windows ou documentos, mas acima dos controles individuais.</span><span class="sxs-lookup"><span data-stu-id="f2076-124">Pane controls represent a level of grouping lower than windows or documents, but above individual controls.</span></span> <span data-ttu-id="f2076-125">O usuário navega entre os painéis pressionando TAB, F6 ou CTRL + TAB, dependendo do contexto.</span><span class="sxs-lookup"><span data-stu-id="f2076-125">The user navigates between panes by pressing TAB, F6, or CTRL+TAB, depending on the context.</span></span>

<span data-ttu-id="f2076-126">As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle de **painel** .</span><span class="sxs-lookup"><span data-stu-id="f2076-126">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Pane** control type.</span></span> <span data-ttu-id="f2076-127">Os requisitos de automação da interface do usuário se aplicam a todos os controles de painel em que a estrutura/plataforma da interface do usuário integra o suporte à automação da interface do usuário para tipos de controle</span><span class="sxs-lookup"><span data-stu-id="f2076-127">The UI Automation requirements apply to all pane controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="f2076-128">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="f2076-128">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="f2076-129">Estrutura de árvore típica</span><span class="sxs-lookup"><span data-stu-id="f2076-129">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="f2076-130">Propriedades relevantes</span><span class="sxs-lookup"><span data-stu-id="f2076-130">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="f2076-131">Padrões de controle necessários</span><span class="sxs-lookup"><span data-stu-id="f2076-131">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="f2076-132">Eventos necessários</span><span class="sxs-lookup"><span data-stu-id="f2076-132">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="f2076-133">Exemplo de tipo de controle de painel</span><span class="sxs-lookup"><span data-stu-id="f2076-133">Pane Control Type Example</span></span>](#pane-control-type-example)
-   [<span data-ttu-id="f2076-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f2076-134">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="f2076-135">Estrutura de árvore típica</span><span class="sxs-lookup"><span data-stu-id="f2076-135">Typical Tree Structure</span></span>

<span data-ttu-id="f2076-136">A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence a controles de painel e descreve o que pode ser contido em cada exibição.</span><span class="sxs-lookup"><span data-stu-id="f2076-136">The following table depicts a typical control and content view of the UI Automation tree that pertains to pane controls and describes what can be contained in each view.</span></span> <span data-ttu-id="f2076-137">Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="f2076-137">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f2076-138">Exibição de controle</span><span class="sxs-lookup"><span data-stu-id="f2076-138">Control View</span></span></th>
<th><span data-ttu-id="f2076-139">Exibição de conteúdo</span><span class="sxs-lookup"><span data-stu-id="f2076-139">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="f2076-140">Painel</span><span class="sxs-lookup"><span data-stu-id="f2076-140">Pane</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="f2076-141">Painel</span><span class="sxs-lookup"><span data-stu-id="f2076-141">Pane</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="f2076-142">Um controle de painel sempre aparece nas exibições de controle e conteúdo.</span><span class="sxs-lookup"><span data-stu-id="f2076-142">A pane control always appears in the control and content views.</span></span> <span data-ttu-id="f2076-143">Não expor um objeto de layout como um painel no controle ou no modo de exibição de conteúdo se o objeto for usado somente para apresentação visual.</span><span class="sxs-lookup"><span data-stu-id="f2076-143">Do not expose a layout object as a pane in either the control or content view if the object is used only for visual presentation.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="f2076-144">Propriedades relevantes</span><span class="sxs-lookup"><span data-stu-id="f2076-144">Relevant Properties</span></span>

<span data-ttu-id="f2076-145">A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para controles de painel.</span><span class="sxs-lookup"><span data-stu-id="f2076-145">The following table lists the UI Automation properties whose value or definition is especially relevant to pane controls.</span></span> <span data-ttu-id="f2076-146">Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="f2076-146">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="f2076-147">Propriedade de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="f2076-147">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="f2076-148">Valor</span><span class="sxs-lookup"><span data-stu-id="f2076-148">Value</span></span>      | <span data-ttu-id="f2076-149">Observações</span><span class="sxs-lookup"><span data-stu-id="f2076-149">Notes</span></span>                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f2076-150">**UIA \_ AccessKeyPropertyId**</span><span class="sxs-lookup"><span data-stu-id="f2076-150">**UIA\_AccessKeyPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="f2076-151">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="f2076-151">See notes.</span></span> | <span data-ttu-id="f2076-152">Se uma combinação de teclas específica fornecer foco ao painel, essas informações deverão ser expostas por essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="f2076-152">If a specific key combination gives focus to the pane, that information should be exposed through this property.</span></span>                                                                                                                                                                                                      |
| [<span data-ttu-id="f2076-153">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="f2076-153">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="f2076-154">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="f2076-154">See notes.</span></span> | <span data-ttu-id="f2076-155">O valor dessa propriedade deve ser exclusivo entre todos os elementos de mesmo nível na exibição bruta da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="f2076-155">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                                                                                                          |
| [<span data-ttu-id="f2076-156">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="f2076-156">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="f2076-157">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="f2076-157">See notes.</span></span> | <span data-ttu-id="f2076-158">O retângulo mais externo que contém o controle inteiro.</span><span class="sxs-lookup"><span data-stu-id="f2076-158">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="f2076-159">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="f2076-159">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="f2076-160">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="f2076-160">See notes.</span></span> | <span data-ttu-id="f2076-161">Essa propriedade expõe um ponto clicável do controle de painel que faz com que o painel se concentre quando é clicado.</span><span class="sxs-lookup"><span data-stu-id="f2076-161">This property exposes a clickable point of the pane control that causes the pane to become focused when it is clicked.</span></span>                                                                                                                                                                                                |
| [<span data-ttu-id="f2076-162">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="f2076-162">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="f2076-163">**Painel**</span><span class="sxs-lookup"><span data-stu-id="f2076-163">**Pane**</span></span>   |                                                                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="f2076-164">**UIA \_ HelpTextPropertyId**</span><span class="sxs-lookup"><span data-stu-id="f2076-164">**UIA\_HelpTextPropertyId**</span></span>](uiauto-automation-element-propids.md)                         | <span data-ttu-id="f2076-165">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="f2076-165">See notes.</span></span> | <span data-ttu-id="f2076-166">O texto de ajuda para controles de painel deve explicar a finalidade do quadro e como ele se relaciona com outros quadros.</span><span class="sxs-lookup"><span data-stu-id="f2076-166">The help text for pane controls should explain the purpose of the frame and how it relates to other frames.</span></span> <span data-ttu-id="f2076-167">Uma descrição será necessária se a finalidade e a relação dos quadros não estiverem claras do valor da propriedade [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md) .</span><span class="sxs-lookup"><span data-stu-id="f2076-167">A description is necessary if the purpose and relationship of the frames is not clear from the value of the [**UIA\_NamePropertyId**](uiauto-automation-element-propids.md) property.</span></span> |
| [<span data-ttu-id="f2076-168">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="f2076-168">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="f2076-169">TRUE</span><span class="sxs-lookup"><span data-stu-id="f2076-169">TRUE</span></span>       | <span data-ttu-id="f2076-170">O controle de painel é sempre incluído na exibição de conteúdo da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="f2076-170">The pane control is always included in the content view of the UI Automation tree.</span></span>                                                                                                                                                                                                                                    |
| [<span data-ttu-id="f2076-171">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="f2076-171">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="f2076-172">TRUE</span><span class="sxs-lookup"><span data-stu-id="f2076-172">TRUE</span></span>       | <span data-ttu-id="f2076-173">O controle de painel é sempre incluído no modo de exibição de controle da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="f2076-173">The pane control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                                                                                                                                    |
| [<span data-ttu-id="f2076-174">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="f2076-174">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="f2076-175">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="f2076-175">See notes.</span></span> | <span data-ttu-id="f2076-176">Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="f2076-176">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                                                                                                                                             |
| [<span data-ttu-id="f2076-177">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="f2076-177">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="f2076-178">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="f2076-178">See notes.</span></span> | <span data-ttu-id="f2076-179">Controles de painel normalmente não têm um rótulo estático.</span><span class="sxs-lookup"><span data-stu-id="f2076-179">Pane controls typically do not have a static label.</span></span> <span data-ttu-id="f2076-180">Se houver um rótulo de texto estático, ele deverá ser exposto por meio dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="f2076-180">If there is a static text label, it should be exposed through this property.</span></span>                                                                                                                                                                                      |
| [<span data-ttu-id="f2076-181">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="f2076-181">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="f2076-182">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="f2076-182">See notes.</span></span> | <span data-ttu-id="f2076-183">Cadeia de caracteres localizada correspondente ao tipo de controle de **painel** .</span><span class="sxs-lookup"><span data-stu-id="f2076-183">Localized string corresponding to the **Pane** control type.</span></span> <span data-ttu-id="f2076-184">O valor padrão é "painel" para en-US ou inglês (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="f2076-184">The default value is "pane" for en-US or English (United States).</span></span>                                                                                                                                                                                        |
| [<span data-ttu-id="f2076-185">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="f2076-185">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="f2076-186">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="f2076-186">See notes.</span></span> | <span data-ttu-id="f2076-187">O valor dessa propriedade sempre deve ser um título claro, conciso e significativo.</span><span class="sxs-lookup"><span data-stu-id="f2076-187">The value for this property must always be a clear, concise and meaningful title.</span></span>                                                                                                                                                                                                                                     |



 

## <a name="required-control-patterns"></a><span data-ttu-id="f2076-188">Padrões de controle necessários</span><span class="sxs-lookup"><span data-stu-id="f2076-188">Required Control Patterns</span></span>

<span data-ttu-id="f2076-189">A tabela a seguir lista os padrões de controle de automação da interface do usuário necessários para serem suportados por controles de painel.</span><span class="sxs-lookup"><span data-stu-id="f2076-189">The following table lists the UI Automation control patterns required to be supported by pane controls.</span></span> <span data-ttu-id="f2076-190">Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="f2076-190">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="f2076-191">Padrão de controle</span><span class="sxs-lookup"><span data-stu-id="f2076-191">Control Pattern</span></span>                                         | <span data-ttu-id="f2076-192">Suporte</span><span class="sxs-lookup"><span data-stu-id="f2076-192">Support</span></span> | <span data-ttu-id="f2076-193">Observações</span><span class="sxs-lookup"><span data-stu-id="f2076-193">Notes</span></span>                                                                                                                                                                                         |
|---------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f2076-194">**IDockProvider**</span><span class="sxs-lookup"><span data-stu-id="f2076-194">**IDockProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)           | <span data-ttu-id="f2076-195">Depende</span><span class="sxs-lookup"><span data-stu-id="f2076-195">Depends</span></span> | <span data-ttu-id="f2076-196">Implemente o padrão de controle [Dock](uiauto-implementingdock.md) se o controle de painel puder ser encaixado.</span><span class="sxs-lookup"><span data-stu-id="f2076-196">Implement the [Dock](uiauto-implementingdock.md) control pattern if the pane control can be docked.</span></span>                                                                                          |
| [<span data-ttu-id="f2076-197">**IScrollProvider**</span><span class="sxs-lookup"><span data-stu-id="f2076-197">**IScrollProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)       | <span data-ttu-id="f2076-198">Depende</span><span class="sxs-lookup"><span data-stu-id="f2076-198">Depends</span></span> | <span data-ttu-id="f2076-199">Implemente o padrão de controle [Scroll](uiauto-implementingscroll.md) se o controle de painel puder ser rolado.</span><span class="sxs-lookup"><span data-stu-id="f2076-199">Implement the [Scroll](uiauto-implementingscroll.md) control pattern if the pane control can be scrolled.</span></span>                                                                                    |
| [<span data-ttu-id="f2076-200">**ITransformProvider**</span><span class="sxs-lookup"><span data-stu-id="f2076-200">**ITransformProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | <span data-ttu-id="f2076-201">Depende</span><span class="sxs-lookup"><span data-stu-id="f2076-201">Depends</span></span> | <span data-ttu-id="f2076-202">Implemente o padrão de controle [Transform](uiauto-implementingtransform.md) se o controle de painel puder ser movido, redimensionado ou girado na tela.</span><span class="sxs-lookup"><span data-stu-id="f2076-202">Implement the [Transform](uiauto-implementingtransform.md) control pattern if the pane control can be moved, resized, or rotated on the screen.</span></span>                                              |
| [<span data-ttu-id="f2076-203">**IWindowProvider**</span><span class="sxs-lookup"><span data-stu-id="f2076-203">**IWindowProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider)       | <span data-ttu-id="f2076-204">Nunca</span><span class="sxs-lookup"><span data-stu-id="f2076-204">Never</span></span>   | <span data-ttu-id="f2076-205">Se o elemento precisar implementar o padrão de controle [Window](uiauto-implementingwindow.md) , o controle deverá ser baseado no tipo de controle [Window](uiauto-supportwindowcontroltype.md) .</span><span class="sxs-lookup"><span data-stu-id="f2076-205">If the element needs to implement the [Window](uiauto-implementingwindow.md) control pattern, the control should be based on the [Window](uiauto-supportwindowcontroltype.md) control type.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="f2076-206">Eventos necessários</span><span class="sxs-lookup"><span data-stu-id="f2076-206">Required Events</span></span>

<span data-ttu-id="f2076-207">A tabela a seguir lista os eventos de automação da interface do usuário aos quais os controles do painel são necessários para dar suporte.</span><span class="sxs-lookup"><span data-stu-id="f2076-207">The following table lists the UI Automation events that pane controls are required to support.</span></span> <span data-ttu-id="f2076-208">Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="f2076-208">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="f2076-209">Evento de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="f2076-209">UI Automation Event</span></span>                                                                                                                                        | <span data-ttu-id="f2076-210">Observações</span><span class="sxs-lookup"><span data-stu-id="f2076-210">Notes</span></span>                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f2076-211">**UIA \_ AsyncContentLoadedEventId**</span><span class="sxs-lookup"><span data-stu-id="f2076-211">**UIA\_AsyncContentLoadedEventId**</span></span>](uiauto-event-ids.md)                                                                   |                                                                                                                            |
| [<span data-ttu-id="f2076-212">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="f2076-212">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                           |                                                                                                                            |
| <span data-ttu-id="f2076-213">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="f2076-213">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                      |                                                                                                                            |
| <span data-ttu-id="f2076-214">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="f2076-214">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                  | <span data-ttu-id="f2076-215">Se o controle oferecer suporte à propriedade [**IsOffscreen**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="f2076-215">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| <span data-ttu-id="f2076-216">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollHorizontallyScrollablePropertyId.</span><span class="sxs-lookup"><span data-stu-id="f2076-216">[**UIA\_ScrollHorizontallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>   | <span data-ttu-id="f2076-217">Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="f2076-217">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="f2076-218">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollHorizontalScrollPercentPropertyId.</span><span class="sxs-lookup"><span data-stu-id="f2076-218">[**UIA\_ScrollHorizontalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="f2076-219">Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="f2076-219">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="f2076-220">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollHorizontalViewSizePropertyId.</span><span class="sxs-lookup"><span data-stu-id="f2076-220">[**UIA\_ScrollHorizontalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>           | <span data-ttu-id="f2076-221">Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="f2076-221">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="f2076-222">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollVerticallyScrollablePropertyId.</span><span class="sxs-lookup"><span data-stu-id="f2076-222">[**UIA\_ScrollVerticallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>       | <span data-ttu-id="f2076-223">Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="f2076-223">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="f2076-224">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollVerticalScrollPercentPropertyId.</span><span class="sxs-lookup"><span data-stu-id="f2076-224">[**UIA\_ScrollVerticalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>     | <span data-ttu-id="f2076-225">Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="f2076-225">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="f2076-226">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollVerticalViewSizePropertyId.</span><span class="sxs-lookup"><span data-stu-id="f2076-226">[**UIA\_ScrollVerticalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>               | <span data-ttu-id="f2076-227">Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="f2076-227">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| [<span data-ttu-id="f2076-228">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="f2076-228">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                       |                                                                                                                            |



 

## <a name="pane-control-type-example"></a><span data-ttu-id="f2076-229">Exemplo de tipo de controle de painel</span><span class="sxs-lookup"><span data-stu-id="f2076-229">Pane Control Type Example</span></span>

<span data-ttu-id="f2076-230">A imagem a seguir ilustra um controle que implementa o tipo de controle de **painel** .</span><span class="sxs-lookup"><span data-stu-id="f2076-230">The following image illustrates a control that implements the **Pane** control type.</span></span>

![captura de tela mostrando exemplo de um controle de painel](images/panexmpl.jpg)



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f2076-232">Árvore de automação da interface do usuário – exibição de controle</span><span class="sxs-lookup"><span data-stu-id="f2076-232">UI Automation Tree—Control View</span></span></th>
<th><span data-ttu-id="f2076-233">Árvore de automação da interface do usuário – exibição de conteúdo</span><span class="sxs-lookup"><span data-stu-id="f2076-233">UI Automation Tree—Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="f2076-234">Painel</span><span class="sxs-lookup"><span data-stu-id="f2076-234">Pane</span></span>
<ul>
<li><span data-ttu-id="f2076-235">Tree (padrão de rolagem)</span><span class="sxs-lookup"><span data-stu-id="f2076-235">Tree (Scroll Pattern)</span></span>
<ul>
<li><span data-ttu-id="f2076-236">TreeItem</span><span class="sxs-lookup"><span data-stu-id="f2076-236">TreeItem</span></span></li>
<li><span data-ttu-id="f2076-237">...</span><span class="sxs-lookup"><span data-stu-id="f2076-237">...</span></span></li>
</ul></li>
</ul></li>
<li><span data-ttu-id="f2076-238">Painel</span><span class="sxs-lookup"><span data-stu-id="f2076-238">Pane</span></span>
<ul>
<li><span data-ttu-id="f2076-239">Editar (padrão de rolagem)</span><span class="sxs-lookup"><span data-stu-id="f2076-239">Edit (Scroll Pattern)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="f2076-240">Painel</span><span class="sxs-lookup"><span data-stu-id="f2076-240">Pane</span></span>
<ul>
<li><span data-ttu-id="f2076-241">Tree (padrão de rolagem)</span><span class="sxs-lookup"><span data-stu-id="f2076-241">Tree (Scroll Pattern)</span></span>
<ul>
<li><span data-ttu-id="f2076-242">TreeItem</span><span class="sxs-lookup"><span data-stu-id="f2076-242">TreeItem</span></span></li>
<li><span data-ttu-id="f2076-243">...</span><span class="sxs-lookup"><span data-stu-id="f2076-243">...</span></span></li>
</ul></li>
<li><span data-ttu-id="f2076-244">Painel</span><span class="sxs-lookup"><span data-stu-id="f2076-244">Pane</span></span>
<ul>
<li><span data-ttu-id="f2076-245">Editar (padrão de rolagem)</span><span class="sxs-lookup"><span data-stu-id="f2076-245">Edit (Scroll Pattern)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="f2076-246">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f2076-246">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="f2076-247">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="f2076-247">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f2076-248">Visão Geral dos Tipos de Controle de Automação de Interface do Usuário</span><span class="sxs-lookup"><span data-stu-id="f2076-248">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="f2076-249">Visão geral de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="f2076-249">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




