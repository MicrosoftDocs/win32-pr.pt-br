---
title: Visão Geral dos Provedores de Automação de Interface do Usuário
description: Este tópico fornece uma visão geral de como os desenvolvedores de controle implementam provedores de automação de interface do usuário.
ms.assetid: 8928c889-0e0a-439f-87e8-a9d121fcf73f
keywords:
- Automação da interface do usuário, visão geral dos provedores
- Automação da interface do usuário, tipos de provedor
- Automação da interface do usuário, conceitos do provedor
- provedores, sobre
- provedores, tipos
- provedores, conceitos
- provedores, elementos
- provedores, navegação
- provedores, exibições
- provedores, estruturas
- provedores, fragmentos
- provedores, hosts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f70a806fe33b16eed2555c123cc50f1f2b28da
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916155"
---
# <a name="ui-automation-providers-overview"></a><span data-ttu-id="abad6-115">Visão Geral dos Provedores de Automação de Interface do Usuário</span><span class="sxs-lookup"><span data-stu-id="abad6-115">UI Automation Providers Overview</span></span>

<span data-ttu-id="abad6-116">Um provedor de automação de interface do usuário da Microsoft é um objeto de software que expõe um elemento da interface do usuário de um aplicativo para que os aplicativos cliente de acessibilidade possam recuperar informações sobre o elemento e invocar sua funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="abad6-116">A Microsoft UI Automation provider is a software object that exposes an element of an application's UI so that accessibility client applications can retrieve information about the element and invoke its functionality.</span></span> <span data-ttu-id="abad6-117">Em geral, cada controle ou outro elemento distinto em uma interface do usuário tem um provedor.</span><span class="sxs-lookup"><span data-stu-id="abad6-117">In general, each control or other distinct element in a UI has a provider.</span></span>

<span data-ttu-id="abad6-118">A Microsoft inclui um provedor para cada um dos controles padrão fornecidos com o Microsoft Win32, Windows Forms e Windows Presentation Foundation (WPF).</span><span class="sxs-lookup"><span data-stu-id="abad6-118">Microsoft includes a provider for each of the standard controls that are supplied with Microsoft Win32, Windows Forms, and Windows Presentation Foundation (WPF).</span></span> <span data-ttu-id="abad6-119">Isso significa que os controles padrão são expostos automaticamente para clientes de automação da interface do usuário; Você não precisa implementar interfaces de acessibilidade para os controles padrão.</span><span class="sxs-lookup"><span data-stu-id="abad6-119">This means that the standard controls are automatically exposed to UI Automation clients; you do not need to implement any accessibility interfaces for the standard controls.</span></span>

<span data-ttu-id="abad6-120">Se seu aplicativo incluir controles personalizados, você precisará implementar provedores de automação de interface do usuário para que esses controles os tornem acessíveis a aplicativos cliente de acessibilidade.</span><span class="sxs-lookup"><span data-stu-id="abad6-120">If your application includes any custom controls, you need to implement UI Automation providers for those controls to make them accessible to accessibility client applications.</span></span> <span data-ttu-id="abad6-121">Você também precisa implementar provedores para controles de terceiros que não incluem um provedor.</span><span class="sxs-lookup"><span data-stu-id="abad6-121">You also need to implement providers for any third party controls that do not include a provider.</span></span> <span data-ttu-id="abad6-122">Você implementa um provedor implementando interfaces de provedor de automação de interface do usuário e interfaces de padrão de controle.</span><span class="sxs-lookup"><span data-stu-id="abad6-122">You implement a provider by implementing UI Automation provider interfaces and control pattern interfaces.</span></span>

<span data-ttu-id="abad6-123">Este tópico fornece uma visão geral de como os desenvolvedores de controle implementam provedores de automação de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="abad6-123">This topic provides an overview of how control developers implement UI Automation providers.</span></span> <span data-ttu-id="abad6-124">Ele inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="abad6-124">It includes the following sections.</span></span>

-   [<span data-ttu-id="abad6-125">Tipos de provedores</span><span class="sxs-lookup"><span data-stu-id="abad6-125">Types of Providers</span></span>](#types-of-providers)
-   [<span data-ttu-id="abad6-126">Conceitos do provedor de automação de interface do usuário</span><span class="sxs-lookup"><span data-stu-id="abad6-126">UI Automation Provider Concepts</span></span>](#ui-automation-provider-concepts)
    -   [<span data-ttu-id="abad6-127">Elementos</span><span class="sxs-lookup"><span data-stu-id="abad6-127">Elements</span></span>](#elements)
    -   [<span data-ttu-id="abad6-128">Estruturas</span><span class="sxs-lookup"><span data-stu-id="abad6-128">Frameworks</span></span>](#frameworks)
    -   [<span data-ttu-id="abad6-129">Fragmentos</span><span class="sxs-lookup"><span data-stu-id="abad6-129">Fragments</span></span>](#fragments)
    -   [<span data-ttu-id="abad6-130">Hosts</span><span class="sxs-lookup"><span data-stu-id="abad6-130">Hosts</span></span>](#hosts)
-   [<span data-ttu-id="abad6-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="abad6-131">Related topics</span></span>](#related-topics)

## <a name="types-of-providers"></a><span data-ttu-id="abad6-132">Tipos de provedores</span><span class="sxs-lookup"><span data-stu-id="abad6-132">Types of Providers</span></span>

<span data-ttu-id="abad6-133">Os provedores de automação da interface do usuário se enquadram em duas categorias: provedores do lado do servidor e provedores do lado do cliente (ou *proxy*).</span><span class="sxs-lookup"><span data-stu-id="abad6-133">UI Automation providers fall into two categories: server-side providers, and client-side (or *proxy*) providers.</span></span>

<span data-ttu-id="abad6-134">Um provedor do lado do servidor é um objeto, como um controle personalizado, que contém sua própria implementação nativa das interfaces do provedor de automação de interface do usuário relevantes.</span><span class="sxs-lookup"><span data-stu-id="abad6-134">A server-side provider is an object, such as a custom control, that contains its own native implementation of the relevant UI Automation provider interfaces.</span></span> <span data-ttu-id="abad6-135">Um provedor do lado do servidor se comunica com aplicativos cliente durante o limite do processo expondo sua implementação das interfaces do provedor com o núcleo de automação da interface do usuário, que fornece solicitações de clientes.</span><span class="sxs-lookup"><span data-stu-id="abad6-135">A server-side provider communicates with client applications across the process boundary by exposing its implementation of the provider interfaces to the UI Automation core, which services requests from clients.</span></span> <span data-ttu-id="abad6-136">Para obter mais informações sobre provedores do lado do servidor, consulte [implementando um provedor de automação de interface do usuário Server-Side](uiauto-serversideprovider.md).</span><span class="sxs-lookup"><span data-stu-id="abad6-136">For more information about server-side providers, see [Implementing a Server-Side UI Automation Provider](uiauto-serversideprovider.md).</span></span>

<span data-ttu-id="abad6-137">Um provedor do lado do cliente, ou proxy, é um objeto que implementa interfaces do provedor de automação da interface do usuário em nome de um controle não inclui uma implementação de provedor completa.</span><span class="sxs-lookup"><span data-stu-id="abad6-137">A client-side provider, or proxy, is an object that implements UI Automation provider interfaces on behalf of a control does not include a full provider implementation of its own.</span></span> <span data-ttu-id="abad6-138">Sem um proxy, esse controle é amplamente opaco para a automação da interface do usuário, que pode fornecer apenas informações básicas disponíveis no identificador de janela (**HWND**), como o local do controle.</span><span class="sxs-lookup"><span data-stu-id="abad6-138">Without a proxy, such a control is largely opaque to UI Automation, which can supply only basic information available from the window handle (**HWND**), such as the control location.</span></span> <span data-ttu-id="abad6-139">Normalmente, os provedores de proxy se comunicam com o aplicativo durante o limite do processo enviando e recebendo mensagens do Windows.</span><span class="sxs-lookup"><span data-stu-id="abad6-139">Typically, proxy providers communicate with the application across the process boundary by sending and receiving Windows messages.</span></span> <span data-ttu-id="abad6-140">Para obter mais informações, consulte [implementando um provedor de automação de interface do usuário de Client-Side (proxy)](uiauto-clientsideprovider.md).</span><span class="sxs-lookup"><span data-stu-id="abad6-140">For more information, see [Implementing a Client-Side (Proxy) UI Automation Provider](uiauto-clientsideprovider.md).</span></span>

## <a name="ui-automation-provider-concepts"></a><span data-ttu-id="abad6-141">Conceitos do provedor de automação de interface do usuário</span><span class="sxs-lookup"><span data-stu-id="abad6-141">UI Automation Provider Concepts</span></span>

<span data-ttu-id="abad6-142">Esta seção fornece breves explicações de alguns dos principais conceitos que você precisa entender para implementar provedores de automação de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="abad6-142">This section provides brief explanations of some of the key concepts you need to understand in order to implement UI Automation providers.</span></span>

### <a name="elements"></a><span data-ttu-id="abad6-143">Elementos</span><span class="sxs-lookup"><span data-stu-id="abad6-143">Elements</span></span>

<span data-ttu-id="abad6-144">Elementos de automação da interface do usuário são partes da interface do usuário, normalmente janelas ou controles, que são visíveis para clientes de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="abad6-144">UI Automation elements are pieces of the UI—typically windows or controls—that are visible to UI Automation clients.</span></span> <span data-ttu-id="abad6-145">Os exemplos incluem janelas de aplicativo, painéis, botões, dicas de ferramenta, caixas de listagem e itens de lista.</span><span class="sxs-lookup"><span data-stu-id="abad6-145">Examples include application windows, panes, buttons, tooltips, list boxes, and list items.</span></span>

<span data-ttu-id="abad6-146">Os elementos de automação da interface do usuário são expostos aos clientes como uma árvore.</span><span class="sxs-lookup"><span data-stu-id="abad6-146">UI Automation elements are exposed to clients as a tree.</span></span> <span data-ttu-id="abad6-147">A automação da interface do usuário constrói a árvore navegando de um elemento para outro.</span><span class="sxs-lookup"><span data-stu-id="abad6-147">UI Automation constructs the tree by navigating from one element to another.</span></span> <span data-ttu-id="abad6-148">A navegação é habilitada pelo provedor para cada elemento.</span><span class="sxs-lookup"><span data-stu-id="abad6-148">Navigation is enabled by the provider for each element.</span></span> <span data-ttu-id="abad6-149">Cada elemento pode apontar para seu próprio elemento pai, seus elementos irmãos e seus primeiros e último elementos filho.</span><span class="sxs-lookup"><span data-stu-id="abad6-149">Each element can point to its own parent element, its sibling elements, and its first and last child elements.</span></span>

<span data-ttu-id="abad6-150">Um cliente pode ver a árvore de automação da interface do usuário em três exibições principais, conforme descrito na tabela a seguir:</span><span class="sxs-lookup"><span data-stu-id="abad6-150">A client can see the UI Automation tree in three principal views, as described in the following table:</span></span>



| <span data-ttu-id="abad6-151">Visualizar</span><span class="sxs-lookup"><span data-stu-id="abad6-151">View</span></span>         | <span data-ttu-id="abad6-152">Descrição</span><span class="sxs-lookup"><span data-stu-id="abad6-152">Description</span></span>                                                    |
|--------------|----------------------------------------------------------------|
| <span data-ttu-id="abad6-153">Exibição bruta</span><span class="sxs-lookup"><span data-stu-id="abad6-153">Raw view</span></span>     | <span data-ttu-id="abad6-154">Inclui todos os elementos.</span><span class="sxs-lookup"><span data-stu-id="abad6-154">Includes all elements.</span></span>                                         |
| <span data-ttu-id="abad6-155">Exibição de controle</span><span class="sxs-lookup"><span data-stu-id="abad6-155">Control view</span></span> | <span data-ttu-id="abad6-156">Inclui elementos que são controles.</span><span class="sxs-lookup"><span data-stu-id="abad6-156">Includes elements that are controls.</span></span>                           |
| <span data-ttu-id="abad6-157">Exibição de conteúdo</span><span class="sxs-lookup"><span data-stu-id="abad6-157">Content view</span></span> | <span data-ttu-id="abad6-158">Inclui elementos de controle que transmitem informações para o usuário.</span><span class="sxs-lookup"><span data-stu-id="abad6-158">Includes control elements that convey information to the user.</span></span> |



 

<span data-ttu-id="abad6-159">É responsabilidade da implementação do provedor definir um elemento como um elemento de conteúdo ou um elemento de controle.</span><span class="sxs-lookup"><span data-stu-id="abad6-159">It is the responsibility of the provider implementation to define an element as a content element or a control element.</span></span> <span data-ttu-id="abad6-160">Elementos de controle podem ou não ser elementos de conteúdo, mas todos os elementos de conteúdo são elementos de controle.</span><span class="sxs-lookup"><span data-stu-id="abad6-160">Control elements may or may not also be content elements, but all content elements are control elements.</span></span>

<span data-ttu-id="abad6-161">Para obter mais informações sobre a exibição de cliente da árvore, consulte [visão geral da árvore de automação da interface do usuário](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="abad6-161">For more information on the client view of the tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>

### <a name="frameworks"></a><span data-ttu-id="abad6-162">Estruturas</span><span class="sxs-lookup"><span data-stu-id="abad6-162">Frameworks</span></span>

<span data-ttu-id="abad6-163">Uma estrutura é um componente que gerencia controles filho, testes de clique e renderização em uma área da tela.</span><span class="sxs-lookup"><span data-stu-id="abad6-163">A framework is a component that manages child controls, hit-testing, and rendering in an area of the screen.</span></span> <span data-ttu-id="abad6-164">Por exemplo, uma janela Win32, geralmente chamada de **HWND**, pode servir como uma estrutura que contém vários elementos de automação da interface do usuário, como uma barra de menus, uma barra de status e botões.</span><span class="sxs-lookup"><span data-stu-id="abad6-164">For example, a Win32 window, often referred to as an **HWND**, can serve as a framework that contains multiple UI Automation elements, such as a menu bar, a status bar, and buttons.</span></span>

<span data-ttu-id="abad6-165">Controles de contêiner do Win32, como caixas de listagem e controles de exibição de árvore, são considerados estruturas porque contêm seu próprio código para renderizar itens filho e executar testes de impacto neles.</span><span class="sxs-lookup"><span data-stu-id="abad6-165">Win32 container controls such as list boxes and tree-view controls are considered to be frameworks because they contain their own code for rendering child items and performing hit-testing on them.</span></span> <span data-ttu-id="abad6-166">Por outro lado, uma caixa de listagem do WPF não é uma estrutura, pois a renderização e o teste de impacto estão sendo tratados pela janela que a contém.</span><span class="sxs-lookup"><span data-stu-id="abad6-166">By contrast, a WPF list box is not a framework, because the rendering and hit-testing is being handled by the containing window.</span></span>

<span data-ttu-id="abad6-167">A interface do usuário em um aplicativo pode ser composta de estruturas diferentes.</span><span class="sxs-lookup"><span data-stu-id="abad6-167">The UI in an application can be made up of different frameworks.</span></span> <span data-ttu-id="abad6-168">Por exemplo, um **HWND** em um aplicativo pode conter HTML dinâmico (DHTML) que, por sua vez, pode conter um componente, como uma caixa de combinação em um **HWND**.</span><span class="sxs-lookup"><span data-stu-id="abad6-168">For example, an **HWND** in an application might contain Dynamic HTML (DHTML) which in turn can contain a component such as a combo box in an **HWND**.</span></span>

### <a name="fragments"></a><span data-ttu-id="abad6-169">Fragmentos</span><span class="sxs-lookup"><span data-stu-id="abad6-169">Fragments</span></span>

<span data-ttu-id="abad6-170">Uma subárvore completa de elementos de uma estrutura específica é chamada de fragmento.</span><span class="sxs-lookup"><span data-stu-id="abad6-170">A complete subtree of elements from a particular framework is called a fragment.</span></span> <span data-ttu-id="abad6-171">O elemento no nó raiz da subárvore é chamado de raiz do fragmento.</span><span class="sxs-lookup"><span data-stu-id="abad6-171">The element at the root node of the subtree is called a fragment root.</span></span> <span data-ttu-id="abad6-172">Uma raiz de fragmento não tem um pai, mas está hospedada em alguma outra estrutura, geralmente uma janela Win32 (**HWND**).</span><span class="sxs-lookup"><span data-stu-id="abad6-172">A fragment root does not have a parent, but is hosted within some other framework, usually a Win32 window (**HWND**).</span></span>

### <a name="hosts"></a><span data-ttu-id="abad6-173">Hosts</span><span class="sxs-lookup"><span data-stu-id="abad6-173">Hosts</span></span>

<span data-ttu-id="abad6-174">O nó raiz de cada fragmento deve ser hospedado em um elemento, geralmente uma janela Win32 (**HWND**).</span><span class="sxs-lookup"><span data-stu-id="abad6-174">The root node of every fragment must be hosted in an element, usually a Win32 window (**HWND**).</span></span> <span data-ttu-id="abad6-175">A exceção é a área de trabalho, que não está hospedada em nenhum outro elemento.</span><span class="sxs-lookup"><span data-stu-id="abad6-175">The exception is the desktop, which is not hosted in any other element.</span></span> <span data-ttu-id="abad6-176">O host de um controle personalizado é o **HWND** do próprio controle, não a janela do aplicativo ou qualquer outra janela que possa conter grupos de controles de nível superior.</span><span class="sxs-lookup"><span data-stu-id="abad6-176">The host of a custom control is the **HWND** of the control itself, not the application window or any other window that might contain groups of top-level controls.</span></span>

<span data-ttu-id="abad6-177">O host de um fragmento desempenha um papel importante no fornecimento de serviços de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="abad6-177">The host of a fragment plays an important role in providing UI Automation services.</span></span> <span data-ttu-id="abad6-178">Ele permite a navegação para a raiz do fragmento e fornece algumas propriedades padrão para que o provedor personalizado não precise implementá-las.</span><span class="sxs-lookup"><span data-stu-id="abad6-178">It enables navigation to the fragment root, and supplies some default properties so that the custom provider does not have to implement them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="abad6-179">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="abad6-179">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="abad6-180">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="abad6-180">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="abad6-181">Implementando um provedor de automação de interface do usuário Client-Side</span><span class="sxs-lookup"><span data-stu-id="abad6-181">Implementing a Client-Side UI Automation Provider</span></span>](uiauto-clientsideprovider.md)
</dt> <dt>

[<span data-ttu-id="abad6-182">Implementando um provedor de automação de interface do usuário Server-Side</span><span class="sxs-lookup"><span data-stu-id="abad6-182">Implementing a Server-Side UI Automation Provider</span></span>](uiauto-serversideprovider.md)
</dt> <dt>

[<span data-ttu-id="abad6-183">Visão geral da árvore de automação de interface do usuário</span><span class="sxs-lookup"><span data-stu-id="abad6-183">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




