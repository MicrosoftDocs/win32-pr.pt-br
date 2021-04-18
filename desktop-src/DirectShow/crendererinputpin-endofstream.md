---
description: 'O método EndOfStream notifica o PIN de que nenhum dado adicional é esperado. Esse método substitui o método CBasePin:: EndOfStream.'
ms.assetid: fb5fd8bb-47be-4df6-b837-2c5ff4347478
title: Método CRendererInputPin. EndOfStream (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6a8f495c87a86efc9d5625868c7f8fd4afd6ff1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756610"
---
# <a name="crendererinputpinendofstream-method"></a><span data-ttu-id="9859d-104">Método CRendererInputPin. EndOfStream</span><span class="sxs-lookup"><span data-stu-id="9859d-104">CRendererInputPin.EndOfStream method</span></span>

<span data-ttu-id="9859d-105">O `EndOfStream` método notifica o PIN de que nenhum dado adicional é esperado.</span><span class="sxs-lookup"><span data-stu-id="9859d-105">The `EndOfStream` method notifies the pin that no additional data is expected.</span></span> <span data-ttu-id="9859d-106">Esse método substitui o método [**CBasePin:: EndOfStream**](cbasepin-endofstream.md) .</span><span class="sxs-lookup"><span data-stu-id="9859d-106">This method overrides the [**CBasePin::EndOfStream**](cbasepin-endofstream.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9859d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9859d-107">Syntax</span></span>


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="9859d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9859d-108">Parameters</span></span>

<span data-ttu-id="9859d-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="9859d-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9859d-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9859d-110">Return value</span></span>

<span data-ttu-id="9859d-111">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9859d-111">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="9859d-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9859d-112">Requirements</span></span>



| <span data-ttu-id="9859d-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="9859d-113">Requirement</span></span> | <span data-ttu-id="9859d-114">Valor</span><span class="sxs-lookup"><span data-stu-id="9859d-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9859d-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9859d-115">Header</span></span><br/>  | <dl> <span data-ttu-id="9859d-116"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9859d-116"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9859d-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9859d-117">Library</span></span><br/> | <dl> <span data-ttu-id="9859d-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="9859d-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9859d-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="9859d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9859d-120">**Classe CRendererInputPin**</span><span class="sxs-lookup"><span data-stu-id="9859d-120">**CRendererInputPin Class**</span></span>](crendererinputpin.md)
</dt> </dl>

 

 




