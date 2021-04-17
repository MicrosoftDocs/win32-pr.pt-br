---
description: O método Set sinaliza o evento.
ms.assetid: dfcb1601-aa65-47f5-ae3c-f13fcd7b1398
title: Método CAMEvent. Set (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.Set
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c9caeed17d42d121ae9263bf6c1fcd011ed573c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780447"
---
# <a name="cameventset-method"></a><span data-ttu-id="4ca02-103">Método CAMEvent. Set</span><span class="sxs-lookup"><span data-stu-id="4ca02-103">CAMEvent.Set method</span></span>

<span data-ttu-id="4ca02-104">O `Set` método sinaliza o evento.</span><span class="sxs-lookup"><span data-stu-id="4ca02-104">The `Set` method signals the event.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ca02-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4ca02-105">Syntax</span></span>


```C++
void Set();
```



## <a name="parameters"></a><span data-ttu-id="4ca02-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4ca02-106">Parameters</span></span>

<span data-ttu-id="4ca02-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="4ca02-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4ca02-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4ca02-108">Return value</span></span>

<span data-ttu-id="4ca02-109">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="4ca02-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ca02-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="4ca02-110">Remarks</span></span>

<span data-ttu-id="4ca02-111">O comportamento depende se o objeto é um evento de redefinição automática ou um evento de redefinição manual:</span><span class="sxs-lookup"><span data-stu-id="4ca02-111">The behavior depends on whether the object is an auto-reset event or a manual-reset event:</span></span>

-   <span data-ttu-id="4ca02-112">**Redefinição automática**: se algum thread estiver aguardando esse evento, um thread será liberado e o evento será redefinido.</span><span class="sxs-lookup"><span data-stu-id="4ca02-112">**Auto-reset**: If any threads are waiting on this event, one thread is released and the event is reset.</span></span> <span data-ttu-id="4ca02-113">Se nenhum thread estiver aguardando esse evento, o evento permanecerá sinalizado.</span><span class="sxs-lookup"><span data-stu-id="4ca02-113">If no threads are waiting on this event, the event remains signaled.</span></span>
-   <span data-ttu-id="4ca02-114">**Redefinição manual**: todos os threads aguardando esse evento são liberados.</span><span class="sxs-lookup"><span data-stu-id="4ca02-114">**Manual-reset**: All the threads waiting on this event are released.</span></span> <span data-ttu-id="4ca02-115">O evento permanece sinalizado.</span><span class="sxs-lookup"><span data-stu-id="4ca02-115">The event remains signaled.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ca02-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ca02-116">Requirements</span></span>



| <span data-ttu-id="4ca02-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ca02-117">Requirement</span></span> | <span data-ttu-id="4ca02-118">Valor</span><span class="sxs-lookup"><span data-stu-id="4ca02-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ca02-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4ca02-119">Header</span></span><br/>  | <dl> <span data-ttu-id="4ca02-120"><dt>Wxutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4ca02-120"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="4ca02-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4ca02-121">Library</span></span><br/> | <dl> <span data-ttu-id="4ca02-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="4ca02-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ca02-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="4ca02-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ca02-124">**Classe CAMEvent**</span><span class="sxs-lookup"><span data-stu-id="4ca02-124">**CAMEvent Class**</span></span>](camevent.md)
</dt> </dl>

 

 




