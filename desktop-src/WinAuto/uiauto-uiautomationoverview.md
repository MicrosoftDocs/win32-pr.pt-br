---
title: Visão geral de automação da interface do usuário
description: A automação da interface do usuário da Microsoft é uma estrutura de acessibilidade para o Windows.
ms.assetid: 99610542-761c-432d-a4ac-4cd3812577a8
keywords:
- Automação da interface do usuário, sobre
- Automação da interface do usuário, acessibilidade
- Automação da interface do usuário, componentes
- Automação da interface do usuário, API do provedor
- Automação da interface do usuário, API do cliente
- Automação da interface do usuário, arquivos de cabeçalho
- Automação da interface do usuário, modelo
- components
- acessibilidade
- API do provedor
- API do cliente
- arquivos de cabeçalho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20ea29b0abd4c6ed791ae3195f36a0f8184c8596
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2020
ms.locfileid: "104365508"
---
# <a name="ui-automation-overview"></a><span data-ttu-id="0337b-115">Visão geral de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="0337b-115">UI Automation Overview</span></span>

<span data-ttu-id="0337b-116">A automação da interface do usuário da Microsoft é uma estrutura de acessibilidade para o Windows.</span><span class="sxs-lookup"><span data-stu-id="0337b-116">Microsoft UI Automation is an accessibility framework for Windows.</span></span> <span data-ttu-id="0337b-117">Ele fornece acesso programático à maioria dos elementos da interface do usuário na área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="0337b-117">It provides programmatic access to most UI elements on the desktop.</span></span> <span data-ttu-id="0337b-118">Ele permite que produtos de tecnologia assistencial, como leitores de tela, forneçam informações sobre a interface do usuário aos usuários finais e manipulem a interface do usuário por meio de entrada padrão.</span><span class="sxs-lookup"><span data-stu-id="0337b-118">It enables assistive technology products, such as screen readers, to provide information about the UI to end users and to manipulate the UI by means other than standard input.</span></span> <span data-ttu-id="0337b-119">A automação da interface do usuário também permite que scripts de teste automatizados interajam com a interface do usuário</span><span class="sxs-lookup"><span data-stu-id="0337b-119">UI Automation also allows automated test scripts to interact with the UI.</span></span>

<span data-ttu-id="0337b-120">A automação da interface do usuário foi disponibilizada pela primeira vez no Windows XP como parte da estrutura de Microsoft .NET.</span><span class="sxs-lookup"><span data-stu-id="0337b-120">UI Automation was first available in Windows XP as part of the Microsoft .NET Framework.</span></span> <span data-ttu-id="0337b-121">Embora uma API C++ não gerenciada também tenha sido publicada nesse momento, a utilidade das funções de cliente era limitada devido a problemas de interoperabilidade.</span><span class="sxs-lookup"><span data-stu-id="0337b-121">Although an unmanaged C++ API was also published at that time, the usefulness of client functions was limited because of interoperability issues.</span></span> <span data-ttu-id="0337b-122">Para o Windows 7, a API foi reescrita na Component Object Model (COM).</span><span class="sxs-lookup"><span data-stu-id="0337b-122">For Windows 7, the API has been rewritten in the Component Object Model (COM).</span></span>

> [!Note]  
> <span data-ttu-id="0337b-123">Embora as funções de biblioteca introduzidas na versão anterior da automação da interface do usuário ainda estejam documentadas, elas não devem ser usadas em novos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="0337b-123">Although the library functions introduced in the earlier version of UI Automation are still documented, they should not be used in new applications.</span></span>

 

<span data-ttu-id="0337b-124">Os aplicativos cliente de automação da interface do usuário podem ser escritos com a garantia de que funcionarão em várias estruturas de controle do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="0337b-124">UI Automation client applications can be written with the assurance that they will work on multiple Microsoft Windows control frameworks.</span></span> <span data-ttu-id="0337b-125">O núcleo de automação da interface do usuário mascara quaisquer diferenças nas estruturas que se basear em várias partes da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="0337b-125">The UI Automation core masks any differences in the frameworks that underlie various pieces of the UI.</span></span> <span data-ttu-id="0337b-126">Por exemplo, a propriedade **Content** de um botão Windows Presentation Foundation (WPF), a propriedade **Caption** de um botão do Microsoft Win32 e a propriedade **ALT** de uma imagem HTML são todas mapeadas para uma única propriedade, **Name**, no modo de exibição de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="0337b-126">For example, the **Content** property of a Windows Presentation Foundation (WPF) button, the **Caption** property of a Microsoft Win32 button, and the **ALT** property of an HTML image are all mapped to a single property, **Name**, in the UI Automation view.</span></span>

<span data-ttu-id="0337b-127">A automação da interface do usuário fornece funcionalidade completa no Windows XP, no Windows Server 2003 e em sistemas operacionais posteriores.</span><span class="sxs-lookup"><span data-stu-id="0337b-127">UI Automation provides full functionality in Windows XP, Windows Server 2003, and later operating systems.</span></span>

<span data-ttu-id="0337b-128">Provedores de automação de interface do usuário são componentes que implementam o suporte à automação da interface do usuário em controles e oferecem suporte a aplicativos cliente do Microsoft Acessibilidade Ativa, por meio de um serviço de ponte interno.</span><span class="sxs-lookup"><span data-stu-id="0337b-128">UI Automation providers are components that implement UI Automation support on controls and offer some support for Microsoft Active Accessibility client applications, through a built-in bridging service.</span></span>

> [!Note]  
> <span data-ttu-id="0337b-129">A automação da interface do usuário não permite a comunicação entre os processos iniciados por usuários diferentes por meio do comando **Executar como** .</span><span class="sxs-lookup"><span data-stu-id="0337b-129">UI Automation does not enable communication between processes that are started by different users through the **Run as** command.</span></span>

 

<span data-ttu-id="0337b-130">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="0337b-130">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="0337b-131">Componentes de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="0337b-131">UI Automation Components</span></span>](#ui-automation-components)
-   [<span data-ttu-id="0337b-132">Arquivos de cabeçalho da automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="0337b-132">UI Automation Header Files</span></span>](#ui-automation-header-files)
-   [<span data-ttu-id="0337b-133">Modelo de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="0337b-133">UI Automation Model</span></span>](#ui-automation-model)
-   [<span data-ttu-id="0337b-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0337b-134">Related topics</span></span>](#related-topics)

## <a name="ui-automation-components"></a><span data-ttu-id="0337b-135">Componentes de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="0337b-135">UI Automation Components</span></span>

<span data-ttu-id="0337b-136">A automação da interface do usuário tem quatro componentes principais, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="0337b-136">UI Automation has four main components, as shown in the following table.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0337b-137">Componente</span><span class="sxs-lookup"><span data-stu-id="0337b-137">Component</span></span></th>
<th><span data-ttu-id="0337b-138">Descrição</span><span class="sxs-lookup"><span data-stu-id="0337b-138">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0337b-139">API do provedor</span><span class="sxs-lookup"><span data-stu-id="0337b-139">Provider API</span></span></td>
<td><span data-ttu-id="0337b-140">Um conjunto de interfaces COM que são implementadas por provedores de automação de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="0337b-140">A set of COM interfaces that are implemented by UI Automation providers.</span></span> <span data-ttu-id="0337b-141">Provedores de automação de interface do usuário são objetos que fornecem informações sobre elementos de interface do usuário e respondem à entrada programática.</span><span class="sxs-lookup"><span data-stu-id="0337b-141">UI Automation providers are objects that provide information about UI elements and respond to programmatic input.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0337b-142">API do cliente</span><span class="sxs-lookup"><span data-stu-id="0337b-142">Client API</span></span></td>
<td><span data-ttu-id="0337b-143">Um conjunto de interfaces COM que permite que os aplicativos cliente obtenham informações sobre a interface do usuário e enviem entradas para controles.</span><span class="sxs-lookup"><span data-stu-id="0337b-143">A set of COM interfaces that enable client applications to obtain information about the UI and to send input to controls.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="0337b-144">As funções descritas em <a href="uiauto-entry-cpfunctions.md">funções de padrão de controle</a> preteridas e funções de <a href="uiauto-entry-uianodefunctions.md">nó preteridas</a> são preteridas.</span><span class="sxs-lookup"><span data-stu-id="0337b-144">The functions described in <a href="uiauto-entry-cpfunctions.md">Deprecated Control Pattern Functions</a> and <a href="uiauto-entry-uianodefunctions.md">Deprecated Node Functions</a> are deprecated.</span></span> <span data-ttu-id="0337b-145">Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário descritas em <a href="uiauto-entry-uiautoclientinterfaces.md">interfaces de elementos de automação da interface do usuário para clientes</a></span><span class="sxs-lookup"><span data-stu-id="0337b-145">Instead, client applications should use the UI Automation COM interfaces described in <a href="uiauto-entry-uiautoclientinterfaces.md">UI Automation Element Interfaces for Clients</a>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0337b-146">UIAutomationCore.dll</span><span class="sxs-lookup"><span data-stu-id="0337b-146">UIAutomationCore.dll</span></span></td>
<td><span data-ttu-id="0337b-147">A biblioteca de tempo de execução, às vezes chamada de núcleo de automação da interface do usuário, que lida com a comunicação entre provedores e clientes.</span><span class="sxs-lookup"><span data-stu-id="0337b-147">The run-time library, sometimes called the UI Automation core, that handles communication between providers and clients.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0337b-148">Oleacc.dll</span><span class="sxs-lookup"><span data-stu-id="0337b-148">Oleacc.dll</span></span></td>
<td><span data-ttu-id="0337b-149">A biblioteca de tempo de execução para o Microsoft Acessibilidade Ativa e os objetos de proxy.</span><span class="sxs-lookup"><span data-stu-id="0337b-149">The run-time library for Microsoft Active Accessibility and the proxy objects.</span></span> <span data-ttu-id="0337b-150">A biblioteca também fornece objetos proxy usados pelo Microsoft Microsoft Acessibilidade Ativa para o proxy de automação da interface do usuário para dar suporte a controles Win32.</span><span class="sxs-lookup"><span data-stu-id="0337b-150">The library also provides proxy objects used by the Microsoft Microsoft Active Accessibility to UI Automation Proxy to support Win32 controls.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="0337b-151">Há duas maneiras de usar a automação da interface do usuário: para criar suporte para controles personalizados usando a API do provedor e para criar aplicativos cliente que usam o núcleo de automação da interface do usuário para se comunicar com o e recuperar informações sobre os elementos da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="0337b-151">There are two ways of using UI Automation: to create support for custom controls by using the provider API, and to create client applications that use the UI Automation core to communicate with, and retrieve information about, UI elements.</span></span> <span data-ttu-id="0337b-152">Dependendo do seu foco, você deve consultar diferentes partes da documentação.</span><span class="sxs-lookup"><span data-stu-id="0337b-152">Depending on your focus, you should refer to different parts of the documentation.</span></span> <span data-ttu-id="0337b-153">Se você precisar criar suporte para controles personalizados, consulte [Guia do programador do provedor de automação de IU](uiauto-providerportal.md).</span><span class="sxs-lookup"><span data-stu-id="0337b-153">If you need to create support for custom controls, see [UI Automation Provider Programmer's Guide](uiauto-providerportal.md).</span></span> <span data-ttu-id="0337b-154">Se você precisar se comunicar com ou recuperar informações sobre elementos da interface do usuário, consulte [Guia do programador do cliente de automação da interface do usuário](uiauto-clientportal.md).</span><span class="sxs-lookup"><span data-stu-id="0337b-154">If you need to communicate with or retrieve information about UI elements, see [UI Automation Client Programmer's Guide](uiauto-clientportal.md).</span></span>

## <a name="ui-automation-header-files"></a><span data-ttu-id="0337b-155">Arquivos de cabeçalho da automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="0337b-155">UI Automation Header Files</span></span>

<span data-ttu-id="0337b-156">A API de automação da interface do usuário é definida em vários arquivos de cabeçalho do C/C++ diferentes que estão incluídos no SDK (Software Development Kit) do Windows.</span><span class="sxs-lookup"><span data-stu-id="0337b-156">The UI Automation API is defined in several different C/C++ header files that are included with the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="0337b-157">Os arquivos de cabeçalho da automação da interface do usuário são descritos na tabela a seguir:</span><span class="sxs-lookup"><span data-stu-id="0337b-157">The UI Automation header files are described in the following table:</span></span>



| <span data-ttu-id="0337b-158">Arquivo de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0337b-158">Header file</span></span>           | <span data-ttu-id="0337b-159">Descrição</span><span class="sxs-lookup"><span data-stu-id="0337b-159">Description</span></span>                                                                                                                                                                                                                                                                      |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0337b-160">UIAutomationClient. h</span><span class="sxs-lookup"><span data-stu-id="0337b-160">UIAutomationClient.h</span></span>  | <span data-ttu-id="0337b-161">Define as interfaces e os elementos de programação relacionados usados por clientes de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="0337b-161">Defines the interfaces and related programming elements used by UI Automation clients.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="0337b-162">UIAutomationCore. h</span><span class="sxs-lookup"><span data-stu-id="0337b-162">UIAutomationCore.h</span></span>    | <span data-ttu-id="0337b-163">Define as interfaces e os elementos de programação relacionados usados pelos provedores de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="0337b-163">Defines the interfaces and related programming elements used by UI Automation providers.</span></span>                                                                                                                                                                                         |
| <span data-ttu-id="0337b-164">UIAutomationCoreApi. h</span><span class="sxs-lookup"><span data-stu-id="0337b-164">UIAutomationCoreApi.h</span></span> | <span data-ttu-id="0337b-165">Define constantes, GUIDs, tipos de dados e estruturas gerais usadas por clientes e provedores de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="0337b-165">Defines general constants, GUIDs, data types, and structures used by UI Automation clients and providers.</span></span> <span data-ttu-id="0337b-166">Ele também contém definições para as funções de padrão de nó e controle preteridas.</span><span class="sxs-lookup"><span data-stu-id="0337b-166">It also contains definitions for the deprecated node and control pattern functions.</span></span>                                                                                    |
| <span data-ttu-id="0337b-167">Automação da IU. h</span><span class="sxs-lookup"><span data-stu-id="0337b-167">UIAutomation.h</span></span>        | <span data-ttu-id="0337b-168">Inclui todos os outros arquivos de cabeçalho de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="0337b-168">Includes all of the other UI Automation header files.</span></span> <span data-ttu-id="0337b-169">Como a maioria dos aplicativos de automação de interface do usuário requer elementos de todos os arquivos de cabeçalho de automação da interface do usuário, é melhor incluir automação da IU. h em seus projetos de aplicativo de automação da interface do usuário em vez de incluir cada arquivo individualmente</span><span class="sxs-lookup"><span data-stu-id="0337b-169">Because most UI Automation applications require elements from all UI Automation header files, it is best to include UIAutomation.h in your UI Automation application projects instead of including each file individually.</span></span> |



 

<span data-ttu-id="0337b-170">Se você estiver desenvolvendo um aplicativo que usa a API de automação da interface do usuário, deverá incluir automação da IU. h em seu projeto.</span><span class="sxs-lookup"><span data-stu-id="0337b-170">If you are developing an application that uses the UI Automation API, you should include UIAutomation.h in your project.</span></span> <span data-ttu-id="0337b-171">Se seu aplicativo der suporte ao Microsoft Acessibilidade Ativa, inclua o arquivo de cabeçalho OleAcc. h.</span><span class="sxs-lookup"><span data-stu-id="0337b-171">If your application supports Microsoft Active Accessibility, include the Oleacc.h header file.</span></span> <span data-ttu-id="0337b-172">Os aplicativos de automação da interface do usuário que usam GUIDs também exigem o arquivo de cabeçalho Initguid. h.</span><span class="sxs-lookup"><span data-stu-id="0337b-172">UI Automation applications that use GUIDs also require the Initguid.h header file.</span></span> <span data-ttu-id="0337b-173">Se necessário, Initguid. h deve ser incluído antes de automação da IU. h.</span><span class="sxs-lookup"><span data-stu-id="0337b-173">If needed, Initguid.h should be included before UIAutomation.h.</span></span>

## <a name="ui-automation-model"></a><span data-ttu-id="0337b-174">Modelo de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="0337b-174">UI Automation Model</span></span>

<span data-ttu-id="0337b-175">A automação da interface do usuário expõe todos os elementos da interface do usuário para aplicativos cliente como um objeto representado pela interface [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) .</span><span class="sxs-lookup"><span data-stu-id="0337b-175">UI Automation exposes every element of the UI to client applications as an object represented by the [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) interface.</span></span> <span data-ttu-id="0337b-176">Os elementos estão contidos em uma estrutura de árvore, com a área de trabalho como o elemento raiz.</span><span class="sxs-lookup"><span data-stu-id="0337b-176">Elements are contained in a tree structure, with the desktop as the root element.</span></span> <span data-ttu-id="0337b-177">Os clientes podem filtrar a exibição bruta da árvore como uma exibição de controle ou de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="0337b-177">Clients can filter the raw view of the tree as a control view or a content view.</span></span> <span data-ttu-id="0337b-178">Essas exibições padrão da estrutura podem ser facilmente vistas usando o aplicativo de [inspeção](inspect-objects.md) incluído no SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="0337b-178">These standard views of the structure can easily be seen by using the [Inspect](inspect-objects.md) application that is included with the Windows SDK.</span></span> <span data-ttu-id="0337b-179">Os aplicativos também podem criar exibições personalizadas.</span><span class="sxs-lookup"><span data-stu-id="0337b-179">Applications can also create custom views.</span></span>

<span data-ttu-id="0337b-180">Um elemento de automação de interface do usuário expõe propriedades do elemento de controle ou de interface do usuário que ele representa.</span><span class="sxs-lookup"><span data-stu-id="0337b-180">A UI Automation element exposes properties of the control or UI element that it represents.</span></span> <span data-ttu-id="0337b-181">Uma dessas propriedades é o tipo de controle, que define a aparência básica e a funcionalidade do elemento de controle ou de interface do usuário como uma única entidade reconhecível, por exemplo, um botão ou caixa de seleção.</span><span class="sxs-lookup"><span data-stu-id="0337b-181">One of these properties is the control type, which defines the basic appearance and functionality of the control or UI element as a single recognizable entity, for example, a button or check box.</span></span> <span data-ttu-id="0337b-182">Para obter mais informações sobre tipos de controle, consulte [visão geral de tipos de controle de automação da interface do usuário](uiauto-controltypesoverview.md).</span><span class="sxs-lookup"><span data-stu-id="0337b-182">For more information about control types, see [UI Automation Control Types Overview](uiauto-controltypesoverview.md).</span></span>

<span data-ttu-id="0337b-183">Além disso, um elemento de automação da interface do usuário expõe um ou mais padrões de controle.</span><span class="sxs-lookup"><span data-stu-id="0337b-183">In addition, a UI Automation element exposes one or more control patterns.</span></span> <span data-ttu-id="0337b-184">Um padrão de controle fornece um conjunto de propriedades que são específicas a um determinado tipo de controle.</span><span class="sxs-lookup"><span data-stu-id="0337b-184">A control pattern provides a set of properties that are specific to a particular control type.</span></span> <span data-ttu-id="0337b-185">Um padrão de controle também expõe métodos que permitem que aplicativos cliente obtenham mais informações sobre o elemento e forneçam entrada para o elemento.</span><span class="sxs-lookup"><span data-stu-id="0337b-185">A control pattern also exposes methods that enable client applications to get more information about the element and to provide input to the element.</span></span> <span data-ttu-id="0337b-186">Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="0337b-186">For more information about control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>

> [!Note]  
> <span data-ttu-id="0337b-187">Não há nenhuma correspondência de um para um entre tipos de controle e padrões de controle.</span><span class="sxs-lookup"><span data-stu-id="0337b-187">There is no one-to-one correspondence between control types and control patterns.</span></span> <span data-ttu-id="0337b-188">Um padrão de controle pode ser suportado por vários tipos de controle, e um controle pode dar suporte a vários padrões de controle, cada um dos quais expõe diferentes aspectos de seu comportamento.</span><span class="sxs-lookup"><span data-stu-id="0337b-188">A control pattern may be supported by multiple control types, and a control may support multiple control patterns, each of which exposes different aspects of its behavior.</span></span> <span data-ttu-id="0337b-189">Por exemplo, uma caixa de combinação tem pelo menos dois padrões de controle: um que representa sua capacidade de expandir e recolher e outro que representa o mecanismo de seleção.</span><span class="sxs-lookup"><span data-stu-id="0337b-189">For example, a combo box has at least two control patterns: one that represents its ability to expand and collapse, and another that represents the selection mechanism.</span></span> <span data-ttu-id="0337b-190">No entanto, um controle pode exibir apenas um único tipo de controle.</span><span class="sxs-lookup"><span data-stu-id="0337b-190">However, a control can exhibit only a single control type.</span></span>

 

<span data-ttu-id="0337b-191">A automação da interface do usuário fornece informações para aplicativos cliente por meio de eventos.</span><span class="sxs-lookup"><span data-stu-id="0337b-191">UI Automation provides information to client applications through events.</span></span> <span data-ttu-id="0337b-192">Ao contrário de WinEvents, os eventos de automação da interface do usuário não são baseados em um mecanismo de difusão.</span><span class="sxs-lookup"><span data-stu-id="0337b-192">Unlike WinEvents, UI Automation events are not based on a broadcast mechanism.</span></span> <span data-ttu-id="0337b-193">Os clientes de automação da interface do usuário se registram para notificações de eventos específicas e podem solicitar que propriedades específicas e informações de padrão de controle sejam passadas para seus manipuladores de eventos.</span><span class="sxs-lookup"><span data-stu-id="0337b-193">UI Automation clients register for specific event notifications and can request that specific properties and control pattern information be passed to their event handlers.</span></span> <span data-ttu-id="0337b-194">Além disso, um evento de automação da interface do usuário contém uma referência ao elemento que o gerou.</span><span class="sxs-lookup"><span data-stu-id="0337b-194">In addition, a UI Automation event contains a reference to the element that raised it.</span></span> <span data-ttu-id="0337b-195">Os provedores podem melhorar o desempenho gerando eventos de forma seletiva, dependendo se algum cliente está ouvindo.</span><span class="sxs-lookup"><span data-stu-id="0337b-195">Providers can improve performance by raising events selectively, depending on whether any clients are listening.</span></span> <span data-ttu-id="0337b-196">Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="0337b-196">For more information about events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0337b-197">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0337b-197">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="0337b-198">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="0337b-198">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0337b-199">Visão Geral dos Tipos de Controle de Automação de Interface do Usuário</span><span class="sxs-lookup"><span data-stu-id="0337b-199">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="0337b-200">Visão Geral de Padrões de Controle de Automação de Interface de Usuário</span><span class="sxs-lookup"><span data-stu-id="0337b-200">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="0337b-201">Visão geral sobre eventos de automação de interface do usuário</span><span class="sxs-lookup"><span data-stu-id="0337b-201">UI Automation Events Overview</span></span>](uiauto-eventsoverview.md)
</dt> </dl>

 

 





