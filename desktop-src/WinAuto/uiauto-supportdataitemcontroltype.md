---
title: Tipo de controle DataItem
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle DataItem.
ms.assetid: def52fe7-9f05-4cd0-8a46-af4e2e3ba03e
keywords:
- Automação da interface do usuário, suporte para tipo de controle DataItem
- Automação da interface do usuário, tipo de controle DataItem
- Automação da interface do usuário, estrutura de árvore para tipo de controle de DataItem
- Automação da interface do usuário, propriedades para tipo de controle DataItem
- Automação da interface do usuário, padrões de controle para o tipo de controle DataItem
- Automação da interface do usuário, eventos para tipo de controle DataItem
- Automação da interface do usuário, listas grandes e tipo de controle de DataItem
- estruturas de árvore, tipo de controle DataItem
- Propriedades, tipo de controle DataItem
- padrões de controle, tipo de controle DataItem
- eventos, tipo de controle DataItem
- listas grandes
- suporte para tipo de controle DataItem
- Tipo de controle DataItem
- tipos de controle, estrutura de árvore para o tipo de controle DataItem
- tipos de controle, padrões de controle para o tipo de controle DataItem
- tipos de controle, listas grandes e tipo de controle DataItem
- tipos de controle, suporte para DataItem
- tipos de controle, DataItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0902cc593ec7f9104ed27031caa2785b7cb9756
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005413"
---
# <a name="dataitem-control-type"></a><span data-ttu-id="7fba8-122">Tipo de controle DataItem</span><span class="sxs-lookup"><span data-stu-id="7fba8-122">DataItem Control Type</span></span>

<span data-ttu-id="7fba8-123">Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle **DataItem** .</span><span class="sxs-lookup"><span data-stu-id="7fba8-123">This topic provides information about Microsoft UI Automation support for the **DataItem** control type.</span></span>

<span data-ttu-id="7fba8-124">Uma entrada em uma lista de contatos é um exemplo de controle de item de dados.</span><span class="sxs-lookup"><span data-stu-id="7fba8-124">An entry in a Contacts list is an example of a data item control.</span></span> <span data-ttu-id="7fba8-125">Um controle de item de dados contém informações de interesse de um usuário final.</span><span class="sxs-lookup"><span data-stu-id="7fba8-125">A data item control contains information that is of interest to an end user.</span></span> <span data-ttu-id="7fba8-126">É mais complicado do que o item de lista simples, pois contém informações mais ricas.</span><span class="sxs-lookup"><span data-stu-id="7fba8-126">It is more complicated than the simple list item because it contains richer information.</span></span>

<span data-ttu-id="7fba8-127">As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle **DataItem** .</span><span class="sxs-lookup"><span data-stu-id="7fba8-127">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **DataItem** control type.</span></span> <span data-ttu-id="7fba8-128">Os requisitos de automação da interface do usuário se aplicam a todos os controles de item de dados onde a estrutura/plataforma da interface do usuário integra o suporte à automação da interface do usuário para tipos de controle</span><span class="sxs-lookup"><span data-stu-id="7fba8-128">The UI Automation requirements apply to all data item controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="7fba8-129">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="7fba8-129">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="7fba8-130">Estrutura de árvore típica</span><span class="sxs-lookup"><span data-stu-id="7fba8-130">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="7fba8-131">Propriedades relevantes</span><span class="sxs-lookup"><span data-stu-id="7fba8-131">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="7fba8-132">Padrões de controle necessários</span><span class="sxs-lookup"><span data-stu-id="7fba8-132">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="7fba8-133">Trabalhando com dataItems em listas grandes</span><span class="sxs-lookup"><span data-stu-id="7fba8-133">Working with DataItems in Large Lists</span></span>](#working-with-dataitems-in-large-lists)
-   [<span data-ttu-id="7fba8-134">Eventos necessários</span><span class="sxs-lookup"><span data-stu-id="7fba8-134">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="7fba8-135">Exemplo de tipo de controle DataItem</span><span class="sxs-lookup"><span data-stu-id="7fba8-135">DataItem Control Type Example</span></span>](#dataitem-control-type-example)
-   [<span data-ttu-id="7fba8-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7fba8-136">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="7fba8-137">Estrutura de árvore típica</span><span class="sxs-lookup"><span data-stu-id="7fba8-137">Typical Tree Structure</span></span>

<span data-ttu-id="7fba8-138">A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence a controles de item de dados e descreve o que pode ser contido em cada exibição.</span><span class="sxs-lookup"><span data-stu-id="7fba8-138">The following table depicts a typical control and content view of the UI Automation tree that pertains to data item controls and describes what can be contained in each view.</span></span> <span data-ttu-id="7fba8-139">Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="7fba8-139">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7fba8-140">Exibição de controle</span><span class="sxs-lookup"><span data-stu-id="7fba8-140">Control View</span></span></th>
<th><span data-ttu-id="7fba8-141">Exibição de conteúdo</span><span class="sxs-lookup"><span data-stu-id="7fba8-141">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="7fba8-142">DataItem</span><span class="sxs-lookup"><span data-stu-id="7fba8-142">DataItem</span></span>
<ul>
<li><span data-ttu-id="7fba8-143">Varia (0 ou mais; pode ser estruturado na hierarquia)</span><span class="sxs-lookup"><span data-stu-id="7fba8-143">Varies (0 or more; can be structured in hierarchy)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="7fba8-144">DataItem</span><span class="sxs-lookup"><span data-stu-id="7fba8-144">DataItem</span></span>
<ul>
<li><span data-ttu-id="7fba8-145">Varia (0 ou mais; pode ser estruturado na hierarquia)</span><span class="sxs-lookup"><span data-stu-id="7fba8-145">Varies (0 or more; can be structured in hierarchy)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="7fba8-146">Um elemento de item de dados em uma grade de dados pode hospedar uma variedade de objetos, incluindo outra camada de itens de dados ou elementos de grade específicos, como texto, imagens ou controles de edição.</span><span class="sxs-lookup"><span data-stu-id="7fba8-146">A data item element in a data grid can host a variety of objects, including another layer of data items, or specific grid elements such as text, images, or edit controls.</span></span> <span data-ttu-id="7fba8-147">Se o elemento de item de dados tiver uma função de objeto específica, o elemento deverá ser exposto como um tipo de controle específico; por exemplo, um tipo de controle de [ListItem](uiauto-supportlistitemcontroltype.md) para um item de dados selecionável na grade.</span><span class="sxs-lookup"><span data-stu-id="7fba8-147">If the data item element has a specific object role, the element should be exposed as a specific control type; for example, a [ListItem](uiauto-supportlistitemcontroltype.md) control type for a selectable data item in the grid.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="7fba8-148">Propriedades relevantes</span><span class="sxs-lookup"><span data-stu-id="7fba8-148">Relevant Properties</span></span>

<span data-ttu-id="7fba8-149">A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para o tipo de controle DataItem.</span><span class="sxs-lookup"><span data-stu-id="7fba8-149">The following table lists the UI Automation properties whose value or definition is especially relevant to the DataItem control type.</span></span> <span data-ttu-id="7fba8-150">Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="7fba8-150">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="7fba8-151">Propriedade de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="7fba8-151">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="7fba8-152">Valor</span><span class="sxs-lookup"><span data-stu-id="7fba8-152">Value</span></span>        | <span data-ttu-id="7fba8-153">Observações</span><span class="sxs-lookup"><span data-stu-id="7fba8-153">Notes</span></span>                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7fba8-154">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="7fba8-154">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="7fba8-155">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="7fba8-155">See notes.</span></span>   | <span data-ttu-id="7fba8-156">O valor dessa propriedade deve ser exclusivo entre todos os elementos de mesmo nível na exibição bruta da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="7fba8-156">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                         |
| [<span data-ttu-id="7fba8-157">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="7fba8-157">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="7fba8-158">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="7fba8-158">See notes.</span></span>   | <span data-ttu-id="7fba8-159">O retângulo mais externo que contém o controle inteiro.</span><span class="sxs-lookup"><span data-stu-id="7fba8-159">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                             |
| [<span data-ttu-id="7fba8-160">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="7fba8-160">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="7fba8-161">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="7fba8-161">See notes.</span></span>   | <span data-ttu-id="7fba8-162">Com suporte se houver um retângulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="7fba8-162">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="7fba8-163">Se nem todos os pontos dentro do retângulo delimitador forem clicáveis, o elemento executará testes de clique especializados, substituirá e fornecerá um ponto clicável.</span><span class="sxs-lookup"><span data-stu-id="7fba8-163">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span> |
| [<span data-ttu-id="7fba8-164">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="7fba8-164">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="7fba8-165">**DataItem**</span><span class="sxs-lookup"><span data-stu-id="7fba8-165">**DataItem**</span></span> |                                                                                                                                                                                                      |
| [<span data-ttu-id="7fba8-166">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="7fba8-166">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="7fba8-167">TRUE</span><span class="sxs-lookup"><span data-stu-id="7fba8-167">TRUE</span></span>         | <span data-ttu-id="7fba8-168">O controle de item de dados sempre deve ser conteúdo.</span><span class="sxs-lookup"><span data-stu-id="7fba8-168">The data item control must always be content.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="7fba8-169">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="7fba8-169">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="7fba8-170">TRUE</span><span class="sxs-lookup"><span data-stu-id="7fba8-170">TRUE</span></span>         | <span data-ttu-id="7fba8-171">O controle de item de dados sempre deve ser um controle.</span><span class="sxs-lookup"><span data-stu-id="7fba8-171">The data item control must always be a control.</span></span>                                                                                                                                                      |
| [<span data-ttu-id="7fba8-172">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="7fba8-172">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="7fba8-173">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="7fba8-173">See notes.</span></span>   | <span data-ttu-id="7fba8-174">Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="7fba8-174">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                            |
| [<span data-ttu-id="7fba8-175">**UIA \_ ItemStatusPropertyId**</span><span class="sxs-lookup"><span data-stu-id="7fba8-175">**UIA\_ItemStatusPropertyId**</span></span>](uiauto-automation-element-propids.md)                     | <span data-ttu-id="7fba8-176">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="7fba8-176">See notes.</span></span>   | <span data-ttu-id="7fba8-177">Se o controle contiver o status que está sendo atualizado dinamicamente, essa propriedade deverá ter suporte para que uma tecnologia assistencial possa receber atualizações quando o status do elemento for alterado.</span><span class="sxs-lookup"><span data-stu-id="7fba8-177">If the control contains status that is being updated dynamically, this property must be supported so that an assistive technology can receive updates when the status of the element changes.</span></span>        |
| [<span data-ttu-id="7fba8-178">**UIA \_ ItemTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="7fba8-178">**UIA\_ItemTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                         | <span data-ttu-id="7fba8-179">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="7fba8-179">See notes.</span></span>   | <span data-ttu-id="7fba8-180">Esse é o valor da cadeia de caracteres que transmite ao usuário final o objeto subjacente que o item representa.</span><span class="sxs-lookup"><span data-stu-id="7fba8-180">This is the string value that conveys to the end user the underlying object that the item represents.</span></span> <span data-ttu-id="7fba8-181">Os exemplos incluem "arquivo de mídia" e "contato".</span><span class="sxs-lookup"><span data-stu-id="7fba8-181">Examples include "Media File" and "Contact".</span></span>                                                   |
| [<span data-ttu-id="7fba8-182">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="7fba8-182">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="7fba8-183">Nulo</span><span class="sxs-lookup"><span data-stu-id="7fba8-183">Null</span></span>         | <span data-ttu-id="7fba8-184">Os controles de item de dados não têm um rótulo de texto estático.</span><span class="sxs-lookup"><span data-stu-id="7fba8-184">Data item controls do not have a static text label.</span></span>                                                                                                                                                  |
| [<span data-ttu-id="7fba8-185">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="7fba8-185">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="7fba8-186">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="7fba8-186">See notes.</span></span>   | <span data-ttu-id="7fba8-187">Cadeia de caracteres localizada correspondente ao tipo de controle **DataItem** .</span><span class="sxs-lookup"><span data-stu-id="7fba8-187">Localized string corresponding to the **DataItem** control type.</span></span> <span data-ttu-id="7fba8-188">O valor padrão é "item de dados" para en-US ou inglês (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="7fba8-188">The default value is "data item" for en-US or English (United States).</span></span>                                                              |
| [<span data-ttu-id="7fba8-189">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="7fba8-189">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="7fba8-190">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="7fba8-190">See notes.</span></span>   | <span data-ttu-id="7fba8-191">O controle de item de dados sempre contém um elemento de texto primário que o usuário reconheceria como o identificador do item.</span><span class="sxs-lookup"><span data-stu-id="7fba8-191">The data item control always contains a primary text element that the user would recognize as the identifier for the item.</span></span>                                                                           |



 

## <a name="required-control-patterns"></a><span data-ttu-id="7fba8-192">Padrões de controle necessários</span><span class="sxs-lookup"><span data-stu-id="7fba8-192">Required Control Patterns</span></span>

<span data-ttu-id="7fba8-193">A tabela a seguir lista os padrões de controle de automação da interface do usuário que devem ter suporte de todos os controles de item de dados.</span><span class="sxs-lookup"><span data-stu-id="7fba8-193">The following table lists the UI Automation control patterns required to be supported by all data item controls.</span></span> <span data-ttu-id="7fba8-194">Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="7fba8-194">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="7fba8-195">Padrão de controle</span><span class="sxs-lookup"><span data-stu-id="7fba8-195">Control Pattern</span></span>                                                   | <span data-ttu-id="7fba8-196">Suporte</span><span class="sxs-lookup"><span data-stu-id="7fba8-196">Support</span></span> | <span data-ttu-id="7fba8-197">Observações</span><span class="sxs-lookup"><span data-stu-id="7fba8-197">Notes</span></span>                                                                                                                                                                                                                 |
|-------------------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7fba8-198">**IExpandCollapseProvider**</span><span class="sxs-lookup"><span data-stu-id="7fba8-198">**IExpandCollapseProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | <span data-ttu-id="7fba8-199">Depende</span><span class="sxs-lookup"><span data-stu-id="7fba8-199">Depends</span></span> | <span data-ttu-id="7fba8-200">Se o item de dados puder ser expandido ou recolhido para mostrar e ocultar informações, o padrão de controle [ExpandCollapse](uiauto-implementingexpandcollapse.md) deverá ser suportado.</span><span class="sxs-lookup"><span data-stu-id="7fba8-200">If the data item can be expanded or collapsed to show and hide information, the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern must be supported.</span></span>                                            |
| [<span data-ttu-id="7fba8-201">**IGridItemProvider**</span><span class="sxs-lookup"><span data-stu-id="7fba8-201">**IGridItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)             | <span data-ttu-id="7fba8-202">Depende</span><span class="sxs-lookup"><span data-stu-id="7fba8-202">Depends</span></span> | <span data-ttu-id="7fba8-203">Os itens de dados oferecerão suporte ao padrão de controle [GridItem](uiauto-implementinggriditem.md) quando uma coleção de itens de dados estiver disponível em um contêiner que pode ser acessado espacialmente item a item.</span><span class="sxs-lookup"><span data-stu-id="7fba8-203">Data items will support the [GridItem](uiauto-implementinggriditem.md) control pattern when a collection of data items is available within a container that can be spatially navigated item-to-item.</span></span>                 |
| [<span data-ttu-id="7fba8-204">**IScrollItemProvider**</span><span class="sxs-lookup"><span data-stu-id="7fba8-204">**IScrollItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider)         | <span data-ttu-id="7fba8-205">Depende</span><span class="sxs-lookup"><span data-stu-id="7fba8-205">Depends</span></span> | <span data-ttu-id="7fba8-206">Todos os itens de dados dão suporte à capacidade de serem rolados para o modo de exibição com o padrão de controle [ScrollItem](uiauto-implementingscrollitem.md) quando o contêiner de dados tem mais itens do que pode caber na tela.</span><span class="sxs-lookup"><span data-stu-id="7fba8-206">All data items support the ability to be scrolled into view with the [ScrollItem](uiauto-implementingscrollitem.md) control pattern when their data container has more items than can fit on the screen.</span></span>             |
| [<span data-ttu-id="7fba8-207">**ISelectionItemProvider**</span><span class="sxs-lookup"><span data-stu-id="7fba8-207">**ISelectionItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)   | <span data-ttu-id="7fba8-208">Depende</span><span class="sxs-lookup"><span data-stu-id="7fba8-208">Depends</span></span> | <span data-ttu-id="7fba8-209">A capacidade de selecionar os itens de dados depende do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="7fba8-209">The ability to select the data items depends on the content.</span></span>                                                                                                                                                          |
| [<span data-ttu-id="7fba8-210">**ITableItemProvider**</span><span class="sxs-lookup"><span data-stu-id="7fba8-210">**ITableItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider)           | <span data-ttu-id="7fba8-211">Depende</span><span class="sxs-lookup"><span data-stu-id="7fba8-211">Depends</span></span> | <span data-ttu-id="7fba8-212">Se o item de dados estiver contido em um tipo de controle [DataGrid](uiauto-supportdatagridcontroltype.md) que tenha um elemento Header, ele deverá dar suporte ao padrão de controle [TableItem](uiauto-implementingtableitem.md) .</span><span class="sxs-lookup"><span data-stu-id="7fba8-212">If the data item is contained within a [DataGrid](uiauto-supportdatagridcontroltype.md) control type that has a header element, it should support the [TableItem](uiauto-implementingtableitem.md) control pattern.</span></span> |
| [<span data-ttu-id="7fba8-213">**IToggleProvider**</span><span class="sxs-lookup"><span data-stu-id="7fba8-213">**IToggleProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                 | <span data-ttu-id="7fba8-214">Depende</span><span class="sxs-lookup"><span data-stu-id="7fba8-214">Depends</span></span> | <span data-ttu-id="7fba8-215">Se o item de dados contiver um estado que possa ser alternado por meio do, ele deve dar suporte ao padrão de controle de [alternância](uiauto-implementingtoggle.md) .</span><span class="sxs-lookup"><span data-stu-id="7fba8-215">If the data item contains a state that can be cycled through, it should support the [Toggle](uiauto-implementingtoggle.md) control pattern.</span></span>                                                                          |
| [<span data-ttu-id="7fba8-216">**IValueProvider**</span><span class="sxs-lookup"><span data-stu-id="7fba8-216">**IValueProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)                   | <span data-ttu-id="7fba8-217">Depende</span><span class="sxs-lookup"><span data-stu-id="7fba8-217">Depends</span></span> | <span data-ttu-id="7fba8-218">Se o texto principal do item de dados for editável, o padrão de controle de [valor](uiauto-implementingvalue.md) deverá ser suportado.</span><span class="sxs-lookup"><span data-stu-id="7fba8-218">If the data item's primary text is editable, the [Value](uiauto-implementingvalue.md) control pattern must be supported.</span></span>                                                                                             |



 

## <a name="working-with-dataitems-in-large-lists"></a><span data-ttu-id="7fba8-219">Trabalhando com dataItems em listas grandes</span><span class="sxs-lookup"><span data-stu-id="7fba8-219">Working with DataItems in Large Lists</span></span>

<span data-ttu-id="7fba8-220">Como as listas grandes geralmente são virtualizadas em estruturas de interface do usuário para auxiliar no desempenho, um cliente de automação de interface do usuário não pode usar o recurso de consulta de automação da interface do usuário para pesquisar o conteúdo da árvore completa da mesma maneira que pode em outros contêineres de item.</span><span class="sxs-lookup"><span data-stu-id="7fba8-220">Because large lists are often virtualized within UI frameworks to assist in performance, a UI Automation client cannot use the UI Automation query feature to search the contents of the full tree in the same way that it can in other item containers.</span></span> <span data-ttu-id="7fba8-221">Um cliente deve rolar o item para a exibição (ou expandir o controle para mostrar todas as opções disponíveis) antes de acessar o conjunto completo de informações do item de dados.</span><span class="sxs-lookup"><span data-stu-id="7fba8-221">A client should scroll the item into view (or expand the control to show all available options) prior to accessing the full set of information from the data item.</span></span>

<span data-ttu-id="7fba8-222">Ao chamar [**SetFocus**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-setfocus) no elemento de automação da interface do usuário para o item de dados, o Microsoft Windows Explorer retorna com êxito e faz com que o foco seja definido como o controle de edição dentro da subárvore do item de dados.</span><span class="sxs-lookup"><span data-stu-id="7fba8-222">When calling [**SetFocus**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-setfocus) on the UI Automation element for the data item, Microsoft Windows Explorer returns successfully and causes focus to be set to the Edit control within the data item subtree.</span></span>

## <a name="required-events"></a><span data-ttu-id="7fba8-223">Eventos necessários</span><span class="sxs-lookup"><span data-stu-id="7fba8-223">Required Events</span></span>

<span data-ttu-id="7fba8-224">A tabela a seguir lista os eventos de automação da interface do usuário aos quais os controles de item de dados devem dar suporte.</span><span class="sxs-lookup"><span data-stu-id="7fba8-224">The following table lists the UI Automation events that data item controls are required to support.</span></span> <span data-ttu-id="7fba8-225">Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="7fba8-225">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="7fba8-226">Evento de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="7fba8-226">UI Automation Event</span></span>                                                                                                                                                | <span data-ttu-id="7fba8-227">Observações</span><span class="sxs-lookup"><span data-stu-id="7fba8-227">Notes</span></span>                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7fba8-228">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="7fba8-228">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| <span data-ttu-id="7fba8-229">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="7fba8-229">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                              |                                                                                                                                  |
| <span data-ttu-id="7fba8-230">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ExpandCollapseExpandCollapseStatePropertyId.</span><span class="sxs-lookup"><span data-stu-id="7fba8-230">[**UIA\_ExpandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="7fba8-231">Se o controle der suporte ao padrão de controle [ExpandCollapse](uiauto-implementingexpandcollapse.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="7fba8-231">If the control supports the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern, it must support this event.</span></span> |
| [<span data-ttu-id="7fba8-232">**UIA \_ invocar \_ InvokedEventId**</span><span class="sxs-lookup"><span data-stu-id="7fba8-232">**UIA\_Invoke\_InvokedEventId**</span></span>](uiauto-event-ids.md)                                                                                  | <span data-ttu-id="7fba8-233">Se o controle der suporte ao padrão de controle [Invoke](uiauto-implementinginvoke.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="7fba8-233">If the control supports the [Invoke](uiauto-implementinginvoke.md) control pattern, it must support this event.</span></span>                 |
| <span data-ttu-id="7fba8-234">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="7fba8-234">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                              | <span data-ttu-id="7fba8-235">Se o controle oferecer suporte à propriedade [**IsEnabled**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="7fba8-235">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>         |
| <span data-ttu-id="7fba8-236">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="7fba8-236">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                          | <span data-ttu-id="7fba8-237">Se o controle oferecer suporte à propriedade [**IsOffscreen**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="7fba8-237">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>       |
| <span data-ttu-id="7fba8-238">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade ItemStatusPropertyId.</span><span class="sxs-lookup"><span data-stu-id="7fba8-238">[**UIA\_ItemStatusPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                            | <span data-ttu-id="7fba8-239">Se o controle der suporte [**à propriedade ItemProperty**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="7fba8-239">If the control supports the [**ItemStatus**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>        |
| <span data-ttu-id="7fba8-240">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade NamePropertyId.</span><span class="sxs-lookup"><span data-stu-id="7fba8-240">[**UIA\_NamePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                                        |                                                                                                                                  |
| [<span data-ttu-id="7fba8-241">**UIA \_ SelectionItem \_ ElementAddedToSelectionEventId**</span><span class="sxs-lookup"><span data-stu-id="7fba8-241">**UIA\_SelectionItem\_ElementAddedToSelectionEventId**</span></span>](uiauto-event-ids.md)                                    | <span data-ttu-id="7fba8-242">Se o controle der suporte ao padrão de controle [SelectionItem](uiauto-implementingselectionitem.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="7fba8-242">If the control supports the [SelectionItem](uiauto-implementingselectionitem.md) control pattern, it must support this event.</span></span>   |
| [<span data-ttu-id="7fba8-243">**UIA \_ SelectionItem \_ ElementRemovedFromSelectionEventId**</span><span class="sxs-lookup"><span data-stu-id="7fba8-243">**UIA\_SelectionItem\_ElementRemovedFromSelectionEventId**</span></span>](uiauto-event-ids.md)                            | <span data-ttu-id="7fba8-244">Se o controle der suporte ao padrão de controle [SelectionItem](uiauto-implementingselectionitem.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="7fba8-244">If the control supports the [SelectionItem](uiauto-implementingselectionitem.md) control pattern, it must support this event.</span></span>   |
| [<span data-ttu-id="7fba8-245">**UIA \_ SelectionItem \_ ElementSelectedEventId**</span><span class="sxs-lookup"><span data-stu-id="7fba8-245">**UIA\_SelectionItem\_ElementSelectedEventId**</span></span>](uiauto-event-ids.md)                                                    | <span data-ttu-id="7fba8-246">Se o controle der suporte ao padrão de controle [SelectionItem](uiauto-implementingselectionitem.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="7fba8-246">If the control supports the [SelectionItem](uiauto-implementingselectionitem.md) control pattern, it must support this event.</span></span>   |
| [<span data-ttu-id="7fba8-247">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="7fba8-247">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                               |                                                                                                                                  |
| <span data-ttu-id="7fba8-248">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ToggleToggleStatePropertyId.</span><span class="sxs-lookup"><span data-stu-id="7fba8-248">[**UIA\_ToggleToggleStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>                                 | <span data-ttu-id="7fba8-249">Se o controle der suporte ao padrão de controle [Toggle](uiauto-implementingtoggle.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="7fba8-249">If the control supports the [Toggle](uiauto-implementingtoggle.md) control pattern, it must support this event.</span></span>                 |
| <span data-ttu-id="7fba8-250">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ValueValuePropertyId.</span><span class="sxs-lookup"><span data-stu-id="7fba8-250">[**UIA\_ValueValuePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>                                               | <span data-ttu-id="7fba8-251">Se o controle der suporte ao padrão de controle de [valor](uiauto-implementingvalue.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="7fba8-251">If the control supports the [Value](uiauto-implementingvalue.md) control pattern, it must support this event.</span></span>                   |



 

## <a name="dataitem-control-type-example"></a><span data-ttu-id="7fba8-252">Exemplo de tipo de controle DataItem</span><span class="sxs-lookup"><span data-stu-id="7fba8-252">DataItem Control Type Example</span></span>

<span data-ttu-id="7fba8-253">A imagem a seguir ilustra um tipo de controle DataItem em um controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="7fba8-253">The following image illustrates a DataItem control type in a list-view control.</span></span>

![captura de tela do controle de exibição de lista com o tipo de controle DataItem](images/dataitemxmpl.jpg)

<span data-ttu-id="7fba8-255">A exibição de controle e a exibição de conteúdo da árvore de automação da interface do usuário que pertencem ao controle de item de dados são exibidas abaixo.</span><span class="sxs-lookup"><span data-stu-id="7fba8-255">The control view and the content view of the UI Automation tree that pertains to the data item control is displayed below.</span></span> <span data-ttu-id="7fba8-256">Os padrões de controle para cada elemento de automação são mostrados entre parênteses.</span><span class="sxs-lookup"><span data-stu-id="7fba8-256">The control patterns for each automation element are shown in parentheses.</span></span> <span data-ttu-id="7fba8-257">O **grupo** "contoso" também faz parte da grade do controle de host de grade de dados.</span><span class="sxs-lookup"><span data-stu-id="7fba8-257">The **Group** "Contoso" is also part of the grid of the data grid host control.</span></span> <span data-ttu-id="7fba8-258">Para obter um exemplo de uma estrutura de grade de nível superior, consulte [tipo de controle DataGrid](uiauto-supportdatagridcontroltype.md).</span><span class="sxs-lookup"><span data-stu-id="7fba8-258">For an example of a higher level grid structure, see [DataGrid Control Type](uiauto-supportdatagridcontroltype.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7fba8-259">Árvore de automação da interface do usuário – exibição de controle</span><span class="sxs-lookup"><span data-stu-id="7fba8-259">UI Automation Tree - Control View</span></span></th>
<th><span data-ttu-id="7fba8-260">Árvore de automação da interface do usuário – exibição de conteúdo</span><span class="sxs-lookup"><span data-stu-id="7fba8-260">UI Automation Tree - Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="7fba8-261">Grupo &quot; Contoso &quot; (tabela, grade)</span><span class="sxs-lookup"><span data-stu-id="7fba8-261">Group &quot;Contoso&quot; (Table, Grid)</span></span>
<ul>
<li><span data-ttu-id="7fba8-262">&quot;Receivable.docde contas &quot; do DataItem (TableItem, GridItem, SelectionItem, Invoke)</span><span class="sxs-lookup"><span data-stu-id="7fba8-262">DataItem &quot;Accounts Receivable.doc&quot; (TableItem, GridItem, SelectionItem, Invoke)</span></span>
<ul>
<li><span data-ttu-id="7fba8-263">Receivable.docde contas de imagem &quot;&quot;</span><span class="sxs-lookup"><span data-stu-id="7fba8-263">Image &quot;Accounts Receivable.doc&quot;</span></span></li>
<li><span data-ttu-id="7fba8-264">Editar &quot; nome &quot; (TableItem, GridItem, valor &quot; contas Receivable.doc&quot; )</span><span class="sxs-lookup"><span data-stu-id="7fba8-264">Edit &quot;Name&quot; (TableItem, GridItem, Value &quot;Accounts Receivable.doc&quot;)</span></span></li>
<li><span data-ttu-id="7fba8-265">Editar &quot; data de modificação &quot; (TableItem, GridItem, valor &quot; 8/25/2006 3:29 PM &quot; )</span><span class="sxs-lookup"><span data-stu-id="7fba8-265">Edit &quot;Date modified&quot; (TableItem, GridItem, Value &quot;8/25/2006 3:29 PM&quot;)</span></span></li>
<li><span data-ttu-id="7fba8-266">Editar &quot; tamanho &quot; (GridItem, TableItem, valor &quot; 11,0 KB &quot; )</span><span class="sxs-lookup"><span data-stu-id="7fba8-266">Edit &quot;Size&quot; (GridItem, TableItem, Value &quot;11.0 KB&quot;)</span></span></li>
</ul></li>
<li><span data-ttu-id="7fba8-267">&quot;Payable.docde contas &quot; do DataItem (TableItem, GridItem, SelectionItem, Invoke)</span><span class="sxs-lookup"><span data-stu-id="7fba8-267">DataItem &quot;Accounts Payable.doc&quot; (TableItem, GridItem, SelectionItem, Invoke)</span></span>
<ul>
<li><span data-ttu-id="7fba8-268">...</span><span class="sxs-lookup"><span data-stu-id="7fba8-268">...</span></span></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="7fba8-269">Grupo &quot; Contoso &quot; (tabela, grade)</span><span class="sxs-lookup"><span data-stu-id="7fba8-269">Group &quot;Contoso&quot; (Table, Grid)</span></span>
<ul>
<li><span data-ttu-id="7fba8-270">&quot;Receivable.docde contas &quot; do DataItem (TableItem, GridItem, SelectionItem, Invoke)</span><span class="sxs-lookup"><span data-stu-id="7fba8-270">DataItem &quot;Accounts Receivable.doc&quot; (TableItem, GridItem, SelectionItem, Invoke)</span></span>
<ul>
<li><span data-ttu-id="7fba8-271">Receivable.docde contas de imagem &quot;&quot;</span><span class="sxs-lookup"><span data-stu-id="7fba8-271">Image &quot;Accounts Receivable.doc&quot;</span></span></li>
<li><span data-ttu-id="7fba8-272">Editar &quot; nome &quot; (TableItem, GridItem, valor &quot; contas Receivable.doc&quot; )</span><span class="sxs-lookup"><span data-stu-id="7fba8-272">Edit &quot;Name&quot; (TableItem, GridItem, Value &quot;Accounts Receivable.doc&quot;)</span></span></li>
<li><span data-ttu-id="7fba8-273">Editar &quot; data de modificação &quot; (TableItem, GridItem, valor &quot; 8/25/2006 3:29 PM &quot; )</span><span class="sxs-lookup"><span data-stu-id="7fba8-273">Edit &quot;Date modified&quot; (TableItem, GridItem, Value &quot;8/25/2006 3:29 PM&quot;)</span></span></li>
<li><span data-ttu-id="7fba8-274">Editar &quot; tamanho &quot; (GridItem, TableItem, valor &quot; 11,0 KB &quot; )</span><span class="sxs-lookup"><span data-stu-id="7fba8-274">Edit &quot;Size&quot; (GridItem, TableItem, Value &quot;11.0 KB&quot;)</span></span></li>
</ul></li>
<li><span data-ttu-id="7fba8-275">&quot;Payable.docde contas &quot; do DataItem (TableItem, GridItem, SelectionItem, Invoke)</span><span class="sxs-lookup"><span data-stu-id="7fba8-275">DataItem &quot;Accounts Payable.doc&quot; (TableItem, GridItem, SelectionItem, Invoke)</span></span>
<ul>
<li><span data-ttu-id="7fba8-276">...</span><span class="sxs-lookup"><span data-stu-id="7fba8-276">...</span></span></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="7fba8-277">Se uma grade representar uma lista de itens selecionáveis, os elementos de interface do usuário selecionáveis correspondentes poderão ser expostos com o tipo de controle [ListItem](uiauto-supportlistitemcontroltype.md) em vez do tipo de controle DataItem.</span><span class="sxs-lookup"><span data-stu-id="7fba8-277">If a grid represents a list of selectable items, the corresponding selectable UI elements can be exposed with the [ListItem](uiauto-supportlistitemcontroltype.md) control type instead of the DataItem control type.</span></span> <span data-ttu-id="7fba8-278">No exemplo anterior, os elementos **DataItem** ("accounts Receivable.doc" e "accounts Payable.doc") em **Group** ("contoso") podem ser aprimorados expondo-os como tipos de controle de ListItem porque esse tipo já dá suporte ao padrão de controle [SelectionItem](uiauto-implementingselectionitem.md) .</span><span class="sxs-lookup"><span data-stu-id="7fba8-278">In the preceding example, the **DataItem** elements ("Accounts Receivable.doc" and "Accounts Payable.doc") under **Group** ("Contoso") can be improved by exposing them as ListItem control types because that type already supports the [SelectionItem](uiauto-implementingselectionitem.md) control pattern.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7fba8-279">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7fba8-279">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="7fba8-280">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="7fba8-280">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7fba8-281">Visão Geral dos Tipos de Controle de Automação de Interface do Usuário</span><span class="sxs-lookup"><span data-stu-id="7fba8-281">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="7fba8-282">Visão geral de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="7fba8-282">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




