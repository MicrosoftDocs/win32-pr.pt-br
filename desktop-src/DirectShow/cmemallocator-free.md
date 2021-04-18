---
description: O método gratuito é chamado durante uma operação de desconfirmação.
ms.assetid: 71a84730-ca71-4418-bf76-52fd42fc7a5a
title: Método CMemAllocator. Free (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.Free
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b707bb5b2a35466c47d05690a0f57f278d784542
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778498"
---
# <a name="cmemallocatorfree-method"></a><span data-ttu-id="d3f4d-103">Método CMemAllocator. Free</span><span class="sxs-lookup"><span data-stu-id="d3f4d-103">CMemAllocator.Free method</span></span>

<span data-ttu-id="d3f4d-104">O `Free` método é chamado durante uma operação de desconfirmação.</span><span class="sxs-lookup"><span data-stu-id="d3f4d-104">The `Free` method is called during a decommit operation.</span></span> <span data-ttu-id="d3f4d-105">Esse método implementa o método puramente virtual [**CBaseAllocator:: Free**](cbaseallocator-free.md) , mas não faz nada.</span><span class="sxs-lookup"><span data-stu-id="d3f4d-105">This method implements the pure virtual [**CBaseAllocator::Free**](cbaseallocator-free.md) method, but does nothing.</span></span> <span data-ttu-id="d3f4d-106">A memória de buffer não é realmente liberada até que o objeto **CMemAllocator** seja destruído.</span><span class="sxs-lookup"><span data-stu-id="d3f4d-106">The buffer memory is not actually released until the **CMemAllocator** object is destroyed.</span></span> <span data-ttu-id="d3f4d-107">O método destruidor chama [**CMemAllocator:: ReallyFree**](cmemallocator-reallyfree.md) para liberar a memória.</span><span class="sxs-lookup"><span data-stu-id="d3f4d-107">The destructor method calls [**CMemAllocator::ReallyFree**](cmemallocator-reallyfree.md) to release the memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3f4d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d3f4d-108">Syntax</span></span>


```C++
void Free();
```



## <a name="parameters"></a><span data-ttu-id="d3f4d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d3f4d-109">Parameters</span></span>

<span data-ttu-id="d3f4d-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="d3f4d-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d3f4d-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d3f4d-111">Return value</span></span>

<span data-ttu-id="d3f4d-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="d3f4d-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3f4d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3f4d-113">Requirements</span></span>



| <span data-ttu-id="d3f4d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3f4d-114">Requirement</span></span> | <span data-ttu-id="d3f4d-115">Valor</span><span class="sxs-lookup"><span data-stu-id="d3f4d-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3f4d-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d3f4d-116">Header</span></span><br/>  | <dl> <span data-ttu-id="d3f4d-117"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d3f4d-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d3f4d-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d3f4d-118">Library</span></span><br/> | <dl> <span data-ttu-id="d3f4d-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="d3f4d-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3f4d-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="d3f4d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3f4d-121">**Classe CMemAllocator**</span><span class="sxs-lookup"><span data-stu-id="d3f4d-121">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 




