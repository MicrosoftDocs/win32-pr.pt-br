---
description: O método NewSegment entrega um novo segmento ao pino de entrada.
ms.assetid: 53189729-9f47-425e-9df6-faea01dd4482
title: Método COutputQueue. NewSegment (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.NewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e682211a98f4409fda35687160c88b121fa93898
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758539"
---
# <a name="coutputqueuenewsegment-method"></a><span data-ttu-id="4fa07-103">Método COutputQueue. NewSegment</span><span class="sxs-lookup"><span data-stu-id="4fa07-103">COutputQueue.NewSegment method</span></span>

<span data-ttu-id="4fa07-104">O `NewSegment` método entrega um novo segmento ao PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="4fa07-104">The `NewSegment` method delivers a new segment to the input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fa07-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4fa07-105">Syntax</span></span>


```C++
HRESULT NewSegment(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop,
   double         dRate
);
```



## <a name="parameters"></a><span data-ttu-id="4fa07-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4fa07-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fa07-107">*tStart*</span><span class="sxs-lookup"><span data-stu-id="4fa07-107">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="4fa07-108">Iniciando a posição de mídia do segmento, em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="4fa07-108">Starting media position of the segment, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="4fa07-109">*tStop*</span><span class="sxs-lookup"><span data-stu-id="4fa07-109">*tStop*</span></span> 
</dt> <dd>

<span data-ttu-id="4fa07-110">Terminar a posição de mídia do segmento, em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="4fa07-110">End media position of the segment, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="4fa07-111">*dRate*</span><span class="sxs-lookup"><span data-stu-id="4fa07-111">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="4fa07-112">Taxa na qual esse segmento deve ser processado, como uma porcentagem da taxa original.</span><span class="sxs-lookup"><span data-stu-id="4fa07-112">Rate at which this segment should be processed, as a percentage of the original rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fa07-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4fa07-113">Return value</span></span>

<span data-ttu-id="4fa07-114">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4fa07-114">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4fa07-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="4fa07-115">Remarks</span></span>

<span data-ttu-id="4fa07-116">Se o objeto estiver usando um thread, ele enfileirará os seguintes itens, na ordem:</span><span class="sxs-lookup"><span data-stu-id="4fa07-116">If the object is using a thread, it queues the following items, in order:</span></span>

-   <span data-ttu-id="4fa07-117">Uma nova \_ mensagem de controle de segmento.</span><span class="sxs-lookup"><span data-stu-id="4fa07-117">A NEW\_SEGMENT control message.</span></span>
-   <span data-ttu-id="4fa07-118">Os dados do segmento.</span><span class="sxs-lookup"><span data-stu-id="4fa07-118">The segment data.</span></span>

<span data-ttu-id="4fa07-119">A nova \_ mensagem de segmento notifica o thread de que o próximo item na fila conterá dados de segmento.</span><span class="sxs-lookup"><span data-stu-id="4fa07-119">The NEW\_SEGMENT message notifies the thread that the next item on the queue will contain segment data.</span></span> <span data-ttu-id="4fa07-120">Os dados de segmento são agrupados em uma estrutura, declarados da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="4fa07-120">The segment data is bundled in a structure, declared as follows:</span></span>


```C++
struct NewSegmentPacket {
    REFERENCE_TIME tStart;
    REFERENCE_TIME tStop;
    double dRate;
}; 
```



<span data-ttu-id="4fa07-121">O thread chama o método [**IPin:: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) no pino de entrada, usando os dados fornecidos na estrutura.</span><span class="sxs-lookup"><span data-stu-id="4fa07-121">The thread calls the [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) method on the input pin, using the data given in the structure.</span></span>

<span data-ttu-id="4fa07-122">Se o objeto não estiver usando um thread, ele chamará o método [**COutputQueue:: SendAnyway**](coutputqueue-sendanyway.md) para entregar quaisquer exemplos pendentes.</span><span class="sxs-lookup"><span data-stu-id="4fa07-122">If the object is not using a thread, it calls the [**COutputQueue::SendAnyway**](coutputqueue-sendanyway.md) method to deliver any pending samples.</span></span> <span data-ttu-id="4fa07-123">Em seguida, ele chama **IPin:: NewSegment** no pino de entrada.</span><span class="sxs-lookup"><span data-stu-id="4fa07-123">Then it calls **IPin::NewSegment** on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fa07-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4fa07-124">Requirements</span></span>



| <span data-ttu-id="4fa07-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="4fa07-125">Requirement</span></span> | <span data-ttu-id="4fa07-126">Valor</span><span class="sxs-lookup"><span data-stu-id="4fa07-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fa07-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4fa07-127">Header</span></span><br/>  | <dl> <span data-ttu-id="4fa07-128"><dt>Outputq. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4fa07-128"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4fa07-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4fa07-129">Library</span></span><br/> | <dl> <span data-ttu-id="4fa07-130"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="4fa07-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fa07-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="4fa07-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fa07-132">**Classe COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="4fa07-132">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




