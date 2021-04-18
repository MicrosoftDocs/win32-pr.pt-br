---
description: Expande a área desta IAnalysisRegion para a área criada por sua união com o IAnalysisRegion especificado.
ms.assetid: cc3ec5c6-98ff-442e-a1e8-d1a57752ad56
title: 'Método IAnalysisRegion:: UnionRegion (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.UnionRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 587986973c4ae4bebaeed3c031c746bc4f842c42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765049"
---
# <a name="ianalysisregionunionregion-method"></a><span data-ttu-id="16cca-103">Método IAnalysisRegion:: UnionRegion</span><span class="sxs-lookup"><span data-stu-id="16cca-103">IAnalysisRegion::UnionRegion method</span></span>

<span data-ttu-id="16cca-104">Expande a área desta [**IAnalysisRegion**](ianalysisregion.md) para a área criada por sua união com o **IAnalysisRegion** especificado.</span><span class="sxs-lookup"><span data-stu-id="16cca-104">Expands the area of this [**IAnalysisRegion**](ianalysisregion.md) to the area created by its union with the specified **IAnalysisRegion**.</span></span>

## <a name="syntax"></a><span data-ttu-id="16cca-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="16cca-105">Syntax</span></span>


```C++
HRESULT UnionRegion(
  [in] IAnalysisRegion *pRegionToUnion
);
```



## <a name="parameters"></a><span data-ttu-id="16cca-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="16cca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16cca-107">*pRegionToUnion* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="16cca-107">*pRegionToUnion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16cca-108">O [**IAnalysisRegion**](ianalysisregion.md) com o qual combinar.</span><span class="sxs-lookup"><span data-stu-id="16cca-108">The [**IAnalysisRegion**](ianalysisregion.md) with which to combine.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16cca-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="16cca-109">Return value</span></span>

<span data-ttu-id="16cca-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="16cca-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="16cca-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="16cca-111">Remarks</span></span>

<span data-ttu-id="16cca-112">Se qualquer área for infinita, a nova área também será infinita.</span><span class="sxs-lookup"><span data-stu-id="16cca-112">If either area is infinite, the new area is also infinite.</span></span>

## <a name="requirements"></a><span data-ttu-id="16cca-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16cca-113">Requirements</span></span>



| <span data-ttu-id="16cca-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="16cca-114">Requirement</span></span> | <span data-ttu-id="16cca-115">Valor</span><span class="sxs-lookup"><span data-stu-id="16cca-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16cca-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="16cca-116">Minimum supported client</span></span><br/> | <span data-ttu-id="16cca-117">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="16cca-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="16cca-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="16cca-118">Minimum supported server</span></span><br/> | <span data-ttu-id="16cca-119">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="16cca-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="16cca-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="16cca-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="16cca-121"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="16cca-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="16cca-122">DLL</span><span class="sxs-lookup"><span data-stu-id="16cca-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16cca-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16cca-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="16cca-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="16cca-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16cca-125">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="16cca-125">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="16cca-126">**IAnalysisRegion::ExcludeRectangle**</span><span class="sxs-lookup"><span data-stu-id="16cca-126">**IAnalysisRegion::ExcludeRectangle**</span></span>](ianalysisregion-excluderectangle.md)
</dt> <dt>

[<span data-ttu-id="16cca-127">**Método IAnalysisRegion:: ExcludeRegion**</span><span class="sxs-lookup"><span data-stu-id="16cca-127">**IAnalysisRegion::ExcludeRegion Method**</span></span>](ianalysisregion-excluderegion.md)
</dt> <dt>

[<span data-ttu-id="16cca-128">**Método IAnalysisRegion:: IntersectRectangle**</span><span class="sxs-lookup"><span data-stu-id="16cca-128">**IAnalysisRegion::IntersectRectangle Method**</span></span>](ianalysisregion-intersectrectangle.md)
</dt> <dt>

[<span data-ttu-id="16cca-129">**Método IAnalysisRegion:: IntersectRegion**</span><span class="sxs-lookup"><span data-stu-id="16cca-129">**IAnalysisRegion::IntersectRegion Method**</span></span>](ianalysisregion-intersectregion.md)
</dt> <dt>

[<span data-ttu-id="16cca-130">**Método IAnalysisRegion:: UnionRectangle**</span><span class="sxs-lookup"><span data-stu-id="16cca-130">**IAnalysisRegion::UnionRectangle Method**</span></span>](ianalysisregion-unionrectangle.md)
</dt> <dt>

[<span data-ttu-id="16cca-131">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="16cca-131">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




