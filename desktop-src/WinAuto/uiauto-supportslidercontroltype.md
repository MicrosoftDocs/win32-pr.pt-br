---
title: Tipo de controle Slider
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle Slider.
ms.assetid: dc7bef7a-b68c-4184-a9e7-745bb41b592e
keywords:
- Automação da interface do usuário, suporte para tipo de controle Slider
- Automação da interface do usuário, tipo de controle Slider
- Automação da interface do usuário, estrutura de árvore para tipo de controle Slider
- Automação da interface do usuário, propriedades para tipo de controle Slider
- Automação da interface do usuário, padrões de controle para tipo de controle Slider
- Automação da interface do usuário, eventos para tipo de controle Slider
- estruturas de árvore, tipo de controle Slider
- Propriedades, tipo de controle Slider
- padrões de controle, tipo de controle Slider
- eventos, tipo de controle Slider
- suporte para tipo de controle Slider
- tipo Controle deslizante
- tipos de controle, estrutura de árvore para tipo de controle Slider
- tipos de controle, padrões de controle para o tipo de controle Slider
- tipos de controle, suporte para controle deslizante
- tipos de controle, controle deslizante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be8e82dfc8f011363086745368ed1693c45a6aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916401"
---
# <a name="slider-control-type"></a><span data-ttu-id="807b2-119">Tipo de controle Slider</span><span class="sxs-lookup"><span data-stu-id="807b2-119">Slider Control Type</span></span>

<span data-ttu-id="807b2-120">Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle **Slider** .</span><span class="sxs-lookup"><span data-stu-id="807b2-120">This topic provides information about Microsoft UI Automation support for the **Slider** control type.</span></span>

<span data-ttu-id="807b2-121">Um controle deslizante é um controle composto com botões que permitem que um usuário defina um intervalo numérico ou selecione um conjunto de itens.</span><span class="sxs-lookup"><span data-stu-id="807b2-121">A slider control is a composite control with buttons that enable a user to set a numerical range or select from a set of items.</span></span>

<span data-ttu-id="807b2-122">As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle **Slider** .</span><span class="sxs-lookup"><span data-stu-id="807b2-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Slider** control type.</span></span> <span data-ttu-id="807b2-123">Os requisitos de automação da interface do usuário se aplicam a todos os controles Slider onde a plataforma/estrutura de interface do usuário integra o suporte à automação da interface do usuário para tipos de controle e padrões</span><span class="sxs-lookup"><span data-stu-id="807b2-123">The UI Automation requirements apply to all slider controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="807b2-124">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="807b2-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="807b2-125">Estrutura de árvore típica</span><span class="sxs-lookup"><span data-stu-id="807b2-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="807b2-126">Propriedades relevantes</span><span class="sxs-lookup"><span data-stu-id="807b2-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="807b2-127">Padrões de controle necessários</span><span class="sxs-lookup"><span data-stu-id="807b2-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="807b2-128">Eventos necessários</span><span class="sxs-lookup"><span data-stu-id="807b2-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="807b2-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="807b2-129">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="807b2-130">Estrutura de árvore típica</span><span class="sxs-lookup"><span data-stu-id="807b2-130">Typical Tree Structure</span></span>

<span data-ttu-id="807b2-131">A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence a controles Slider e descreve o que pode ser contido em cada exibição.</span><span class="sxs-lookup"><span data-stu-id="807b2-131">The following table depicts a typical control and content view of the UI Automation tree that pertains to slider controls and describes what can be contained in each view.</span></span> <span data-ttu-id="807b2-132">Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="807b2-132">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="807b2-133">Exibição de controle</span><span class="sxs-lookup"><span data-stu-id="807b2-133">Control View</span></span></th>
<th><span data-ttu-id="807b2-134">Exibição de conteúdo</span><span class="sxs-lookup"><span data-stu-id="807b2-134">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="807b2-135">Controle deslizante</span><span class="sxs-lookup"><span data-stu-id="807b2-135">Slider</span></span>
<ul>
<li><span data-ttu-id="807b2-136">Botão (2 ou 4)</span><span class="sxs-lookup"><span data-stu-id="807b2-136">Button (2 or 4)</span></span></li>
<li><span data-ttu-id="807b2-137">Thumb (1)</span><span class="sxs-lookup"><span data-stu-id="807b2-137">Thumb (1)</span></span></li>
<li><span data-ttu-id="807b2-138">Item de lista (0 ou mais)</span><span class="sxs-lookup"><span data-stu-id="807b2-138">List Item (0 or more)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="807b2-139">Controle deslizante</span><span class="sxs-lookup"><span data-stu-id="807b2-139">Slider</span></span>
<ul>
<li><span data-ttu-id="807b2-140">Item de lista (0 ou mais)</span><span class="sxs-lookup"><span data-stu-id="807b2-140">List Item (0 or more)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="807b2-141">Propriedades relevantes</span><span class="sxs-lookup"><span data-stu-id="807b2-141">Relevant Properties</span></span>

<span data-ttu-id="807b2-142">A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para controles deslizantes.</span><span class="sxs-lookup"><span data-stu-id="807b2-142">The following table lists the UI Automation properties whose value or definition is especially relevant to slider controls.</span></span> <span data-ttu-id="807b2-143">Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="807b2-143">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="807b2-144">Propriedade de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="807b2-144">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="807b2-145">Valor</span><span class="sxs-lookup"><span data-stu-id="807b2-145">Value</span></span>      | <span data-ttu-id="807b2-146">Observações</span><span class="sxs-lookup"><span data-stu-id="807b2-146">Notes</span></span>                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="807b2-147">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="807b2-147">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="807b2-148">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="807b2-148">See notes.</span></span> | <span data-ttu-id="807b2-149">O valor dessa propriedade deve ser exclusivo entre todos os elementos de mesmo nível na exibição bruta da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="807b2-149">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                   |
| [<span data-ttu-id="807b2-150">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="807b2-150">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="807b2-151">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="807b2-151">See notes.</span></span> | <span data-ttu-id="807b2-152">O retângulo mais externo que contém o controle inteiro.</span><span class="sxs-lookup"><span data-stu-id="807b2-152">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="807b2-153">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="807b2-153">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="807b2-154">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="807b2-154">See notes.</span></span> | <span data-ttu-id="807b2-155">A maioria dos controles deslizantes deve retornar o erro [**UIA \_ E \_ NOCLICKABLEPOINT**](uiauto-error-codes.md) porque o retângulo delimitador inteiro do controle deslizante é ocupado por controles filho.</span><span class="sxs-lookup"><span data-stu-id="807b2-155">The majority of slider controls must return the [**UIA\_E\_NOCLICKABLEPOINT**](uiauto-error-codes.md) error because the entire bounding rectangle of the slider control is occupied by child controls.</span></span> |
| [<span data-ttu-id="807b2-156">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="807b2-156">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="807b2-157">**Controle deslizante**</span><span class="sxs-lookup"><span data-stu-id="807b2-157">**Slider**</span></span> | <span data-ttu-id="807b2-158">Esse valor é o mesmo para todas as estruturas.</span><span class="sxs-lookup"><span data-stu-id="807b2-158">This value is the same for all frameworks.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="807b2-159">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="807b2-159">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="807b2-160">TRUE</span><span class="sxs-lookup"><span data-stu-id="807b2-160">TRUE</span></span>       | <span data-ttu-id="807b2-161">O controle deslizante sempre é incluído na exibição de conteúdo da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="807b2-161">The slider control is always included in the content view of the UI Automation tree.</span></span>                                                                                                                                           |
| [<span data-ttu-id="807b2-162">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="807b2-162">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="807b2-163">TRUE</span><span class="sxs-lookup"><span data-stu-id="807b2-163">TRUE</span></span>       | <span data-ttu-id="807b2-164">O controle deslizante sempre é incluído na exibição de controle da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="807b2-164">The slider control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                                           |
| [<span data-ttu-id="807b2-165">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="807b2-165">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="807b2-166">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="807b2-166">See notes.</span></span> | <span data-ttu-id="807b2-167">Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="807b2-167">If the control can receive keyboard focus, it must support this property.</span></span> <span data-ttu-id="807b2-168">Os filhos (botões e Thumb) de um controle deslizante nunca devem assumir o foco.</span><span class="sxs-lookup"><span data-stu-id="807b2-168">The children (buttons and thumb) of a slider control should never take the focus.</span></span> <span data-ttu-id="807b2-169">O foco sempre deve permanecer no controle Slider em si.</span><span class="sxs-lookup"><span data-stu-id="807b2-169">The focus should always remain on the slider control itself.</span></span>       |
| [<span data-ttu-id="807b2-170">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="807b2-170">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="807b2-171">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="807b2-171">See notes.</span></span> | <span data-ttu-id="807b2-172">Se houver um rótulo de texto estático associado ao controle, essa propriedade deverá expor uma referência a esse controle.</span><span class="sxs-lookup"><span data-stu-id="807b2-172">If there is a static text label associated with the control, this property must expose a reference to that control.</span></span> <span data-ttu-id="807b2-173">Se o controle de texto for um subcomponente de outro controle, ele não terá uma propriedade **LabeledBy** definida.</span><span class="sxs-lookup"><span data-stu-id="807b2-173">If the text control is a subcomponent of another control, it will not have a **LabeledBy** property set.</span></span>   |
| [<span data-ttu-id="807b2-174">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="807b2-174">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="807b2-175">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="807b2-175">See notes.</span></span> | <span data-ttu-id="807b2-176">Cadeia de caracteres localizada correspondente ao tipo de controle **Slider** .</span><span class="sxs-lookup"><span data-stu-id="807b2-176">Localized string corresponding to the **Slider** control type.</span></span> <span data-ttu-id="807b2-177">O valor padrão é "slider" para en-US ou inglês (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="807b2-177">The default value is "slider" for en-US or English (United States).</span></span>                                                                                             |
| [<span data-ttu-id="807b2-178">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="807b2-178">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="807b2-179">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="807b2-179">See notes.</span></span> | <span data-ttu-id="807b2-180">O nome do controle deslizante normalmente é gerado a partir de um rótulo de texto estático.</span><span class="sxs-lookup"><span data-stu-id="807b2-180">The name of the slider control is typically generated from a static text label.</span></span> <span data-ttu-id="807b2-181">Se não houver um rótulo de texto estático, um valor de propriedade para **nome** deverá ser atribuído pelo desenvolvedor do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="807b2-181">If there is not a static text label, a property value for **Name** must be assigned by the application developer.</span></span>                              |



 

## <a name="required-control-patterns"></a><span data-ttu-id="807b2-182">Padrões de controle necessários</span><span class="sxs-lookup"><span data-stu-id="807b2-182">Required Control Patterns</span></span>

<span data-ttu-id="807b2-183">A tabela a seguir lista os padrões de controle de automação da interface do usuário que devem ter suporte em todos os controles Slider.</span><span class="sxs-lookup"><span data-stu-id="807b2-183">The following table lists the UI Automation control patterns required to be supported by all slider controls.</span></span> <span data-ttu-id="807b2-184">Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="807b2-184">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="807b2-185">Propriedade padrão de controle/padrão</span><span class="sxs-lookup"><span data-stu-id="807b2-185">Control Pattern/Pattern Property</span></span>                          | <span data-ttu-id="807b2-186">Suporte/valor</span><span class="sxs-lookup"><span data-stu-id="807b2-186">Support/Value</span></span> | <span data-ttu-id="807b2-187">Observações</span><span class="sxs-lookup"><span data-stu-id="807b2-187">Notes</span></span>                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="807b2-188">**IRangeValueProvider**</span><span class="sxs-lookup"><span data-stu-id="807b2-188">**IRangeValueProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) | <span data-ttu-id="807b2-189">Depende</span><span class="sxs-lookup"><span data-stu-id="807b2-189">Depends</span></span>       | <span data-ttu-id="807b2-190">Um controle deslizante deve dar suporte ao padrão de controle [RangeValue](uiauto-implementingrangevalue.md) se o conteúdo puder ser definido como um valor dentro de um intervalo numérico.</span><span class="sxs-lookup"><span data-stu-id="807b2-190">A slider should support the [RangeValue](uiauto-implementingrangevalue.md) control pattern if the content can be set to a value within a numerical range.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="807b2-191">**ISelectionProvider**</span><span class="sxs-lookup"><span data-stu-id="807b2-191">**ISelectionProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)   | <span data-ttu-id="807b2-192">Depende</span><span class="sxs-lookup"><span data-stu-id="807b2-192">Depends</span></span>       | <span data-ttu-id="807b2-193">Um controle deslizante deve dar suporte ao padrão de controle de [seleção](uiauto-implementingselection.md) se o conteúdo representar um valor entre um conjunto discreto de opções.</span><span class="sxs-lookup"><span data-stu-id="807b2-193">A slider should support the [Selection](uiauto-implementingselection.md) control pattern if the content represents one value among a discrete set of options.</span></span> <span data-ttu-id="807b2-194">Quando há suporte para o padrão de controle de seleção, a seleção correspondente deve ser exposta como um ou mais itens de lista filho do controle deslizante.</span><span class="sxs-lookup"><span data-stu-id="807b2-194">When the Selection control pattern is supported, the corresponding selection must be exposed as one or more child list items of the slider.</span></span> |
| [<span data-ttu-id="807b2-195">**IValueProvider**</span><span class="sxs-lookup"><span data-stu-id="807b2-195">**IValueProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)           | <span data-ttu-id="807b2-196">Depende</span><span class="sxs-lookup"><span data-stu-id="807b2-196">Depends</span></span>       | <span data-ttu-id="807b2-197">Um controle deslizante deve dar suporte ao padrão de controle de [valor](uiauto-implementingvalue.md) se o conteúdo representar um valor entre um conjunto discreto de opções.</span><span class="sxs-lookup"><span data-stu-id="807b2-197">A slider should support the [Value](uiauto-implementingvalue.md) control pattern if the content represents one value among a discrete set of options.</span></span>                                                                                                                                                     |



 

## <a name="required-events"></a><span data-ttu-id="807b2-198">Eventos necessários</span><span class="sxs-lookup"><span data-stu-id="807b2-198">Required Events</span></span>

<span data-ttu-id="807b2-199">A tabela a seguir lista os eventos de automação da interface do usuário aos quais os controles deslizantes são necessários para dar suporte.</span><span class="sxs-lookup"><span data-stu-id="807b2-199">The following table lists the UI Automation events that slider controls are required to support.</span></span> <span data-ttu-id="807b2-200">Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="807b2-200">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="807b2-201">Evento de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="807b2-201">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="807b2-202">Observações</span><span class="sxs-lookup"><span data-stu-id="807b2-202">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="807b2-203">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="807b2-203">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="807b2-204">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="807b2-204">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="807b2-205">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="807b2-205">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="807b2-206">Se o controle oferecer suporte à propriedade [**IsEnabled**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="807b2-206">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="807b2-207">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="807b2-207">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="807b2-208">Se o controle oferecer suporte à propriedade [**IsOffscreen**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="807b2-208">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| <span data-ttu-id="807b2-209">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade RangeValueValuePropertyId.</span><span class="sxs-lookup"><span data-stu-id="807b2-209">[**UIA\_RangeValueValuePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>        | <span data-ttu-id="807b2-210">Se o controle der suporte ao padrão de controle [RangeValue](uiauto-implementingrangevalue.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="807b2-210">If the control supports the [RangeValue](uiauto-implementingrangevalue.md) control pattern, it must support this event.</span></span>   |
| [<span data-ttu-id="807b2-211">**\_InvalidatedEventId de seleção de UIA \_**</span><span class="sxs-lookup"><span data-stu-id="807b2-211">**UIA\_Selection\_InvalidatedEventId**</span></span>](uiauto-event-ids.md)                                       | <span data-ttu-id="807b2-212">Se o controle der suporte ao padrão de controle [Selection](uiauto-implementingselection.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="807b2-212">If the control supports the [Selection](uiauto-implementingselection.md) control pattern, it must support this event.</span></span>     |
| [<span data-ttu-id="807b2-213">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="807b2-213">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |
| <span data-ttu-id="807b2-214">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ValueValuePropertyId.</span><span class="sxs-lookup"><span data-stu-id="807b2-214">[**UIA\_ValueValuePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>                  | <span data-ttu-id="807b2-215">Se o controle der suporte ao padrão de controle de [valor](uiauto-implementingvalue.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="807b2-215">If the control supports the [Value](uiauto-implementingvalue.md) control pattern, it must support this event.</span></span>             |



 

## <a name="related-topics"></a><span data-ttu-id="807b2-216">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="807b2-216">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="807b2-217">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="807b2-217">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="807b2-218">Visão Geral dos Tipos de Controle de Automação de Interface do Usuário</span><span class="sxs-lookup"><span data-stu-id="807b2-218">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="807b2-219">Visão geral de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="807b2-219">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




