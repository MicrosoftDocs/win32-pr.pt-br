---
title: Padrão de controle TableItem
description: Descreve as diretrizes e convenções para implementar o ITableItemProvider, incluindo informações sobre métodos. O padrão de controle TableItem é usado para dar suporte a controles filho de contêineres que implementam ITableProvider.
ms.assetid: e00c7a58-410c-4818-8f61-57ee98527d6e
keywords:
- Automação da interface do usuário, implementando o padrão de controle TableItem
- Automação da interface do usuário, padrão de controle TableItem
- Automação da interface do usuário, ITableItemProvider
- ITableItemProvider
- Implementando padrões de controle TableItem de automação da interface do usuário
- Padrões de controle TableItem
- padrões de controle, ITableItemProvider
- padrões de controle, implementando a automação da interface do usuário TableItem
- padrões de controle, TableItem
- interfaces, ITableItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bae3e6d5379ec9a662e31ec6181476b112631381
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635494"
---
# <a name="tableitem-control-pattern"></a><span data-ttu-id="2b59e-114">Padrão de controle TableItem</span><span class="sxs-lookup"><span data-stu-id="2b59e-114">TableItem Control Pattern</span></span>

<span data-ttu-id="2b59e-115">Descreve as diretrizes e convenções para implementar o [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider), incluindo informações sobre métodos.</span><span class="sxs-lookup"><span data-stu-id="2b59e-115">Describes guidelines and conventions for implementing [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider), including information about methods.</span></span> <span data-ttu-id="2b59e-116">O padrão de controle **TableItem** é usado para dar suporte a controles filho de contêineres que implementam [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider).</span><span class="sxs-lookup"><span data-stu-id="2b59e-116">The **TableItem** control pattern is used to support child controls of containers that implement [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider).</span></span>

<span data-ttu-id="2b59e-117">O acesso à funcionalidade de célula individual é fornecido pela implementação simultânea e necessária do [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider).</span><span class="sxs-lookup"><span data-stu-id="2b59e-117">Access to individual cell functionality is provided by the required, concurrent implementation of [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider).</span></span> <span data-ttu-id="2b59e-118">Esse padrão de controle é análogo a **IGridItemProvider** com a distinção de que qualquer controle que implementa [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) deve expor de forma programática a relação entre a célula individual e suas informações de linha e coluna.</span><span class="sxs-lookup"><span data-stu-id="2b59e-118">This control pattern is analogous to **IGridItemProvider** with the distinction that any control implementing [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) must programmatically expose the relationship between the individual cell and its row and column information.</span></span> <span data-ttu-id="2b59e-119">Para obter exemplos de controles que implementam esse padrão de controle, consulte [tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="2b59e-119">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="2b59e-120">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="2b59e-120">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="2b59e-121">Diretrizes e convenções de implementação</span><span class="sxs-lookup"><span data-stu-id="2b59e-121">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="2b59e-122">Membros necessários para **ITableItemProvider**</span><span class="sxs-lookup"><span data-stu-id="2b59e-122">Required Members for **ITableItemProvider**</span></span>](#required-members-for-itableitemprovider)
-   [<span data-ttu-id="2b59e-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2b59e-123">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="2b59e-124">Diretrizes e convenções de implementação</span><span class="sxs-lookup"><span data-stu-id="2b59e-124">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="2b59e-125">Ao implementar o padrão de controle **TableItem** , observe as seguintes diretrizes e convenções:</span><span class="sxs-lookup"><span data-stu-id="2b59e-125">When implementing the **TableItem** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="2b59e-126">Para obter a funcionalidade de item de grade relacionada, consulte [padrão de controle GridItem](uiauto-implementinggriditem.md).</span><span class="sxs-lookup"><span data-stu-id="2b59e-126">For related grid item functionality, see [GridItem Control Pattern](uiauto-implementinggriditem.md).</span></span>

## <a name="required-members-for-itableitemprovider"></a><span data-ttu-id="2b59e-127">Membros necessários para **ITableItemProvider**</span><span class="sxs-lookup"><span data-stu-id="2b59e-127">Required Members for **ITableItemProvider**</span></span>

<span data-ttu-id="2b59e-128">Os métodos a seguir são necessários para implementar a interface [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) .</span><span class="sxs-lookup"><span data-stu-id="2b59e-128">The following methods are required for implementing the [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) interface.</span></span>



| <span data-ttu-id="2b59e-129">Membros necessários</span><span class="sxs-lookup"><span data-stu-id="2b59e-129">Required members</span></span>                                                               | <span data-ttu-id="2b59e-130">Tipo de membro</span><span class="sxs-lookup"><span data-stu-id="2b59e-130">Member type</span></span> | <span data-ttu-id="2b59e-131">Observações</span><span class="sxs-lookup"><span data-stu-id="2b59e-131">Notes</span></span> |
|--------------------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="2b59e-132">**GetColumnHeaderItems**</span><span class="sxs-lookup"><span data-stu-id="2b59e-132">**GetColumnHeaderItems**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableitemprovider-getcolumnheaderitems) | <span data-ttu-id="2b59e-133">Método</span><span class="sxs-lookup"><span data-stu-id="2b59e-133">Method</span></span>      | <span data-ttu-id="2b59e-134">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="2b59e-134">None</span></span>  |
| [<span data-ttu-id="2b59e-135">**GetRowHeaderItems**</span><span class="sxs-lookup"><span data-stu-id="2b59e-135">**GetRowHeaderItems**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableitemprovider-getrowheaderitems)       | <span data-ttu-id="2b59e-136">Método</span><span class="sxs-lookup"><span data-stu-id="2b59e-136">Method</span></span>      | <span data-ttu-id="2b59e-137">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="2b59e-137">None</span></span>  |



 

<span data-ttu-id="2b59e-138">Este padrão de controle não tem propriedades ou eventos associados.</span><span class="sxs-lookup"><span data-stu-id="2b59e-138">This control pattern has no associated properties or events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2b59e-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2b59e-139">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="2b59e-140">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="2b59e-140">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2b59e-141">Tipos de controle e seus padrões de controle com suporte</span><span class="sxs-lookup"><span data-stu-id="2b59e-141">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="2b59e-142">Padrão de controle de tabela</span><span class="sxs-lookup"><span data-stu-id="2b59e-142">Table Control Pattern</span></span>](uiauto-implementingtable.md)
</dt> <dt>

[<span data-ttu-id="2b59e-143">Visão Geral de Padrões de Controle de Automação de Interface de Usuário</span><span class="sxs-lookup"><span data-stu-id="2b59e-143">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="2b59e-144">Visão geral da árvore de automação de interface do usuário</span><span class="sxs-lookup"><span data-stu-id="2b59e-144">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




