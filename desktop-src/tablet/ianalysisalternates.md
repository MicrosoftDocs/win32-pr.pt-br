---
description: Contém uma coleção de objetos que implementam a interface IAnalysisAlternate e que são o resultado da análise de tinta.
ms.assetid: 53802a62-4425-40fd-bf48-0da55ea8ffbe
title: Interface IAnalysisAlternates (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternates
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4e43feaa40f519707531894936bf34ce19e57723
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788859"
---
# <a name="ianalysisalternates-interface"></a><span data-ttu-id="aa4f1-103">Interface IAnalysisAlternates</span><span class="sxs-lookup"><span data-stu-id="aa4f1-103">IAnalysisAlternates interface</span></span>

<span data-ttu-id="aa4f1-104">Contém uma coleção de objetos que implementam a interface [**IAnalysisAlternate**](ianalysisalternate.md) e que são o resultado da análise de tinta.</span><span class="sxs-lookup"><span data-stu-id="aa4f1-104">Contains a collection of objects that implement the [**IAnalysisAlternate**](ianalysisalternate.md) interface and that are the result of ink analysis.</span></span>

## <a name="members"></a><span data-ttu-id="aa4f1-105">Membros</span><span class="sxs-lookup"><span data-stu-id="aa4f1-105">Members</span></span>

<span data-ttu-id="aa4f1-106">A interface **IAnalysisAlternates** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="aa4f1-106">The **IAnalysisAlternates** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="aa4f1-107">**IAnalysisAlternates** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="aa4f1-107">**IAnalysisAlternates** also has these types of members:</span></span>

-   [<span data-ttu-id="aa4f1-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="aa4f1-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="aa4f1-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="aa4f1-109">Methods</span></span>

<span data-ttu-id="aa4f1-110">A interface **IAnalysisAlternates** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="aa4f1-110">The **IAnalysisAlternates** interface has these methods.</span></span>



| <span data-ttu-id="aa4f1-111">Método</span><span class="sxs-lookup"><span data-stu-id="aa4f1-111">Method</span></span>                                                                   | <span data-ttu-id="aa4f1-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="aa4f1-112">Description</span></span>                                                                                                                                      |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="aa4f1-113">**GetAnalysisAlternate**</span><span class="sxs-lookup"><span data-stu-id="aa4f1-113">**GetAnalysisAlternate**</span></span>](ianalysisalternates-getanalysisalternate.md) | <span data-ttu-id="aa4f1-114">Recupera o objeto [**IAnalysisAlternate**](ianalysisalternate.md) no índice especificado dentro da coleção.</span><span class="sxs-lookup"><span data-stu-id="aa4f1-114">Retrieves the [**IAnalysisAlternate**](ianalysisalternate.md) object at the specified index within the collection.</span></span><br/>                   |
| [<span data-ttu-id="aa4f1-115">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="aa4f1-115">**GetCount**</span></span>](ianalysisalternates-getcount.md)                         | <span data-ttu-id="aa4f1-116">Recupera o número de objetos [**IAnalysisAlternate**](ianalysisalternate.md) contidos na coleção **IAnalysisAlternates** .</span><span class="sxs-lookup"><span data-stu-id="aa4f1-116">Retrieves the number of [**IAnalysisAlternate**](ianalysisalternate.md) objects contained in the **IAnalysisAlternates** collection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="aa4f1-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="aa4f1-117">Remarks</span></span>

<span data-ttu-id="aa4f1-118">Essa interface é equivalente à classe [**System. Windows. Ink. AnalysisCore. AnalysisAlternateBaseCollection**](/previous-versions/ms610094(v=vs.100)) na .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="aa4f1-118">This interface is equivalent to the [**System.Windows.Ink.AnalysisCore.AnalysisAlternateBaseCollection**](/previous-versions/ms610094(v=vs.100)) class in the .NET Framework.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa4f1-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa4f1-119">Requirements</span></span>



| <span data-ttu-id="aa4f1-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa4f1-120">Requirement</span></span> | <span data-ttu-id="aa4f1-121">Valor</span><span class="sxs-lookup"><span data-stu-id="aa4f1-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa4f1-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa4f1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="aa4f1-123">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="aa4f1-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="aa4f1-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa4f1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="aa4f1-125">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="aa4f1-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="aa4f1-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="aa4f1-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa4f1-127"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="aa4f1-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="aa4f1-128">DLL</span><span class="sxs-lookup"><span data-stu-id="aa4f1-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa4f1-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa4f1-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="aa4f1-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="aa4f1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa4f1-131">**IAnalysisAlternate**</span><span class="sxs-lookup"><span data-stu-id="aa4f1-131">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="aa4f1-132">**Método IInkAnalyzer:: getalternations**</span><span class="sxs-lookup"><span data-stu-id="aa4f1-132">**IInkAnalyzer::GetAlternates Method**</span></span>](iinkanalyzer-getalternates.md)
</dt> <dt>

[<span data-ttu-id="aa4f1-133">**Método IInkAnalyzer:: GetAlternatesForContextNodes**</span><span class="sxs-lookup"><span data-stu-id="aa4f1-133">**IInkAnalyzer::GetAlternatesForContextNodes Method**</span></span>](iinkanalyzer-getalternatesforcontextnodes.md)
</dt> <dt>

[<span data-ttu-id="aa4f1-134">**Método IInkAnalyzer:: GetAlternatesForStrokes**</span><span class="sxs-lookup"><span data-stu-id="aa4f1-134">**IInkAnalyzer::GetAlternatesForStrokes Method**</span></span>](iinkanalyzer-getalternatesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="aa4f1-135">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="aa4f1-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

