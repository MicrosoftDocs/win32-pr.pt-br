---
description: Recupera um valor que indica se IAnalysisRegion representa uma região vazia.
ms.assetid: 3a536b01-e7ee-4103-88c4-d83377ea9fdb
title: 'Método IAnalysisRegion:: IsEmpty (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IsEmpty
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: c1fb4ebbe487119c65f153f78e192de38e6393fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105791072"
---
# <a name="ianalysisregionisempty-method"></a><span data-ttu-id="75184-103">Método IAnalysisRegion:: IsEmpty</span><span class="sxs-lookup"><span data-stu-id="75184-103">IAnalysisRegion::IsEmpty method</span></span>

<span data-ttu-id="75184-104">Recupera um valor que indica se [**IAnalysisRegion**](ianalysisregion.md) representa uma região vazia.</span><span class="sxs-lookup"><span data-stu-id="75184-104">Retrieves a value indicating whether the [**IAnalysisRegion**](ianalysisregion.md) represents an empty region.</span></span>

## <a name="syntax"></a><span data-ttu-id="75184-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="75184-105">Syntax</span></span>


```C++
HRESULT IsEmpty(
  [out] VARIANT_BOOL *pfIsEmpty
);
```



## <a name="parameters"></a><span data-ttu-id="75184-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="75184-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75184-107">*pfIsEmpty* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="75184-107">*pfIsEmpty* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="75184-108">**Variante \_ TRUE** se a região representada estiver vazia; caso contrário, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="75184-108">**VARIANT\_TRUE** if the represented region is empty; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75184-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="75184-109">Return value</span></span>

<span data-ttu-id="75184-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="75184-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="75184-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75184-111">Requirements</span></span>



| <span data-ttu-id="75184-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="75184-112">Requirement</span></span> | <span data-ttu-id="75184-113">Valor</span><span class="sxs-lookup"><span data-stu-id="75184-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75184-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="75184-114">Minimum supported client</span></span><br/> | <span data-ttu-id="75184-115">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="75184-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="75184-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="75184-116">Minimum supported server</span></span><br/> | <span data-ttu-id="75184-117">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="75184-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="75184-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="75184-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="75184-119"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="75184-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="75184-120">DLL</span><span class="sxs-lookup"><span data-stu-id="75184-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75184-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75184-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="75184-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="75184-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75184-123">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="75184-123">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="75184-124">**Método IAnalysisRegion:: isFinite**</span><span class="sxs-lookup"><span data-stu-id="75184-124">**IAnalysisRegion::IsInfinite Method**</span></span>](ianalysisregion-isinfinite.md)
</dt> <dt>

[<span data-ttu-id="75184-125">**Método IAnalysisRegion:: MakeEmpty**</span><span class="sxs-lookup"><span data-stu-id="75184-125">**IAnalysisRegion::MakeEmpty Method**</span></span>](ianalysisregion-makeempty.md)
</dt> <dt>

[<span data-ttu-id="75184-126">**Método IAnalysisRegion:: MakeInfinite**</span><span class="sxs-lookup"><span data-stu-id="75184-126">**IAnalysisRegion::MakeInfinite Method**</span></span>](ianalysisregion-makeinfinite.md)
</dt> <dt>

[<span data-ttu-id="75184-127">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="75184-127">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




