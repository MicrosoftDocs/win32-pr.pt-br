---
description: Saiba mais sobre o método de Construtor CMediaPosition. CMediaPosition (Ctlutil. h). Este método usa os parâmetros ' pName ' e ' pUnk '.
ms.assetid: 18a7785c-30c6-43b8-9a41-542a8424522c
title: Construtor CMediaPosition. CMediaPosition (Ctlutil. h)-pName, pUnk parâmetros
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
ms.openlocfilehash: e65f034e5f8857b21bc706bce45aa74c3c3cf966
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "105771853"
---
# <a name="cmediapositioncmediaposition-constructor-ctlutilh---pname-punk-parameters"></a><span data-ttu-id="0eddf-104">Construtor CMediaPosition. CMediaPosition (Ctlutil. h)-pName, pUnk parâmetros</span><span class="sxs-lookup"><span data-stu-id="0eddf-104">CMediaPosition.CMediaPosition constructor (Ctlutil.h) - pName, pUnk parameters</span></span>

<span data-ttu-id="0eddf-105">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="0eddf-105">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0eddf-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0eddf-106">Syntax</span></span>


```C++
CMediaPosition(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a><span data-ttu-id="0eddf-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0eddf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0eddf-108">*pName*</span><span class="sxs-lookup"><span data-stu-id="0eddf-108">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="0eddf-109">Ponteiro para o nome do objeto, para fins de depuração.</span><span class="sxs-lookup"><span data-stu-id="0eddf-109">Pointer to the name of the object, for debugging purposes.</span></span> <span data-ttu-id="0eddf-110">Aloque esse parâmetro na memória estática.</span><span class="sxs-lookup"><span data-stu-id="0eddf-110">Allocate this parameter in static memory.</span></span>

</dd> <dt>

<span data-ttu-id="0eddf-111">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="0eddf-111">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="0eddf-112">Ponteiro para o proprietário deste objeto ou **NULL** se o objeto não for agregado.</span><span class="sxs-lookup"><span data-stu-id="0eddf-112">Pointer to the owner of this object, or **NULL** if the object is not aggregated.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0eddf-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0eddf-113">Requirements</span></span>

| <span data-ttu-id="0eddf-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0eddf-114">Requirement</span></span> | <span data-ttu-id="0eddf-115">Valor</span><span class="sxs-lookup"><span data-stu-id="0eddf-115">Value</span></span> |
|-|-|
| <span data-ttu-id="0eddf-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0eddf-116">Header</span></span> | <span data-ttu-id="0eddf-117">Ctlutil. h (incluir fluxos. h)</span><span class="sxs-lookup"><span data-stu-id="0eddf-117">Ctlutil.h (include Streams.h)</span></span> |
| <span data-ttu-id="0eddf-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0eddf-118">Library</span></span>| <span data-ttu-id="0eddf-119">Strmbase. lib (compilações de varejo); Strmbasd. lib (compilações de depuração)</span><span class="sxs-lookup"><span data-stu-id="0eddf-119">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="0eddf-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="0eddf-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0eddf-121">**Classe CMediaPosition**</span><span class="sxs-lookup"><span data-stu-id="0eddf-121">**CMediaPosition Class**</span></span>](cmediaposition.md)
</dt> </dl>

 

 




