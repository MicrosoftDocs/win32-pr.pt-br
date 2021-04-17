---
description: O método DeliverBeginFlush solicita o pino de entrada conectado para iniciar uma operação de liberação.
ms.assetid: eafc3835-7696-480b-abc8-154938e19b15
title: Método CDynamicOutputPin. DeliverBeginFlush (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.DeliverBeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 242394a327b63fcc901b08f572096bf2f42238b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754540"
---
# <a name="cdynamicoutputpindeliverbeginflush-method"></a><span data-ttu-id="a36aa-103">Método CDynamicOutputPin. DeliverBeginFlush</span><span class="sxs-lookup"><span data-stu-id="a36aa-103">CDynamicOutputPin.DeliverBeginFlush method</span></span>

<span data-ttu-id="a36aa-104">O `DeliverBeginFlush` método solicita o PIN de entrada conectado para iniciar uma operação de liberação.</span><span class="sxs-lookup"><span data-stu-id="a36aa-104">The `DeliverBeginFlush` method requests the connected input pin to begin a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="a36aa-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a36aa-105">Syntax</span></span>


```C++
HRESULT DeliverBeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="a36aa-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a36aa-106">Parameters</span></span>

<span data-ttu-id="a36aa-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="a36aa-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a36aa-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a36aa-108">Return value</span></span>

<span data-ttu-id="a36aa-109">Retorna S \_ OK se bem-sucedido ou um valor **HRESULT** que indica a causa da falha.</span><span class="sxs-lookup"><span data-stu-id="a36aa-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="a36aa-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="a36aa-110">Remarks</span></span>

<span data-ttu-id="a36aa-111">Esse método substitui o método [**CBaseOutputPin::D eliverbeginflush**](cbaseoutputpin-deliverbeginflush.md) .</span><span class="sxs-lookup"><span data-stu-id="a36aa-111">This method overrides the [**CBaseOutputPin::DeliverBeginFlush**](cbaseoutputpin-deliverbeginflush.md) method.</span></span> <span data-ttu-id="a36aa-112">Ele define o evento [**CDynamicOutputPin:: m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md) .</span><span class="sxs-lookup"><span data-stu-id="a36aa-112">It sets the [**CDynamicOutputPin::m\_hStopEvent**](cdynamicoutputpin-m-hstopevent.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="a36aa-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a36aa-113">Requirements</span></span>



| <span data-ttu-id="a36aa-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a36aa-114">Requirement</span></span> | <span data-ttu-id="a36aa-115">Valor</span><span class="sxs-lookup"><span data-stu-id="a36aa-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a36aa-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a36aa-116">Header</span></span><br/>  | <dl> <span data-ttu-id="a36aa-117"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a36aa-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a36aa-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a36aa-118">Library</span></span><br/> | <dl> <span data-ttu-id="a36aa-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="a36aa-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a36aa-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="a36aa-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a36aa-121">**Classe CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="a36aa-121">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




