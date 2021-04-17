---
description: Método destruidor.
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
ms.openlocfilehash: d49046eccd8d7ef71c4eeb4c75acffbf90f7d826
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756196"
---
# <a name="cmemallocatorcmemallocator-destructor"></a><span data-ttu-id="a1b16-103">Destruidor CMemAllocator. ~ CMemAllocator</span><span class="sxs-lookup"><span data-stu-id="a1b16-103">CMemAllocator.~CMemAllocator destructor</span></span>

<span data-ttu-id="a1b16-104">Método destruidor.</span><span class="sxs-lookup"><span data-stu-id="a1b16-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1b16-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a1b16-105">Syntax</span></span>


```C++
~CMemAllocator();
```



## <a name="remarks"></a><span data-ttu-id="a1b16-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="a1b16-106">Remarks</span></span>

<span data-ttu-id="a1b16-107">Esse método substitui o destruidor de classe base para chamar [**CBaseAllocator::D ecommit**](cbaseallocator-decommit.md) e [**CMemAllocator:: ReallyFree**](cmemallocator-reallyfree.md).</span><span class="sxs-lookup"><span data-stu-id="a1b16-107">This method overrides the base-class destructor to call [**CBaseAllocator::Decommit**](cbaseallocator-decommit.md) and [**CMemAllocator::ReallyFree**](cmemallocator-reallyfree.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a1b16-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1b16-108">Requirements</span></span>



| <span data-ttu-id="a1b16-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1b16-109">Requirement</span></span> | <span data-ttu-id="a1b16-110">Valor</span><span class="sxs-lookup"><span data-stu-id="a1b16-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1b16-111">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a1b16-111">Header</span></span><br/>  | <dl> <span data-ttu-id="a1b16-112"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a1b16-112"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a1b16-113">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a1b16-113">Library</span></span><br/> | <dl> <span data-ttu-id="a1b16-114"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="a1b16-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1b16-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="a1b16-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1b16-116">**Classe CMemAllocator**</span><span class="sxs-lookup"><span data-stu-id="a1b16-116">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 




