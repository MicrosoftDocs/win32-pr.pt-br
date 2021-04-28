---
description: Método CDynamicOutputPin. DeliverEndFlush – o método DeliverEndFlush solicita o pino de entrada conectado para finalizar uma operação de liberação.
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
ms.openlocfilehash: c8b6952ff50dc2266655c58bd5c2e1ed13105598
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095704"
---
# <a name="cdynamicoutputpindeliverendflush-method"></a><span data-ttu-id="dda43-103">Método CDynamicOutputPin. DeliverEndFlush</span><span class="sxs-lookup"><span data-stu-id="dda43-103">CDynamicOutputPin.DeliverEndFlush method</span></span>

<span data-ttu-id="dda43-104">O `DeliverEndFlush` método solicita o PIN de entrada conectado para finalizar uma operação de liberação.</span><span class="sxs-lookup"><span data-stu-id="dda43-104">The `DeliverEndFlush` method requests the connected input pin to end a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="dda43-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dda43-105">Syntax</span></span>


```C++
HRESULT DeliverEndFlush();
```



## <a name="parameters"></a><span data-ttu-id="dda43-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dda43-106">Parameters</span></span>

<span data-ttu-id="dda43-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="dda43-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dda43-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="dda43-108">Return value</span></span>

<span data-ttu-id="dda43-109">Retorna S \_ OK se bem-sucedido ou um valor **HRESULT** que indica a causa da falha.</span><span class="sxs-lookup"><span data-stu-id="dda43-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="dda43-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="dda43-110">Remarks</span></span>

<span data-ttu-id="dda43-111">Esse método substitui o método [**CBaseOutputPin::D eliverendflush**](cbaseoutputpin-deliverendflush.md) .</span><span class="sxs-lookup"><span data-stu-id="dda43-111">This method overrides the [**CBaseOutputPin::DeliverEndFlush**](cbaseoutputpin-deliverendflush.md) method.</span></span> <span data-ttu-id="dda43-112">Ele redefine o evento [**CDynamicOutputPin:: m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md) .</span><span class="sxs-lookup"><span data-stu-id="dda43-112">It resets the [**CDynamicOutputPin::m\_hStopEvent**](cdynamicoutputpin-m-hstopevent.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="dda43-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dda43-113">Requirements</span></span>



| <span data-ttu-id="dda43-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="dda43-114">Requirement</span></span> | <span data-ttu-id="dda43-115">Valor</span><span class="sxs-lookup"><span data-stu-id="dda43-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dda43-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dda43-116">Header</span></span><br/>  | <dl> <span data-ttu-id="dda43-117"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dda43-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="dda43-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dda43-118">Library</span></span><br/> | <dl> <span data-ttu-id="dda43-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="dda43-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dda43-120">Consulte também</span><span class="sxs-lookup"><span data-stu-id="dda43-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dda43-121">**Classe CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="dda43-121">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




