---
title: Tipo de controle de tabela
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle de tabela.
ms.assetid: 508db2af-1ca3-4003-8e1f-6e225cf79b7a
keywords:
- Automação da interface do usuário, suporte para tipo de controle de tabela
- Automação da interface do usuário, tipo de controle de tabela
- Automação da interface do usuário, estrutura de árvore para tipo de controle de tabela
- Automação da interface do usuário, propriedades para tipo de controle de tabela
- Automação da interface do usuário, padrões de controle para tipo de controle de tabela
- Automação da interface do usuário, eventos para tipo de controle de tabela
- estruturas de árvore, tipo de controle de tabela
- Propriedades, tipo de controle de tabela
- padrões de controle, tipo de controle de tabela
- eventos, tipo de controle de tabela
- suporte para tipo de controle de tabela
- tipo de controle Tabela
- tipos de controle, estrutura de árvore para tipo de controle de tabela
- tipos de controle, padrões de controle para tipo de controle de tabela
- tipos de controle, suporte para tabela
- tipos de controle, tabela
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb4ee709bd16156a62882aeee014b4744dab2214
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498756"
---
# <a name="table-control-type"></a><span data-ttu-id="82e71-119">Tipo de controle de tabela</span><span class="sxs-lookup"><span data-stu-id="82e71-119">Table Control Type</span></span>

<span data-ttu-id="82e71-120">Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle de **tabela** .</span><span class="sxs-lookup"><span data-stu-id="82e71-120">This topic provides information about Microsoft UI Automation support for the **Table** control type.</span></span>

<span data-ttu-id="82e71-121">Os controles de tabela contêm linhas e colunas de texto e, opcionalmente, cabeçalhos de linha e cabeçalhos de coluna.</span><span class="sxs-lookup"><span data-stu-id="82e71-121">Table controls contain rows and columns of text and, optionally, row headers and column headers.</span></span>

<span data-ttu-id="82e71-122">As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle **Table** .</span><span class="sxs-lookup"><span data-stu-id="82e71-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Table** control type.</span></span> <span data-ttu-id="82e71-123">Os requisitos de automação da interface do usuário se aplicam a todos os controles de tabela em que a estrutura/plataforma da interface do usuário integra o suporte à automação da interface do usuário para tipos de controle</span><span class="sxs-lookup"><span data-stu-id="82e71-123">The UI Automation requirements apply to all table controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="82e71-124">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="82e71-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="82e71-125">Estrutura de árvore típica</span><span class="sxs-lookup"><span data-stu-id="82e71-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="82e71-126">Propriedades relevantes</span><span class="sxs-lookup"><span data-stu-id="82e71-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="82e71-127">Padrões de controle necessários</span><span class="sxs-lookup"><span data-stu-id="82e71-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="82e71-128">Eventos necessários</span><span class="sxs-lookup"><span data-stu-id="82e71-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="82e71-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="82e71-129">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="82e71-130">Estrutura de árvore típica</span><span class="sxs-lookup"><span data-stu-id="82e71-130">Typical Tree Structure</span></span>

<span data-ttu-id="82e71-131">A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence a controles de tabela e descreve o que pode ser contido em cada exibição.</span><span class="sxs-lookup"><span data-stu-id="82e71-131">The following table depicts a typical control and content view of the UI Automation tree that pertains to table controls and describes what can be contained in each view.</span></span> <span data-ttu-id="82e71-132">Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="82e71-132">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="82e71-133">Exibição de controle</span><span class="sxs-lookup"><span data-stu-id="82e71-133">Control View</span></span></th>
<th><span data-ttu-id="82e71-134">Exibição de conteúdo</span><span class="sxs-lookup"><span data-stu-id="82e71-134">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="82e71-135">Tabela</span><span class="sxs-lookup"><span data-stu-id="82e71-135">Table</span></span>
<ul>
<li><span data-ttu-id="82e71-136">Texto (0 ou 1)</span><span class="sxs-lookup"><span data-stu-id="82e71-136">Text (0 or 1)</span></span></li>
<li><span data-ttu-id="82e71-137">Cabeçalho (0 ou mais)</span><span class="sxs-lookup"><span data-stu-id="82e71-137">Header (0 or more)</span></span></li>
<li><span data-ttu-id="82e71-138">Vários controles (0 ou mais)</span><span class="sxs-lookup"><span data-stu-id="82e71-138">Various controls (0 or more)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="82e71-139">Tabela</span><span class="sxs-lookup"><span data-stu-id="82e71-139">Table</span></span>
<ul>
<li><span data-ttu-id="82e71-140">Texto (1 ou mais)</span><span class="sxs-lookup"><span data-stu-id="82e71-140">Text (1 or more)</span></span></li>
<li><span data-ttu-id="82e71-141">Vários controles (0 ou mais)</span><span class="sxs-lookup"><span data-stu-id="82e71-141">Various controls (0 or more)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="82e71-142">Se um controle de tabela tiver cabeçalhos de linha ou coluna, eles deverão ser expostos no modo de exibição de controle da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="82e71-142">If a table control has row or column headers, they must be exposed in the control view of the UI Automation tree.</span></span> <span data-ttu-id="82e71-143">A exibição de conteúdo não precisa expor essas informações porque ela pode ser acessada usando [**IUIAutomationTablePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtablepattern).</span><span class="sxs-lookup"><span data-stu-id="82e71-143">The content view does not need to expose this information because it can be accessed using [**IUIAutomationTablePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtablepattern).</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="82e71-144">Propriedades relevantes</span><span class="sxs-lookup"><span data-stu-id="82e71-144">Relevant Properties</span></span>

<span data-ttu-id="82e71-145">A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para os controles de tabela.</span><span class="sxs-lookup"><span data-stu-id="82e71-145">The following table lists the UI Automation properties whose value or definition is especially relevant to table controls.</span></span> <span data-ttu-id="82e71-146">Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="82e71-146">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="82e71-147">Propriedade de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="82e71-147">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="82e71-148">Valor</span><span class="sxs-lookup"><span data-stu-id="82e71-148">Value</span></span>      | <span data-ttu-id="82e71-149">Observações</span><span class="sxs-lookup"><span data-stu-id="82e71-149">Notes</span></span>                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="82e71-150">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="82e71-150">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="82e71-151">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="82e71-151">See notes.</span></span> | <span data-ttu-id="82e71-152">O valor dessa propriedade deve ser exclusivo entre todos os elementos de mesmo nível na exibição bruta da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="82e71-152">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                      |
| [<span data-ttu-id="82e71-153">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="82e71-153">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="82e71-154">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="82e71-154">See notes.</span></span> | <span data-ttu-id="82e71-155">O retângulo mais externo que contém o controle inteiro.</span><span class="sxs-lookup"><span data-stu-id="82e71-155">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                          |
| [<span data-ttu-id="82e71-156">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="82e71-156">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="82e71-157">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="82e71-157">See notes.</span></span> | <span data-ttu-id="82e71-158">Com suporte se houver um retângulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="82e71-158">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="82e71-159">Se nem todos os pontos dentro do retângulo delimitador forem clicáveis, o elemento executará testes de clique especializados, substituirá e fornecerá um ponto clicável.</span><span class="sxs-lookup"><span data-stu-id="82e71-159">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span>                              |
| [<span data-ttu-id="82e71-160">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="82e71-160">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="82e71-161">**Table**</span><span class="sxs-lookup"><span data-stu-id="82e71-161">**Table**</span></span>  |                                                                                                                                                                                                                                   |
| [<span data-ttu-id="82e71-162">**UIA \_ DescribedByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="82e71-162">**UIA\_DescribedByPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="82e71-163">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="82e71-163">See notes.</span></span> | <span data-ttu-id="82e71-164">Se a tabela for anotada por outro elemento de interface do usuário (por exemplo, um elemento de texto que contém a descrição da tabela), a propriedade DescribedBy deverá expor uma referência ao elemento Automation do controle de texto.</span><span class="sxs-lookup"><span data-stu-id="82e71-164">If the table is annotated by other UI element (for example, a text element that holds the description for the table), the DescribedBy property should expose a reference to the automation element of the text control.</span></span>           |
| [<span data-ttu-id="82e71-165">**UIA \_ HelpTextPropertyId**</span><span class="sxs-lookup"><span data-stu-id="82e71-165">**UIA\_HelpTextPropertyId**</span></span>](uiauto-automation-element-propids.md)                         | <span data-ttu-id="82e71-166">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="82e71-166">See notes.</span></span> | <span data-ttu-id="82e71-167">Mais detalhes sobre a finalidade da tabela devem ser expostos por meio dessa propriedade se não for suficientemente explicado pela propriedade [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md) .</span><span class="sxs-lookup"><span data-stu-id="82e71-167">More details about the purpose of the table should be exposed through this property if it is not sufficiently explained by the [**UIA\_NamePropertyId**](uiauto-automation-element-propids.md) property.</span></span>      |
| [<span data-ttu-id="82e71-168">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="82e71-168">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="82e71-169">TRUE</span><span class="sxs-lookup"><span data-stu-id="82e71-169">TRUE</span></span>       | <span data-ttu-id="82e71-170">O controle tabela sempre deve aparecer na exibição de conteúdo da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="82e71-170">The table control must always appear in the content view of the UI Automation tree.</span></span>                                                                                                                                               |
| [<span data-ttu-id="82e71-171">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="82e71-171">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="82e71-172">TRUE</span><span class="sxs-lookup"><span data-stu-id="82e71-172">TRUE</span></span>       | <span data-ttu-id="82e71-173">O controle tabela sempre deve aparecer na exibição de controle da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="82e71-173">The table control must always appear in the control view of the UI Automation tree.</span></span>                                                                                                                                               |
| [<span data-ttu-id="82e71-174">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="82e71-174">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="82e71-175">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="82e71-175">See notes.</span></span> | <span data-ttu-id="82e71-176">Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="82e71-176">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                                                         |
| [<span data-ttu-id="82e71-177">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="82e71-177">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="82e71-178">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="82e71-178">See notes.</span></span> | <span data-ttu-id="82e71-179">Se houver um rótulo de texto estático, essa propriedade deverá expor uma referência ao elemento Automation do controle.</span><span class="sxs-lookup"><span data-stu-id="82e71-179">If there is a static text label, this property should expose a reference to the automation element of the control.</span></span>                                                                                                                |
| [<span data-ttu-id="82e71-180">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="82e71-180">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="82e71-181">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="82e71-181">See notes.</span></span> | <span data-ttu-id="82e71-182">Cadeia de caracteres localizada correspondente ao tipo de controle de **tabela** .</span><span class="sxs-lookup"><span data-stu-id="82e71-182">Localized string corresponding to the **Table** control type.</span></span> <span data-ttu-id="82e71-183">O valor padrão é "Table" para en-US ou inglês (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="82e71-183">The default value is "table" for en-US or English (United States).</span></span>                                                                                                  |
| [<span data-ttu-id="82e71-184">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="82e71-184">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="82e71-185">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="82e71-185">See notes.</span></span> | <span data-ttu-id="82e71-186">O controle tabela normalmente Obtém o valor para seu nome a partir de um rótulo de texto estático.</span><span class="sxs-lookup"><span data-stu-id="82e71-186">The table control typically gets the value for its name from a static text label.</span></span> <span data-ttu-id="82e71-187">Se não houver um rótulo de texto estático, o elemento deverá atribuir uma propriedade Name que deve estar sempre disponível para explicar a finalidade da tabela.</span><span class="sxs-lookup"><span data-stu-id="82e71-187">If there is not a static text label, the element must assign a Name property that must always be available to explain the purpose of the table.</span></span> |



 

## <a name="required-control-patterns"></a><span data-ttu-id="82e71-188">Padrões de controle necessários</span><span class="sxs-lookup"><span data-stu-id="82e71-188">Required Control Patterns</span></span>

<span data-ttu-id="82e71-189">A tabela a seguir lista os padrões de controle de automação da interface do usuário necessários para ter suporte de todos os controles de tabela.</span><span class="sxs-lookup"><span data-stu-id="82e71-189">The following table lists the UI Automation control patterns required to be supported by all table controls.</span></span> <span data-ttu-id="82e71-190">Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="82e71-190">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="82e71-191">Padrão de controle</span><span class="sxs-lookup"><span data-stu-id="82e71-191">Control Pattern</span></span>                                         | <span data-ttu-id="82e71-192">Suporte</span><span class="sxs-lookup"><span data-stu-id="82e71-192">Support</span></span>                     | <span data-ttu-id="82e71-193">Observações</span><span class="sxs-lookup"><span data-stu-id="82e71-193">Notes</span></span>                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="82e71-194">**IGridProvider**</span><span class="sxs-lookup"><span data-stu-id="82e71-194">**IGridProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)           | <span data-ttu-id="82e71-195">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="82e71-195">Required</span></span>                    | <span data-ttu-id="82e71-196">Como o controle tabela contém itens apresentados em uma grade, ele sempre dá suporte ao padrão de controle de [grade](uiauto-implementinggrid.md) .</span><span class="sxs-lookup"><span data-stu-id="82e71-196">Because the table control contains items presented in a grid, it always supports the [Grid](uiauto-implementinggrid.md) control pattern.</span></span>                                                                                                                                                    |
| [<span data-ttu-id="82e71-197">**IGridItemProvider**</span><span class="sxs-lookup"><span data-stu-id="82e71-197">**IGridItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)   | <span data-ttu-id="82e71-198">Necessário com objetos filho</span><span class="sxs-lookup"><span data-stu-id="82e71-198">Required with child objects</span></span> | <span data-ttu-id="82e71-199">Os objetos internos de uma tabela devem dar suporte aos padrões de controle [GridItem](uiauto-implementinggriditem.md) e [TableItem](uiauto-implementingtableitem.md) .</span><span class="sxs-lookup"><span data-stu-id="82e71-199">The inner objects of a table should support both the [GridItem](uiauto-implementinggriditem.md) and [TableItem](uiauto-implementingtableitem.md) control patterns.</span></span> <span data-ttu-id="82e71-200">A tabela em si não precisa oferecer suporte ao padrão de controle GridItem ou TableItem, a menos que a tabela faça parte de outra tabela.</span><span class="sxs-lookup"><span data-stu-id="82e71-200">The table itself need not support the GridItem or TableItem control pattern unless the table is part of another table.</span></span>  |
| [<span data-ttu-id="82e71-201">**ITableProvider**</span><span class="sxs-lookup"><span data-stu-id="82e71-201">**ITableProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)         | <span data-ttu-id="82e71-202">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="82e71-202">Required</span></span>                    | <span data-ttu-id="82e71-203">O controle tabela sempre pode ter cabeçalhos associados ao conteúdo.</span><span class="sxs-lookup"><span data-stu-id="82e71-203">The table control can always have headers associated with the content.</span></span>                                                                                                                                                                                                                       |
| [<span data-ttu-id="82e71-204">**ITableItemProvider**</span><span class="sxs-lookup"><span data-stu-id="82e71-204">**ITableItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) | <span data-ttu-id="82e71-205">Necessário com objetos filho</span><span class="sxs-lookup"><span data-stu-id="82e71-205">Required with child objects</span></span> | <span data-ttu-id="82e71-206">Os objetos internos de uma tabela devem dar suporte aos padrões de controle [GridItem](uiauto-implementinggriditem.md) e [TableItem](uiauto-implementingtableitem.md) .</span><span class="sxs-lookup"><span data-stu-id="82e71-206">The inner objects of a table should support both the [GridItem](uiauto-implementinggriditem.md) and [TableItem](uiauto-implementingtableitem.md) control patterns.</span></span> <span data-ttu-id="82e71-207">A própria tabela não precisa dar suporte aos padrões de controle GridItem ou TableItem, a menos que a tabela faça parte de outra tabela.</span><span class="sxs-lookup"><span data-stu-id="82e71-207">The table itself need not support the GridItem or TableItem control patterns unless the table is part of another table.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="82e71-208">Eventos necessários</span><span class="sxs-lookup"><span data-stu-id="82e71-208">Required Events</span></span>

<span data-ttu-id="82e71-209">A tabela a seguir lista os eventos de automação da interface do usuário aos quais os controles de tabela são necessários para dar suporte.</span><span class="sxs-lookup"><span data-stu-id="82e71-209">The following table lists the UI Automation events that table controls are required to support.</span></span> <span data-ttu-id="82e71-210">Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="82e71-210">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="82e71-211">Evento de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="82e71-211">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="82e71-212">Observações</span><span class="sxs-lookup"><span data-stu-id="82e71-212">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="82e71-213">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="82e71-213">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="82e71-214">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="82e71-214">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="82e71-215">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="82e71-215">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="82e71-216">Se o controle oferecer suporte à propriedade [**IsEnabled**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="82e71-216">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="82e71-217">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="82e71-217">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="82e71-218">Se o controle oferecer suporte à propriedade [**IsOffscreen**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="82e71-218">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="82e71-219">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="82e71-219">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="82e71-220">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="82e71-220">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="82e71-221">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="82e71-221">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="82e71-222">Visão Geral dos Tipos de Controle de Automação de Interface do Usuário</span><span class="sxs-lookup"><span data-stu-id="82e71-222">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="82e71-223">Visão geral de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="82e71-223">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




