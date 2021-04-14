---
title: Padrão de controle de tabela
description: Descreve as diretrizes e convenções para implementar o ITableProvider, incluindo informações sobre propriedades e métodos. O padrão de controle Table é usado para dar suporte a controles que atuam como contêineres para uma coleção de elementos filho.
ms.assetid: 81a1a316-cdd6-4490-8de2-1b6db52d84e6
keywords:
- Automação da interface do usuário, implementando o padrão de controle de tabela
- Automação da interface do usuário, padrão de controle de tabela
- Automação da interface do usuário, ITableProvider
- ITableProvider
- Implementando padrões de controle de tabela de automação de IU
- Padrões de controle de tabela
- padrões de controle, ITableProvider
- padrões de controle, implementação da tabela de automação da interface do usuário
- padrões de controle, tabela
- interfaces, ITableProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9879d1589985df0257a1dd7805f474c013b93732
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104555634"
---
# <a name="table-control-pattern"></a><span data-ttu-id="9bafc-114">Padrão de controle de tabela</span><span class="sxs-lookup"><span data-stu-id="9bafc-114">Table Control Pattern</span></span>

<span data-ttu-id="9bafc-115">Descreve as diretrizes e convenções para implementar o [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider), incluindo informações sobre propriedades e métodos.</span><span class="sxs-lookup"><span data-stu-id="9bafc-115">Describes guidelines and conventions for implementing [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider), including information about properties and methods.</span></span> <span data-ttu-id="9bafc-116">O padrão de controle **Table** é usado para dar suporte a controles que atuam como contêineres para uma coleção de elementos filho.</span><span class="sxs-lookup"><span data-stu-id="9bafc-116">The **Table** control pattern is used to support controls that act as containers for a collection of child elements.</span></span>

<span data-ttu-id="9bafc-117">Os filhos do elemento container devem implementar [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) e ser organizados em um sistema de coordenadas lógico bidimensional que possa ser percorrido por linha e coluna.</span><span class="sxs-lookup"><span data-stu-id="9bafc-117">The children of the container element must implement [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) and be organized in a two-dimensional logical coordinate system that can be traversed by row and column.</span></span> <span data-ttu-id="9bafc-118">Esse padrão de controle é análogo a [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) com a distinção de que qualquer controle que implementa [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider) também deve expor uma relação de cabeçalho de coluna e/ou linha para cada elemento filho.</span><span class="sxs-lookup"><span data-stu-id="9bafc-118">This control pattern is analogous to [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) with the distinction that any control implementing [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider) must also expose a column and/or row header relationship for each child element.</span></span> <span data-ttu-id="9bafc-119">Para obter exemplos de controles que implementam esse padrão de controle, consulte [tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="9bafc-119">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="9bafc-120">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="9bafc-120">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="9bafc-121">Diretrizes e convenções de implementação</span><span class="sxs-lookup"><span data-stu-id="9bafc-121">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="9bafc-122">Membros necessários para **ITableProvider**</span><span class="sxs-lookup"><span data-stu-id="9bafc-122">Required Members for **ITableProvider**</span></span>](#required-members-for-itableprovider)
-   [<span data-ttu-id="9bafc-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9bafc-123">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="9bafc-124">Diretrizes e convenções de implementação</span><span class="sxs-lookup"><span data-stu-id="9bafc-124">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="9bafc-125">Ao implementar o padrão de controle de **tabela** , observe as seguintes diretrizes e convenções:</span><span class="sxs-lookup"><span data-stu-id="9bafc-125">When implementing the **Table** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="9bafc-126">O acesso ao conteúdo de células individuais é por meio de um sistema de coordenadas lógica bidimensional ou uma matriz fornecida pela implementação de [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)necessária e simultânea.</span><span class="sxs-lookup"><span data-stu-id="9bafc-126">Access to the content of individual cells is through a two-dimensional logical coordinate system or array provided by the required, concurrent implementation of [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider).</span></span>
-   <span data-ttu-id="9bafc-127">Um cabeçalho de coluna ou de linha pode estar contido em um objeto de tabela ou ser um objeto de cabeçalho separado que está associado a um objeto de tabela.</span><span class="sxs-lookup"><span data-stu-id="9bafc-127">A column or row header can be contained within a table object or be a separate header object that is associated with a table object.</span></span>
-   <span data-ttu-id="9bafc-128">Cabeçalhos de coluna e linha podem incluir um cabeçalho principal, bem como quaisquer cabeçalhos de suporte.</span><span class="sxs-lookup"><span data-stu-id="9bafc-128">Column and row headers may include both a primary header as well as any supporting headers.</span></span>
    > [!Note]  
    > <span data-ttu-id="9bafc-129">Esse conceito se torna evidente em uma planilha do Microsoft Excel em que um usuário definiu uma coluna de **nome** .</span><span class="sxs-lookup"><span data-stu-id="9bafc-129">This concept becomes evident in a Microsoft Excel spreadsheet where a user has defined a **First name** column.</span></span> <span data-ttu-id="9bafc-130">Agora, esta coluna tem dois cabeçalhos, incluindo o primeiro cabeçalho de **nome** definido pelo usuário e a designação alfanumérica para aquela coluna atribuída pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9bafc-130">This column now has two headers, including the **First name** header defined by the user, and the alphanumeric designation for that column assigned by the application.</span></span>

     

-   <span data-ttu-id="9bafc-131">Consulte [padrão de controle de grade](uiauto-implementinggrid.md) para funcionalidade de grade relacionada.</span><span class="sxs-lookup"><span data-stu-id="9bafc-131">See [Grid Control Pattern](uiauto-implementinggrid.md) for related grid functionality.</span></span>

    <span data-ttu-id="9bafc-132">A imagem a seguir mostra uma tabela com cabeçalhos de coluna complexos.</span><span class="sxs-lookup"><span data-stu-id="9bafc-132">The following image shows a table with complex column headers.</span></span>

    ![tabela com cabeçalhos de coluna complexos](images/uia-valuepattern-colorpicker.jpg)

    <span data-ttu-id="9bafc-134">A imagem a seguir mostra uma tabela com uma propriedade [**ITableProvider:: RowOrColumnMajor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-get_roworcolumnmajor) ambígua.</span><span class="sxs-lookup"><span data-stu-id="9bafc-134">The following image shows a table with an ambiguous [**ITableProvider::RowOrColumnMajor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-get_roworcolumnmajor) property.</span></span>

    ![tabela com uma propriedade RowOrColumnMajor ambígua](images/uia-tablepattern-roworcolumnmajorproperty.jpg)

## <a name="required-members-for-itableprovider"></a><span data-ttu-id="9bafc-136">Membros necessários para **ITableProvider**</span><span class="sxs-lookup"><span data-stu-id="9bafc-136">Required Members for **ITableProvider**</span></span>

<span data-ttu-id="9bafc-137">As propriedades e os métodos a seguir são necessários para implementar a interface [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider) .</span><span class="sxs-lookup"><span data-stu-id="9bafc-137">The following properties and methods are required for implementing the [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider) interface.</span></span>



| <span data-ttu-id="9bafc-138">Membros necessários</span><span class="sxs-lookup"><span data-stu-id="9bafc-138">Required members</span></span>                                                   | <span data-ttu-id="9bafc-139">Tipo de membro</span><span class="sxs-lookup"><span data-stu-id="9bafc-139">Member type</span></span> | <span data-ttu-id="9bafc-140">Observações</span><span class="sxs-lookup"><span data-stu-id="9bafc-140">Notes</span></span> |
|--------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="9bafc-141">**RowOrColumnMajor**</span><span class="sxs-lookup"><span data-stu-id="9bafc-141">**RowOrColumnMajor**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-get_roworcolumnmajor) | <span data-ttu-id="9bafc-142">Propriedade</span><span class="sxs-lookup"><span data-stu-id="9bafc-142">Property</span></span>    | <span data-ttu-id="9bafc-143">Nenhum</span><span class="sxs-lookup"><span data-stu-id="9bafc-143">None</span></span>  |
| [<span data-ttu-id="9bafc-144">**GetColumnHeaders**</span><span class="sxs-lookup"><span data-stu-id="9bafc-144">**GetColumnHeaders**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-getcolumnheaders) | <span data-ttu-id="9bafc-145">Método</span><span class="sxs-lookup"><span data-stu-id="9bafc-145">Method</span></span>      | <span data-ttu-id="9bafc-146">Nenhum</span><span class="sxs-lookup"><span data-stu-id="9bafc-146">None</span></span>  |
| [<span data-ttu-id="9bafc-147">**GetRowHeaders**</span><span class="sxs-lookup"><span data-stu-id="9bafc-147">**GetRowHeaders**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-getrowheaders)       | <span data-ttu-id="9bafc-148">Método</span><span class="sxs-lookup"><span data-stu-id="9bafc-148">Method</span></span>      | <span data-ttu-id="9bafc-149">Nenhum</span><span class="sxs-lookup"><span data-stu-id="9bafc-149">None</span></span>  |



 

<span data-ttu-id="9bafc-150">Este padrão de controle não tem eventos associados.</span><span class="sxs-lookup"><span data-stu-id="9bafc-150">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9bafc-151">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9bafc-151">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="9bafc-152">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="9bafc-152">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9bafc-153">Tipos de controle e seus padrões de controle com suporte</span><span class="sxs-lookup"><span data-stu-id="9bafc-153">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="9bafc-154">Padrão de controle TableItem</span><span class="sxs-lookup"><span data-stu-id="9bafc-154">TableItem Control Pattern</span></span>](uiauto-implementingtableitem.md)
</dt> <dt>

[<span data-ttu-id="9bafc-155">Visão Geral de Padrões de Controle de Automação de Interface de Usuário</span><span class="sxs-lookup"><span data-stu-id="9bafc-155">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="9bafc-156">Visão geral da árvore de automação de interface do usuário</span><span class="sxs-lookup"><span data-stu-id="9bafc-156">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




