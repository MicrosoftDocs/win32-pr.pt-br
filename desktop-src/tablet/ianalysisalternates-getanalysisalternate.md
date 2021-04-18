---
description: Recupera o objeto IAnalysisAlternate no índice especificado dentro da coleção.
ms.assetid: d927e2f1-ca21-415d-90ad-d1ded575fcb7
title: 'Método IAnalysisAlternates:: GetAnalysisAlternate (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternates.GetAnalysisAlternate
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 122bccc4985ed7ba5617e9d373ecdf3d0c84dac2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788838"
---
# <a name="ianalysisalternatesgetanalysisalternate-method"></a><span data-ttu-id="08338-103">Método IAnalysisAlternates:: GetAnalysisAlternate</span><span class="sxs-lookup"><span data-stu-id="08338-103">IAnalysisAlternates::GetAnalysisAlternate method</span></span>

<span data-ttu-id="08338-104">Recupera o objeto [**IAnalysisAlternate**](ianalysisalternate.md) no índice especificado dentro da coleção.</span><span class="sxs-lookup"><span data-stu-id="08338-104">Retrieves the [**IAnalysisAlternate**](ianalysisalternate.md) object at the specified index within the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="08338-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="08338-105">Syntax</span></span>


```C++
HRESULT GetAnalysisAlternate(
  [in]  ULONG              ulIndex,
  [out] IAnalysisAlternate **ppAlternate
);
```



## <a name="parameters"></a><span data-ttu-id="08338-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="08338-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08338-107">*ulIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="08338-107">*ulIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08338-108">O índice de base zero do objeto [**IAnalysisAlternate**](ianalysisalternate.md) a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="08338-108">The zero-based index of the [**IAnalysisAlternate**](ianalysisalternate.md) object to get.</span></span>

</dd> <dt>

<span data-ttu-id="08338-109">*ppAlternate* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="08338-109">*ppAlternate* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="08338-110">Um ponteiro para o objeto [**IAnalysisAlternate**](ianalysisalternate.md) no índice especificado dentro da coleção.</span><span class="sxs-lookup"><span data-stu-id="08338-110">A pointer to the [**IAnalysisAlternate**](ianalysisalternate.md) object at the specified index within the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08338-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="08338-111">Return value</span></span>

<span data-ttu-id="08338-112">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="08338-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="08338-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="08338-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="08338-114">Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em \* *ppAlternate* quando você não precisar mais usar a alternativa de análise.</span><span class="sxs-lookup"><span data-stu-id="08338-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppAlternate* when you no longer need to use the analysis alternate.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="08338-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08338-115">Requirements</span></span>



| <span data-ttu-id="08338-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="08338-116">Requirement</span></span> | <span data-ttu-id="08338-117">Valor</span><span class="sxs-lookup"><span data-stu-id="08338-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08338-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="08338-118">Minimum supported client</span></span><br/> | <span data-ttu-id="08338-119">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="08338-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="08338-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="08338-120">Minimum supported server</span></span><br/> | <span data-ttu-id="08338-121">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="08338-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="08338-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="08338-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="08338-123"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="08338-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="08338-124">DLL</span><span class="sxs-lookup"><span data-stu-id="08338-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08338-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08338-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="08338-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="08338-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08338-127">**IAnalysisAlternates**</span><span class="sxs-lookup"><span data-stu-id="08338-127">**IAnalysisAlternates**</span></span>](ianalysisalternates.md)
</dt> <dt>

[<span data-ttu-id="08338-128">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="08338-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

