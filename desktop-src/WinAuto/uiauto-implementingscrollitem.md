---
title: Padrão de controle ScrollItem
description: Descreve as diretrizes e convenções para implementar o IScrollItemProvider, incluindo informações sobre métodos.
ms.assetid: ea0d7438-218c-4925-b24c-a8011f305b9d
keywords:
- Automação da interface do usuário, implementando o padrão de controle ScrollItem
- Automação da interface do usuário, padrão de controle ScrollItem
- Automação da interface do usuário, IScrollItemProvider
- IScrollItemProvider
- Implementando padrões de controle ScrollItem de automação da interface do usuário
- Padrões de controle ScrollItem
- padrões de controle, IScrollItemProvider
- padrões de controle, implementando a automação da interface do usuário ScrollItem
- padrões de controle, ScrollItem
- interfaces, IScrollItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7233dfe649d166a3172ff2dda3122895f259abcc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159951"
---
# <a name="scrollitem-control-pattern"></a><span data-ttu-id="d1cd5-113">Padrão de controle ScrollItem</span><span class="sxs-lookup"><span data-stu-id="d1cd5-113">ScrollItem Control Pattern</span></span>

<span data-ttu-id="d1cd5-114">Descreve as diretrizes e convenções para implementar o [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider), incluindo informações sobre métodos.</span><span class="sxs-lookup"><span data-stu-id="d1cd5-114">Describes guidelines and conventions for implementing [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider), including information about methods.</span></span> <span data-ttu-id="d1cd5-115">O padrão de controle **ScrollItem** é usado para dar suporte a controles filho individuais de contêineres que implementam [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider).</span><span class="sxs-lookup"><span data-stu-id="d1cd5-115">The **ScrollItem** control pattern is used to support individual child controls of containers that implement [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider).</span></span> <span data-ttu-id="d1cd5-116">A existência do padrão de controle **ScrollItem** em um controle não significa que seu contêiner ou qualquer ancestral deve implementar o padrão de controle **Scroll** .</span><span class="sxs-lookup"><span data-stu-id="d1cd5-116">The existence of the **ScrollItem** control pattern on a control does not imply that its container or any ancestor must implement the **Scroll** control pattern.</span></span>

<span data-ttu-id="d1cd5-117">Quando o contêiner implementa o padrão de controle **Scroll** , o padrão de controle **ScrollItem** atua como um canal de comunicação entre um controle filho e seu contêiner para garantir que o contêiner possa alterar o conteúdo visível no momento (ou região) dentro de seu visor para exibir o controle filho.</span><span class="sxs-lookup"><span data-stu-id="d1cd5-117">When the container does implement the **Scroll** control pattern, the **ScrollItem** control pattern acts as a communication channel between a child control and its container to ensure that the container can change the currently visible content (or region) within its viewport to display the child control.</span></span> <span data-ttu-id="d1cd5-118">Para obter exemplos de controles que implementam esse padrão de controle, consulte [tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="d1cd5-118">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="d1cd5-119">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="d1cd5-119">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="d1cd5-120">Diretrizes e convenções de implementação</span><span class="sxs-lookup"><span data-stu-id="d1cd5-120">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="d1cd5-121">Membros necessários para **IScrollItemProvider**</span><span class="sxs-lookup"><span data-stu-id="d1cd5-121">Required Members for **IScrollItemProvider**</span></span>](#required-members-for-iscrollitemprovider)
-   [<span data-ttu-id="d1cd5-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d1cd5-122">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="d1cd5-123">Diretrizes e convenções de implementação</span><span class="sxs-lookup"><span data-stu-id="d1cd5-123">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="d1cd5-124">Ao implementar o padrão de controle **ScrollItem** , observe as seguintes diretrizes e convenções:</span><span class="sxs-lookup"><span data-stu-id="d1cd5-124">When implementing the **ScrollItem** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="d1cd5-125">Os itens contidos em um controle de [janela](uiauto-supportwindowcontroltype.md) ou **Canvas** não são necessários para implementar a interface [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider) .</span><span class="sxs-lookup"><span data-stu-id="d1cd5-125">Items contained within a [Window](uiauto-supportwindowcontroltype.md) or **Canvas** control are not required to implement the [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider) interface.</span></span> <span data-ttu-id="d1cd5-126">No entanto, como alternativa, eles devem expor um local válido para a propriedade [**IUIAutomationElement:: CurrentBoundingRectangle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentboundingrectangle) (ou [**CachedBoundingRectangle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedboundingrectangle)).</span><span class="sxs-lookup"><span data-stu-id="d1cd5-126">As an alternative, however, they must expose a valid location for the [**IUIAutomationElement::CurrentBoundingRectangle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentboundingrectangle) (or [**CachedBoundingRectangle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedboundingrectangle)) property.</span></span> <span data-ttu-id="d1cd5-127">Isso permitirá que um aplicativo cliente de automação da interface do usuário da Microsoft use os métodos de padrão de controle [**IUIAutomationScrollPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationscrollpattern) no contêiner para exibir o item filho.</span><span class="sxs-lookup"><span data-stu-id="d1cd5-127">This will allow a Microsoft UI Automation client application to use the [**IUIAutomationScrollPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationscrollpattern) control pattern methods on the container to display the child item.</span></span>

## <a name="required-members-for-iscrollitemprovider"></a><span data-ttu-id="d1cd5-128">Membros necessários para **IScrollItemProvider**</span><span class="sxs-lookup"><span data-stu-id="d1cd5-128">Required Members for **IScrollItemProvider**</span></span>

<span data-ttu-id="d1cd5-129">O método a seguir é necessário para implementar a interface [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider) .</span><span class="sxs-lookup"><span data-stu-id="d1cd5-129">The following method is required for implementing the [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider) interface.</span></span>



| <span data-ttu-id="d1cd5-130">Membros necessários</span><span class="sxs-lookup"><span data-stu-id="d1cd5-130">Required members</span></span>                                                    | <span data-ttu-id="d1cd5-131">Tipo de membro</span><span class="sxs-lookup"><span data-stu-id="d1cd5-131">Member type</span></span> | <span data-ttu-id="d1cd5-132">Observações</span><span class="sxs-lookup"><span data-stu-id="d1cd5-132">Notes</span></span> |
|---------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="d1cd5-133">**ScrollIntoView**</span><span class="sxs-lookup"><span data-stu-id="d1cd5-133">**ScrollIntoView**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollitemprovider-scrollintoview) | <span data-ttu-id="d1cd5-134">Método</span><span class="sxs-lookup"><span data-stu-id="d1cd5-134">Method</span></span>      | <span data-ttu-id="d1cd5-135">Nenhum</span><span class="sxs-lookup"><span data-stu-id="d1cd5-135">None</span></span>  |



 

<span data-ttu-id="d1cd5-136">Este padrão de controle não tem propriedades ou eventos associados.</span><span class="sxs-lookup"><span data-stu-id="d1cd5-136">This control pattern has no associated properties or events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d1cd5-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d1cd5-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1cd5-138">Tipos de controle e seus padrões de controle com suporte</span><span class="sxs-lookup"><span data-stu-id="d1cd5-138">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="d1cd5-139">Padrão de controle de seleção</span><span class="sxs-lookup"><span data-stu-id="d1cd5-139">Selection Control Pattern</span></span>](uiauto-implementingselection.md)
</dt> <dt>

[<span data-ttu-id="d1cd5-140">Visão Geral de Padrões de Controle de Automação de Interface de Usuário</span><span class="sxs-lookup"><span data-stu-id="d1cd5-140">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="d1cd5-141">Visão geral da árvore de automação de interface do usuário</span><span class="sxs-lookup"><span data-stu-id="d1cd5-141">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




