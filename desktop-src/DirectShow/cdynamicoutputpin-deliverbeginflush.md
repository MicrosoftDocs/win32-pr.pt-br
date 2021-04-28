---
description: Método CDynamicOutputPin. DeliverBeginFlush – o método DeliverBeginFlush solicita o pino de entrada conectado para iniciar uma operação de liberação.
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
ms.openlocfilehash: e4158a3d6191325e8b647e4551133952d623f795
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099314"
---
# <a name="cdynamicoutputpindeliverbeginflush-method"></a><span data-ttu-id="cc2c6-103">Método CDynamicOutputPin. DeliverBeginFlush</span><span class="sxs-lookup"><span data-stu-id="cc2c6-103">CDynamicOutputPin.DeliverBeginFlush method</span></span>

<span data-ttu-id="cc2c6-104">O `DeliverBeginFlush` método solicita o PIN de entrada conectado para iniciar uma operação de liberação.</span><span class="sxs-lookup"><span data-stu-id="cc2c6-104">The `DeliverBeginFlush` method requests the connected input pin to begin a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc2c6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cc2c6-105">Syntax</span></span>


```C++
HRESULT DeliverBeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="cc2c6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cc2c6-106">Parameters</span></span>

<span data-ttu-id="cc2c6-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="cc2c6-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cc2c6-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="cc2c6-108">Return value</span></span>

<span data-ttu-id="cc2c6-109">Retorna S \_ OK se bem-sucedido ou um valor **HRESULT** que indica a causa da falha.</span><span class="sxs-lookup"><span data-stu-id="cc2c6-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc2c6-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="cc2c6-110">Remarks</span></span>

<span data-ttu-id="cc2c6-111">Esse método substitui o método [**CBaseOutputPin::D eliverbeginflush**](cbaseoutputpin-deliverbeginflush.md) .</span><span class="sxs-lookup"><span data-stu-id="cc2c6-111">This method overrides the [**CBaseOutputPin::DeliverBeginFlush**](cbaseoutputpin-deliverbeginflush.md) method.</span></span> <span data-ttu-id="cc2c6-112">Ele define o evento [**CDynamicOutputPin:: m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md) .</span><span class="sxs-lookup"><span data-stu-id="cc2c6-112">It sets the [**CDynamicOutputPin::m\_hStopEvent**](cdynamicoutputpin-m-hstopevent.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc2c6-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc2c6-113">Requirements</span></span>



| <span data-ttu-id="cc2c6-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc2c6-114">Requirement</span></span> | <span data-ttu-id="cc2c6-115">Valor</span><span class="sxs-lookup"><span data-stu-id="cc2c6-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc2c6-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cc2c6-116">Header</span></span><br/>  | <dl> <span data-ttu-id="cc2c6-117"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cc2c6-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="cc2c6-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cc2c6-118">Library</span></span><br/> | <dl> <span data-ttu-id="cc2c6-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="cc2c6-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc2c6-120">Consulte também</span><span class="sxs-lookup"><span data-stu-id="cc2c6-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc2c6-121">**Classe CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="cc2c6-121">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




