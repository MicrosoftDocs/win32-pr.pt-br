---
title: Acessando servidores Microsoft Acessibilidade Ativa
description: O Microsoft Acessibilidade Ativa para o proxy de automação da interface do usuário é um componente de software que permite que os clientes da automação da interface do usuário da Microsoft interajam com os servidores do Microsoft Acessibilidade Ativa que implementam a interface IAccessible nativamente.
ms.assetid: 44690b16-4a9d-4e8b-865a-b428ad616b1e
keywords:
- Automação da interface do usuário, acessando Acessibilidade Ativa
- Automação da interface do usuário, Acessibilidade Ativa
- Proxy de automação da interface do usuário
- Automação da interface do usuário, proxy de automação da IU
- Padrão de controle LegacyIAccessible
- Automação da interface do usuário, padrão de controle LegacyIAccessible
- Acessibilidade Ativa da Microsoft
- Acessibilidade Ativa
- clientes, acessando servidores Acessibilidade Ativa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97319028203351cd9f45b39d133fa38727d6861e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005217"
---
# <a name="accessing-microsoft-active-accessibility-servers"></a><span data-ttu-id="f6995-112">Acessando servidores Microsoft Acessibilidade Ativa</span><span class="sxs-lookup"><span data-stu-id="f6995-112">Accessing Microsoft Active Accessibility Servers</span></span>

<span data-ttu-id="f6995-113">O Microsoft Acessibilidade Ativa para o proxy de automação da interface do usuário é um componente de software que permite que os clientes da automação da interface do usuário da Microsoft interajam com os servidores do Microsoft Acessibilidade Ativa que implementam a interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) nativamente.</span><span class="sxs-lookup"><span data-stu-id="f6995-113">The Microsoft Active Accessibility to UI Automation Proxy is a software component that enables Microsoft UI Automation clients to interact with Microsoft Active Accessibility servers that implement the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface natively.</span></span> <span data-ttu-id="f6995-114">O proxy dá suporte ao padrão de controle [LegacyIAccessible](uiauto-implementinglegacyiaccessible.md) e fornece uma instância da interface [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) para cada servidor do Microsoft acessibilidade ativa detectado.</span><span class="sxs-lookup"><span data-stu-id="f6995-114">The proxy supports the [LegacyIAccessible](uiauto-implementinglegacyiaccessible.md) control pattern, and supplies an instance of the [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) interface for each Microsoft Active Accessibility server detected.</span></span> <span data-ttu-id="f6995-115">Os clientes de automação da interface do usuário usam os métodos expostos por **IUIAutomationLegacyIAccessiblePattern** para acessar as propriedades do Microsoft acessibilidade ativa e os objetos com suporte no servidor.</span><span class="sxs-lookup"><span data-stu-id="f6995-115">UI Automation clients use the methods exposed by **IUIAutomationLegacyIAccessiblePattern** to access the Microsoft Active Accessibility properties and objects supported by the server.</span></span>

<span data-ttu-id="f6995-116">Se um elemento de automação da interface do usuário tiver uma implementação subjacente do Microsoft Acessibilidade Ativa, um cliente poderá obter um ponteiro de interface [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) para o elemento, passando a ID do padrão de controle [**UIA \_ LegacyIAccessiblePatternId**](uiauto-controlpattern-ids.md) para um dos seguintes métodos [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) :</span><span class="sxs-lookup"><span data-stu-id="f6995-116">If a UI Automation element has an underlying Microsoft Active Accessibility implementation, a client can obtain an [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) interface pointer for the element by passing the [**UIA\_LegacyIAccessiblePatternId**](uiauto-controlpattern-ids.md) control pattern ID to one of the following [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) methods:</span></span>

-   [<span data-ttu-id="f6995-117">**GetCachedPattern**</span><span class="sxs-lookup"><span data-stu-id="f6995-117">**GetCachedPattern**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpattern)
-   [<span data-ttu-id="f6995-118">**GetCachedPatternAs**</span><span class="sxs-lookup"><span data-stu-id="f6995-118">**GetCachedPatternAs**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpatternas)
-   [<span data-ttu-id="f6995-119">**GetCurrentPattern**</span><span class="sxs-lookup"><span data-stu-id="f6995-119">**GetCurrentPattern**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern)
-   [<span data-ttu-id="f6995-120">**GetCurrentPatternAs**</span><span class="sxs-lookup"><span data-stu-id="f6995-120">**GetCurrentPatternAs**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpatternas)

<span data-ttu-id="f6995-121">A interface [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) não está disponível para controles baseados na automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="f6995-121">The [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) interface is not available for controls based on UI Automation.</span></span>

<span data-ttu-id="f6995-122">A interface [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) permite que clientes de automação da interface do usuário acessem a implementação base do [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) de um elemento Microsoft acessibilidade ativa.</span><span class="sxs-lookup"><span data-stu-id="f6995-122">The [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) interface enables UI Automation clients to access the underlying [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) implementation of an Microsoft Active Accessibility element.</span></span> <span data-ttu-id="f6995-123">No entanto, a interface não oferece suporte a métodos obsoletos ou redundantes com recursos de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="f6995-123">However, the interface does not support methods that are obsolete or redundant with UI Automation features.</span></span> <span data-ttu-id="f6995-124">Por exemplo, **IUIAutomationLegacyIAccessiblePattern** não tem um método equivalente a [**IAccessible:: accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) porque o local atual de um elemento de interface do usuário está disponível na propriedade BoundingRectangle de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="f6995-124">For example, **IUIAutomationLegacyIAccessiblePattern** does not have a method that is equivalent to [**IAccessible::accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) because the current location of a UI element is available from the UI Automation BoundingRectangle property.</span></span>

<span data-ttu-id="f6995-125">O método [**IUIAutomationLegacyIAccessiblePattern:: getiaccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationlegacyiaccessiblepattern-getiaccessible) permite que um cliente recupere um ponteiro de interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) de um elemento de automação de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="f6995-125">The [**IUIAutomationLegacyIAccessiblePattern::GetIAccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationlegacyiaccessiblepattern-getiaccessible) method enables a client to retrieve an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer from an UI Automation element.</span></span> <span data-ttu-id="f6995-126">O inverso também é possível usando os métodos [**IUIAutomation:: ElementFromIAccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromiaccessible) e [**IUIAutomation:: ElementFromIAccessibleBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromiaccessiblebuildcache) .</span><span class="sxs-lookup"><span data-stu-id="f6995-126">The reverse is also possible by using the [**IUIAutomation::ElementFromIAccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromiaccessible) and [**IUIAutomation::ElementFromIAccessibleBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromiaccessiblebuildcache) methods.</span></span>

<span data-ttu-id="f6995-127">[**IUIAutomationLegacyIAccessiblePattern:: getiaccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationlegacyiaccessiblepattern-getiaccessible) retornará **nulo** se a interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) do elemento for fornecida por um objeto proxy de OLEACC.dll ou da automação da interface do usuário para o Microsoft acessibilidade ativa Bridge.</span><span class="sxs-lookup"><span data-stu-id="f6995-127">[**IUIAutomationLegacyIAccessiblePattern::GetIAccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationlegacyiaccessiblepattern-getiaccessible) returns **NULL** if the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface for the element is provided by a proxy object from OLEACC.dll or from the UI Automation to Microsoft Active Accessibility Bridge.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f6995-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f6995-128">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="f6995-129">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="f6995-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f6995-130">Automação e Acessibilidade Ativa da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="f6995-130">UI Automation and Active Accessibility</span></span>](uiauto-msaa.md)
</dt> <dt>

[<span data-ttu-id="f6995-131">Visão Geral de Padrões de Controle de Automação de Interface de Usuário</span><span class="sxs-lookup"><span data-stu-id="f6995-131">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




