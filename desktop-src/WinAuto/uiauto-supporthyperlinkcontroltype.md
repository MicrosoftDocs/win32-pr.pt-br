---
title: Tipo de controle de hiperlink
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle HyperLink.
ms.assetid: 6dd16ae6-eff0-4913-8916-5092aec34f1f
keywords:
- Automação da interface do usuário, suporte para tipo de controle de hiperlink
- Automação da interface do usuário, tipo de controle de hiperlink
- Automação da interface do usuário, estrutura de árvore para tipo de controle de hiperlink
- Automação da interface do usuário, propriedades para tipo de controle de hiperlink
- Automação da interface do usuário, padrões de controle para tipo de controle de hiperlink
- Automação da interface do usuário, eventos para tipo de controle de hiperlink
- estruturas de árvore, tipo de controle de hiperlink
- Propriedades, tipo de controle hiperlink
- padrões de controle, tipo de controle de hiperlink
- eventos, tipo de controle de hiperlink
- suporte para tipo de controle de hiperlink
- tipo de controle Hiperlink
- tipos de controle, estrutura de árvore para tipo de controle de hiperlink
- tipos de controle, padrões de controle para tipo de controle de hiperlink
- tipos de controle, suporte para hiperlink
- tipos de controle, hiperlink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71547f37380aeb029e4f73f8d9b2286b285187ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635839"
---
# <a name="hyperlink-control-type"></a><span data-ttu-id="34138-119">Tipo de controle de hiperlink</span><span class="sxs-lookup"><span data-stu-id="34138-119">Hyperlink Control Type</span></span>

<span data-ttu-id="34138-120">Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle **Hyperlink** .</span><span class="sxs-lookup"><span data-stu-id="34138-120">This topic provides information about Microsoft UI Automation support for the **Hyperlink** control type.</span></span>

<span data-ttu-id="34138-121">Os controles de hiperlink criam links que permitem que os usuários naveguem dentro da mesma página ou de uma página para outra.</span><span class="sxs-lookup"><span data-stu-id="34138-121">Hyperlink controls create links that enable users to navigate within the same page, or from one page to another.</span></span>

<span data-ttu-id="34138-122">As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle **Hyperlink** .</span><span class="sxs-lookup"><span data-stu-id="34138-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Hyperlink** control type.</span></span> <span data-ttu-id="34138-123">Os requisitos de automação da interface do usuário se aplicam a todos os controles de hiperlink em que a estrutura/plataforma da interface do usuário integra o suporte à automação da interface do usuário para tipos de controle</span><span class="sxs-lookup"><span data-stu-id="34138-123">The UI Automation requirements apply to all hyperlink controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="34138-124">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="34138-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="34138-125">Estrutura de árvore típica</span><span class="sxs-lookup"><span data-stu-id="34138-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="34138-126">Propriedades relevantes</span><span class="sxs-lookup"><span data-stu-id="34138-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="34138-127">Padrões de controle necessários</span><span class="sxs-lookup"><span data-stu-id="34138-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="34138-128">Eventos necessários</span><span class="sxs-lookup"><span data-stu-id="34138-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="34138-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="34138-129">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="34138-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="34138-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="34138-131">Estrutura de árvore típica</span><span class="sxs-lookup"><span data-stu-id="34138-131">Typical Tree Structure</span></span>

<span data-ttu-id="34138-132">A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence a controles de hiperlink e descreve o que pode ser contido em cada exibição.</span><span class="sxs-lookup"><span data-stu-id="34138-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to hyperlink controls and describes what can be contained in each view.</span></span> <span data-ttu-id="34138-133">Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="34138-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="34138-134">Exibição de controle</span><span class="sxs-lookup"><span data-stu-id="34138-134">Control View</span></span></th>
<th><span data-ttu-id="34138-135">Exibição de conteúdo</span><span class="sxs-lookup"><span data-stu-id="34138-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="34138-136">Hyperlink</span><span class="sxs-lookup"><span data-stu-id="34138-136">Hyperlink</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="34138-137">Hyperlink</span><span class="sxs-lookup"><span data-stu-id="34138-137">Hyperlink</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="34138-138">Propriedades relevantes</span><span class="sxs-lookup"><span data-stu-id="34138-138">Relevant Properties</span></span>

<span data-ttu-id="34138-139">A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para os controles de hiperlink.</span><span class="sxs-lookup"><span data-stu-id="34138-139">The following table lists the UI Automation properties whose value or definition is especially relevant to the hyperlink controls.</span></span> <span data-ttu-id="34138-140">Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="34138-140">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="34138-141">Propriedade de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="34138-141">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="34138-142">Valor</span><span class="sxs-lookup"><span data-stu-id="34138-142">Value</span></span>         | <span data-ttu-id="34138-143">Observações</span><span class="sxs-lookup"><span data-stu-id="34138-143">Notes</span></span>                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="34138-144">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="34138-144">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="34138-145">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="34138-145">See notes.</span></span>    | <span data-ttu-id="34138-146">O valor dessa propriedade deve ser exclusivo em todos os controles em um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="34138-146">The value of this property must be unique across all controls in an application.</span></span>                                                         |
| [<span data-ttu-id="34138-147">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="34138-147">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="34138-148">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="34138-148">See notes.</span></span>    | <span data-ttu-id="34138-149">O retângulo mais externo que contém o controle inteiro.</span><span class="sxs-lookup"><span data-stu-id="34138-149">The outermost rectangle that contains the whole control.</span></span>                                                                                 |
| [<span data-ttu-id="34138-150">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="34138-150">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="34138-151">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="34138-151">See notes.</span></span>    | <span data-ttu-id="34138-152">O ponto clicável do controle de hiperlink deve ser um ponto que inicia o hiperlink se clicado com um ponteiro do mouse.</span><span class="sxs-lookup"><span data-stu-id="34138-152">The hyperlink control's clickable point must be a point that launches the hyperlink if clicked with a mouse pointer.</span></span>                     |
| [<span data-ttu-id="34138-153">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="34138-153">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="34138-154">**Hiperlink**</span><span class="sxs-lookup"><span data-stu-id="34138-154">**Hyperlink**</span></span> |                                                                                                                                          |
| [<span data-ttu-id="34138-155">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="34138-155">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="34138-156">TRUE</span><span class="sxs-lookup"><span data-stu-id="34138-156">TRUE</span></span>          | <span data-ttu-id="34138-157">O controle HyperLink é sempre incluído na exibição de conteúdo da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="34138-157">The hyperlink control is always included in the content view of the UI Automation tree.</span></span>                                                  |
| [<span data-ttu-id="34138-158">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="34138-158">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="34138-159">TRUE</span><span class="sxs-lookup"><span data-stu-id="34138-159">TRUE</span></span>          | <span data-ttu-id="34138-160">O controle HyperLink é sempre incluído no modo de exibição de controle da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="34138-160">The hyperlink control is always included in the control view of the UI Automation tree.</span></span>                                                  |
| [<span data-ttu-id="34138-161">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="34138-161">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="34138-162">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="34138-162">See notes.</span></span>    | <span data-ttu-id="34138-163">Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="34138-163">If the control can receive keyboard focus, it must support this property.</span></span>                                                                |
| [<span data-ttu-id="34138-164">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="34138-164">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="34138-165">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="34138-165">See notes.</span></span>    | <span data-ttu-id="34138-166">Se houver um rótulo de texto estático, essa propriedade deverá expor uma referência a esse controle.</span><span class="sxs-lookup"><span data-stu-id="34138-166">If there is a static text label, this property must expose a reference to that control.</span></span>                                                  |
| [<span data-ttu-id="34138-167">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="34138-167">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="34138-168">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="34138-168">See notes.</span></span>    | <span data-ttu-id="34138-169">Cadeia de caracteres localizada correspondente ao tipo de controle de **hiperlink** .</span><span class="sxs-lookup"><span data-stu-id="34138-169">Localized string corresponding to the **Hyperlink** control type.</span></span> <span data-ttu-id="34138-170">O valor padrão é "HYPERLINK" para en-US ou inglês (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="34138-170">The default value is "hyperlink" for en-US or English (United States).</span></span> |
| [<span data-ttu-id="34138-171">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="34138-171">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="34138-172">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="34138-172">See notes.</span></span>    | <span data-ttu-id="34138-173">O nome do controle de hiperlink é o texto que é exibido na tela como sublinhado.</span><span class="sxs-lookup"><span data-stu-id="34138-173">The hyperlink control's name is the text that is displayed on the screen as underlined.</span></span>                                                  |



 

## <a name="required-control-patterns"></a><span data-ttu-id="34138-174">Padrões de controle necessários</span><span class="sxs-lookup"><span data-stu-id="34138-174">Required Control Patterns</span></span>

<span data-ttu-id="34138-175">A tabela a seguir lista os padrões de controle de automação da interface do usuário para os quais os controles de hiperlink precisam dar suporte.</span><span class="sxs-lookup"><span data-stu-id="34138-175">The following table lists the UI Automation control patterns that hyperlink controls are required to support.</span></span> <span data-ttu-id="34138-176">Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="34138-176">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="34138-177">Propriedade padrão de controle/padrão</span><span class="sxs-lookup"><span data-stu-id="34138-177">Control Pattern/Pattern Property</span></span>                  | <span data-ttu-id="34138-178">Suporte/valor</span><span class="sxs-lookup"><span data-stu-id="34138-178">Support/Value</span></span>                | <span data-ttu-id="34138-179">Observações</span><span class="sxs-lookup"><span data-stu-id="34138-179">Notes</span></span>                                                                                                                                                                                                                                                  |
|---------------------------------------------------|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="34138-180">**IInvokeProvider**</span><span class="sxs-lookup"><span data-stu-id="34138-180">**IInvokeProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) | <span data-ttu-id="34138-181">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="34138-181">Required</span></span>                     | <span data-ttu-id="34138-182">Todos os controles de hiperlink devem dar suporte ao padrão de controle [Invoke](uiauto-implementinginvoke.md) .</span><span class="sxs-lookup"><span data-stu-id="34138-182">All hyperlink controls must support the [Invoke](uiauto-implementinginvoke.md) control pattern.</span></span>                                                                                                                                                       |
| [<span data-ttu-id="34138-183">**IValueProvider**</span><span class="sxs-lookup"><span data-stu-id="34138-183">**IValueProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)   | <span data-ttu-id="34138-184">Depende</span><span class="sxs-lookup"><span data-stu-id="34138-184">Depends</span></span>                      | <span data-ttu-id="34138-185">Os controles de hiperlink devem dar suporte ao padrão de controle de [valor](uiauto-implementingvalue.md) quando o link contém informações que podem ser usadas e significativas para o usuário.</span><span class="sxs-lookup"><span data-stu-id="34138-185">Hyperlink controls should support the [Value](uiauto-implementingvalue.md) control pattern when the link contains information that is usable and meaningful to the user.</span></span>                                                                              |
| [<span data-ttu-id="34138-186">**Valor**</span><span class="sxs-lookup"><span data-stu-id="34138-186">**Value**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value)      | <span data-ttu-id="34138-187">Por exemplo, "https://www..".</span><span class="sxs-lookup"><span data-stu-id="34138-187">For example, "https://www..."</span></span> | <span data-ttu-id="34138-188">Uma URL para um endereço de Internet ou intranet é um exemplo de um hiperlink que contém informações que são significativas para o usuário.</span><span class="sxs-lookup"><span data-stu-id="34138-188">A URL for an Internet or intranet address is an example of a hyperlink that contains information that is meaningful to the user.</span></span> <span data-ttu-id="34138-189">Um link programático, no entanto, é significativo apenas para um aplicativo e não é recomendado para a propriedade **Value** .</span><span class="sxs-lookup"><span data-stu-id="34138-189">A programmatic link, however, is meaningful only to an application and is not recommended for the **Value** property.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="34138-190">Eventos necessários</span><span class="sxs-lookup"><span data-stu-id="34138-190">Required Events</span></span>

<span data-ttu-id="34138-191">A tabela a seguir lista os eventos de automação da interface do usuário aos quais os controles de hiperlink são necessários para dar suporte.</span><span class="sxs-lookup"><span data-stu-id="34138-191">The following table lists the UI Automation events that hyperlink controls are required to support.</span></span> <span data-ttu-id="34138-192">Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="34138-192">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="34138-193">Evento de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="34138-193">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="34138-194">Observações</span><span class="sxs-lookup"><span data-stu-id="34138-194">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="34138-195">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="34138-195">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="34138-196">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="34138-196">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| [<span data-ttu-id="34138-197">**UIA \_ invocar \_ InvokedEventId**</span><span class="sxs-lookup"><span data-stu-id="34138-197">**UIA\_Invoke\_InvokedEventId**</span></span>](uiauto-event-ids.md)                                                     |                                                                                                                            |
| <span data-ttu-id="34138-198">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="34138-198">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="34138-199">Se o controle oferecer suporte à propriedade [**IsEnabled**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="34138-199">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="34138-200">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="34138-200">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="34138-201">Se o controle oferecer suporte à propriedade [**IsOffscreen**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="34138-201">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="34138-202">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="34138-202">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="34138-203">Comentários</span><span class="sxs-lookup"><span data-stu-id="34138-203">Remarks</span></span>

<span data-ttu-id="34138-204">O tipo de controle hiperlink deve ser aplicado somente a um objeto que, quando clicado, faz com que a navegação ocorra; Ele não deve ser aplicado ao contêiner do hiperlink.</span><span class="sxs-lookup"><span data-stu-id="34138-204">The Hyperlink control type should be applied only to an object that, when clicked, causes navigation to occur; it should not be applied to the container of the hyperlink.</span></span> <span data-ttu-id="34138-205">Por exemplo, somente os "pontos de acesso" clicáveis dentro de um mapa de imagem devem ter o tipo de controle **Hyperlink** .</span><span class="sxs-lookup"><span data-stu-id="34138-205">For example, only the clickable "hot spots" inside an image map should have the **Hyperlink** control type.</span></span> <span data-ttu-id="34138-206">O mesmo é verdadeiro para hiperlinks em um campo de texto ou contêiner de documento.</span><span class="sxs-lookup"><span data-stu-id="34138-206">The same is true of hyperlinks in a text field or document container.</span></span> <span data-ttu-id="34138-207">Nesse caso, somente o texto ou a imagem do hiperlink deve ter o tipo de controle **Hyperlink** , não o contêiner.</span><span class="sxs-lookup"><span data-stu-id="34138-207">In this case, only the hyperlink text or image should have the **Hyperlink** control type, not the container.</span></span>

<span data-ttu-id="34138-208">O padrão de controle de [texto](uiauto-implementingtextandtextrange.md) é ideal para dar suporte a hiperlinks inseridos em elementos de texto ou documento.</span><span class="sxs-lookup"><span data-stu-id="34138-208">The [Text](uiauto-implementingtextandtextrange.md) control pattern is ideal for supporting embedded hyperlinks in text or document elements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="34138-209">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="34138-209">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="34138-210">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="34138-210">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="34138-211">Visão Geral dos Tipos de Controle de Automação de Interface do Usuário</span><span class="sxs-lookup"><span data-stu-id="34138-211">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="34138-212">Visão geral de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="34138-212">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




