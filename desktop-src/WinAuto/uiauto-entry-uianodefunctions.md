---
title: Funções de nó preteridas
description: Funções de nó preteridas
ms.assetid: 72833757-a356-4727-8fc8-77a60e26aa99
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7273ffd6c704c9db6408165d1eba3a293f3d1cf
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "103917749"
---
# <a name="deprecated-node-functions"></a><span data-ttu-id="a7900-103">Funções de nó preteridas</span><span class="sxs-lookup"><span data-stu-id="a7900-103">Deprecated Node Functions</span></span>

> [!Note]  
> <span data-ttu-id="a7900-104">As funções de padrão de controle descritas nesta seção são preteridas.</span><span class="sxs-lookup"><span data-stu-id="a7900-104">The control pattern functions described in this section are deprecated.</span></span> <span data-ttu-id="a7900-105">Os aplicativos cliente devem usar as interfaces de Component Object Model (COM) descritas nas seções a seguir:</span><span class="sxs-lookup"><span data-stu-id="a7900-105">Client applications should use the Component Object Model (COM) interfaces described in the following sections:</span></span>
>
> -   [<span data-ttu-id="a7900-106">Interfaces de elementos de automação da interface do usuário para clientes</span><span class="sxs-lookup"><span data-stu-id="a7900-106">UI Automation Element Interfaces for Clients</span></span>](uiauto-entry-uiautoclientinterfaces.md)
> -   [<span data-ttu-id="a7900-107">Interface de condição de propriedade para clientes</span><span class="sxs-lookup"><span data-stu-id="a7900-107">Property Condition Interface for Clients</span></span>](uiauto-client-propconditioninterfaces.md)
> -   [<span data-ttu-id="a7900-108">Interfaces de padrão de controle para clientes</span><span class="sxs-lookup"><span data-stu-id="a7900-108">Control Pattern Interfaces for Clients</span></span>](uiauto-client-controlpatterninterfaces.md)
> -   [<span data-ttu-id="a7900-109">Interfaces de manipulação de eventos para clientes</span><span class="sxs-lookup"><span data-stu-id="a7900-109">Event Handling Interfaces for Clients</span></span>](uiauto-client-eventhandlinginterfaces.md)
> -   [<span data-ttu-id="a7900-110">Interfaces de fábrica de proxy para clientes</span><span class="sxs-lookup"><span data-stu-id="a7900-110">Proxy Factory Interfaces for Clients</span></span>](uiauto-client-proxyfactoryinterfaces.md)

 

## <a name="in-this-section"></a><span data-ttu-id="a7900-111">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="a7900-111">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a7900-112">Função</span><span class="sxs-lookup"><span data-stu-id="a7900-112">Function</span></span></th>
<th><span data-ttu-id="a7900-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="a7900-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a7900-114"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaaddevent"><strong>UiaAddEvent</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7900-114"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaaddevent"><strong>UiaAddEvent</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="a7900-115">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="a7900-115">This function is deprecated.</span></span> <span data-ttu-id="a7900-116">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a7900-116">Client applications should use the Microsoft UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="a7900-117">Adiciona um ouvinte para eventos em um nó na árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="a7900-117">Adds a listener for events on a node in the UI Automation tree.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7900-118"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaeventaddwindow"><strong>UiaEventAddWindow</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7900-118"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaeventaddwindow"><strong>UiaEventAddWindow</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="a7900-119">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="a7900-119">This function is deprecated.</span></span> <span data-ttu-id="a7900-120">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="a7900-120">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="a7900-121">Adiciona uma janela ao ouvinte de eventos.</span><span class="sxs-lookup"><span data-stu-id="a7900-121">Adds a window to the event listener.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7900-122"><a href="/windows/desktop/api/UIAutomationCoreApi/nc-uiautomationcoreapi-uiaeventcallback"><em>UiaEventCallback</em></a></span><span class="sxs-lookup"><span data-stu-id="a7900-122"><a href="/windows/desktop/api/UIAutomationCoreApi/nc-uiautomationcoreapi-uiaeventcallback"><em>UiaEventCallback</em></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="a7900-123">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="a7900-123">This function is deprecated.</span></span> <span data-ttu-id="a7900-124">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="a7900-124">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="a7900-125">Uma função implementada pelo cliente que é chamada pela automação da interface do usuário quando é gerado um evento que o cliente assinou.</span><span class="sxs-lookup"><span data-stu-id="a7900-125">A client-implemented function that is called by UI Automation when an event is raised that the client has subscribed to.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7900-126"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaeventremovewindow"><strong>UiaEventRemoveWindow</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7900-126"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaeventremovewindow"><strong>UiaEventRemoveWindow</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="a7900-127">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="a7900-127">This function is deprecated.</span></span> <span data-ttu-id="a7900-128">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="a7900-128">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="a7900-129">Remove uma janela do ouvinte de eventos.</span><span class="sxs-lookup"><span data-stu-id="a7900-129">Removes a window from the event listener.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7900-130"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiafind"><strong>UiaFind</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7900-130"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiafind"><strong>UiaFind</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="a7900-131">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="a7900-131">This function is deprecated.</span></span> <span data-ttu-id="a7900-132">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="a7900-132">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="a7900-133">Recupera um ou mais nós de automação da interface do usuário que correspondem aos critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="a7900-133">Retrieves one or more UI Automation nodes that match the search criteria.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7900-134"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiageterrordescription"><strong>UiaGetErrorDescription</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7900-134"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiageterrordescription"><strong>UiaGetErrorDescription</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="a7900-135">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="a7900-135">This function is deprecated.</span></span> <span data-ttu-id="a7900-136">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="a7900-136">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="a7900-137">Obtém uma cadeia de caracteres de erro para que possa ser passada para o cliente.</span><span class="sxs-lookup"><span data-stu-id="a7900-137">Gets an error string so that it can be passed to the client.</span></span> <span data-ttu-id="a7900-138">Esse método não é usado diretamente pelos clientes.</span><span class="sxs-lookup"><span data-stu-id="a7900-138">This method is not used directly by clients.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7900-139"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetpatternprovider"><strong>UiaGetPatternProvider</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7900-139"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetpatternprovider"><strong>UiaGetPatternProvider</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="a7900-140">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="a7900-140">This function is deprecated.</span></span> <span data-ttu-id="a7900-141">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="a7900-141">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="a7900-142">Recupera um <em>padrão de controle</em>.</span><span class="sxs-lookup"><span data-stu-id="a7900-142">Retrieves a <em>control pattern</em>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7900-143"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetpropertyvalue"><strong>UiaGetPropertyValue</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7900-143"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetpropertyvalue"><strong>UiaGetPropertyValue</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="a7900-144">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="a7900-144">This function is deprecated.</span></span> <span data-ttu-id="a7900-145">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="a7900-145">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="a7900-146">Recupera o valor de uma propriedade de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="a7900-146">Retrieves the value of a UI Automation property.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7900-147"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetrootnode"><strong>UiaGetRootNode</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7900-147"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetrootnode"><strong>UiaGetRootNode</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="a7900-148">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="a7900-148">This function is deprecated.</span></span> <span data-ttu-id="a7900-149">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="a7900-149">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="a7900-150">Recupera o nó de automação da interface do usuário raiz.</span><span class="sxs-lookup"><span data-stu-id="a7900-150">Retrieves the root UI Automation node.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7900-151"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetruntimeid"><strong>UiaGetRuntimeId</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7900-151"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetruntimeid"><strong>UiaGetRuntimeId</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="a7900-152">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="a7900-152">This function is deprecated.</span></span> <span data-ttu-id="a7900-153">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="a7900-153">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="a7900-154">Recupera o identificador de tempo de execução de um nó de automação de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="a7900-154">Retrieves the runtime identifier of a UI Automation node.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7900-155"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetupdatedcache"><strong>UiaGetUpdatedCache</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7900-155"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetupdatedcache"><strong>UiaGetUpdatedCache</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="a7900-156">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="a7900-156">This function is deprecated.</span></span> <span data-ttu-id="a7900-157">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="a7900-157">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="a7900-158">Atualiza o cache de valores de propriedade e padrões de controle.</span><span class="sxs-lookup"><span data-stu-id="a7900-158">Updates the cache of property values and control patterns.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7900-159"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahpatternobjectfromvariant"><strong>UiaHPatternObjectFromVariant</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7900-159"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahpatternobjectfromvariant"><strong>UiaHPatternObjectFromVariant</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="a7900-160">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="a7900-160">This function is deprecated.</span></span> <span data-ttu-id="a7900-161">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="a7900-161">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="a7900-162">Obtém um objeto de padrão de controle de um tipo <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>Variant</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="a7900-162">Gets a control pattern object from a <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>VARIANT</strong></a> type.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7900-163"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahtextrangefromvariant"><strong>UiaHTextRangeFromVariant</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7900-163"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahtextrangefromvariant"><strong>UiaHTextRangeFromVariant</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="a7900-164">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="a7900-164">This function is deprecated.</span></span> <span data-ttu-id="a7900-165">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="a7900-165">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="a7900-166">Obtém um intervalo de texto de um tipo <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>Variant</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="a7900-166">Gets a text range from a <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>VARIANT</strong></a> type.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7900-167"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahuianodefromvariant"><strong>UiaHUiaNodeFromVariant</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7900-167"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahuianodefromvariant"><strong>UiaHUiaNodeFromVariant</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="a7900-168">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="a7900-168">This function is deprecated.</span></span> <span data-ttu-id="a7900-169">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="a7900-169">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="a7900-170">Obtém um HUIANODE de um tipo <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>Variant</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="a7900-170">Gets an HUIANODE from a <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>VARIANT</strong></a> type.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7900-171"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uialookupid"><strong>UiaLookupId</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7900-171"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uialookupid"><strong>UiaLookupId</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="a7900-172">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="a7900-172">This function is deprecated.</span></span> <span data-ttu-id="a7900-173">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="a7900-173">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="a7900-174">Obtém o identificador de inteiro que pode ser usado em métodos que exigem uma PROPERTYid, o PATTERNid, o CONTROLTYPEid, o textattributeid ou EVENTID.</span><span class="sxs-lookup"><span data-stu-id="a7900-174">Gets the integer identifier that can be used in methods that require a PROPERTYID, PATTERNID, CONTROLTYPEID, TEXTATTRIBUTEID, or EVENTID.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7900-175"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianavigate"><strong>UiaNavigate</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7900-175"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianavigate"><strong>UiaNavigate</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="a7900-176">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="a7900-176">This function is deprecated.</span></span> <span data-ttu-id="a7900-177">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="a7900-177">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="a7900-178">Navega na árvore de automação da interface do usuário, recuperando opcionalmente as informações armazenadas em cache.</span><span class="sxs-lookup"><span data-stu-id="a7900-178">Navigates in the UI Automation tree, optionally retrieving cached information.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7900-179"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromfocus"><strong>UiaNodeFromFocus</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7900-179"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromfocus"><strong>UiaNodeFromFocus</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="a7900-180">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="a7900-180">This function is deprecated.</span></span> <span data-ttu-id="a7900-181">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="a7900-181">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="a7900-182">Recupera o nó de automação da interface do usuário para o elemento de interface do usuário que atualmente tem o foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="a7900-182">Retrieves the UI Automation node for the UI element that currently has input focus.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7900-183"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromhandle"><strong>UiaNodeFromHandle</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7900-183"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromhandle"><strong>UiaNodeFromHandle</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="a7900-184">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="a7900-184">This function is deprecated.</span></span> <span data-ttu-id="a7900-185">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="a7900-185">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="a7900-186">Recupera o nó de automação da interface do usuário associado a uma janela.</span><span class="sxs-lookup"><span data-stu-id="a7900-186">Retrieves the UI Automation node associated with a window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7900-187"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefrompoint"><strong>UiaNodeFromPoint</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7900-187"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefrompoint"><strong>UiaNodeFromPoint</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="a7900-188">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="a7900-188">This function is deprecated.</span></span> <span data-ttu-id="a7900-189">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="a7900-189">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="a7900-190">Recupera o nó de automação da interface do usuário para o elemento no ponto especificado.</span><span class="sxs-lookup"><span data-stu-id="a7900-190">Retrieves the UI Automation node for the element at the specified point.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7900-191"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromprovider"><strong>UiaNodeFromProvider</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7900-191"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromprovider"><strong>UiaNodeFromProvider</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="a7900-192">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="a7900-192">This function is deprecated.</span></span> <span data-ttu-id="a7900-193">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="a7900-193">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="a7900-194">Recupera o nó de automação da interface do usuário para um provedor de elementos brutos.</span><span class="sxs-lookup"><span data-stu-id="a7900-194">Retrieves the UI Automation node for a raw element provider.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7900-195"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianoderelease"><strong>UiaNodeRelease</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7900-195"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianoderelease"><strong>UiaNodeRelease</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="a7900-196">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="a7900-196">This function is deprecated.</span></span> <span data-ttu-id="a7900-197">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="a7900-197">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="a7900-198">Exclui um nó da memória.</span><span class="sxs-lookup"><span data-stu-id="a7900-198">Deletes a node from memory.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7900-199"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiapatternrelease"><strong>UiaPatternRelease</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7900-199"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiapatternrelease"><strong>UiaPatternRelease</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="a7900-200">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="a7900-200">This function is deprecated.</span></span> <span data-ttu-id="a7900-201">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="a7900-201">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="a7900-202">Exclui um objeto de padrão alocado da memória.</span><span class="sxs-lookup"><span data-stu-id="a7900-202">Deletes an allocated pattern object from memory.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7900-203"><a href="/windows/desktop/api/UIAutomationCoreApi/nc-uiautomationcoreapi-uiaprovidercallback"><em>UiaProviderCallback</em></a></span><span class="sxs-lookup"><span data-stu-id="a7900-203"><a href="/windows/desktop/api/UIAutomationCoreApi/nc-uiautomationcoreapi-uiaprovidercallback"><em>UiaProviderCallback</em></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="a7900-204">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="a7900-204">This function is deprecated.</span></span> <span data-ttu-id="a7900-205">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="a7900-205">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="a7900-206">Uma função definida pelo aplicativo que é chamada pela automação da interface do usuário para obter um provedor do lado do cliente para um elemento.</span><span class="sxs-lookup"><span data-stu-id="a7900-206">An application-defined function that is called by UI Automation to obtain a client-side provider for an element.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7900-207"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiarectisempty"><strong>UiaRectIsEmpty</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7900-207"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiarectisempty"><strong>UiaRectIsEmpty</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="a7900-208">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="a7900-208">This function is deprecated.</span></span> <span data-ttu-id="a7900-209">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="a7900-209">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="a7900-210">Obtém um valor booliano que especifica se um retângulo tem todas as suas coordenadas definidas como 0.</span><span class="sxs-lookup"><span data-stu-id="a7900-210">Gets a Boolean value that specifies whether a rectangle has all its coordinates set to 0.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7900-211"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiarectsetempty"><strong>UiaRectSetEmpty</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7900-211"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiarectsetempty"><strong>UiaRectSetEmpty</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="a7900-212">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="a7900-212">This function is deprecated.</span></span> <span data-ttu-id="a7900-213">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="a7900-213">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="a7900-214">Define os elementos de uma estrutura <a href="/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiarect"><strong>UiaRect</strong></a> como 0.</span><span class="sxs-lookup"><span data-stu-id="a7900-214">Sets the elements of a <a href="/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiarect"><strong>UiaRect</strong></a> structure to 0.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7900-215"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaregisterprovidercallback"><strong>UiaRegisterProviderCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7900-215"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaregisterprovidercallback"><strong>UiaRegisterProviderCallback</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="a7900-216">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="a7900-216">This function is deprecated.</span></span> <span data-ttu-id="a7900-217">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="a7900-217">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="a7900-218">Registra o método definido pelo aplicativo que é chamado pela automação da interface do usuário para obter um provedor de um elemento.</span><span class="sxs-lookup"><span data-stu-id="a7900-218">Registers the application-defined method that is called by UI Automation to obtain a provider for an element.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7900-219"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaremoveevent"><strong>UiaRemoveEvent</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7900-219"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaremoveevent"><strong>UiaRemoveEvent</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="a7900-220">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="a7900-220">This function is deprecated.</span></span> <span data-ttu-id="a7900-221">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="a7900-221">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="a7900-222">Remove um ouvinte de eventos em um nó na árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="a7900-222">Removes a listener for events on a node in the UI Automation tree.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7900-223"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiasetfocus"><strong>UiaSetFocus</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7900-223"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiasetfocus"><strong>UiaSetFocus</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="a7900-224">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="a7900-224">This function is deprecated.</span></span> <span data-ttu-id="a7900-225">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="a7900-225">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="a7900-226">Define o foco de entrada para o elemento especificado na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="a7900-226">Sets the input focus to the specified element in the UI.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7900-227"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiatextrangerelease"><strong>UiaTextRangeRelease</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7900-227"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiatextrangerelease"><strong>UiaTextRangeRelease</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="a7900-228">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="a7900-228">This function is deprecated.</span></span> <span data-ttu-id="a7900-229">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="a7900-229">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="a7900-230">Exclui um objeto de intervalo de texto alocado da memória.</span><span class="sxs-lookup"><span data-stu-id="a7900-230">Deletes an allocated text range object from memory.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="a7900-231">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a7900-231">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7900-232">Clientes de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="a7900-232">UI Automation Clients</span></span>](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

