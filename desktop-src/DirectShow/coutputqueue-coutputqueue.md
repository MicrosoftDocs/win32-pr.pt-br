---
description: Método de construtor.
ms.assetid: 672c0337-0c36-4f53-9125-d02fe8b36b1c
title: Construtor COutputQueue. COutputQueue (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.COutputQueue
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: de4d8fe0d0a7c3dcf90e67f80a939f6294cb3d5b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778493"
---
# <a name="coutputqueuecoutputqueue-constructor"></a><span data-ttu-id="d1a5d-103">Construtor COutputQueue. COutputQueue</span><span class="sxs-lookup"><span data-stu-id="d1a5d-103">COutputQueue.COutputQueue constructor</span></span>

<span data-ttu-id="d1a5d-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="d1a5d-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1a5d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d1a5d-105">Syntax</span></span>


```C++
COutputQueue(
   IPin    *pInputPin,
   HRESULT *phr,
   BOOL    bAuto = TRUE,
   BOOL    bQueue = TRUE,
   LONG    lBatchSize = 1,
   BOOL    bBatchExact = FALSE,
   LONG    lListSize = DEFAULTCACHE,
   DWORD   dwPriority = THREAD_PRIORITY_NORMAL
);
```



## <a name="parameters"></a><span data-ttu-id="d1a5d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d1a5d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1a5d-107">*pInputPin*</span><span class="sxs-lookup"><span data-stu-id="d1a5d-107">*pInputPin*</span></span> 
</dt> <dd>

<span data-ttu-id="d1a5d-108">Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do pino de entrada.</span><span class="sxs-lookup"><span data-stu-id="d1a5d-108">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the input pin.</span></span> <span data-ttu-id="d1a5d-109">O objeto fornecerá amostras para esse PIN.</span><span class="sxs-lookup"><span data-stu-id="d1a5d-109">The object will deliver samples to this pin.</span></span>

</dd> <dt>

<span data-ttu-id="d1a5d-110">*phr*</span><span class="sxs-lookup"><span data-stu-id="d1a5d-110">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="d1a5d-111">Ponteiro para um código de retorno **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d1a5d-111">Pointer to an **HRESULT** return code.</span></span> <span data-ttu-id="d1a5d-112">Defina o valor como S \_ OK antes de chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="d1a5d-112">Set the value to S\_OK before calling this method.</span></span> <span data-ttu-id="d1a5d-113">No retorno, *PHR* recebe um valor que indica o êxito ou a falha do método.</span><span class="sxs-lookup"><span data-stu-id="d1a5d-113">On return, *phr* receives a value that indicates the success or failure of the method.</span></span>

</dd> <dt>

<span data-ttu-id="d1a5d-114">*bAuto*</span><span class="sxs-lookup"><span data-stu-id="d1a5d-114">*bAuto*</span></span> 
</dt> <dd>

<span data-ttu-id="d1a5d-115">Sinalizador que especifica se o objeto decide quando criar uma fila.</span><span class="sxs-lookup"><span data-stu-id="d1a5d-115">Flag that specifies whether the object decides when to create a queue.</span></span> <span data-ttu-id="d1a5d-116">Se **for true**, o objeto criará uma fila somente se o PIN de entrada puder ser bloqueado.</span><span class="sxs-lookup"><span data-stu-id="d1a5d-116">If **TRUE**, the object creates a queue only if the input pin might block.</span></span> <span data-ttu-id="d1a5d-117">Se **for false**, o parâmetro *bQueue* especificará se uma fila deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="d1a5d-117">If **FALSE**, the *bQueue* parameter specifies whether to create a queue.</span></span>

</dd> <dt>

<span data-ttu-id="d1a5d-118">*bQueue*</span><span class="sxs-lookup"><span data-stu-id="d1a5d-118">*bQueue*</span></span> 
</dt> <dd>

<span data-ttu-id="d1a5d-119">Se *Bauto* for **true**, esse parâmetro será ignorado.</span><span class="sxs-lookup"><span data-stu-id="d1a5d-119">If *bAuto* is **TRUE**, this parameter is ignored.</span></span> <span data-ttu-id="d1a5d-120">Se *Bauto* for **false**, esse sinalizador especificará se uma fila deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="d1a5d-120">If *bAuto* is **FALSE**, this flag specifies whether to create a queue.</span></span>

</dd> <dt>

<span data-ttu-id="d1a5d-121">*lBatchSize*</span><span class="sxs-lookup"><span data-stu-id="d1a5d-121">*lBatchSize*</span></span> 
</dt> <dd>

<span data-ttu-id="d1a5d-122">Número máximo de amostras a serem entregues em um lote.</span><span class="sxs-lookup"><span data-stu-id="d1a5d-122">Maximum number of samples to deliver in one batch.</span></span>

</dd> <dt>

<span data-ttu-id="d1a5d-123">*bBatchExact*</span><span class="sxs-lookup"><span data-stu-id="d1a5d-123">*bBatchExact*</span></span> 
</dt> <dd>

<span data-ttu-id="d1a5d-124">Sinalizador que especifica se os tamanhos de lote exatos devem ser usados.</span><span class="sxs-lookup"><span data-stu-id="d1a5d-124">Flag that specifies whether to use exact batch sizes.</span></span> <span data-ttu-id="d1a5d-125">Se **for true**, o objeto aguardará exemplos de *lBatchSize* antes de entregá-los ao PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="d1a5d-125">If **TRUE**, the object waits for *lBatchSize* samples before delivering them to the input pin.</span></span> <span data-ttu-id="d1a5d-126">Se **for false**, o objeto fornecerá exemplos à medida que ele os receber.</span><span class="sxs-lookup"><span data-stu-id="d1a5d-126">If **FALSE**, the object delivers samples as it receives them.</span></span>

</dd> <dt>

<span data-ttu-id="d1a5d-127">*lListSize*</span><span class="sxs-lookup"><span data-stu-id="d1a5d-127">*lListSize*</span></span> 
</dt> <dd>

<span data-ttu-id="d1a5d-128">Tamanho do cache da fila.</span><span class="sxs-lookup"><span data-stu-id="d1a5d-128">Cache size for the queue.</span></span> <span data-ttu-id="d1a5d-129">O valor padrão, defaultcache, é uma constante definida para a classe [**CBaseList**](cbaselist.md) .</span><span class="sxs-lookup"><span data-stu-id="d1a5d-129">The default value, DEFAULTCACHE, is a constant defined for the [**CBaseList**](cbaselist.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="d1a5d-130">*dwPriority*</span><span class="sxs-lookup"><span data-stu-id="d1a5d-130">*dwPriority*</span></span> 
</dt> <dd>

<span data-ttu-id="d1a5d-131">Prioridade do thread que fornece exemplos.</span><span class="sxs-lookup"><span data-stu-id="d1a5d-131">Priority of the thread that delivers samples.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d1a5d-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="d1a5d-132">Remarks</span></span>

<span data-ttu-id="d1a5d-133">Se *Bauto* for **true**, o objeto chamará o método [**IMemInputPin:: ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) no PIN do downstream.</span><span class="sxs-lookup"><span data-stu-id="d1a5d-133">If *bAuto* is **TRUE**, the object calls the [**IMemInputPin::ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) method on the downstream pin.</span></span> <span data-ttu-id="d1a5d-134">Se **ReceiveCanBlock** retornar S \_ OK (o que significa que o PIN pode bloquear em [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) calls), o objeto criará um thread para fornecer exemplos.</span><span class="sxs-lookup"><span data-stu-id="d1a5d-134">If **ReceiveCanBlock** returns S\_OK (meaning the pin might block on [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) calls), the object creates a thread for delivering samples.</span></span> <span data-ttu-id="d1a5d-135">Caso contrário, ele não cria um thread.</span><span class="sxs-lookup"><span data-stu-id="d1a5d-135">Otherwise, it does not create a thread.</span></span>

<span data-ttu-id="d1a5d-136">Se *Bauto* for **false**, o valor de *bQueue* determinará se um thread deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="d1a5d-136">If *bAuto* is **FALSE**, the value of *bQueue* determines whether to create a thread.</span></span>

<span data-ttu-id="d1a5d-137">Se o objeto criar um thread, ele atribuirá o identificador de thread à variável de membro [**COutputQueue:: m \_ hThread**](coutputqueue-m-hthread.md) .</span><span class="sxs-lookup"><span data-stu-id="d1a5d-137">If the object creates a thread, it assigns the thread handle to the [**COutputQueue::m\_hThread**](coutputqueue-m-hthread.md) member variable.</span></span> <span data-ttu-id="d1a5d-138">O procedimento de thread é [**COutputQueue:: InitialThreadProc**](coutputqueue-initialthreadproc.md)e o parâmetro thread é um ponteiro para isso.</span><span class="sxs-lookup"><span data-stu-id="d1a5d-138">The thread procedure is [**COutputQueue::InitialThreadProc**](coutputqueue-initialthreadproc.md), and the thread parameter is a pointer to this.</span></span> <span data-ttu-id="d1a5d-139">O objeto também cria uma fila para manter amostras, que é fornecida pela variável de membro da [**\_ lista COutputQueue:: m**](coutputqueue-m-list.md) .</span><span class="sxs-lookup"><span data-stu-id="d1a5d-139">The object also creates a queue for holding samples, which is given by the [**COutputQueue::m\_List**](coutputqueue-m-list.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1a5d-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1a5d-140">Requirements</span></span>



| <span data-ttu-id="d1a5d-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1a5d-141">Requirement</span></span> | <span data-ttu-id="d1a5d-142">Valor</span><span class="sxs-lookup"><span data-stu-id="d1a5d-142">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1a5d-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d1a5d-143">Header</span></span><br/>  | <dl> <span data-ttu-id="d1a5d-144"><dt>Outputq. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d1a5d-144"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d1a5d-145">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d1a5d-145">Library</span></span><br/> | <dl> <span data-ttu-id="d1a5d-146"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="d1a5d-146"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1a5d-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="d1a5d-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1a5d-148">**Classe COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="d1a5d-148">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




