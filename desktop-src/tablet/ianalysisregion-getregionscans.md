---
description: Recupera uma matriz de retângulos que define a área do IAnalysisRegion.
ms.assetid: 40de4c27-4b3b-4db3-af08-cb53e638db6b
title: 'Método IAnalysisRegion:: GetRegionScans (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.GetRegionScans
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6cb8db60b5818f5bc2bc38892912e9ec40af1eb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105779508"
---
# <a name="ianalysisregiongetregionscans-method"></a><span data-ttu-id="128cd-103">Método IAnalysisRegion:: GetRegionScans</span><span class="sxs-lookup"><span data-stu-id="128cd-103">IAnalysisRegion::GetRegionScans method</span></span>

<span data-ttu-id="128cd-104">Recupera uma matriz de retângulos que define a área do [**IAnalysisRegion**](ianalysisregion.md).</span><span class="sxs-lookup"><span data-stu-id="128cd-104">Retrieves an array of rectangles that defines the area of the [**IAnalysisRegion**](ianalysisregion.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="128cd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="128cd-105">Syntax</span></span>


```C++
HRESULT GetRegionScans(
  [out] ULONG *pulCount,
  [out] RECT  **pRegionScans
);
```



## <a name="parameters"></a><span data-ttu-id="128cd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="128cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="128cd-107">*pulCount* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="128cd-107">*pulCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="128cd-108">O número de retângulos retornados em *pRegionScans*.</span><span class="sxs-lookup"><span data-stu-id="128cd-108">The number of rectangles returned in *pRegionScans*.</span></span>

</dd> <dt>

<span data-ttu-id="128cd-109">*pRegionScans* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="128cd-109">*pRegionScans* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="128cd-110">Um ponteiro para uma matriz de retângulos que define a área do [**IAnalysisRegion**](ianalysisregion.md).</span><span class="sxs-lookup"><span data-stu-id="128cd-110">A pointer to an array of rectangles that defines the area of the [**IAnalysisRegion**](ianalysisregion.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="128cd-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="128cd-111">Return value</span></span>

<span data-ttu-id="128cd-112">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="128cd-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="128cd-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="128cd-113">Remarks</span></span>

<span data-ttu-id="128cd-114">Se *pRegionScans* for passado como **NULL**, o método **GetRegionScans** retornará **S \_ OK** e o número de retângulos será retornado em *pulCount*.</span><span class="sxs-lookup"><span data-stu-id="128cd-114">If *pRegionScans* is passed as **NULL**, the **GetRegionScans** method returns **S\_OK** and the number of rectangles is returned in *pulCount*.</span></span>

> [!Caution]  
> <span data-ttu-id="128cd-115">Para evitar um vazamento de memória, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar a memória do \* *pRegionScans* quando você não precisar mais das informações.</span><span class="sxs-lookup"><span data-stu-id="128cd-115">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**pRegionScans* when you no longer need the information.</span></span>

 

<span data-ttu-id="128cd-116">Os limites dos retângulos estão em coordenadas de espaço de tinta.</span><span class="sxs-lookup"><span data-stu-id="128cd-116">The bounds of the rectangles are in ink-space coordinates.</span></span>

<span data-ttu-id="128cd-117">A União dos retângulos retornados representa a área do [**IAnalysisRegion**](ianalysisregion.md).</span><span class="sxs-lookup"><span data-stu-id="128cd-117">The union of the returned rectangles represents the area of the [**IAnalysisRegion**](ianalysisregion.md).</span></span>

## <a name="examples"></a><span data-ttu-id="128cd-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="128cd-118">Examples</span></span>

<span data-ttu-id="128cd-119">O exemplo a seguir mostra como obter os retângulos que definem a área do [**IAnalysisRegion**](ianalysisregion.md) `region` e como obter apenas o número de retângulos.</span><span class="sxs-lookup"><span data-stu-id="128cd-119">The following example shows how to get the rectangles that define the area of the [**IAnalysisRegion**](ianalysisregion.md), `region` and how to get only the number of rectangles.</span></span>


```C++
// Get the count and the rectangles.
ULONG count = 0;
RECT* rects = 0;
region->GetRegionScans(&count, &rects);

// Use rects

::CoTaskMemFree(rects);

// GetRegionScans just gets the count and returns S_OK
ULONG number = 0;
region->GetRegionScans(&number, NULL); 
```



## <a name="requirements"></a><span data-ttu-id="128cd-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="128cd-120">Requirements</span></span>



| <span data-ttu-id="128cd-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="128cd-121">Requirement</span></span> | <span data-ttu-id="128cd-122">Valor</span><span class="sxs-lookup"><span data-stu-id="128cd-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="128cd-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="128cd-123">Minimum supported client</span></span><br/> | <span data-ttu-id="128cd-124">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="128cd-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="128cd-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="128cd-125">Minimum supported server</span></span><br/> | <span data-ttu-id="128cd-126">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="128cd-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="128cd-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="128cd-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="128cd-128"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="128cd-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="128cd-129">DLL</span><span class="sxs-lookup"><span data-stu-id="128cd-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="128cd-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="128cd-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="128cd-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="128cd-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="128cd-132">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="128cd-132">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="128cd-133">**Método IAnalysisRegion:: GetBounds**</span><span class="sxs-lookup"><span data-stu-id="128cd-133">**IAnalysisRegion::GetBounds Method**</span></span>](ianalysisregion-getbounds.md)
</dt> <dt>

[<span data-ttu-id="128cd-134">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="128cd-134">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

