---
description: Expande a área desta IAnalysisRegion para a área criada por sua união com o retângulo especificado.
ms.assetid: 9b12f509-4f6a-43b0-9639-bef060fd6d50
title: 'Método IAnalysisRegion:: UnionRectangle (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.UnionRectangle
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 3a28a60eae95641225dd9c01791d89a9c38ada82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105790497"
---
# <a name="ianalysisregionunionrectangle-method"></a><span data-ttu-id="df589-103">Método IAnalysisRegion:: UnionRectangle</span><span class="sxs-lookup"><span data-stu-id="df589-103">IAnalysisRegion::UnionRectangle method</span></span>

<span data-ttu-id="df589-104">Expande a área desta [**IAnalysisRegion**](ianalysisregion.md) para a área criada por sua união com o retângulo especificado.</span><span class="sxs-lookup"><span data-stu-id="df589-104">Expands the area of this [**IAnalysisRegion**](ianalysisregion.md) to the area created by its union with the specified rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="df589-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="df589-105">Syntax</span></span>


```C++
HRESULT UnionRectangle(
  [in] RECT *pRectangle
);
```



## <a name="parameters"></a><span data-ttu-id="df589-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="df589-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df589-107">*pRectangle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="df589-107">*pRectangle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df589-108">Um ponteiro para o retângulo com o qual combinar, em coordenadas de espaço de tinta.</span><span class="sxs-lookup"><span data-stu-id="df589-108">A pointer to the rectangle with which to combine, in ink-space coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df589-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="df589-109">Return value</span></span>

<span data-ttu-id="df589-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="df589-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="df589-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="df589-111">Remarks</span></span>

<span data-ttu-id="df589-112">As coordenadas de retângulo estão em unidades HIMETRIC.</span><span class="sxs-lookup"><span data-stu-id="df589-112">The rectangle coordinates are in HIMETRIC units.</span></span>

<span data-ttu-id="df589-113">Se qualquer área for infinita, a nova área também será infinita.</span><span class="sxs-lookup"><span data-stu-id="df589-113">If either area is infinite, the new area is also infinite.</span></span>

## <a name="requirements"></a><span data-ttu-id="df589-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df589-114">Requirements</span></span>



| <span data-ttu-id="df589-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="df589-115">Requirement</span></span> | <span data-ttu-id="df589-116">Valor</span><span class="sxs-lookup"><span data-stu-id="df589-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df589-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="df589-117">Minimum supported client</span></span><br/> | <span data-ttu-id="df589-118">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="df589-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="df589-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="df589-119">Minimum supported server</span></span><br/> | <span data-ttu-id="df589-120">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="df589-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="df589-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="df589-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="df589-122"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="df589-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="df589-123">DLL</span><span class="sxs-lookup"><span data-stu-id="df589-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df589-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df589-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="df589-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="df589-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df589-126">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="df589-126">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="df589-127">**IAnalysisRegion::ExcludeRectangle**</span><span class="sxs-lookup"><span data-stu-id="df589-127">**IAnalysisRegion::ExcludeRectangle**</span></span>](ianalysisregion-excluderectangle.md)
</dt> <dt>

[<span data-ttu-id="df589-128">**Método IAnalysisRegion:: ExcludeRegion**</span><span class="sxs-lookup"><span data-stu-id="df589-128">**IAnalysisRegion::ExcludeRegion Method**</span></span>](ianalysisregion-excluderegion.md)
</dt> <dt>

[<span data-ttu-id="df589-129">**Método IAnalysisRegion:: IntersectRectangle**</span><span class="sxs-lookup"><span data-stu-id="df589-129">**IAnalysisRegion::IntersectRectangle Method**</span></span>](ianalysisregion-intersectrectangle.md)
</dt> <dt>

[<span data-ttu-id="df589-130">**Método IAnalysisRegion:: IntersectRegion**</span><span class="sxs-lookup"><span data-stu-id="df589-130">**IAnalysisRegion::IntersectRegion Method**</span></span>](ianalysisregion-intersectregion.md)
</dt> <dt>

[<span data-ttu-id="df589-131">**Método IAnalysisRegion:: UnionRegion**</span><span class="sxs-lookup"><span data-stu-id="df589-131">**IAnalysisRegion::UnionRegion Method**</span></span>](ianalysisregion-unionregion.md)
</dt> <dt>

[<span data-ttu-id="df589-132">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="df589-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




