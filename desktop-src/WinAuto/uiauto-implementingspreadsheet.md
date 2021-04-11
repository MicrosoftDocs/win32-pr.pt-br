---
title: Padrão de controle de planilha
description: Descreve as diretrizes e convenções para implementar o ISpreadsheetProvider, incluindo informações sobre métodos.
ms.assetid: 4004D867-8367-486A-96ED-DE5B41D24935
keywords:
- Automação da interface do usuário, implementação do padrão de controle da planilha
- Automação da interface do usuário, padrão de controle da planilha
- Automação da interface do usuário, ISpreadsheetProvider
- ISpreadsheetProvider
- Implementando o padrão de controle da planilha de automação da interface
- padrão de controle de planilha
- padrões de controle, ISpreadsheetProvider
- padrões de controle, implementação da planilha de automação da interface do usuário
- padrões de controle, planilha
- interfaces, ISpreadsheetProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4be34174745ccf91435db92665b98eb387f7241a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294273"
---
# <a name="spreadsheet-control-pattern"></a><span data-ttu-id="a5ef9-113">Padrão de controle de planilha</span><span class="sxs-lookup"><span data-stu-id="a5ef9-113">Spreadsheet Control Pattern</span></span>

<span data-ttu-id="a5ef9-114">Descreve as diretrizes e convenções para implementar o [**ISpreadsheetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider), incluindo informações sobre métodos.</span><span class="sxs-lookup"><span data-stu-id="a5ef9-114">Describes guidelines and conventions for implementing [**ISpreadsheetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider), including information about methods.</span></span> <span data-ttu-id="a5ef9-115">Links para referências adicionais são listados no final do tópico.</span><span class="sxs-lookup"><span data-stu-id="a5ef9-115">Links to additional references are listed at the end of the topic.</span></span> <span data-ttu-id="a5ef9-116">O padrão de controle de **planilha** é usado para expor o conteúdo de uma planilha ou outro documento baseado em grade.</span><span class="sxs-lookup"><span data-stu-id="a5ef9-116">The **Spreadsheet** control pattern is used to expose the contents of a spreadsheet or other grid-based document.</span></span>

<span data-ttu-id="a5ef9-117">O padrão de controle de **planilha** está fortemente relacionado ao padrão de controle de [grade](uiauto-implementinggrid.md) ; os controles que implementam o padrão de controle de **planilha** também devem implementar o padrão de controle de grade.</span><span class="sxs-lookup"><span data-stu-id="a5ef9-117">The **Spreadsheet** control pattern is closely related to the [Grid](uiauto-implementinggrid.md) control pattern; controls that implement the **Spreadsheet** control pattern should also implement the Grid control pattern.</span></span> <span data-ttu-id="a5ef9-118">Os controles também podem implementar o padrão de controle de [tabela](uiauto-implementingtable.md) , se apropriado.</span><span class="sxs-lookup"><span data-stu-id="a5ef9-118">Controls can also implement the [Table](uiauto-implementingtable.md) control pattern, if appropriate.</span></span> <span data-ttu-id="a5ef9-119">Para obter exemplos de controles que implementam esses padrões de controle, consulte [tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="a5ef9-119">For examples of controls that implement these control patterns, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="a5ef9-120">Diretrizes e convenções de implementação</span><span class="sxs-lookup"><span data-stu-id="a5ef9-120">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="a5ef9-121">Ao implementar o padrão de controle de **planilha** , observe as seguintes diretrizes e convenções:</span><span class="sxs-lookup"><span data-stu-id="a5ef9-121">When implementing the **Spreadsheet** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="a5ef9-122">Se uma planilha implementar a interface [**ISpreadsheetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider) , suas células deverão implementar a interface [**ISpreadsheetItemProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetitemprovider) .</span><span class="sxs-lookup"><span data-stu-id="a5ef9-122">If a spreadsheet implements the [**ISpreadsheetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider) interface, its cells must implement the [**ISpreadsheetItemProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetitemprovider) interface.</span></span>
-   <span data-ttu-id="a5ef9-123">O método [**ISpreadsheetProvider:: GetItemByName**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetprovider-getitembyname) destina-se a fornecer o mesmo tipo de navegação que um aplicativo pode fornecer com um recurso de **salto para rótulo** .</span><span class="sxs-lookup"><span data-stu-id="a5ef9-123">The [**ISpreadsheetProvider::GetItemByName**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetprovider-getitembyname) method is intended to provide the same kind of navigation that an application might supply with a **Jump to Label** feature.</span></span> <span data-ttu-id="a5ef9-124">Muitos programas de planilha permitem que células específicas recebam um nome amigável ou rótulo.</span><span class="sxs-lookup"><span data-stu-id="a5ef9-124">Many spreadsheet programs let specific cells be given a friendly name or label.</span></span> <span data-ttu-id="a5ef9-125">O **GetItemByName** permite que o cliente pesquise uma célula com base em seu nome amigável.</span><span class="sxs-lookup"><span data-stu-id="a5ef9-125">**GetItemByName** enables the client to look up a cell based on its friendly name.</span></span> <span data-ttu-id="a5ef9-126">Esse método não deve recuperar nenhuma célula que contenha o texto de nome porque os resultados podem ser altamente ambíguos.</span><span class="sxs-lookup"><span data-stu-id="a5ef9-126">This method should not retrieve any cells that contain the name text because the results can be highly ambiguous.</span></span> <span data-ttu-id="a5ef9-127">Se o programa de planilha permitir que várias células na mesma planilha tenham o mesmo nome amigável ou rótulo, o comportamento da automação da interface do usuário da Microsoft será indefinido.</span><span class="sxs-lookup"><span data-stu-id="a5ef9-127">If the spreadsheet program allows multiple cells in the same a spreadsheet to have the same friendly name or label, the Microsoft UI Automation behavior is undefined.</span></span>

## <a name="required-members-for-ispreadsheetprovider"></a><span data-ttu-id="a5ef9-128">Membros necessários para **ISpreadsheetProvider**</span><span class="sxs-lookup"><span data-stu-id="a5ef9-128">Required Members for **ISpreadsheetProvider**</span></span>

<span data-ttu-id="a5ef9-129">O método a seguir é necessário para implementar a interface [**ISpreadsheetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider) .</span><span class="sxs-lookup"><span data-stu-id="a5ef9-129">The following method is required for implementing the [**ISpreadsheetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider) interface.</span></span>



| <span data-ttu-id="a5ef9-130">Membros necessários</span><span class="sxs-lookup"><span data-stu-id="a5ef9-130">Required members</span></span>                                                       | <span data-ttu-id="a5ef9-131">Tipo de membro</span><span class="sxs-lookup"><span data-stu-id="a5ef9-131">Member type</span></span> | <span data-ttu-id="a5ef9-132">Observações</span><span class="sxs-lookup"><span data-stu-id="a5ef9-132">Notes</span></span> |
|------------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="a5ef9-133">**GetItemByName**</span><span class="sxs-lookup"><span data-stu-id="a5ef9-133">**GetItemByName**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetprovider-getitembyname) | <span data-ttu-id="a5ef9-134">Método</span><span class="sxs-lookup"><span data-stu-id="a5ef9-134">Method</span></span>      | <span data-ttu-id="a5ef9-135">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a5ef9-135">None</span></span>  |



 

<span data-ttu-id="a5ef9-136">Este padrão de controle não tem eventos associados.</span><span class="sxs-lookup"><span data-stu-id="a5ef9-136">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a5ef9-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a5ef9-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5ef9-138">Tipos de controle e seus padrões de controle com suporte</span><span class="sxs-lookup"><span data-stu-id="a5ef9-138">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="a5ef9-139">Visão Geral de Padrões de Controle de Automação de Interface de Usuário</span><span class="sxs-lookup"><span data-stu-id="a5ef9-139">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="a5ef9-140">Visão geral da árvore de automação de interface do usuário</span><span class="sxs-lookup"><span data-stu-id="a5ef9-140">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 