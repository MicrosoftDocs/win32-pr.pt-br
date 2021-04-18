---
description: Restringe a área de IAnalysisRegion para a área criada por sua interseção com o IAnalysisRegion especificado.
ms.assetid: 02b3049f-ada9-4de3-a7a2-f9ff8313fbab
title: 'Método IAnalysisRegion:: IntersectRegion (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IntersectRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 7ff3caad382e54f41685f6102edafdeb86b813c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105791613"
---
# <a name="ianalysisregionintersectregion-method"></a><span data-ttu-id="b1e87-103">Método IAnalysisRegion:: IntersectRegion</span><span class="sxs-lookup"><span data-stu-id="b1e87-103">IAnalysisRegion::IntersectRegion method</span></span>

<span data-ttu-id="b1e87-104">Restringe a área de [**IAnalysisRegion**](ianalysisregion.md) para a área criada por sua interseção com o **IAnalysisRegion** especificado.</span><span class="sxs-lookup"><span data-stu-id="b1e87-104">Restricts the area of the [**IAnalysisRegion**](ianalysisregion.md) to the area created by its intersection with the specified **IAnalysisRegion**.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1e87-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b1e87-105">Syntax</span></span>


```C++
HRESULT IntersectRegion(
  [in] IAnalysisRegion *pRegionToIntersect
);
```



## <a name="parameters"></a><span data-ttu-id="b1e87-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b1e87-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1e87-107">*pRegionToIntersect* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b1e87-107">*pRegionToIntersect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1e87-108">O [**IAnalysisRegion**](ianalysisregion.md) com o qual fazer a interseção.</span><span class="sxs-lookup"><span data-stu-id="b1e87-108">The [**IAnalysisRegion**](ianalysisregion.md) with which to intersect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1e87-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b1e87-109">Return value</span></span>

<span data-ttu-id="b1e87-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="b1e87-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b1e87-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="b1e87-111">Remarks</span></span>

<span data-ttu-id="b1e87-112">Se as duas áreas não se interseccionarem, a nova área estará vazia.</span><span class="sxs-lookup"><span data-stu-id="b1e87-112">If the two areas do not intersect, the new area is empty.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1e87-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1e87-113">Requirements</span></span>



| <span data-ttu-id="b1e87-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1e87-114">Requirement</span></span> | <span data-ttu-id="b1e87-115">Valor</span><span class="sxs-lookup"><span data-stu-id="b1e87-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1e87-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b1e87-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b1e87-117">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="b1e87-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b1e87-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b1e87-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b1e87-119">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b1e87-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="b1e87-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b1e87-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1e87-121"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b1e87-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b1e87-122">DLL</span><span class="sxs-lookup"><span data-stu-id="b1e87-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1e87-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1e87-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="b1e87-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="b1e87-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1e87-125">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="b1e87-125">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="b1e87-126">**IAnalysisRegion::ExcludeRectangle**</span><span class="sxs-lookup"><span data-stu-id="b1e87-126">**IAnalysisRegion::ExcludeRectangle**</span></span>](ianalysisregion-excluderectangle.md)
</dt> <dt>

[<span data-ttu-id="b1e87-127">**Método IAnalysisRegion:: ExcludeRegion**</span><span class="sxs-lookup"><span data-stu-id="b1e87-127">**IAnalysisRegion::ExcludeRegion Method**</span></span>](ianalysisregion-excluderegion.md)
</dt> <dt>

[<span data-ttu-id="b1e87-128">**Método IAnalysisRegion:: IntersectRectangle**</span><span class="sxs-lookup"><span data-stu-id="b1e87-128">**IAnalysisRegion::IntersectRectangle Method**</span></span>](ianalysisregion-intersectrectangle.md)
</dt> <dt>

[<span data-ttu-id="b1e87-129">**Método IAnalysisRegion:: UnionRectangle**</span><span class="sxs-lookup"><span data-stu-id="b1e87-129">**IAnalysisRegion::UnionRectangle Method**</span></span>](ianalysisregion-unionrectangle.md)
</dt> <dt>

[<span data-ttu-id="b1e87-130">**Método IAnalysisRegion:: UnionRegion**</span><span class="sxs-lookup"><span data-stu-id="b1e87-130">**IAnalysisRegion::UnionRegion Method**</span></span>](ianalysisregion-unionregion.md)
</dt> <dt>

[<span data-ttu-id="b1e87-131">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="b1e87-131">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




