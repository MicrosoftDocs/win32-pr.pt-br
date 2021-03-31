---
title: Guia do programador do cliente de automação da interface do usuário
description: Esta seção contém informações sobre como criar aplicativos que usam a automação da interface do usuário da Microsoft para interagir com a interface do usuário de outros aplicativos e a área de trabalho.
ms.assetid: d3616e1f-7b38-4a3e-ac96-72ec70cc13fc
keywords:
- Criando aplicativos cliente de automação de interface do usuário
- Criando aplicativos cliente
- clientes, criando aplicativos de automação da interface do usuário
- clientes, criação de aplicativo de automação da interface do usuário
- Automação da interface do usuário, criando aplicativos cliente
- Automação da interface do usuário, criação de aplicativo cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f353243c8c194e2d732efd1d68bc2894ca930285
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641204"
---
# <a name="ui-automation-client-programmers-guide"></a><span data-ttu-id="eff8a-109">Guia do programador do cliente de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="eff8a-109">UI Automation Client Programmer's Guide</span></span>

<span data-ttu-id="eff8a-110">Esta seção contém informações sobre como criar aplicativos que usam a automação da interface do usuário da Microsoft para interagir com a interface do usuário de outros aplicativos e a área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="eff8a-110">This section contains information about creating applications that use Microsoft UI Automation to interact with the UI of other applications and the desktop.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="eff8a-111">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="eff8a-111">In this section</span></span>

-   [<span data-ttu-id="eff8a-112">Visão geral de clientes de automação de IU</span><span class="sxs-lookup"><span data-stu-id="eff8a-112">UI Automation Clients Overview</span></span>](/windows/desktop/WinAuto/uiauto-clientsoverview)
-   [<span data-ttu-id="eff8a-113">Criando o objeto CUIAutomation</span><span class="sxs-lookup"><span data-stu-id="eff8a-113">Creating the CUIAutomation Object</span></span>](uiauto-creatingcuiautomation.md)
-   [<span data-ttu-id="eff8a-114">Obtendo elementos da automação interface do usuário</span><span class="sxs-lookup"><span data-stu-id="eff8a-114">Obtaining UI Automation Elements</span></span>](uiauto-obtainingelements.md)
-   [<span data-ttu-id="eff8a-115">Recuperando propriedades de elementos de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="eff8a-115">Retrieving Properties from UI Automation Elements</span></span>](uiauto-propertiesforclients.md)
-   [<span data-ttu-id="eff8a-116">Cache de propriedades de automação da interface do usuário e padrões de controle</span><span class="sxs-lookup"><span data-stu-id="eff8a-116">Caching UI Automation Properties and Control Patterns</span></span>](uiauto-cachingforclients.md)
-   [<span data-ttu-id="eff8a-117">Inscrevendo-se em eventos de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="eff8a-117">Subscribing to UI Automation Events</span></span>](uiauto-eventsforclients.md)
-   [<span data-ttu-id="eff8a-118">Trabalhando com controles baseados em texto</span><span class="sxs-lookup"><span data-stu-id="eff8a-118">Working with Text-based Controls</span></span>](uiauto-workingwithtextbasedcontrols.md)
-   [<span data-ttu-id="eff8a-119">Trabalhando com itens virtualizados</span><span class="sxs-lookup"><span data-stu-id="eff8a-119">Working with Virtualized Items</span></span>](uiauto-workingwithvirtualizeditems.md)
-   [<span data-ttu-id="eff8a-120">Acessando servidores Microsoft Acessibilidade Ativa</span><span class="sxs-lookup"><span data-stu-id="eff8a-120">Accessing Microsoft Active Accessibility Servers</span></span>](uiauto-accessingmsaaservers.md)
-   [<span data-ttu-id="eff8a-121">Usando automação de interface do usuário para testes automatizados</span><span class="sxs-lookup"><span data-stu-id="eff8a-121">Using UI Automation for Automated Testing</span></span>](uiauto-usefortesting.md)
-   [<span data-ttu-id="eff8a-122">Noções básicas sobre problemas de dimensionamento de tela</span><span class="sxs-lookup"><span data-stu-id="eff8a-122">Understanding Screen Scaling Issues</span></span>](uiauto-screenscaling.md)
-   [<span data-ttu-id="eff8a-123">Noções básicas sobre problemas de Threading</span><span class="sxs-lookup"><span data-stu-id="eff8a-123">Understanding Threading Issues</span></span>](uiauto-threading.md)
-   [<span data-ttu-id="eff8a-124">Tópicos de instruções para clientes de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="eff8a-124">How-To Topics for UI Automation Clients</span></span>](uiauto-howto-topics-for-uiautomation-clients.md)

## <a name="related-topics"></a><span data-ttu-id="eff8a-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="eff8a-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eff8a-126">Registrando com facilidade de acesso</span><span class="sxs-lookup"><span data-stu-id="eff8a-126">Registering with Ease of Access</span></span>](/windows/desktop/WinAuto/ease-of-access---assistive-technology-registration)
</dt> <dt>

[<span data-ttu-id="eff8a-127">Considerações de segurança para tecnologias assistenciais</span><span class="sxs-lookup"><span data-stu-id="eff8a-127">Security Considerations for Assistive Technologies</span></span>](uiauto-securityoverview.md)
</dt> <dt>

[<span data-ttu-id="eff8a-128">Automação da Interface do Usuário</span><span class="sxs-lookup"><span data-stu-id="eff8a-128">UI Automation</span></span>](entry-uiauto-win32.md)
</dt> </dl>

 

 