---
title: Funções de padrão de controle preteridas
description: Funções de padrão de controle preteridas
ms.assetid: 06434b07-7592-4909-8c4e-064382bdbf98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f646f9a9e3139d487785e344b9d3fc242b1a40e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363743"
---
# <a name="deprecated-control-pattern-functions"></a><span data-ttu-id="fe28b-103">Funções de padrão de controle preteridas</span><span class="sxs-lookup"><span data-stu-id="fe28b-103">Deprecated Control Pattern Functions</span></span>

> [!Note]  
> <span data-ttu-id="fe28b-104">As funções de padrão de controle descritas nesta seção são preteridas.</span><span class="sxs-lookup"><span data-stu-id="fe28b-104">The control pattern functions described in this section are deprecated.</span></span> <span data-ttu-id="fe28b-105">Os aplicativos cliente devem usar as interfaces de Component Object Model (COM) descritas nas seções a seguir:</span><span class="sxs-lookup"><span data-stu-id="fe28b-105">Client applications should use the Component Object Model (COM) interfaces described in the following sections:</span></span>
>
> -   [<span data-ttu-id="fe28b-106">Interfaces de elementos de automação da interface do usuário para clientes</span><span class="sxs-lookup"><span data-stu-id="fe28b-106">UI Automation Element Interfaces for Clients</span></span>](uiauto-entry-uiautoclientinterfaces.md)
> -   [<span data-ttu-id="fe28b-107">Interface de condição de propriedade para clientes</span><span class="sxs-lookup"><span data-stu-id="fe28b-107">Property Condition Interface for Clients</span></span>](uiauto-client-propconditioninterfaces.md)
> -   [<span data-ttu-id="fe28b-108">Interfaces de padrão de controle para clientes</span><span class="sxs-lookup"><span data-stu-id="fe28b-108">Control Pattern Interfaces for Clients</span></span>](uiauto-client-controlpatterninterfaces.md)
> -   [<span data-ttu-id="fe28b-109">Interfaces de manipulação de eventos para clientes</span><span class="sxs-lookup"><span data-stu-id="fe28b-109">Event Handling Interfaces for Clients</span></span>](uiauto-client-eventhandlinginterfaces.md)
> -   [<span data-ttu-id="fe28b-110">Interfaces de fábrica de proxy para clientes</span><span class="sxs-lookup"><span data-stu-id="fe28b-110">Proxy Factory Interfaces for Clients</span></span>](uiauto-client-proxyfactoryinterfaces.md)

 

## <a name="in-this-section"></a><span data-ttu-id="fe28b-111">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="fe28b-111">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fe28b-112">Função</span><span class="sxs-lookup"><span data-stu-id="fe28b-112">Function</span></span></th>
<th><span data-ttu-id="fe28b-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="fe28b-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fe28b-114"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-dockpattern_setdockposition"><strong>DockPattern_SetDockPosition</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe28b-114"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-dockpattern_setdockposition"><strong>DockPattern_SetDockPosition</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fe28b-115">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="fe28b-115">This function is deprecated.</span></span> <span data-ttu-id="fe28b-116">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="fe28b-116">Client applications should use the Microsoft UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fe28b-117">Encaixa o elemento de automação da interface do usuário no <em>DockPosition</em> solicitado dentro de um contêiner de encaixe.</span><span class="sxs-lookup"><span data-stu-id="fe28b-117">Docks the UI Automation element at the requested <em>dockPosition</em> within a docking container.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe28b-118"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-expandcollapsepattern_collapse"><strong>ExpandCollapsePattern_Collapse</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe28b-118"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-expandcollapsepattern_collapse"><strong>ExpandCollapsePattern_Collapse</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fe28b-119">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="fe28b-119">This function is deprecated.</span></span> <span data-ttu-id="fe28b-120">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe28b-120">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fe28b-121">Oculta todos os nós descendentes, controles ou conteúdo do elemento de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe28b-121">Hides all descendant nodes, controls, or content of the UI Automation element.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe28b-122"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-expandcollapsepattern_expand"><strong>ExpandCollapsePattern_Expand</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe28b-122"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-expandcollapsepattern_expand"><strong>ExpandCollapsePattern_Expand</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fe28b-123">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="fe28b-123">This function is deprecated.</span></span> <span data-ttu-id="fe28b-124">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe28b-124">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fe28b-125">Expande um controle na tela para que ele mostre mais informações.</span><span class="sxs-lookup"><span data-stu-id="fe28b-125">Expands a control on the screen so that it shows more information.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe28b-126"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-gridpattern_getitem"><strong>GridPattern_GetItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe28b-126"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-gridpattern_getitem"><strong>GridPattern_GetItem</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fe28b-127">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="fe28b-127">This function is deprecated.</span></span> <span data-ttu-id="fe28b-128">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe28b-128">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fe28b-129">Obtém o nó de um item em uma grade.</span><span class="sxs-lookup"><span data-stu-id="fe28b-129">Gets the node for an item in a grid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe28b-130"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-invokepattern_invoke"><strong>InvokePattern_Invoke</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe28b-130"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-invokepattern_invoke"><strong>InvokePattern_Invoke</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fe28b-131">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="fe28b-131">This function is deprecated.</span></span> <span data-ttu-id="fe28b-132">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe28b-132">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fe28b-133">Envia uma solicitação para ativar um controle e iniciar sua ação única não ambígua.</span><span class="sxs-lookup"><span data-stu-id="fe28b-133">Sends a request to activate a control and initiate its single, unambiguous action.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe28b-134"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-itemcontainerpattern_finditembyproperty"><strong>ItemContainerPattern_FindItemByProperty</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe28b-134"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-itemcontainerpattern_finditembyproperty"><strong>ItemContainerPattern_FindItemByProperty</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fe28b-135">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="fe28b-135">This function is deprecated.</span></span> <span data-ttu-id="fe28b-136">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe28b-136">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fe28b-137">Recupera um nó dentro de um nó que contém, com base em um valor de propriedade especificado.</span><span class="sxs-lookup"><span data-stu-id="fe28b-137">Retrieves a node within a containing node, based on a specified property value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe28b-138"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-legacyiaccessiblepattern_dodefaultaction"><strong>LegacyIAccessiblePattern_DoDefaultAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe28b-138"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-legacyiaccessiblepattern_dodefaultaction"><strong>LegacyIAccessiblePattern_DoDefaultAction</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fe28b-139">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="fe28b-139">This function is deprecated.</span></span> <span data-ttu-id="fe28b-140">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe28b-140">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fe28b-141">Executa a ação padrão do Microsoft Acessibilidade Ativa para o elemento.</span><span class="sxs-lookup"><span data-stu-id="fe28b-141">Performs the Microsoft Active Accessibility default action for the element.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe28b-142"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-legacyiaccessiblepattern_getiaccessible"><strong>LegacyIAccessiblePattern_GetIAccessible</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe28b-142"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-legacyiaccessiblepattern_getiaccessible"><strong>LegacyIAccessiblePattern_GetIAccessible</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fe28b-143">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="fe28b-143">This function is deprecated.</span></span> <span data-ttu-id="fe28b-144">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe28b-144">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fe28b-145">Recupera um objeto <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible"><strong>IAccessible</strong></a> que corresponde ao elemento de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe28b-145">Retrieves an <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible"><strong>IAccessible</strong></a> object that corresponds to the UI Automation element.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe28b-146"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-legacyiaccessiblepattern_select"><strong>LegacyIAccessiblePattern_Select</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe28b-146"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-legacyiaccessiblepattern_select"><strong>LegacyIAccessiblePattern_Select</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fe28b-147">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="fe28b-147">This function is deprecated.</span></span> <span data-ttu-id="fe28b-148">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe28b-148">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fe28b-149">Executa uma seleção de Acessibilidade Ativa da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="fe28b-149">Performs a Microsoft Active Accessibility selection.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe28b-150"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-legacyiaccessiblepattern_setvalue"><strong>LegacyIAccessiblePattern_SetValue</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe28b-150"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-legacyiaccessiblepattern_setvalue"><strong>LegacyIAccessiblePattern_SetValue</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fe28b-151">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="fe28b-151">This function is deprecated.</span></span> <span data-ttu-id="fe28b-152">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe28b-152">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fe28b-153">Define a propriedade de valor do Microsoft Acessibilidade Ativa para o nó.</span><span class="sxs-lookup"><span data-stu-id="fe28b-153">Sets the Microsoft Active Accessibility value property for the node.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe28b-154"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-multipleviewpattern_getviewname"><strong>MultipleViewPattern_GetViewName</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe28b-154"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-multipleviewpattern_getviewname"><strong>MultipleViewPattern_GetViewName</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fe28b-155">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="fe28b-155">This function is deprecated.</span></span> <span data-ttu-id="fe28b-156">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe28b-156">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fe28b-157">Recupera o nome de um modo de exibição específico do controle.</span><span class="sxs-lookup"><span data-stu-id="fe28b-157">Retrieves the name of a control-specific view.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe28b-158"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-multipleviewpattern_setcurrentview"><strong>MultipleViewPattern_SetCurrentView</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe28b-158"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-multipleviewpattern_setcurrentview"><strong>MultipleViewPattern_SetCurrentView</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fe28b-159">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="fe28b-159">This function is deprecated.</span></span> <span data-ttu-id="fe28b-160">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe28b-160">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fe28b-161">Define um controle para um layout diferente.</span><span class="sxs-lookup"><span data-stu-id="fe28b-161">Sets a control to a different layout.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe28b-162"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-rangevaluepattern_setvalue"><strong>RangeValuePattern_SetValue</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe28b-162"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-rangevaluepattern_setvalue"><strong>RangeValuePattern_SetValue</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fe28b-163">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="fe28b-163">This function is deprecated.</span></span> <span data-ttu-id="fe28b-164">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe28b-164">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fe28b-165">Define o valor de um controle que tem um intervalo numérico.</span><span class="sxs-lookup"><span data-stu-id="fe28b-165">Sets the value of a control that has a numerical range.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe28b-166"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-scrollitempattern_scrollintoview"><strong>ScrollItemPattern_ScrollIntoView</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe28b-166"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-scrollitempattern_scrollintoview"><strong>ScrollItemPattern_ScrollIntoView</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fe28b-167">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="fe28b-167">This function is deprecated.</span></span> <span data-ttu-id="fe28b-168">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe28b-168">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fe28b-169">Rola a área de conteúdo de um objeto de contêiner para exibir o elemento de automação da interface do usuário na região visível (visor) do contêiner.</span><span class="sxs-lookup"><span data-stu-id="fe28b-169">Scrolls the content area of a container object in order to display the UI Automation element within the visible region (viewport) of the container.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe28b-170"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-scrollpattern_scroll"><strong>ScrollPattern_Scroll</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe28b-170"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-scrollpattern_scroll"><strong>ScrollPattern_Scroll</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fe28b-171">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="fe28b-171">This function is deprecated.</span></span> <span data-ttu-id="fe28b-172">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe28b-172">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fe28b-173">Rola a região visível no momento da área de conteúdo especificada como <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-scrollamount"><strong>ScrollAmount</strong></a>, horizontalmente, verticalmente ou ambas.</span><span class="sxs-lookup"><span data-stu-id="fe28b-173">Scrolls the currently visible region of the content area the specified <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-scrollamount"><strong>ScrollAmount</strong></a>, horizontally, vertically, or both.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe28b-174"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-scrollpattern_setscrollpercent"><strong>ScrollPattern_SetScrollPercent</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe28b-174"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-scrollpattern_setscrollpercent"><strong>ScrollPattern_SetScrollPercent</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fe28b-175">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="fe28b-175">This function is deprecated.</span></span> <span data-ttu-id="fe28b-176">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe28b-176">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fe28b-177">Rola um contêiner para uma posição específica horizontalmente, verticalmente ou para ambos.</span><span class="sxs-lookup"><span data-stu-id="fe28b-177">Scrolls a container to a specific position horizontally, vertically, or both.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe28b-178"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-selectionitempattern_addtoselection"><strong>SelectionItemPattern_AddToSelection</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe28b-178"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-selectionitempattern_addtoselection"><strong>SelectionItemPattern_AddToSelection</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fe28b-179">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="fe28b-179">This function is deprecated.</span></span> <span data-ttu-id="fe28b-180">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe28b-180">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fe28b-181">Adiciona um elemento não selecionado a uma seleção em um controle.</span><span class="sxs-lookup"><span data-stu-id="fe28b-181">Adds an unselected element to a selection in a control.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe28b-182"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-selectionitempattern_removefromselection"><strong>SelectionItemPattern_RemoveFromSelection</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe28b-182"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-selectionitempattern_removefromselection"><strong>SelectionItemPattern_RemoveFromSelection</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fe28b-183">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="fe28b-183">This function is deprecated.</span></span> <span data-ttu-id="fe28b-184">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe28b-184">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fe28b-185">Remove um elemento da seleção em um contêiner de seleção.</span><span class="sxs-lookup"><span data-stu-id="fe28b-185">Removes an element from the selection in a selection container.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe28b-186"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-selectionitempattern_select"><strong>SelectionItemPattern_Select</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe28b-186"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-selectionitempattern_select"><strong>SelectionItemPattern_Select</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fe28b-187">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="fe28b-187">This function is deprecated.</span></span> <span data-ttu-id="fe28b-188">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe28b-188">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fe28b-189">Seleciona um elemento em um contêiner de seleção.</span><span class="sxs-lookup"><span data-stu-id="fe28b-189">Selects an element in a selection container.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe28b-190"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-synchronizedinputpattern_cancel"><strong>SynchronizedInputPattern_Cancel</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe28b-190"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-synchronizedinputpattern_cancel"><strong>SynchronizedInputPattern_Cancel</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fe28b-191">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="fe28b-191">This function is deprecated.</span></span> <span data-ttu-id="fe28b-192">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe28b-192">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fe28b-193">Faz com que o provedor de automação da interface do usuário pare de escutar a entrada do mouse ou do teclado.</span><span class="sxs-lookup"><span data-stu-id="fe28b-193">Causes the UI Automation provider to stop listening for mouse or keyboard input.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe28b-194"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-synchronizedinputpattern_startlistening"><strong>SynchronizedInputPattern_StartListening</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe28b-194"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-synchronizedinputpattern_startlistening"><strong>SynchronizedInputPattern_StartListening</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fe28b-195">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="fe28b-195">This function is deprecated.</span></span> <span data-ttu-id="fe28b-196">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe28b-196">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fe28b-197">Faz com que o provedor de automação da interface do usuário comece a escutar a entrada do mouse ou do teclado.</span><span class="sxs-lookup"><span data-stu-id="fe28b-197">Causes the UI Automation provider to start listening for mouse or keyboard input.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe28b-198"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_get_documentrange"><strong>TextPattern_get_DocumentRange</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe28b-198"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_get_documentrange"><strong>TextPattern_get_DocumentRange</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fe28b-199">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="fe28b-199">This function is deprecated.</span></span> <span data-ttu-id="fe28b-200">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe28b-200">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fe28b-201">Obtém o intervalo de texto para o documento inteiro.</span><span class="sxs-lookup"><span data-stu-id="fe28b-201">Gets the text range for the entire document.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe28b-202"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_get_supportedtextselection"><strong>TextPattern_get_SupportedTextSelection</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe28b-202"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_get_supportedtextselection"><strong>TextPattern_get_SupportedTextSelection</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fe28b-203">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="fe28b-203">This function is deprecated.</span></span> <span data-ttu-id="fe28b-204">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe28b-204">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fe28b-205">Asseguro se o conteúdo do contêiner de texto pode ser selecionado e desmarcado.</span><span class="sxs-lookup"><span data-stu-id="fe28b-205">Ascertains whether the text container's contents can be selected and deselected.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe28b-206"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_getselection"><strong>TextPattern_GetSelection</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe28b-206"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_getselection"><strong>TextPattern_GetSelection</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fe28b-207">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="fe28b-207">This function is deprecated.</span></span> <span data-ttu-id="fe28b-208">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe28b-208">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fe28b-209">Obtém o intervalo atual do texto selecionado de um contêiner de texto que dá suporte ao padrão de texto.</span><span class="sxs-lookup"><span data-stu-id="fe28b-209">Gets the current range of selected text from a text container supporting the text pattern.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe28b-210"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_getvisibleranges"><strong>TextPattern_GetVisibleRanges</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe28b-210"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_getvisibleranges"><strong>TextPattern_GetVisibleRanges</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fe28b-211">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="fe28b-211">This function is deprecated.</span></span> <span data-ttu-id="fe28b-212">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe28b-212">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fe28b-213">Recupera uma matriz de intervalos de texto não contíguos de um contêiner de texto em que cada intervalo de texto começa com a primeira linha parcialmente visível até o final da última linha parcialmente visível.</span><span class="sxs-lookup"><span data-stu-id="fe28b-213">Retrieves an array of disjoint text ranges from a text container where each text range begins with the first partially visible line through to the end of the last partially visible line.</span></span> <span data-ttu-id="fe28b-214">Por exemplo, um layout de várias colunas em que as colunas são parcialmente roladas para fora da área visível do visor e o conteúdo flui da parte inferior de uma coluna para a parte superior da próxima.</span><span class="sxs-lookup"><span data-stu-id="fe28b-214">For example, a multi-column layout where the columns are partially scrolled out of the visible area of the viewport and the content flows from the bottom of one column to the top of the next.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe28b-215"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_rangefromchild"><strong>TextPattern_RangeFromChild</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe28b-215"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_rangefromchild"><strong>TextPattern_RangeFromChild</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fe28b-216">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="fe28b-216">This function is deprecated.</span></span> <span data-ttu-id="fe28b-217">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe28b-217">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fe28b-218">Obtém o intervalo de texto que um determinado nó abrange.</span><span class="sxs-lookup"><span data-stu-id="fe28b-218">Gets the text range that a given node spans.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe28b-219"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_rangefrompoint"><strong>TextPattern_RangeFromPoint</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe28b-219"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_rangefrompoint"><strong>TextPattern_RangeFromPoint</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fe28b-220">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="fe28b-220">This function is deprecated.</span></span> <span data-ttu-id="fe28b-221">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe28b-221">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fe28b-222">Recupera o intervalo de texto degenerado (vazio) mais próximo às coordenadas de tela especificadas.</span><span class="sxs-lookup"><span data-stu-id="fe28b-222">Retrieves the degenerate (empty) text range nearest to the specified screen coordinates.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe28b-223"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_addtoselection"><strong>TextRange_AddToSelection</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe28b-223"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_addtoselection"><strong>TextRange_AddToSelection</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fe28b-224">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="fe28b-224">This function is deprecated.</span></span> <span data-ttu-id="fe28b-225">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe28b-225">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fe28b-226">Adiciona à coleção existente de texto realçado em um contêiner de texto que dá suporte a várias seleções não combinadas realçando o texto suplementar correspondente aos pontos de extremidade de <em>início</em> e <em>término</em> do intervalo de texto de chamada.</span><span class="sxs-lookup"><span data-stu-id="fe28b-226">Adds to the existing collection of highlighted text in a text container that supports multiple, disjoint selections by highlighting supplementary text corresponding to the calling text range <em>Start</em> and <em>End</em> endpoints.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe28b-227"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_clone"><strong>TextRange_Clone</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe28b-227"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_clone"><strong>TextRange_Clone</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fe28b-228">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="fe28b-228">This function is deprecated.</span></span> <span data-ttu-id="fe28b-229">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe28b-229">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fe28b-230">Copia um intervalo de texto.</span><span class="sxs-lookup"><span data-stu-id="fe28b-230">Copies a text range.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe28b-231"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_compare"><strong>TextRange_Compare</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe28b-231"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_compare"><strong>TextRange_Compare</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fe28b-232">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="fe28b-232">This function is deprecated.</span></span> <span data-ttu-id="fe28b-233">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe28b-233">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fe28b-234">Compara dois intervalos de texto.</span><span class="sxs-lookup"><span data-stu-id="fe28b-234">Compares two text ranges.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe28b-235"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_compareendpoints"><strong>TextRange_CompareEndpoints</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe28b-235"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_compareendpoints"><strong>TextRange_CompareEndpoints</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fe28b-236">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="fe28b-236">This function is deprecated.</span></span> <span data-ttu-id="fe28b-237">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe28b-237">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fe28b-238">Retorna um valor que indica se dois intervalos de texto têm pontos de extremidade idênticos.</span><span class="sxs-lookup"><span data-stu-id="fe28b-238">Returns a value indicating whether two text ranges have identical endpoints.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe28b-239"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_expandtoenclosingunit"><strong>TextRange_ExpandToEnclosingUnit</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe28b-239"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_expandtoenclosingunit"><strong>TextRange_ExpandToEnclosingUnit</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fe28b-240">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="fe28b-240">This function is deprecated.</span></span> <span data-ttu-id="fe28b-241">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe28b-241">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fe28b-242">Expande o intervalo de texto para uma unidade maior ou menor, como caractere, palavra, linha ou página.</span><span class="sxs-lookup"><span data-stu-id="fe28b-242">Expands the text range to a larger or smaller unit such as Character, Word, Line, or Page.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe28b-243"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_findattribute"><strong>TextRange_FindAttribute</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe28b-243"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_findattribute"><strong>TextRange_FindAttribute</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fe28b-244">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="fe28b-244">This function is deprecated.</span></span> <span data-ttu-id="fe28b-245">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe28b-245">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fe28b-246">Pesquisa em uma direção especificada para a primeira parte do texto que dá suporte a um atributo de texto especificado.</span><span class="sxs-lookup"><span data-stu-id="fe28b-246">Searches in a specified direction for the first piece of text supporting a specified text attribute.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe28b-247"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_findtext"><strong>TextRange_FindText</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe28b-247"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_findtext"><strong>TextRange_FindText</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fe28b-248">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="fe28b-248">This function is deprecated.</span></span> <span data-ttu-id="fe28b-249">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe28b-249">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fe28b-250">Retorna o primeiro intervalo de texto na direção especificada que contém o texto que o cliente está pesquisando.</span><span class="sxs-lookup"><span data-stu-id="fe28b-250">Returns the first text range in the specified direction that contains the text the client is searching for.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe28b-251"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_getattributevalue"><strong>TextRange_GetAttributeValue</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe28b-251"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_getattributevalue"><strong>TextRange_GetAttributeValue</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fe28b-252">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="fe28b-252">This function is deprecated.</span></span> <span data-ttu-id="fe28b-253">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe28b-253">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fe28b-254">Obtém o valor de um atributo de texto para um intervalo de texto.</span><span class="sxs-lookup"><span data-stu-id="fe28b-254">Gets the value of an text attribute for a text range.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe28b-255"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_getboundingrectangles"><strong>TextRange_GetBoundingRectangles</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe28b-255"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_getboundingrectangles"><strong>TextRange_GetBoundingRectangles</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fe28b-256">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="fe28b-256">This function is deprecated.</span></span> <span data-ttu-id="fe28b-257">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe28b-257">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fe28b-258">Recupera o número mínimo de retângulos delimitadores que podem incluir o intervalo, um retângulo por linha.</span><span class="sxs-lookup"><span data-stu-id="fe28b-258">Retrieves the minimum number of bounding rectangles that can enclose the range, one rectangle per line.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe28b-259"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_getchildren"><strong>TextRange_GetChildren</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe28b-259"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_getchildren"><strong>TextRange_GetChildren</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fe28b-260">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="fe28b-260">This function is deprecated.</span></span> <span data-ttu-id="fe28b-261">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe28b-261">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fe28b-262">Retorna todos os elementos de automação da interface do usuário contidos no intervalo de texto especificado.</span><span class="sxs-lookup"><span data-stu-id="fe28b-262">Returns all UI Automation elements contained within the specified text range.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe28b-263"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_getenclosingelement"><strong>TextRange_GetEnclosingElement</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe28b-263"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_getenclosingelement"><strong>TextRange_GetEnclosingElement</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fe28b-264">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="fe28b-264">This function is deprecated.</span></span> <span data-ttu-id="fe28b-265">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe28b-265">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fe28b-266">Retorna o nó para o próximo provedor menor que abrange o intervalo.</span><span class="sxs-lookup"><span data-stu-id="fe28b-266">Returns the node for the next smallest provider that covers the range.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe28b-267"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_gettext"><strong>TextRange_GetText</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe28b-267"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_gettext"><strong>TextRange_GetText</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fe28b-268">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="fe28b-268">This function is deprecated.</span></span> <span data-ttu-id="fe28b-269">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe28b-269">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fe28b-270">Retorna o texto em um intervalo de texto, até um número especificado de caracteres.</span><span class="sxs-lookup"><span data-stu-id="fe28b-270">Returns the text in a text range, up to a specified number of characters.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe28b-271"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_move"><strong>TextRange_Move</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe28b-271"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_move"><strong>TextRange_Move</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fe28b-272">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="fe28b-272">This function is deprecated.</span></span> <span data-ttu-id="fe28b-273">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe28b-273">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fe28b-274">Move o intervalo de texto do número especificado de unidades solicitadas pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="fe28b-274">Moves the text range the specified number of units requested by the client.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe28b-275"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_moveendpointbyrange"><strong>TextRange_MoveEndpointByRange</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe28b-275"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_moveendpointbyrange"><strong>TextRange_MoveEndpointByRange</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fe28b-276">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="fe28b-276">This function is deprecated.</span></span> <span data-ttu-id="fe28b-277">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe28b-277">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fe28b-278">Move um ponto de extremidade de um intervalo para o ponto de extremidade de outro intervalo.</span><span class="sxs-lookup"><span data-stu-id="fe28b-278">Moves an endpoint of one range to the endpoint of another range.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe28b-279"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_moveendpointbyunit"><strong>TextRange_MoveEndpointByUnit</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe28b-279"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_moveendpointbyunit"><strong>TextRange_MoveEndpointByUnit</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fe28b-280">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="fe28b-280">This function is deprecated.</span></span> <span data-ttu-id="fe28b-281">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe28b-281">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fe28b-282">Move um ponto de extremidade do intervalo do número especificado de unidades.</span><span class="sxs-lookup"><span data-stu-id="fe28b-282">Moves an endpoint of the range the specified number of units.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe28b-283"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_removefromselection"><strong>TextRange_RemoveFromSelection</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe28b-283"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_removefromselection"><strong>TextRange_RemoveFromSelection</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fe28b-284">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="fe28b-284">This function is deprecated.</span></span> <span data-ttu-id="fe28b-285">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe28b-285">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fe28b-286">Remove o texto selecionado, que corresponde ao intervalo de texto de chamada <em>TextPatternRangeEndpoint_Start</em> e <em>TextPatternRangeEndpoint_End</em> pontos de extremidade, de uma coleção existente de texto selecionado em um contêiner de texto que dá suporte a várias seleções não associadas.</span><span class="sxs-lookup"><span data-stu-id="fe28b-286">Removes the selected text, corresponding to the calling text range <em>TextPatternRangeEndpoint_Start</em> and <em>TextPatternRangeEndpoint_End</em> endpoints, from an existing collection of selected text in a text container that supports multiple, disjoint selections.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe28b-287"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_scrollintoview"><strong>TextRange_ScrollIntoView</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe28b-287"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_scrollintoview"><strong>TextRange_ScrollIntoView</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fe28b-288">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="fe28b-288">This function is deprecated.</span></span> <span data-ttu-id="fe28b-289">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe28b-289">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fe28b-290">Rola o texto para que o intervalo especificado fique visível no visor.</span><span class="sxs-lookup"><span data-stu-id="fe28b-290">Scrolls the text so the specified range is visible in the viewport.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe28b-291"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_select"><strong>TextRange_Select</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe28b-291"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_select"><strong>TextRange_Select</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fe28b-292">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="fe28b-292">This function is deprecated.</span></span> <span data-ttu-id="fe28b-293">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe28b-293">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fe28b-294">Seleciona um intervalo de texto.</span><span class="sxs-lookup"><span data-stu-id="fe28b-294">Selects a text range.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe28b-295"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-togglepattern_toggle"><strong>TogglePattern_Toggle</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe28b-295"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-togglepattern_toggle"><strong>TogglePattern_Toggle</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fe28b-296">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="fe28b-296">This function is deprecated.</span></span> <span data-ttu-id="fe28b-297">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe28b-297">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fe28b-298">Alterna um controle para seu próximo estado com suporte.</span><span class="sxs-lookup"><span data-stu-id="fe28b-298">Toggles a control to its next supported state.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe28b-299"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-transformpattern_move"><strong>TransformPattern_Move</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe28b-299"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-transformpattern_move"><strong>TransformPattern_Move</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fe28b-300">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="fe28b-300">This function is deprecated.</span></span> <span data-ttu-id="fe28b-301">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe28b-301">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fe28b-302">Move um elemento para um local especificado na tela.</span><span class="sxs-lookup"><span data-stu-id="fe28b-302">Moves an element to a specified location on the screen.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe28b-303"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-transformpattern_resize"><strong>TransformPattern_Resize</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe28b-303"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-transformpattern_resize"><strong>TransformPattern_Resize</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fe28b-304">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="fe28b-304">This function is deprecated.</span></span> <span data-ttu-id="fe28b-305">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe28b-305">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fe28b-306">Redimensiona um elemento na tela.</span><span class="sxs-lookup"><span data-stu-id="fe28b-306">Resizes an element on the screen.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe28b-307"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-transformpattern_rotate"><strong>TransformPattern_Rotate</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe28b-307"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-transformpattern_rotate"><strong>TransformPattern_Rotate</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fe28b-308">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="fe28b-308">This function is deprecated.</span></span> <span data-ttu-id="fe28b-309">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe28b-309">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fe28b-310">Gira um elemento na tela.</span><span class="sxs-lookup"><span data-stu-id="fe28b-310">Rotates an element on the screen.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe28b-311"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-valuepattern_setvalue"><strong>ValuePattern_SetValue</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe28b-311"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-valuepattern_setvalue"><strong>ValuePattern_SetValue</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fe28b-312">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="fe28b-312">This function is deprecated.</span></span> <span data-ttu-id="fe28b-313">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe28b-313">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fe28b-314">Define o valor de texto de um elemento.</span><span class="sxs-lookup"><span data-stu-id="fe28b-314">Sets the text value of an element.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe28b-315"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-virtualizeditempattern_realize"><strong>VirtualizedItemPattern_Realize</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe28b-315"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-virtualizeditempattern_realize"><strong>VirtualizedItemPattern_Realize</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fe28b-316">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="fe28b-316">This function is deprecated.</span></span> <span data-ttu-id="fe28b-317">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe28b-317">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fe28b-318">Torna o item virtual totalmente acessível como um elemento de Automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe28b-318">Makes the virtual item fully accessible as a UI Automation element.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe28b-319"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-windowpattern_close"><strong>WindowPattern_Close</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe28b-319"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-windowpattern_close"><strong>WindowPattern_Close</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fe28b-320">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="fe28b-320">This function is deprecated.</span></span> <span data-ttu-id="fe28b-321">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe28b-321">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fe28b-322">Fecha uma janela aberta.</span><span class="sxs-lookup"><span data-stu-id="fe28b-322">Closes an open window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe28b-323"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-windowpattern_setwindowvisualstate"><strong>WindowPattern_SetWindowVisualState</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe28b-323"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-windowpattern_setwindowvisualstate"><strong>WindowPattern_SetWindowVisualState</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fe28b-324">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="fe28b-324">This function is deprecated.</span></span> <span data-ttu-id="fe28b-325">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe28b-325">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fe28b-326">Define o estado visual de uma janela; por exemplo, para maximizar uma janela.</span><span class="sxs-lookup"><span data-stu-id="fe28b-326">Sets the visual state of a window; for example, to maximize a window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe28b-327"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-windowpattern_waitforinputidle"><strong>WindowPattern_WaitForInputIdle</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe28b-327"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-windowpattern_waitforinputidle"><strong>WindowPattern_WaitForInputIdle</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fe28b-328">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="fe28b-328">This function is deprecated.</span></span> <span data-ttu-id="fe28b-329">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe28b-329">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fe28b-330">Faz com que o código de chamada bloqueie pelo tempo especificado ou até que o processo associado entre em um estado ocioso, aquele que for concluído primeiro.</span><span class="sxs-lookup"><span data-stu-id="fe28b-330">Causes the calling code to block for the specified time or until the associated process enters an idle state, whichever completes first.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="fe28b-331">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fe28b-331">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe28b-332">Clientes de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="fe28b-332">UI Automation Clients</span></span>](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

 





