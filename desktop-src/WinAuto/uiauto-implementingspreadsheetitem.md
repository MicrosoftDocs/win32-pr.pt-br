---
title: Padrão de controle SpreadsheetItem
description: Descreve as diretrizes e convenções para implementar o ISpreadsheetItemProvider, incluindo informações sobre propriedades e métodos.
ms.assetid: AADD06C5-CF51-4A1A-9ACB-3E896050D7DD
keywords:
- Automação da interface do usuário, implementando o padrão de controle SpreadsheetItem
- Automação da interface do usuário, padrão de controle SpreadsheetItem
- Automação da interface do usuário, ISpreadsheetItemProvider
- ISpreadsheetItemProvider
- Implementando o padrão de controle SpreadsheetItem Automation UI
- Padrão de controle SpreadsheetItem
- padrões de controle, ISpreadsheetItemProvider
- padrões de controle, implementando a automação da interface do usuário SpreadsheetItem
- padrões de controle, SpreadsheetItem
- interfaces, ISpreadsheetItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88ba050c5a5c8b10c68695fdf1a05d845353e638
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008036"
---
# <a name="spreadsheetitem-control-pattern"></a><span data-ttu-id="93df1-113">Padrão de controle SpreadsheetItem</span><span class="sxs-lookup"><span data-stu-id="93df1-113">SpreadsheetItem Control Pattern</span></span>

<span data-ttu-id="93df1-114">Descreve as diretrizes e convenções para implementar o [**ISpreadsheetItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ispreadsheetitemprovider), incluindo informações sobre propriedades e métodos.</span><span class="sxs-lookup"><span data-stu-id="93df1-114">Describes guidelines and conventions for implementing [**ISpreadsheetItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ispreadsheetitemprovider), including information about properties and methods.</span></span> <span data-ttu-id="93df1-115">O padrão de controle **SpreadsheetItem** é usado para expor as propriedades de uma célula em uma planilha ou outro documento baseado em grade.</span><span class="sxs-lookup"><span data-stu-id="93df1-115">The **SpreadsheetItem** control pattern is used to expose the properties of a cell in a spreadsheet or other grid-based document.</span></span>

<span data-ttu-id="93df1-116">O padrão de controle **SpreadsheetItem** está fortemente relacionado ao padrão de controle [GridItem](uiauto-implementinggriditem.md) ; os controles que implementam o padrão de controle **SpreadsheetItem** também devem implementar o padrão de controle GridItem.</span><span class="sxs-lookup"><span data-stu-id="93df1-116">The **SpreadsheetItem** control pattern is closely related to the [GridItem](uiauto-implementinggriditem.md) control pattern; controls that implement the **SpreadsheetItem** control pattern should also implement the GridItem control pattern.</span></span> <span data-ttu-id="93df1-117">Os controles também podem implementar o padrão de controle [TableItem](uiauto-implementingtableitem.md) , se apropriado.</span><span class="sxs-lookup"><span data-stu-id="93df1-117">Controls can also implement the [TableItem](uiauto-implementingtableitem.md) control pattern, if appropriate.</span></span> <span data-ttu-id="93df1-118">Para obter exemplos de controles que implementam esses padrões de controle, consulte [tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="93df1-118">For examples of controls that implement these control patterns, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="93df1-119">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="93df1-119">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="93df1-120">Diretrizes e convenções de implementação</span><span class="sxs-lookup"><span data-stu-id="93df1-120">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="93df1-121">Membros necessários para **ISpreadsheetItemProvider**</span><span class="sxs-lookup"><span data-stu-id="93df1-121">Required Members for **ISpreadsheetItemProvider**</span></span>](#required-members-for-ispreadsheetitemprovider)
-   [<span data-ttu-id="93df1-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="93df1-122">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="93df1-123">Diretrizes e convenções de implementação</span><span class="sxs-lookup"><span data-stu-id="93df1-123">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="93df1-124">Ao implementar o padrão de controle **SpreadsheetItem** , observe as seguintes diretrizes e convenções:</span><span class="sxs-lookup"><span data-stu-id="93df1-124">When implementing the **SpreadsheetItem** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="93df1-125">Ao implementar os métodos [**ISpreadsheetItemProvider:: GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) e [**ISpreadsheetItemProvider:: GetAnnotationTypes**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes) , consulte a documentação do [**IAnnotationProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) .</span><span class="sxs-lookup"><span data-stu-id="93df1-125">When implementing the [**ISpreadsheetItemProvider::GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) and [**ISpreadsheetItemProvider::GetAnnotationTypes**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes) methods, please refer to the [**IAnnotationProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) documentation.</span></span> <span data-ttu-id="93df1-126">Esses métodos retornam matrizes para permitir que os provedores ofereçam suporte a várias anotações em uma única célula.</span><span class="sxs-lookup"><span data-stu-id="93df1-126">These methods both return arrays to enable providers to support multiple annotations on a single cell.</span></span>
-   <span data-ttu-id="93df1-127">Alguns tipos de anotações não exigem uma implementação completa da interface [**IAnnotationProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) .</span><span class="sxs-lookup"><span data-stu-id="93df1-127">Some kinds of annotations do not require a full implementation of the [**IAnnotationProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) interface.</span></span> <span data-ttu-id="93df1-128">Por exemplo, um indicador de erro ortográfico simples poderia ser representado ao fazer com que [**GetAnnotationTypes**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes) retornasse um identificador de atributo de texto de [**\_ SpellingError de AnnotationType**](uiauto-annotation-type-identifiers.md)e ter [**GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) retornado um valor nulo.</span><span class="sxs-lookup"><span data-stu-id="93df1-128">For example, a simple spelling-error indicator could be represented by having [**GetAnnotationTypes**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes) return a text attribute identifier of [**AnnotationType\_SpellingError**](uiauto-annotation-type-identifiers.md), and having [**GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) return a null value.</span></span>

## <a name="required-members-for-ispreadsheetitemprovider"></a><span data-ttu-id="93df1-129">Membros necessários para **ISpreadsheetItemProvider**</span><span class="sxs-lookup"><span data-stu-id="93df1-129">Required Members for **ISpreadsheetItemProvider**</span></span>

<span data-ttu-id="93df1-130">As propriedades e os métodos a seguir são necessários para implementar a interface [**ISpreadsheetItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ispreadsheetitemprovider) .</span><span class="sxs-lookup"><span data-stu-id="93df1-130">The following properties and methods are required for implementing the [**ISpreadsheetItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ispreadsheetitemprovider) interface.</span></span>



| <span data-ttu-id="93df1-131">Membros necessários</span><span class="sxs-lookup"><span data-stu-id="93df1-131">Required members</span></span>                                                                         | <span data-ttu-id="93df1-132">Tipo de membro</span><span class="sxs-lookup"><span data-stu-id="93df1-132">Member type</span></span> | <span data-ttu-id="93df1-133">Observações</span><span class="sxs-lookup"><span data-stu-id="93df1-133">Notes</span></span>                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="93df1-134">**Fórmula**</span><span class="sxs-lookup"><span data-stu-id="93df1-134">**Formula**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-get_formula)                           | <span data-ttu-id="93df1-135">Propriedade</span><span class="sxs-lookup"><span data-stu-id="93df1-135">Property</span></span>    | <span data-ttu-id="93df1-136">A implementação de uma propriedade de [**fórmula**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-get_formula) separada é necessária porque a propriedade de [valor](value-property.md) de uma célula normalmente retorna o valor calculado da célula.</span><span class="sxs-lookup"><span data-stu-id="93df1-136">Implementing a separate [**Formula**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-get_formula) property is necessary because a cell’s [Value](value-property.md) property typically returns the computed value of the cell.</span></span> <span data-ttu-id="93df1-137">A propriedade de **fórmula** deverá ser **nula** se nenhuma fórmula for definida.</span><span class="sxs-lookup"><span data-stu-id="93df1-137">The **Formula** property should be **NULL** if no formula is set.</span></span> |
| [<span data-ttu-id="93df1-138">**GetAnnotationObjects**</span><span class="sxs-lookup"><span data-stu-id="93df1-138">**GetAnnotationObjects**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) | <span data-ttu-id="93df1-139">Método</span><span class="sxs-lookup"><span data-stu-id="93df1-139">Method</span></span>      | <span data-ttu-id="93df1-140">Retorna uma matriz de provedores de elementos que se refere às anotações vinculadas a esta célula.</span><span class="sxs-lookup"><span data-stu-id="93df1-140">Returns an array of element providers that refer to the annotations linked to this cell.</span></span> <span data-ttu-id="93df1-141">Os ponteiros dentro da matriz poderão ser nulos se uma anotação não tiver um provedor vinculado.</span><span class="sxs-lookup"><span data-stu-id="93df1-141">Pointers within the array can be null if an annotation does not have a linked provider.</span></span>                                                                                                       |
| [<span data-ttu-id="93df1-142">**GetAnnotationTypes**</span><span class="sxs-lookup"><span data-stu-id="93df1-142">**GetAnnotationTypes**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes)     | <span data-ttu-id="93df1-143">Método</span><span class="sxs-lookup"><span data-stu-id="93df1-143">Method</span></span>      | <span data-ttu-id="93df1-144">Retorna uma matriz de identificadores de tipo de anotação que descrevem as anotações nesta célula.</span><span class="sxs-lookup"><span data-stu-id="93df1-144">Returns an array of annotation type identifiers that describe the annotations on this cell.</span></span> <span data-ttu-id="93df1-145">A matriz deve ter o mesmo tamanho que a matriz retornada por [**GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects).</span><span class="sxs-lookup"><span data-stu-id="93df1-145">The array must be the same size as the array returned by [**GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects).</span></span>                                         |



 

<span data-ttu-id="93df1-146">Este padrão de controle não tem eventos associados.</span><span class="sxs-lookup"><span data-stu-id="93df1-146">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="93df1-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="93df1-147">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="93df1-148">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="93df1-148">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="93df1-149">Tipos de controle e seus padrões de controle com suporte</span><span class="sxs-lookup"><span data-stu-id="93df1-149">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="93df1-150">Padrão de controle de planilha</span><span class="sxs-lookup"><span data-stu-id="93df1-150">Spreadsheet Control Pattern</span></span>](uiauto-implementingspreadsheet.md)
</dt> <dt>

[<span data-ttu-id="93df1-151">Visão Geral de Padrões de Controle de Automação de Interface de Usuário</span><span class="sxs-lookup"><span data-stu-id="93df1-151">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="93df1-152">Visão geral da árvore de automação de interface do usuário</span><span class="sxs-lookup"><span data-stu-id="93df1-152">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 