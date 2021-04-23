---
description: O método QueueSample enfileira um exemplo.
ms.assetid: f34c0689-5afb-4941-bc3a-e4765fbbe525
title: Método COutputQueue. QueueSample (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.QueueSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8efe0ec3b2326d1af0d0075770bdc6443ab9dcad
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910064"
---
# <a name="coutputqueuequeuesample-method"></a><span data-ttu-id="0a56c-103">Método COutputQueue. QueueSample</span><span class="sxs-lookup"><span data-stu-id="0a56c-103">COutputQueue.QueueSample method</span></span>

<span data-ttu-id="0a56c-104">O `QueueSample` método enfileira um exemplo.</span><span class="sxs-lookup"><span data-stu-id="0a56c-104">The `QueueSample` method queues a sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a56c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0a56c-105">Syntax</span></span>


```C++
void QueueSample(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="0a56c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0a56c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a56c-107">*pSample*</span><span class="sxs-lookup"><span data-stu-id="0a56c-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="0a56c-108">Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do exemplo.</span><span class="sxs-lookup"><span data-stu-id="0a56c-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a56c-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0a56c-109">Return value</span></span>

<span data-ttu-id="0a56c-110">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="0a56c-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a56c-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="0a56c-111">Remarks</span></span>

<span data-ttu-id="0a56c-112">Esse método adiciona um exemplo à parte final da fila.</span><span class="sxs-lookup"><span data-stu-id="0a56c-112">This method adds a sample to the tail of the queue.</span></span> <span data-ttu-id="0a56c-113">Mantenha a seção crítica antes de chamar esse método e chame-a somente quando o objeto estiver usando um thread para fornecer exemplos.</span><span class="sxs-lookup"><span data-stu-id="0a56c-113">Hold the critical section before calling this method, and call it only when the object is using a thread to deliver samples.</span></span> <span data-ttu-id="0a56c-114">Para determinar se o objeto está usando um thread, chame o método [**COutputQueue:: IsQueued**](coutputqueue-isqueued.md) .</span><span class="sxs-lookup"><span data-stu-id="0a56c-114">To determine if the object is using a thread, call the [**COutputQueue::IsQueued**](coutputqueue-isqueued.md) method.</span></span>

<span data-ttu-id="0a56c-115">Esse método também pode ser usado para colocar as mensagens de controle na fila.</span><span class="sxs-lookup"><span data-stu-id="0a56c-115">This method can also be used to put control messages onto the queue.</span></span> <span data-ttu-id="0a56c-116">Uma mensagem de controle é uma constante definida (conversão para um \_ tipo PTR longo) que instrui o thread a executar alguma ação.</span><span class="sxs-lookup"><span data-stu-id="0a56c-116">A control message is a defined constant (cast to a LONG\_PTR type) that instructs the thread to perform some action.</span></span> <span data-ttu-id="0a56c-117">A classe **COutputQueue** define as mensagens de controle mostradas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="0a56c-117">The **COutputQueue** class defines the control messages shown in the following table.</span></span>



| <span data-ttu-id="0a56c-118">Label</span><span class="sxs-lookup"><span data-stu-id="0a56c-118">Label</span></span> | <span data-ttu-id="0a56c-119">Valor</span><span class="sxs-lookup"><span data-stu-id="0a56c-119">Value</span></span> |
|---------------|----------------------------------------|
| <span data-ttu-id="0a56c-120">Mensagem</span><span class="sxs-lookup"><span data-stu-id="0a56c-120">Message</span></span>       | <span data-ttu-id="0a56c-121">Ação</span><span class="sxs-lookup"><span data-stu-id="0a56c-121">Action</span></span>                                 |
| <span data-ttu-id="0a56c-122">\_pacote EOS</span><span class="sxs-lookup"><span data-stu-id="0a56c-122">EOS\_PACKET</span></span>   | <span data-ttu-id="0a56c-123">Fornecer uma notificação de fim de fluxo.</span><span class="sxs-lookup"><span data-stu-id="0a56c-123">Deliver an end-of-stream notification.</span></span> |
| <span data-ttu-id="0a56c-124">NOVO \_ segmento</span><span class="sxs-lookup"><span data-stu-id="0a56c-124">NEW\_SEGMENT</span></span>  | <span data-ttu-id="0a56c-125">Entregar um novo segmento.</span><span class="sxs-lookup"><span data-stu-id="0a56c-125">Deliver a new segment.</span></span>                 |
| <span data-ttu-id="0a56c-126">REDEFINIR \_ pacote</span><span class="sxs-lookup"><span data-stu-id="0a56c-126">RESET\_PACKET</span></span> | <span data-ttu-id="0a56c-127">Redefina o estado da fila.</span><span class="sxs-lookup"><span data-stu-id="0a56c-127">Reset the state of the queue.</span></span>          |
| <span data-ttu-id="0a56c-128">Enviar \_ pacote</span><span class="sxs-lookup"><span data-stu-id="0a56c-128">SEND\_PACKET</span></span>  | <span data-ttu-id="0a56c-129">Envie um lote parcial de exemplos.</span><span class="sxs-lookup"><span data-stu-id="0a56c-129">Send a partial batch of samples.</span></span>       |



 

<span data-ttu-id="0a56c-130">Esse é um método protegido, que a classe **COutputQueue** usa internamente.</span><span class="sxs-lookup"><span data-stu-id="0a56c-130">This is a protected method, which the **COutputQueue** class uses internally.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a56c-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a56c-131">Requirements</span></span>



| <span data-ttu-id="0a56c-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a56c-132">Requirement</span></span> | <span data-ttu-id="0a56c-133">Valor</span><span class="sxs-lookup"><span data-stu-id="0a56c-133">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a56c-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0a56c-134">Header</span></span><br/>  | <dl> <span data-ttu-id="0a56c-135"><dt>Outputq. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0a56c-135"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0a56c-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0a56c-136">Library</span></span><br/> | <dl> <span data-ttu-id="0a56c-137"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="0a56c-137"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a56c-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="0a56c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a56c-139">**Classe COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="0a56c-139">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




