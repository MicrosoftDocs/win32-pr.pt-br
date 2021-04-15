---
description: Processa solicitações. Essa é uma função de membro virtual pura.
ms.assetid: ffdbc287-ca17-44e4-b00a-d72a2367f510
title: Método CMsgThread. ThreadMessageProc (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.ThreadMessageProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cf47eb63a6f9d8fe4921985bb64567de6678b44c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753751"
---
# <a name="cmsgthreadthreadmessageproc-method"></a><span data-ttu-id="3e94b-104">Método CMsgThread. ThreadMessageProc</span><span class="sxs-lookup"><span data-stu-id="3e94b-104">CMsgThread.ThreadMessageProc method</span></span>

<span data-ttu-id="3e94b-105">Processa solicitações.</span><span class="sxs-lookup"><span data-stu-id="3e94b-105">Processes requests.</span></span> <span data-ttu-id="3e94b-106">Essa é uma função de membro virtual pura.</span><span class="sxs-lookup"><span data-stu-id="3e94b-106">This is a pure virtual member function.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e94b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3e94b-107">Syntax</span></span>


```C++
virtual LRESULT ThreadMessageProc(
   UINT     uMsg,
   DWORD    dwFlags,
   LPVOID   lpParam,
   CAMEvent *pEvent
);
```



## <a name="parameters"></a><span data-ttu-id="3e94b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3e94b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e94b-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="3e94b-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="3e94b-110">Código de solicitação.</span><span class="sxs-lookup"><span data-stu-id="3e94b-110">Request code.</span></span>

</dd> <dt>

<span data-ttu-id="3e94b-111">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="3e94b-111">*dwFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="3e94b-112">Parâmetro de sinalizador opcional a ser solicitado.</span><span class="sxs-lookup"><span data-stu-id="3e94b-112">Optional flag parameter to request.</span></span>

</dd> <dt>

<span data-ttu-id="3e94b-113">*lpParam*</span><span class="sxs-lookup"><span data-stu-id="3e94b-113">*lpParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3e94b-114">Ponteiro opcional para dados adicionais ou um bloco de dados de retorno.</span><span class="sxs-lookup"><span data-stu-id="3e94b-114">Optional pointer to extra data or a return data block.</span></span>

</dd> <dt>

<span data-ttu-id="3e94b-115">*pEvent*</span><span class="sxs-lookup"><span data-stu-id="3e94b-115">*pEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="3e94b-116">Ponteiro opcional para um objeto de evento.</span><span class="sxs-lookup"><span data-stu-id="3e94b-116">Optional pointer to an event object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e94b-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3e94b-117">Return value</span></span>

<span data-ttu-id="3e94b-118">Qualquer retorno diferente de zero faz com que o thread saia.</span><span class="sxs-lookup"><span data-stu-id="3e94b-118">Any nonzero return causes the thread to exit.</span></span> <span data-ttu-id="3e94b-119">Retorna zero, a menos que uma solicitação de saída tenha sido processada recentemente.</span><span class="sxs-lookup"><span data-stu-id="3e94b-119">Returns zero unless an exit request has been processed recently.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e94b-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="3e94b-120">Remarks</span></span>

<span data-ttu-id="3e94b-121">Essa função virtual pura deve ser substituída em sua classe derivada.</span><span class="sxs-lookup"><span data-stu-id="3e94b-121">This pure virtual function must be overridden in your derived class.</span></span> <span data-ttu-id="3e94b-122">Ele será chamado uma vez para cada solicitação em fila por uma chamada para a função de membro [**CMsgThread::P utthreadmsg**](cmsgthread-putthreadmsg.md) .</span><span class="sxs-lookup"><span data-stu-id="3e94b-122">It will be called once for each request queued by a call to the [**CMsgThread::PutThreadMsg**](cmsgthread-putthreadmsg.md) member function.</span></span>

<span data-ttu-id="3e94b-123">A função membro define os quatro parâmetros.</span><span class="sxs-lookup"><span data-stu-id="3e94b-123">The member function defines the four parameters.</span></span> <span data-ttu-id="3e94b-124">Normalmente, use o parâmetro *uMsg* para indicar a solicitação e os outros três parâmetros serão parâmetros adicionais opcionais.</span><span class="sxs-lookup"><span data-stu-id="3e94b-124">Typically, use the *uMsg* parameter to indicate the request, and the other three parameters will be optional additional parameters.</span></span> <span data-ttu-id="3e94b-125">O aplicativo de chamada pode fornecer um ponteiro para um objeto [**CAMEvent**](camevent.md) no parâmetro *pEvent* se o seu aplicativo exigir.</span><span class="sxs-lookup"><span data-stu-id="3e94b-125">The calling application can supply a pointer to a [**CAMEvent**](camevent.md) object in the *pEvent* parameter if your application requires it.</span></span> <span data-ttu-id="3e94b-126">Você deve definir esse evento depois de processar o evento usando uma expressão como:</span><span class="sxs-lookup"><span data-stu-id="3e94b-126">You must set this event after processing the event by using an expression such as:</span></span>


```C++
pEvent->SetEvent
```



<span data-ttu-id="3e94b-127">Um código de solicitação deve ser reservado para informar ao thread de trabalho para sair.</span><span class="sxs-lookup"><span data-stu-id="3e94b-127">One request code must be set aside to tell the worker thread to exit.</span></span> <span data-ttu-id="3e94b-128">Após o recebimento dessa solicitação, retorne 1 dessa função de membro.</span><span class="sxs-lookup"><span data-stu-id="3e94b-128">Upon receiving this request, return 1 from this member function.</span></span> <span data-ttu-id="3e94b-129">Retorne 0 se você não quiser que o thread de trabalho saia.</span><span class="sxs-lookup"><span data-stu-id="3e94b-129">Return 0 if you do not want the worker thread to exit.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e94b-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e94b-130">Requirements</span></span>



| <span data-ttu-id="3e94b-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e94b-131">Requirement</span></span> | <span data-ttu-id="3e94b-132">Valor</span><span class="sxs-lookup"><span data-stu-id="3e94b-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e94b-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3e94b-133">Header</span></span><br/>  | <dl> <span data-ttu-id="3e94b-134"><dt>Msgthrd. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3e94b-134"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3e94b-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3e94b-135">Library</span></span><br/> | <dl> <span data-ttu-id="3e94b-136"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="3e94b-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e94b-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="3e94b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e94b-138">**Classe CMsgThread**</span><span class="sxs-lookup"><span data-stu-id="3e94b-138">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




