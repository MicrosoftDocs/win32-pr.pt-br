---
title: Tipo de controle TitleBar
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle TitleBar. Um controle da barra de título representa um título ou uma barra de legenda em uma janela.
ms.assetid: dc707198-ceb6-4fbf-ace4-8fec88c92b98
keywords:
- Automação da interface do usuário, suporte para tipo de controle TitleBar
- Automação da interface do usuário, tipo de controle TitleBar
- Automação da interface do usuário, estrutura de árvore para tipo de controle TitleBar
- Automação da interface do usuário, propriedades para tipo de controle TitleBar
- Automação da interface do usuário, padrões de controle para o tipo de controle TitleBar
- Automação da interface do usuário, eventos para tipo de controle TitleBar
- estruturas de árvore, tipo de controle TitleBar
- Propriedades, tipo de controle TitleBar
- padrões de controle, tipo de controle TitleBar
- eventos, tipo de controle TitleBar
- suporte para tipo de controle TitleBar
- Tipo de controle TitleBar
- tipos de controle, estrutura de árvore para o tipo de controle TitleBar
- tipos de controle, padrões de controle para o tipo de controle TitleBar
- tipos de controle, suporte para a TitleBar
- tipos de controle, TitleBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f9471d08479345bf8c1df118f720bf273d4d89d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916600"
---
# <a name="titlebar-control-type"></a><span data-ttu-id="0961a-120">Tipo de controle TitleBar</span><span class="sxs-lookup"><span data-stu-id="0961a-120">TitleBar Control Type</span></span>

<span data-ttu-id="0961a-121">Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle **TitleBar** .</span><span class="sxs-lookup"><span data-stu-id="0961a-121">This topic provides information about Microsoft UI Automation support for the **TitleBar** control type.</span></span> <span data-ttu-id="0961a-122">Um controle da barra de título representa um título ou uma barra de legenda em uma janela.</span><span class="sxs-lookup"><span data-stu-id="0961a-122">A title bar control represents a title or caption bar in a window.</span></span>

<span data-ttu-id="0961a-123">As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle **TitleBar** .</span><span class="sxs-lookup"><span data-stu-id="0961a-123">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **TitleBar** control type.</span></span> <span data-ttu-id="0961a-124">Os requisitos de automação da interface do usuário se aplicam a todos os controles da barra de título, em que a estrutura/plataforma da interface do usuário integra o suporte à automação da interface do usuário para tipos</span><span class="sxs-lookup"><span data-stu-id="0961a-124">The UI Automation requirements apply to all title bar controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="0961a-125">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="0961a-125">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="0961a-126">Estrutura de árvore típica</span><span class="sxs-lookup"><span data-stu-id="0961a-126">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="0961a-127">Propriedades relevantes</span><span class="sxs-lookup"><span data-stu-id="0961a-127">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="0961a-128">Padrões de controle necessários</span><span class="sxs-lookup"><span data-stu-id="0961a-128">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="0961a-129">Eventos necessários</span><span class="sxs-lookup"><span data-stu-id="0961a-129">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="0961a-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0961a-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="0961a-131">Estrutura de árvore típica</span><span class="sxs-lookup"><span data-stu-id="0961a-131">Typical Tree Structure</span></span>

<span data-ttu-id="0961a-132">A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence a controles de barra de título e descreve o que pode ser contido em cada exibição.</span><span class="sxs-lookup"><span data-stu-id="0961a-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to title bar controls and describes what can be contained in each view.</span></span> <span data-ttu-id="0961a-133">Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="0961a-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0961a-134">Exibição de controle</span><span class="sxs-lookup"><span data-stu-id="0961a-134">Control View</span></span></th>
<th><span data-ttu-id="0961a-135">Exibição de conteúdo</span><span class="sxs-lookup"><span data-stu-id="0961a-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="0961a-136">TitleBar</span><span class="sxs-lookup"><span data-stu-id="0961a-136">TitleBar</span></span>
<ul>
<li><span data-ttu-id="0961a-137">Menu (0 ou 1)</span><span class="sxs-lookup"><span data-stu-id="0961a-137">Menu (0 or 1)</span></span></li>
<li><span data-ttu-id="0961a-138">Botão (0 ou mais)</span><span class="sxs-lookup"><span data-stu-id="0961a-138">Button (0 or more)</span></span></li>
</ul></li>
</ul></td>
<td><span data-ttu-id="0961a-139">(Não aplicável; o controle da barra de título não tem conteúdo)</span><span class="sxs-lookup"><span data-stu-id="0961a-139">(Not applicable; the title bar control has no content)</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="0961a-140">Propriedades relevantes</span><span class="sxs-lookup"><span data-stu-id="0961a-140">Relevant Properties</span></span>

<span data-ttu-id="0961a-141">A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para o tipo de controle **TitleBar** .</span><span class="sxs-lookup"><span data-stu-id="0961a-141">The following table lists the UI Automation properties whose value or definition is especially relevant to the **TitleBar** control type.</span></span> <span data-ttu-id="0961a-142">Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="0961a-142">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="0961a-143">Propriedade de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="0961a-143">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="0961a-144">Valor</span><span class="sxs-lookup"><span data-stu-id="0961a-144">Value</span></span>        | <span data-ttu-id="0961a-145">Observações</span><span class="sxs-lookup"><span data-stu-id="0961a-145">Notes</span></span>                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0961a-146">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="0961a-146">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="0961a-147">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="0961a-147">See notes.</span></span>   | <span data-ttu-id="0961a-148">O valor dessa propriedade deve ser exclusivo entre todos os elementos de mesmo nível na exibição bruta da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="0961a-148">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                         |
| [<span data-ttu-id="0961a-149">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="0961a-149">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="0961a-150">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="0961a-150">See notes.</span></span>   | <span data-ttu-id="0961a-151">O valor exposto por essa propriedade deve incluir todos os controles contidos nela.</span><span class="sxs-lookup"><span data-stu-id="0961a-151">The value exposed by this property must include all of the controls contained within it.</span></span>                                                                                                             |
| [<span data-ttu-id="0961a-152">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="0961a-152">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="0961a-153">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="0961a-153">See notes.</span></span>   | <span data-ttu-id="0961a-154">Com suporte se houver um retângulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="0961a-154">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="0961a-155">Se nem todos os pontos dentro do retângulo delimitador forem clicáveis, o elemento executará testes de clique especializados, substituirá e fornecerá um ponto clicável.</span><span class="sxs-lookup"><span data-stu-id="0961a-155">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span> |
| [<span data-ttu-id="0961a-156">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="0961a-156">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="0961a-157">**TitleBar**</span><span class="sxs-lookup"><span data-stu-id="0961a-157">**TitleBar**</span></span> | <span data-ttu-id="0961a-158">Esse valor é o mesmo para todas as estruturas de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="0961a-158">This value is the same for all UI frameworks.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="0961a-159">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="0961a-159">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="0961a-160">FALSE</span><span class="sxs-lookup"><span data-stu-id="0961a-160">FALSE</span></span>        | <span data-ttu-id="0961a-161">O controle da barra de título nunca é incluído na exibição de conteúdo da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="0961a-161">The title bar control is never included in the content view of the UI Automation tree.</span></span>                                                                                                               |
| [<span data-ttu-id="0961a-162">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="0961a-162">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="0961a-163">TRUE</span><span class="sxs-lookup"><span data-stu-id="0961a-163">TRUE</span></span>         | <span data-ttu-id="0961a-164">O controle da barra de título sempre é incluído no modo de exibição de controle da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="0961a-164">The title bar control is always included in the control view of the UI Automation tree.</span></span>                                                                                                              |
| [<span data-ttu-id="0961a-165">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="0961a-165">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="0961a-166">FALSE</span><span class="sxs-lookup"><span data-stu-id="0961a-166">FALSE</span></span>        | <span data-ttu-id="0961a-167">Um controle de barra de título nunca tem foco no teclado.</span><span class="sxs-lookup"><span data-stu-id="0961a-167">A title bar control never has keyboard focus.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="0961a-168">**UIA \_ IsOffscreenPropertyId**</span><span class="sxs-lookup"><span data-stu-id="0961a-168">**UIA\_IsOffscreenPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="0961a-169">Depende</span><span class="sxs-lookup"><span data-stu-id="0961a-169">Depends</span></span>      | <span data-ttu-id="0961a-170">Um controle da barra de título retorna um valor dependendo se ele está visível na tela.</span><span class="sxs-lookup"><span data-stu-id="0961a-170">A title bar control returns a value depending on whether it is visible on the screen.</span></span>                                                                                                                |
| [<span data-ttu-id="0961a-171">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="0961a-171">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="0961a-172">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="0961a-172">See notes.</span></span>   | <span data-ttu-id="0961a-173">Um controle de barra de título normalmente não tem um rótulo.</span><span class="sxs-lookup"><span data-stu-id="0961a-173">A title bar control typically does not have a label.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="0961a-174">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="0961a-174">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="0961a-175">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="0961a-175">See notes.</span></span>   | <span data-ttu-id="0961a-176">Cadeia de caracteres localizada correspondente ao tipo de controle TitleBar.</span><span class="sxs-lookup"><span data-stu-id="0961a-176">Localized string corresponding to the TitleBar control type.</span></span> <span data-ttu-id="0961a-177">O valor padrão é "barra de título" para en-US ou inglês (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="0961a-177">The default value is "title bar" for en-US or English (United States).</span></span>                                                                  |
| [<span data-ttu-id="0961a-178">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="0961a-178">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="0961a-179">""</span><span class="sxs-lookup"><span data-stu-id="0961a-179">""</span></span>           | <span data-ttu-id="0961a-180">Uma barra de título não é conteúdo; suas informações textuais são expostas pelo nome da janela pai.</span><span class="sxs-lookup"><span data-stu-id="0961a-180">A title bar is not content; its textual information is exposed by the name of the parent window.</span></span>                                                                                                     |



 

## <a name="required-control-patterns"></a><span data-ttu-id="0961a-181">Padrões de controle necessários</span><span class="sxs-lookup"><span data-stu-id="0961a-181">Required Control Patterns</span></span>

<span data-ttu-id="0961a-182">O tipo de controle **TitleBar** não é necessário para dar suporte a nenhum padrão de controle.</span><span class="sxs-lookup"><span data-stu-id="0961a-182">The **TitleBar** control type is not required to support any control patterns.</span></span> <span data-ttu-id="0961a-183">Sua funcionalidade é exposta por meio do padrão de controle [Window](uiauto-implementingwindow.md) no tipo de controle [Window](uiauto-supportwindowcontroltype.md) .</span><span class="sxs-lookup"><span data-stu-id="0961a-183">Its functionality is exposed through the [Window](uiauto-implementingwindow.md) control pattern on the [Window](uiauto-supportwindowcontroltype.md) control type.</span></span>

## <a name="required-events"></a><span data-ttu-id="0961a-184">Eventos necessários</span><span class="sxs-lookup"><span data-stu-id="0961a-184">Required Events</span></span>

<span data-ttu-id="0961a-185">A tabela a seguir lista os eventos de automação da interface do usuário aos quais os controles de barra de título precisam dar suporte.</span><span class="sxs-lookup"><span data-stu-id="0961a-185">The following table lists the UI Automation events that title bar controls are required to support.</span></span> <span data-ttu-id="0961a-186">Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="0961a-186">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="0961a-187">Evento de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="0961a-187">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="0961a-188">Observações</span><span class="sxs-lookup"><span data-stu-id="0961a-188">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0961a-189">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="0961a-189">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="0961a-190">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="0961a-190">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="0961a-191">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="0961a-191">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="0961a-192">Se o controle oferecer suporte à propriedade [**IsEnabled**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="0961a-192">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="0961a-193">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="0961a-193">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="0961a-194">Se o controle oferecer suporte à propriedade [**IsOffscreen**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="0961a-194">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="0961a-195">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="0961a-195">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="0961a-196">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0961a-196">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="0961a-197">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="0961a-197">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0961a-198">Visão Geral dos Tipos de Controle de Automação de Interface do Usuário</span><span class="sxs-lookup"><span data-stu-id="0961a-198">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="0961a-199">Visão geral de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="0961a-199">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




