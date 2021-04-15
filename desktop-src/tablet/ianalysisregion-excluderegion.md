---
description: Restringe a área do IAnalysisRegion à parte de sua área que não faz a interseção do IAnalysisRegion especificado.
ms.assetid: 7a11d2a8-c2ca-4088-b932-8a6c3e789b7f
title: 'Método IAnalysisRegion:: ExcludeRegion (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.ExcludeRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 13324d872a76a9184e6ea67b227dbd7444684bb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501824"
---
# <a name="ianalysisregionexcluderegion-method"></a><span data-ttu-id="555e7-103">Método IAnalysisRegion:: ExcludeRegion</span><span class="sxs-lookup"><span data-stu-id="555e7-103">IAnalysisRegion::ExcludeRegion method</span></span>

<span data-ttu-id="555e7-104">Restringe a área do [**IAnalysisRegion**](ianalysisregion.md) à parte de sua área que não faz a interseção do **IAnalysisRegion** especificado.</span><span class="sxs-lookup"><span data-stu-id="555e7-104">Restricts the area of the [**IAnalysisRegion**](ianalysisregion.md) to the portion of its area that does not intersect the specified **IAnalysisRegion**.</span></span>

## <a name="syntax"></a><span data-ttu-id="555e7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="555e7-105">Syntax</span></span>


```C++
HRESULT ExcludeRegion(
  [in] IAnalysisRegion *pRegionToExclude
);
```



## <a name="parameters"></a><span data-ttu-id="555e7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="555e7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="555e7-107">*pRegionToExclude* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="555e7-107">*pRegionToExclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="555e7-108">O [**IAnalysisRegion**](ianalysisregion.md) a ser excluído deste **IAnalysisRegion**.</span><span class="sxs-lookup"><span data-stu-id="555e7-108">The [**IAnalysisRegion**](ianalysisregion.md) to exclude from this **IAnalysisRegion**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="555e7-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="555e7-109">Return value</span></span>

<span data-ttu-id="555e7-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="555e7-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="555e7-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="555e7-111">Remarks</span></span>

<span data-ttu-id="555e7-112">Se as duas áreas não interseccionarem, esse [**IAnalysisRegion**](ianalysisregion.md) não será alterado.</span><span class="sxs-lookup"><span data-stu-id="555e7-112">If the two areas do not intersect, this [**IAnalysisRegion**](ianalysisregion.md) is unchanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="555e7-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="555e7-113">Requirements</span></span>



| <span data-ttu-id="555e7-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="555e7-114">Requirement</span></span> | <span data-ttu-id="555e7-115">Valor</span><span class="sxs-lookup"><span data-stu-id="555e7-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="555e7-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="555e7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="555e7-117">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="555e7-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="555e7-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="555e7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="555e7-119">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="555e7-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="555e7-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="555e7-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="555e7-121"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="555e7-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="555e7-122">DLL</span><span class="sxs-lookup"><span data-stu-id="555e7-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="555e7-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="555e7-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="555e7-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="555e7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="555e7-125">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="555e7-125">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="555e7-126">**IAnalysisRegion::ExcludeRectangle**</span><span class="sxs-lookup"><span data-stu-id="555e7-126">**IAnalysisRegion::ExcludeRectangle**</span></span>](ianalysisregion-excluderectangle.md)
</dt> <dt>

[<span data-ttu-id="555e7-127">**Método IAnalysisRegion:: IntersectRectangle**</span><span class="sxs-lookup"><span data-stu-id="555e7-127">**IAnalysisRegion::IntersectRectangle Method**</span></span>](ianalysisregion-intersectrectangle.md)
</dt> <dt>

[<span data-ttu-id="555e7-128">**Método IAnalysisRegion:: IntersectRegion**</span><span class="sxs-lookup"><span data-stu-id="555e7-128">**IAnalysisRegion::IntersectRegion Method**</span></span>](ianalysisregion-intersectregion.md)
</dt> <dt>

[<span data-ttu-id="555e7-129">**Método IAnalysisRegion:: UnionRectangle**</span><span class="sxs-lookup"><span data-stu-id="555e7-129">**IAnalysisRegion::UnionRectangle Method**</span></span>](ianalysisregion-unionrectangle.md)
</dt> <dt>

[<span data-ttu-id="555e7-130">**Método IAnalysisRegion:: UnionRegion**</span><span class="sxs-lookup"><span data-stu-id="555e7-130">**IAnalysisRegion::UnionRegion Method**</span></span>](ianalysisregion-unionregion.md)
</dt> <dt>

[<span data-ttu-id="555e7-131">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="555e7-131">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




