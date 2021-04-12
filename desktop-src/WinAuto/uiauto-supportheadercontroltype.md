---
title: Tipo de controle de cabeçalho
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle de cabeçalho.
ms.assetid: 032fc3a1-f939-40db-abbb-532afe309ba3
keywords:
- Automação da interface do usuário, suporte para tipo de controle de cabeçalho
- Automação da interface do usuário, tipo de controle de cabeçalho
- Automação da interface do usuário, estrutura de árvore para tipo de controle de cabeçalho
- Automação da interface do usuário, propriedades para tipo de controle de cabeçalho
- Automação da interface do usuário, padrões de controle para tipo de controle de cabeçalho
- Automação da interface do usuário, eventos para tipo de controle de cabeçalho
- estruturas de árvore, tipo de controle de cabeçalho
- Propriedades, tipo de controle de cabeçalho
- padrões de controle, tipo de controle de cabeçalho
- eventos, tipo de controle de cabeçalho
- suporte para tipo de controle de cabeçalho
- tipo Controle Cabeçalho
- tipos de controle, estrutura de árvore para tipo de controle de cabeçalho
- tipos de controle, padrões de controle para o tipo de controle de cabeçalho
- tipos de controle, suporte para cabeçalho
- tipos de controle, cabeçalho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c38ee0a00749888c624b627db247f2d01d24ff1c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363935"
---
# <a name="header-control-type"></a><span data-ttu-id="52f38-119">Tipo de controle de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="52f38-119">Header Control Type</span></span>

<span data-ttu-id="52f38-120">Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle de **cabeçalho** .</span><span class="sxs-lookup"><span data-stu-id="52f38-120">This topic provides information about Microsoft UI Automation support for the **Header** control type.</span></span>

<span data-ttu-id="52f38-121">O controle de cabeçalho fornece um contêiner Visual para os rótulos de linhas ou colunas de informações.</span><span class="sxs-lookup"><span data-stu-id="52f38-121">The header control provides a visual container for the labels for rows or columns of information.</span></span>

<span data-ttu-id="52f38-122">As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle de **cabeçalho** .</span><span class="sxs-lookup"><span data-stu-id="52f38-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Header** control type.</span></span> <span data-ttu-id="52f38-123">Os requisitos de automação da interface do usuário se aplicam a todos os controles de cabeçalho nos quais a plataforma/estrutura da interface do usuário integra o suporte à automação da interface do usuário para tipos de controle</span><span class="sxs-lookup"><span data-stu-id="52f38-123">The UI Automation requirements apply to all header controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="52f38-124">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="52f38-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="52f38-125">Estrutura de árvore típica</span><span class="sxs-lookup"><span data-stu-id="52f38-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="52f38-126">Propriedades relevantes</span><span class="sxs-lookup"><span data-stu-id="52f38-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="52f38-127">Padrões de controle necessários</span><span class="sxs-lookup"><span data-stu-id="52f38-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="52f38-128">Eventos necessários</span><span class="sxs-lookup"><span data-stu-id="52f38-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="52f38-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="52f38-129">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="52f38-130">Estrutura de árvore típica</span><span class="sxs-lookup"><span data-stu-id="52f38-130">Typical Tree Structure</span></span>

<span data-ttu-id="52f38-131">A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence a controles de cabeçalho e descreve o que pode ser contido em cada exibição.</span><span class="sxs-lookup"><span data-stu-id="52f38-131">The following table depicts a typical control and content view of the UI Automation tree that pertains to header controls and describes what can be contained in each view.</span></span> <span data-ttu-id="52f38-132">Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="52f38-132">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="52f38-133">Exibição de controle</span><span class="sxs-lookup"><span data-stu-id="52f38-133">Control View</span></span></th>
<th><span data-ttu-id="52f38-134">Exibição de conteúdo</span><span class="sxs-lookup"><span data-stu-id="52f38-134">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="52f38-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="52f38-135">Header</span></span>
<ul>
<li><span data-ttu-id="52f38-136">HeaderItem (1 ou mais)</span><span class="sxs-lookup"><span data-stu-id="52f38-136">HeaderItem (1 or more)</span></span></li>
</ul></li>
</ul></td>
<td><span data-ttu-id="52f38-137">(Não aplicável)</span><span class="sxs-lookup"><span data-stu-id="52f38-137">(Not applicable)</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="52f38-138">Controles de cabeçalho sempre têm um ou mais filhos na exibição de controle da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="52f38-138">Header controls always have one or more children in the control view of the UI Automation tree.</span></span>

<span data-ttu-id="52f38-139">Os controles de cabeçalho têm zero filhos na exibição de conteúdo da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="52f38-139">Header controls have zero children in the content view of the UI Automation tree.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="52f38-140">Propriedades relevantes</span><span class="sxs-lookup"><span data-stu-id="52f38-140">Relevant Properties</span></span>

<span data-ttu-id="52f38-141">A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para os controles de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="52f38-141">The following table lists the UI Automation properties whose value or definition is especially relevant to header controls.</span></span> <span data-ttu-id="52f38-142">Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="52f38-142">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="52f38-143">Propriedade de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="52f38-143">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="52f38-144">Valor</span><span class="sxs-lookup"><span data-stu-id="52f38-144">Value</span></span>                                                            | <span data-ttu-id="52f38-145">Observações</span><span class="sxs-lookup"><span data-stu-id="52f38-145">Notes</span></span>                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="52f38-146">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="52f38-146">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="52f38-147">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="52f38-147">See notes.</span></span>                                                       | <span data-ttu-id="52f38-148">O valor dessa propriedade deve ser exclusivo em todos os controles em um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="52f38-148">The value of this property must be unique across all controls in an application.</span></span>                                                                                                                     |
| [<span data-ttu-id="52f38-149">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="52f38-149">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="52f38-150">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="52f38-150">See notes.</span></span>                                                       | <span data-ttu-id="52f38-151">O retângulo mais externo que contém o controle inteiro.</span><span class="sxs-lookup"><span data-stu-id="52f38-151">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                             |
| [<span data-ttu-id="52f38-152">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="52f38-152">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="52f38-153">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="52f38-153">See notes.</span></span>                                                       | <span data-ttu-id="52f38-154">Com suporte se houver um retângulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="52f38-154">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="52f38-155">Se nem todos os pontos dentro do retângulo delimitador forem clicáveis, o elemento executará testes de clique especializados, substituirá e fornecerá um ponto clicável.</span><span class="sxs-lookup"><span data-stu-id="52f38-155">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span> |
| [<span data-ttu-id="52f38-156">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="52f38-156">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="52f38-157">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="52f38-157">**Header**</span></span>                                                       |                                                                                                                                                                                                      |
| [<span data-ttu-id="52f38-158">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="52f38-158">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="52f38-159">FALSE</span><span class="sxs-lookup"><span data-stu-id="52f38-159">FALSE</span></span>                                                            | <span data-ttu-id="52f38-160">O controle de cabeçalho não está incluído na exibição de conteúdo da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="52f38-160">The header control is not included in the content view of the UI Automation tree.</span></span>                                                                                                                    |
| [<span data-ttu-id="52f38-161">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="52f38-161">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="52f38-162">TRUE</span><span class="sxs-lookup"><span data-stu-id="52f38-162">TRUE</span></span>                                                             | <span data-ttu-id="52f38-163">O controle de cabeçalho é sempre incluído no modo de exibição de controle da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="52f38-163">The header control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                 |
| [<span data-ttu-id="52f38-164">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="52f38-164">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="52f38-165">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="52f38-165">See notes.</span></span>                                                       | <span data-ttu-id="52f38-166">Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="52f38-166">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                            |
| [<span data-ttu-id="52f38-167">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="52f38-167">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="52f38-168">NULO</span><span class="sxs-lookup"><span data-stu-id="52f38-168">NULL</span></span>                                                             | <span data-ttu-id="52f38-169">Os controles de cabeçalho não têm um rótulo estático.</span><span class="sxs-lookup"><span data-stu-id="52f38-169">Header controls do not have a static label.</span></span>                                                                                                                                                          |
| [<span data-ttu-id="52f38-170">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="52f38-170">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="52f38-171">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="52f38-171">See notes.</span></span>                                                       | <span data-ttu-id="52f38-172">O valor padrão é "header" para en-US ou inglês (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="52f38-172">The default value is "header" for en-US or English (United States).</span></span>                                                                                                                                  |
| [<span data-ttu-id="52f38-173">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="52f38-173">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="52f38-174">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="52f38-174">See notes.</span></span>                                                       | <span data-ttu-id="52f38-175">O controle de cabeçalho precisa de um nome se houver mais de um cabeçalho de linha ou mais de um cabeçalho de coluna.</span><span class="sxs-lookup"><span data-stu-id="52f38-175">The header control needs a name if there is more than one row header or more than one column header.</span></span> <span data-ttu-id="52f38-176">Isso identifica as informações dentro do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="52f38-176">This identifies the information within the header.</span></span>                                              |
| [<span data-ttu-id="52f38-177">**UIA \_ OrientationPropertyId**</span><span class="sxs-lookup"><span data-stu-id="52f38-177">**UIA\_OrientationPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="52f38-178">**\_ OrientationType Horizontal** ou **OrientationType \_ vertical**</span><span class="sxs-lookup"><span data-stu-id="52f38-178">**OrientationType\_Horizontal** or **OrientationType\_Vertical**</span></span> | <span data-ttu-id="52f38-179">O valor dessa propriedade expõe a posição do controle de cabeçalho — seja um cabeçalho de linha (**OrientationType \_ horizontal**) ou um cabeçalho de coluna (**OrientationType \_ vertical**).</span><span class="sxs-lookup"><span data-stu-id="52f38-179">The value of this property exposes the position of the header control—whether it is a row header (**OrientationType\_Horizontal**) or column header (**OrientationType\_Vertical**).</span></span>                 |



 

## <a name="required-control-patterns"></a><span data-ttu-id="52f38-180">Padrões de controle necessários</span><span class="sxs-lookup"><span data-stu-id="52f38-180">Required Control Patterns</span></span>

<span data-ttu-id="52f38-181">A tabela a seguir lista os padrões de controle de automação da interface do usuário que devem ter suporte para controles de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="52f38-181">The following table lists the UI Automation control patterns required to be supported for header controls.</span></span> <span data-ttu-id="52f38-182">Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="52f38-182">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="52f38-183">Padrão de controle</span><span class="sxs-lookup"><span data-stu-id="52f38-183">Control Pattern</span></span>                                         | <span data-ttu-id="52f38-184">Suporte</span><span class="sxs-lookup"><span data-stu-id="52f38-184">Support</span></span> | <span data-ttu-id="52f38-185">Observações</span><span class="sxs-lookup"><span data-stu-id="52f38-185">Notes</span></span>                                                                                                             |
|---------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="52f38-186">**ITransformProvider**</span><span class="sxs-lookup"><span data-stu-id="52f38-186">**ITransformProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | <span data-ttu-id="52f38-187">Depende</span><span class="sxs-lookup"><span data-stu-id="52f38-187">Depends</span></span> | <span data-ttu-id="52f38-188">Implemente o padrão de controle [Transform](uiauto-implementingtransform.md) se o controle de cabeçalho puder ser redimensionado.</span><span class="sxs-lookup"><span data-stu-id="52f38-188">Implement the [Transform](uiauto-implementingtransform.md) control pattern if the header control can be resized.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="52f38-189">Eventos necessários</span><span class="sxs-lookup"><span data-stu-id="52f38-189">Required Events</span></span>

<span data-ttu-id="52f38-190">A tabela a seguir lista os eventos de automação da interface do usuário aos quais os controles de cabeçalho são necessários para dar suporte.</span><span class="sxs-lookup"><span data-stu-id="52f38-190">The following table lists the UI Automation events that header controls are required to support.</span></span> <span data-ttu-id="52f38-191">Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="52f38-191">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="52f38-192">Evento de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="52f38-192">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="52f38-193">Observações</span><span class="sxs-lookup"><span data-stu-id="52f38-193">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="52f38-194">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="52f38-194">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="52f38-195">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="52f38-195">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="52f38-196">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="52f38-196">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="52f38-197">Se o controle oferecer suporte à propriedade [**IsEnabled**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="52f38-197">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="52f38-198">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="52f38-198">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="52f38-199">Se o controle oferecer suporte à propriedade [**IsOffscreen**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="52f38-199">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="52f38-200">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="52f38-200">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="52f38-201">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="52f38-201">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="52f38-202">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="52f38-202">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="52f38-203">Visão Geral dos Tipos de Controle de Automação de Interface do Usuário</span><span class="sxs-lookup"><span data-stu-id="52f38-203">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="52f38-204">Visão geral de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="52f38-204">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




