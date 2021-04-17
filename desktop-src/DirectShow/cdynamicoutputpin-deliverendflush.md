---
description: O método DeliverEndFlush solicita o pino de entrada conectado para finalizar uma operação de liberação.
ms.assetid: e37bf06a-6cdc-4f14-bf2e-7a7d7004cff6
title: Método CDynamicOutputPin. DeliverEndFlush (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.DeliverEndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2666681dcd5637a8e919ced2c61d6536663d7b30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748813"
---
# <a name="cdynamicoutputpindeliverendflush-method"></a><span data-ttu-id="46ad3-103">Método CDynamicOutputPin. DeliverEndFlush</span><span class="sxs-lookup"><span data-stu-id="46ad3-103">CDynamicOutputPin.DeliverEndFlush method</span></span>

<span data-ttu-id="46ad3-104">O `DeliverEndFlush` método solicita o PIN de entrada conectado para finalizar uma operação de liberação.</span><span class="sxs-lookup"><span data-stu-id="46ad3-104">The `DeliverEndFlush` method requests the connected input pin to end a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="46ad3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="46ad3-105">Syntax</span></span>


```C++
HRESULT DeliverEndFlush();
```



## <a name="parameters"></a><span data-ttu-id="46ad3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="46ad3-106">Parameters</span></span>

<span data-ttu-id="46ad3-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="46ad3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="46ad3-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="46ad3-108">Return value</span></span>

<span data-ttu-id="46ad3-109">Retorna S \_ OK se bem-sucedido ou um valor **HRESULT** que indica a causa da falha.</span><span class="sxs-lookup"><span data-stu-id="46ad3-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="46ad3-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="46ad3-110">Remarks</span></span>

<span data-ttu-id="46ad3-111">Esse método substitui o método [**CBaseOutputPin::D eliverendflush**](cbaseoutputpin-deliverendflush.md) .</span><span class="sxs-lookup"><span data-stu-id="46ad3-111">This method overrides the [**CBaseOutputPin::DeliverEndFlush**](cbaseoutputpin-deliverendflush.md) method.</span></span> <span data-ttu-id="46ad3-112">Ele redefine o evento [**CDynamicOutputPin:: m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md) .</span><span class="sxs-lookup"><span data-stu-id="46ad3-112">It resets the [**CDynamicOutputPin::m\_hStopEvent**](cdynamicoutputpin-m-hstopevent.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="46ad3-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46ad3-113">Requirements</span></span>



| <span data-ttu-id="46ad3-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="46ad3-114">Requirement</span></span> | <span data-ttu-id="46ad3-115">Valor</span><span class="sxs-lookup"><span data-stu-id="46ad3-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46ad3-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="46ad3-116">Header</span></span><br/>  | <dl> <span data-ttu-id="46ad3-117"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="46ad3-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="46ad3-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="46ad3-118">Library</span></span><br/> | <dl> <span data-ttu-id="46ad3-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="46ad3-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46ad3-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="46ad3-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46ad3-121">**Classe CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="46ad3-121">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




