---
description: O método NotifyThread notifica o thread de que a fila contém dados.
ms.assetid: d91cde3f-2876-4fb4-a124-f1460bba2cc9
title: Método COutputQueue. NotifyThread (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.NotifyThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7bb5f965bac15e99140955e8ee2519feaadfef85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771845"
---
# <a name="coutputqueuenotifythread-method"></a><span data-ttu-id="5540f-103">Método COutputQueue. NotifyThread</span><span class="sxs-lookup"><span data-stu-id="5540f-103">COutputQueue.NotifyThread method</span></span>

<span data-ttu-id="5540f-104">O `NotifyThread` método notifica o thread de que a fila contém dados.</span><span class="sxs-lookup"><span data-stu-id="5540f-104">The `NotifyThread` method notifies the thread that the queue contains data.</span></span>

## <a name="syntax"></a><span data-ttu-id="5540f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5540f-105">Syntax</span></span>


```C++
void NotifyThread();
```



## <a name="parameters"></a><span data-ttu-id="5540f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5540f-106">Parameters</span></span>

<span data-ttu-id="5540f-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="5540f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5540f-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5540f-108">Return value</span></span>

<span data-ttu-id="5540f-109">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="5540f-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5540f-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="5540f-110">Remarks</span></span>

<span data-ttu-id="5540f-111">Mantenha a seção crítica antes de chamar este método.</span><span class="sxs-lookup"><span data-stu-id="5540f-111">Hold the critical section before calling this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="5540f-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5540f-112">Requirements</span></span>



| <span data-ttu-id="5540f-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="5540f-113">Requirement</span></span> | <span data-ttu-id="5540f-114">Valor</span><span class="sxs-lookup"><span data-stu-id="5540f-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5540f-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5540f-115">Header</span></span><br/>  | <dl> <span data-ttu-id="5540f-116"><dt>Outputq. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5540f-116"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5540f-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5540f-117">Library</span></span><br/> | <dl> <span data-ttu-id="5540f-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="5540f-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5540f-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="5540f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5540f-120">**Classe COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="5540f-120">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




