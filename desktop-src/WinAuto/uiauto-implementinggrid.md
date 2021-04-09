---
title: Padrão de controle de grade
description: Descreve as diretrizes e convenções para implementar o IGridProvider, incluindo informações sobre propriedades e métodos. O padrão de controle de grade é usado para dar suporte a controles que atuam como contêineres para uma coleção de elementos filho.
ms.assetid: c50fb6f7-884a-4147-a6b2-c59d787fc04b
keywords:
- Automação da interface do usuário, implementando o padrão de controle de grade
- Automação da interface do usuário, padrão de controle de grade
- Automação da interface do usuário, IGridProvider
- IGridProvider
- Implementando padrões de controle de grade de automação da IU
- Padrões de controle de grade
- padrões de controle, IGridProvider
- padrões de controle, implementação da grade de automação da interface do usuário
- padrões de controle, grade
- interfaces, IGridProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 328d8536a367389a6d17422bd6f6476a3e82aa11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005281"
---
# <a name="grid-control-pattern"></a><span data-ttu-id="1c9e5-114">Padrão de controle de grade</span><span class="sxs-lookup"><span data-stu-id="1c9e5-114">Grid Control Pattern</span></span>

<span data-ttu-id="1c9e5-115">Descreve as diretrizes e convenções para implementar o [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider), incluindo informações sobre propriedades e métodos.</span><span class="sxs-lookup"><span data-stu-id="1c9e5-115">Describes guidelines and conventions for implementing [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider), including information about properties and methods.</span></span> <span data-ttu-id="1c9e5-116">O padrão de controle de **grade** é usado para dar suporte a controles que atuam como contêineres para uma coleção de elementos filho.</span><span class="sxs-lookup"><span data-stu-id="1c9e5-116">The **Grid** control pattern is used to support controls that act as containers for a collection of child elements.</span></span>

<span data-ttu-id="1c9e5-117">Os filhos deste elemento devem implementar [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider) e ser organizados em um sistema de coordenadas lógico bidimensional que possa ser atravessado por linha e coluna.</span><span class="sxs-lookup"><span data-stu-id="1c9e5-117">The children of this element must implement [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider) and be organized in a two-dimensional logical coordinate system that can be traversed by row and column.</span></span> <span data-ttu-id="1c9e5-118">Para obter exemplos de controles que implementam esse padrão de controle, consulte [tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="1c9e5-118">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="1c9e5-119">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="1c9e5-119">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="1c9e5-120">Diretrizes e convenções de implementação</span><span class="sxs-lookup"><span data-stu-id="1c9e5-120">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="1c9e5-121">Membros necessários para **IGridProvider**</span><span class="sxs-lookup"><span data-stu-id="1c9e5-121">Required Members for **IGridProvider**</span></span>](#required-members-for-igridprovider)
-   [<span data-ttu-id="1c9e5-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1c9e5-122">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="1c9e5-123">Diretrizes e convenções de implementação</span><span class="sxs-lookup"><span data-stu-id="1c9e5-123">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="1c9e5-124">Ao implementar o padrão de controle de **grade** , observe as seguintes diretrizes e convenções:</span><span class="sxs-lookup"><span data-stu-id="1c9e5-124">When implementing the **Grid** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="1c9e5-125">As coordenadas de grade são baseadas em zero com o canto superior esquerdo (ou célula superior direita, dependendo da localidade) com coordenadas (0, 0).</span><span class="sxs-lookup"><span data-stu-id="1c9e5-125">Grid coordinates are zero-based with the upper left (or upper right cell depending on locale) having coordinates (0,0).</span></span>
-   <span data-ttu-id="1c9e5-126">Se uma célula estiver vazia, um elemento de automação da interface do usuário da Microsoft ainda deverá ser retornado para dar suporte à propriedade [**IGridItemProvider:: ContainingGrid**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_containinggrid) dessa célula.</span><span class="sxs-lookup"><span data-stu-id="1c9e5-126">If a cell is empty, a Microsoft UI Automation element must still be returned in order to support the [**IGridItemProvider::ContainingGrid**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_containinggrid) property for that cell.</span></span> <span data-ttu-id="1c9e5-127">Isso é possível quando o layout dos elementos filho na grade é semelhante a uma matriz irregular (Veja o exemplo abaixo).</span><span class="sxs-lookup"><span data-stu-id="1c9e5-127">This is possible when the layout of child elements in the grid is similar to a ragged array (see example below).</span></span>

    ![exemplo de um controle de grade com coordenadas vazias](images/grid.png)

-   <span data-ttu-id="1c9e5-129">Uma grade com um único item ainda é necessária para implementar [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) se for considerada logicamente como uma grade.</span><span class="sxs-lookup"><span data-stu-id="1c9e5-129">A grid with a single item is still required to implement [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) if it is logically considered to be a grid.</span></span> <span data-ttu-id="1c9e5-130">O número de itens filho na grade é irrelevante.</span><span class="sxs-lookup"><span data-stu-id="1c9e5-130">The number of child items in the grid is immaterial.</span></span>
-   <span data-ttu-id="1c9e5-131">Linhas e colunas ocultas, dependendo da implementação do provedor, podem ser carregadas na árvore de automação da interface do usuário e, portanto, serão refletidas nas propriedades [**IGridProvider:: RowCount**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_rowcount) e [**ColumnCount**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_columncount) .</span><span class="sxs-lookup"><span data-stu-id="1c9e5-131">Hidden rows and columns, depending on the provider implementation, may be loaded in the UI Automation tree and will therefore be reflected in the [**IGridProvider::RowCount**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_rowcount) and [**ColumnCount**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_columncount) properties.</span></span> <span data-ttu-id="1c9e5-132">Se as linhas e colunas ocultas ainda não tiverem sido carregadas, elas não deverão ser contadas.</span><span class="sxs-lookup"><span data-stu-id="1c9e5-132">If the hidden rows and columns have not yet been loaded, they should not be counted.</span></span>
-   <span data-ttu-id="1c9e5-133">[**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) não habilita a manipulação ativa de uma grade; [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) deve ser implementado para habilitar essa funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="1c9e5-133">[**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) does not enable active manipulation of a grid; [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) must be implemented to enable this functionality.</span></span>
-   <span data-ttu-id="1c9e5-134">Use um [**IUIAutomationStructureChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationstructurechangedeventhandler) para escutar alterações estruturais ou de layout na grade, como células que foram adicionadas, removidas ou mescladas.</span><span class="sxs-lookup"><span data-stu-id="1c9e5-134">Use a [**IUIAutomationStructureChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationstructurechangedeventhandler) to listen for structural or layout changes to the grid such as cells that have been added, removed, or merged.</span></span>
-   <span data-ttu-id="1c9e5-135">Use um [**IUIAutomationFocusChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationfocuschangedeventhandler) para acompanhar a passagem pelos itens ou células de uma grade.</span><span class="sxs-lookup"><span data-stu-id="1c9e5-135">Use a [**IUIAutomationFocusChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationfocuschangedeventhandler) to track traversal through the items or cells of a grid.</span></span>

## <a name="required-members-for-igridprovider"></a><span data-ttu-id="1c9e5-136">Membros necessários para **IGridProvider**</span><span class="sxs-lookup"><span data-stu-id="1c9e5-136">Required Members for **IGridProvider**</span></span>

<span data-ttu-id="1c9e5-137">As propriedades e os métodos a seguir são necessários para implementar a interface [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) .</span><span class="sxs-lookup"><span data-stu-id="1c9e5-137">The following properties and methods are required for implementing the [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) interface.</span></span>



| <span data-ttu-id="1c9e5-138">Membros necessários</span><span class="sxs-lookup"><span data-stu-id="1c9e5-138">Required members</span></span>                                        | <span data-ttu-id="1c9e5-139">Tipo de membro</span><span class="sxs-lookup"><span data-stu-id="1c9e5-139">Member type</span></span> | <span data-ttu-id="1c9e5-140">Observações</span><span class="sxs-lookup"><span data-stu-id="1c9e5-140">Notes</span></span> |
|---------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="1c9e5-141">**Linhas**</span><span class="sxs-lookup"><span data-stu-id="1c9e5-141">**RowCount**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_rowcount)       | <span data-ttu-id="1c9e5-142">Propriedade</span><span class="sxs-lookup"><span data-stu-id="1c9e5-142">Property</span></span>    | <span data-ttu-id="1c9e5-143">Nenhum</span><span class="sxs-lookup"><span data-stu-id="1c9e5-143">None</span></span>  |
| [<span data-ttu-id="1c9e5-144">**ColumnCount**</span><span class="sxs-lookup"><span data-stu-id="1c9e5-144">**ColumnCount**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_columncount) | <span data-ttu-id="1c9e5-145">Propriedade</span><span class="sxs-lookup"><span data-stu-id="1c9e5-145">Property</span></span>    | <span data-ttu-id="1c9e5-146">Nenhum</span><span class="sxs-lookup"><span data-stu-id="1c9e5-146">None</span></span>  |
| [<span data-ttu-id="1c9e5-147">**GetItem**</span><span class="sxs-lookup"><span data-stu-id="1c9e5-147">**GetItem**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-getitem)         | <span data-ttu-id="1c9e5-148">Método</span><span class="sxs-lookup"><span data-stu-id="1c9e5-148">Method</span></span>      | <span data-ttu-id="1c9e5-149">Nenhum</span><span class="sxs-lookup"><span data-stu-id="1c9e5-149">None</span></span>  |



 

<span data-ttu-id="1c9e5-150">Este padrão de controle não tem eventos associados.</span><span class="sxs-lookup"><span data-stu-id="1c9e5-150">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1c9e5-151">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1c9e5-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c9e5-152">Tipos de controle e seus padrões de controle com suporte</span><span class="sxs-lookup"><span data-stu-id="1c9e5-152">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="1c9e5-153">Padrão de controle GridItem</span><span class="sxs-lookup"><span data-stu-id="1c9e5-153">GridItem Control Pattern</span></span>](uiauto-implementinggriditem.md)
</dt> <dt>

[<span data-ttu-id="1c9e5-154">Visão Geral de Padrões de Controle de Automação de Interface de Usuário</span><span class="sxs-lookup"><span data-stu-id="1c9e5-154">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="1c9e5-155">Visão geral da árvore de automação de interface do usuário</span><span class="sxs-lookup"><span data-stu-id="1c9e5-155">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




