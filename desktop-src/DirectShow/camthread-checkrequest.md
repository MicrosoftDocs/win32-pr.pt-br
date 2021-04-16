---
description: O método CheckRequest verifica se há uma solicitação, sem bloqueio.
ms.assetid: 46d0840e-a304-41e3-9016-9f35e404cd30
title: Método CAMThread. CheckRequest (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.CheckRequest
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5a004e0f5303cf6702c03e78c292a6a2d832a489
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779859"
---
# <a name="camthreadcheckrequest-method"></a><span data-ttu-id="7526e-103">Método CAMThread. CheckRequest</span><span class="sxs-lookup"><span data-stu-id="7526e-103">CAMThread.CheckRequest method</span></span>

<span data-ttu-id="7526e-104">O `CheckRequest` método verifica se há uma solicitação, sem bloqueio.</span><span class="sxs-lookup"><span data-stu-id="7526e-104">The `CheckRequest` method checks if there is a request, without blocking.</span></span>

## <a name="syntax"></a><span data-ttu-id="7526e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7526e-105">Syntax</span></span>


```C++
BOOL CheckRequest(
   DWORD *pParam
);
```



## <a name="parameters"></a><span data-ttu-id="7526e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7526e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7526e-107">*pParam*</span><span class="sxs-lookup"><span data-stu-id="7526e-107">*pParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7526e-108">Ponteiro para uma variável que recebe o valor passado na última chamada para o método [**CAMThread:: CallWorker**](camthread-callworker.md) .</span><span class="sxs-lookup"><span data-stu-id="7526e-108">Pointer to a variable that receives the value passed in the last call to the [**CAMThread::CallWorker**](camthread-callworker.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7526e-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7526e-109">Return value</span></span>

<span data-ttu-id="7526e-110">Retorna **true** se houver uma solicitação pendente ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="7526e-110">Returns **TRUE** if there is a pending request, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7526e-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="7526e-111">Remarks</span></span>

<span data-ttu-id="7526e-112">Esse método é uma versão sem bloqueio do método [**CAMThread:: GetRequest**](camthread-getrequest.md) .</span><span class="sxs-lookup"><span data-stu-id="7526e-112">This method is a non-blocking version of the [**CAMThread::GetRequest**](camthread-getrequest.md) method.</span></span>

<span data-ttu-id="7526e-113">Se outro thread estiver aguardando uma chamada para CallWorker, esse método recuperará o parâmetro de solicitação e retornará **true**.</span><span class="sxs-lookup"><span data-stu-id="7526e-113">If another thread is waiting on a call to CallWorker, this method retrieves the request parameter and returns **TRUE**.</span></span> <span data-ttu-id="7526e-114">Caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="7526e-114">Otherwise, it returns **FALSE**.</span></span> <span data-ttu-id="7526e-115">Se o método retornar **true**, chame o método [**CAMThread:: Reply**](camthread-reply.md) para liberar o thread solicitante.</span><span class="sxs-lookup"><span data-stu-id="7526e-115">If the method returns **TRUE**, call the [**CAMThread::Reply**](camthread-reply.md) method to release the requesting thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="7526e-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7526e-116">Requirements</span></span>



| <span data-ttu-id="7526e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7526e-117">Requirement</span></span> | <span data-ttu-id="7526e-118">Valor</span><span class="sxs-lookup"><span data-stu-id="7526e-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7526e-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7526e-119">Header</span></span><br/>  | <dl> <span data-ttu-id="7526e-120"><dt>Wxutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7526e-120"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="7526e-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7526e-121">Library</span></span><br/> | <dl> <span data-ttu-id="7526e-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="7526e-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7526e-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="7526e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7526e-124">**Classe CAMThread**</span><span class="sxs-lookup"><span data-stu-id="7526e-124">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




