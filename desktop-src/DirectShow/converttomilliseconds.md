---
description: A função ConvertToMilliseconds converte um tempo de referência em milissegundos.
ms.assetid: fae3baa4-9344-4197-b375-4abe2656e1b7
title: Função ConvertToMilliseconds (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertToMilliseconds
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 066f50856824a9bc7b5bbb8c4918c7cbfe5b9da5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750471"
---
# <a name="converttomilliseconds-function"></a><span data-ttu-id="5b509-103">Função ConvertToMilliseconds</span><span class="sxs-lookup"><span data-stu-id="5b509-103">ConvertToMilliseconds function</span></span>

<span data-ttu-id="5b509-104">A `ConvertToMilliseconds` função converte um tempo de referência em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="5b509-104">The `ConvertToMilliseconds` function converts a reference time to milliseconds.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b509-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5b509-105">Syntax</span></span>


```C++
LONGLONG ConvertToMilliseconds(
   const REFERENCE_TIME &RT
);
```



## <a name="parameters"></a><span data-ttu-id="5b509-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5b509-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b509-107">*RT* \[ referência\]</span><span class="sxs-lookup"><span data-stu-id="5b509-107">*RT* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="5b509-108">Tempo de referência, em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="5b509-108">Reference time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b509-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5b509-109">Return value</span></span>

<span data-ttu-id="5b509-110">Retorna o tempo de referência convertido em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="5b509-110">Returns the reference time converted to milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b509-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b509-111">Requirements</span></span>



| <span data-ttu-id="5b509-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b509-112">Requirement</span></span> | <span data-ttu-id="5b509-113">Valor</span><span class="sxs-lookup"><span data-stu-id="5b509-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b509-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5b509-114">Header</span></span><br/>  | <dl> <span data-ttu-id="5b509-115"><dt>Refclock. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5b509-115"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5b509-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5b509-116">Library</span></span><br/> | <dl> <span data-ttu-id="5b509-117"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="5b509-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b509-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="5b509-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b509-119">**Classe CBaseReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="5b509-119">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




