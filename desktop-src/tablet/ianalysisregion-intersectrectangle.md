---
description: Restringe a área desta IAnalysisRegion para a área criada por sua interseção com o retângulo especificado.
ms.assetid: de6b565f-34c1-4551-ab92-db6bacb8608d
title: 'Método IAnalysisRegion:: IntersectRectangle (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IntersectRectangle
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4ce0e514b24aba0331d9ea604333680db1c67c8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501823"
---
# <a name="ianalysisregionintersectrectangle-method"></a><span data-ttu-id="26f23-103">Método IAnalysisRegion:: IntersectRectangle</span><span class="sxs-lookup"><span data-stu-id="26f23-103">IAnalysisRegion::IntersectRectangle method</span></span>

<span data-ttu-id="26f23-104">Restringe a área desta [**IAnalysisRegion**](ianalysisregion.md) para a área criada por sua interseção com o retângulo especificado.</span><span class="sxs-lookup"><span data-stu-id="26f23-104">Restricts the area of this [**IAnalysisRegion**](ianalysisregion.md) to the area created by its intersection with the specified rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="26f23-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="26f23-105">Syntax</span></span>


```C++
HRESULT IntersectRectangle(
  [in] RECT *pIntersectingRectangle
);
```



## <a name="parameters"></a><span data-ttu-id="26f23-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="26f23-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26f23-107">*pIntersectingRectangle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="26f23-107">*pIntersectingRectangle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26f23-108">Um ponteiro para o retângulo com o qual Interseccionar, em coordenadas de espaço de tinta.</span><span class="sxs-lookup"><span data-stu-id="26f23-108">A pointer to the rectangle with which to intersect, in ink-space coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26f23-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="26f23-109">Return value</span></span>

<span data-ttu-id="26f23-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="26f23-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="26f23-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="26f23-111">Remarks</span></span>

<span data-ttu-id="26f23-112">As coordenadas de retângulo estão em unidades HIMETRIC.</span><span class="sxs-lookup"><span data-stu-id="26f23-112">The rectangle coordinates are in HIMETRIC units.</span></span>

<span data-ttu-id="26f23-113">Se as duas áreas não se interseccionarem, a nova área estará vazia.</span><span class="sxs-lookup"><span data-stu-id="26f23-113">If the two areas do not intersect, the new area is empty.</span></span>

## <a name="requirements"></a><span data-ttu-id="26f23-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26f23-114">Requirements</span></span>



| <span data-ttu-id="26f23-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="26f23-115">Requirement</span></span> | <span data-ttu-id="26f23-116">Valor</span><span class="sxs-lookup"><span data-stu-id="26f23-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26f23-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="26f23-117">Minimum supported client</span></span><br/> | <span data-ttu-id="26f23-118">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="26f23-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="26f23-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="26f23-119">Minimum supported server</span></span><br/> | <span data-ttu-id="26f23-120">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="26f23-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="26f23-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="26f23-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="26f23-122"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="26f23-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="26f23-123">DLL</span><span class="sxs-lookup"><span data-stu-id="26f23-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26f23-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26f23-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="26f23-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="26f23-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26f23-126">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="26f23-126">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="26f23-127">**IAnalysisRegion::ExcludeRectangle**</span><span class="sxs-lookup"><span data-stu-id="26f23-127">**IAnalysisRegion::ExcludeRectangle**</span></span>](ianalysisregion-excluderectangle.md)
</dt> <dt>

[<span data-ttu-id="26f23-128">**Método IAnalysisRegion:: ExcludeRegion**</span><span class="sxs-lookup"><span data-stu-id="26f23-128">**IAnalysisRegion::ExcludeRegion Method**</span></span>](ianalysisregion-excluderegion.md)
</dt> <dt>

[<span data-ttu-id="26f23-129">**Método IAnalysisRegion:: IntersectRegion**</span><span class="sxs-lookup"><span data-stu-id="26f23-129">**IAnalysisRegion::IntersectRegion Method**</span></span>](ianalysisregion-intersectregion.md)
</dt> <dt>

[<span data-ttu-id="26f23-130">**Método IAnalysisRegion:: UnionRectangle**</span><span class="sxs-lookup"><span data-stu-id="26f23-130">**IAnalysisRegion::UnionRectangle Method**</span></span>](ianalysisregion-unionrectangle.md)
</dt> <dt>

[<span data-ttu-id="26f23-131">**Método IAnalysisRegion:: UnionRegion**</span><span class="sxs-lookup"><span data-stu-id="26f23-131">**IAnalysisRegion::UnionRegion Method**</span></span>](ianalysisregion-unionregion.md)
</dt> <dt>

[<span data-ttu-id="26f23-132">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="26f23-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




