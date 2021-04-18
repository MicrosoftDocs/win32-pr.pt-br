---
description: O método GetRequest aguarda a próxima solicitação.
ms.assetid: 9f275ee6-cb78-455a-b924-7337c8d2a6dd
title: Método CAMThread. GetRequest (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.GetRequest
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 506707bc78583fd9729ad28fb5507b82bee5e670
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760287"
---
# <a name="camthreadgetrequest-method"></a><span data-ttu-id="db4f6-103">Método CAMThread. GetRequest</span><span class="sxs-lookup"><span data-stu-id="db4f6-103">CAMThread.GetRequest method</span></span>

<span data-ttu-id="db4f6-104">O `GetRequest` método aguarda a próxima solicitação.</span><span class="sxs-lookup"><span data-stu-id="db4f6-104">The `GetRequest` method waits for the next request.</span></span>

## <a name="syntax"></a><span data-ttu-id="db4f6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="db4f6-105">Syntax</span></span>


```C++
DWORD GetRequest();
```



## <a name="parameters"></a><span data-ttu-id="db4f6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="db4f6-106">Parameters</span></span>

<span data-ttu-id="db4f6-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="db4f6-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="db4f6-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="db4f6-108">Return value</span></span>

<span data-ttu-id="db4f6-109">Retorna um valor que é definido pela classe derivada.</span><span class="sxs-lookup"><span data-stu-id="db4f6-109">Returns a value that is defined by the derived class.</span></span>

## <a name="remarks"></a><span data-ttu-id="db4f6-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="db4f6-110">Remarks</span></span>

<span data-ttu-id="db4f6-111">Esse método é bloqueado até que outro thread chame o método [**CAMThread:: CallWorker**](camthread-callworker.md) .</span><span class="sxs-lookup"><span data-stu-id="db4f6-111">This method blocks until another thread calls the [**CAMThread::CallWorker**](camthread-callworker.md) method.</span></span> <span data-ttu-id="db4f6-112">Em seguida, ele retorna o parâmetro que foi passado para CallWorker.</span><span class="sxs-lookup"><span data-stu-id="db4f6-112">Then it returns the parameter that was passed to CallWorker.</span></span> <span data-ttu-id="db4f6-113">Chame o método [**CAMThread:: Reply**](camthread-reply.md) para liberar o thread solicitante.</span><span class="sxs-lookup"><span data-stu-id="db4f6-113">Call the [**CAMThread::Reply**](camthread-reply.md) method to release the requesting thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="db4f6-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db4f6-114">Requirements</span></span>



| <span data-ttu-id="db4f6-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="db4f6-115">Requirement</span></span> | <span data-ttu-id="db4f6-116">Valor</span><span class="sxs-lookup"><span data-stu-id="db4f6-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db4f6-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="db4f6-117">Header</span></span><br/>  | <dl> <span data-ttu-id="db4f6-118"><dt>Wxutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="db4f6-118"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="db4f6-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="db4f6-119">Library</span></span><br/> | <dl> <span data-ttu-id="db4f6-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="db4f6-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db4f6-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="db4f6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db4f6-122">**Classe CAMThread**</span><span class="sxs-lookup"><span data-stu-id="db4f6-122">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




