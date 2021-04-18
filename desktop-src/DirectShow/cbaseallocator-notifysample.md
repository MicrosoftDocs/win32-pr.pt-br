---
description: O método NotifySample libera todos os threads que estão aguardando exemplos.
ms.assetid: b09c48a0-9cd5-44a7-9267-d2a11e8cde4c
title: Método CBaseAllocator. NotifySample (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.NotifySample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: acaf5e45eac6a630d0589e3c8fad106ae29fa3dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780893"
---
# <a name="cbaseallocatornotifysample-method"></a><span data-ttu-id="ba40e-103">Método CBaseAllocator. NotifySample</span><span class="sxs-lookup"><span data-stu-id="ba40e-103">CBaseAllocator.NotifySample method</span></span>

<span data-ttu-id="ba40e-104">O `NotifySample` método libera todos os threads que estão aguardando exemplos.</span><span class="sxs-lookup"><span data-stu-id="ba40e-104">The `NotifySample` method releases any threads that are waiting for samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba40e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ba40e-105">Syntax</span></span>


```C++
void NotifySample();
```



## <a name="parameters"></a><span data-ttu-id="ba40e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ba40e-106">Parameters</span></span>

<span data-ttu-id="ba40e-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="ba40e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ba40e-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ba40e-108">Return value</span></span>

<span data-ttu-id="ba40e-109">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="ba40e-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba40e-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="ba40e-110">Remarks</span></span>

<span data-ttu-id="ba40e-111">Quando há threads aguardando exemplos, o valor de [**CBaseAllocator:: m \_ lWaiting**](cbaseallocator-m-lwaiting.md) é maior que zero.</span><span class="sxs-lookup"><span data-stu-id="ba40e-111">When there are threads waiting for samples, the value of [**CBaseAllocator::m\_lWaiting**](cbaseallocator-m-lwaiting.md) is greater than zero.</span></span> <span data-ttu-id="ba40e-112">Se *m \_ lWaiting* for maior que zero, esse método chamará a função **ReleaseSemaphore** no semáforo [**CBaseAllocator:: m \_ hSem**](cbaseallocator-m-hsem.md) , ativando todos os threads em espera.</span><span class="sxs-lookup"><span data-stu-id="ba40e-112">If *m\_lWaiting* is greater than zero, this method calls the **ReleaseSemaphore** function on the [**CBaseAllocator::m\_hSem**](cbaseallocator-m-hsem.md) semaphore, activating any waiting threads.</span></span> <span data-ttu-id="ba40e-113">Ele também redefine *m \_ lWaiting* para zero.</span><span class="sxs-lookup"><span data-stu-id="ba40e-113">It also resets *m\_lWaiting* to zero.</span></span>

<span data-ttu-id="ba40e-114">Esse método é chamado de dentro do método [**CBaseAllocator:: ReleaseBuffer**](cbaseallocator-releasebuffer.md) , quando um exemplo é retornado para a lista livre; e do método [**CBaseAllocator::D ecommit**](cbaseallocator-decommit.md) , quando o alocador é decommitdo.</span><span class="sxs-lookup"><span data-stu-id="ba40e-114">This method is called from within the [**CBaseAllocator::ReleaseBuffer**](cbaseallocator-releasebuffer.md) method, when a sample is returned to the free list; and from the [**CBaseAllocator::Decommit**](cbaseallocator-decommit.md) method, when the allocator is decommitted.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba40e-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba40e-115">Requirements</span></span>



| <span data-ttu-id="ba40e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba40e-116">Requirement</span></span> | <span data-ttu-id="ba40e-117">Valor</span><span class="sxs-lookup"><span data-stu-id="ba40e-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba40e-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ba40e-118">Header</span></span><br/>  | <dl> <span data-ttu-id="ba40e-119"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ba40e-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ba40e-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ba40e-120">Library</span></span><br/> | <dl> <span data-ttu-id="ba40e-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="ba40e-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba40e-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="ba40e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba40e-123">**Classe CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="ba40e-123">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




