---
title: Padrão de controle GridItem
description: Descreve as diretrizes e convenções para implementar o IGridItemProvider, incluindo informações sobre propriedades. O padrão de controle GridItem é usado para dar suporte a controles filho individuais de contêineres que implementam IGridProvider.
ms.assetid: ae4b9021-1800-485b-99a2-54ddf9c21f93
keywords:
- Automação da interface do usuário, implementando o padrão de controle GridItem
- Automação da interface do usuário, padrão de controle GridItem
- Automação da interface do usuário, IGridItemProvider
- IGridItemProvider
- Implementando padrões de controle GridItem de automação da interface do usuário
- Padrões de controle de GridItem
- padrões de controle, IGridItemProvider
- padrões de controle, implementando o GridItem de automação da interface do usuário
- padrões de controle, GridItem
- interfaces, IGridItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ef45b5f655e3ef09350c508271233de49f964a4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635633"
---
# <a name="griditem-control-pattern"></a><span data-ttu-id="9f40c-114">Padrão de controle GridItem</span><span class="sxs-lookup"><span data-stu-id="9f40c-114">GridItem Control Pattern</span></span>

<span data-ttu-id="9f40c-115">Descreve as diretrizes e convenções para implementar o [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider), incluindo informações sobre propriedades.</span><span class="sxs-lookup"><span data-stu-id="9f40c-115">Describes guidelines and conventions for implementing [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider), including information about properties.</span></span> <span data-ttu-id="9f40c-116">O padrão de controle **GridItem** é usado para dar suporte a controles filho individuais de contêineres que implementam [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider).</span><span class="sxs-lookup"><span data-stu-id="9f40c-116">The **GridItem** control pattern is used to support individual child controls of containers that implement [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider).</span></span>

<span data-ttu-id="9f40c-117">Para obter exemplos de controles que implementam esse padrão de controle, consulte [tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="9f40c-117">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="9f40c-118">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="9f40c-118">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="9f40c-119">Diretrizes e convenções de implementação</span><span class="sxs-lookup"><span data-stu-id="9f40c-119">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="9f40c-120">Membros necessários para **IGridItemProvider**</span><span class="sxs-lookup"><span data-stu-id="9f40c-120">Required Members for **IGridItemProvider**</span></span>](#required-members-for-igriditemprovider)
-   [<span data-ttu-id="9f40c-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9f40c-121">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="9f40c-122">Diretrizes e convenções de implementação</span><span class="sxs-lookup"><span data-stu-id="9f40c-122">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="9f40c-123">Ao implementar o padrão de controle **GridItem** , observe as seguintes diretrizes e convenções:</span><span class="sxs-lookup"><span data-stu-id="9f40c-123">When implementing the **GridItem** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="9f40c-124">As coordenadas de grade são baseadas em zero com a célula superior esquerda com coordenadas (0, 0).</span><span class="sxs-lookup"><span data-stu-id="9f40c-124">Grid coordinates are zero-based with the upper left cell having coordinates (0, 0).</span></span>
-   <span data-ttu-id="9f40c-125">As células mescladas relatarão suas propriedades de [**linha**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_row) e [**coluna**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_column) com base em sua célula de âncora subjacente, conforme definido pelo provedor de automação de interface do usuário da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9f40c-125">Merged cells will report their [**Row**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_row) and [**Column**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_column) properties based on their underlying anchor cell as defined by the Microsoft UI Automation provider.</span></span> <span data-ttu-id="9f40c-126">Normalmente, será a linha ou coluna mais alta e mais à esquerda.</span><span class="sxs-lookup"><span data-stu-id="9f40c-126">Typically, it will be the topmost and leftmost row or column.</span></span>
-   <span data-ttu-id="9f40c-127">O [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) não fornece manipulação ativa da grade, como mesclagem ou divisão de células.</span><span class="sxs-lookup"><span data-stu-id="9f40c-127">[**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) does not provide for active manipulation of the grid such as merging or splitting cells.</span></span>
-   <span data-ttu-id="9f40c-128">Controles que implementam [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) normalmente podem ser percorridos (ou seja, um cliente de automação de interface do usuário pode mover para controles adjacentes) usando o teclado.</span><span class="sxs-lookup"><span data-stu-id="9f40c-128">Controls that implement [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) can typically be traversed (that is, a UI Automation client can move to adjacent controls) by using the keyboard.</span></span>

## <a name="required-members-for-igriditemprovider"></a><span data-ttu-id="9f40c-129">Membros necessários para **IGridItemProvider**</span><span class="sxs-lookup"><span data-stu-id="9f40c-129">Required Members for **IGridItemProvider**</span></span>

<span data-ttu-id="9f40c-130">As propriedades a seguir são necessárias para implementar a interface [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider) .</span><span class="sxs-lookup"><span data-stu-id="9f40c-130">The following properties are required for implementing the [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider) interface.</span></span>



| <span data-ttu-id="9f40c-131">Membros necessários</span><span class="sxs-lookup"><span data-stu-id="9f40c-131">Required members</span></span>                                                  | <span data-ttu-id="9f40c-132">Tipo de membro</span><span class="sxs-lookup"><span data-stu-id="9f40c-132">Member type</span></span> | <span data-ttu-id="9f40c-133">Observações</span><span class="sxs-lookup"><span data-stu-id="9f40c-133">Notes</span></span> |
|-------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="9f40c-134">**Fila**</span><span class="sxs-lookup"><span data-stu-id="9f40c-134">**Row**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_row)                       | <span data-ttu-id="9f40c-135">Propriedade</span><span class="sxs-lookup"><span data-stu-id="9f40c-135">Property</span></span>    | <span data-ttu-id="9f40c-136">Nenhum</span><span class="sxs-lookup"><span data-stu-id="9f40c-136">None</span></span>  |
| [<span data-ttu-id="9f40c-137">**Pilha**</span><span class="sxs-lookup"><span data-stu-id="9f40c-137">**Column**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_column)                 | <span data-ttu-id="9f40c-138">Propriedade</span><span class="sxs-lookup"><span data-stu-id="9f40c-138">Property</span></span>    | <span data-ttu-id="9f40c-139">Nenhum</span><span class="sxs-lookup"><span data-stu-id="9f40c-139">None</span></span>  |
| [<span data-ttu-id="9f40c-140">**RowSpan**</span><span class="sxs-lookup"><span data-stu-id="9f40c-140">**RowSpan**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_rowspan)               | <span data-ttu-id="9f40c-141">Propriedade</span><span class="sxs-lookup"><span data-stu-id="9f40c-141">Property</span></span>    | <span data-ttu-id="9f40c-142">Nenhum</span><span class="sxs-lookup"><span data-stu-id="9f40c-142">None</span></span>  |
| [<span data-ttu-id="9f40c-143">**ColumnSpan**</span><span class="sxs-lookup"><span data-stu-id="9f40c-143">**ColumnSpan**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_columnspan)         | <span data-ttu-id="9f40c-144">Propriedade</span><span class="sxs-lookup"><span data-stu-id="9f40c-144">Property</span></span>    | <span data-ttu-id="9f40c-145">Nenhum</span><span class="sxs-lookup"><span data-stu-id="9f40c-145">None</span></span>  |
| [<span data-ttu-id="9f40c-146">**ContainingGrid**</span><span class="sxs-lookup"><span data-stu-id="9f40c-146">**ContainingGrid**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_containinggrid) | <span data-ttu-id="9f40c-147">Propriedade</span><span class="sxs-lookup"><span data-stu-id="9f40c-147">Property</span></span>    | <span data-ttu-id="9f40c-148">Nenhum</span><span class="sxs-lookup"><span data-stu-id="9f40c-148">None</span></span>  |



 

<span data-ttu-id="9f40c-149">Este padrão de controle não tem nenhum método ou evento associado.</span><span class="sxs-lookup"><span data-stu-id="9f40c-149">This control pattern has no associated methods or events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9f40c-150">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9f40c-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f40c-151">Tipos de controle e seus padrões de controle com suporte</span><span class="sxs-lookup"><span data-stu-id="9f40c-151">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="9f40c-152">Padrão de controle de grade</span><span class="sxs-lookup"><span data-stu-id="9f40c-152">Grid Control Pattern</span></span>](uiauto-implementinggrid.md)
</dt> <dt>

[<span data-ttu-id="9f40c-153">Visão Geral de Padrões de Controle de Automação de Interface de Usuário</span><span class="sxs-lookup"><span data-stu-id="9f40c-153">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="9f40c-154">Visão geral da árvore de automação de interface do usuário</span><span class="sxs-lookup"><span data-stu-id="9f40c-154">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




