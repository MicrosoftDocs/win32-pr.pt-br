---
description: Determina se a área do IAnalysisRegion intersecciona com o retângulo especificado.
ms.assetid: 683c3ad8-0236-474e-a16d-6164c2244cfb
title: 'Método IAnalysisRegion:: IntersectsWith (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IntersectsWith
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 99ff1ce8d3039b04d83f9cdd5c1d6aebe00be407
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501822"
---
# <a name="ianalysisregionintersectswith-method"></a><span data-ttu-id="c3616-103">Método IAnalysisRegion:: IntersectsWith</span><span class="sxs-lookup"><span data-stu-id="c3616-103">IAnalysisRegion::IntersectsWith method</span></span>

<span data-ttu-id="c3616-104">Determina se a área do [**IAnalysisRegion**](ianalysisregion.md) intersecciona com o retângulo especificado.</span><span class="sxs-lookup"><span data-stu-id="c3616-104">Determines whether the area of the [**IAnalysisRegion**](ianalysisregion.md) intersects with the specified rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3616-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c3616-105">Syntax</span></span>


```C++
HRESULT IntersectsWith(
  [in]  RECT         *pRectangle,
  [out] VARIANT_BOOL *pfIsIntersecting
);
```



## <a name="parameters"></a><span data-ttu-id="c3616-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c3616-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3616-107">*pRectangle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c3616-107">*pRectangle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3616-108">Um ponteiro para o retângulo com o qual comparar, em coordenadas de espaço de tinta.</span><span class="sxs-lookup"><span data-stu-id="c3616-108">A pointer to the rectangle with which to compare, in ink-space coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="c3616-109">*pfIsIntersecting* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c3616-109">*pfIsIntersecting* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c3616-110">**Variante \_ TRUE** se a área do [**IAnalysisRegion**](ianalysisregion.md) Interseccionar com o retângulo especificado; caso contrário, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="c3616-110">**VARIANT\_TRUE** if the area of the [**IAnalysisRegion**](ianalysisregion.md) intersects with the specified rectangle; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3616-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c3616-111">Return value</span></span>

<span data-ttu-id="c3616-112">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="c3616-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c3616-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="c3616-113">Remarks</span></span>

<span data-ttu-id="c3616-114">A comparação está em coordenadas de espaço de tinta.</span><span class="sxs-lookup"><span data-stu-id="c3616-114">The comparison is in ink-space coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3616-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3616-115">Requirements</span></span>



| <span data-ttu-id="c3616-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3616-116">Requirement</span></span> | <span data-ttu-id="c3616-117">Valor</span><span class="sxs-lookup"><span data-stu-id="c3616-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3616-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c3616-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c3616-119">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="c3616-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c3616-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c3616-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c3616-121">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="c3616-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="c3616-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c3616-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3616-123"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="c3616-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c3616-124">DLL</span><span class="sxs-lookup"><span data-stu-id="c3616-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3616-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3616-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="c3616-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="c3616-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3616-127">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="c3616-127">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="c3616-128">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="c3616-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




