---
description: 'O método GetRequestHandle recupera um identificador para o evento que é sinalizado pelo método CAMThread:: CallWorker.'
ms.assetid: 6e4496ae-a635-4b55-ae7a-31748f21068b
title: Método CAMThread. GetRequestHandle (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.GetRequestHandle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 051a6a3e3daed1dae6df3bdbb42e36f07b852d85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105792561"
---
# <a name="camthreadgetrequesthandle-method"></a><span data-ttu-id="10f87-103">Método CAMThread. GetRequestHandle</span><span class="sxs-lookup"><span data-stu-id="10f87-103">CAMThread.GetRequestHandle method</span></span>

<span data-ttu-id="10f87-104">O `GetRequestHandle` método recupera um identificador para o evento que é sinalizado pelo método [**CAMThread:: CallWorker**](camthread-callworker.md) .</span><span class="sxs-lookup"><span data-stu-id="10f87-104">The `GetRequestHandle` method retrieves a handle to the event that is signaled by the [**CAMThread::CallWorker**](camthread-callworker.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="10f87-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="10f87-105">Syntax</span></span>


```C++
HANDLE GetRequestHandle() const;
```



## <a name="parameters"></a><span data-ttu-id="10f87-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="10f87-106">Parameters</span></span>

<span data-ttu-id="10f87-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="10f87-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="10f87-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="10f87-108">Return value</span></span>

<span data-ttu-id="10f87-109">Retorna um identificador de evento.</span><span class="sxs-lookup"><span data-stu-id="10f87-109">Returns an event handle.</span></span>

## <a name="remarks"></a><span data-ttu-id="10f87-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="10f87-110">Remarks</span></span>

<span data-ttu-id="10f87-111">A classe CAMEvent mantém um evento particular de redefinição manual, que é definido por CallWorker e redefinido pelo método [**CAMThread:: Reply**](camthread-reply.md) .</span><span class="sxs-lookup"><span data-stu-id="10f87-111">The CAMEvent class keeps a private manual-reset event, which is set by CallWorker and reset by the [**CAMThread::Reply**](camthread-reply.md) method.</span></span>

<span data-ttu-id="10f87-112">Se você chamar uma função como WaitForMultipleObjects, use GetRequestHandle para recuperar o identificador de evento.</span><span class="sxs-lookup"><span data-stu-id="10f87-112">If you call a function such as WaitForMultipleObjects, use GetRequestHandle to retrieve the event handle.</span></span>

## <a name="requirements"></a><span data-ttu-id="10f87-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10f87-113">Requirements</span></span>



| <span data-ttu-id="10f87-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="10f87-114">Requirement</span></span> | <span data-ttu-id="10f87-115">Valor</span><span class="sxs-lookup"><span data-stu-id="10f87-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10f87-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="10f87-116">Header</span></span><br/>  | <dl> <span data-ttu-id="10f87-117"><dt>Wxutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="10f87-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="10f87-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="10f87-118">Library</span></span><br/> | <dl> <span data-ttu-id="10f87-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="10f87-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10f87-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="10f87-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10f87-121">**Classe CAMThread**</span><span class="sxs-lookup"><span data-stu-id="10f87-121">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




