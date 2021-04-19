---
description: O método CallWorker sinaliza o thread com uma solicitação.
ms.assetid: 51431688-bf55-4778-afc0-91b6ab336aa3
title: Método CAMThread. CallWorker (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.CallWorker
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7410fbee4ece729d1579f525731bddaceded1153
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812997"
---
# <a name="camthreadcallworker-method"></a><span data-ttu-id="c09fc-103">Método CAMThread. CallWorker</span><span class="sxs-lookup"><span data-stu-id="c09fc-103">CAMThread.CallWorker method</span></span>

<span data-ttu-id="c09fc-104">O `CallWorker` método sinaliza o thread com uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="c09fc-104">The `CallWorker` method signals the thread with a request.</span></span>

## <a name="syntax"></a><span data-ttu-id="c09fc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c09fc-105">Syntax</span></span>


```C++
DWORD CallWorker(
   DWORD dwParam
);
```



## <a name="parameters"></a><span data-ttu-id="c09fc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c09fc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c09fc-107">*dwParam*</span><span class="sxs-lookup"><span data-stu-id="c09fc-107">*dwParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c09fc-108">Parâmetro de solicitação.</span><span class="sxs-lookup"><span data-stu-id="c09fc-108">Request parameter.</span></span> <span data-ttu-id="c09fc-109">A classe derivada define o significado do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="c09fc-109">The derived class defines the meaning of the parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c09fc-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c09fc-110">Return value</span></span>

<span data-ttu-id="c09fc-111">Retorna um valor que é definido pela classe derivada.</span><span class="sxs-lookup"><span data-stu-id="c09fc-111">Returns a value that is defined by the derived class.</span></span>

## <a name="remarks"></a><span data-ttu-id="c09fc-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="c09fc-112">Remarks</span></span>

<span data-ttu-id="c09fc-113">Os métodos [**CAMThread:: GetRequest**](camthread-getrequest.md) e [**CAMThread:: CheckRequest**](camthread-checkrequest.md) recuperam o valor do parâmetro *dwParam* .</span><span class="sxs-lookup"><span data-stu-id="c09fc-113">The [**CAMThread::GetRequest**](camthread-getrequest.md) and [**CAMThread::CheckRequest**](camthread-checkrequest.md) methods retrieve the value of the *dwParam* parameter.</span></span> <span data-ttu-id="c09fc-114">O método GetRequest é bloqueado até que `CallWorker` seja chamado.</span><span class="sxs-lookup"><span data-stu-id="c09fc-114">The GetRequest method blocks until `CallWorker` is called.</span></span>

<span data-ttu-id="c09fc-115">Esse método é bloqueado até que o método [**CAMThread:: Reply**](camthread-reply.md) seja chamado.</span><span class="sxs-lookup"><span data-stu-id="c09fc-115">This method blocks until the [**CAMThread::Reply**](camthread-reply.md) method is called.</span></span> <span data-ttu-id="c09fc-116">O valor de retorno é o parâmetro fornecido para reply.</span><span class="sxs-lookup"><span data-stu-id="c09fc-116">The return value is the parameter given to Reply.</span></span>

<span data-ttu-id="c09fc-117">Esse método contém o bloqueio [**CAMThread:: m \_ AccessLock**](camthread-m-accesslock.md) para serializar solicitações.</span><span class="sxs-lookup"><span data-stu-id="c09fc-117">This method holds the [**CAMThread::m\_AccessLock**](camthread-m-accesslock.md) lock to serialize requests.</span></span> <span data-ttu-id="c09fc-118">Portanto, chame esse método do próprio thread ou de qualquer função de membro que seja executada no contexto do thread.</span><span class="sxs-lookup"><span data-stu-id="c09fc-118">Therefore, do call this method from the thread itself or from any member function that executes in the context of the thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="c09fc-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c09fc-119">Requirements</span></span>



| <span data-ttu-id="c09fc-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c09fc-120">Requirement</span></span> | <span data-ttu-id="c09fc-121">Valor</span><span class="sxs-lookup"><span data-stu-id="c09fc-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c09fc-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c09fc-122">Header</span></span><br/>  | <dl> <span data-ttu-id="c09fc-123"><dt>Wxutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c09fc-123"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="c09fc-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c09fc-124">Library</span></span><br/> | <dl> <span data-ttu-id="c09fc-125"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="c09fc-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c09fc-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="c09fc-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c09fc-127">**Classe CAMThread**</span><span class="sxs-lookup"><span data-stu-id="c09fc-127">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




