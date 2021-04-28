---
description: CBaseAllocator. ~ CBaseAllocator destruidor-método Destruitor.
ms.assetid: b1e5653f-d72f-4cde-a8c9-d25763434374
title: CBaseAllocator. ~ CBaseAllocator Destruitor (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.~CBaseAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9a4b754c8937b87a547f4583b3270f5782a6a415
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096414"
---
# <a name="cbaseallocatorcbaseallocator-destructor"></a><span data-ttu-id="49698-103">Destruidor CBaseAllocator. ~ CBaseAllocator</span><span class="sxs-lookup"><span data-stu-id="49698-103">CBaseAllocator.~CBaseAllocator destructor</span></span>

<span data-ttu-id="49698-104">Método destruidor.</span><span class="sxs-lookup"><span data-stu-id="49698-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="49698-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="49698-105">Syntax</span></span>


```C++
~CBaseAllocator();
```



## <a name="remarks"></a><span data-ttu-id="49698-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="49698-106">Remarks</span></span>

<span data-ttu-id="49698-107">Sempre chame o método [**CBaseAllocator::D ecommit**](cbaseallocator-decommit.md) antes de destruir o objeto.</span><span class="sxs-lookup"><span data-stu-id="49698-107">Always call the [**CBaseAllocator::Decommit**](cbaseallocator-decommit.md) method before destroying the object.</span></span> <span data-ttu-id="49698-108">O destruidor de classe base não pode chamar **uncommit**, porque esse método chama o método virtual puro [**CBaseAllocator:: Free**](cbaseallocator-free.md).</span><span class="sxs-lookup"><span data-stu-id="49698-108">The base-class destructor cannot call **Decommit**, because that method calls the pure virtual method [**CBaseAllocator::Free**](cbaseallocator-free.md).</span></span> <span data-ttu-id="49698-109">As classes derivadas devem substituir esse destruidor e chamar a **deconfirmação**.</span><span class="sxs-lookup"><span data-stu-id="49698-109">Derived classes should override this destructor and call **Decommit**.</span></span>

## <a name="requirements"></a><span data-ttu-id="49698-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49698-110">Requirements</span></span>



| <span data-ttu-id="49698-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="49698-111">Requirement</span></span> | <span data-ttu-id="49698-112">Valor</span><span class="sxs-lookup"><span data-stu-id="49698-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49698-113">parâmetro</span><span class="sxs-lookup"><span data-stu-id="49698-113">Header</span></span><br/>  | <dl> <span data-ttu-id="49698-114"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="49698-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="49698-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="49698-115">Library</span></span><br/> | <dl> <span data-ttu-id="49698-116"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="49698-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49698-117">Consulte também</span><span class="sxs-lookup"><span data-stu-id="49698-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49698-118">**Classe CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="49698-118">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




