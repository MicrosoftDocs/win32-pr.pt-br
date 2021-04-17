---
description: O método PeekAllocator retorna um ponteiro para o alocador do PIN. O método não incrementa a contagem de referência na interface.
ms.assetid: 3653d472-059c-426c-8e81-4f7cbd1a8ec3
title: Método CTransInPlaceOutputPin. PeekAllocator (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.PeekAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 805de37e2df2bf5a198107eea69d9107e799598c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759083"
---
# <a name="ctransinplaceoutputpinpeekallocator-method"></a><span data-ttu-id="ae635-104">Método CTransInPlaceOutputPin. PeekAllocator</span><span class="sxs-lookup"><span data-stu-id="ae635-104">CTransInPlaceOutputPin.PeekAllocator method</span></span>

<span data-ttu-id="ae635-105">O `PeekAllocator` método retorna um ponteiro para o alocador do PIN.</span><span class="sxs-lookup"><span data-stu-id="ae635-105">The `PeekAllocator` method returns a pointer to the pin's allocator.</span></span> <span data-ttu-id="ae635-106">O método não incrementa a contagem de referência na interface.</span><span class="sxs-lookup"><span data-stu-id="ae635-106">The method does not increment the reference count on the interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae635-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ae635-107">Syntax</span></span>


```C++
IMemAllocator* PeekAllocator();
```



## <a name="parameters"></a><span data-ttu-id="ae635-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ae635-108">Parameters</span></span>

<span data-ttu-id="ae635-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="ae635-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ae635-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ae635-110">Return value</span></span>

<span data-ttu-id="ae635-111">Retorna a variável de membro [**CBaseOutputPin:: m \_ pAllocator**](cbaseoutputpin-m-pallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="ae635-111">Returns the [**CBaseOutputPin::m\_pAllocator**](cbaseoutputpin-m-pallocator.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae635-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae635-112">Requirements</span></span>



| <span data-ttu-id="ae635-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae635-113">Requirement</span></span> | <span data-ttu-id="ae635-114">Valor</span><span class="sxs-lookup"><span data-stu-id="ae635-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae635-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ae635-115">Header</span></span><br/>  | <dl> <span data-ttu-id="ae635-116"><dt>TRANSip. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ae635-116"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ae635-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ae635-117">Library</span></span><br/> | <dl> <span data-ttu-id="ae635-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="ae635-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae635-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="ae635-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae635-120">**Classe CTransInPlaceOutputPin**</span><span class="sxs-lookup"><span data-stu-id="ae635-120">**CTransInPlaceOutputPin Class**</span></span>](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




