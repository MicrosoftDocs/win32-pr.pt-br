---
description: Método destruidor.
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
ms.openlocfilehash: 53587482c5d9cf8f5a772453f220c7633c17d383
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750912"
---
# <a name="cbaseallocatorcbaseallocator-destructor"></a><span data-ttu-id="ca67c-103">Destruidor CBaseAllocator. ~ CBaseAllocator</span><span class="sxs-lookup"><span data-stu-id="ca67c-103">CBaseAllocator.~CBaseAllocator destructor</span></span>

<span data-ttu-id="ca67c-104">Método destruidor.</span><span class="sxs-lookup"><span data-stu-id="ca67c-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca67c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ca67c-105">Syntax</span></span>


```C++
~CBaseAllocator();
```



## <a name="remarks"></a><span data-ttu-id="ca67c-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="ca67c-106">Remarks</span></span>

<span data-ttu-id="ca67c-107">Sempre chame o método [**CBaseAllocator::D ecommit**](cbaseallocator-decommit.md) antes de destruir o objeto.</span><span class="sxs-lookup"><span data-stu-id="ca67c-107">Always call the [**CBaseAllocator::Decommit**](cbaseallocator-decommit.md) method before destroying the object.</span></span> <span data-ttu-id="ca67c-108">O destruidor de classe base não pode chamar **uncommit**, porque esse método chama o método virtual puro [**CBaseAllocator:: Free**](cbaseallocator-free.md).</span><span class="sxs-lookup"><span data-stu-id="ca67c-108">The base-class destructor cannot call **Decommit**, because that method calls the pure virtual method [**CBaseAllocator::Free**](cbaseallocator-free.md).</span></span> <span data-ttu-id="ca67c-109">As classes derivadas devem substituir esse destruidor e chamar a **deconfirmação**.</span><span class="sxs-lookup"><span data-stu-id="ca67c-109">Derived classes should override this destructor and call **Decommit**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca67c-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca67c-110">Requirements</span></span>



| <span data-ttu-id="ca67c-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca67c-111">Requirement</span></span> | <span data-ttu-id="ca67c-112">Valor</span><span class="sxs-lookup"><span data-stu-id="ca67c-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca67c-113">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ca67c-113">Header</span></span><br/>  | <dl> <span data-ttu-id="ca67c-114"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ca67c-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ca67c-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ca67c-115">Library</span></span><br/> | <dl> <span data-ttu-id="ca67c-116"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="ca67c-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca67c-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="ca67c-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca67c-118">**Classe CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="ca67c-118">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




