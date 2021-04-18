---
description: Saiba mais sobre o método de Construtor CMediaPosition. CMediaPosition (Ctlutil. h). Este método usa os parâmetros ' pName ', ' pUnk ' e ' PHR '.
ms.assetid: 4074f513-d1e7-4311-8732-4d755e621e55
title: Construtor CMediaPosition. CMediaPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.CMediaPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cb9d86a2403cd0e2e71130b51cdb87bad15c4e95
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "105757032"
---
# <a name="cmediapositioncmediaposition-constructor-ctlutilh---pname-punk-phr-parameters"></a><span data-ttu-id="8033a-104">Construtor CMediaPosition. CMediaPosition (Ctlutil. h)-pName, pUnk, PHR parâmetros</span><span class="sxs-lookup"><span data-stu-id="8033a-104">CMediaPosition.CMediaPosition constructor (Ctlutil.h) - pName, pUnk, phr parameters</span></span>

<span data-ttu-id="8033a-105">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="8033a-105">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8033a-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8033a-106">Syntax</span></span>


```C++
CMediaPosition(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="8033a-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8033a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8033a-108">*pName*</span><span class="sxs-lookup"><span data-stu-id="8033a-108">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="8033a-109">Ponteiro para o nome do objeto, para fins de depuração.</span><span class="sxs-lookup"><span data-stu-id="8033a-109">Pointer to the name of the object, for debugging purposes.</span></span> <span data-ttu-id="8033a-110">Aloque esse parâmetro na memória estática.</span><span class="sxs-lookup"><span data-stu-id="8033a-110">Allocate this parameter in static memory.</span></span>

</dd> <dt>

<span data-ttu-id="8033a-111">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="8033a-111">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="8033a-112">Ponteiro para o proprietário deste objeto ou **NULL** se o objeto não for agregado.</span><span class="sxs-lookup"><span data-stu-id="8033a-112">Pointer to the owner of this object, or **NULL** if the object is not aggregated.</span></span>

</dd> <dt>

<span data-ttu-id="8033a-113">*phr*</span><span class="sxs-lookup"><span data-stu-id="8033a-113">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="8033a-114">Ponteiro para um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8033a-114">Pointer to an **HRESULT** value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8033a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8033a-115">Requirements</span></span>

| <span data-ttu-id="8033a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8033a-116">Requirement</span></span> | <span data-ttu-id="8033a-117">Valor</span><span class="sxs-lookup"><span data-stu-id="8033a-117">Value</span></span> |
|-|-|
| <span data-ttu-id="8033a-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8033a-118">Header</span></span> | <span data-ttu-id="8033a-119">Ctlutil. h (incluir fluxos. h)</span><span class="sxs-lookup"><span data-stu-id="8033a-119">Ctlutil.h (include Streams.h)</span></span> |
| <span data-ttu-id="8033a-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8033a-120">Library</span></span>| <span data-ttu-id="8033a-121">Strmbase. lib (compilações de varejo); Strmbasd. lib (compilações de depuração)</span><span class="sxs-lookup"><span data-stu-id="8033a-121">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="8033a-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="8033a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8033a-123">**Classe CMediaPosition**</span><span class="sxs-lookup"><span data-stu-id="8033a-123">**CMediaPosition Class**</span></span>](cmediaposition.md)
</dt> </dl>

 

 




