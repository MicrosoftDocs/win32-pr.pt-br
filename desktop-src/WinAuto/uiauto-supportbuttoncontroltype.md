---
title: Tipo de controle de botão
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle de botão.
ms.assetid: a2942067-461c-4281-80cf-385e3c08c874
keywords:
- Automação da interface do usuário, suporte para tipo de controle de botão
- Automação da interface do usuário, tipo de controle de botão
- Automação da interface do usuário, estrutura de árvore para tipo de controle de botão
- Automação da interface do usuário, propriedades para tipo de controle de botão
- Automação da interface do usuário, padrões de controle para tipo de controle de botão
- Automação da interface do usuário, eventos para tipo de controle de botão
- estruturas de árvore, tipo de controle de botão
- Propriedades, tipo de controle de botão
- padrões de controle, tipo de controle de botão
- eventos, tipo de controle de botão
- suporte para tipo de controle de botão
- Tipo Controle de botão
- tipos de controle, estrutura de árvore para tipo de controle de botão
- tipos de controle, padrões de controle para tipo de controle de botão
- tipos de controle, suporte para botão
- tipos de controle, botão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: def18e7094e297303a70fc0980bfdd0cb4413c0c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160494"
---
# <a name="button-control-type"></a><span data-ttu-id="31912-119">Tipo de controle de botão</span><span class="sxs-lookup"><span data-stu-id="31912-119">Button Control Type</span></span>

<span data-ttu-id="31912-120">Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle de **botão** .</span><span class="sxs-lookup"><span data-stu-id="31912-120">This topic provides information about Microsoft UI Automation support for the **Button** control type.</span></span>

<span data-ttu-id="31912-121">Um botão é um objeto com o qual um usuário interage para executar uma ação como os botões OK e cancelar em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="31912-121">A button is an object that a user interacts with to perform an action such as the OK and Cancel buttons on a dialog box.</span></span> <span data-ttu-id="31912-122">O controle de botão é um controle simples para expor porque ele é mapeado para um único comando que o usuário deseja concluir.</span><span class="sxs-lookup"><span data-stu-id="31912-122">The button control is a simple control to expose because it maps to a single command that the user wishes to complete.</span></span>

<span data-ttu-id="31912-123">As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle de **botão** .</span><span class="sxs-lookup"><span data-stu-id="31912-123">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Button** control type.</span></span> <span data-ttu-id="31912-124">Os requisitos de automação da interface do usuário se aplicam a todos os controles de botão onde a estrutura/plataforma da interface do usuário integra o suporte à automação da interface do usuário para tipos de controle</span><span class="sxs-lookup"><span data-stu-id="31912-124">The UI Automation requirements apply to all button controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="31912-125">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="31912-125">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="31912-126">Estrutura de árvore típica</span><span class="sxs-lookup"><span data-stu-id="31912-126">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="31912-127">Propriedades relevantes</span><span class="sxs-lookup"><span data-stu-id="31912-127">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="31912-128">Padrões de controle necessários</span><span class="sxs-lookup"><span data-stu-id="31912-128">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="31912-129">Eventos necessários</span><span class="sxs-lookup"><span data-stu-id="31912-129">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="31912-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="31912-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="31912-131">Estrutura de árvore típica</span><span class="sxs-lookup"><span data-stu-id="31912-131">Typical Tree Structure</span></span>

<span data-ttu-id="31912-132">A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence a controles de botão e descreve o que pode ser contido em cada exibição.</span><span class="sxs-lookup"><span data-stu-id="31912-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to button controls and describes what can be contained in each view.</span></span> <span data-ttu-id="31912-133">Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="31912-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="31912-134">Exibição de controle</span><span class="sxs-lookup"><span data-stu-id="31912-134">Control View</span></span></th>
<th><span data-ttu-id="31912-135">Exibição de conteúdo</span><span class="sxs-lookup"><span data-stu-id="31912-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="31912-136">Botão</span><span class="sxs-lookup"><span data-stu-id="31912-136">Button</span></span>
<ul>
<li><span data-ttu-id="31912-137">Imagem (0 ou mais)</span><span class="sxs-lookup"><span data-stu-id="31912-137">Image (0 or more)</span></span></li>
<li><span data-ttu-id="31912-138">Texto (0 ou mais)</span><span class="sxs-lookup"><span data-stu-id="31912-138">Text (0 or more)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="31912-139">Botão</span><span class="sxs-lookup"><span data-stu-id="31912-139">Button</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="31912-140">Propriedades relevantes</span><span class="sxs-lookup"><span data-stu-id="31912-140">Relevant Properties</span></span>

<span data-ttu-id="31912-141">A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para os controles que implementam o tipo de controle de **botão** (como controles de botão).</span><span class="sxs-lookup"><span data-stu-id="31912-141">The following table lists the UI Automation properties whose value or definition is especially relevant to the controls that implement the **Button** control type (such as button controls).</span></span> <span data-ttu-id="31912-142">Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="31912-142">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="31912-143">Propriedade de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="31912-143">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="31912-144">Valor</span><span class="sxs-lookup"><span data-stu-id="31912-144">Value</span></span>      | <span data-ttu-id="31912-145">Observações</span><span class="sxs-lookup"><span data-stu-id="31912-145">Notes</span></span>                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="31912-146">**UIA \_ AcceleratorKeyPropertyId**</span><span class="sxs-lookup"><span data-stu-id="31912-146">**UIA\_AcceleratorKeyPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="31912-147">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="31912-147">See notes.</span></span> | <span data-ttu-id="31912-148">Um controle de botão geralmente dá suporte a uma tecla aceleradora para permitir que o usuário final execute rapidamente a ação representada pelo botão do teclado.</span><span class="sxs-lookup"><span data-stu-id="31912-148">A button control typically supports an accelerator key to enable the end user to quickly perform the action represented by the button from the keyboard.</span></span>                                             |
| [<span data-ttu-id="31912-149">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="31912-149">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="31912-150">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="31912-150">See notes.</span></span> | <span data-ttu-id="31912-151">O valor dessa propriedade deve ser exclusivo entre todos os elementos de mesmo nível na exibição bruta da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="31912-151">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                         |
| [<span data-ttu-id="31912-152">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="31912-152">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="31912-153">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="31912-153">See notes.</span></span> | <span data-ttu-id="31912-154">O retângulo mais externo que contém o controle inteiro.</span><span class="sxs-lookup"><span data-stu-id="31912-154">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                             |
| [<span data-ttu-id="31912-155">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="31912-155">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="31912-156">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="31912-156">See notes.</span></span> | <span data-ttu-id="31912-157">Com suporte se houver um retângulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="31912-157">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="31912-158">Se nem todos os pontos dentro do retângulo delimitador forem clicáveis, o elemento executará testes de clique especializados, substituirá e fornecerá um ponto clicável.</span><span class="sxs-lookup"><span data-stu-id="31912-158">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span> |
| [<span data-ttu-id="31912-159">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="31912-159">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="31912-160">**Botão**</span><span class="sxs-lookup"><span data-stu-id="31912-160">**Button**</span></span> |                                                                                                                                                                                                      |
| [<span data-ttu-id="31912-161">**UIA \_ HelpTextPropertyId**</span><span class="sxs-lookup"><span data-stu-id="31912-161">**UIA\_HelpTextPropertyId**</span></span>](uiauto-automation-element-propids.md)                         | <span data-ttu-id="31912-162">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="31912-162">See notes.</span></span> | <span data-ttu-id="31912-163">O texto de ajuda deve indicar qual será o resultado final da ativação do botão.</span><span class="sxs-lookup"><span data-stu-id="31912-163">The help text should indicate what the end result of activating the button will be.</span></span> <span data-ttu-id="31912-164">Normalmente, esse é o mesmo tipo de informações apresentadas por meio de uma dica de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="31912-164">This is typically the same type of information presented through a tooltip.</span></span>                                      |
| [<span data-ttu-id="31912-165">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="31912-165">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="31912-166">TRUE</span><span class="sxs-lookup"><span data-stu-id="31912-166">TRUE</span></span>       | <span data-ttu-id="31912-167">O controle de botão sempre deve ser conteúdo.</span><span class="sxs-lookup"><span data-stu-id="31912-167">The button control must always be content.</span></span>                                                                                                                                                           |
| [<span data-ttu-id="31912-168">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="31912-168">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="31912-169">TRUE</span><span class="sxs-lookup"><span data-stu-id="31912-169">TRUE</span></span>       | <span data-ttu-id="31912-170">O controle de botão sempre deve ser um controle.</span><span class="sxs-lookup"><span data-stu-id="31912-170">The button control must always be a control.</span></span>                                                                                                                                                         |
| [<span data-ttu-id="31912-171">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="31912-171">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="31912-172">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="31912-172">See notes.</span></span> | <span data-ttu-id="31912-173">Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="31912-173">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                            |
| [<span data-ttu-id="31912-174">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="31912-174">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="31912-175">Nulo</span><span class="sxs-lookup"><span data-stu-id="31912-175">Null</span></span>       | <span data-ttu-id="31912-176">Os controles de botão são rotulados automaticamente por seu conteúdo.</span><span class="sxs-lookup"><span data-stu-id="31912-176">Button controls are self-labeled by their contents.</span></span>                                                                                                                                                  |
| [<span data-ttu-id="31912-177">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="31912-177">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="31912-178">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="31912-178">See notes.</span></span> | <span data-ttu-id="31912-179">Cadeia de caracteres localizada correspondente ao tipo de controle de **botão** .</span><span class="sxs-lookup"><span data-stu-id="31912-179">Localized string corresponding to the **Button** control type.</span></span> <span data-ttu-id="31912-180">O valor padrão é "Button" para en-US ou inglês (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="31912-180">The default value is "button" for en-US or English (United States).</span></span>                                                                   |
| [<span data-ttu-id="31912-181">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="31912-181">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="31912-182">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="31912-182">See notes.</span></span> | <span data-ttu-id="31912-183">O nome do controle de botão é o texto usado para rotulá-lo.</span><span class="sxs-lookup"><span data-stu-id="31912-183">The name of the button control is the text used to label it.</span></span> <span data-ttu-id="31912-184">Sempre que uma imagem é usada para rotular um botão, o texto alternativo deve ser fornecido para a propriedade **Name** do botão.</span><span class="sxs-lookup"><span data-stu-id="31912-184">Whenever an image is used to label a button, alternate text must be supplied for the button's **Name** property.</span></span>                        |



 

## <a name="required-control-patterns"></a><span data-ttu-id="31912-185">Padrões de controle necessários</span><span class="sxs-lookup"><span data-stu-id="31912-185">Required Control Patterns</span></span>

<span data-ttu-id="31912-186">A tabela a seguir lista os padrões de controle de automação da interface do usuário necessários para ter suporte de todos os controles de botão.</span><span class="sxs-lookup"><span data-stu-id="31912-186">The following table lists the UI Automation control patterns required to be supported by all button controls.</span></span> <span data-ttu-id="31912-187">Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="31912-187">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="31912-188">Propriedade padrão de controle/padrão</span><span class="sxs-lookup"><span data-stu-id="31912-188">Control Pattern/Pattern Property</span></span>                                  | <span data-ttu-id="31912-189">Suporte/valor</span><span class="sxs-lookup"><span data-stu-id="31912-189">Support/Value</span></span> | <span data-ttu-id="31912-190">Observações</span><span class="sxs-lookup"><span data-stu-id="31912-190">Notes</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="31912-191">**IExpandCollapseProvider**</span><span class="sxs-lookup"><span data-stu-id="31912-191">**IExpandCollapseProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | <span data-ttu-id="31912-192">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="31912-192">See notes.</span></span>    | <span data-ttu-id="31912-193">Quando um botão é hospedado como um filho de um botão de divisão, o botão filho pode dar suporte ao padrão de controle [ExpandCollapse](uiauto-implementingexpandcollapse.md) em vez do padrão de controle [Invoke](uiauto-implementinginvoke.md) ou [Toggle](uiauto-implementingtoggle.md) .</span><span class="sxs-lookup"><span data-stu-id="31912-193">When a button is hosted as a child of a split button, the child button can support the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern instead of the [Invoke](uiauto-implementinginvoke.md) or [Toggle](uiauto-implementingtoggle.md) control pattern.</span></span> <span data-ttu-id="31912-194">O padrão de controle ExpandCollapse pode ser usado para abrir ou fechar um menu ou outra subestrutura associada ao elemento Button.</span><span class="sxs-lookup"><span data-stu-id="31912-194">The ExpandCollapse control pattern can be used for opening or closing a menu or other sub-structure associated with the button element.</span></span> |
| [<span data-ttu-id="31912-195">**IInvokeProvider**</span><span class="sxs-lookup"><span data-stu-id="31912-195">**IInvokeProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                 | <span data-ttu-id="31912-196">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="31912-196">See notes.</span></span>    | <span data-ttu-id="31912-197">Todos os botões devem dar suporte ao padrão de controle [Invoke](uiauto-implementinginvoke.md) ou ao padrão de controle [Toggle](uiauto-implementingtoggle.md) , mas não a ambos.</span><span class="sxs-lookup"><span data-stu-id="31912-197">All buttons should support the [Invoke](uiauto-implementinginvoke.md) control pattern or the [Toggle](uiauto-implementingtoggle.md) control pattern but not both.</span></span> <span data-ttu-id="31912-198">O padrão de controle Invoke deve ser suportado quando o botão executa um comando na solicitação do usuário.</span><span class="sxs-lookup"><span data-stu-id="31912-198">The Invoke control pattern must be supported when the button performs a command at the request of the user.</span></span> <span data-ttu-id="31912-199">Esse comando é mapeado para uma única operação, como recortar, copiar, colar ou excluir.</span><span class="sxs-lookup"><span data-stu-id="31912-199">This command maps to a single operation such as Cut, Copy, Paste, or Delete.</span></span>                                                              |
| [<span data-ttu-id="31912-200">**IToggleProvider**</span><span class="sxs-lookup"><span data-stu-id="31912-200">**IToggleProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                 | <span data-ttu-id="31912-201">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="31912-201">See notes.</span></span>    | <span data-ttu-id="31912-202">Todos os botões devem dar suporte ao padrão de controle [Invoke](uiauto-implementinginvoke.md) ou ao padrão de controle [Toggle](uiauto-implementingtoggle.md) , mas não a ambos.</span><span class="sxs-lookup"><span data-stu-id="31912-202">All buttons should support the [Invoke](uiauto-implementinginvoke.md) control pattern or the [Toggle](uiauto-implementingtoggle.md) control pattern but not both.</span></span> <span data-ttu-id="31912-203">O padrão de controle Toggle deve ter suporte se o botão puder percorrer uma série de até três Estados.</span><span class="sxs-lookup"><span data-stu-id="31912-203">The Toggle control pattern must be supported if the button can cycle through a series of up to three states.</span></span> <span data-ttu-id="31912-204">Normalmente, isso é visto como uma opção liga/desliga para recursos específicos.</span><span class="sxs-lookup"><span data-stu-id="31912-204">Typically this is seen as an on/off switch for specific features.</span></span>                                                                        |



 

## <a name="required-events"></a><span data-ttu-id="31912-205">Eventos necessários</span><span class="sxs-lookup"><span data-stu-id="31912-205">Required Events</span></span>

<span data-ttu-id="31912-206">A tabela a seguir lista os eventos de automação da interface do usuário aos quais os controles de botão são necessários para dar suporte.</span><span class="sxs-lookup"><span data-stu-id="31912-206">The following table lists the UI Automation events that button controls are required to support.</span></span> <span data-ttu-id="31912-207">Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="31912-207">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="31912-208">Evento de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="31912-208">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="31912-209">Observações</span><span class="sxs-lookup"><span data-stu-id="31912-209">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="31912-210">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="31912-210">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="31912-211">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="31912-211">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| [<span data-ttu-id="31912-212">**UIA \_ invocar \_ InvokedEventId**</span><span class="sxs-lookup"><span data-stu-id="31912-212">**UIA\_Invoke\_InvokedEventId**</span></span>](uiauto-event-ids.md)                                                     | <span data-ttu-id="31912-213">Se o controle der suporte ao padrão de controle [Invoke](uiauto-implementinginvoke.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="31912-213">If the control supports the [Invoke](uiauto-implementinginvoke.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="31912-214">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="31912-214">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="31912-215">Se o controle oferecer suporte à propriedade [**IsEnabled**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="31912-215">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="31912-216">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="31912-216">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="31912-217">Se o controle oferecer suporte à propriedade [**IsOffscreen**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="31912-217">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| <span data-ttu-id="31912-218">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade NamePropertyId.</span><span class="sxs-lookup"><span data-stu-id="31912-218">[**UIA\_NamePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                           |                                                                                                                            |
| [<span data-ttu-id="31912-219">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="31912-219">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |
| <span data-ttu-id="31912-220">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ToggleToggleStatePropertyId.</span><span class="sxs-lookup"><span data-stu-id="31912-220">[**UIA\_ToggleToggleStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>    | <span data-ttu-id="31912-221">Se o controle der suporte ao padrão de controle [Toggle](uiauto-implementingtoggle.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="31912-221">If the control supports the [Toggle](uiauto-implementingtoggle.md) control pattern, it must support this event.</span></span>           |



 

## <a name="related-topics"></a><span data-ttu-id="31912-222">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="31912-222">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="31912-223">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="31912-223">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="31912-224">Visão Geral dos Tipos de Controle de Automação de Interface do Usuário</span><span class="sxs-lookup"><span data-stu-id="31912-224">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="31912-225">Visão geral de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="31912-225">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




