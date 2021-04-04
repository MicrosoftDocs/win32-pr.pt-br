---
title: Arquitetura e interoperabilidade
description: Este tópico descreve brevemente a arquitetura do Microsoft Acessibilidade Ativa e a automação da interface do usuário da Microsoft e os componentes que permitem a interoperabilidade entre aplicativos com base em duas tecnologias diferentes.
ms.assetid: 7309819c-7c72-4bb3-ab9c-608a27c56d42
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f318e46a6a0ad833b7aedb114974240fc4e52c08
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "104084315"
---
# <a name="architecture-and-interoperability"></a><span data-ttu-id="1dcfb-103">Arquitetura e interoperabilidade</span><span class="sxs-lookup"><span data-stu-id="1dcfb-103">Architecture and Interoperability</span></span>

<span data-ttu-id="1dcfb-104">Este tópico descreve brevemente a arquitetura do Microsoft Acessibilidade Ativa e a automação da interface do usuário da Microsoft e os componentes que permitem a interoperabilidade entre aplicativos com base em duas tecnologias diferentes.</span><span class="sxs-lookup"><span data-stu-id="1dcfb-104">This topic briefly describes the architecture of Microsoft Active Accessibility and Microsoft UI Automation, and the components that allow interoperability between applications based on the two different technologies.</span></span>

<span data-ttu-id="1dcfb-105">Para obter mais informações sobre a interoperabilidade do Microsoft Acessibilidade Ativa e da automação da interface do usuário, consulte [infraestrutura comum](common-infrastructure.md).</span><span class="sxs-lookup"><span data-stu-id="1dcfb-105">For more information about Microsoft Active Accessibility and UI Automation interoperability, see [Common Infrastructure](common-infrastructure.md).</span></span>

<span data-ttu-id="1dcfb-106">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="1dcfb-106">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="1dcfb-107">Arquitetura do Microsoft Acessibilidade Ativa</span><span class="sxs-lookup"><span data-stu-id="1dcfb-107">Microsoft Active Accessibility Architecture</span></span>](#microsoft-active-accessibility-architecture)
-   [<span data-ttu-id="1dcfb-108">Arquitetura de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="1dcfb-108">UI Automation Architecture</span></span>](#ui-automation-architecture)
-   [<span data-ttu-id="1dcfb-109">Microsoft Acessibilidade Ativa e interoperabilidade de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="1dcfb-109">Microsoft Active Accessibility and UI Automation Interoperability</span></span>](#microsoft-active-accessibility-and-ui-automation-interoperability)
-   [<span data-ttu-id="1dcfb-110">A interface IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="1dcfb-110">The IAccessibleEx Interface</span></span>](#the-iaccessibleex-interface)
-   [<span data-ttu-id="1dcfb-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1dcfb-111">Related topics</span></span>](#related-topics)

## <a name="microsoft-active-accessibility-architecture"></a><span data-ttu-id="1dcfb-112">Arquitetura do Microsoft Acessibilidade Ativa</span><span class="sxs-lookup"><span data-stu-id="1dcfb-112">Microsoft Active Accessibility Architecture</span></span>

<span data-ttu-id="1dcfb-113">O Microsoft Acessibilidade Ativa expõe informações básicas sobre controles como o nome do controle, o local na tela e o tipo de controle, bem como informações de estado, como visibilidade e status habilitado/desabilitado.</span><span class="sxs-lookup"><span data-stu-id="1dcfb-113">Microsoft Active Accessibility exposes basic information about controls such as control name, location on screen, and type of control, as well as state information such as visibility and enabled/disabled status.</span></span> <span data-ttu-id="1dcfb-114">A interface do usuário é representada como uma hierarquia de objetos acessíveis; as alterações e ações são representadas como WinEvents.</span><span class="sxs-lookup"><span data-stu-id="1dcfb-114">The UI is represented as a hierarchy of accessible objects; changes and actions are represented as WinEvents.</span></span>

<span data-ttu-id="1dcfb-115">O Microsoft Acessibilidade Ativa consiste nos seguintes componentes:</span><span class="sxs-lookup"><span data-stu-id="1dcfb-115">Microsoft Active Accessibility consists of the following components:</span></span>

-   <span data-ttu-id="1dcfb-116">Objeto acessível — um elemento lógico da interface do usuário (como um botão) que é representado por uma interface de Component Object Model do [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) (com) e um identificador filho inteiro (childID).</span><span class="sxs-lookup"><span data-stu-id="1dcfb-116">Accessible object—A logical UI element (such as a button) that is represented by an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Component Object Model (COM) interface and an integer child identifier (ChildID).</span></span>
-   <span data-ttu-id="1dcfb-117">WinEvents — um sistema de eventos que permite que os servidores Notifiquem os clientes quando um objeto acessível é alterado.</span><span class="sxs-lookup"><span data-stu-id="1dcfb-117">WinEvents—An event system that enables servers to notify clients when an accessible object changes.</span></span> <span data-ttu-id="1dcfb-118">Para obter mais informações, consulte [WinEvents](winevents-infrastructure.md).</span><span class="sxs-lookup"><span data-stu-id="1dcfb-118">For more information, see [WinEvents](winevents-infrastructure.md).</span></span>
-   <span data-ttu-id="1dcfb-119">OLEACC.dll — a biblioteca de link dinâmico, em tempo de execução, que fornece a API do Microsoft Acessibilidade Ativa e a estrutura do sistema de acessibilidade.</span><span class="sxs-lookup"><span data-stu-id="1dcfb-119">OLEACC.dll—The run-time, dynamic-link library that provides the Microsoft Active Accessibility API and the accessibility system framework.</span></span> <span data-ttu-id="1dcfb-120">OLEACC implementa objetos de proxy que fornecem informações de acessibilidade padrão para elementos de interface do usuário padrão, incluindo controles de usuários, menus de usuário e controles comuns.</span><span class="sxs-lookup"><span data-stu-id="1dcfb-120">OLEACC implements proxy objects that provide default accessibility information for standard UI elements, including USER controls, USER menus, and common controls.</span></span>

<span data-ttu-id="1dcfb-121">Para o Microsoft Acessibilidade Ativa, o componente de sistema da estrutura de acessibilidade (OLEACC) ajuda a comunicação entre tecnologias assistenciais (ferramentas de acessibilidade) e aplicativos, como mostra a ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="1dcfb-121">For Microsoft Active Accessibility, the system component of the accessibility framework (OLEACC) helps the communication between assistive technologies (accessibility tools) and applications, as the following illustration shows.</span></span>

![ilustração mostrando como as ferramentas de acessibilidade interagem com aplicativos](images/msaaarch.gif)

<span data-ttu-id="1dcfb-123">Os aplicativos (servidores do Microsoft Acessibilidade Ativa) fornecem informações de acessibilidade da interface do usuário para ferramentas (clientes do Microsoft Acessibilidade Ativa), que interagem com a interface do usuário em nome dos usuários.</span><span class="sxs-lookup"><span data-stu-id="1dcfb-123">The applications (Microsoft Active Accessibility servers) provide UI accessibility information to tools (Microsoft Active Accessibility clients), which interact with the UI on behalf of users.</span></span> <span data-ttu-id="1dcfb-124">O limite de código é um limite de programação e um de processo.</span><span class="sxs-lookup"><span data-stu-id="1dcfb-124">The code boundary is both a programmatic and a process boundary.</span></span>

## <a name="ui-automation-architecture"></a><span data-ttu-id="1dcfb-125">Arquitetura de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="1dcfb-125">UI Automation Architecture</span></span>

<span data-ttu-id="1dcfb-126">Com a automação da interface do usuário, o componente de núcleo de automação da interface do usuário (UIAutomationCore.dll) é carregado nos processos das ferramentas de acessibilidade e dos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="1dcfb-126">With UI Automation, the UI Automation core component (UIAutomationCore.dll) is loaded into both the accessibility tools' and applications' processes.</span></span> <span data-ttu-id="1dcfb-127">O componente principal gerencia a comunicação entre processos, fornece serviços de nível superior, como a pesquisa de elementos por valores de propriedade, e permite a busca em massa ou o cache de propriedades, o que proporciona um melhor desempenho do que a implementação do Microsoft Acessibilidade Ativa.</span><span class="sxs-lookup"><span data-stu-id="1dcfb-127">The core component manages cross-process communication, provides higher level services such as searching for elements by property values, and enables bulk fetching or caching of properties, which provides better performance than the Microsoft Active Accessibility implementation.</span></span>

<span data-ttu-id="1dcfb-128">A automação da interface do usuário inclui objetos de proxy que fornecem informações de interface do usuário sobre elementos padrão da interface, como controles de usuários, menus de usuário e controles comuns.</span><span class="sxs-lookup"><span data-stu-id="1dcfb-128">UI Automation includes proxy objects that provide UI information about standard UI elements such as USER controls, USER menus, and common controls.</span></span> <span data-ttu-id="1dcfb-129">Ele também inclui proxies que permitem que clientes de automação da interface do usuário obtenham informações da interface do usuário de servidores do Microsoft Acessibilidade Ativa.</span><span class="sxs-lookup"><span data-stu-id="1dcfb-129">It also includes proxies that enable UI Automation clients to get UI information from Microsoft Active Accessibility servers.</span></span>

<span data-ttu-id="1dcfb-130">A ilustração a seguir mostra as relações entre as várias compontents de automação de interface do usuário usadas em ferramentas de acessibilidade (clientes) e em aplicativos (provedores).</span><span class="sxs-lookup"><span data-stu-id="1dcfb-130">The following illustration shows the relationships among the various UI Automation compontents used in accessibility tools (clients) and in applications (providers).</span></span>

![ilustração mostrando como os componentes das ferramentas de acessibilidade interagem com aqueles em aplicativos](images/uiaarch.gif)

## <a name="microsoft-active-accessibility-and-ui-automation-interoperability"></a><span data-ttu-id="1dcfb-132">Microsoft Acessibilidade Ativa e interoperabilidade de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="1dcfb-132">Microsoft Active Accessibility and UI Automation Interoperability</span></span>

<span data-ttu-id="1dcfb-133">A automação da interface do usuário para o Microsoft Acessibilidade Ativa Bridge permite que os clientes do Microsoft Acessibilidade Ativa acessem provedores de automação da interface do usuário, convertendo o modelo de objeto de automação da interface para um modelo de objeto Microsoft Acessibilidade Ativa</span><span class="sxs-lookup"><span data-stu-id="1dcfb-133">The UI Automation to Microsoft Active Accessibility Bridge enables Microsoft Active Accessibility clients to access UI Automation providers by converting the UI Automation object model to a Microsoft Active Accessibility object model.</span></span> <span data-ttu-id="1dcfb-134">A ilustração a seguir mostra a função da ponte de interface do usuário de automação para a Microsoft Acessibilidade Ativa.</span><span class="sxs-lookup"><span data-stu-id="1dcfb-134">The following illustration shows the role of the UI Automation-to-Microsoft Active Accessibility Bridge.</span></span>

![ilustração mostrando como a automação da interface do usuário funciona com aplicativos e ferramentas de acessibilidade](images/uiatomsaabridge.gif)

<span data-ttu-id="1dcfb-136">Da mesma forma, o proxy de automação do Microsoft Acessibilidade Ativa para interface do usuário converte modelos de objeto de servidor baseados no Microsoft Acessibilidade Ativa para clientes de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="1dcfb-136">Similarly, the Microsoft Active Accessibility-to-UI Automation Proxy translates Microsoft Active Accessibility-based server object models for UI Automation clients.</span></span> <span data-ttu-id="1dcfb-137">A ilustração a seguir mostra a função do proxy de automação do Microsoft Acessibilidade Ativa para interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="1dcfb-137">The following illustration shows the role of the Microsoft Active Accessibility-to-UI Automation Proxy.</span></span>

![ilustração mostrando como o proxy de automação de interface do usuário funciona com aplicativos e ferramentas de acessibilidade](images/msaatouiaproxy.gif)

## <a name="the-iaccessibleex-interface"></a><span data-ttu-id="1dcfb-139">A interface IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="1dcfb-139">The IAccessibleEx Interface</span></span>

<span data-ttu-id="1dcfb-140">A interface [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) permite que aplicativos existentes ou bibliotecas de interface do usuário estendam seu modelo de objeto do Microsoft acessibilidade ativa para dar suporte à automação da interface do usuário sem reescrever a implementação do zero.</span><span class="sxs-lookup"><span data-stu-id="1dcfb-140">The [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface enables existing applications or UI libraries to extend their Microsoft Active Accessibility object model to support UI Automation without rewriting the implementation from scratch.</span></span> <span data-ttu-id="1dcfb-141">Com o **IAccessibleEx**, você pode implementar apenas as propriedades adicionais de automação da interface do usuário e os padrões de controle necessários para descrever totalmente a interface do usuário e sua funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="1dcfb-141">With **IAccessibleEx**, you can implement only the additional UI Automation properties and control patterns needed to fully describe the UI and its functionality.</span></span>

<span data-ttu-id="1dcfb-142">Como o proxy de automação do Microsoft Acessibilidade Ativa para interface do usuário traduz os modelos de objeto dos servidores Microsoft Acessibilidade Ativa habilitados para [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex)como modelos de objeto de automação da interface do usuário, os clientes de automação da interface do usuário não precisam fazer nenhum trabalho extra.</span><span class="sxs-lookup"><span data-stu-id="1dcfb-142">Because the Microsoft Active Accessibility-to-UI Automation Proxy translates the object models of [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex)-enabled Microsoft Active Accessibility servers as UI Automation object models, UI Automation clients do not need to do any extra work.</span></span> <span data-ttu-id="1dcfb-143">A interface **IAccessibleEx** também pode permitir que clientes em processo do Microsoft acessibilidade ativa interajam diretamente com os provedores de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="1dcfb-143">The **IAccessibleEx** interface can also enable in-process Microsoft Active Accessibility clients to interact directly with UI Automation providers.</span></span>

<span data-ttu-id="1dcfb-144">Para obter mais informações, consulte [a interface IAccessibleEx](iaccessibleex.md).</span><span class="sxs-lookup"><span data-stu-id="1dcfb-144">For more information, see [The IAccessibleEx Interface](iaccessibleex.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1dcfb-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1dcfb-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1dcfb-146">Visão geral da API de automação do Windows</span><span class="sxs-lookup"><span data-stu-id="1dcfb-146">Windows Automation API Overview</span></span>](windows-automation-api-overview.md)
</dt> <dt>

[<span data-ttu-id="1dcfb-147">A interface IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="1dcfb-147">The IAccessibleEx Interface</span></span>](iaccessibleex.md)
</dt> <dt>

[<span data-ttu-id="1dcfb-148">Considerações de segurança para tecnologias assistenciais</span><span class="sxs-lookup"><span data-stu-id="1dcfb-148">Security Considerations for Assistive Technologies</span></span>](uiauto-securityoverview.md)
</dt> </dl>

 

 




