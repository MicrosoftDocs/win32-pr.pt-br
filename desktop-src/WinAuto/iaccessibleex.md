---
title: A interface IAccessibleEx
description: Controles que não têm um provedor de automação da interface do usuário da Microsoft, mas que implementam o IAccessible, podem ser facilmente atualizados para fornecer algumas funcionalidades de automação da interface do usuário implementando a interface IAccessibleEx.
ms.assetid: 5523156e-c9b8-4aad-b568-f3b3c402d33e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a74e7d464acf18244d91bc69199a56004b20beb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104084107"
---
# <a name="the-iaccessibleex-interface"></a><span data-ttu-id="2d64a-103">A interface IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="2d64a-103">The IAccessibleEx Interface</span></span>

<span data-ttu-id="2d64a-104">Controles que não têm um provedor de automação da interface do usuário da Microsoft, mas que implementam o [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), podem ser facilmente atualizados para fornecer algumas funcionalidades de automação da interface do usuário implementando a interface [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) .</span><span class="sxs-lookup"><span data-stu-id="2d64a-104">Controls that do not have a Microsoft UI Automation provider, but that implement [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), can easily be upgraded to provide some UI Automation functionality by implementing the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface.</span></span> <span data-ttu-id="2d64a-105">Essa interface permite que o controle exponha Propriedades de automação da interface do usuário e padrões de controle, sem a necessidade de uma implementação completa das interfaces do provedor de automação da interface do usuário, como [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment).</span><span class="sxs-lookup"><span data-stu-id="2d64a-105">This interface enables the control to expose UI Automation properties and control patterns, without the need for a full implementation of UI Automation provider interfaces such as [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment).</span></span> <span data-ttu-id="2d64a-106">Para usar **IAccessibleEx**, **IRawElementProviderFragment** e todas as outras interfaces de automação de interface do usuário, inclua o arquivo de cabeçalho automação da IU. h em seu código-fonte.</span><span class="sxs-lookup"><span data-stu-id="2d64a-106">To use **IAccessibleEx**, **IRawElementProviderFragment**, and all other UI Automation interfaces, include the UIAutomation.h header file in your source code.</span></span>

<span data-ttu-id="2d64a-107">Por exemplo, considere um controle personalizado que tem um valor de intervalo.</span><span class="sxs-lookup"><span data-stu-id="2d64a-107">For example, consider a custom control that has a range value.</span></span> <span data-ttu-id="2d64a-108">O Microsoft Acessibilidade Ativa Server para o controle define a função do controle e é capaz de retornar seu valor atual.</span><span class="sxs-lookup"><span data-stu-id="2d64a-108">The Microsoft Active Accessibility server for the control defines the control's role and is able to return its current value.</span></span> <span data-ttu-id="2d64a-109">No entanto, como o Microsoft Acessibilidade Ativa não define as propriedades mínima e máxima, o servidor não tem os meios para retornar os valores mínimo e máximo do controle.</span><span class="sxs-lookup"><span data-stu-id="2d64a-109">However, because Microsoft Active Accessibility does not define minimum and maximum properties, the server lacks the means to return the minimum and maximum values of the control.</span></span> <span data-ttu-id="2d64a-110">Um cliente de automação de interface do usuário é capaz de recuperar a função do controle, o valor atual e outras propriedades do Microsoft Acessibilidade Ativa, porque o núcleo de automação da interface do usuário pode obtê-los por meio do [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span><span class="sxs-lookup"><span data-stu-id="2d64a-110">A UI Automation client is able to retrieve the control's role, current value, and other Microsoft Active Accessibility properties, because the UI Automation core can obtain these through [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span></span> <span data-ttu-id="2d64a-111">No entanto, sem acesso a uma interface [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) no objeto, a automação da interface do usuário também não consegue recuperar os valores mínimo e máximo.</span><span class="sxs-lookup"><span data-stu-id="2d64a-111">However, without access to an [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) interface on the object, UI Automation is also unable to retrieve the maximum and minimum values.</span></span>

<span data-ttu-id="2d64a-112">O desenvolvedor de controle poderia fornecer um provedor de automação de interface do usuário completo para o controle, mas isso significaria duplicar grande parte da funcionalidade existente da implementação do [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) : por exemplo, navegação e propriedades comuns.</span><span class="sxs-lookup"><span data-stu-id="2d64a-112">The control developer could supply a complete UI Automation provider for the control, but this would mean duplicating much of the existing functionality of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) implementation: for example, navigation and common properties.</span></span> <span data-ttu-id="2d64a-113">Em vez disso, o desenvolvedor pode continuar a confiar no **IAccessible** para fornecer essa funcionalidade, ao mesmo tempo em que adiciona suporte para propriedades específicas de controle por meio de [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider).</span><span class="sxs-lookup"><span data-stu-id="2d64a-113">Instead, the developer can continue to rely on **IAccessible** to supply this functionality, while adding support for control-specific properties through [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2d64a-114">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="2d64a-114">In this section</span></span>

-   [<span data-ttu-id="2d64a-115">Diretrizes de implementação do IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="2d64a-115">IAccessibleEx Implementation Guidelines</span></span>](iaccessibleex-implementation-guidelines.md)
-   [<span data-ttu-id="2d64a-116">Implementando IAccessibleEx para provedores</span><span class="sxs-lookup"><span data-stu-id="2d64a-116">Implementing IAccessibleEx for Providers</span></span>](implementing-iaccessibleex-for-providers.md)
-   [<span data-ttu-id="2d64a-117">Usando o IAccessibleEx de um cliente</span><span class="sxs-lookup"><span data-stu-id="2d64a-117">Using IAccessibleEx from a Client</span></span>](using-iaccessibleex-from-a-client.md)

## <a name="related-topics"></a><span data-ttu-id="2d64a-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2d64a-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d64a-119">Infraestrutura comum</span><span class="sxs-lookup"><span data-stu-id="2d64a-119">Common Infrastructure</span></span>](common-infrastructure.md)
</dt> </dl>

 

 




