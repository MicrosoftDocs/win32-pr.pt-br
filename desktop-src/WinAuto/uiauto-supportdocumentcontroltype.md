---
title: Tipo de controle de documento
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle de documento.
ms.assetid: 62565f16-f0d6-42ff-bc36-897a2618c867
keywords:
- Automação da interface do usuário, suporte para tipo de controle de documento
- Automação da interface do usuário, tipo de controle de documento
- Automação da interface do usuário, estrutura de árvore para tipo de controle de documento
- Automação da interface do usuário, propriedades para tipo de controle de documento
- Automação da interface do usuário, padrões de controle para tipo de controle de documento
- Automação da interface do usuário, eventos para tipo de controle de documento
- estruturas de árvore, tipo de controle de documento
- Propriedades, tipo de controle de documento
- padrões de controle, tipo de controle de documento
- eventos, tipo de controle de documento
- suporte para tipo de controle de documento
- tipo de controle Documento
- tipos de controle, estrutura de árvore para tipo de controle de documento
- tipos de controle, padrões de controle para tipo de controle de documento
- tipos de controle, suporte para documento
- tipos de controle, documento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46ca481df812e3321da7bb4bbb39bdcb5628fb98
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005412"
---
# <a name="document-control-type"></a><span data-ttu-id="57c12-119">Tipo de controle de documento</span><span class="sxs-lookup"><span data-stu-id="57c12-119">Document Control Type</span></span>

<span data-ttu-id="57c12-120">Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle de **documento** .</span><span class="sxs-lookup"><span data-stu-id="57c12-120">This topic provides information about Microsoft UI Automation support for the **Document** control type.</span></span>

<span data-ttu-id="57c12-121">Os controles de documento permitem que um usuário exiba e manipule várias páginas de texto.</span><span class="sxs-lookup"><span data-stu-id="57c12-121">Document controls let a user view and manipulate multiple pages of text.</span></span> <span data-ttu-id="57c12-122">Ao contrário dos controles de edição que oferecem suporte apenas a uma linha simples de texto não formatado, os controles de documento podem hospedar texto com estilo rico e formatado</span><span class="sxs-lookup"><span data-stu-id="57c12-122">Unlike edit controls which only support a simple line of unformatted text, document controls can host text that is richly styled and formatted</span></span>

<span data-ttu-id="57c12-123">As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle de **documento** .</span><span class="sxs-lookup"><span data-stu-id="57c12-123">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Document** control type.</span></span> <span data-ttu-id="57c12-124">Os requisitos de automação da interface do usuário se aplicam a todos os controles de documento onde a estrutura/plataforma da interface do usuário integra o suporte à automação da interface do usuário para tipos de controle</span><span class="sxs-lookup"><span data-stu-id="57c12-124">The UI Automation requirements apply to all document controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="57c12-125">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="57c12-125">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="57c12-126">Estrutura de árvore típica</span><span class="sxs-lookup"><span data-stu-id="57c12-126">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="57c12-127">Propriedades relevantes</span><span class="sxs-lookup"><span data-stu-id="57c12-127">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="57c12-128">Padrões de controle necessários</span><span class="sxs-lookup"><span data-stu-id="57c12-128">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="57c12-129">Eventos necessários</span><span class="sxs-lookup"><span data-stu-id="57c12-129">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="57c12-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="57c12-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="57c12-131">Estrutura de árvore típica</span><span class="sxs-lookup"><span data-stu-id="57c12-131">Typical Tree Structure</span></span>

<span data-ttu-id="57c12-132">A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence a controles de documento e descreve o que pode ser contido em cada exibição.</span><span class="sxs-lookup"><span data-stu-id="57c12-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to document controls and describes what can be contained in each view.</span></span> <span data-ttu-id="57c12-133">Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="57c12-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="57c12-134">Exibição de controle</span><span class="sxs-lookup"><span data-stu-id="57c12-134">Control View</span></span></th>
<th><span data-ttu-id="57c12-135">Exibição de conteúdo</span><span class="sxs-lookup"><span data-stu-id="57c12-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="57c12-136">Documento</span><span class="sxs-lookup"><span data-stu-id="57c12-136">Document</span></span>
<ul>
<li><span data-ttu-id="57c12-137">Varia</span><span class="sxs-lookup"><span data-stu-id="57c12-137">Varies</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="57c12-138">Documento</span><span class="sxs-lookup"><span data-stu-id="57c12-138">Document</span></span>
<ul>
<li><span data-ttu-id="57c12-139">Varia</span><span class="sxs-lookup"><span data-stu-id="57c12-139">Varies</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="57c12-140">Propriedades relevantes</span><span class="sxs-lookup"><span data-stu-id="57c12-140">Relevant Properties</span></span>

<span data-ttu-id="57c12-141">A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para os controles de documento.</span><span class="sxs-lookup"><span data-stu-id="57c12-141">The following table lists the UI Automation properties whose value or definition is especially relevant to document controls.</span></span> <span data-ttu-id="57c12-142">Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="57c12-142">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="57c12-143">Propriedade de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="57c12-143">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="57c12-144">Valor</span><span class="sxs-lookup"><span data-stu-id="57c12-144">Value</span></span>        | <span data-ttu-id="57c12-145">Observações</span><span class="sxs-lookup"><span data-stu-id="57c12-145">Notes</span></span>                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="57c12-146">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="57c12-146">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="57c12-147">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="57c12-147">See notes.</span></span>   | <span data-ttu-id="57c12-148">O valor dessa propriedade deve ser exclusivo entre todos os elementos de mesmo nível na exibição bruta da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="57c12-148">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                      |
| [<span data-ttu-id="57c12-149">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="57c12-149">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="57c12-150">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="57c12-150">See notes.</span></span>   | <span data-ttu-id="57c12-151">O retângulo mais externo que contém o controle inteiro.</span><span class="sxs-lookup"><span data-stu-id="57c12-151">The outermost rectangle that contains the whole control.</span></span>                                                                                          |
| [<span data-ttu-id="57c12-152">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="57c12-152">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="57c12-153">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="57c12-153">See notes.</span></span>   | <span data-ttu-id="57c12-154">O documento tem um ponto clicável que fará com que o documento de um de seus elementos no contêiner do documento tenha foco.</span><span class="sxs-lookup"><span data-stu-id="57c12-154">The document has a clickable point that will cause the document of one of its elements in the document container to have focus.</span></span>                   |
| [<span data-ttu-id="57c12-155">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="57c12-155">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="57c12-156">**Documento**</span><span class="sxs-lookup"><span data-stu-id="57c12-156">**Document**</span></span> |                                                                                                                                                   |
| [<span data-ttu-id="57c12-157">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="57c12-157">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="57c12-158">TRUE</span><span class="sxs-lookup"><span data-stu-id="57c12-158">TRUE</span></span>         | <span data-ttu-id="57c12-159">O controle de documento sempre é incluído na exibição de conteúdo da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="57c12-159">The document control is always included in the content view of the UI Automation tree.</span></span>                                                            |
| [<span data-ttu-id="57c12-160">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="57c12-160">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="57c12-161">TRUE</span><span class="sxs-lookup"><span data-stu-id="57c12-161">TRUE</span></span>         | <span data-ttu-id="57c12-162">O controle de documento sempre é incluído no modo de exibição de controle da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="57c12-162">The document control is always included in the control view of the UI Automation tree.</span></span>                                                            |
| [<span data-ttu-id="57c12-163">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="57c12-163">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="57c12-164">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="57c12-164">See notes.</span></span>   | <span data-ttu-id="57c12-165">Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="57c12-165">If the control can receive keyboard focus, it must support this property.</span></span>                                                                         |
| [<span data-ttu-id="57c12-166">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="57c12-166">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="57c12-167">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="57c12-167">See notes.</span></span>   | <span data-ttu-id="57c12-168">O valor dessa propriedade deve ser o rótulo do controle de documento.</span><span class="sxs-lookup"><span data-stu-id="57c12-168">The value of this property should be the label of the document control.</span></span> <span data-ttu-id="57c12-169">Normalmente, o título do documento é usado.</span><span class="sxs-lookup"><span data-stu-id="57c12-169">Typically, the title of the document is used.</span></span>                             |
| [<span data-ttu-id="57c12-170">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="57c12-170">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="57c12-171">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="57c12-171">See notes.</span></span>   | <span data-ttu-id="57c12-172">Cadeia de caracteres localizada correspondente ao tipo de controle de **documento** .</span><span class="sxs-lookup"><span data-stu-id="57c12-172">Localized string corresponding to the **Document** control type.</span></span> <span data-ttu-id="57c12-173">O valor padrão é "Document" para en-US ou inglês (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="57c12-173">The default value is "document" for en-US or English (United States).</span></span>            |
| [<span data-ttu-id="57c12-174">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="57c12-174">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="57c12-175">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="57c12-175">See notes.</span></span>   | <span data-ttu-id="57c12-176">O controle de documento normalmente obtém seu nome do nome de arquivo do qual ele está carregado.</span><span class="sxs-lookup"><span data-stu-id="57c12-176">The document control typically gets its name from the file name it is loaded from.</span></span> <span data-ttu-id="57c12-177">Isso é geralmente exibido em uma janela contendo um título de quadro.</span><span class="sxs-lookup"><span data-stu-id="57c12-177">This is often displayed in a containing window or frame title.</span></span> |



 

## <a name="required-control-patterns"></a><span data-ttu-id="57c12-178">Padrões de controle necessários</span><span class="sxs-lookup"><span data-stu-id="57c12-178">Required Control Patterns</span></span>

<span data-ttu-id="57c12-179">A tabela a seguir lista os padrões de controle de automação da interface do usuário necessários para serem suportados pelos controles de documento.</span><span class="sxs-lookup"><span data-stu-id="57c12-179">The following table lists the UI Automation control patterns required to be supported by document controls.</span></span> <span data-ttu-id="57c12-180">Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="57c12-180">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="57c12-181">Propriedade padrão de controle/padrão</span><span class="sxs-lookup"><span data-stu-id="57c12-181">Control Pattern/Pattern Property</span></span>                  | <span data-ttu-id="57c12-182">Suporte/valor</span><span class="sxs-lookup"><span data-stu-id="57c12-182">Support/Value</span></span> | <span data-ttu-id="57c12-183">Observações</span><span class="sxs-lookup"><span data-stu-id="57c12-183">Notes</span></span>                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="57c12-184">**IScrollProvider**</span><span class="sxs-lookup"><span data-stu-id="57c12-184">**IScrollProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider) | <span data-ttu-id="57c12-185">Depende</span><span class="sxs-lookup"><span data-stu-id="57c12-185">Depends</span></span>       | <span data-ttu-id="57c12-186">O controle de documento pode abranger maior do que aquele span do visor.</span><span class="sxs-lookup"><span data-stu-id="57c12-186">The document control can span larger than that span of the viewport.</span></span> <span data-ttu-id="57c12-187">O controle deve dar suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) se o conteúdo for rolável.</span><span class="sxs-lookup"><span data-stu-id="57c12-187">The control should support the [Scroll](uiauto-implementingscroll.md) control pattern if the content is scrollable.</span></span>                                                                                                                              |
| [<span data-ttu-id="57c12-188">**ITextProvider**</span><span class="sxs-lookup"><span data-stu-id="57c12-188">**ITextProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider)     | <span data-ttu-id="57c12-189">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="57c12-189">Required</span></span>      | <span data-ttu-id="57c12-190">Todos os controles de documento devem dar suporte ao padrão de controle de [texto](uiauto-implementingtextandtextrange.md) .</span><span class="sxs-lookup"><span data-stu-id="57c12-190">All document controls must support the [Text](uiauto-implementingtextandtextrange.md) control pattern.</span></span>                                                                                                                                                                                                                |
| [<span data-ttu-id="57c12-191">**IValueProvider**</span><span class="sxs-lookup"><span data-stu-id="57c12-191">**IValueProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)   | <span data-ttu-id="57c12-192">Depende</span><span class="sxs-lookup"><span data-stu-id="57c12-192">Depends</span></span>       | <span data-ttu-id="57c12-193">Embora os clientes de automação da interface do usuário possam usar o [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) para obter informações de texto sobre um documento, eles precisam do padrão de controle de [valor](uiauto-implementingvalue.md) para definir o valor interno.</span><span class="sxs-lookup"><span data-stu-id="57c12-193">While UI Automation clients can use [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) to obtain text information about a document, they need the [Value](uiauto-implementingvalue.md) control pattern to set the inner value.</span></span> <span data-ttu-id="57c12-194">A entrada de texto simples só é possível por meio do padrão de controle de valor.</span><span class="sxs-lookup"><span data-stu-id="57c12-194">Simple text entry is possible only through the Value control pattern.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="57c12-195">Eventos necessários</span><span class="sxs-lookup"><span data-stu-id="57c12-195">Required Events</span></span>

<span data-ttu-id="57c12-196">A tabela a seguir lista os eventos de automação da interface do usuário aos quais os controles de documento são necessários para dar suporte.</span><span class="sxs-lookup"><span data-stu-id="57c12-196">The following table lists the UI Automation events that document controls are required to support.</span></span> <span data-ttu-id="57c12-197">Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="57c12-197">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="57c12-198">Evento de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="57c12-198">UI Automation Event</span></span>                                                                                                                                        | <span data-ttu-id="57c12-199">Observações</span><span class="sxs-lookup"><span data-stu-id="57c12-199">Notes</span></span>                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="57c12-200">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="57c12-200">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                           |                                                                                                                            |
| <span data-ttu-id="57c12-201">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="57c12-201">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                      |                                                                                                                            |
| <span data-ttu-id="57c12-202">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="57c12-202">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                      | <span data-ttu-id="57c12-203">Se o controle oferecer suporte à propriedade [**IsEnabled**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="57c12-203">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="57c12-204">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="57c12-204">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                  | <span data-ttu-id="57c12-205">Se o controle oferecer suporte à propriedade [**IsOffscreen**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="57c12-205">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="57c12-206">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="57c12-206">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                       |                                                                                                                            |
| <span data-ttu-id="57c12-207">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollHorizontallyScrollablePropertyId.</span><span class="sxs-lookup"><span data-stu-id="57c12-207">[**UIA\_ScrollHorizontallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>   | <span data-ttu-id="57c12-208">Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="57c12-208">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="57c12-209">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollHorizontalScrollPercentPropertyId.</span><span class="sxs-lookup"><span data-stu-id="57c12-209">[**UIA\_ScrollHorizontalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="57c12-210">Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="57c12-210">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="57c12-211">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollHorizontalViewSizePropertyId.</span><span class="sxs-lookup"><span data-stu-id="57c12-211">[**UIA\_ScrollHorizontalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>           | <span data-ttu-id="57c12-212">Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="57c12-212">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="57c12-213">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollVerticallyScrollablePropertyId.</span><span class="sxs-lookup"><span data-stu-id="57c12-213">[**UIA\_ScrollVerticallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>       | <span data-ttu-id="57c12-214">Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="57c12-214">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="57c12-215">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollVerticalScrollPercentPropertyId.</span><span class="sxs-lookup"><span data-stu-id="57c12-215">[**UIA\_ScrollVerticalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>     | <span data-ttu-id="57c12-216">Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="57c12-216">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="57c12-217">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollVerticalViewSizePropertyId.</span><span class="sxs-lookup"><span data-stu-id="57c12-217">[**UIA\_ScrollVerticalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>               | <span data-ttu-id="57c12-218">Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="57c12-218">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| [<span data-ttu-id="57c12-219">**\_InvalidatedEventId de seleção de UIA \_**</span><span class="sxs-lookup"><span data-stu-id="57c12-219">**UIA\_Selection\_InvalidatedEventId**</span></span>](uiauto-event-ids.md)                                                            | <span data-ttu-id="57c12-220">Se o controle der suporte ao padrão de controle [Selection](uiauto-implementingselection.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="57c12-220">If the control supports the [Selection](uiauto-implementingselection.md) control pattern, it must support this event.</span></span>     |
| [<span data-ttu-id="57c12-221">**\_TextSelectionChangedEventId de texto UIA \_**</span><span class="sxs-lookup"><span data-stu-id="57c12-221">**UIA\_Text\_TextSelectionChangedEventId**</span></span>](uiauto-event-ids.md)                                                    |                                                                                                                            |
| [<span data-ttu-id="57c12-222">**\_TextChangedEventId de texto UIA \_**</span><span class="sxs-lookup"><span data-stu-id="57c12-222">**UIA\_Text\_TextChangedEventId**</span></span>](uiauto-event-ids.md)                                                                      |                                                                                                                            |
| <span data-ttu-id="57c12-223">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ValueValuePropertyId.</span><span class="sxs-lookup"><span data-stu-id="57c12-223">[**UIA\_ValueValuePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>                                       | <span data-ttu-id="57c12-224">Se o controle der suporte ao padrão de controle de [valor](uiauto-implementingvalue.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="57c12-224">If the control supports the [Value](uiauto-implementingvalue.md) control pattern, it must support this event.</span></span>             |



 

## <a name="related-topics"></a><span data-ttu-id="57c12-225">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="57c12-225">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="57c12-226">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="57c12-226">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="57c12-227">Visão Geral dos Tipos de Controle de Automação de Interface do Usuário</span><span class="sxs-lookup"><span data-stu-id="57c12-227">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="57c12-228">Visão geral de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="57c12-228">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




