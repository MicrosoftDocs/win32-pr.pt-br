---
description: Restringe a área do IAnalysisRegion à parte de sua área que não faz a interseção do retângulo especificado.
ms.assetid: a35b8bfc-a87a-4e9a-908f-2b13a128d222
title: 'Método IAnalysisRegion:: ExcludeRectangle (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.ExcludeRectangle
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 684ce2ceb57c7954c732fb2816aca50fcbae5297
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780432"
---
# <a name="ianalysisregionexcluderectangle-method"></a><span data-ttu-id="07843-103">Método IAnalysisRegion:: ExcludeRectangle</span><span class="sxs-lookup"><span data-stu-id="07843-103">IAnalysisRegion::ExcludeRectangle method</span></span>

<span data-ttu-id="07843-104">Restringe a área do [**IAnalysisRegion**](ianalysisregion.md) à parte de sua área que não faz a interseção do retângulo especificado.</span><span class="sxs-lookup"><span data-stu-id="07843-104">Restricts the area of the [**IAnalysisRegion**](ianalysisregion.md) to the portion of its area that does not intersect the specified rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="07843-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="07843-105">Syntax</span></span>


```C++
HRESULT ExcludeRectangle(
  [in] RECT *pExcludingRectangle
);
```



## <a name="parameters"></a><span data-ttu-id="07843-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="07843-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07843-107">*pExcludingRectangle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="07843-107">*pExcludingRectangle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07843-108">O retângulo a ser excluído deste [**IAnalysisRegion**](ianalysisregion.md).</span><span class="sxs-lookup"><span data-stu-id="07843-108">The rectangle to exclude from this [**IAnalysisRegion**](ianalysisregion.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07843-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="07843-109">Return value</span></span>

<span data-ttu-id="07843-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="07843-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="07843-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="07843-111">Remarks</span></span>

<span data-ttu-id="07843-112">As coordenadas de retângulo estão em unidades HIMETRIC.</span><span class="sxs-lookup"><span data-stu-id="07843-112">The rectangle coordinates are in HIMETRIC units.</span></span>

<span data-ttu-id="07843-113">Se as duas áreas não se interseccionarem, o [**IAnalysisRegion**](ianalysisregion.md) não será alterado.</span><span class="sxs-lookup"><span data-stu-id="07843-113">If the two areas do not intersect, the [**IAnalysisRegion**](ianalysisregion.md) is unchanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="07843-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07843-114">Requirements</span></span>



| <span data-ttu-id="07843-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="07843-115">Requirement</span></span> | <span data-ttu-id="07843-116">Valor</span><span class="sxs-lookup"><span data-stu-id="07843-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07843-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="07843-117">Minimum supported client</span></span><br/> | <span data-ttu-id="07843-118">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="07843-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="07843-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="07843-119">Minimum supported server</span></span><br/> | <span data-ttu-id="07843-120">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="07843-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="07843-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="07843-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="07843-122"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="07843-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="07843-123">DLL</span><span class="sxs-lookup"><span data-stu-id="07843-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07843-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07843-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="07843-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="07843-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07843-126">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="07843-126">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="07843-127">**Método IAnalysisRegion:: ExcludeRegion**</span><span class="sxs-lookup"><span data-stu-id="07843-127">**IAnalysisRegion::ExcludeRegion Method**</span></span>](ianalysisregion-excluderegion.md)
</dt> <dt>

[<span data-ttu-id="07843-128">**Método IAnalysisRegion:: IntersectRectangle**</span><span class="sxs-lookup"><span data-stu-id="07843-128">**IAnalysisRegion::IntersectRectangle Method**</span></span>](ianalysisregion-intersectrectangle.md)
</dt> <dt>

[<span data-ttu-id="07843-129">**Método IAnalysisRegion:: IntersectRegion**</span><span class="sxs-lookup"><span data-stu-id="07843-129">**IAnalysisRegion::IntersectRegion Method**</span></span>](ianalysisregion-intersectregion.md)
</dt> <dt>

[<span data-ttu-id="07843-130">**Método IAnalysisRegion:: UnionRectangle**</span><span class="sxs-lookup"><span data-stu-id="07843-130">**IAnalysisRegion::UnionRectangle Method**</span></span>](ianalysisregion-unionrectangle.md)
</dt> <dt>

[<span data-ttu-id="07843-131">**Método IAnalysisRegion:: UnionRegion**</span><span class="sxs-lookup"><span data-stu-id="07843-131">**IAnalysisRegion::UnionRegion Method**</span></span>](ianalysisregion-unionregion.md)
</dt> <dt>

[<span data-ttu-id="07843-132">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="07843-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




