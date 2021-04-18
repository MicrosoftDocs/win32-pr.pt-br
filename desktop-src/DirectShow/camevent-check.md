---
description: O método check verifica se o evento está definido, sem bloqueio.
ms.assetid: b8e55798-fd8e-4442-bc35-08887d8a3129
title: Método CAMEvent. check (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.Check
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1a112d1b9484acb4d7e9cc2992b8dee629f40e23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758887"
---
# <a name="cameventcheck-method"></a><span data-ttu-id="e223f-103">Método CAMEvent. check</span><span class="sxs-lookup"><span data-stu-id="e223f-103">CAMEvent.Check method</span></span>

<span data-ttu-id="e223f-104">O `Check` método verifica se o evento está definido, sem bloqueio.</span><span class="sxs-lookup"><span data-stu-id="e223f-104">The `Check` method checks whether the event is set, without blocking.</span></span>

## <a name="syntax"></a><span data-ttu-id="e223f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e223f-105">Syntax</span></span>


```C++
BOOL Check();
```



## <a name="parameters"></a><span data-ttu-id="e223f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e223f-106">Parameters</span></span>

<span data-ttu-id="e223f-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="e223f-107">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="e223f-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="e223f-108">Remarks</span></span>

<span data-ttu-id="e223f-109">Retornará **true** se o evento for definido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="e223f-109">Returns **TRUE** if the event is set, or **FALSE** otherwise.</span></span> <span data-ttu-id="e223f-110">Esse método chama o método [**CAMEvent:: Wait**](camevent-wait.md) com um tempo limite de zero.</span><span class="sxs-lookup"><span data-stu-id="e223f-110">This method calls the [**CAMEvent::Wait**](camevent-wait.md) method with a time-out of zero.</span></span> <span data-ttu-id="e223f-111">Se o objeto for um evento de redefinição automática, esse método redefinirá o evento.</span><span class="sxs-lookup"><span data-stu-id="e223f-111">If the object is an auto-reset event, this method resets the event.</span></span>

## <a name="requirements"></a><span data-ttu-id="e223f-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e223f-112">Requirements</span></span>



| <span data-ttu-id="e223f-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="e223f-113">Requirement</span></span> | <span data-ttu-id="e223f-114">Valor</span><span class="sxs-lookup"><span data-stu-id="e223f-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e223f-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e223f-115">Header</span></span><br/>  | <dl> <span data-ttu-id="e223f-116"><dt>Wxutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e223f-116"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="e223f-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e223f-117">Library</span></span><br/> | <dl> <span data-ttu-id="e223f-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="e223f-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e223f-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="e223f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e223f-120">**Classe CAMEvent**</span><span class="sxs-lookup"><span data-stu-id="e223f-120">**CAMEvent Class**</span></span>](camevent.md)
</dt> </dl>

 

 




