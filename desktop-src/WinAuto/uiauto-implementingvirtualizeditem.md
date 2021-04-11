---
title: Padrão de controle VirtualizedItem
description: Descreve as diretrizes e convenções para implementar o IVirtualizedItemProvider, incluindo informações sobre propriedades e métodos.
ms.assetid: 7a95e92f-7ccb-4c9b-8986-1d2de7038e47
keywords:
- Automação da interface do usuário, implementando o padrão de controle VirtualizedItem
- Automação da interface do usuário, padrão de controle VirtualizedItem
- Automação da interface do usuário, IVirtualizedItemProvider
- IVirtualizedItemProvider
- Implementando padrões de controle VirtualizedItem de automação da interface do usuário
- Padrões de controle VirtualizedItem
- padrões de controle, IVirtualizedItemProvider
- padrões de controle, implementando a automação da interface do usuário VirtualizedItem
- padrões de controle, VirtualizedItem
- interfaces, IVirtualizedItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8dac9e34dd9bff5d0ba2d245aa2fb8de621f40a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160480"
---
# <a name="virtualizeditem-control-pattern"></a><span data-ttu-id="28510-113">Padrão de controle VirtualizedItem</span><span class="sxs-lookup"><span data-stu-id="28510-113">VirtualizedItem Control Pattern</span></span>

<span data-ttu-id="28510-114">Descreve as diretrizes e convenções para implementar o [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider), incluindo informações sobre propriedades e métodos.</span><span class="sxs-lookup"><span data-stu-id="28510-114">Describes guidelines and conventions for implementing [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider), including information about properties and methods.</span></span> <span data-ttu-id="28510-115">O padrão de controle **VirtualizedItem** é usado para dar suporte a itens virtualizados, que são itens representados por elementos de automação de espaço reservado na árvore de automação da interface do usuário da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="28510-115">The **VirtualizedItem** control pattern is used to support virtualized items, which are items that are represented by placeholder automation elements in the Microsoft UI Automation tree.</span></span>

<span data-ttu-id="28510-116">Itens virtualizados podem incluir itens recuperados de um controle que dá suporte ao padrão de controle de item [contido](uiauto-implementingitemcontainer.md) ou um objeto incorporado virtualizado recuperado de um controle que dá suporte ao padrão de controle de [texto](uiauto-implementingtextandtextrange.md) .</span><span class="sxs-lookup"><span data-stu-id="28510-116">Virtualized items can include items retrieved from a control that supports the [ItemContainer](uiauto-implementingitemcontainer.md) control pattern, or a virtualized embedded object retrieved from a control that supports the [Text](uiauto-implementingtextandtextrange.md) control pattern.</span></span> <span data-ttu-id="28510-117">O espaço reservado para um item virtualizado pode não ter dados carregados para todas as propriedades de automação da interface do usuário e pode retornar [**UIA \_ E \_ ELEMENTNOTAVAILABLE**](uiauto-error-codes.md) em resposta a consultas de propriedades que não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="28510-117">The placeholder for a virtualized item might not have loaded data for all UI Automation properties, and may return [**UIA\_E\_ELEMENTNOTAVAILABLE**](uiauto-error-codes.md) in response to queries for properties that are not available.</span></span> <span data-ttu-id="28510-118">O padrão de controle **VirtualizedItem** fornece um método para concretizar um item virtual para que as informações completas sejam disponibilizadas para o item e um elemento de automação completa possa ser criado para o item na árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="28510-118">The **VirtualizedItem** control pattern provides a method for realizing a virtual item so that full information is made available for the item, and a full automation element can be created for the item in the UI Automation tree.</span></span>

<span data-ttu-id="28510-119">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="28510-119">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="28510-120">Diretrizes e convenções de implementação</span><span class="sxs-lookup"><span data-stu-id="28510-120">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="28510-121">Membros necessários para **IVirtualizedItemProvider**</span><span class="sxs-lookup"><span data-stu-id="28510-121">Required Members for **IVirtualizedItemProvider**</span></span>](#required-members-for-ivirtualizeditemprovider)
-   [<span data-ttu-id="28510-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="28510-122">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="28510-123">Diretrizes e convenções de implementação</span><span class="sxs-lookup"><span data-stu-id="28510-123">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="28510-124">Ao implementar o padrão de controle **VirtualizedItem** , observe as seguintes diretrizes e convenções:</span><span class="sxs-lookup"><span data-stu-id="28510-124">When implementing the **VirtualizedItem** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="28510-125">Qualquer elemento de espaço reservado de automação da interface do usuário que pode ser virtualizado deve dar suporte ao padrão de controle **VirtualizedItem** expondo a interface [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider) .</span><span class="sxs-lookup"><span data-stu-id="28510-125">Any UI Automation placeholder element that can be virtualized must support the **VirtualizedItem** control pattern by exposing the [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider) interface.</span></span>
-   <span data-ttu-id="28510-126">Quando [**IVirtualizedItemProvider:: perceba**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) é chamado, o objeto de espaço reservado deve ser atualizado com implementações completas de suas propriedades e padrões de controle.</span><span class="sxs-lookup"><span data-stu-id="28510-126">When [**IVirtualizedItemProvider::Realize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) is called, the placeholder object must be updated with full implementations of its properties and control patterns.</span></span>
-   <span data-ttu-id="28510-127">Quando [**IVirtualizedItemProvider:: perceba**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) é chamado, o provedor pode alterar o visor para que o item virtualizado venha a ser exibido.</span><span class="sxs-lookup"><span data-stu-id="28510-127">When [**IVirtualizedItemProvider::Realize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) is called, the provider can change the viewport so that the virtualized item comes into view.</span></span> <span data-ttu-id="28510-128">Não é necessário colocar o item na exibição; no entanto, itens fora da tela, não virtualizados, devem dar suporte ao método [**IScrollItemProvider:: ScrollIntoView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollitemprovider-scrollintoview) .</span><span class="sxs-lookup"><span data-stu-id="28510-128">Bringing the item into view is not required; however, off-screen, non-virtualized items should support the [**IScrollItemProvider::ScrollIntoView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollitemprovider-scrollintoview) method.</span></span>

## <a name="required-members-for-ivirtualizeditemprovider"></a><span data-ttu-id="28510-129">Membros necessários para **IVirtualizedItemProvider**</span><span class="sxs-lookup"><span data-stu-id="28510-129">Required Members for **IVirtualizedItemProvider**</span></span>

<span data-ttu-id="28510-130">As propriedades e os métodos a seguir são necessários para implementar a interface [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider) .</span><span class="sxs-lookup"><span data-stu-id="28510-130">The following properties and methods are required for implementing the [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider) interface.</span></span>



| <span data-ttu-id="28510-131">Membros necessários</span><span class="sxs-lookup"><span data-stu-id="28510-131">Required members</span></span>                                           | <span data-ttu-id="28510-132">Tipo de membro</span><span class="sxs-lookup"><span data-stu-id="28510-132">Member type</span></span> | <span data-ttu-id="28510-133">Observações</span><span class="sxs-lookup"><span data-stu-id="28510-133">Notes</span></span> |
|------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="28510-134">**State**</span><span class="sxs-lookup"><span data-stu-id="28510-134">**Realize**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) | <span data-ttu-id="28510-135">Método</span><span class="sxs-lookup"><span data-stu-id="28510-135">Method</span></span>      | <span data-ttu-id="28510-136">Nenhum</span><span class="sxs-lookup"><span data-stu-id="28510-136">None</span></span>  |



 

<span data-ttu-id="28510-137">Este padrão de controle não tem eventos associados.</span><span class="sxs-lookup"><span data-stu-id="28510-137">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="28510-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="28510-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28510-139">Implementando o padrão de controle do contêiner de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="28510-139">Implementing the UI Automation ItemContainer Control Pattern</span></span>](uiauto-implementingitemcontainer.md)
</dt> <dt>

[<span data-ttu-id="28510-140">Visão Geral de Padrões de Controle de Automação de Interface de Usuário</span><span class="sxs-lookup"><span data-stu-id="28510-140">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="28510-141">Visão geral da árvore de automação de interface do usuário</span><span class="sxs-lookup"><span data-stu-id="28510-141">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> <dt>

[<span data-ttu-id="28510-142">Trabalhando com itens virtualizados</span><span class="sxs-lookup"><span data-stu-id="28510-142">Working with Virtualized Items</span></span>](uiauto-workingwithvirtualizeditems.md)
</dt> </dl>

 

 




