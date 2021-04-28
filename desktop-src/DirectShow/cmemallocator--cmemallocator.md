---
description: CMemAllocator. ~ CMemAllocator destruidor-método Destruitor.
ms.assetid: e0a04d93-fb77-4dc1-9bc8-7d3965bc6803
title: CMemAllocator. ~ CMemAllocator Destruitor (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.~CMemAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 43b0505ee34df72ab82e4204b08440ac1a2558b5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095404"
---
# <a name="cmemallocatorcmemallocator-destructor"></a><span data-ttu-id="5316b-103">Destruidor CMemAllocator. ~ CMemAllocator</span><span class="sxs-lookup"><span data-stu-id="5316b-103">CMemAllocator.~CMemAllocator destructor</span></span>

<span data-ttu-id="5316b-104">Método destruidor.</span><span class="sxs-lookup"><span data-stu-id="5316b-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5316b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5316b-105">Syntax</span></span>


```C++
~CMemAllocator();
```



## <a name="remarks"></a><span data-ttu-id="5316b-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="5316b-106">Remarks</span></span>

<span data-ttu-id="5316b-107">Esse método substitui o destruidor de classe base para chamar [**CBaseAllocator::D ecommit**](cbaseallocator-decommit.md) e [**CMemAllocator:: ReallyFree**](cmemallocator-reallyfree.md).</span><span class="sxs-lookup"><span data-stu-id="5316b-107">This method overrides the base-class destructor to call [**CBaseAllocator::Decommit**](cbaseallocator-decommit.md) and [**CMemAllocator::ReallyFree**](cmemallocator-reallyfree.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5316b-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5316b-108">Requirements</span></span>



| <span data-ttu-id="5316b-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="5316b-109">Requirement</span></span> | <span data-ttu-id="5316b-110">Valor</span><span class="sxs-lookup"><span data-stu-id="5316b-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5316b-111">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5316b-111">Header</span></span><br/>  | <dl> <span data-ttu-id="5316b-112"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5316b-112"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5316b-113">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5316b-113">Library</span></span><br/> | <dl> <span data-ttu-id="5316b-114"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="5316b-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5316b-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="5316b-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5316b-116">**Classe CMemAllocator**</span><span class="sxs-lookup"><span data-stu-id="5316b-116">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 




