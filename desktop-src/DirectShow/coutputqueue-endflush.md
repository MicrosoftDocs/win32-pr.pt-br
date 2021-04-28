---
description: Método COutputQueue. EndFlush – o método EndFlush termina uma operação de liberação.
ms.assetid: 9171a62a-9072-49a3-8e83-f66d7e1483da
title: Método COutputQueue. EndFlush (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 37701526de66c8cd679f6849703c4eb2a1feb3ee
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099004"
---
# <a name="coutputqueueendflush-method"></a><span data-ttu-id="1c3b6-103">Método COutputQueue. EndFlush</span><span class="sxs-lookup"><span data-stu-id="1c3b6-103">COutputQueue.EndFlush method</span></span>

<span data-ttu-id="1c3b6-104">O `EndFlush` método encerra uma operação de liberação.</span><span class="sxs-lookup"><span data-stu-id="1c3b6-104">The `EndFlush` method ends a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c3b6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1c3b6-105">Syntax</span></span>


```C++
void EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="1c3b6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1c3b6-106">Parameters</span></span>

<span data-ttu-id="1c3b6-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="1c3b6-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1c3b6-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="1c3b6-108">Return value</span></span>

<span data-ttu-id="1c3b6-109">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="1c3b6-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c3b6-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="1c3b6-110">Remarks</span></span>

<span data-ttu-id="1c3b6-111">Se o objeto estiver usando um thread, esse método aguardará o evento [**COutputQueue:: m \_ evFlushComplete**](coutputqueue-m-evflushcomplete.md) .</span><span class="sxs-lookup"><span data-stu-id="1c3b6-111">If the object is using a thread, this method waits for the [**COutputQueue::m\_evFlushComplete**](coutputqueue-m-evflushcomplete.md) event.</span></span> <span data-ttu-id="1c3b6-112">O thread sinaliza esse evento depois de liberar quaisquer amostras pendentes.</span><span class="sxs-lookup"><span data-stu-id="1c3b6-112">The thread signals this event after it frees any pending samples.</span></span> <span data-ttu-id="1c3b6-113">Se o objeto não estiver usando um thread, esse método chamará o método [**COutputQueue:: FreeSamples**](coutputqueue-freesamples.md) .</span><span class="sxs-lookup"><span data-stu-id="1c3b6-113">If the object is not using a thread, this method calls the [**COutputQueue::FreeSamples**](coutputqueue-freesamples.md) method.</span></span> <span data-ttu-id="1c3b6-114">Em seguida, o `EndFlush` método chama o método [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) no pino de entrada.</span><span class="sxs-lookup"><span data-stu-id="1c3b6-114">Then the `EndFlush` method calls the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c3b6-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c3b6-115">Requirements</span></span>



| <span data-ttu-id="1c3b6-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c3b6-116">Requirement</span></span> | <span data-ttu-id="1c3b6-117">Valor</span><span class="sxs-lookup"><span data-stu-id="1c3b6-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c3b6-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1c3b6-118">Header</span></span><br/>  | <dl> <span data-ttu-id="1c3b6-119"><dt>Outputq. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1c3b6-119"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1c3b6-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1c3b6-120">Library</span></span><br/> | <dl> <span data-ttu-id="1c3b6-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="1c3b6-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c3b6-122">Consulte também</span><span class="sxs-lookup"><span data-stu-id="1c3b6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c3b6-123">**Classe COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="1c3b6-123">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




