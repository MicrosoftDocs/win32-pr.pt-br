---
description: O método setaguardando incrementa a contagem de threads em espera.
ms.assetid: 4aec6177-fb32-44be-a58e-41a4f4aaf4f2
title: Método CBaseAllocator. setaguardating (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.SetWaiting
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 92cba22e128a76f7884050d74a7819142c696dc9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752918"
---
# <a name="cbaseallocatorsetwaiting-method"></a><span data-ttu-id="44d92-103">Método CBaseAllocator. setaguardando</span><span class="sxs-lookup"><span data-stu-id="44d92-103">CBaseAllocator.SetWaiting method</span></span>

<span data-ttu-id="44d92-104">O `SetWaiting` método incrementa a contagem de threads em espera.</span><span class="sxs-lookup"><span data-stu-id="44d92-104">The `SetWaiting` method increments the count of waiting threads.</span></span>

## <a name="syntax"></a><span data-ttu-id="44d92-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="44d92-105">Syntax</span></span>


```C++
void SetWaiting();
```



## <a name="parameters"></a><span data-ttu-id="44d92-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="44d92-106">Parameters</span></span>

<span data-ttu-id="44d92-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="44d92-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="44d92-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="44d92-108">Return value</span></span>

<span data-ttu-id="44d92-109">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="44d92-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="44d92-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="44d92-110">Remarks</span></span>

<span data-ttu-id="44d92-111">Esse método incrementa a variável de membro [**CBaseAllocator:: m \_ lWaiting**](cbaseallocator-m-lwaiting.md) .</span><span class="sxs-lookup"><span data-stu-id="44d92-111">This method increments the [**CBaseAllocator::m\_lWaiting**](cbaseallocator-m-lwaiting.md) member variable.</span></span> <span data-ttu-id="44d92-112">Se um thread estiver bloqueado no método [**CBaseAllocator:: GetBuffer**](cbaseallocator-getbuffer.md) , o alocador chamará `SetWaiting` e esperará que o semáforo de [**CBaseAllocator:: m \_ hSem**](cbaseallocator-m-hsem.md) seja sinalizado.</span><span class="sxs-lookup"><span data-stu-id="44d92-112">If a thread is blocked in the [**CBaseAllocator::GetBuffer**](cbaseallocator-getbuffer.md) method, the allocator calls `SetWaiting` and then waits for the [**CBaseAllocator::m\_hSem**](cbaseallocator-m-hsem.md) semaphore to be signaled.</span></span> <span data-ttu-id="44d92-113">O método [**CBaseAllocator:: ReleaseBuffer**](cbaseallocator-releasebuffer.md) sinaliza o semáforo e define *m \_ lWaiting* de volta como zero.</span><span class="sxs-lookup"><span data-stu-id="44d92-113">The [**CBaseAllocator::ReleaseBuffer**](cbaseallocator-releasebuffer.md) method signals the semaphore and sets *m\_lWaiting* back to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="44d92-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44d92-114">Requirements</span></span>



| <span data-ttu-id="44d92-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="44d92-115">Requirement</span></span> | <span data-ttu-id="44d92-116">Valor</span><span class="sxs-lookup"><span data-stu-id="44d92-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44d92-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="44d92-117">Header</span></span><br/>  | <dl> <span data-ttu-id="44d92-118"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="44d92-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="44d92-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="44d92-119">Library</span></span><br/> | <dl> <span data-ttu-id="44d92-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="44d92-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44d92-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="44d92-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44d92-122">**Classe CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="44d92-122">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




