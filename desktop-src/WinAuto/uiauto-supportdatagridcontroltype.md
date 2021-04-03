---
title: Tipo de controle DataGrid
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle DataGrid.
ms.assetid: 2381b302-37d6-4159-bb7d-862ae41af695
keywords:
- Automação da interface do usuário, suporte para tipo de controle DataGrid
- Automação da interface do usuário, tipo de controle DataGrid
- Automação da interface do usuário, estrutura de árvore para tipo de controle DataGrid
- Automação da interface do usuário, propriedades para tipo de controle DataGrid
- Automação da interface do usuário, padrões de controle para tipo de controle DataGrid
- Automação da interface do usuário, eventos para tipo de controle DataGrid
- estruturas de árvore, tipo de controle DataGrid
- Propriedades, tipo de controle DataGrid
- padrões de controle, tipo de controle DataGrid
- eventos, tipo de controle DataGrid
- suporte para tipo de controle DataGrid
- Tipo de controle DataGrid
- tipos de controle, estrutura de árvore para tipo de controle DataGrid
- tipos de controle, padrões de controle para o tipo de controle DataGrid
- tipos de controle, suporte para DataGrid
- tipos de controle, DataGrid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8af1e35e062c778285d1cb7edcca9ac6192792b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916207"
---
# <a name="datagrid-control-type"></a><span data-ttu-id="6f962-119">Tipo de controle DataGrid</span><span class="sxs-lookup"><span data-stu-id="6f962-119">DataGrid Control Type</span></span>

<span data-ttu-id="6f962-120">Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle **DataGrid** .</span><span class="sxs-lookup"><span data-stu-id="6f962-120">This topic provides information about Microsoft UI Automation support for the **DataGrid** control type.</span></span>

<span data-ttu-id="6f962-121">O tipo de controle **DataGrid** permite que um usuário trabalhe facilmente com itens que contêm dados ou elementos de automação apresentados em colunas ou linhas.</span><span class="sxs-lookup"><span data-stu-id="6f962-121">The **DataGrid** control type lets a user easily work with items that contain data or automation elements presented in columns or rows.</span></span> <span data-ttu-id="6f962-122">Os controles de grade de dados têm linhas de itens e colunas de informações sobre esses itens.</span><span class="sxs-lookup"><span data-stu-id="6f962-122">Data grid controls have rows of items and columns of information about those items.</span></span> <span data-ttu-id="6f962-123">Um controle de exibição de lista no Windows Vista Explorer é um exemplo que dá suporte ao tipo de controle **DataGrid** .</span><span class="sxs-lookup"><span data-stu-id="6f962-123">A list-view control in Windows Vista Explorer is an example that supports the **DataGrid** control type.</span></span>

<span data-ttu-id="6f962-124">As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle **DataGrid** .</span><span class="sxs-lookup"><span data-stu-id="6f962-124">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **DataGrid** control type.</span></span> <span data-ttu-id="6f962-125">Os requisitos de automação da interface do usuário se aplicam a todos os controles de grade de dados onde a estrutura/plataforma da interface do usuário integra o suporte à automação da interface do usuário para tipos de controle</span><span class="sxs-lookup"><span data-stu-id="6f962-125">The UI Automation requirements apply to all data grid controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="6f962-126">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="6f962-126">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="6f962-127">Estrutura de árvore típica</span><span class="sxs-lookup"><span data-stu-id="6f962-127">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="6f962-128">Propriedades relevantes</span><span class="sxs-lookup"><span data-stu-id="6f962-128">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="6f962-129">Padrões de controle necessários</span><span class="sxs-lookup"><span data-stu-id="6f962-129">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="6f962-130">Eventos necessários</span><span class="sxs-lookup"><span data-stu-id="6f962-130">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="6f962-131">Exemplo do tipo de controle DataGrid</span><span class="sxs-lookup"><span data-stu-id="6f962-131">DataGrid Control Type Example</span></span>](#datagrid-control-type-example)
-   [<span data-ttu-id="6f962-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6f962-132">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="6f962-133">Estrutura de árvore típica</span><span class="sxs-lookup"><span data-stu-id="6f962-133">Typical Tree Structure</span></span>

<span data-ttu-id="6f962-134">A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence a controles de grade de dados e descreve o que pode ser contido em cada exibição.</span><span class="sxs-lookup"><span data-stu-id="6f962-134">The following table depicts a typical control and content view of the UI Automation tree that pertains to data grid controls and describes what can be contained in each view.</span></span> <span data-ttu-id="6f962-135">Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="6f962-135">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6f962-136">Exibição de controle</span><span class="sxs-lookup"><span data-stu-id="6f962-136">Control View</span></span></th>
<th><span data-ttu-id="6f962-137">Exibição de conteúdo</span><span class="sxs-lookup"><span data-stu-id="6f962-137">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="6f962-138">DataGrid</span><span class="sxs-lookup"><span data-stu-id="6f962-138">DataGrid</span></span>
<ul>
<li><span data-ttu-id="6f962-139">Cabeçalho (0, 1 ou 2)</span><span class="sxs-lookup"><span data-stu-id="6f962-139">Header (0, 1, or 2)</span></span>
<ul>
<li><span data-ttu-id="6f962-140">HeaderItem (número de colunas ou linhas)</span><span class="sxs-lookup"><span data-stu-id="6f962-140">HeaderItem (number of columns or rows)</span></span></li>
</ul></li>
<li><span data-ttu-id="6f962-141">DataItem (0 ou mais; pode ser estruturado em uma hierarquia)</span><span class="sxs-lookup"><span data-stu-id="6f962-141">DataItem (0 or more; can be structured in a hierarchy)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="6f962-142">DataGrid</span><span class="sxs-lookup"><span data-stu-id="6f962-142">DataGrid</span></span>
<ul>
<li><span data-ttu-id="6f962-143">DataItem (0 ou mais; pode ser estruturado em uma hierarquia)</span><span class="sxs-lookup"><span data-stu-id="6f962-143">DataItem (0 or more; can be structured in a hierarchy)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="6f962-144">Propriedades relevantes</span><span class="sxs-lookup"><span data-stu-id="6f962-144">Relevant Properties</span></span>

<span data-ttu-id="6f962-145">A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para o tipo de controle **DataGrid** .</span><span class="sxs-lookup"><span data-stu-id="6f962-145">The following table lists the UI Automation properties whose value or definition is especially relevant to the **DataGrid** control type.</span></span> <span data-ttu-id="6f962-146">Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="6f962-146">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="6f962-147">Propriedade de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="6f962-147">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="6f962-148">Valor</span><span class="sxs-lookup"><span data-stu-id="6f962-148">Value</span></span>        | <span data-ttu-id="6f962-149">Observações</span><span class="sxs-lookup"><span data-stu-id="6f962-149">Notes</span></span>                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6f962-150">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="6f962-150">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="6f962-151">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="6f962-151">See notes.</span></span>   | <span data-ttu-id="6f962-152">O valor dessa propriedade deve ser exclusivo entre todos os elementos de mesmo nível na exibição bruta da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="6f962-152">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                                                                                                 |
| [<span data-ttu-id="6f962-153">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="6f962-153">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="6f962-154">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="6f962-154">See notes.</span></span>   | <span data-ttu-id="6f962-155">O retângulo mais externo que contém o controle inteiro.</span><span class="sxs-lookup"><span data-stu-id="6f962-155">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="6f962-156">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="6f962-156">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="6f962-157">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="6f962-157">See notes.</span></span>   | <span data-ttu-id="6f962-158">Com suporte se houver um retângulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="6f962-158">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="6f962-159">Se nem todos os pontos dentro do retângulo delimitador forem clicáveis, o elemento executará testes de clique especializados, substituirá e fornecerá um ponto clicável.</span><span class="sxs-lookup"><span data-stu-id="6f962-159">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span>                                                                                                         |
| [<span data-ttu-id="6f962-160">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="6f962-160">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="6f962-161">**DataGrid**</span><span class="sxs-lookup"><span data-stu-id="6f962-161">**DataGrid**</span></span> |                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="6f962-162">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="6f962-162">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="6f962-163">TRUE</span><span class="sxs-lookup"><span data-stu-id="6f962-163">TRUE</span></span>         | <span data-ttu-id="6f962-164">O valor dessa propriedade sempre deve ser **verdadeiro**.</span><span class="sxs-lookup"><span data-stu-id="6f962-164">The value of this property must always be **TRUE**.</span></span> <span data-ttu-id="6f962-165">Isso significa que o controle de grade de dados sempre deve estar na exibição de conteúdo da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="6f962-165">This means that the data grid control must always be in the content view of the UI Automation tree.</span></span>                                                                                                                                                      |
| [<span data-ttu-id="6f962-166">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="6f962-166">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="6f962-167">TRUE</span><span class="sxs-lookup"><span data-stu-id="6f962-167">TRUE</span></span>         | <span data-ttu-id="6f962-168">O valor dessa propriedade sempre deve ser **verdadeiro**.</span><span class="sxs-lookup"><span data-stu-id="6f962-168">The value of this property must always **TRUE**.</span></span> <span data-ttu-id="6f962-169">Isso significa que o controle de grade de dados sempre deve ser incluído na exibição de controle da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="6f962-169">This means that the data grid control must always be included in the control view of the UI Automation tree.</span></span>                                                                                                                                                |
| [<span data-ttu-id="6f962-170">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="6f962-170">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="6f962-171">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="6f962-171">See notes.</span></span>   | <span data-ttu-id="6f962-172">Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="6f962-172">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                                                                                                                                    |
| [<span data-ttu-id="6f962-173">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="6f962-173">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="6f962-174">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="6f962-174">See notes.</span></span>   | <span data-ttu-id="6f962-175">Se houver um rótulo de texto estático, essa propriedade deverá expor uma referência a esse controle.</span><span class="sxs-lookup"><span data-stu-id="6f962-175">If there is a static text label, this property must expose a reference to that control.</span></span>                                                                                                                                                                                                                      |
| [<span data-ttu-id="6f962-176">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="6f962-176">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="6f962-177">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="6f962-177">See notes.</span></span>   | <span data-ttu-id="6f962-178">Cadeia de caracteres localizada correspondente ao tipo de controle **DataGrid** .</span><span class="sxs-lookup"><span data-stu-id="6f962-178">Localized string corresponding to the **DataGrid** control type.</span></span> <span data-ttu-id="6f962-179">O valor padrão é "grade de dados" para en-US ou inglês (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="6f962-179">The default value is "data grid" for en-US or English (United States).</span></span>                                                                                                                                                                      |
| [<span data-ttu-id="6f962-180">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="6f962-180">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="6f962-181">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="6f962-181">See notes.</span></span>   | <span data-ttu-id="6f962-182">O controle de grade de dados normalmente Obtém o valor de sua propriedade **Name** de um rótulo de texto estático.</span><span class="sxs-lookup"><span data-stu-id="6f962-182">The data grid control typically gets the value for its **Name** property from a static text label.</span></span> <span data-ttu-id="6f962-183">Se não houver um rótulo de texto estático, um desenvolvedor de aplicativo deverá atribuir um valor para a propriedade **Name** .</span><span class="sxs-lookup"><span data-stu-id="6f962-183">If there is not a static text label an application developer must assign a value to for the **Name** property.</span></span> <span data-ttu-id="6f962-184">O valor da propriedade **Name** nunca deve ser o conteúdo textual do controle de edição.</span><span class="sxs-lookup"><span data-stu-id="6f962-184">The value of the **Name** property must never be the textual contents of the edit control.</span></span> |



 

## <a name="required-control-patterns"></a><span data-ttu-id="6f962-185">Padrões de controle necessários</span><span class="sxs-lookup"><span data-stu-id="6f962-185">Required Control Patterns</span></span>

<span data-ttu-id="6f962-186">A tabela a seguir lista os padrões de controle de automação da interface do usuário que devem ter suporte de todos os controles de grade de dados.</span><span class="sxs-lookup"><span data-stu-id="6f962-186">The following table lists the UI Automation control patterns required to be supported by all data grid controls.</span></span> <span data-ttu-id="6f962-187">Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="6f962-187">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="6f962-188">Padrão de controle</span><span class="sxs-lookup"><span data-stu-id="6f962-188">Control Pattern</span></span>                                         | <span data-ttu-id="6f962-189">Suporte</span><span class="sxs-lookup"><span data-stu-id="6f962-189">Support</span></span>  | <span data-ttu-id="6f962-190">Observações</span><span class="sxs-lookup"><span data-stu-id="6f962-190">Notes</span></span>                                                                                                                                                                             |
|---------------------------------------------------------|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6f962-191">**IGridProvider**</span><span class="sxs-lookup"><span data-stu-id="6f962-191">**IGridProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)           | <span data-ttu-id="6f962-192">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="6f962-192">Required</span></span> | <span data-ttu-id="6f962-193">O próprio controle de grade de dados sempre dá suporte ao padrão de controle de [grade](uiauto-implementinggrid.md) porque os itens que ele contém têm metadados que são dispostos em uma grade.</span><span class="sxs-lookup"><span data-stu-id="6f962-193">The data grid control itself always supports the [Grid](uiauto-implementinggrid.md) control pattern because the items that it contains have metadata that is laid out in a grid.</span></span> |
| [<span data-ttu-id="6f962-194">**IScrollProvider**</span><span class="sxs-lookup"><span data-stu-id="6f962-194">**IScrollProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)       | <span data-ttu-id="6f962-195">Depende</span><span class="sxs-lookup"><span data-stu-id="6f962-195">Depends</span></span>  | <span data-ttu-id="6f962-196">A capacidade de rolar a grade de dados depende do conteúdo e se as barras de rolagem estão presentes.</span><span class="sxs-lookup"><span data-stu-id="6f962-196">The ability to scroll the data grid depends on content and whether scroll bars are present.</span></span>                                                                                       |
| [<span data-ttu-id="6f962-197">**ISelectionProvider**</span><span class="sxs-lookup"><span data-stu-id="6f962-197">**ISelectionProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) | <span data-ttu-id="6f962-198">Depende</span><span class="sxs-lookup"><span data-stu-id="6f962-198">Depends</span></span>  | <span data-ttu-id="6f962-199">A capacidade de selecionar a grade de dados depende do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="6f962-199">The ability to select the data grid depends on content.</span></span>                                                                                                                           |
| [<span data-ttu-id="6f962-200">**ITableProvider**</span><span class="sxs-lookup"><span data-stu-id="6f962-200">**ITableProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)         | <span data-ttu-id="6f962-201">Depende</span><span class="sxs-lookup"><span data-stu-id="6f962-201">Depends</span></span>  | <span data-ttu-id="6f962-202">Um controle de grade de dados que tem um cabeçalho deve dar suporte ao padrão de controle de [tabela](uiauto-implementingtable.md) .</span><span class="sxs-lookup"><span data-stu-id="6f962-202">A data grid control that has a header should support the [Table](uiauto-implementingtable.md) control pattern.</span></span>                                                                   |



 

<span data-ttu-id="6f962-203">Os itens de dados dentro dos contêineres de grade de dados terão suporte no mínimo:</span><span class="sxs-lookup"><span data-stu-id="6f962-203">Data items within the data grid containers will support at a minimum:</span></span>

-   <span data-ttu-id="6f962-204">Padrão de controle [SelectionItem](uiauto-implementingselectionitem.md) (se a grade de dados for selecionável)</span><span class="sxs-lookup"><span data-stu-id="6f962-204">[SelectionItem](uiauto-implementingselectionitem.md) control pattern (if the data grid is selectable)</span></span>
-   <span data-ttu-id="6f962-205">Padrão de controle [ScrollItem](uiauto-implementingscrollitem.md) (se a grade de dados for rolável)</span><span class="sxs-lookup"><span data-stu-id="6f962-205">[ScrollItem](uiauto-implementingscrollitem.md) control pattern (if the data grid is scrollable)</span></span>
-   <span data-ttu-id="6f962-206">Padrão de controle [GridItem](uiauto-implementinggriditem.md)</span><span class="sxs-lookup"><span data-stu-id="6f962-206">[GridItem](uiauto-implementinggriditem.md) control pattern</span></span>
-   <span data-ttu-id="6f962-207">Padrão de controle [TableItem](uiauto-implementingtableitem.md) (se a grade de dados tiver um cabeçalho)</span><span class="sxs-lookup"><span data-stu-id="6f962-207">[TableItem](uiauto-implementingtableitem.md) control pattern (if the data grid has a header)</span></span>

## <a name="required-events"></a><span data-ttu-id="6f962-208">Eventos necessários</span><span class="sxs-lookup"><span data-stu-id="6f962-208">Required Events</span></span>

<span data-ttu-id="6f962-209">A tabela a seguir lista os eventos de automação da interface do usuário aos quais os controles de grade de dados devem dar suporte.</span><span class="sxs-lookup"><span data-stu-id="6f962-209">The following table lists the UI Automation events that data grid controls are required to support.</span></span> <span data-ttu-id="6f962-210">Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="6f962-210">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="6f962-211">Evento de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="6f962-211">UI Automation Event</span></span>                                                                                                                                        | <span data-ttu-id="6f962-212">Observações</span><span class="sxs-lookup"><span data-stu-id="6f962-212">Notes</span></span>                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6f962-213">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="6f962-213">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                           |                                                                                                                                                          |
| <span data-ttu-id="6f962-214">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="6f962-214">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                      |                                                                                                                                                          |
| <span data-ttu-id="6f962-215">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="6f962-215">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                      | <span data-ttu-id="6f962-216">Se o controle oferecer suporte à propriedade [**IsEnabled**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="6f962-216">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>                                 |
| <span data-ttu-id="6f962-217">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="6f962-217">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                  | <span data-ttu-id="6f962-218">Se o controle oferecer suporte à propriedade [**IsOffscreen**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="6f962-218">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>                               |
| [<span data-ttu-id="6f962-219">**UIA \_ LayoutInvalidatedEventId**</span><span class="sxs-lookup"><span data-stu-id="6f962-219">**UIA\_LayoutInvalidatedEventId**</span></span>](uiauto-event-ids.md)                                                                     |                                                                                                                                                          |
| [<span data-ttu-id="6f962-220">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="6f962-220">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                       |                                                                                                                                                          |
| <span data-ttu-id="6f962-221">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade MultipleViewCurrentViewPropertyId.</span><span class="sxs-lookup"><span data-stu-id="6f962-221">[**UIA\_MultipleViewCurrentViewPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>             | <span data-ttu-id="6f962-222">Se o controle der suporte à propriedade Modoatual do padrão de controle [MultipleView](uiauto-implementingmultipleview.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="6f962-222">If the control supports the CurrentView property of the [MultipleView](uiauto-implementingmultipleview.md) control pattern, it must support this event.</span></span> |
| <span data-ttu-id="6f962-223">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollHorizontallyScrollablePropertyId.</span><span class="sxs-lookup"><span data-stu-id="6f962-223">[**UIA\_ScrollHorizontallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>   | <span data-ttu-id="6f962-224">Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="6f962-224">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>                                         |
| <span data-ttu-id="6f962-225">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollHorizontalScrollPercentPropertyId.</span><span class="sxs-lookup"><span data-stu-id="6f962-225">[**UIA\_ScrollHorizontalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="6f962-226">Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="6f962-226">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>                                         |
| <span data-ttu-id="6f962-227">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollHorizontalViewSizePropertyId.</span><span class="sxs-lookup"><span data-stu-id="6f962-227">[**UIA\_ScrollHorizontalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>           | <span data-ttu-id="6f962-228">Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="6f962-228">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>                                         |
| <span data-ttu-id="6f962-229">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollVerticalScrollPercentPropertyId.</span><span class="sxs-lookup"><span data-stu-id="6f962-229">[**UIA\_ScrollVerticalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>     | <span data-ttu-id="6f962-230">Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="6f962-230">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>                                         |
| <span data-ttu-id="6f962-231">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollVerticallyScrollablePropertyId.</span><span class="sxs-lookup"><span data-stu-id="6f962-231">[**UIA\_ScrollVerticallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>       | <span data-ttu-id="6f962-232">Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="6f962-232">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>                                         |
| <span data-ttu-id="6f962-233">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollVerticalViewSizePropertyId.</span><span class="sxs-lookup"><span data-stu-id="6f962-233">[**UIA\_ScrollVerticalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>               | <span data-ttu-id="6f962-234">Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="6f962-234">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>                                         |
| [<span data-ttu-id="6f962-235">**\_InvalidatedEventId de seleção de UIA \_**</span><span class="sxs-lookup"><span data-stu-id="6f962-235">**UIA\_Selection\_InvalidatedEventId**</span></span>](uiauto-event-ids.md)                                                            |                                                                                                                                                          |



 

## <a name="datagrid-control-type-example"></a><span data-ttu-id="6f962-236">Exemplo do tipo de controle DataGrid</span><span class="sxs-lookup"><span data-stu-id="6f962-236">DataGrid Control Type Example</span></span>

<span data-ttu-id="6f962-237">A imagem a seguir ilustra um controle de exibição de lista que implementa o tipo de controle **DataGrid** .</span><span class="sxs-lookup"><span data-stu-id="6f962-237">The following image illustrates a list-view control that implements the **DataGrid** control type.</span></span>

![captura de tela do controle de exibição de lista com o tipo de controle DataGrid](images/datagridxmpl.jpg)

<span data-ttu-id="6f962-239">A exibição de controle e a exibição de conteúdo da árvore de automação da interface do usuário que pertencem ao controle de exibição de lista são exibidas abaixo.</span><span class="sxs-lookup"><span data-stu-id="6f962-239">The control view and the content view of the UI Automation tree that pertains to the list-view control is displayed below.</span></span> <span data-ttu-id="6f962-240">Os padrões de controle para cada elemento de automação são mostrados entre parênteses.</span><span class="sxs-lookup"><span data-stu-id="6f962-240">The control patterns for each automation element are shown in parentheses.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6f962-241">Árvore de automação da interface do usuário – exibição de controle</span><span class="sxs-lookup"><span data-stu-id="6f962-241">UI Automation Tree - Control View</span></span></th>
<th><span data-ttu-id="6f962-242">Árvore de automação da interface do usuário – exibição de conteúdo</span><span class="sxs-lookup"><span data-stu-id="6f962-242">UI Automation Tree - Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6f962-243">DataGrid (classificação, tabela, seleção, grade)</span><span class="sxs-lookup"><span data-stu-id="6f962-243">DataGrid (Sort, Table, Selection, Grid)</span></span>
<ul>
<li><span data-ttu-id="6f962-244">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6f962-244">Header</span></span>
<ul>
<li><span data-ttu-id="6f962-245">&quot;Nome &quot; do HeaderItem (invocar)</span><span class="sxs-lookup"><span data-stu-id="6f962-245">HeaderItem &quot;Name&quot; (Invoke)</span></span></li>
<li><span data-ttu-id="6f962-246">HeaderItem &quot; data modificada &quot; (Invoke)</span><span class="sxs-lookup"><span data-stu-id="6f962-246">HeaderItem &quot;Date Modified&quot; (Invoke)</span></span></li>
<li><span data-ttu-id="6f962-247">&quot;Tamanho &quot; do HeaderItem (Invoke)</span><span class="sxs-lookup"><span data-stu-id="6f962-247">HeaderItem &quot;Size&quot; (Invoke)</span></span></li>
</ul></li>
<li><span data-ttu-id="6f962-248">Grupo &quot; Contoso &quot; (TableItem, GridItem, SelectionItem, tabela *, grade*)</span><span class="sxs-lookup"><span data-stu-id="6f962-248">Group &quot;Contoso&quot; (TableItem, GridItem, SelectionItem, Table *, Grid*)</span></span>
<ul>
<li><span data-ttu-id="6f962-249">&quot;Receivable.docde contas &quot; do DataItem (SelectionItem, Invoke, TableItem *, GridItem*)</span><span class="sxs-lookup"><span data-stu-id="6f962-249">DataItem &quot;Accounts Receivable.doc&quot; (SelectionItem, Invoke, TableItem *, GridItem*)</span></span></li>
<li><span data-ttu-id="6f962-250">&quot;Payable.docde contas &quot; do DataItem (SelectionItem, Invoke, TableItem *, GridItem*)</span><span class="sxs-lookup"><span data-stu-id="6f962-250">DataItem &quot;Accounts Payable.doc&quot; (SelectionItem, Invoke, TableItem *, GridItem*)</span></span></li>
</ul></li>
</ul></td>
<td><span data-ttu-id="6f962-251">DataGrid (tabela, grade, seleção)</span><span class="sxs-lookup"><span data-stu-id="6f962-251">DataGrid (Table, Grid, Selection)</span></span>
<ul>
<li><span data-ttu-id="6f962-252">Grupo &quot; Contoso &quot; (TableItem, GridItem, SelectionItem, tabela *, grade*)</span><span class="sxs-lookup"><span data-stu-id="6f962-252">Group &quot;Contoso&quot; (TableItem, GridItem, SelectionItem, Table *, Grid*)</span></span>
<ul>
<li><span data-ttu-id="6f962-253">&quot;Receivable.docde contas &quot; do DataItem (SelectionItem, Invoke, TableItem *, GridItem*)</span><span class="sxs-lookup"><span data-stu-id="6f962-253">DataItem &quot;Accounts Receivable.doc&quot; (SelectionItem, Invoke, TableItem *, GridItem*)</span></span></li>
<li><span data-ttu-id="6f962-254">&quot;Payable.docde contas &quot; do DataItem (SelectionItem, Invoke, TableItem *, GridItem*)</span><span class="sxs-lookup"><span data-stu-id="6f962-254">DataItem &quot;Accounts Payable.doc&quot; (SelectionItem, Invoke, TableItem *, GridItem*)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="6f962-255">\*O exemplo anterior mostra uma grade de dados que contém vários níveis de controles.</span><span class="sxs-lookup"><span data-stu-id="6f962-255">\*The preceding example shows a data grid that contains multiple levels of controls.</span></span> <span data-ttu-id="6f962-256">O controle **Group** ("contoso") contém dois controles **DataItem** ("accounts Receivable.doc" e "accounts Payable.doc").</span><span class="sxs-lookup"><span data-stu-id="6f962-256">The **Group** ("Contoso") control contains two **DataItem** controls ("Accounts Receivable.doc" and "Accounts Payable.doc").</span></span> <span data-ttu-id="6f962-257">Um  / par de **GridItem** DataGrid é independente de um par em outro nível.</span><span class="sxs-lookup"><span data-stu-id="6f962-257">A **DataGrid**/**GridItem** pair is independent of a pair at another level.</span></span> <span data-ttu-id="6f962-258">Os controles de **DataItem** em um **grupo** também podem ser expostos como um tipo de controle [ListItem](uiauto-supportlistitemcontroltype.md) , permitindo que eles sejam apresentados mais claramente como objetos selecionáveis, e não como elementos de dados simples.</span><span class="sxs-lookup"><span data-stu-id="6f962-258">The **DataItem** controls under a **Group** can also be exposed as a [ListItem](uiauto-supportlistitemcontroltype.md) control type, enabling them to be presented more clearly as selectable objects, rather than as simple data elements.</span></span> <span data-ttu-id="6f962-259">Este exemplo não inclui os subelementos dos itens de dados agrupados.</span><span class="sxs-lookup"><span data-stu-id="6f962-259">This example does not include the sub-elements of the grouped data items.</span></span> <span data-ttu-id="6f962-260">Para obter outro exemplo de vários níveis de controles, consulte o tipo de controle [DataItem](uiauto-supportdataitemcontroltype.md) .</span><span class="sxs-lookup"><span data-stu-id="6f962-260">For another example of multiple levels of controls, see the [DataItem](uiauto-supportdataitemcontroltype.md) control type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6f962-261">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6f962-261">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="6f962-262">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="6f962-262">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6f962-263">Visão Geral dos Tipos de Controle de Automação de Interface do Usuário</span><span class="sxs-lookup"><span data-stu-id="6f962-263">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="6f962-264">Visão geral de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="6f962-264">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




