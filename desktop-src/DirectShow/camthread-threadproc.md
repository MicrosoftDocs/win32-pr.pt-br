---
description: O método ThreadProc é o procedimento de thread.
ms.assetid: 2d991f15-afea-4843-bc68-aeb5ca69d28b
title: Método CAMThread. ThreadProc (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.ThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7081a7f7e1cd84a6bf8d482aa7dddf7a48b39f0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750913"
---
# <a name="camthreadthreadproc-method"></a><span data-ttu-id="db85d-103">Método CAMThread. ThreadProc</span><span class="sxs-lookup"><span data-stu-id="db85d-103">CAMThread.ThreadProc method</span></span>

<span data-ttu-id="db85d-104">O `ThreadProc` método é o procedimento de thread.</span><span class="sxs-lookup"><span data-stu-id="db85d-104">The `ThreadProc` method is the thread procedure.</span></span>

## <a name="syntax"></a><span data-ttu-id="db85d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="db85d-105">Syntax</span></span>


```C++
virtual DWORD ThreadProc() = 0;
```



## <a name="parameters"></a><span data-ttu-id="db85d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="db85d-106">Parameters</span></span>

<span data-ttu-id="db85d-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="db85d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="db85d-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="db85d-108">Return value</span></span>

<span data-ttu-id="db85d-109">Retorna um valor **DWORD** cujo significado é definido pela classe derivada.</span><span class="sxs-lookup"><span data-stu-id="db85d-109">Returns a **DWORD** value whose meaning is defined by the derived class.</span></span>

## <a name="remarks"></a><span data-ttu-id="db85d-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="db85d-110">Remarks</span></span>

<span data-ttu-id="db85d-111">Esse é um método virtual puro.</span><span class="sxs-lookup"><span data-stu-id="db85d-111">This is a pure virtual method.</span></span> <span data-ttu-id="db85d-112">Implemente esse método em sua classe derivada para fornecer um procedimento de thread.</span><span class="sxs-lookup"><span data-stu-id="db85d-112">Implement this method in your derived class to supply a thread procedure.</span></span> <span data-ttu-id="db85d-113">Quando o método [**CAMThread:: Create**](camthread-create.md) cria um thread, ele fornece o endereço do método [**CAMThread:: InitialThreadProc**](camthread-initialthreadproc.md) que, por sua vez, chama o método ThreadProc.</span><span class="sxs-lookup"><span data-stu-id="db85d-113">When the [**CAMThread::Create**](camthread-create.md) method creates a thread, it gives the address of the [**CAMThread::InitialThreadProc**](camthread-initialthreadproc.md) method, which in turn calls your ThreadProc method.</span></span>

<span data-ttu-id="db85d-114">Normalmente, o método ThreadProc entrará em um loop que recupera solicitações (chamando os métodos [**CAMThread:: GetRequest**](camthread-getrequest.md) ou [**CAMThread:: CheckRequest**](camthread-checkrequest.md) ) e processa os dados.</span><span class="sxs-lookup"><span data-stu-id="db85d-114">Typically, your ThreadProc method will enter a loop that retrieves requests (by calling the [**CAMThread::GetRequest**](camthread-getrequest.md) or [**CAMThread::CheckRequest**](camthread-checkrequest.md) methods) and processes data.</span></span>

<span data-ttu-id="db85d-115">Quando esse método retorna, o thread é encerrado.</span><span class="sxs-lookup"><span data-stu-id="db85d-115">When this method returns, the thread exits.</span></span>

## <a name="requirements"></a><span data-ttu-id="db85d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db85d-116">Requirements</span></span>



| <span data-ttu-id="db85d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="db85d-117">Requirement</span></span> | <span data-ttu-id="db85d-118">Valor</span><span class="sxs-lookup"><span data-stu-id="db85d-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db85d-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="db85d-119">Header</span></span><br/>  | <dl> <span data-ttu-id="db85d-120"><dt>Wxutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="db85d-120"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="db85d-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="db85d-121">Library</span></span><br/> | <dl> <span data-ttu-id="db85d-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="db85d-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db85d-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="db85d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db85d-124">**Classe CAMThread**</span><span class="sxs-lookup"><span data-stu-id="db85d-124">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




