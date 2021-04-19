---
description: O método ThreadProc recupera amostras da fila e as entrega ao PIN de entrada.
ms.assetid: e5da0a12-c722-4d08-bf84-5e3aa60b64a9
title: Método COutputQueue. ThreadProc (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.ThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 75e2e6bd7fa05480603f30e68eeaf0487918ae7f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749246"
---
# <a name="coutputqueuethreadproc-method"></a><span data-ttu-id="d0454-103">Método COutputQueue. ThreadProc</span><span class="sxs-lookup"><span data-stu-id="d0454-103">COutputQueue.ThreadProc method</span></span>

<span data-ttu-id="d0454-104">O `ThreadProc` método recupera amostras da fila e as entrega ao PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="d0454-104">The `ThreadProc` method retrieves samples from the queue and delivers them to the input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0454-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d0454-105">Syntax</span></span>


```C++
DWORD ThreadProc();
```



## <a name="parameters"></a><span data-ttu-id="d0454-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d0454-106">Parameters</span></span>

<span data-ttu-id="d0454-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="d0454-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d0454-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d0454-108">Return value</span></span>

<span data-ttu-id="d0454-109">Retorna zero.</span><span class="sxs-lookup"><span data-stu-id="d0454-109">Returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0454-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="d0454-110">Remarks</span></span>

<span data-ttu-id="d0454-111">O método [**COutputQueue:: InitialThreadProc**](coutputqueue-initialthreadproc.md) chama esse método, que implementa o loop de thread principal.</span><span class="sxs-lookup"><span data-stu-id="d0454-111">The [**COutputQueue::InitialThreadProc**](coutputqueue-initialthreadproc.md) method calls this method, which implements the main thread loop.</span></span> <span data-ttu-id="d0454-112">Dentro do loop, o método executa as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="d0454-112">Within the loop, the method performs the following steps:</span></span>

1.  <span data-ttu-id="d0454-113">Recupera um exemplo para a fila.</span><span class="sxs-lookup"><span data-stu-id="d0454-113">Retrieves a sample for the queue.</span></span>
2.  <span data-ttu-id="d0454-114">Se o exemplo for uma mensagem de controle, o Thread executará a ação de controle.</span><span class="sxs-lookup"><span data-stu-id="d0454-114">If the sample is a control message, the thread executes the control action.</span></span> <span data-ttu-id="d0454-115">Caso contrário, ele coloca o exemplo na matriz [**COutputQueue:: m \_ ppSamples**](coutputqueue-m-ppsamples.md) .</span><span class="sxs-lookup"><span data-stu-id="d0454-115">Otherwise, it places the sample into the [**COutputQueue::m\_ppSamples**](coutputqueue-m-ppsamples.md) array.</span></span>
3.  <span data-ttu-id="d0454-116">Quando a matriz estiver cheia (ou se [**COutputQueue:: m \_ BBatchExact**](coutputqueue-m-bbatchexact.md) for **false**), o thread chamará o método [**IMemInputPin:: ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) para entregar os exemplos.</span><span class="sxs-lookup"><span data-stu-id="d0454-116">When the array is full (or if [**COutputQueue::m\_bBatchExact**](coutputqueue-m-bbatchexact.md) is **FALSE**), the thread calls the [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) method to deliver the samples.</span></span>
4.  <span data-ttu-id="d0454-117">Se nenhuma amostra for enfileirada, o thread aguardará o semáforo [**COutputQueue:: m \_ hSem**](coutputqueue-m-hsem.md) .</span><span class="sxs-lookup"><span data-stu-id="d0454-117">If no samples are queued, the thread waits on the [**COutputQueue::m\_hSem**](coutputqueue-m-hsem.md) semaphore.</span></span>

<span data-ttu-id="d0454-118">O thread termina quando a variável de membro [**COutputQueue:: m \_ bTerminate**](coutputqueue-m-bterminate.md) se torna **verdadeira**.</span><span class="sxs-lookup"><span data-stu-id="d0454-118">The thread terminates when the [**COutputQueue::m\_bTerminate**](coutputqueue-m-bterminate.md) member variable becomes **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0454-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0454-119">Requirements</span></span>



| <span data-ttu-id="d0454-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0454-120">Requirement</span></span> | <span data-ttu-id="d0454-121">Valor</span><span class="sxs-lookup"><span data-stu-id="d0454-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0454-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d0454-122">Header</span></span><br/>  | <dl> <span data-ttu-id="d0454-123"><dt>Outputq. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d0454-123"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d0454-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d0454-124">Library</span></span><br/> | <dl> <span data-ttu-id="d0454-125"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="d0454-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0454-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="d0454-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0454-127">**Classe COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="d0454-127">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




