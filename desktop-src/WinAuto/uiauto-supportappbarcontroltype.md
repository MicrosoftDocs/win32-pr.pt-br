---
title: Tipo de controle AppBar
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle AppBar.
ms.assetid: B56F4E7A-934F-8516-9B1B-B23B80D54273
keywords:
- Automação da interface do usuário, suporte para tipo de controle AppBar
- Automação da interface do usuário, tipo de controle AppBar
- Automação da interface do usuário, padrões de controle para o tipo de controle AppBar
- padrões de controle, tipo de controle AppBar
- suporte para tipo de controle AppBar
- Tipo de controle AppBar
- tipos de controle, AppBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 151aecc0f5f97878e10b59b091c4c59ec98cb26d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454250"
---
# <a name="appbar-control-type"></a><span data-ttu-id="709f8-110">Tipo de controle AppBar</span><span class="sxs-lookup"><span data-stu-id="709f8-110">AppBar Control Type</span></span>

<span data-ttu-id="709f8-111">Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle **AppBar** .</span><span class="sxs-lookup"><span data-stu-id="709f8-111">This topic provides information about Microsoft UI Automation support for the **AppBar** control type.</span></span>

<span data-ttu-id="709f8-112">Uma barra de aplicativo é um elemento de interface do usuário que apresenta navegação, comandos e ferramentas para ele.</span><span class="sxs-lookup"><span data-stu-id="709f8-112">An app bar is a UI element that presents navigation, commands, and tools to the user.</span></span> <span data-ttu-id="709f8-113">Para aplicativos da Windows Store, as barras de aplicativos para aplicativos podem ser exibidas pressionando-se a tecla Windows + Z.</span><span class="sxs-lookup"><span data-stu-id="709f8-113">For Windows Store apps, app bars for apps can be displayed by pressing Windows Key + Z.</span></span>

<span data-ttu-id="709f8-114">As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle **AppBar** .</span><span class="sxs-lookup"><span data-stu-id="709f8-114">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **AppBar** control type.</span></span>

<span data-ttu-id="709f8-115">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="709f8-115">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="709f8-116">Estrutura de árvore típica</span><span class="sxs-lookup"><span data-stu-id="709f8-116">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="709f8-117">Propriedades relevantes</span><span class="sxs-lookup"><span data-stu-id="709f8-117">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="709f8-118">Eventos necessários</span><span class="sxs-lookup"><span data-stu-id="709f8-118">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="709f8-119">Eventos relevantes</span><span class="sxs-lookup"><span data-stu-id="709f8-119">Relevant Events</span></span>](#relevant-events)
-   [<span data-ttu-id="709f8-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="709f8-120">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="709f8-121">Estrutura de árvore típica</span><span class="sxs-lookup"><span data-stu-id="709f8-121">Typical Tree Structure</span></span>

<span data-ttu-id="709f8-122">A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence a controles **AppBar** e descreve o que pode ser contido em cada exibição.</span><span class="sxs-lookup"><span data-stu-id="709f8-122">The following table depicts a typical control and content view of the UI Automation tree that pertains to **AppBar** controls and describes what can be contained in each view.</span></span> <span data-ttu-id="709f8-123">O **botão** é o elemento mais comum dentro de um **AppBar** , mas outros controles que chamam ações para um aplicativo também são possíveis.</span><span class="sxs-lookup"><span data-stu-id="709f8-123">**Button** is the most common element within an **AppBar** but other controls that invoke actions for an app are also possible.</span></span> <span data-ttu-id="709f8-124">Um **AppBar** também pode ter 0 ou mais separadores (tipo de controle **Separator** ), que aparecem no modo de exibição de controle como colocado entre os outros controles.</span><span class="sxs-lookup"><span data-stu-id="709f8-124">An **AppBar** can also have 0 or more separators (**Separator** control type), which appear in the control view as placed between the other controls.</span></span> <span data-ttu-id="709f8-125">Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="709f8-125">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="709f8-126">Exibição de controle</span><span class="sxs-lookup"><span data-stu-id="709f8-126">Control View</span></span></th>
<th><span data-ttu-id="709f8-127">Exibição de conteúdo</span><span class="sxs-lookup"><span data-stu-id="709f8-127">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="709f8-128">AppBar</span><span class="sxs-lookup"><span data-stu-id="709f8-128">AppBar</span></span>
<ul>
<li><span data-ttu-id="709f8-129">Botão (0 ou muitos)</span><span class="sxs-lookup"><span data-stu-id="709f8-129">Button (0 or many)</span></span></li>
<li><span data-ttu-id="709f8-130">Outros controles (0 ou muitos)</span><span class="sxs-lookup"><span data-stu-id="709f8-130">Other controls (0 or many)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="709f8-131">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="709f8-131">Not applicable</span></span>
<ul>
<li><span data-ttu-id="709f8-132">Botão (0 ou muitos)</span><span class="sxs-lookup"><span data-stu-id="709f8-132">Button (0 or many)</span></span></li>
<li><span data-ttu-id="709f8-133">Outros controles (0 ou muitos)</span><span class="sxs-lookup"><span data-stu-id="709f8-133">Other controls (0 or many)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="709f8-134">Propriedades relevantes</span><span class="sxs-lookup"><span data-stu-id="709f8-134">Relevant Properties</span></span>

<span data-ttu-id="709f8-135">A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para os controles que implementam o tipo de controle **AppBar** .</span><span class="sxs-lookup"><span data-stu-id="709f8-135">The following table lists the UI Automation properties whose value or definition is especially relevant to the controls that implement the **AppBar** control type.</span></span> <span data-ttu-id="709f8-136">Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="709f8-136">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="709f8-137">Propriedade de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="709f8-137">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="709f8-138">Valor</span><span class="sxs-lookup"><span data-stu-id="709f8-138">Value</span></span>      | <span data-ttu-id="709f8-139">Observações</span><span class="sxs-lookup"><span data-stu-id="709f8-139">Notes</span></span>                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="709f8-140">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="709f8-140">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="709f8-141">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="709f8-141">See notes.</span></span> | <span data-ttu-id="709f8-142">O valor dessa propriedade deve ser exclusivo entre todos os elementos de mesmo nível na exibição bruta da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="709f8-142">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                |
| [<span data-ttu-id="709f8-143">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="709f8-143">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="709f8-144">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="709f8-144">See notes.</span></span> | <span data-ttu-id="709f8-145">O valor exposto por essa propriedade deve incluir todos os controles contidos nela.</span><span class="sxs-lookup"><span data-stu-id="709f8-145">The value exposed by this property must include all of the controls contained within it.</span></span>                                                                                                                                    |
| [<span data-ttu-id="709f8-146">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="709f8-146">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="709f8-147">**AppBar**</span><span class="sxs-lookup"><span data-stu-id="709f8-147">**AppBar**</span></span> |                                                                                                                                                                                                                             |
| [<span data-ttu-id="709f8-148">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="709f8-148">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="709f8-149">FALSE</span><span class="sxs-lookup"><span data-stu-id="709f8-149">FALSE</span></span>      | <span data-ttu-id="709f8-150">Um controle da barra de aplicativos não está incluído na exibição de conteúdo da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="709f8-150">An app bar control is not included in the content view of the UI Automation tree.</span></span>                                                                                                                                           |
| [<span data-ttu-id="709f8-151">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="709f8-151">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="709f8-152">TRUE</span><span class="sxs-lookup"><span data-stu-id="709f8-152">TRUE</span></span>       | <span data-ttu-id="709f8-153">Um controle da barra de aplicativo sempre é incluído no modo de exibição de controle da árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="709f8-153">An app bar control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                                        |
| [<span data-ttu-id="709f8-154">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="709f8-154">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="709f8-155">Consulte as observações</span><span class="sxs-lookup"><span data-stu-id="709f8-155">See notes</span></span>  | <span data-ttu-id="709f8-156">Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="709f8-156">If the control can receive keyboard focus, it must support this property.</span></span> <span data-ttu-id="709f8-157">Controles na barra de aplicativos normalmente podem assumir o foco do teclado.</span><span class="sxs-lookup"><span data-stu-id="709f8-157">Controls within the app bar typically can take keyboard focus.</span></span>                                                                                    |
| [<span data-ttu-id="709f8-158">**UIA \_ IsOffscreenPropertyId**</span><span class="sxs-lookup"><span data-stu-id="709f8-158">**UIA\_IsOffscreenPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="709f8-159">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="709f8-159">See notes.</span></span> | <span data-ttu-id="709f8-160">O valor dessa propriedade depende de se o controle é visível na tela.</span><span class="sxs-lookup"><span data-stu-id="709f8-160">The value of this property depends on whether the control is viewable on the screen.</span></span>                                                                                                                                        |
| [<span data-ttu-id="709f8-161">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="709f8-161">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="709f8-162">Nulo</span><span class="sxs-lookup"><span data-stu-id="709f8-162">Null</span></span>       | <span data-ttu-id="709f8-163">Os controles da barra de aplicativos geralmente não têm um rótulo.</span><span class="sxs-lookup"><span data-stu-id="709f8-163">App bar controls usually do not have a label.</span></span>                                                                                                                                                                               |
| [<span data-ttu-id="709f8-164">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="709f8-164">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="709f8-165">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="709f8-165">See notes.</span></span> | <span data-ttu-id="709f8-166">Cadeia de caracteres localizada correspondente ao tipo de controle **AppBar** .</span><span class="sxs-lookup"><span data-stu-id="709f8-166">Localized string corresponding to the **AppBar** control type.</span></span> <span data-ttu-id="709f8-167">O valor padrão é "barra de aplicativos" para en-US ou inglês (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="709f8-167">The default value is "app bar" for en-US or English (United States).</span></span>                                                                                         |
| [<span data-ttu-id="709f8-168">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="709f8-168">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="709f8-169">Consulte observações.</span><span class="sxs-lookup"><span data-stu-id="709f8-169">See notes.</span></span> | <span data-ttu-id="709f8-170">O controle da barra de aplicativos não precisa de um nome, a menos que um aplicativo tenha mais de uma barra de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="709f8-170">The app bar control does not need a name unless an application has more than one app bar.</span></span> <span data-ttu-id="709f8-171">Se houver mais de uma barra de aplicativos em um aplicativo, use essa propriedade para expor nomes de distinção, como "Top" ou "Bottom".</span><span class="sxs-lookup"><span data-stu-id="709f8-171">If there is more than one app bar in an application, use this property to expose distinguishing names, such as "Top" or "Bottom."</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="709f8-172">Eventos necessários</span><span class="sxs-lookup"><span data-stu-id="709f8-172">Required Events</span></span>

<span data-ttu-id="709f8-173">A tabela a seguir lista os eventos de automação da interface do usuário aos quais os controles da barra de aplicativos precisam dar suporte.</span><span class="sxs-lookup"><span data-stu-id="709f8-173">The following table lists the UI Automation events that app bar controls are required to support.</span></span> <span data-ttu-id="709f8-174">Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="709f8-174">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="709f8-175">Evento de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="709f8-175">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="709f8-176">Observações</span><span class="sxs-lookup"><span data-stu-id="709f8-176">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="709f8-177">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="709f8-177">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="709f8-178">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="709f8-178">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="709f8-179">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="709f8-179">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="709f8-180">Se o controle oferecer suporte à propriedade [**IsEnabled**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="709f8-180">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="709f8-181">[**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="709f8-181">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="709f8-182">Se o controle oferecer suporte à propriedade [**IsOffscreen**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="709f8-182">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="709f8-183">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="709f8-183">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="relevant-events"></a><span data-ttu-id="709f8-184">Eventos relevantes</span><span class="sxs-lookup"><span data-stu-id="709f8-184">Relevant Events</span></span>

<span data-ttu-id="709f8-185">A tabela a seguir lista os eventos de automação da interface do usuário que são especialmente relevantes para os controles que implementam o tipo de controle **AppBar** , mas não são estritamente necessários.</span><span class="sxs-lookup"><span data-stu-id="709f8-185">The following table lists the UI Automation events that are especially relevant to the controls that implement the **AppBar** control type but not strictly required.</span></span>



| <span data-ttu-id="709f8-186">Evento de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="709f8-186">UI Automation Event</span></span>                                                                                 | <span data-ttu-id="709f8-187">Observações</span><span class="sxs-lookup"><span data-stu-id="709f8-187">Notes</span></span>                                                                              |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="709f8-188">**UIA \_ MenuClosedEventId**</span><span class="sxs-lookup"><span data-stu-id="709f8-188">**UIA\_MenuClosedEventId**</span></span>](uiauto-event-ids.md)                            | <span data-ttu-id="709f8-189">Implementações de plataforma podem acionar esse evento quando o controle da barra de aplicativo é fechado.</span><span class="sxs-lookup"><span data-stu-id="709f8-189">Platform implementations might fire this event when the app bar control is closed.</span></span> |
| [<span data-ttu-id="709f8-190">**UIA \_ MenuOpenedEventId**</span><span class="sxs-lookup"><span data-stu-id="709f8-190">**UIA\_MenuOpenedEventId**</span></span>](uiauto-event-ids.md)                            | <span data-ttu-id="709f8-191">Implementações de plataforma podem acionar esse evento quando o controle da barra de aplicativo é aberto.</span><span class="sxs-lookup"><span data-stu-id="709f8-191">Platform implementations might fire this event when the app bar control is opened.</span></span> |
| [<span data-ttu-id="709f8-192">**IUIAutomationPropertyChangedEventHandler**</span><span class="sxs-lookup"><span data-stu-id="709f8-192">**IUIAutomationPropertyChangedEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler) | <span data-ttu-id="709f8-193">Manipulador de eventos de alteração de propriedade.</span><span class="sxs-lookup"><span data-stu-id="709f8-193">Property-changed event handler.</span></span>                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="709f8-194">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="709f8-194">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="709f8-195">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="709f8-195">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="709f8-196">Visão Geral dos Tipos de Controle de Automação de Interface do Usuário</span><span class="sxs-lookup"><span data-stu-id="709f8-196">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="709f8-197">Visão geral de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="709f8-197">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> <dt>

<span data-ttu-id="709f8-198">**Referência**</span><span class="sxs-lookup"><span data-stu-id="709f8-198">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="709f8-199">**Controle XAML AppBar**</span><span class="sxs-lookup"><span data-stu-id="709f8-199">**AppBar XAML control**</span></span>](/uwp/api/Windows.UI.Xaml.Controls.AppBar)
</dt> <dt>

<span data-ttu-id="709f8-200">[**Objeto WinJS. UI. AppBar**](/previous-versions/windows/apps/br229670(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="709f8-200">[**WinJS.UI.AppBar object**](/previous-versions/windows/apps/br229670(v=win.10))</span></span>
</dt> </dl>

 

 