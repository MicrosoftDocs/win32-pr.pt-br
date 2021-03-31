---
title: Tipo de controle da guia
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle de guia.
ms.assetid: 49e3f025-f49b-44b1-90ca-09f40dce8f2a
keywords:
- Automação da interface do usuário, suporte para tipo de controle de guia
- Automação da interface do usuário, tipo de controle da guia
- Automação da interface do usuário, estrutura de árvore para tipo de controle de guia
- Automação da interface do usuário, propriedades para tipo de controle de guia
- Automação da interface do usuário, padrões de controle para tipo de controle de guia
- Automação da interface do usuário, eventos para tipo de controle de guia
- estruturas de árvore, tipo de controle de guia
- Propriedades, tipo de controle guia
- padrões de controle, tipo de controle de guia
- eventos, tipo de controle de guia
- suporte para tipo de controle de guia
- tipo de controle Guia
- tipos de controle, estrutura de árvore para tipo de controle de guia
- tipos de controle, padrões de controle para tipo de controle de guia
- tipos de controle, suporte para Tab
- tipos de controle, guia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 769a03617830c33fce4a8f64c594010b2120785b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916400"
---
# <a name="tab-control-type"></a><span data-ttu-id="74c5f-119">Tipo de controle da guia</span><span class="sxs-lookup"><span data-stu-id="74c5f-119">Tab Control Type</span></span>

<span data-ttu-id="74c5f-120">Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle de **guia** .</span><span class="sxs-lookup"><span data-stu-id="74c5f-120">This topic provides information about Microsoft UI Automation support for the **Tab** control type.</span></span>

<span data-ttu-id="74c5f-121">Um controle guia é análogo aos divisores em um bloco de anotações ou aos rótulos em um arquivo de gabinete.</span><span class="sxs-lookup"><span data-stu-id="74c5f-121">A tab control is analogous to the dividers in a notebook or the labels in a file cabinet.</span></span> <span data-ttu-id="74c5f-122">Usando um controle guia, um aplicativo pode definir várias páginas para a mesma área de uma janela ou caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="74c5f-122">By using a tab control, an application can define multiple pages for the same area of a window or dialog box.</span></span>

<span data-ttu-id="74c5f-123">As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle **guia** .</span><span class="sxs-lookup"><span data-stu-id="74c5f-123">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Tab** control type.</span></span> <span data-ttu-id="74c5f-124">Os requisitos de automação da interface do usuário se aplicam a todos os controles guia onde a estrutura/plataforma da interface do usuário integra o suporte à automação da interface do usuário para tipos de controle e padrões</span><span class="sxs-lookup"><span data-stu-id="74c5f-124">The UI Automation requirements apply to all tab controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="74c5f-125">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="74c5f-125">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="74c5f-126">Estrutura de árvore típica</span><span class="sxs-lookup"><span data-stu-id="74c5f-126">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="74c5f-127">Propriedades relevantes</span><span class="sxs-lookup"><span data-stu-id="74c5f-127">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="74c5f-128">Padrões de controle necessários</span><span class="sxs-lookup"><span data-stu-id="74c5f-128">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="74c5f-129">Eventos necessários</span><span class="sxs-lookup"><span data-stu-id="74c5f-129">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="74c5f-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="74c5f-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="74c5f-131">Estrutura de árvore típica</span><span class="sxs-lookup"><span data-stu-id="74c5f-131">Typical Tree Structure</span></span>

<span data-ttu-id="74c5f-132">A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence a controles de guia e descreve o que pode ser contido em cada exibição.</span><span class="sxs-lookup"><span data-stu-id="74c5f-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to tab controls and describes what can be contained in each view.</span></span> <span data-ttu-id="74c5f-133">Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="74c5f-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="74c5f-134">Exibição de controle</span><span class="sxs-lookup"><span data-stu-id="74c5f-134">Control View</span></span></th>
<th><span data-ttu-id="74c5f-135">Exibição de conteúdo</span><span class="sxs-lookup"><span data-stu-id="74c5f-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="74c5f-136">Tab</span><span class="sxs-lookup"><span data-stu-id="74c5f-136">Tab</span></span>
<ul>
<li><span data-ttu-id="74c5f-137">TabItem (1 ou mais)</span><span class="sxs-lookup"><span data-stu-id="74c5f-137">TabItem (1 or more)</span></span></li>
<li><span data-ttu-id="74c5f-138">Barra de rolagem (0 ou 1)</span><span class="sxs-lookup"><span data-stu-id="74c5f-138">ScrollBar (0 or 1)</span></span>
<ul>
<li><span data-ttu-id="74c5f-139">Botão (0 ou 2)</span><span class="sxs-lookup"><span data-stu-id="74c5f-139">Button (0 or 2)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="74c5f-140">Tab</span><span class="sxs-lookup"><span data-stu-id="74c5f-140">Tab</span></span>
<ul>
<li><span data-ttu-id="74c5f-141">TabItem (1 ou mais)</span><span class="sxs-lookup"><span data-stu-id="74c5f-141">TabItem (1 or more)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="74c5f-142">Os controles guia têm elementos de automação da interface do usuário filhos com base no tipo de controle [TabItem](uiauto-supporttabitemcontroltype.md) .</span><span class="sxs-lookup"><span data-stu-id="74c5f-142">Tab controls have child UI Automation elements based on the [TabItem](uiauto-supporttabitemcontroltype.md) control type.</span></span> <span data-ttu-id="74c5f-143">Quando os itens da guia são agrupados (por exemplo, como em aplicativos Microsoft Office), o tipo de controle **guia** também pode hospedar tipos de controle de **grupos** para os itens de guia agrupados, como mostra a seguinte estrutura de árvore.</span><span class="sxs-lookup"><span data-stu-id="74c5f-143">When tab items are grouped (for example, as in Microsoft Office applications) the **Tab** control type can also host **Groups** control types for the grouped tab items, as the following tree structure shows.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="74c5f-144">Exibição de controle</span><span class="sxs-lookup"><span data-stu-id="74c5f-144">Control View</span></span></th>
<th><span data-ttu-id="74c5f-145">Exibição de conteúdo</span><span class="sxs-lookup"><span data-stu-id="74c5f-145">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="74c5f-146">Tab</span><span class="sxs-lookup"><span data-stu-id="74c5f-146">Tab</span></span>
<ul>
<li><span data-ttu-id="74c5f-147">TabItem (1 ou mais)</span><span class="sxs-lookup"><span data-stu-id="74c5f-147">TabItem (1 or more)</span></span></li>
<li><span data-ttu-id="74c5f-148">Grupo (0 ou mais)</span><span class="sxs-lookup"><span data-stu-id="74c5f-148">Group (0 or more)</span></span>
<ul>
<li><span data-ttu-id="74c5f-149">TabItem (0 ou mais)</span><span class="sxs-lookup"><span data-stu-id="74c5f-149">TabItem (0 or more)</span></span></li>
</ul></li>
<li><span data-ttu-id="74c5f-150">Barra de rolagem (0 ou 1)</span><span class="sxs-lookup"><span data-stu-id="74c5f-150">ScrollBar (0 or 1)</span></span>
<ul>
<li><span data-ttu-id="74c5f-151">Botão (0 ou 2)</span><span class="sxs-lookup"><span data-stu-id="74c5f-151">Button (0 or 2)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="74c5f-152">Tab</span><span class="sxs-lookup"><span data-stu-id="74c5f-152">Tab</span></span>
<ul>
<li><span data-ttu-id="74c5f-153">TabItem (1 ou mais)</span><span class="sxs-lookup"><span data-stu-id="74c5f-153">TabItem (1 or more)</span></span></li>
<li><span data-ttu-id="74c5f-154">Grupo (0 ou mais)</span><span class="sxs-lookup"><span data-stu-id="74c5f-154">Group (0 or more)</span></span>
<ul>
<li><span data-ttu-id="74c5f-155">TabItem (0 ou mais)</span><span class="sxs-lookup"><span data-stu-id="74c5f-155">TabItem (0 or more)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="74c5f-156">Propriedades relevantes</span><span class="sxs-lookup"><span data-stu-id="74c5f-156">Relevant Properties</span></span>

<span data-ttu-id="74c5f-157">A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para controles de guia.</span><span class="sxs-lookup"><span data-stu-id="74c5f-157">The following table lists the UI Automation properties whose value or definition is especially relevant to tab controls.</span></span> <span data-ttu-id="74c5f-158">Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="74c5f-158">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="74c5f-159">Propriedade de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="74c5f-159">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="74c5f-160">Valor</span><span class="sxs-lookup"><span data-stu-id="74c5f-160">Value</span></span>      | <span data-ttu-id="74c5f-161">Observações</span><span class="sxs-lookup"><span data-stu-id="74c5f-161">Notes</span></span>                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="74c5f-162">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="74c5f-162">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="74c5f-163">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="74c5f-163">See notes.</span></span> | <span data-ttu-id="74c5f-164">O valor dessa propriedade deve ser exclusivo entre todos os elementos de mesmo nível na exibição bruta da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="74c5f-164">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="74c5f-165">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="74c5f-165">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="74c5f-166">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="74c5f-166">See notes.</span></span> | <span data-ttu-id="74c5f-167">O retângulo mais externo que contém o controle inteiro.</span><span class="sxs-lookup"><span data-stu-id="74c5f-167">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="74c5f-168">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="74c5f-168">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="74c5f-169">Não</span><span class="sxs-lookup"><span data-stu-id="74c5f-169">No</span></span>         | <span data-ttu-id="74c5f-170">O controle guia não tem pontos clicáveis.</span><span class="sxs-lookup"><span data-stu-id="74c5f-170">The tab control does not have clickable points.</span></span>                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="74c5f-171">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="74c5f-171">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="74c5f-172">**Tab**</span><span class="sxs-lookup"><span data-stu-id="74c5f-172">**Tab**</span></span>    |                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="74c5f-173">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="74c5f-173">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="74c5f-174">TRUE</span><span class="sxs-lookup"><span data-stu-id="74c5f-174">TRUE</span></span>       | <span data-ttu-id="74c5f-175">O controle guia é sempre incluído na exibição de conteúdo da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="74c5f-175">The tab control is always included in the content view of the UI Automation tree.</span></span>                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="74c5f-176">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="74c5f-176">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="74c5f-177">TRUE</span><span class="sxs-lookup"><span data-stu-id="74c5f-177">TRUE</span></span>       | <span data-ttu-id="74c5f-178">O controle guia é sempre incluído no modo de exibição de controle da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="74c5f-178">The tab control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="74c5f-179">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="74c5f-179">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="74c5f-180">TRUE</span><span class="sxs-lookup"><span data-stu-id="74c5f-180">TRUE</span></span>       | <span data-ttu-id="74c5f-181">O tipo de controle guia deve ser capaz de receber o foco do teclado.</span><span class="sxs-lookup"><span data-stu-id="74c5f-181">The Tab control type must be able to receive keyboard focus.</span></span> <span data-ttu-id="74c5f-182">Normalmente, um cliente de automação de interface do usuário chama [**IUIAutomationElement:: SetFocus**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-setfocus) em um controle guia e um de seus itens encaminhará o foco do teclado para o controle guia.</span><span class="sxs-lookup"><span data-stu-id="74c5f-182">Typically, a UI Automation client calls [**IUIAutomationElement::SetFocus**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-setfocus) on a tab control and one of its items will forward the keyboard focus to the tab control.</span></span> <span data-ttu-id="74c5f-183">É possível que alguns contêineres de guias tenham foco sem definir o foco para um de seus itens.</span><span class="sxs-lookup"><span data-stu-id="74c5f-183">It is possible for some tab containers to take focus without setting focus to one of its items.</span></span> |
| [<span data-ttu-id="74c5f-184">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="74c5f-184">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="74c5f-185">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="74c5f-185">See notes.</span></span> | <span data-ttu-id="74c5f-186">Controles de guia normalmente têm um rótulo de texto estático que é exposto por essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="74c5f-186">Tab controls typically have a static text label that is exposed through this property.</span></span>                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="74c5f-187">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="74c5f-187">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="74c5f-188">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="74c5f-188">See notes.</span></span> | <span data-ttu-id="74c5f-189">Cadeia de caracteres localizada correspondente ao tipo de controle de **guia** .</span><span class="sxs-lookup"><span data-stu-id="74c5f-189">Localized string corresponding to the **Tab** control type.</span></span> <span data-ttu-id="74c5f-190">O valor padrão é "Tab" para en-US ou inglês (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="74c5f-190">The default value is "tab" for en-US or English (United States).</span></span>                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="74c5f-191">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="74c5f-191">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="74c5f-192">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="74c5f-192">See notes.</span></span> | <span data-ttu-id="74c5f-193">O controle guia raramente requer uma propriedade **Name** .</span><span class="sxs-lookup"><span data-stu-id="74c5f-193">The tab control rarely requires a **Name** property.</span></span>                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="74c5f-194">**UIA \_ OrientationPropertyId**</span><span class="sxs-lookup"><span data-stu-id="74c5f-194">**UIA\_OrientationPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="74c5f-195">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="74c5f-195">See notes.</span></span> | <span data-ttu-id="74c5f-196">O controle guia sempre deve indicar se está posicionado horizontal ou verticalmente.</span><span class="sxs-lookup"><span data-stu-id="74c5f-196">The tab control must always indicate whether it is positioned horizontally or vertically.</span></span>                                                                                                                                                                                                                                                                                     |



 

## <a name="required-control-patterns"></a><span data-ttu-id="74c5f-197">Padrões de controle necessários</span><span class="sxs-lookup"><span data-stu-id="74c5f-197">Required Control Patterns</span></span>

<span data-ttu-id="74c5f-198">A tabela a seguir lista os padrões de controle de automação da interface do usuário que devem ter suporte em todos os controles guia.</span><span class="sxs-lookup"><span data-stu-id="74c5f-198">The following table lists the UI Automation control patterns required to be supported by all tab controls.</span></span> <span data-ttu-id="74c5f-199">Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="74c5f-199">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="74c5f-200">Propriedade padrão de controle/padrão</span><span class="sxs-lookup"><span data-stu-id="74c5f-200">Control Pattern/Pattern Property</span></span>                                             | <span data-ttu-id="74c5f-201">Suporte/valor</span><span class="sxs-lookup"><span data-stu-id="74c5f-201">Support/Value</span></span> | <span data-ttu-id="74c5f-202">Observações</span><span class="sxs-lookup"><span data-stu-id="74c5f-202">Notes</span></span>                                                                                                                                                                  |
|------------------------------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="74c5f-203">**ISelectionProvider**</span><span class="sxs-lookup"><span data-stu-id="74c5f-203">**ISelectionProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)                      | <span data-ttu-id="74c5f-204">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="74c5f-204">Required</span></span>      | <span data-ttu-id="74c5f-205">Todos os controles guia devem oferecer suporte ao padrão de controle [Selection](uiauto-implementingselection.md) .</span><span class="sxs-lookup"><span data-stu-id="74c5f-205">All tab controls must support the [Selection](uiauto-implementingselection.md) control pattern.</span></span>                                                                       |
| [<span data-ttu-id="74c5f-206">**IsSelectionRequired**</span><span class="sxs-lookup"><span data-stu-id="74c5f-206">**IsSelectionRequired**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired) | <span data-ttu-id="74c5f-207">TRUE</span><span class="sxs-lookup"><span data-stu-id="74c5f-207">TRUE</span></span>          | <span data-ttu-id="74c5f-208">Controles de guia sempre exigem que uma seleção seja feita.</span><span class="sxs-lookup"><span data-stu-id="74c5f-208">Tab controls always require that a selection be made.</span></span>                                                                                                                  |
| [<span data-ttu-id="74c5f-209">**CanSelectMultiple**</span><span class="sxs-lookup"><span data-stu-id="74c5f-209">**CanSelectMultiple**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple)     | <span data-ttu-id="74c5f-210">FALSE</span><span class="sxs-lookup"><span data-stu-id="74c5f-210">FALSE</span></span>         | <span data-ttu-id="74c5f-211">Os controles de guia são sempre contêineres de seleção única.</span><span class="sxs-lookup"><span data-stu-id="74c5f-211">Tab controls are always single-selection containers.</span></span>                                                                                                                   |
| [<span data-ttu-id="74c5f-212">**IScrollProvider**</span><span class="sxs-lookup"><span data-stu-id="74c5f-212">**IScrollProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)                            | <span data-ttu-id="74c5f-213">Depende</span><span class="sxs-lookup"><span data-stu-id="74c5f-213">Depends</span></span>       | <span data-ttu-id="74c5f-214">O padrão de controle [Scroll](uiauto-implementingscroll.md) deve ter suporte se o controle guia tiver widgets que permitem que um conjunto de itens de guia seja rolado.</span><span class="sxs-lookup"><span data-stu-id="74c5f-214">The [Scroll](uiauto-implementingscroll.md) control pattern must be supported if the tab control has widgets that allow for a set of tab items to be scrolled through.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="74c5f-215">Eventos necessários</span><span class="sxs-lookup"><span data-stu-id="74c5f-215">Required Events</span></span>

<span data-ttu-id="74c5f-216">A tabela a seguir lista os eventos de automação da interface do usuário aos quais os controles de guia são necessários para dar suporte.</span><span class="sxs-lookup"><span data-stu-id="74c5f-216">The following table lists the UI Automation events that tab controls are required to support.</span></span> <span data-ttu-id="74c5f-217">Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="74c5f-217">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="74c5f-218">Evento de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="74c5f-218">UI Automation Event</span></span>                                                                                                                                        | <span data-ttu-id="74c5f-219">Observações</span><span class="sxs-lookup"><span data-stu-id="74c5f-219">Notes</span></span>                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="74c5f-220">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="74c5f-220">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                           |                                                                                                                            |
| <span data-ttu-id="74c5f-221">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="74c5f-221">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                      |                                                                                                                            |
| <span data-ttu-id="74c5f-222">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="74c5f-222">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                      | <span data-ttu-id="74c5f-223">Se o controle oferecer suporte à propriedade [**IsEnabled**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="74c5f-223">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="74c5f-224">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="74c5f-224">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                  | <span data-ttu-id="74c5f-225">Se o controle oferecer suporte à propriedade [**IsOffscreen**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="74c5f-225">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| <span data-ttu-id="74c5f-226">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollHorizontallyScrollablePropertyId.</span><span class="sxs-lookup"><span data-stu-id="74c5f-226">[**UIA\_ScrollHorizontallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>   | <span data-ttu-id="74c5f-227">Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="74c5f-227">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="74c5f-228">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollHorizontalScrollPercentPropertyId.</span><span class="sxs-lookup"><span data-stu-id="74c5f-228">[**UIA\_ScrollHorizontalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="74c5f-229">Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="74c5f-229">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="74c5f-230">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollHorizontalViewSizePropertyId.</span><span class="sxs-lookup"><span data-stu-id="74c5f-230">[**UIA\_ScrollHorizontalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>           | <span data-ttu-id="74c5f-231">Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="74c5f-231">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="74c5f-232">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollVerticallyScrollablePropertyId.</span><span class="sxs-lookup"><span data-stu-id="74c5f-232">[**UIA\_ScrollVerticallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>       | <span data-ttu-id="74c5f-233">Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="74c5f-233">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="74c5f-234">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollVerticalScrollPercentPropertyId.</span><span class="sxs-lookup"><span data-stu-id="74c5f-234">[**UIA\_ScrollVerticalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>     | <span data-ttu-id="74c5f-235">Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="74c5f-235">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="74c5f-236">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollVerticalViewSizePropertyId.</span><span class="sxs-lookup"><span data-stu-id="74c5f-236">[**UIA\_ScrollVerticalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>               | <span data-ttu-id="74c5f-237">Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="74c5f-237">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| [<span data-ttu-id="74c5f-238">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="74c5f-238">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                       |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="74c5f-239">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="74c5f-239">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="74c5f-240">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="74c5f-240">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="74c5f-241">Visão Geral dos Tipos de Controle de Automação de Interface do Usuário</span><span class="sxs-lookup"><span data-stu-id="74c5f-241">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="74c5f-242">Visão geral de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="74c5f-242">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




