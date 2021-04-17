---
description: O método PeekAllocator retorna um ponteiro para o alocador do PIN. O método não incrementa a contagem de referência na interface.
ms.assetid: 67f1b872-4ae2-4fbe-9240-801ef8ae1e5b
title: Método CTransInPlaceInputPin. PeekAllocator (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.PeekAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 22358dd776a0536cfbae819ec7cace02dd1775a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812787"
---
# <a name="ctransinplaceinputpinpeekallocator-method"></a><span data-ttu-id="69d4f-104">Método CTransInPlaceInputPin. PeekAllocator</span><span class="sxs-lookup"><span data-stu-id="69d4f-104">CTransInPlaceInputPin.PeekAllocator method</span></span>

<span data-ttu-id="69d4f-105">O `PeekAllocator` método retorna um ponteiro para o alocador do PIN.</span><span class="sxs-lookup"><span data-stu-id="69d4f-105">The `PeekAllocator` method returns a pointer to the pin's allocator.</span></span> <span data-ttu-id="69d4f-106">O método não incrementa a contagem de referência na interface.</span><span class="sxs-lookup"><span data-stu-id="69d4f-106">The method does not increment the reference count on the interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="69d4f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="69d4f-107">Syntax</span></span>


```C++
IMemAllocator* PeekAllocator();
```



## <a name="parameters"></a><span data-ttu-id="69d4f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="69d4f-108">Parameters</span></span>

<span data-ttu-id="69d4f-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="69d4f-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="69d4f-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="69d4f-110">Return value</span></span>

<span data-ttu-id="69d4f-111">Retorna a variável de membro [**CBaseInputPin:: m \_ pAllocator**](cbaseinputpin-m-pallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="69d4f-111">Returns the [**CBaseInputPin::m\_pAllocator**](cbaseinputpin-m-pallocator.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="69d4f-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69d4f-112">Requirements</span></span>



| <span data-ttu-id="69d4f-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="69d4f-113">Requirement</span></span> | <span data-ttu-id="69d4f-114">Valor</span><span class="sxs-lookup"><span data-stu-id="69d4f-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69d4f-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="69d4f-115">Header</span></span><br/>  | <dl> <span data-ttu-id="69d4f-116"><dt>TRANSip. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="69d4f-116"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="69d4f-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="69d4f-117">Library</span></span><br/> | <dl> <span data-ttu-id="69d4f-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="69d4f-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69d4f-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="69d4f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69d4f-120">**Classe CTransInPlaceInputPin**</span><span class="sxs-lookup"><span data-stu-id="69d4f-120">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




