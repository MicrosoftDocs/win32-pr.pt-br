---
description: O método de desconfirmação deconfirma o alocador. Esse método implementa o método IMemAllocator::D ecommit.
ms.assetid: 0c8d44e0-17ea-4f7f-be44-f9ae2e34fbef
title: Método CBaseAllocator. decommit (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.Decommit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 613af805f1c04a7bf375755ff8f3adba7b70be18
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755624"
---
# <a name="cbaseallocatordecommit-method"></a><span data-ttu-id="86fca-104">Método CBaseAllocator. decommit</span><span class="sxs-lookup"><span data-stu-id="86fca-104">CBaseAllocator.Decommit method</span></span>

<span data-ttu-id="86fca-105">O `Decommit` método desconfirma o alocador.</span><span class="sxs-lookup"><span data-stu-id="86fca-105">The `Decommit` method decommits the allocator.</span></span> <span data-ttu-id="86fca-106">Esse método implementa o método [**IMemAllocator::D ecommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) .</span><span class="sxs-lookup"><span data-stu-id="86fca-106">This method implements the [**IMemAllocator::Decommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="86fca-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="86fca-107">Syntax</span></span>


```C++
HRESULT Decommit();
```



## <a name="parameters"></a><span data-ttu-id="86fca-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="86fca-108">Parameters</span></span>

<span data-ttu-id="86fca-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="86fca-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="86fca-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="86fca-110">Return value</span></span>

<span data-ttu-id="86fca-111">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="86fca-111">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="86fca-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="86fca-112">Remarks</span></span>

<span data-ttu-id="86fca-113">Depois que esse método for chamado, ocorrerá uma falha nas chamadas para o método [**CBaseAllocator:: GetBuffer**](cbaseallocator-getbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="86fca-113">After this method is called, calls to the [**CBaseAllocator::GetBuffer**](cbaseallocator-getbuffer.md) method will fail.</span></span> <span data-ttu-id="86fca-114">Conforme os exemplos são liberados, eles são retornados para a lista gratuita.</span><span class="sxs-lookup"><span data-stu-id="86fca-114">As samples are released, they get returned to the free list.</span></span> <span data-ttu-id="86fca-115">Quando o último exemplo é retornado, o alocador chama o método [**CBaseAllocator:: Free**](cbaseallocator-free.md) , que libera a memória alocada.</span><span class="sxs-lookup"><span data-stu-id="86fca-115">When the last sample is returned, the allocator calls the [**CBaseAllocator::Free**](cbaseallocator-free.md) method, which releases the allocated memory.</span></span> <span data-ttu-id="86fca-116">(Na classe base, **Free** é um método virtual puro.)</span><span class="sxs-lookup"><span data-stu-id="86fca-116">(In the base class, **Free** is a pure virtual method.)</span></span>

<span data-ttu-id="86fca-117">Além disso, esse método libera todos os threads bloqueados em chamadas **GetBuffer** .</span><span class="sxs-lookup"><span data-stu-id="86fca-117">In addition, this method releases any threads that are blocked on **GetBuffer** calls.</span></span> <span data-ttu-id="86fca-118">As chamadas para **GetBuffer** falham.</span><span class="sxs-lookup"><span data-stu-id="86fca-118">The calls to **GetBuffer** fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="86fca-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86fca-119">Requirements</span></span>



| <span data-ttu-id="86fca-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="86fca-120">Requirement</span></span> | <span data-ttu-id="86fca-121">Valor</span><span class="sxs-lookup"><span data-stu-id="86fca-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86fca-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="86fca-122">Header</span></span><br/>  | <dl> <span data-ttu-id="86fca-123"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="86fca-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="86fca-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="86fca-124">Library</span></span><br/> | <dl> <span data-ttu-id="86fca-125"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="86fca-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86fca-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="86fca-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86fca-127">**Classe CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="86fca-127">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




