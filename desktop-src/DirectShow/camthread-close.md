---
description: O método Close aguarda até que o thread saia e, em seguida, libera seus recursos.
ms.assetid: 57e27ff7-3665-416e-8a6e-660483c5aed2
title: Método CAMThread. Close (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.Close
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9cac5ee4a1e1a9cc3fecc8d09096d031e9fc9a63
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760286"
---
# <a name="camthreadclose-method"></a><span data-ttu-id="331a0-103">Método CAMThread. Close</span><span class="sxs-lookup"><span data-stu-id="331a0-103">CAMThread.Close method</span></span>

<span data-ttu-id="331a0-104">O `Close` método aguarda até que o thread saia e, em seguida, libera seus recursos.</span><span class="sxs-lookup"><span data-stu-id="331a0-104">The `Close` method waits for the thread to exit, then releases its resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="331a0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="331a0-105">Syntax</span></span>


```C++
void Close();
```



## <a name="parameters"></a><span data-ttu-id="331a0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="331a0-106">Parameters</span></span>

<span data-ttu-id="331a0-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="331a0-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="331a0-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="331a0-108">Return value</span></span>

<span data-ttu-id="331a0-109">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="331a0-109">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="331a0-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="331a0-110">Remarks</span></span>

<span data-ttu-id="331a0-111">Antes de chamar esse método, você deve fornecer uma maneira para o thread sair.</span><span class="sxs-lookup"><span data-stu-id="331a0-111">Before calling this method, you must provide a way for the thread to exit.</span></span> <span data-ttu-id="331a0-112">Por exemplo, no método [**CAMThread:: ThreadProc**](camthread-threadproc.md) , defina uma solicitação que sinaliza o thread para sair.</span><span class="sxs-lookup"><span data-stu-id="331a0-112">For example, in your [**CAMThread::ThreadProc**](camthread-threadproc.md) method, define a request that signals the thread to exit.</span></span> <span data-ttu-id="331a0-113">Em seguida, chame o método [**CAMThread:: CallWorker**](camthread-callworker.md) com esse valor.</span><span class="sxs-lookup"><span data-stu-id="331a0-113">Then call the [**CAMThread::CallWorker**](camthread-callworker.md) method with that value.</span></span>

<span data-ttu-id="331a0-114">O método destruidor [**~ CAMThread**](camthread--camthread.md) chama esse método.</span><span class="sxs-lookup"><span data-stu-id="331a0-114">The [**~ CAMThread**](camthread--camthread.md) destructor method calls this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="331a0-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="331a0-115">Requirements</span></span>



| <span data-ttu-id="331a0-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="331a0-116">Requirement</span></span> | <span data-ttu-id="331a0-117">Valor</span><span class="sxs-lookup"><span data-stu-id="331a0-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="331a0-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="331a0-118">Header</span></span><br/>  | <dl> <span data-ttu-id="331a0-119"><dt>Wxutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="331a0-119"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="331a0-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="331a0-120">Library</span></span><br/> | <dl> <span data-ttu-id="331a0-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="331a0-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="331a0-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="331a0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="331a0-123">**Classe CAMThread**</span><span class="sxs-lookup"><span data-stu-id="331a0-123">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




