---
title: Fundamentos de automação da interface do usuário
description: Esta seção explica os conceitos fundamentais em que a automação da interface do usuário se baseia.
ms.assetid: 109f113f-9ed0-4a57-b3af-90e831e53c42
keywords:
- Automação da interface do usuário, API do Microsoft Win32
- Automação da interface do usuário, API do Win32
- Automação da interface do usuário, provedores
- Automação da interface do usuário, aplicativos cliente
- clientes, automação da interface do usuário da Microsoft para API do Microsoft Win32
- clientes, automação da interface do usuário para API do Microsoft Win32
- API de Win32
- API do Microsoft Win32
- Automação da interface do usuário para a API do Microsoft Win32
- Automação da interface do usuário da Microsoft para API do Microsoft Win32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ba8147a8dd7f8d03340fad43465c225a174e606
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364216"
---
# <a name="ui-automation-fundamentals"></a><span data-ttu-id="54554-113">Fundamentos de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="54554-113">UI Automation Fundamentals</span></span>

<span data-ttu-id="54554-114">A automação da interface do usuário da Microsoft permite que aplicativos de tecnologia assistencial e ferramentas de teste automatizada interajam com os controles da interface do usuário de outros aplicativos.</span><span class="sxs-lookup"><span data-stu-id="54554-114">Microsoft UI Automation enables assistive technology applications and automated testing tools to interact with the UI controls of other applications.</span></span> <span data-ttu-id="54554-115">Esta seção explica os conceitos fundamentais em que a automação da interface do usuário se baseia.</span><span class="sxs-lookup"><span data-stu-id="54554-115">This section explains the fundamental concepts that UI Automation is based on.</span></span>

<span data-ttu-id="54554-116">A API de automação da interface do usuário está em duas partes.</span><span class="sxs-lookup"><span data-stu-id="54554-116">The UI Automation API is in two parts.</span></span> <span data-ttu-id="54554-117">Uma parte é usada por aplicativos de *provedor de automação de interface do usuário* e a outra é usada por aplicativos *cliente de automação da interface do usuário* .</span><span class="sxs-lookup"><span data-stu-id="54554-117">One part is used by *UI Automation provider* applications, and the other is used by *UI Automation client* applications.</span></span> <span data-ttu-id="54554-118">A API do provedor permite que os desenvolvedores de controle personalizado do Microsoft Win32 e outras estruturas de controle exponham esses controles à automação da interface do usuário e os tornem visíveis para os aplicativos cliente.</span><span class="sxs-lookup"><span data-stu-id="54554-118">The provider API enables developers of Microsoft Win32 custom control and other control frameworks to expose those controls to UI Automation and make them visible to client applications.</span></span> <span data-ttu-id="54554-119">A API do cliente permite que os aplicativos interajam com controles em outros aplicativos e recuperem informações sobre eles.</span><span class="sxs-lookup"><span data-stu-id="54554-119">The client API enables applications to interact with controls in other applications and retrieve information about them.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="54554-120">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="54554-120">In this section</span></span>

-   [<span data-ttu-id="54554-121">Visão geral de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="54554-121">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
-   [<span data-ttu-id="54554-122">Automação e Acessibilidade Ativa da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="54554-122">UI Automation and Active Accessibility</span></span>](uiauto-msaa.md)
-   [<span data-ttu-id="54554-123">Visão geral da árvore de automação de interface do usuário</span><span class="sxs-lookup"><span data-stu-id="54554-123">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
-   [<span data-ttu-id="54554-124">Visão Geral dos Tipos de Controle de Automação de Interface do Usuário</span><span class="sxs-lookup"><span data-stu-id="54554-124">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
-   [<span data-ttu-id="54554-125">Visão Geral de Padrões de Controle de Automação de Interface de Usuário</span><span class="sxs-lookup"><span data-stu-id="54554-125">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
-   [<span data-ttu-id="54554-126">Visão geral das propriedades de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="54554-126">UI Automation Properties Overview</span></span>](uiauto-propertiesoverview.md)
-   [<span data-ttu-id="54554-127">Visão geral sobre eventos de automação de interface do usuário</span><span class="sxs-lookup"><span data-stu-id="54554-127">UI Automation Events Overview</span></span>](uiauto-eventsoverview.md)
-   [<span data-ttu-id="54554-128">Propriedades personalizadas, eventos e padrões de controle</span><span class="sxs-lookup"><span data-stu-id="54554-128">Custom Properties, Events, and Control Patterns</span></span>](uiauto-custompropertieseventscontrolpatterns.md)
-   [<span data-ttu-id="54554-129">Suporte à automação da interface do usuário para conteúdo textual</span><span class="sxs-lookup"><span data-stu-id="54554-129">UI Automation Support for Textual Content</span></span>](uiauto-ui-automation-textpattern-overview.md)
-   [<span data-ttu-id="54554-130">Suporte à automação da interface do usuário para arrastar e soltar</span><span class="sxs-lookup"><span data-stu-id="54554-130">UI Automation Support for Drag-and-Drop</span></span>](ui-automation-support-for-drag-and-drop.md)
-   [<span data-ttu-id="54554-131">Considerações de segurança para tecnologias assistenciais</span><span class="sxs-lookup"><span data-stu-id="54554-131">Security Considerations for Assistive Technologies</span></span>](uiauto-securityoverview.md)
-   [<span data-ttu-id="54554-132">Práticas recomendadas para usar matrizes seguras</span><span class="sxs-lookup"><span data-stu-id="54554-132">Best Practices for Using Safe Arrays</span></span>](uiauto-workingwithsafearrays.md)
-   [<span data-ttu-id="54554-133">Especificação da automação da interface do usuário e promessa da comunidade</span><span class="sxs-lookup"><span data-stu-id="54554-133">UI Automation Specification and Community Promise</span></span>](uiauto-specandcommunitypromise.md)

## <a name="related-topics"></a><span data-ttu-id="54554-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="54554-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54554-135">Automação da Interface do Usuário</span><span class="sxs-lookup"><span data-stu-id="54554-135">UI Automation</span></span>](entry-uiauto-win32.md)
</dt> </dl>

 

 




