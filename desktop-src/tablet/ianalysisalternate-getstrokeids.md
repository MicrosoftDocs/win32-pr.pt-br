---
description: Retorna os identificadores de traço associados a este IAnalysisAlternate.
ms.assetid: 495d485f-0d16-4085-9213-cc55f3f259f0
title: 'Método IAnalysisAlternate:: GetStrokeIds (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate.GetStrokeIds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 80882a83e9a0fa9bf973990a689e2abf1a52a870
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827195"
---
# <a name="ianalysisalternategetstrokeids-method"></a><span data-ttu-id="baa19-103">Método IAnalysisAlternate:: GetStrokeIds</span><span class="sxs-lookup"><span data-stu-id="baa19-103">IAnalysisAlternate::GetStrokeIds method</span></span>

<span data-ttu-id="baa19-104">Retorna os identificadores de traço associados a este [**IAnalysisAlternate**](ianalysisalternate.md).</span><span class="sxs-lookup"><span data-stu-id="baa19-104">Returns the stroke identifiers that are associated with this [**IAnalysisAlternate**](ianalysisalternate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="baa19-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="baa19-105">Syntax</span></span>


```C++
HRESULT GetStrokeIds(
  [in, out] ULONG *pulStrokeIdsCount,
  [out]     LONG  **pplStrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="baa19-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="baa19-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="baa19-107">*pulStrokeIdsCount* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="baa19-107">*pulStrokeIdsCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="baa19-108">Um ponteiro para um **ULONG** que é definido como o número de identificadores de traço associados a este [**IAnalysisAlternate**](ianalysisalternate.md).</span><span class="sxs-lookup"><span data-stu-id="baa19-108">A pointer to a **ULONG** that is set to the number of stroke identifiers associated with this [**IAnalysisAlternate**](ianalysisalternate.md).</span></span>

</dd> <dt>

<span data-ttu-id="baa19-109">*pplStrokeIds* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="baa19-109">*pplStrokeIds* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="baa19-110">\[out, tamanho \_ é ( \* *PULSTROKEIDSCOUNT* \* sizeof (Long))\]</span><span class="sxs-lookup"><span data-stu-id="baa19-110">\[out, size\_is(\**pulStrokeIdsCount* \* sizeof(LONG))\]</span></span>

<span data-ttu-id="baa19-111">Uma matriz de *pulStrokeIdsCount* de comprimento **longa** que é definida para os identificadores de traço associados a esse [**IAnalysisAlternate**](ianalysisalternate.md).</span><span class="sxs-lookup"><span data-stu-id="baa19-111">An array of **LONG** of length *pulStrokeIdsCount* that is set to the stroke identifiers associated with this [**IAnalysisAlternate**](ianalysisalternate.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="baa19-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="baa19-112">Return value</span></span>

<span data-ttu-id="baa19-113">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="baa19-113">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="baa19-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="baa19-114">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="baa19-115">Para evitar um vazamento de memória, use [CoTaskMemFree](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar a memória do \* *pplStrokeIds* quando você não precisar mais das informações.</span><span class="sxs-lookup"><span data-stu-id="baa19-115">To avoid a memory leak, use [CoTaskMemFree](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**pplStrokeIds* when you no longer need the information.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="baa19-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="baa19-116">Requirements</span></span>



| <span data-ttu-id="baa19-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="baa19-117">Requirement</span></span> | <span data-ttu-id="baa19-118">Valor</span><span class="sxs-lookup"><span data-stu-id="baa19-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="baa19-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="baa19-119">Minimum supported client</span></span><br/> | <span data-ttu-id="baa19-120">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="baa19-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="baa19-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="baa19-121">Minimum supported server</span></span><br/> | <span data-ttu-id="baa19-122">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="baa19-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="baa19-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="baa19-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="baa19-124"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="baa19-124"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="baa19-125">DLL</span><span class="sxs-lookup"><span data-stu-id="baa19-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="baa19-126"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="baa19-126"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="baa19-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="baa19-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="baa19-128">**IAnalysisAlternate**</span><span class="sxs-lookup"><span data-stu-id="baa19-128">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="baa19-129">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="baa19-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

