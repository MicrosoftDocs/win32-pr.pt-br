---
title: Tipo de controle StatusBar
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle StatusBar.
ms.assetid: a28df0a1-95a8-4941-a00d-1f5570589626
keywords:
- Automação da interface do usuário, suporte para tipo de controle StatusBar
- Automação da interface do usuário, tipo de controle StatusBar
- Automação da interface do usuário, estrutura de árvore para tipo de controle StatusBar
- Automação da interface do usuário, propriedades para tipo de controle StatusBar
- Automação da interface do usuário, padrões de controle para tipo de controle StatusBar
- Automação da interface do usuário, eventos para tipo de controle StatusBar
- estruturas de árvore, tipo de controle StatusBar
- Propriedades, tipo de controle StatusBar
- padrões de controle, tipo de controle StatusBar
- eventos, tipo de controle StatusBar
- suporte para tipo de controle StatusBar
- StatusBar (tipo de controle)
- tipos de controle, estrutura de árvore para tipo de controle StatusBar
- tipos de controle, padrões de controle para o tipo de controle StatusBar
- tipos de controle, suporte para StatusBar
- tipos de controle, StatusBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65ace64d34429a6d381dfdef2d99d82a3693fca2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292465"
---
# <a name="statusbar-control-type"></a><span data-ttu-id="e2fa6-119">Tipo de controle StatusBar</span><span class="sxs-lookup"><span data-stu-id="e2fa6-119">StatusBar Control Type</span></span>

<span data-ttu-id="e2fa6-120">Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle **StatusBar** .</span><span class="sxs-lookup"><span data-stu-id="e2fa6-120">This topic provides information about Microsoft UI Automation support for the **StatusBar** control type.</span></span>

<span data-ttu-id="e2fa6-121">Um controle barra de status exibe informações sobre um objeto que está sendo exibido em uma janela de um aplicativo, o componente do objeto ou informações contextuais relacionadas à operação desse objeto em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e2fa6-121">A status bar control displays information about an object being viewed in a window of an application, the object's component, or contextual information that relates to that object's operation within your application.</span></span>

<span data-ttu-id="e2fa6-122">As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle **StatusBar** .</span><span class="sxs-lookup"><span data-stu-id="e2fa6-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **StatusBar** control type.</span></span> <span data-ttu-id="e2fa6-123">Os requisitos de automação da interface do usuário se aplicam a todos os controles da barra de status, em que a estrutura/plataforma da interface do usuário integra o suporte à automação da interface do usuário para tipos</span><span class="sxs-lookup"><span data-stu-id="e2fa6-123">The UI Automation requirements apply to all status bar controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="e2fa6-124">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="e2fa6-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="e2fa6-125">Estrutura de árvore típica</span><span class="sxs-lookup"><span data-stu-id="e2fa6-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="e2fa6-126">Propriedades relevantes</span><span class="sxs-lookup"><span data-stu-id="e2fa6-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="e2fa6-127">Padrões de controle necessários</span><span class="sxs-lookup"><span data-stu-id="e2fa6-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="e2fa6-128">Eventos necessários</span><span class="sxs-lookup"><span data-stu-id="e2fa6-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="e2fa6-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="e2fa6-129">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="e2fa6-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e2fa6-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="e2fa6-131">Estrutura de árvore típica</span><span class="sxs-lookup"><span data-stu-id="e2fa6-131">Typical Tree Structure</span></span>

<span data-ttu-id="e2fa6-132">A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence aos controles da barra de status e descreve o que pode ser contido em cada exibição.</span><span class="sxs-lookup"><span data-stu-id="e2fa6-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to status bar controls and describes what can be contained in each view.</span></span> <span data-ttu-id="e2fa6-133">Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="e2fa6-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e2fa6-134">Exibição de controle</span><span class="sxs-lookup"><span data-stu-id="e2fa6-134">Control View</span></span></th>
<th><span data-ttu-id="e2fa6-135">Exibição de conteúdo</span><span class="sxs-lookup"><span data-stu-id="e2fa6-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="e2fa6-136">StatusBar</span><span class="sxs-lookup"><span data-stu-id="e2fa6-136">StatusBar</span></span>
<ul>
<li><span data-ttu-id="e2fa6-137">Editar (0 ou mais)</span><span class="sxs-lookup"><span data-stu-id="e2fa6-137">Edit (0 or more)</span></span></li>
<li><span data-ttu-id="e2fa6-138">ProgressBar (0 ou muitos)</span><span class="sxs-lookup"><span data-stu-id="e2fa6-138">ProgressBar (0 or many)</span></span></li>
<li><span data-ttu-id="e2fa6-139">Imagem (0 ou muitos)</span><span class="sxs-lookup"><span data-stu-id="e2fa6-139">Image (0 or many)</span></span></li>
<li><span data-ttu-id="e2fa6-140">Botão (0 ou muitos)</span><span class="sxs-lookup"><span data-stu-id="e2fa6-140">Button (0 or many)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="e2fa6-141">StatusBar</span><span class="sxs-lookup"><span data-stu-id="e2fa6-141">StatusBar</span></span>
<ul>
<li><span data-ttu-id="e2fa6-142">Editar (0 ou mais)</span><span class="sxs-lookup"><span data-stu-id="e2fa6-142">Edit (0 or more)</span></span></li>
<li><span data-ttu-id="e2fa6-143">ProgressBar (0 ou muitos)</span><span class="sxs-lookup"><span data-stu-id="e2fa6-143">ProgressBar (0 or many)</span></span></li>
<li><span data-ttu-id="e2fa6-144">Imagem (0 ou muitos)</span><span class="sxs-lookup"><span data-stu-id="e2fa6-144">Image (0 or many)</span></span></li>
<li><span data-ttu-id="e2fa6-145">Botão (0 ou muitos)</span><span class="sxs-lookup"><span data-stu-id="e2fa6-145">Button (0 or many)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="e2fa6-146">Propriedades relevantes</span><span class="sxs-lookup"><span data-stu-id="e2fa6-146">Relevant Properties</span></span>

<span data-ttu-id="e2fa6-147">A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para os controles da barra de status.</span><span class="sxs-lookup"><span data-stu-id="e2fa6-147">The following table lists the UI Automation properties whose value or definition is especially relevant to the status bar controls.</span></span> <span data-ttu-id="e2fa6-148">Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="e2fa6-148">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="e2fa6-149">Propriedade de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="e2fa6-149">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="e2fa6-150">Valor</span><span class="sxs-lookup"><span data-stu-id="e2fa6-150">Value</span></span>         | <span data-ttu-id="e2fa6-151">Observações</span><span class="sxs-lookup"><span data-stu-id="e2fa6-151">Notes</span></span>                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e2fa6-152">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="e2fa6-152">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="e2fa6-153">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="e2fa6-153">See notes.</span></span>    | <span data-ttu-id="e2fa6-154">O valor dessa propriedade deve ser exclusivo entre todos os elementos de mesmo nível na exibição bruta da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="e2fa6-154">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                        |
| [<span data-ttu-id="e2fa6-155">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="e2fa6-155">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="e2fa6-156">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="e2fa6-156">See notes.</span></span>    | <span data-ttu-id="e2fa6-157">O retângulo delimitador de uma barra de status deve abranger todos os controles contidos nela.</span><span class="sxs-lookup"><span data-stu-id="e2fa6-157">The bounding rectangle of a status bar must encompass all of the controls contained within it.</span></span>                                                                                                                      |
| [<span data-ttu-id="e2fa6-158">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="e2fa6-158">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="e2fa6-159">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="e2fa6-159">See notes.</span></span>    | <span data-ttu-id="e2fa6-160">Com suporte se houver um retângulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="e2fa6-160">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="e2fa6-161">Se houver áreas dentro do retângulo delimitador que não são clicáveis, e o elemento executar um teste de clique especializado, substitua isso e forneça um ponto clicável.</span><span class="sxs-lookup"><span data-stu-id="e2fa6-161">If there are areas within the bounding rectangle that are not clickable, and the element performs specialized hit testing, override this and provide a clickable point.</span></span> |
| [<span data-ttu-id="e2fa6-162">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="e2fa6-162">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="e2fa6-163">**StatusBar**</span><span class="sxs-lookup"><span data-stu-id="e2fa6-163">**StatusBar**</span></span> |                                                                                                                                                                                                                     |
| [<span data-ttu-id="e2fa6-164">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="e2fa6-164">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="e2fa6-165">TRUE</span><span class="sxs-lookup"><span data-stu-id="e2fa6-165">TRUE</span></span>          | <span data-ttu-id="e2fa6-166">O controle da barra de status é sempre incluído na exibição de conteúdo da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="e2fa6-166">The status bar control is always included in the content view of the UI Automation tree.</span></span>                                                                                                                            |
| [<span data-ttu-id="e2fa6-167">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="e2fa6-167">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="e2fa6-168">TRUE</span><span class="sxs-lookup"><span data-stu-id="e2fa6-168">TRUE</span></span>          | <span data-ttu-id="e2fa6-169">O controle da barra de status é sempre incluído na exibição de controle da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="e2fa6-169">The status bar control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                            |
| [<span data-ttu-id="e2fa6-170">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="e2fa6-170">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="e2fa6-171">Depende</span><span class="sxs-lookup"><span data-stu-id="e2fa6-171">Depends</span></span>       | <span data-ttu-id="e2fa6-172">Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="e2fa6-172">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                                           |
| [<span data-ttu-id="e2fa6-173">**UIA \_ IsOffscreenPropertyId**</span><span class="sxs-lookup"><span data-stu-id="e2fa6-173">**UIA\_IsOffscreenPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="e2fa6-174">Depende</span><span class="sxs-lookup"><span data-stu-id="e2fa6-174">Depends</span></span>       | <span data-ttu-id="e2fa6-175">Se um controle da barra de status não estiver visível no momento, ele retornará TRUE para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="e2fa6-175">If a status bar control is not currently visible, it will return TRUE for this property.</span></span>                                                                                                                            |
| [<span data-ttu-id="e2fa6-176">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="e2fa6-176">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="e2fa6-177">NULO</span><span class="sxs-lookup"><span data-stu-id="e2fa6-177">NULL</span></span>          | <span data-ttu-id="e2fa6-178">O controle da barra de status normalmente não tem um rótulo.</span><span class="sxs-lookup"><span data-stu-id="e2fa6-178">The status bar control typically does not have a label.</span></span>                                                                                                                                                             |
| [<span data-ttu-id="e2fa6-179">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="e2fa6-179">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="e2fa6-180">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="e2fa6-180">See notes.</span></span>    | <span data-ttu-id="e2fa6-181">Cadeia de caracteres localizada correspondente ao tipo de controle **StatusBar** .</span><span class="sxs-lookup"><span data-stu-id="e2fa6-181">Localized string corresponding to the **StatusBar** control type.</span></span> <span data-ttu-id="e2fa6-182">O valor padrão é "barra de status" para en-US ou inglês (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="e2fa6-182">The default value is "status bar" for en-US or English (United States).</span></span>                                                                           |
| [<span data-ttu-id="e2fa6-183">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="e2fa6-183">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="e2fa6-184">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="e2fa6-184">See notes.</span></span>    | <span data-ttu-id="e2fa6-185">O controle da barra de status não precisa de um nome, a menos que mais de um seja usado em um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e2fa6-185">The status bar control does not need a name unless more than one is used within an application.</span></span> <span data-ttu-id="e2fa6-186">Nesse caso, diferencie cada barra com nomes como "status da Internet" ou "status do aplicativo".</span><span class="sxs-lookup"><span data-stu-id="e2fa6-186">In this case, distinguish each bar with names such as "Internet Status" or "Application Status".</span></span>                    |
| [<span data-ttu-id="e2fa6-187">**UIA \_ OrientationPropertyId**</span><span class="sxs-lookup"><span data-stu-id="e2fa6-187">**UIA\_OrientationPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="e2fa6-188">Depende</span><span class="sxs-lookup"><span data-stu-id="e2fa6-188">Depends</span></span>       | <span data-ttu-id="e2fa6-189">Um valor que indica a orientação do controle: horizontal ou vertical.</span><span class="sxs-lookup"><span data-stu-id="e2fa6-189">A value indicating the control's orientation: horizontal or vertical.</span></span>                                                                                                                                               |



 

## <a name="required-control-patterns"></a><span data-ttu-id="e2fa6-190">Padrões de controle necessários</span><span class="sxs-lookup"><span data-stu-id="e2fa6-190">Required Control Patterns</span></span>

<span data-ttu-id="e2fa6-191">A tabela a seguir lista os padrões de controle de automação da interface do usuário necessários para ter suporte para controles de barra de status.</span><span class="sxs-lookup"><span data-stu-id="e2fa6-191">The following table lists the UI Automation control patterns required to be supported for status bar controls.</span></span> <span data-ttu-id="e2fa6-192">Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="e2fa6-192">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="e2fa6-193">Padrão de controle</span><span class="sxs-lookup"><span data-stu-id="e2fa6-193">Control Pattern</span></span>                               | <span data-ttu-id="e2fa6-194">Suporte</span><span class="sxs-lookup"><span data-stu-id="e2fa6-194">Support</span></span>  | <span data-ttu-id="e2fa6-195">Observações</span><span class="sxs-lookup"><span data-stu-id="e2fa6-195">Notes</span></span>                                                                                                                                                                        |
|-----------------------------------------------|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e2fa6-196">**IGridProvider**</span><span class="sxs-lookup"><span data-stu-id="e2fa6-196">**IGridProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) | <span data-ttu-id="e2fa6-197">Opcional</span><span class="sxs-lookup"><span data-stu-id="e2fa6-197">Optional</span></span> | <span data-ttu-id="e2fa6-198">Os controles da barra de status devem dar suporte ao padrão de controle de [grade](uiauto-implementinggrid.md) para que partes individuais possam ser monitoradas e facilmente referenciadas por informações.</span><span class="sxs-lookup"><span data-stu-id="e2fa6-198">Status bar controls should support the [Grid](uiauto-implementinggrid.md) control pattern so that individual pieces can be monitored and easily referenced for information.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="e2fa6-199">Eventos necessários</span><span class="sxs-lookup"><span data-stu-id="e2fa6-199">Required Events</span></span>

<span data-ttu-id="e2fa6-200">A tabela a seguir lista os eventos de automação da interface do usuário aos quais os controles de barra de status são necessários para dar suporte.</span><span class="sxs-lookup"><span data-stu-id="e2fa6-200">The following table lists the UI Automation events that status bar controls are required to support.</span></span> <span data-ttu-id="e2fa6-201">Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="e2fa6-201">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="e2fa6-202">Evento de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="e2fa6-202">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="e2fa6-203">Observações</span><span class="sxs-lookup"><span data-stu-id="e2fa6-203">Notes</span></span>                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="e2fa6-204">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="e2fa6-204">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                   |
| <span data-ttu-id="e2fa6-205">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="e2fa6-205">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                   |
| <span data-ttu-id="e2fa6-206">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="e2fa6-206">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="e2fa6-207">Se o controle oferecer suporte à propriedade **IsEnabled** , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="e2fa6-207">If the control supports the **IsEnabled** property, it must support this event.</span></span>   |
| <span data-ttu-id="e2fa6-208">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="e2fa6-208">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="e2fa6-209">Se o controle oferecer suporte à propriedade **IsOffscreen** , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="e2fa6-209">If the control supports the **IsOffscreen** property, it must support this event.</span></span> |
| [<span data-ttu-id="e2fa6-210">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="e2fa6-210">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="e2fa6-211">Comentários</span><span class="sxs-lookup"><span data-stu-id="e2fa6-211">Remarks</span></span>

<span data-ttu-id="e2fa6-212">Recomendamos que os controles de edição sejam usados como elementos de grade filho em uma barra de status.</span><span class="sxs-lookup"><span data-stu-id="e2fa6-212">We recommend that edit controls be used as child grid elements in a status bar.</span></span> <span data-ttu-id="e2fa6-213">O uso de controles de edição facilita a associação do objetivo do campo status com seu valor usando o nome do elemento e a propriedade Value.</span><span class="sxs-lookup"><span data-stu-id="e2fa6-213">Using edit controls makes it easier to associate the purpose of the status field with its value by using the element name and value property.</span></span> <span data-ttu-id="e2fa6-214">Como os controles de texto não devem dar suporte ao padrão de controle de **valor** , eles não devem ser usados como elementos de grade filho.</span><span class="sxs-lookup"><span data-stu-id="e2fa6-214">Because text controls should not support the **Value** control pattern, they should not be used as child grid elements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e2fa6-215">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e2fa6-215">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="e2fa6-216">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="e2fa6-216">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e2fa6-217">Visão Geral dos Tipos de Controle de Automação de Interface do Usuário</span><span class="sxs-lookup"><span data-stu-id="e2fa6-217">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="e2fa6-218">Visão geral de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="e2fa6-218">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




