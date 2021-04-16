---
description: 'O método ThreadProc é o procedimento de thread para o thread de trabalho. Esse método implementa o método puramente virtual CAMThread:: ThreadProc.'
ms.assetid: 8e66b609-d795-45a8-8fe5-774c659ee350
title: Método CSourceStream. ThreadProc (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.ThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6dc7d08643cc0ca76d3d05f0b9090f30200eb181
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757688"
---
# <a name="csourcestreamthreadproc-method"></a><span data-ttu-id="14ebc-104">Método CSourceStream. ThreadProc</span><span class="sxs-lookup"><span data-stu-id="14ebc-104">CSourceStream.ThreadProc method</span></span>

<span data-ttu-id="14ebc-105">O `ThreadProc` método é o procedimento de thread para o thread de trabalho.</span><span class="sxs-lookup"><span data-stu-id="14ebc-105">The `ThreadProc` method is the thread procedure for the worker thread.</span></span> <span data-ttu-id="14ebc-106">Esse método implementa o método puramente virtual [**CAMThread:: ThreadProc**](camthread-threadproc.md) .</span><span class="sxs-lookup"><span data-stu-id="14ebc-106">This method implements the pure virtual [**CAMThread::ThreadProc**](camthread-threadproc.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="14ebc-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="14ebc-107">Syntax</span></span>


```C++
virtual DWORD ThreadProc();
```



## <a name="parameters"></a><span data-ttu-id="14ebc-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="14ebc-108">Parameters</span></span>

<span data-ttu-id="14ebc-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="14ebc-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="14ebc-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="14ebc-110">Return value</span></span>

<span data-ttu-id="14ebc-111">Retornará 0 se o thread tiver sido concluído com êxito ou 1 caso contrário.</span><span class="sxs-lookup"><span data-stu-id="14ebc-111">Returns 0 if the thread completed successfully or 1 otherwise.</span></span> <span data-ttu-id="14ebc-112">Se o valor de retorno for 1, os recursos do thread ainda poderão ser alocados.</span><span class="sxs-lookup"><span data-stu-id="14ebc-112">If the return value is 1, the thread's resources might still be allocated.</span></span>

## <a name="remarks"></a><span data-ttu-id="14ebc-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="14ebc-113">Remarks</span></span>

<span data-ttu-id="14ebc-114">Esse método aguarda indefinidamente as solicitações de thread, chamando o método [**CAMThread:: GetRequest**](camthread-getrequest.md) .</span><span class="sxs-lookup"><span data-stu-id="14ebc-114">This method waits indefinitely for thread requests, by calling the [**CAMThread::GetRequest**](camthread-getrequest.md) method.</span></span> <span data-ttu-id="14ebc-115">Se receber uma solicitação [**CSourceStream:: Run**](csourcestream-run.md) ou [**CSourceStream::P ause**](csourcestream-pause.md) , ele chamará o método [**CSourceStream::D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) .</span><span class="sxs-lookup"><span data-stu-id="14ebc-115">If it receives a [**CSourceStream::Run**](csourcestream-run.md) or [**CSourceStream::Pause**](csourcestream-pause.md) request, it calls the [**CSourceStream::DoBufferProcessingLoop**](csourcestream-dobufferprocessingloop.md) method.</span></span> <span data-ttu-id="14ebc-116">O método **DoBufferProcessingLoop** envia dados por push até receber uma solicitação [**CSourceStream:: Stop**](csourcestream-stop.md) .</span><span class="sxs-lookup"><span data-stu-id="14ebc-116">The **DoBufferProcessingLoop** method pushes data until it receives a [**CSourceStream::Stop**](csourcestream-stop.md) request.</span></span> <span data-ttu-id="14ebc-117">O procedimento de thread é encerrado quando recebe uma solicitação [**CSourceStream:: Exit**](csourcestream-exit.md) .</span><span class="sxs-lookup"><span data-stu-id="14ebc-117">The thread procedure exits when it receives a [**CSourceStream::Exit**](csourcestream-exit.md) request.</span></span>

## <a name="requirements"></a><span data-ttu-id="14ebc-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14ebc-118">Requirements</span></span>



| <span data-ttu-id="14ebc-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="14ebc-119">Requirement</span></span> | <span data-ttu-id="14ebc-120">Valor</span><span class="sxs-lookup"><span data-stu-id="14ebc-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14ebc-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="14ebc-121">Header</span></span><br/>  | <dl> <span data-ttu-id="14ebc-122"><dt>Source. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="14ebc-122"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="14ebc-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="14ebc-123">Library</span></span><br/> | <dl> <span data-ttu-id="14ebc-124"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="14ebc-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14ebc-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="14ebc-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14ebc-126">**Classe CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="14ebc-126">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




