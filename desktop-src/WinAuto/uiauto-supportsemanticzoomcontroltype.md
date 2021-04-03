---
title: Tipo de controle SemanticZoom
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário para o tipo de controle SemanticZoom.
ms.assetid: 37C14610-431F-46BF-97B6-CB476EA1642D
keywords:
- Automação da interface do usuário, suporte para tipo de controle SemanticZoom
- Automação da interface do usuário, tipo de controle SemanticZoom
- Automação da interface do usuário, estrutura de árvore para tipo de controle SemanticZoom
- Automação da interface do usuário, propriedades para tipo de controle SemanticZoom
- Automação da interface do usuário, padrões de controle para o tipo de controle SemanticZoom
- Automação da interface do usuário, eventos para o tipo de controle SemanticZoom
- estruturas de árvore, tipo de controle SemanticZoom
- Propriedades, tipo de controle SemanticZoom
- padrões de controle, tipo de controle SemanticZoom
- eventos, tipo de controle SemanticZoom
- suporte para tipo de controle SemanticZoom
- Tipo de controle SemanticZoom
- tipos de controle, estrutura de árvore para o tipo de controle SemanticZoom
- tipos de controle, padrões de controle para o tipo de controle SemanticZoom
- tipos de controle, suporte para SemanticZoom
- tipos de controle, SemanticZoom
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b17d4712aa4f10489081b1b5d0f69fed849080bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084564"
---
# <a name="semanticzoom-control-type"></a><span data-ttu-id="a760e-119">Tipo de controle SemanticZoom</span><span class="sxs-lookup"><span data-stu-id="a760e-119">SemanticZoom Control Type</span></span>

<span data-ttu-id="a760e-120">Este tópico fornece informações sobre o suporte de automação da interface do usuário para o tipo de controle **SemanticZoom** .</span><span class="sxs-lookup"><span data-stu-id="a760e-120">This topic provides information about UI Automation support for the **SemanticZoom** control type.</span></span>

<span data-ttu-id="a760e-121">O zoom semântico é uma técnica introduzida no Windows 8 para apresentar e navegar por grandes conjuntos de dados ou conteúdo relacionados em uma única exibição, como um álbum de fotos, uma lista de aplicativos ou um catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="a760e-121">Semantic Zoom is a technique introduced in Windows 8 for presenting and navigating large sets of related data or content within a single view, such as a photo album, app list, or address book.</span></span> <span data-ttu-id="a760e-122">O zoom semântico usa dois modos distintos de classificação, ou *níveis de zoom*, para organizar e apresentar o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="a760e-122">Semantic Zoom uses two distinct modes of classification, or *zoom levels*, for organizing and presenting the content.</span></span> <span data-ttu-id="a760e-123">O modo de baixo nível (ou *ampliado*) exibe itens em uma estrutura simples, "tudo para cima"; e o modo de alto nível (ou *zoom*) exibe itens em grupos, permitindo que o usuário navegue e navegue rapidamente pelo conteúdo.</span><span class="sxs-lookup"><span data-stu-id="a760e-123">The low-level (or *zoomed in*) mode displays items in a flat, "all-up" structure; and the high-level (or *zoomed out*) mode displays items in groups, enabling the user to quickly navigate and browse through the content.</span></span> <span data-ttu-id="a760e-124">Por exemplo, aplicar zoom em uma lista de cidades pode mudar para uma lista de Estados que contém essas cidades.</span><span class="sxs-lookup"><span data-stu-id="a760e-124">For example, zooming a list of cities might change to a list of states containing those cities.</span></span> <span data-ttu-id="a760e-125">O zoom de uma lista de programas pode ser alterado para uma lista de grupos de programas lógicos.</span><span class="sxs-lookup"><span data-stu-id="a760e-125">Zooming a list of programs might change to a list of logical program groups.</span></span>

<span data-ttu-id="a760e-126">Para obter mais informações sobre o zoom semântico especificamente como usado para aplicativos da Windows Store, consulte [diretrizes para zoom semântico](/windows/uwp/controls-and-patterns/semantic-zoom).</span><span class="sxs-lookup"><span data-stu-id="a760e-126">For more information about Semantic Zoom specifically as used for Windows Store apps, see [Guidelines for Semantic Zoom](/windows/uwp/controls-and-patterns/semantic-zoom).</span></span>

<span data-ttu-id="a760e-127">O modelo de uso para o tipo de controle **SemanticZoom** é incomum, pois ele existe principalmente para acesso programático.</span><span class="sxs-lookup"><span data-stu-id="a760e-127">The usage model for the **SemanticZoom** control type is unusual in that it exists mainly for programmatic access.</span></span> <span data-ttu-id="a760e-128">Os clientes de automação da interface do usuário da Microsoft podem monitorar e manipular o controle de zoom semântico para controlar o estado de zoom da lista.</span><span class="sxs-lookup"><span data-stu-id="a760e-128">Microsoft UI Automation clients can monitor and manipulate the Semantic Zoom control to control the zoomed-in state of the list.</span></span> <span data-ttu-id="a760e-129">Os usuários que não estão usando tecnologia assistencial normalmente manipulariam o controle de zoom semântico diretamente por meio de gestos de toque ou atalhos de teclado.</span><span class="sxs-lookup"><span data-stu-id="a760e-129">Users who are not using assistive technology would typically manipulate the Semantic Zoom control directly through touch gestures or keyboard shortcuts.</span></span>

<span data-ttu-id="a760e-130">As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle **SemanticZoom** .</span><span class="sxs-lookup"><span data-stu-id="a760e-130">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **SemanticZoom** control type.</span></span> <span data-ttu-id="a760e-131">Os requisitos de automação da interface do usuário se aplicam a todos os controles de zoom semânticos, em que a estrutura da interface do usuário/plataforma integra o suporte à automação da interface do usuário para tipos</span><span class="sxs-lookup"><span data-stu-id="a760e-131">The UI Automation requirements apply to all Semantic Zoom controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="a760e-132">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="a760e-132">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="a760e-133">Estrutura de árvore típica</span><span class="sxs-lookup"><span data-stu-id="a760e-133">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="a760e-134">Propriedades relevantes</span><span class="sxs-lookup"><span data-stu-id="a760e-134">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="a760e-135">Propriedades e padrões de controle necessários</span><span class="sxs-lookup"><span data-stu-id="a760e-135">Required Control Patterns and Properties</span></span>](#required-control-patterns-and-properties)
-   [<span data-ttu-id="a760e-136">Eventos necessários</span><span class="sxs-lookup"><span data-stu-id="a760e-136">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="a760e-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="a760e-137">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="a760e-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a760e-138">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="a760e-139">Estrutura de árvore típica</span><span class="sxs-lookup"><span data-stu-id="a760e-139">Typical Tree Structure</span></span>

<span data-ttu-id="a760e-140">A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence ao tipo de controle **SemanticZoom** e descreve o que pode ser contido em cada exibição.</span><span class="sxs-lookup"><span data-stu-id="a760e-140">The following table depicts a typical control and content view of the UI Automation tree that pertains to the **SemanticZoom** control type and describes what can be contained in each view.</span></span> <span data-ttu-id="a760e-141">Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="a760e-141">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a760e-142">Exibição de controle</span><span class="sxs-lookup"><span data-stu-id="a760e-142">Control View</span></span></th>
<th><span data-ttu-id="a760e-143">Exibição de conteúdo</span><span class="sxs-lookup"><span data-stu-id="a760e-143">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="a760e-144">Lista</span><span class="sxs-lookup"><span data-stu-id="a760e-144">List</span></span>
<ul>
<li><span data-ttu-id="a760e-145">SemanticZoom</span><span class="sxs-lookup"><span data-stu-id="a760e-145">[SemanticZoom]</span></span>
<ul>
<li><span data-ttu-id="a760e-146">ListItem (0 ou mais)</span><span class="sxs-lookup"><span data-stu-id="a760e-146">ListItem (0 or more)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="a760e-147">Lista</span><span class="sxs-lookup"><span data-stu-id="a760e-147">List</span></span>
<ul>
<li><span data-ttu-id="a760e-148">ListItem (0 ou mais)</span><span class="sxs-lookup"><span data-stu-id="a760e-148">ListItem (0 or more)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="a760e-149">Ou:</span><span class="sxs-lookup"><span data-stu-id="a760e-149">Or:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a760e-150">Exibição de controle</span><span class="sxs-lookup"><span data-stu-id="a760e-150">Control View</span></span></th>
<th><span data-ttu-id="a760e-151">Exibição de conteúdo</span><span class="sxs-lookup"><span data-stu-id="a760e-151">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="a760e-152">SemanticZoom</span><span class="sxs-lookup"><span data-stu-id="a760e-152">[SemanticZoom]</span></span>
<ul>
<li><span data-ttu-id="a760e-153">Lista</span><span class="sxs-lookup"><span data-stu-id="a760e-153">List</span></span>
<ul>
<li><span data-ttu-id="a760e-154">ListItem (0 ou mais)</span><span class="sxs-lookup"><span data-stu-id="a760e-154">ListItem (0 or more)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="a760e-155">Lista</span><span class="sxs-lookup"><span data-stu-id="a760e-155">List</span></span>
<ul>
<li><span data-ttu-id="a760e-156">ListItem (0 ou mais)</span><span class="sxs-lookup"><span data-stu-id="a760e-156">ListItem (0 or more)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="a760e-157">Propriedades relevantes</span><span class="sxs-lookup"><span data-stu-id="a760e-157">Relevant Properties</span></span>

<span data-ttu-id="a760e-158">A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para os controles que implementam o tipo de controle **SemanticZoom** .</span><span class="sxs-lookup"><span data-stu-id="a760e-158">The following table lists the UI Automation properties whose value or definition is especially relevant to the controls that implement the **SemanticZoom** control type.</span></span> <span data-ttu-id="a760e-159">Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="a760e-159">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a760e-160">Propriedade de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="a760e-160">UI Automation Property</span></span></th>
<th><span data-ttu-id="a760e-161">Valor</span><span class="sxs-lookup"><span data-stu-id="a760e-161">Value</span></span></th>
<th><span data-ttu-id="a760e-162">Observações</span><span class="sxs-lookup"><span data-stu-id="a760e-162">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a760e-163"><a href="uiauto-automation-element-propids.md"><strong>UIA_AutomationIdPropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="a760e-163"><a href="uiauto-automation-element-propids.md"><strong>UIA_AutomationIdPropertyId</strong></a></span></span></td>
<td><span data-ttu-id="a760e-164">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="a760e-164">See notes.</span></span></td>
<td><span data-ttu-id="a760e-165">O valor dessa propriedade deve ser exclusivo entre todos os elementos de mesmo nível na exibição bruta da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="a760e-165">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a760e-166"><a href="uiauto-automation-element-propids.md"><strong>UIA_BoundingRectanglePropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="a760e-166"><a href="uiauto-automation-element-propids.md"><strong>UIA_BoundingRectanglePropertyId</strong></a></span></span></td>
<td><span data-ttu-id="a760e-167">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="a760e-167">See notes.</span></span></td>
<td><span data-ttu-id="a760e-168">O retângulo mais externo que contém o controle inteiro.</span><span class="sxs-lookup"><span data-stu-id="a760e-168">The outermost rectangle that contains the whole control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a760e-169"><a href="uiauto-automation-element-propids.md"><strong>UIA_ClickablePointPropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="a760e-169"><a href="uiauto-automation-element-propids.md"><strong>UIA_ClickablePointPropertyId</strong></a></span></span></td>
<td><span data-ttu-id="a760e-170">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="a760e-170">See notes.</span></span></td>
<td><span data-ttu-id="a760e-171">Se o controle de lista tiver um ponto clicável (um ponto que pode ser clicado para fazer com que a lista tenha foco), esse ponto deve ser exposto por essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="a760e-171">If the list control has a clickable point (a point that can be clicked to cause the list to take focus), that point must be exposed through this property.</span></span> <span data-ttu-id="a760e-172">Se o valor da propriedade <a href="uiauto-automation-element-propids.md"><strong>UIA_IsOffscreenPropertyId</strong></a> for <strong>true</strong>, a tentativa de recuperar essa propriedade resultará na <a href="uiauto-error-codes.md"><strong>UIA_E_NOCLICKABLEPOINT</strong></a> erro.</span><span class="sxs-lookup"><span data-stu-id="a760e-172">If the value of the <a href="uiauto-automation-element-propids.md"><strong>UIA_IsOffscreenPropertyId</strong></a> property is <strong>TRUE</strong>, attempting to retrieve this property results in the <a href="uiauto-error-codes.md"><strong>UIA_E_NOCLICKABLEPOINT</strong></a> error.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a760e-173"><a href="uiauto-automation-element-propids.md"><strong>UIA_ControlTypePropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="a760e-173"><a href="uiauto-automation-element-propids.md"><strong>UIA_ControlTypePropertyId</strong></a></span></span></td>
<td><span data-ttu-id="a760e-174"><strong>SemanticZoom</strong></span><span class="sxs-lookup"><span data-stu-id="a760e-174"><strong>SemanticZoom</strong></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="a760e-175"><a href="uiauto-automation-element-propids.md"><strong>UIA_IsContentElementPropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="a760e-175"><a href="uiauto-automation-element-propids.md"><strong>UIA_IsContentElementPropertyId</strong></a></span></span></td>
<td><span data-ttu-id="a760e-176">TRUE</span><span class="sxs-lookup"><span data-stu-id="a760e-176">TRUE</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="a760e-177"><a href="uiauto-automation-element-propids.md"><strong>UIA_IsControlElementPropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="a760e-177"><a href="uiauto-automation-element-propids.md"><strong>UIA_IsControlElementPropertyId</strong></a></span></span></td>
<td><span data-ttu-id="a760e-178">TRUE</span><span class="sxs-lookup"><span data-stu-id="a760e-178">TRUE</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="a760e-179"><a href="uiauto-automation-element-propids.md"><strong>UIA_IsKeyboardFocusablePropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="a760e-179"><a href="uiauto-automation-element-propids.md"><strong>UIA_IsKeyboardFocusablePropertyId</strong></a></span></span></td>
<td><span data-ttu-id="a760e-180">FALSE</span><span class="sxs-lookup"><span data-stu-id="a760e-180">FALSE</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="a760e-181"><a href="uiauto-automation-element-propids.md"><strong>UIA_LabeledByPropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="a760e-181"><a href="uiauto-automation-element-propids.md"><strong>UIA_LabeledByPropertyId</strong></a></span></span></td>
<td><span data-ttu-id="a760e-182">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="a760e-182">See notes.</span></span></td>
<td><span data-ttu-id="a760e-183">Se houver um rótulo de texto estático, essa propriedade deverá expor uma referência a esse controle.</span><span class="sxs-lookup"><span data-stu-id="a760e-183">If there is a static text label, this property must expose a reference to that control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a760e-184"><a href="uiauto-automation-element-propids.md"><strong>UIA_LocalizedControlTypePropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="a760e-184"><a href="uiauto-automation-element-propids.md"><strong>UIA_LocalizedControlTypePropertyId</strong></a></span></span></td>
<td><span data-ttu-id="a760e-185">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="a760e-185">See notes.</span></span></td>
<td><span data-ttu-id="a760e-186">Uma cadeia de caracteres localizada correspondente ao tipo de controle <strong>SemanticZoom</strong> .</span><span class="sxs-lookup"><span data-stu-id="a760e-186">A localized string corresponding to the <strong>SemanticZoom</strong> control type.</span></span> <span data-ttu-id="a760e-187">O valor padrão é &quot; zoom semântico &quot; para en-US ou inglês (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="a760e-187">The default value is &quot;semantic zoom&quot; for en-US or English (United States).</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="a760e-188">Algumas estruturas concatenam isso como &quot; semanticzoom &quot; .</span><span class="sxs-lookup"><span data-stu-id="a760e-188">Some frameworks concatenated this as &quot;semanticzoom&quot;.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a760e-189"><a href="uiauto-automation-element-propids.md"><strong>UIA_NamePropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="a760e-189"><a href="uiauto-automation-element-propids.md"><strong>UIA_NamePropertyId</strong></a></span></span></td>
<td><span data-ttu-id="a760e-190">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="a760e-190">See notes.</span></span></td>
<td><span data-ttu-id="a760e-191">Uma cadeia de caracteres vazia é aceitável ou um nome mais útil pode ser fornecido, desde que não contenha o termo zoom semântico, o que tornaria a combinação de tipo de controle e nome confuso.</span><span class="sxs-lookup"><span data-stu-id="a760e-191">An empty string is acceptable, or a more useful name could be provided, as long as it does not contain the term  semantic zoom , which would make the combination of control type and name confusing.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="required-control-patterns-and-properties"></a><span data-ttu-id="a760e-192">Propriedades e padrões de controle necessários</span><span class="sxs-lookup"><span data-stu-id="a760e-192">Required Control Patterns and Properties</span></span>

<span data-ttu-id="a760e-193">A tabela a seguir lista os padrões de controle de automação da interface do usuário que devem ter suporte de todos os controles de zoom semânticos.</span><span class="sxs-lookup"><span data-stu-id="a760e-193">The following table lists the UI Automation control patterns required to be supported by all Semantic Zoom controls.</span></span> <span data-ttu-id="a760e-194">Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="a760e-194">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="a760e-195">Propriedade padrão de controle/padrão</span><span class="sxs-lookup"><span data-stu-id="a760e-195">Control Pattern/Pattern Property</span></span>                  | <span data-ttu-id="a760e-196">Suporte/valor</span><span class="sxs-lookup"><span data-stu-id="a760e-196">Support/Value</span></span> | <span data-ttu-id="a760e-197">Observações</span><span class="sxs-lookup"><span data-stu-id="a760e-197">Notes</span></span>                                                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------------|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a760e-198">**IToggleProvider**</span><span class="sxs-lookup"><span data-stu-id="a760e-198">**IToggleProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) | <span data-ttu-id="a760e-199">Depende</span><span class="sxs-lookup"><span data-stu-id="a760e-199">Depends</span></span>       | <span data-ttu-id="a760e-200">Os controles de zoom semânticos dão suporte ao padrão de controle de [alternância](uiauto-implementingtoggle.md) para permitir que o zoom seja habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="a760e-200">Semantic Zoom controls support the [Toggle](uiauto-implementingtoggle.md) control pattern to allow the zoom to be enabled or disabled.</span></span> <span data-ttu-id="a760e-201">[**\_ Alternânciastate Off**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) corresponde ao estado simples, todo, e [**ToggleState \_ em**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) corresponde à exibição de alto nível e ampliada.</span><span class="sxs-lookup"><span data-stu-id="a760e-201">[**ToggleState\_Off**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) corresponds to the flat, all-up state, and [**ToggleState\_On**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) corresponds to the high level, zoomed-out view.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="a760e-202">Eventos necessários</span><span class="sxs-lookup"><span data-stu-id="a760e-202">Required Events</span></span>

<span data-ttu-id="a760e-203">A tabela a seguir lista os eventos de automação da interface do usuário aos quais os controles de zoom semânticos precisam dar suporte.</span><span class="sxs-lookup"><span data-stu-id="a760e-203">The following table lists the UI Automation events that Semantic Zoom controls are required to support.</span></span> <span data-ttu-id="a760e-204">Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="a760e-204">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="a760e-205">Evento de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="a760e-205">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="a760e-206">Observações</span><span class="sxs-lookup"><span data-stu-id="a760e-206">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a760e-207">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="a760e-207">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="a760e-208">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="a760e-208">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="a760e-209">Se o controle oferecer suporte à propriedade [**IsEnabled**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="a760e-209">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="a760e-210">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="a760e-210">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="a760e-211">Se o controle oferecer suporte à propriedade [**IsOffscreen**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="a760e-211">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| <span data-ttu-id="a760e-212">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ToggleToggleStatePropertyId.</span><span class="sxs-lookup"><span data-stu-id="a760e-212">[**UIA\_ToggleToggleStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>    |                                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="a760e-213">Comentários</span><span class="sxs-lookup"><span data-stu-id="a760e-213">Remarks</span></span>

<span data-ttu-id="a760e-214">Se uma interface do usuário tiver um botão visível para alternar o comportamento de controle de zoom semântico, esse botão não deverá ter um tipo de controle **SemanticZoom** .</span><span class="sxs-lookup"><span data-stu-id="a760e-214">If a UI has a visible button to toggle Semantic Zoom control behavior, this button should not have a **SemanticZoom** control type.</span></span> <span data-ttu-id="a760e-215">Isso é um contador intuitivo, mas o tipo de controle **SemanticZoom** caracteriza o contêiner do conteúdo de zoom, não um botão que controla o zoom.</span><span class="sxs-lookup"><span data-stu-id="a760e-215">This is counter-intuitive, but the **SemanticZoom** control type characterizes the container of the zooming content, not a button that controls the zoom.</span></span> <span data-ttu-id="a760e-216">(Esse botão pode ser representado simplesmente como um tipo de controle de [botão](uiauto-supportbuttoncontroltype.md) com o padrão de controle de [alternância](uiauto-implementingtoggle.md) .)</span><span class="sxs-lookup"><span data-stu-id="a760e-216">(Such a button could be represented simply as a [Button](uiauto-supportbuttoncontroltype.md) control type with the [Toggle](uiauto-implementingtoggle.md) control pattern.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="a760e-217">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a760e-217">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a760e-218">Visão Geral dos Tipos de Controle de Automação de Interface do Usuário</span><span class="sxs-lookup"><span data-stu-id="a760e-218">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="a760e-219">Visão geral de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="a760e-219">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

