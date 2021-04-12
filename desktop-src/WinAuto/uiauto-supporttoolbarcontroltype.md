---
title: Tipo de controle ToolBar
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle ToolBar. Os controles da barra de ferramentas permitem que os usuários finais ativem comandos e ferramentas contidos em um aplicativo.
ms.assetid: e2a72ce3-5263-43f8-be4d-715a78224b68
keywords:
- Automação da interface do usuário, suporte para tipo de controle da barra de ferramentas
- Automação da interface do usuário, tipo de controle ToolBar
- Automação da interface do usuário, estrutura de árvore para tipo de controle ToolBar
- Automação da interface do usuário, propriedades para tipo de controle da barra de ferramentas
- Automação da interface do usuário, padrões de controle para tipo de controle ToolBar
- Automação da interface do usuário, eventos para tipo de controle da barra de ferramentas
- estruturas de árvore, tipo de controle da barra de ferramentas
- Propriedades, tipo de controle barra de ferramentas
- padrões de controle, tipo de controle da barra de ferramentas
- eventos, tipo de controle ToolBar
- suporte para tipo de controle ToolBar
- ToolBar (tipo de controle)
- tipos de controle, estrutura de árvore para tipo de controle da barra de ferramentas
- tipos de controle, padrões de controle para o tipo de controle barra de ferramentas
- tipos de controle, suporte para barra de ferramentas
- tipos de controle, barra de ferramentas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4327c187a86ace6f02b93082675c345eae4d4edf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364379"
---
# <a name="toolbar-control-type"></a><span data-ttu-id="c7156-120">Tipo de controle ToolBar</span><span class="sxs-lookup"><span data-stu-id="c7156-120">ToolBar Control Type</span></span>

<span data-ttu-id="c7156-121">Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle **Toolbar** .</span><span class="sxs-lookup"><span data-stu-id="c7156-121">This topic provides information about Microsoft UI Automation support for the **ToolBar** control type.</span></span> <span data-ttu-id="c7156-122">Os controles da barra de ferramentas permitem que os usuários finais ativem comandos e ferramentas contidos em um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c7156-122">Toolbar controls enable end users to activate commands and tools contained within a application.</span></span>

<span data-ttu-id="c7156-123">As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle **Toolbar** .</span><span class="sxs-lookup"><span data-stu-id="c7156-123">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **ToolBar** control type.</span></span> <span data-ttu-id="c7156-124">Os requisitos de automação da interface do usuário se aplicam a todos os controles da barra de ferramentas em que a estrutura/plataforma da interface do usuário integra o suporte à automação da interface do usuário para tipos</span><span class="sxs-lookup"><span data-stu-id="c7156-124">The UI Automation requirements apply to all toolbar controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="c7156-125">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="c7156-125">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="c7156-126">Estrutura de árvore típica</span><span class="sxs-lookup"><span data-stu-id="c7156-126">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="c7156-127">Propriedades relevantes</span><span class="sxs-lookup"><span data-stu-id="c7156-127">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="c7156-128">Padrões de controle necessários</span><span class="sxs-lookup"><span data-stu-id="c7156-128">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="c7156-129">Eventos necessários</span><span class="sxs-lookup"><span data-stu-id="c7156-129">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="c7156-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c7156-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="c7156-131">Estrutura de árvore típica</span><span class="sxs-lookup"><span data-stu-id="c7156-131">Typical Tree Structure</span></span>

<span data-ttu-id="c7156-132">A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence aos controles da barra de ferramentas e descreve o que pode ser contido em cada exibição.</span><span class="sxs-lookup"><span data-stu-id="c7156-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to toolbar controls and describes what can be contained in each view.</span></span> <span data-ttu-id="c7156-133">Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="c7156-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c7156-134">Exibição de controle</span><span class="sxs-lookup"><span data-stu-id="c7156-134">Control View</span></span></th>
<th><span data-ttu-id="c7156-135">Exibição de conteúdo</span><span class="sxs-lookup"><span data-stu-id="c7156-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="c7156-136">ToolBar</span><span class="sxs-lookup"><span data-stu-id="c7156-136">ToolBar</span></span>
<ul>
<li><span data-ttu-id="c7156-137">Vários controles (0 ou mais)</span><span class="sxs-lookup"><span data-stu-id="c7156-137">Various controls (0 or more)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="c7156-138">ToolBar</span><span class="sxs-lookup"><span data-stu-id="c7156-138">ToolBar</span></span>
<ul>
<li><span data-ttu-id="c7156-139">Vários controles (0 ou mais)</span><span class="sxs-lookup"><span data-stu-id="c7156-139">Various controls (0 or more)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="c7156-140">Um controle ToolBar pode conter qualquer tipo de controle dentro de sua subárvore.</span><span class="sxs-lookup"><span data-stu-id="c7156-140">A toolbar control can contain any type of control within its subtree.</span></span> <span data-ttu-id="c7156-141">Geralmente, eles contêm botões, caixas de combinação e botões de divisão.</span><span class="sxs-lookup"><span data-stu-id="c7156-141">They most often contain buttons, combo boxes, and split buttons.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="c7156-142">Propriedades relevantes</span><span class="sxs-lookup"><span data-stu-id="c7156-142">Relevant Properties</span></span>

<span data-ttu-id="c7156-143">A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para o tipo de controle **Toolbar** .</span><span class="sxs-lookup"><span data-stu-id="c7156-143">The following table lists the UI Automation properties whose value or definition is especially relevant to the **ToolBar** control type.</span></span> <span data-ttu-id="c7156-144">Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="c7156-144">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="c7156-145">Propriedade de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="c7156-145">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="c7156-146">Valor</span><span class="sxs-lookup"><span data-stu-id="c7156-146">Value</span></span>       | <span data-ttu-id="c7156-147">Observações</span><span class="sxs-lookup"><span data-stu-id="c7156-147">Notes</span></span>                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c7156-148">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="c7156-148">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="c7156-149">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="c7156-149">See notes.</span></span>  | <span data-ttu-id="c7156-150">O valor dessa propriedade deve ser exclusivo entre todos os elementos de mesmo nível na exibição bruta da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="c7156-150">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                               |
| [<span data-ttu-id="c7156-151">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="c7156-151">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="c7156-152">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="c7156-152">See notes.</span></span>  | <span data-ttu-id="c7156-153">O retângulo mais externo que contém o controle inteiro.</span><span class="sxs-lookup"><span data-stu-id="c7156-153">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                   |
| [<span data-ttu-id="c7156-154">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="c7156-154">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="c7156-155">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="c7156-155">See notes.</span></span>  | <span data-ttu-id="c7156-156">Com suporte se houver um retângulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="c7156-156">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="c7156-157">Se nem todos os pontos dentro do retângulo delimitador forem clicáveis, o elemento executará testes de clique especializados, substituirá e fornecerá um ponto clicável.</span><span class="sxs-lookup"><span data-stu-id="c7156-157">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span>       |
| [<span data-ttu-id="c7156-158">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="c7156-158">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="c7156-159">**Barra**</span><span class="sxs-lookup"><span data-stu-id="c7156-159">**ToolBar**</span></span> | <span data-ttu-id="c7156-160">Esse valor é o mesmo para todas as estruturas de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="c7156-160">This value is the same for all UI frameworks.</span></span>                                                                                                                                                              |
| [<span data-ttu-id="c7156-161">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="c7156-161">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="c7156-162">TRUE</span><span class="sxs-lookup"><span data-stu-id="c7156-162">TRUE</span></span>        | <span data-ttu-id="c7156-163">O controle Toolbar sempre é incluído na exibição de conteúdo da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="c7156-163">The toolbar control is always included in the content view of the UI Automation tree.</span></span>                                                                                                                      |
| [<span data-ttu-id="c7156-164">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="c7156-164">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="c7156-165">TRUE</span><span class="sxs-lookup"><span data-stu-id="c7156-165">TRUE</span></span>        | <span data-ttu-id="c7156-166">O controle Toolbar sempre é incluído na exibição de controle da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="c7156-166">The toolbar control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                      |
| [<span data-ttu-id="c7156-167">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="c7156-167">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="c7156-168">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="c7156-168">See notes.</span></span>  | <span data-ttu-id="c7156-169">Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="c7156-169">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                                  |
| [<span data-ttu-id="c7156-170">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="c7156-170">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="c7156-171">NULO</span><span class="sxs-lookup"><span data-stu-id="c7156-171">NULL</span></span>        | <span data-ttu-id="c7156-172">Um controle Toolbar nunca tem um rótulo.</span><span class="sxs-lookup"><span data-stu-id="c7156-172">A toolbar control never has a label.</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="c7156-173">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="c7156-173">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="c7156-174">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="c7156-174">See notes.</span></span>  | <span data-ttu-id="c7156-175">Cadeia de caracteres localizada correspondente ao tipo de controle **Toolbar** .</span><span class="sxs-lookup"><span data-stu-id="c7156-175">Localized string corresponding to the **ToolBar** control type.</span></span> <span data-ttu-id="c7156-176">O valor padrão é "barra de ferramentas" para en-US ou inglês (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="c7156-176">The default value is "tool bar" for en-US or English (United States).</span></span>                                                                      |
| [<span data-ttu-id="c7156-177">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="c7156-177">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="c7156-178">Depende</span><span class="sxs-lookup"><span data-stu-id="c7156-178">Depends</span></span>     | <span data-ttu-id="c7156-179">O controle Toolbar não precisa de um nome, a menos que mais de um seja usado em um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c7156-179">The toolbar control does not need a name unless more than one is used within an application.</span></span> <span data-ttu-id="c7156-180">Se mais de um estiver presente, cada um deve ter um nome diferenciado (por exemplo, "formatação" ou "estrutura de tópicos").</span><span class="sxs-lookup"><span data-stu-id="c7156-180">If more than one is present, each must have a distinguishing name (for example, "Formatting" or "Outlining").</span></span> |



 

## <a name="required-control-patterns"></a><span data-ttu-id="c7156-181">Padrões de controle necessários</span><span class="sxs-lookup"><span data-stu-id="c7156-181">Required Control Patterns</span></span>

<span data-ttu-id="c7156-182">A tabela a seguir lista os padrões de controle de automação da interface do usuário necessários para serem suportados pelos controles da barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="c7156-182">The following table lists the UI Automation control patterns required to be supported by toolbar controls.</span></span> <span data-ttu-id="c7156-183">Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="c7156-183">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="c7156-184">Padrão de controle</span><span class="sxs-lookup"><span data-stu-id="c7156-184">Control Pattern</span></span>                                                   | <span data-ttu-id="c7156-185">Suporte</span><span class="sxs-lookup"><span data-stu-id="c7156-185">Support</span></span> | <span data-ttu-id="c7156-186">Observações</span><span class="sxs-lookup"><span data-stu-id="c7156-186">Notes</span></span>                                                                                                                                                         |
|-------------------------------------------------------------------|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c7156-187">**IDockProvider**</span><span class="sxs-lookup"><span data-stu-id="c7156-187">**IDockProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)                     | <span data-ttu-id="c7156-188">Depende</span><span class="sxs-lookup"><span data-stu-id="c7156-188">Depends</span></span> | <span data-ttu-id="c7156-189">Se a barra de ferramentas puder ser encaixada em partes diferentes da tela, ela deverá dar suporte ao padrão de controle [Dock](uiauto-implementingdock.md) .</span><span class="sxs-lookup"><span data-stu-id="c7156-189">If the toolbar can be docked to different parts of the screen, it must support the [Dock](uiauto-implementingdock.md) control pattern.</span></span>                       |
| [<span data-ttu-id="c7156-190">**IExpandCollapseProvider**</span><span class="sxs-lookup"><span data-stu-id="c7156-190">**IExpandCollapseProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | <span data-ttu-id="c7156-191">Depende</span><span class="sxs-lookup"><span data-stu-id="c7156-191">Depends</span></span> | <span data-ttu-id="c7156-192">Se a barra de ferramentas puder ser expandida e recolhida para mostrar mais itens, ela deverá dar suporte ao padrão de controle [ExpandCollapse](uiauto-implementingexpandcollapse.md) .</span><span class="sxs-lookup"><span data-stu-id="c7156-192">If the toolbar can be expanded and collapsed to show more items, it must support the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern.</span></span> |
| [<span data-ttu-id="c7156-193">**ITransformProvider**</span><span class="sxs-lookup"><span data-stu-id="c7156-193">**ITransformProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider)           | <span data-ttu-id="c7156-194">Depende</span><span class="sxs-lookup"><span data-stu-id="c7156-194">Depends</span></span> | <span data-ttu-id="c7156-195">Se a barra de ferramentas puder ser redimensionada, girada ou movida, ela deverá oferecer suporte ao padrão de controle [Transform](uiauto-implementingtransform.md) .</span><span class="sxs-lookup"><span data-stu-id="c7156-195">If the toolbar can be resized, rotated, or moved, it must support the [Transform](uiauto-implementingtransform.md) control pattern.</span></span>                          |



 

## <a name="required-events"></a><span data-ttu-id="c7156-196">Eventos necessários</span><span class="sxs-lookup"><span data-stu-id="c7156-196">Required Events</span></span>

<span data-ttu-id="c7156-197">A tabela a seguir lista os eventos de automação da interface do usuário aos quais os controles da barra de ferramentas precisam dar suporte.</span><span class="sxs-lookup"><span data-stu-id="c7156-197">The following table lists the UI Automation events that toolbar controls are required to support.</span></span> <span data-ttu-id="c7156-198">Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="c7156-198">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="c7156-199">Evento de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="c7156-199">UI Automation Event</span></span>                                                                                                                                                | <span data-ttu-id="c7156-200">Observações</span><span class="sxs-lookup"><span data-stu-id="c7156-200">Notes</span></span>                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c7156-201">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="c7156-201">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| <span data-ttu-id="c7156-202">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="c7156-202">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                              |                                                                                                                                  |
| <span data-ttu-id="c7156-203">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ExpandCollapseExpandCollapseStatePropertyId.</span><span class="sxs-lookup"><span data-stu-id="c7156-203">[**UIA\_ExpandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="c7156-204">Se o controle der suporte ao padrão de controle [ExpandCollapse](uiauto-implementingexpandcollapse.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="c7156-204">If the control supports the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern, it must support this event.</span></span> |
| <span data-ttu-id="c7156-205">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="c7156-205">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                              | <span data-ttu-id="c7156-206">Se o controle oferecer suporte à propriedade [**IsEnabled**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="c7156-206">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>         |
| <span data-ttu-id="c7156-207">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="c7156-207">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                          | <span data-ttu-id="c7156-208">Se o controle oferecer suporte à propriedade [**IsOffscreen**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="c7156-208">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>       |
| [<span data-ttu-id="c7156-209">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="c7156-209">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                               |                                                                                                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="c7156-210">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c7156-210">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="c7156-211">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="c7156-211">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c7156-212">Visão Geral dos Tipos de Controle de Automação de Interface do Usuário</span><span class="sxs-lookup"><span data-stu-id="c7156-212">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="c7156-213">Visão geral de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="c7156-213">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




