---
title: Tipo de controle de texto
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle de texto.
ms.assetid: 69a3b243-8ee5-48e4-a01e-c7ad69b9a3aa
keywords:
- Automação da interface do usuário, suporte para tipo de controle de texto
- Automação da interface do usuário, tipo de controle de texto
- Automação da interface do usuário, estrutura de árvore para tipo de controle de texto
- Automação da interface do usuário, propriedades para tipo de controle de texto
- Automação da interface do usuário, padrões de controle para tipo de controle de texto
- Automação da interface do usuário, eventos para tipo de controle de texto
- estruturas de árvore, tipo de controle de texto
- Propriedades, tipo de controle de texto
- padrões de controle, tipo de controle de texto
- eventos, tipo de controle de texto
- suporte para tipo de controle de texto
- tipo de controle Texto
- tipos de controle, estrutura de árvore para tipo de controle de texto
- tipos de controle, padrões de controle para tipo de controle de texto
- tipos de controle, suporte para texto
- tipos de controle, texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 902b3c7c523417abde2c60e1f8039ad9f2c322b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292464"
---
# <a name="text-control-type"></a><span data-ttu-id="f19b3-119">Tipo de controle de texto</span><span class="sxs-lookup"><span data-stu-id="f19b3-119">Text Control Type</span></span>

<span data-ttu-id="f19b3-120">Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle de **texto** .</span><span class="sxs-lookup"><span data-stu-id="f19b3-120">This topic provides information about Microsoft UI Automation support for the **Text** control type.</span></span>

<span data-ttu-id="f19b3-121">Um controle de texto é um item básico da interface do usuário que representa uma parte do texto na tela.</span><span class="sxs-lookup"><span data-stu-id="f19b3-121">A text control is a basic user interface item that represents a piece of text on the screen.</span></span>

<span data-ttu-id="f19b3-122">As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle de **texto** .</span><span class="sxs-lookup"><span data-stu-id="f19b3-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Text** control type.</span></span> <span data-ttu-id="f19b3-123">Os requisitos de automação da interface do usuário se aplicam a todos os controles de árvore em que a estrutura/plataforma da interface do usuário integra o suporte à automação da interface do usuário para tipos de controle</span><span class="sxs-lookup"><span data-stu-id="f19b3-123">The UI Automation requirements apply to all tree controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="f19b3-124">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="f19b3-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="f19b3-125">Estrutura de árvore típica</span><span class="sxs-lookup"><span data-stu-id="f19b3-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="f19b3-126">Propriedades relevantes</span><span class="sxs-lookup"><span data-stu-id="f19b3-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="f19b3-127">Padrões de controle necessários</span><span class="sxs-lookup"><span data-stu-id="f19b3-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="f19b3-128">Eventos necessários</span><span class="sxs-lookup"><span data-stu-id="f19b3-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="f19b3-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f19b3-129">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="f19b3-130">Estrutura de árvore típica</span><span class="sxs-lookup"><span data-stu-id="f19b3-130">Typical Tree Structure</span></span>

<span data-ttu-id="f19b3-131">A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence a controles de texto e descreve o que pode ser contido em cada exibição.</span><span class="sxs-lookup"><span data-stu-id="f19b3-131">The following table depicts a typical control and content view of the UI Automation tree that pertains to text controls and describes what can be contained in each view.</span></span> <span data-ttu-id="f19b3-132">Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="f19b3-132">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f19b3-133">Exibição de controle</span><span class="sxs-lookup"><span data-stu-id="f19b3-133">Control View</span></span></th>
<th><span data-ttu-id="f19b3-134">Exibição de conteúdo</span><span class="sxs-lookup"><span data-stu-id="f19b3-134">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="f19b3-135">Texto</span><span class="sxs-lookup"><span data-stu-id="f19b3-135">Text</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="f19b3-136">Texto (se o conteúdo)</span><span class="sxs-lookup"><span data-stu-id="f19b3-136">Text (if content)</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="f19b3-137">Um controle de texto pode ser usado sozinho como um rótulo ou como texto estático em um formulário.</span><span class="sxs-lookup"><span data-stu-id="f19b3-137">A text control can be used alone as a label or as static text on a form.</span></span> <span data-ttu-id="f19b3-138">Ele também pode estar contido na estrutura de um dos seguintes itens:</span><span class="sxs-lookup"><span data-stu-id="f19b3-138">It can also be contained within the structure of one of the following items:</span></span>

-   [<span data-ttu-id="f19b3-139">DataItem</span><span class="sxs-lookup"><span data-stu-id="f19b3-139">DataItem</span></span>](uiauto-supportdataitemcontroltype.md)
-   [<span data-ttu-id="f19b3-140">Item</span><span class="sxs-lookup"><span data-stu-id="f19b3-140">ListItem</span></span>](uiauto-supportlistitemcontroltype.md)
-   [<span data-ttu-id="f19b3-141">TreeItem</span><span class="sxs-lookup"><span data-stu-id="f19b3-141">TreeItem</span></span>](uiauto-supporttreeitemcontroltype.md)

<span data-ttu-id="f19b3-142">Os controles de texto podem não aparecer na exibição de conteúdo da árvore de automação da interface do usuário porque o texto geralmente é exibido por meio da propriedade **Name** de outro controle.</span><span class="sxs-lookup"><span data-stu-id="f19b3-142">Text controls might not appear in the content view of the UI Automation tree because text is often displayed through the **Name** property of another control.</span></span> <span data-ttu-id="f19b3-143">Por exemplo, o texto usado para rotular um controle de caixa de combinação é exposto por meio da propriedade **Name** do controle.</span><span class="sxs-lookup"><span data-stu-id="f19b3-143">For example, the text used to label a combo box control is exposed through the control's **Name** property.</span></span> <span data-ttu-id="f19b3-144">Como o controle de caixa de combinação está na exibição de conteúdo da árvore de automação da interface do usuário, o controle de texto não precisa estar lá.</span><span class="sxs-lookup"><span data-stu-id="f19b3-144">Because the combo box control is in the content view of the UI Automation tree, the text control need not be there.</span></span> <span data-ttu-id="f19b3-145">Os controles de texto podem ter filhos na exibição de conteúdo se houver um objeto inserido, como um hiperlink.</span><span class="sxs-lookup"><span data-stu-id="f19b3-145">Text controls may have children in the content view if there is an embedded object such as a hyperlink.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="f19b3-146">Propriedades relevantes</span><span class="sxs-lookup"><span data-stu-id="f19b3-146">Relevant Properties</span></span>

<span data-ttu-id="f19b3-147">A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para os controles de texto.</span><span class="sxs-lookup"><span data-stu-id="f19b3-147">The following table lists the UI Automation properties whose value or definition is especially relevant to the text controls.</span></span> <span data-ttu-id="f19b3-148">Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="f19b3-148">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="f19b3-149">Propriedade de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="f19b3-149">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="f19b3-150">Valor</span><span class="sxs-lookup"><span data-stu-id="f19b3-150">Value</span></span>      | <span data-ttu-id="f19b3-151">Observações</span><span class="sxs-lookup"><span data-stu-id="f19b3-151">Notes</span></span>                                                                                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f19b3-152">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="f19b3-152">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="f19b3-153">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="f19b3-153">See notes.</span></span> | <span data-ttu-id="f19b3-154">O valor dessa propriedade deve ser exclusivo entre todos os elementos de mesmo nível na exibição bruta da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="f19b3-154">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                                                                                                                                        |
| [<span data-ttu-id="f19b3-155">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="f19b3-155">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="f19b3-156">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="f19b3-156">See notes.</span></span> | <span data-ttu-id="f19b3-157">O retângulo mais externo que contém o controle inteiro.</span><span class="sxs-lookup"><span data-stu-id="f19b3-157">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="f19b3-158">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="f19b3-158">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="f19b3-159">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="f19b3-159">See notes.</span></span> | <span data-ttu-id="f19b3-160">Com suporte se houver um retângulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="f19b3-160">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="f19b3-161">Se nem todos os pontos dentro do retângulo delimitador forem clicáveis, o elemento executará testes de clique especializados, substituirá e fornecerá um ponto clicável.</span><span class="sxs-lookup"><span data-stu-id="f19b3-161">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span>                                                                                                                                                |
| [<span data-ttu-id="f19b3-162">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="f19b3-162">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="f19b3-163">**Text**</span><span class="sxs-lookup"><span data-stu-id="f19b3-163">**Text**</span></span>   |                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="f19b3-164">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="f19b3-164">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="f19b3-165">Depende</span><span class="sxs-lookup"><span data-stu-id="f19b3-165">Depends</span></span>    | <span data-ttu-id="f19b3-166">O controle de texto será Content se ele contiver informações não expostas na propriedade Name de outro controle.</span><span class="sxs-lookup"><span data-stu-id="f19b3-166">The text control is content if it contains information not exposed in another control's Name property.</span></span>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="f19b3-167">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="f19b3-167">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="f19b3-168">TRUE</span><span class="sxs-lookup"><span data-stu-id="f19b3-168">TRUE</span></span>       | <span data-ttu-id="f19b3-169">O controle de texto sempre deve ser um controle.</span><span class="sxs-lookup"><span data-stu-id="f19b3-169">The text control must always be a control.</span></span>                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="f19b3-170">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="f19b3-170">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="f19b3-171">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="f19b3-171">See notes.</span></span> | <span data-ttu-id="f19b3-172">Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="f19b3-172">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="f19b3-173">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="f19b3-173">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="f19b3-174">NULO</span><span class="sxs-lookup"><span data-stu-id="f19b3-174">NULL</span></span>       | <span data-ttu-id="f19b3-175">Os controles de texto não têm um rótulo de texto estático.</span><span class="sxs-lookup"><span data-stu-id="f19b3-175">Text controls do not have a static text label.</span></span>                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="f19b3-176">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="f19b3-176">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="f19b3-177">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="f19b3-177">See notes.</span></span> | <span data-ttu-id="f19b3-178">Cadeia de caracteres localizada correspondente ao tipo de controle de **texto** .</span><span class="sxs-lookup"><span data-stu-id="f19b3-178">Localized string corresponding to the **Text** control type.</span></span> <span data-ttu-id="f19b3-179">O valor padrão é "text" para en-US ou inglês (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="f19b3-179">The default value is "text" for en-US or English (United States).</span></span>                                                                                                                                                                                                                      |
| [<span data-ttu-id="f19b3-180">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="f19b3-180">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="f19b3-181">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="f19b3-181">See notes.</span></span> | <span data-ttu-id="f19b3-182">O nome de um controle de texto pode ser o texto que ele exibe.</span><span class="sxs-lookup"><span data-stu-id="f19b3-182">The name of a text control can be the text that it displays.</span></span> <span data-ttu-id="f19b3-183">No entanto, se o controle também oferecer suporte ao padrão de [texto](uiauto-implementingtextandtextrange.md) e o texto for extensivo, não use o conteúdo de texto completo como o valor do **nome** .</span><span class="sxs-lookup"><span data-stu-id="f19b3-183">However, if the control also supports the [Text](uiauto-implementingtextandtextrange.md) pattern, and the text is extensive, don't use the full text content as the **Name** value.</span></span> <span data-ttu-id="f19b3-184">Em vez disso, forneça um valor de **nome** que seja menor, derivado de outras propriedades do seu controle.</span><span class="sxs-lookup"><span data-stu-id="f19b3-184">Instead, provide a **Name** value that is shorter, derived from other properties of your control.</span></span> |



 

## <a name="required-control-patterns"></a><span data-ttu-id="f19b3-185">Padrões de controle necessários</span><span class="sxs-lookup"><span data-stu-id="f19b3-185">Required Control Patterns</span></span>

<span data-ttu-id="f19b3-186">A tabela a seguir lista os padrões de controle de automação da interface do usuário necessários para serem suportados por controles de texto.</span><span class="sxs-lookup"><span data-stu-id="f19b3-186">The following table lists the UI Automation control patterns required to be supported by text controls.</span></span> <span data-ttu-id="f19b3-187">Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="f19b3-187">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="f19b3-188">Padrão de controle</span><span class="sxs-lookup"><span data-stu-id="f19b3-188">Control Pattern</span></span>                                         | <span data-ttu-id="f19b3-189">Suporte</span><span class="sxs-lookup"><span data-stu-id="f19b3-189">Support</span></span> | <span data-ttu-id="f19b3-190">Observações</span><span class="sxs-lookup"><span data-stu-id="f19b3-190">Notes</span></span>                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f19b3-191">**IGridItemProvider**</span><span class="sxs-lookup"><span data-stu-id="f19b3-191">**IGridItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)   | <span data-ttu-id="f19b3-192">Depende</span><span class="sxs-lookup"><span data-stu-id="f19b3-192">Depends</span></span> | <span data-ttu-id="f19b3-193">Se o controle de texto estiver contido em um controle de tabela, o padrão de controle [GridItem](uiauto-implementinggriditem.md) deverá ser suportado.</span><span class="sxs-lookup"><span data-stu-id="f19b3-193">If the text control is contained within a table control, the [GridItem](uiauto-implementinggriditem.md) control pattern must be supported.</span></span>                                                                                                                            |
| [<span data-ttu-id="f19b3-194">**ITableItemProvider**</span><span class="sxs-lookup"><span data-stu-id="f19b3-194">**ITableItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) | <span data-ttu-id="f19b3-195">Depende</span><span class="sxs-lookup"><span data-stu-id="f19b3-195">Depends</span></span> | <span data-ttu-id="f19b3-196">Se o controle de texto estiver contido em um controle de tabela, o padrão de controle [TableItem](uiauto-implementingtableitem.md) deverá ser suportado.</span><span class="sxs-lookup"><span data-stu-id="f19b3-196">If the text control is contained within a table control, the [TableItem](uiauto-implementingtableitem.md) control pattern must be supported.</span></span>                                                                                                                          |
| [<span data-ttu-id="f19b3-197">**ITextProvider**</span><span class="sxs-lookup"><span data-stu-id="f19b3-197">**ITextProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider)           | <span data-ttu-id="f19b3-198">Depende</span><span class="sxs-lookup"><span data-stu-id="f19b3-198">Depends</span></span> | <span data-ttu-id="f19b3-199">O texto deve dar suporte ao padrão de controle de [texto](uiauto-implementingtextandtextrange.md) para melhor acessibilidade; no entanto, isso não é necessário.</span><span class="sxs-lookup"><span data-stu-id="f19b3-199">Text should support the [Text](uiauto-implementingtextandtextrange.md) control pattern for better accessibility; however, it is not required.</span></span> <span data-ttu-id="f19b3-200">O padrão de controle de texto é útil quando o texto tem estilo e atributos avançados (por exemplo, cor, negrito e itálico).</span><span class="sxs-lookup"><span data-stu-id="f19b3-200">The Text control pattern is useful when the text has rich style and attributes (for example, color, bold, and italics).</span></span> |
| [<span data-ttu-id="f19b3-201">**IValueProvider**</span><span class="sxs-lookup"><span data-stu-id="f19b3-201">**IValueProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)         | <span data-ttu-id="f19b3-202">Nunca</span><span class="sxs-lookup"><span data-stu-id="f19b3-202">Never</span></span>   | <span data-ttu-id="f19b3-203">Um controle de texto nunca dá suporte ao padrão de controle de [valor](uiauto-implementingvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="f19b3-203">A text control never supports the [Value](uiauto-implementingvalue.md) control pattern.</span></span> <span data-ttu-id="f19b3-204">Se o texto for editável, ele será o tipo de controle de [edição](uiauto-supporteditcontroltype.md) .</span><span class="sxs-lookup"><span data-stu-id="f19b3-204">If the text is editable, it is the [Edit](uiauto-supporteditcontroltype.md) control type.</span></span>                                                                                    |



 

## <a name="required-events"></a><span data-ttu-id="f19b3-205">Eventos necessários</span><span class="sxs-lookup"><span data-stu-id="f19b3-205">Required Events</span></span>

<span data-ttu-id="f19b3-206">A tabela a seguir lista os eventos de automação da interface do usuário aos quais os controles de texto são necessários para dar suporte.</span><span class="sxs-lookup"><span data-stu-id="f19b3-206">The following table lists the UI Automation events that text controls are required to support.</span></span> <span data-ttu-id="f19b3-207">Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="f19b3-207">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="f19b3-208">Evento de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="f19b3-208">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="f19b3-209">Observações</span><span class="sxs-lookup"><span data-stu-id="f19b3-209">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f19b3-210">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="f19b3-210">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="f19b3-211">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="f19b3-211">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="f19b3-212">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="f19b3-212">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="f19b3-213">Se o controle oferecer suporte à propriedade [**IsEnabled**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="f19b3-213">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="f19b3-214">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="f19b3-214">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="f19b3-215">Se o controle oferecer suporte à propriedade [**IsOffscreen**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="f19b3-215">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| <span data-ttu-id="f19b3-216">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade NamePropertyId.</span><span class="sxs-lookup"><span data-stu-id="f19b3-216">[**UIA\_NamePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                           |                                                                                                                            |
| [<span data-ttu-id="f19b3-217">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="f19b3-217">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [<span data-ttu-id="f19b3-218">**\_TextChangedEventId de texto UIA \_**</span><span class="sxs-lookup"><span data-stu-id="f19b3-218">**UIA\_Text\_TextChangedEventId**</span></span>](uiauto-event-ids.md)                                                 | <span data-ttu-id="f19b3-219">Se o controle der suporte ao padrão de controle de [texto](uiauto-implementingtextandtextrange.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="f19b3-219">If the control supports the [Text](uiauto-implementingtextandtextrange.md) control pattern, it must support this event.</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="f19b3-220">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f19b3-220">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="f19b3-221">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="f19b3-221">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f19b3-222">Visão Geral dos Tipos de Controle de Automação de Interface do Usuário</span><span class="sxs-lookup"><span data-stu-id="f19b3-222">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="f19b3-223">Visão geral de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="f19b3-223">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




