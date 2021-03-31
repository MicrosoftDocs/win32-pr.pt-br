---
title: Tipo de controle de menu
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle de menu.
ms.assetid: cdbb6db7-63d7-422e-952c-7b59779fefbe
keywords:
- Automação da interface do usuário, suporte para tipo de controle de menu
- Automação da interface do usuário, tipo de controle de menu
- Automação da interface do usuário, estrutura de árvore para tipo de controle de menu
- Automação da interface do usuário, propriedades para tipo de controle de menu
- Automação da interface do usuário, padrões de controle para tipo de controle de menu
- Automação da interface do usuário, eventos para tipo de controle de menu
- estruturas de árvore, tipo de controle de menu
- Propriedades, tipo de controle de menu
- padrões de controle, tipo de controle de menu
- eventos, tipo de controle de menu
- suporte para tipo de controle de menu
- tipo de controle Menu
- tipos de controle, estrutura de árvore para tipo de controle de menu
- tipos de controle, padrões de controle para tipo de controle de menu
- tipos de controle, suporte para menu
- tipos de controle, menu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edee9f30f4d4cea123a2c7f5ff4dac235782faea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005410"
---
# <a name="menu-control-type"></a><span data-ttu-id="51690-119">Tipo de controle de menu</span><span class="sxs-lookup"><span data-stu-id="51690-119">Menu Control Type</span></span>

<span data-ttu-id="51690-120">Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle de **menu** .</span><span class="sxs-lookup"><span data-stu-id="51690-120">This topic provides information about Microsoft UI Automation support for the **Menu** control type.</span></span>

<span data-ttu-id="51690-121">Um controle de menu permite a organização hierárquica de elementos associados a comandos e manipuladores de eventos.</span><span class="sxs-lookup"><span data-stu-id="51690-121">A menu control allows hierarchal organization of elements associated with commands and event handlers.</span></span> <span data-ttu-id="51690-122">Em um aplicativo típico do Microsoft Windows, uma barra de menus contém vários botões de menu (como **arquivo**, **Editar** e **janela**) e cada botão de menu exibe um menu.</span><span class="sxs-lookup"><span data-stu-id="51690-122">In a typical Microsoft Windows application, a menu bar contains several menu buttons (such as **File**, **Edit**, and **Window**), and each menu button displays a menu.</span></span> <span data-ttu-id="51690-123">Um menu contém uma coleção de itens de menu (como **novo**, **aberto** e **fechado**), que pode ser expandida para exibir itens de menu adicionais ou para executar uma ação específica quando clicado.</span><span class="sxs-lookup"><span data-stu-id="51690-123">A menu contains a collection of menu items (such as **New**, **Open**, and **Close**), which can be expanded to display additional menu items or to perform a specific action when clicked.</span></span>

<span data-ttu-id="51690-124">As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle de **menu** .</span><span class="sxs-lookup"><span data-stu-id="51690-124">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Menu** control type.</span></span> <span data-ttu-id="51690-125">Os requisitos de automação da interface do usuário se aplicam a todos os controles de menu em que a estrutura/plataforma da interface do usuário integra o suporte à automação da interface do usuário para tipos de controle</span><span class="sxs-lookup"><span data-stu-id="51690-125">The UI Automation requirements apply to all menu controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="51690-126">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="51690-126">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="51690-127">Estrutura de árvore típica</span><span class="sxs-lookup"><span data-stu-id="51690-127">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="51690-128">Propriedades relevantes</span><span class="sxs-lookup"><span data-stu-id="51690-128">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="51690-129">Padrões de controle necessários</span><span class="sxs-lookup"><span data-stu-id="51690-129">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="51690-130">Eventos necessários</span><span class="sxs-lookup"><span data-stu-id="51690-130">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="51690-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="51690-131">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="51690-132">Estrutura de árvore típica</span><span class="sxs-lookup"><span data-stu-id="51690-132">Typical Tree Structure</span></span>

<span data-ttu-id="51690-133">A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence a controles de menu e descreve o que pode ser contido em cada exibição.</span><span class="sxs-lookup"><span data-stu-id="51690-133">The following table depicts a typical control and content view of the UI Automation tree that pertains to menu controls and describes what can be contained in each view.</span></span> <span data-ttu-id="51690-134">Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="51690-134">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="51690-135">Exibição de controle</span><span class="sxs-lookup"><span data-stu-id="51690-135">Control View</span></span></th>
<th><span data-ttu-id="51690-136">Exibição de conteúdo</span><span class="sxs-lookup"><span data-stu-id="51690-136">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="51690-137">Menu</span><span class="sxs-lookup"><span data-stu-id="51690-137">Menu</span></span>
<ul>
<li><span data-ttu-id="51690-138">MenuItem (1 ou muitos)</span><span class="sxs-lookup"><span data-stu-id="51690-138">MenuItem (1 or many)</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="51690-139">Outros controles (0 ou muitos)</span><span class="sxs-lookup"><span data-stu-id="51690-139">Other controls (0 or many)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="51690-140">Menu</span><span class="sxs-lookup"><span data-stu-id="51690-140">Menu</span></span>
<ul>
<li><span data-ttu-id="51690-141">MenuItem (1 ou muitos)</span><span class="sxs-lookup"><span data-stu-id="51690-141">MenuItem (1 or many)</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="51690-142">Outros controles (0 ou muitos)</span><span class="sxs-lookup"><span data-stu-id="51690-142">Other controls (0 or many)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="51690-143">Os controles de menu sempre aparecem na exibição de controle e na exibição de conteúdo da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="51690-143">Menu controls always appear in the control view and the content view of the UI Automation tree.</span></span> <span data-ttu-id="51690-144">Os controles de menu devem aparecer sob o controle ao qual suas informações se referem.</span><span class="sxs-lookup"><span data-stu-id="51690-144">Menu controls should appear under the control that their information is referring to.</span></span> <span data-ttu-id="51690-145">Os clientes de automação da interface do usuário podem escutar [**\_ MenuOpenedEventId UIA**](uiauto-event-ids.md) para garantir que eles obtenham consistentemente as informações transmitidas por controles de menu.</span><span class="sxs-lookup"><span data-stu-id="51690-145">UI Automation clients can listen for [**UIA\_MenuOpenedEventId**](uiauto-event-ids.md) to ensure that they consistently obtain information conveyed by menu controls.</span></span> <span data-ttu-id="51690-146">Os controles de menu de contexto são um caso especial.</span><span class="sxs-lookup"><span data-stu-id="51690-146">Context menu controls are a special case.</span></span> <span data-ttu-id="51690-147">Eles podem aparecer como filhos da área de trabalho ou de uma janela de aplicativo de nível superior.</span><span class="sxs-lookup"><span data-stu-id="51690-147">They may appear as children of the desktop or of a top level application window.</span></span>

<span data-ttu-id="51690-148">Um controle de menu pode conter outros controles, como controles de edição e caixas de combinação, dentro de sua estrutura.</span><span class="sxs-lookup"><span data-stu-id="51690-148">A menu control can contain other controls, such as edit controls and combo boxes, within its structure.</span></span> <span data-ttu-id="51690-149">Esses controles adicionais correspondem aos "outros controles" listados na tabela anterior nas exibições de controle e conteúdo.</span><span class="sxs-lookup"><span data-stu-id="51690-149">These additional controls correspond to the "other controls" listed in the previous table in the control and content views.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="51690-150">Propriedades relevantes</span><span class="sxs-lookup"><span data-stu-id="51690-150">Relevant Properties</span></span>

<span data-ttu-id="51690-151">A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para o tipo de controle de **menu** .</span><span class="sxs-lookup"><span data-stu-id="51690-151">The following table lists the UI Automation properties whose value or definition is especially relevant to the **Menu** control type.</span></span> <span data-ttu-id="51690-152">Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="51690-152">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="51690-153">Propriedade de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="51690-153">UI Automation Property</span></span>                                                                                      | <span data-ttu-id="51690-154">Valor</span><span class="sxs-lookup"><span data-stu-id="51690-154">Value</span></span>      | <span data-ttu-id="51690-155">Observações</span><span class="sxs-lookup"><span data-stu-id="51690-155">Notes</span></span>                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="51690-156">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="51690-156">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)           | <span data-ttu-id="51690-157">**Menu**</span><span class="sxs-lookup"><span data-stu-id="51690-157">**Menu**</span></span>   |                                                                                                                                                                         |
| [<span data-ttu-id="51690-158">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="51690-158">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="51690-159">TRUE</span><span class="sxs-lookup"><span data-stu-id="51690-159">TRUE</span></span>       | <span data-ttu-id="51690-160">O controle menu é sempre incluído na exibição de conteúdo da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="51690-160">The menu control is always included in the content view of the UI Automation tree.</span></span>                                                                                      |
| [<span data-ttu-id="51690-161">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="51690-161">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="51690-162">TRUE</span><span class="sxs-lookup"><span data-stu-id="51690-162">TRUE</span></span>       | <span data-ttu-id="51690-163">O controle menu é sempre incluído no modo de exibição de controle da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="51690-163">The menu control is always included in the control view of the UI Automation tree.</span></span>                                                                                      |
| [<span data-ttu-id="51690-164">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="51690-164">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)               | <span data-ttu-id="51690-165">NULO</span><span class="sxs-lookup"><span data-stu-id="51690-165">NULL</span></span>       | <span data-ttu-id="51690-166">Nenhum rótulo é previsto com um controle de menu típico.</span><span class="sxs-lookup"><span data-stu-id="51690-166">No label is anticipated with a typical menu control.</span></span>                                                                                                                    |
| [<span data-ttu-id="51690-167">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="51690-167">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                         | <span data-ttu-id="51690-168">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="51690-168">See notes.</span></span> | <span data-ttu-id="51690-169">O controle de menu não exige a definição de uma propriedade **Name** ou pode ter o mesmo nome que o controle associado, como um item de menu que abriu o submenu.</span><span class="sxs-lookup"><span data-stu-id="51690-169">The menu control does not require a **Name** property to be set, or it could have the same name as the associated control, such as a menu item that opened the submenu.</span></span> |



 

## <a name="required-control-patterns"></a><span data-ttu-id="51690-170">Padrões de controle necessários</span><span class="sxs-lookup"><span data-stu-id="51690-170">Required Control Patterns</span></span>

<span data-ttu-id="51690-171">Não há padrões de controle necessários para o tipo de controle de menu.</span><span class="sxs-lookup"><span data-stu-id="51690-171">There are no required control patterns for the Menu control type.</span></span>

## <a name="required-events"></a><span data-ttu-id="51690-172">Eventos necessários</span><span class="sxs-lookup"><span data-stu-id="51690-172">Required Events</span></span>

<span data-ttu-id="51690-173">Os controles de menu devem gerar o evento [**UIA \_ MenuOpenedEventId**](uiauto-event-ids.md) quando eles aparecerem na tela.</span><span class="sxs-lookup"><span data-stu-id="51690-173">Menu controls must raise the [**UIA\_MenuOpenedEventId**](uiauto-event-ids.md) event when they appear on the screen.</span></span> <span data-ttu-id="51690-174">O evento **UIA \_ MenuOpenedEventId** incluirá o texto do controle.</span><span class="sxs-lookup"><span data-stu-id="51690-174">The **UIA\_MenuOpenedEventId** event will include the text of the control.</span></span> <span data-ttu-id="51690-175">O evento [**UIA \_ MenuClosedEventId**](uiauto-event-ids.md) deve ser gerado quando um menu desaparece da tela.</span><span class="sxs-lookup"><span data-stu-id="51690-175">The [**UIA\_MenuClosedEventId**](uiauto-event-ids.md) event must be raised when a menu disappears from the screen.</span></span>

<span data-ttu-id="51690-176">A tabela a seguir lista os eventos de automação da interface do usuário aos quais os controles de menu são necessários para dar suporte.</span><span class="sxs-lookup"><span data-stu-id="51690-176">The following table lists the UI Automation events that menu controls are required to support.</span></span> <span data-ttu-id="51690-177">Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="51690-177">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="51690-178">Evento de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="51690-178">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="51690-179">Observações</span><span class="sxs-lookup"><span data-stu-id="51690-179">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="51690-180">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="51690-180">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="51690-181">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="51690-181">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="51690-182">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="51690-182">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="51690-183">Se o controle oferecer suporte à propriedade [**IsEnabled**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="51690-183">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="51690-184">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="51690-184">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="51690-185">Se o controle oferecer suporte à propriedade [**IsOffscreen**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="51690-185">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="51690-186">**UIA \_ MenuClosedEventId**</span><span class="sxs-lookup"><span data-stu-id="51690-186">**UIA\_MenuClosedEventId**</span></span>](uiauto-event-ids.md)                                                              |                                                                                                                            |
| [<span data-ttu-id="51690-187">**UIA \_ MenuOpenedEventId**</span><span class="sxs-lookup"><span data-stu-id="51690-187">**UIA\_MenuOpenedEventId**</span></span>](uiauto-event-ids.md)                                                              |                                                                                                                            |
| [<span data-ttu-id="51690-188">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="51690-188">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="51690-189">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="51690-189">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="51690-190">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="51690-190">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="51690-191">Visão Geral dos Tipos de Controle de Automação de Interface do Usuário</span><span class="sxs-lookup"><span data-stu-id="51690-191">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="51690-192">Visão geral de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="51690-192">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




