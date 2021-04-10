---
description: Recupera um valor que indica se IAnalysisRegion representa uma região infinita.
ms.assetid: b84ec9ec-42d0-4d03-b78b-433e55d04897
title: 'Método IAnalysisRegion:: isFinite (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IsInfinite
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4f7d284c043f38a681b969f72d751f9acaa954c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164558"
---
# <a name="ianalysisregionisinfinite-method"></a><span data-ttu-id="64fae-103">Método IAnalysisRegion:: isFinite</span><span class="sxs-lookup"><span data-stu-id="64fae-103">IAnalysisRegion::IsInfinite method</span></span>

<span data-ttu-id="64fae-104">Recupera um valor que indica se [**IAnalysisRegion**](ianalysisregion.md) representa uma região infinita.</span><span class="sxs-lookup"><span data-stu-id="64fae-104">Retrieves a value indicating whether the [**IAnalysisRegion**](ianalysisregion.md) represents an infinite region.</span></span>

## <a name="syntax"></a><span data-ttu-id="64fae-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="64fae-105">Syntax</span></span>


```C++
HRESULT IsInfinite(
  [out] VARIANT_BOOL *pfIsInfinite
);
```



## <a name="parameters"></a><span data-ttu-id="64fae-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="64fae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64fae-107">*pfIsInfinite* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="64fae-107">*pfIsInfinite* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="64fae-108">**Variante \_ TRUE** se a região representada for infinita; caso contrário, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="64fae-108">**VARIANT\_TRUE** if the represented region is infinite; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64fae-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="64fae-109">Return value</span></span>

<span data-ttu-id="64fae-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="64fae-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="64fae-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64fae-111">Requirements</span></span>



| <span data-ttu-id="64fae-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="64fae-112">Requirement</span></span> | <span data-ttu-id="64fae-113">Valor</span><span class="sxs-lookup"><span data-stu-id="64fae-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64fae-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="64fae-114">Minimum supported client</span></span><br/> | <span data-ttu-id="64fae-115">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="64fae-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="64fae-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="64fae-116">Minimum supported server</span></span><br/> | <span data-ttu-id="64fae-117">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="64fae-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="64fae-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="64fae-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="64fae-119"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="64fae-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="64fae-120">DLL</span><span class="sxs-lookup"><span data-stu-id="64fae-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64fae-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64fae-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="64fae-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="64fae-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64fae-123">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="64fae-123">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="64fae-124">**Método IAnalysisRegion:: IsEmpty**</span><span class="sxs-lookup"><span data-stu-id="64fae-124">**IAnalysisRegion::IsEmpty Method**</span></span>](ianalysisregion-isempty.md)
</dt> <dt>

[<span data-ttu-id="64fae-125">**Método IAnalysisRegion:: MakeEmpty**</span><span class="sxs-lookup"><span data-stu-id="64fae-125">**IAnalysisRegion::MakeEmpty Method**</span></span>](ianalysisregion-makeempty.md)
</dt> <dt>

[<span data-ttu-id="64fae-126">**Método IAnalysisRegion:: MakeInfinite**</span><span class="sxs-lookup"><span data-stu-id="64fae-126">**IAnalysisRegion::MakeInfinite Method**</span></span>](ianalysisregion-makeinfinite.md)
</dt> <dt>

[<span data-ttu-id="64fae-127">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="64fae-127">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




