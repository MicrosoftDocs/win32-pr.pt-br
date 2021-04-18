---
description: Enfileira uma solicitação de execução pelo thread de trabalho.
ms.assetid: a854f962-143d-4776-bf98-119d003867df
title: Método CMsgThread. PutThreadMsg (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.PutThreadMsg
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3445d9af4ec9c7abe6a4401e219fc305e254d555
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770282"
---
# <a name="cmsgthreadputthreadmsg-method"></a><span data-ttu-id="c8332-103">Método CMsgThread. PutThreadMsg</span><span class="sxs-lookup"><span data-stu-id="c8332-103">CMsgThread.PutThreadMsg method</span></span>

<span data-ttu-id="c8332-104">Enfileira uma solicitação de execução pelo thread de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c8332-104">Queues a request for execution by the worker thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8332-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c8332-105">Syntax</span></span>


```C++
void PutThreadMsg(
   UINT     uMsg,
   DWORD    dwMsgFlags,
   LPVOID   lpMsgParam,
   CAMEvent *pEvent = NULL
);
```



## <a name="parameters"></a><span data-ttu-id="c8332-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c8332-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8332-107">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="c8332-107">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="c8332-108">Código de solicitação.</span><span class="sxs-lookup"><span data-stu-id="c8332-108">Request code.</span></span>

</dd> <dt>

<span data-ttu-id="c8332-109">*dwMsgFlags*</span><span class="sxs-lookup"><span data-stu-id="c8332-109">*dwMsgFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="c8332-110">Parâmetro de sinalizadores opcionais.</span><span class="sxs-lookup"><span data-stu-id="c8332-110">Optional flags parameter.</span></span>

</dd> <dt>

<span data-ttu-id="c8332-111">*lpMsgParam*</span><span class="sxs-lookup"><span data-stu-id="c8332-111">*lpMsgParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c8332-112">Ponteiro opcional para um bloco de dados que contém parâmetros adicionais ou valores de retorno.</span><span class="sxs-lookup"><span data-stu-id="c8332-112">Optional pointer to a data block containing additional parameters or return values.</span></span> <span data-ttu-id="c8332-113">Deve ser estático ou alocado para heap e não automático.</span><span class="sxs-lookup"><span data-stu-id="c8332-113">Must be statically or heap-allocated and not automatic.</span></span>

</dd> <dt>

<span data-ttu-id="c8332-114">*pEvent*</span><span class="sxs-lookup"><span data-stu-id="c8332-114">*pEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="c8332-115">Ponteiro opcional para um objeto de evento a ser sinalizado após a conclusão.</span><span class="sxs-lookup"><span data-stu-id="c8332-115">Optional pointer to an event object to be signaled upon completion.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8332-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c8332-116">Return value</span></span>

<span data-ttu-id="c8332-117">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="c8332-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8332-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="c8332-118">Remarks</span></span>

<span data-ttu-id="c8332-119">Essa função de membro enfileira uma solicitação de execução pelo thread de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c8332-119">This member function queues a request for execution by the worker thread.</span></span> <span data-ttu-id="c8332-120">Os parâmetros dessa função de membro serão enfileirados (em um objeto [**CMsg**](cmsg.md) ) e passados para a função membro [**CMsgThread:: ThreadMessageProc**](cmsgthread-threadmessageproc.md) do thread de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c8332-120">The parameters of this member function will be queued (in a [**CMsg**](cmsg.md) object) and passed to the [**CMsgThread::ThreadMessageProc**](cmsgthread-threadmessageproc.md) member function of the worker thread.</span></span> <span data-ttu-id="c8332-121">Essa função de membro retorna imediatamente após o enfileiramento da solicitação e não aguarda o thread atender à solicitação.</span><span class="sxs-lookup"><span data-stu-id="c8332-121">This member function returns immediately after queuing the request and does not wait for the thread to fulfill the request.</span></span> <span data-ttu-id="c8332-122">A função membro **CMsgThread:: ThreadMessageProc** da classe derivada define os quatro parâmetros.</span><span class="sxs-lookup"><span data-stu-id="c8332-122">The **CMsgThread::ThreadMessageProc** member function of the derived class defines the four parameters.</span></span>

<span data-ttu-id="c8332-123">Essa função de membro usa uma lista multithread segura, portanto, várias chamadas para essa função de membro de threads diferentes podem ser feitas com segurança.</span><span class="sxs-lookup"><span data-stu-id="c8332-123">This member function uses a multithread safe list, so multiple calls to this member function from different threads can be made safely.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8332-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8332-124">Requirements</span></span>



| <span data-ttu-id="c8332-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8332-125">Requirement</span></span> | <span data-ttu-id="c8332-126">Valor</span><span class="sxs-lookup"><span data-stu-id="c8332-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8332-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c8332-127">Header</span></span><br/>  | <dl> <span data-ttu-id="c8332-128"><dt>Msgthrd. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c8332-128"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c8332-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c8332-129">Library</span></span><br/> | <dl> <span data-ttu-id="c8332-130"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="c8332-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8332-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="c8332-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8332-132">**Classe CMsgThread**</span><span class="sxs-lookup"><span data-stu-id="c8332-132">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




