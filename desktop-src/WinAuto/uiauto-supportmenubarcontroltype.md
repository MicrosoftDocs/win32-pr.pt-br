---
title: Tipo de controle MenuBar
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle MenuBar.
ms.assetid: e93a92ce-7c98-4e8f-8a6a-a365ccb705d6
keywords:
- Automação da interface do usuário, suporte para tipo de controle MenuBar
- Automação da interface do usuário, tipo de controle MenuBar
- Automação da interface do usuário, estrutura de árvore para tipo de controle MenuBar
- Automação da interface do usuário, propriedades para tipo de controle MenuBar
- Automação da interface do usuário, padrões de controle para o tipo de controle MenuBar
- Automação da interface do usuário, eventos para tipo de controle MenuBar
- estruturas de árvore, tipo de controle MenuBar
- Propriedades, tipo de controle MenuBar
- padrões de controle, tipo de controle MenuBar
- eventos, tipo de controle MenuBar
- suporte para tipo de controle MenuBar
- Tipo de controle MenuBar
- tipos de controle, estrutura de árvore para tipo de controle MenuBar
- tipos de controle, padrões de controle para o tipo de controle MenuBar
- tipos de controle, suporte para MenuBar
- tipos de controle, BarraDeMenu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b94bb60c13b5999bc8020eb70b84f6c932a2fb94
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105781508"
---
# <a name="menubar-control-type"></a><span data-ttu-id="79703-119">Tipo de controle MenuBar</span><span class="sxs-lookup"><span data-stu-id="79703-119">MenuBar Control Type</span></span>

<span data-ttu-id="79703-120">Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle **MenuBar** .</span><span class="sxs-lookup"><span data-stu-id="79703-120">This topic provides information about Microsoft UI Automation support for the **MenuBar** control type.</span></span>

<span data-ttu-id="79703-121">Os controles de barra de menus são um exemplo de controles que implementam o tipo de controle **MenuBar** .</span><span class="sxs-lookup"><span data-stu-id="79703-121">Menu bar controls are an example of controls that implement the **MenuBar** control type.</span></span> <span data-ttu-id="79703-122">As barras de menu fornecem um meio para os usuários ativarem comandos e opções contidas em um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="79703-122">Menu bars provide a means for users to activate commands and options contained in an application.</span></span>

<span data-ttu-id="79703-123">As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle **MenuBar** .</span><span class="sxs-lookup"><span data-stu-id="79703-123">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **MenuBar** control type.</span></span> <span data-ttu-id="79703-124">Os requisitos de automação da interface do usuário se aplicam a todos os controles da barra de menus, em que a estrutura/plataforma da interface do usuário integra o suporte à automação da interface do usuário para tipos</span><span class="sxs-lookup"><span data-stu-id="79703-124">The UI Automation requirements apply to all menu bar controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="79703-125">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="79703-125">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="79703-126">Estrutura de árvore típica</span><span class="sxs-lookup"><span data-stu-id="79703-126">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="79703-127">Propriedades relevantes</span><span class="sxs-lookup"><span data-stu-id="79703-127">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="79703-128">Padrões de controle necessários</span><span class="sxs-lookup"><span data-stu-id="79703-128">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="79703-129">Eventos necessários</span><span class="sxs-lookup"><span data-stu-id="79703-129">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="79703-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="79703-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="79703-131">Estrutura de árvore típica</span><span class="sxs-lookup"><span data-stu-id="79703-131">Typical Tree Structure</span></span>

<span data-ttu-id="79703-132">A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence a controles de barra de menus e descreve o que pode ser contido em cada exibição.</span><span class="sxs-lookup"><span data-stu-id="79703-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to menu bar controls and describes what can be contained in each view.</span></span> <span data-ttu-id="79703-133">Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="79703-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="79703-134">Exibição de controle</span><span class="sxs-lookup"><span data-stu-id="79703-134">Control View</span></span></th>
<th><span data-ttu-id="79703-135">Exibição de conteúdo</span><span class="sxs-lookup"><span data-stu-id="79703-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="79703-136">MenuBar</span><span class="sxs-lookup"><span data-stu-id="79703-136">MenuBar</span></span>
<ul>
<li><span data-ttu-id="79703-137">MenuItem (1 ou mais)</span><span class="sxs-lookup"><span data-stu-id="79703-137">MenuItem (1 or more)</span></span></li>
<li><span data-ttu-id="79703-138">Outros controles (0 ou muitos)</span><span class="sxs-lookup"><span data-stu-id="79703-138">Other controls (0 or many)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="79703-139">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="79703-139">Not applicable</span></span>
<ul>
<li><span data-ttu-id="79703-140">MenuItem (1 ou mais)</span><span class="sxs-lookup"><span data-stu-id="79703-140">MenuItem (1 or more)</span></span></li>
<li><span data-ttu-id="79703-141">Outros controles (0 ou muitos)</span><span class="sxs-lookup"><span data-stu-id="79703-141">Other controls (0 or many)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="79703-142">Um controle barra de menus sempre aparece no modo de exibição de controle, mas não no modo de exibição de conteúdo porque ele geralmente não transmite informações significativas para o usuário final (a menos que o aplicativo contenha mais de uma barra de menus).</span><span class="sxs-lookup"><span data-stu-id="79703-142">A menu bar control always appears in the control view, but not in content view because it usually does not convey meaningful information to the end user (unless the application contains more than one menu bar).</span></span>

<span data-ttu-id="79703-143">Os clientes de automação da interface do usuário podem escutar o evento [**UIA \_ MenuModeStartEventId**](uiauto-event-ids.md) para garantir que eles sejam notificados consistentemente quando a interface do usuário entrar no modo de menu.</span><span class="sxs-lookup"><span data-stu-id="79703-143">UI Automation clients can listen for the [**UIA\_MenuModeStartEventId**](uiauto-event-ids.md) event to ensure that they are consistently notified when the UI enters menu mode.</span></span> <span data-ttu-id="79703-144">Quando o aplicativo está no modo de menu, toda a entrada do teclado pode ser capturada para navegação de menu (por exemplo, a digitação ' ' pode invocar o menu **salvar** em vez de digitar o caractere na área do cliente do aplicativo).</span><span class="sxs-lookup"><span data-stu-id="79703-144">When the application is in menu mode, all of the keyboard input may be captured for menu navigation (for example, typing 's' might invoke the **Save** menu instead of typing the character on the application client area).</span></span> <span data-ttu-id="79703-145">O evento **UIA \_ MenuModeStartEventId** deve preceder o primeiro evento [**UIA \_ MenuOpenedEventId**](uiauto-event-ids.md) para garantir a consistência lógica.</span><span class="sxs-lookup"><span data-stu-id="79703-145">The **UIA\_MenuModeStartEventId** event must precede the first [**UIA\_MenuOpenedEventId**](uiauto-event-ids.md) event to ensure logical consistency.</span></span> <span data-ttu-id="79703-146">O evento [**UIA \_ MenuModeEndEventId**](uiauto-event-ids.md) segue o último evento [**UIA \_ MenuClosedEventId**](uiauto-event-ids.md) .</span><span class="sxs-lookup"><span data-stu-id="79703-146">The [**UIA\_MenuModeEndEventId**](uiauto-event-ids.md) event follows the last [**UIA\_MenuClosedEventId**](uiauto-event-ids.md) event.</span></span> <span data-ttu-id="79703-147">Clicar em um item de menu também pode disparar imediatamente o evento **UIA \_ MenuModeStartEventId** , seguido por um evento **UIA \_ MenuOpenedEventId** .</span><span class="sxs-lookup"><span data-stu-id="79703-147">Clicking a menu item may also immediately trigger the **UIA\_MenuModeStartEventId** event, followed by a **UIA\_MenuOpenedEventId** event.</span></span>

<span data-ttu-id="79703-148">Um controle de barra de menus pode conter outros controles, como controles de edição e caixas de combinação, dentro de sua estrutura.</span><span class="sxs-lookup"><span data-stu-id="79703-148">A menu bar control can contain other controls, such as edit controls and combo boxes, within its structure.</span></span> <span data-ttu-id="79703-149">Esses controles adicionais correspondem aos "outros controles" listados acima nas exibições de controle e conteúdo.</span><span class="sxs-lookup"><span data-stu-id="79703-149">These additional controls correspond to the "other controls" listed above in the control and content views.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="79703-150">Propriedades relevantes</span><span class="sxs-lookup"><span data-stu-id="79703-150">Relevant Properties</span></span>

<span data-ttu-id="79703-151">A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para o tipo de controle **MenuBar** .</span><span class="sxs-lookup"><span data-stu-id="79703-151">The following table lists the UI Automation properties whose value or definition is especially relevant to the **MenuBar** control type.</span></span> <span data-ttu-id="79703-152">Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="79703-152">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="79703-153">Propriedade de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="79703-153">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="79703-154">Valor</span><span class="sxs-lookup"><span data-stu-id="79703-154">Value</span></span>       | <span data-ttu-id="79703-155">Observações</span><span class="sxs-lookup"><span data-stu-id="79703-155">Notes</span></span>                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="79703-156">**UIA \_ AcceleratorKeyPropertyId**</span><span class="sxs-lookup"><span data-stu-id="79703-156">**UIA\_AcceleratorKeyPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="79703-157">NULO</span><span class="sxs-lookup"><span data-stu-id="79703-157">NULL</span></span>        | <span data-ttu-id="79703-158">As barras de menu geralmente não têm teclas de aceleração.</span><span class="sxs-lookup"><span data-stu-id="79703-158">Menu bars usually do not have accelerator keys.</span></span>                                                                                                                                                                                          |
| [<span data-ttu-id="79703-159">**UIA \_ AccessKeyPropertyId**</span><span class="sxs-lookup"><span data-stu-id="79703-159">**UIA\_AccessKeyPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="79703-160">PRESSIONANDO</span><span class="sxs-lookup"><span data-stu-id="79703-160">"ALT"</span></span>       | <span data-ttu-id="79703-161">Pressionar a tecla ALT geralmente deve trazer o foco para a barra de menus dentro do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="79703-161">Pressing the ALT key should usually bring focus to the menu bar within the application.</span></span>                                                                                                                                                  |
| [<span data-ttu-id="79703-162">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="79703-162">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="79703-163">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="79703-163">See notes.</span></span>  | <span data-ttu-id="79703-164">O valor exposto por essa propriedade deve incluir todos os controles contidos nela.</span><span class="sxs-lookup"><span data-stu-id="79703-164">The value exposed by this property must include all of the controls contained within it.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="79703-165">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="79703-165">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="79703-166">**MenuBar**</span><span class="sxs-lookup"><span data-stu-id="79703-166">**MenuBar**</span></span> |                                                                                                                                                                                                                                          |
| [<span data-ttu-id="79703-167">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="79703-167">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="79703-168">FALSE</span><span class="sxs-lookup"><span data-stu-id="79703-168">FALSE</span></span>       | <span data-ttu-id="79703-169">O controle de barra de menus não está incluído na exibição de conteúdo da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="79703-169">The menu bar control is not included in the content view of the UI Automation tree.</span></span>                                                                                                                                                      |
| [<span data-ttu-id="79703-170">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="79703-170">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="79703-171">TRUE</span><span class="sxs-lookup"><span data-stu-id="79703-171">TRUE</span></span>        | <span data-ttu-id="79703-172">O controle barra de menus sempre é incluído na exibição de controle da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="79703-172">The menu bar control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                                                   |
| [<span data-ttu-id="79703-173">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="79703-173">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="79703-174">TRUE</span><span class="sxs-lookup"><span data-stu-id="79703-174">TRUE</span></span>        | <span data-ttu-id="79703-175">Os controles de barra de menus têm foco no teclado, pois os controles que eles contêm podem ter o foco do teclado.</span><span class="sxs-lookup"><span data-stu-id="79703-175">Menu bar controls are keyboard-focusable because the controls they contain can take keyboard focus.</span></span>                                                                                                                                      |
| [<span data-ttu-id="79703-176">**UIA \_ IsOffscreenPropertyId**</span><span class="sxs-lookup"><span data-stu-id="79703-176">**UIA\_IsOffscreenPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="79703-177">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="79703-177">See notes.</span></span>  | <span data-ttu-id="79703-178">O valor dessa propriedade depende de se o controle é visível na tela.</span><span class="sxs-lookup"><span data-stu-id="79703-178">The value of this property depends on whether the control is viewable on the screen.</span></span>                                                                                                                                                     |
| [<span data-ttu-id="79703-179">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="79703-179">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="79703-180">NULO</span><span class="sxs-lookup"><span data-stu-id="79703-180">NULL</span></span>        | <span data-ttu-id="79703-181">Os controles de barra de menus geralmente não têm um rótulo.</span><span class="sxs-lookup"><span data-stu-id="79703-181">Menu bar controls usually do not have a label.</span></span>                                                                                                                                                                                           |
| [<span data-ttu-id="79703-182">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="79703-182">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="79703-183">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="79703-183">See notes.</span></span>  | <span data-ttu-id="79703-184">Cadeia de caracteres localizada correspondente ao tipo de controle **MenuBar** .</span><span class="sxs-lookup"><span data-stu-id="79703-184">Localized string corresponding to the **MenuBar** control type.</span></span> <span data-ttu-id="79703-185">O valor padrão é "barra de menus" para en-US ou inglês (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="79703-185">The default value is "menu bar" for en-US or English (United States).</span></span>                                                                                                    |
| [<span data-ttu-id="79703-186">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="79703-186">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="79703-187">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="79703-187">See notes.</span></span>  | <span data-ttu-id="79703-188">O controle de barra de menus não precisa de um nome, a menos que um aplicativo tenha mais de uma barra de menus.</span><span class="sxs-lookup"><span data-stu-id="79703-188">The menu bar control does not need a name unless an application has more than one menu bar.</span></span> <span data-ttu-id="79703-189">Se houver mais de uma barra de menus em um aplicativo, use essa propriedade para expor nomes de distinção, como "formatação" ou "estrutura de tópicos".</span><span class="sxs-lookup"><span data-stu-id="79703-189">If there is more than one menu bar in an application, use this property to expose distinguishing names, such as "Formatting" or "Outlining".</span></span> |
| [<span data-ttu-id="79703-190">**UIA \_ OrientationPropertyId**</span><span class="sxs-lookup"><span data-stu-id="79703-190">**UIA\_OrientationPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="79703-191">Depende</span><span class="sxs-lookup"><span data-stu-id="79703-191">Depends</span></span>     | <span data-ttu-id="79703-192">Essa propriedade expõe se o controle de barra de menus é horizontal ou vertical.</span><span class="sxs-lookup"><span data-stu-id="79703-192">This property exposes whether the menu bar control is horizontal or vertical.</span></span>                                                                                                                                                            |



 

## <a name="required-control-patterns"></a><span data-ttu-id="79703-193">Padrões de controle necessários</span><span class="sxs-lookup"><span data-stu-id="79703-193">Required Control Patterns</span></span>

<span data-ttu-id="79703-194">A tabela a seguir lista os padrões de controle de automação da interface do usuário necessários para serem suportados por controles de barra de menus.</span><span class="sxs-lookup"><span data-stu-id="79703-194">The following table lists the UI Automation control patterns required to be supported by menu bar controls.</span></span> <span data-ttu-id="79703-195">Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="79703-195">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="79703-196">Padrão de controle</span><span class="sxs-lookup"><span data-stu-id="79703-196">Control Pattern</span></span>                                                   | <span data-ttu-id="79703-197">Suporte</span><span class="sxs-lookup"><span data-stu-id="79703-197">Support</span></span> | <span data-ttu-id="79703-198">Observações</span><span class="sxs-lookup"><span data-stu-id="79703-198">Notes</span></span>                                                                                                                                       |
|-------------------------------------------------------------------|---------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="79703-199">**IExpandCollapseProvider**</span><span class="sxs-lookup"><span data-stu-id="79703-199">**IExpandCollapseProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | <span data-ttu-id="79703-200">Depende</span><span class="sxs-lookup"><span data-stu-id="79703-200">Depends</span></span> | <span data-ttu-id="79703-201">Se o controle puder ser expandido ou recolhido, ele deverá implementar o padrão de controle [ExpandCollapse](uiauto-implementingexpandcollapse.md) .</span><span class="sxs-lookup"><span data-stu-id="79703-201">If the control can be expanded or collapsed, it must implement the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern.</span></span> |
| [<span data-ttu-id="79703-202">**IDockProvider**</span><span class="sxs-lookup"><span data-stu-id="79703-202">**IDockProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)                     | <span data-ttu-id="79703-203">Depende</span><span class="sxs-lookup"><span data-stu-id="79703-203">Depends</span></span> | <span data-ttu-id="79703-204">Se o controle puder ser encaixado em partes diferentes da tela, ele deverá implementar o padrão de controle [Dock](uiauto-implementingdock.md) .</span><span class="sxs-lookup"><span data-stu-id="79703-204">If the control can be docked to different parts of the screen, it must implement the [Dock](uiauto-implementingdock.md) control pattern.</span></span>   |
| [<span data-ttu-id="79703-205">**ITransformProvider**</span><span class="sxs-lookup"><span data-stu-id="79703-205">**ITransformProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider)           | <span data-ttu-id="79703-206">Depende</span><span class="sxs-lookup"><span data-stu-id="79703-206">Depends</span></span> | <span data-ttu-id="79703-207">Se o controle puder ser redimensionado, girado ou movido, ele deverá implementar o padrão de controle [Transform](uiauto-implementingtransform.md) .</span><span class="sxs-lookup"><span data-stu-id="79703-207">If the control can be resized, rotated, or moved, it must implement the [Transform](uiauto-implementingtransform.md) control pattern.</span></span>      |



 

## <a name="required-events"></a><span data-ttu-id="79703-208">Eventos necessários</span><span class="sxs-lookup"><span data-stu-id="79703-208">Required Events</span></span>

<span data-ttu-id="79703-209">A tabela a seguir lista os eventos de automação da interface do usuário aos quais os controles de barra de menu devem dar suporte.</span><span class="sxs-lookup"><span data-stu-id="79703-209">The following table lists the UI Automation events that menu bar controls are required to support.</span></span> <span data-ttu-id="79703-210">Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="79703-210">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="79703-211">Evento de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="79703-211">UI Automation Event</span></span>                                                                                                                                                | <span data-ttu-id="79703-212">Observações</span><span class="sxs-lookup"><span data-stu-id="79703-212">Notes</span></span>                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="79703-213">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="79703-213">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| <span data-ttu-id="79703-214">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="79703-214">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                              |                                                                                                                                  |
| <span data-ttu-id="79703-215">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ExpandCollapseExpandCollapseStatePropertyId.</span><span class="sxs-lookup"><span data-stu-id="79703-215">[**UIA\_ExpandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="79703-216">Se o controle der suporte ao padrão de controle [ExpandCollapse](uiauto-implementingexpandcollapse.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="79703-216">If the control supports the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern, it must support this event.</span></span> |
| <span data-ttu-id="79703-217">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="79703-217">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                              | <span data-ttu-id="79703-218">Se o controle oferecer suporte à propriedade [**IsEnabled**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="79703-218">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>         |
| <span data-ttu-id="79703-219">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="79703-219">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                          | <span data-ttu-id="79703-220">Se o controle oferecer suporte à propriedade [**IsOffscreen**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="79703-220">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>       |
| [<span data-ttu-id="79703-221">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="79703-221">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                               |                                                                                                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="79703-222">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="79703-222">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="79703-223">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="79703-223">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="79703-224">Visão Geral dos Tipos de Controle de Automação de Interface do Usuário</span><span class="sxs-lookup"><span data-stu-id="79703-224">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="79703-225">Visão geral de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="79703-225">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




