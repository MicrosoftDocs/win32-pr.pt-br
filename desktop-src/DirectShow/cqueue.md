---
description: O modelo de classe CQueue implementa uma fila simples e de tamanho estático.
ms.assetid: 5a4f0bcf-24ed-427d-898d-f3ddc6a35b59
title: Classe CQueue (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CQueue
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4ceef0d29e0f6f06c30355a47e3274495f17dceb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760753"
---
# <a name="cqueue-class"></a><span data-ttu-id="cdb6e-103">Classe CQueue</span><span class="sxs-lookup"><span data-stu-id="cdb6e-103">CQueue class</span></span>

<span data-ttu-id="cdb6e-104">O modelo de classe **CQueue** implementa uma fila simples e de tamanho estático.</span><span class="sxs-lookup"><span data-stu-id="cdb6e-104">The **CQueue** class template implements a simple, statically sized queue.</span></span>



| <span data-ttu-id="cdb6e-105">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="cdb6e-105">Public Methods</span></span>                                  | <span data-ttu-id="cdb6e-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="cdb6e-106">Description</span></span>                             |
|-------------------------------------------------|-----------------------------------------|
| [<span data-ttu-id="cdb6e-107">**CQueue**</span><span class="sxs-lookup"><span data-stu-id="cdb6e-107">**CQueue**</span></span>](cqueue-cqueue.md)                 | <span data-ttu-id="cdb6e-108">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="cdb6e-108">Constructor method.</span></span>                     |
| [<span data-ttu-id="cdb6e-109">**~ CQueue**</span><span class="sxs-lookup"><span data-stu-id="cdb6e-109">**~CQueue**</span></span>](cqueue--cqueue.md)               | <span data-ttu-id="cdb6e-110">Método destruidor.</span><span class="sxs-lookup"><span data-stu-id="cdb6e-110">Destructor method.</span></span>                      |
| [<span data-ttu-id="cdb6e-111">**GetQueueObject**</span><span class="sxs-lookup"><span data-stu-id="cdb6e-111">**GetQueueObject**</span></span>](cqueue-getqueueobject.md) | <span data-ttu-id="cdb6e-112">Recupera o próximo item da fila.</span><span class="sxs-lookup"><span data-stu-id="cdb6e-112">Retrieves the next item from the queue.</span></span> |
| [<span data-ttu-id="cdb6e-113">**PutQueueObject**</span><span class="sxs-lookup"><span data-stu-id="cdb6e-113">**PutQueueObject**</span></span>](cqueue-putqueueobject.md) | <span data-ttu-id="cdb6e-114">Coloca um item na fila.</span><span class="sxs-lookup"><span data-stu-id="cdb6e-114">Puts an item onto the queue.</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="cdb6e-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="cdb6e-115">Remarks</span></span>

<span data-ttu-id="cdb6e-116">O construtor de classe especifica o tamanho da fila.</span><span class="sxs-lookup"><span data-stu-id="cdb6e-116">The class constructor specifies the size of the queue.</span></span> <span data-ttu-id="cdb6e-117">Use o [**CQueue::P utqueueobject**](cqueue-putqueueobject.md) para colocar um item na fila e o método [**CQueue:: GetQueueObject**](cqueue-getqueueobject.md) para retirar um item da fila.</span><span class="sxs-lookup"><span data-stu-id="cdb6e-117">Use the [**CQueue::PutQueueObject**](cqueue-putqueueobject.md) to put an item on the queue, and the [**CQueue::GetQueueObject**](cqueue-getqueueobject.md) method to dequeues an item.</span></span> <span data-ttu-id="cdb6e-118">Se a fila estiver cheia, o método **PutQueueObject** será bloqueado até que um item seja removido da fila.</span><span class="sxs-lookup"><span data-stu-id="cdb6e-118">If the queue is full, the **PutQueueObject** method blocks until an item is dequeued.</span></span> <span data-ttu-id="cdb6e-119">Se a fila estiver vazia, os blocos **GetQueueObject** até que um item seja enfileirado.</span><span class="sxs-lookup"><span data-stu-id="cdb6e-119">If the queue is empty, the **GetQueueObject** blocks until an item is queued.</span></span> <span data-ttu-id="cdb6e-120">O parâmetro de modelo especifica o tipo de item.</span><span class="sxs-lookup"><span data-stu-id="cdb6e-120">The template parameter specifies the type of item.</span></span> <span data-ttu-id="cdb6e-121">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="cdb6e-121">For example:</span></span>


```
CQueue<int> number_queue;
number_queue.PutQueueObject(7);
```



<span data-ttu-id="cdb6e-122">A classe usa dois semáforos para controlar as operações de enfileiramento, um semáforo "Get" e um semáforo "Put".</span><span class="sxs-lookup"><span data-stu-id="cdb6e-122">The class uses two semaphores to control queuing operations, a "get" semaphore and a "put" semaphore.</span></span> <span data-ttu-id="cdb6e-123">O método [**GetQueueObject**](cqueue-getqueueobject.md) aguarda o semáforo "Get" (usando a função **WaitForSingleObject** ) e libera o sinal "Put" (usando a função **ReleaseSemaphore** ).</span><span class="sxs-lookup"><span data-stu-id="cdb6e-123">The [**GetQueueObject**](cqueue-getqueueobject.md) method waits on the "get" semaphore (using the **WaitForSingleObject** function) and releases the "put" semaphore (using the **ReleaseSemaphore** function).</span></span> <span data-ttu-id="cdb6e-124">O método [**PutQueueObject**](cqueue-putqueueobject.md) aguarda o semáforo "Put" e libera o sinal "Get".</span><span class="sxs-lookup"><span data-stu-id="cdb6e-124">The [**PutQueueObject**](cqueue-putqueueobject.md) method waits on the "put" semaphore and releases the "get" semaphore.</span></span> <span data-ttu-id="cdb6e-125">A classe usa uma seção crítica para serializar operações de enfileiramento entre vários threads.</span><span class="sxs-lookup"><span data-stu-id="cdb6e-125">The class uses a critical section to serialize queuing operations among multiple threads.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdb6e-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cdb6e-126">Requirements</span></span>



| <span data-ttu-id="cdb6e-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="cdb6e-127">Requirement</span></span> | <span data-ttu-id="cdb6e-128">Valor</span><span class="sxs-lookup"><span data-stu-id="cdb6e-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdb6e-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cdb6e-129">Header</span></span><br/>  | <dl> <span data-ttu-id="cdb6e-130"><dt>Wxutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cdb6e-130"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="cdb6e-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cdb6e-131">Library</span></span><br/> | <dl> <span data-ttu-id="cdb6e-132"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="cdb6e-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




