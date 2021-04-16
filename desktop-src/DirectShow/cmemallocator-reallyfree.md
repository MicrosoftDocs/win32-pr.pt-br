---
description: O método ReallyFree libera a memória para os buffers.
ms.assetid: c5c5d09f-b4f2-4a06-9309-3b2a8b8f8f1f
title: Método CMemAllocator. ReallyFree (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.ReallyFree
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 187807658c8e15ddf530ca6687d860fe826f4208
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757697"
---
# <a name="cmemallocatorreallyfree-method"></a><span data-ttu-id="c33df-103">Método CMemAllocator. ReallyFree</span><span class="sxs-lookup"><span data-stu-id="c33df-103">CMemAllocator.ReallyFree method</span></span>

<span data-ttu-id="c33df-104">O `ReallyFree` método libera a memória para os buffers.</span><span class="sxs-lookup"><span data-stu-id="c33df-104">The `ReallyFree` method releases the memory for the buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="c33df-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c33df-105">Syntax</span></span>


```C++
void ReallyFree();
```



## <a name="parameters"></a><span data-ttu-id="c33df-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c33df-106">Parameters</span></span>

<span data-ttu-id="c33df-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="c33df-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c33df-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c33df-108">Return value</span></span>

<span data-ttu-id="c33df-109">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="c33df-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c33df-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="c33df-110">Remarks</span></span>

<span data-ttu-id="c33df-111">A classe [**CMemAllocator**](cmemallocator.md) mantém a memória até que o objeto seja excluído.</span><span class="sxs-lookup"><span data-stu-id="c33df-111">The [**CMemAllocator**](cmemallocator.md) class holds memory until the object is deleted.</span></span>

## <a name="requirements"></a><span data-ttu-id="c33df-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c33df-112">Requirements</span></span>



| <span data-ttu-id="c33df-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="c33df-113">Requirement</span></span> | <span data-ttu-id="c33df-114">Valor</span><span class="sxs-lookup"><span data-stu-id="c33df-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c33df-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c33df-115">Header</span></span><br/>  | <dl> <span data-ttu-id="c33df-116"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c33df-116"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c33df-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c33df-117">Library</span></span><br/> | <dl> <span data-ttu-id="c33df-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="c33df-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c33df-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="c33df-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c33df-120">**Classe CMemAllocator**</span><span class="sxs-lookup"><span data-stu-id="c33df-120">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 




