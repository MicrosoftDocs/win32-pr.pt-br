---
description: Recupera o próximo item da fila.
ms.assetid: 406ae640-5903-427d-91f9-8b01beb1aaa7
title: Método CQueue. GetQueueObject (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CQueue.GetQueueObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c3ae68c0564c7f76f38e91b7d27c8c3deb5ef2b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758531"
---
# <a name="cqueuegetqueueobject-method"></a><span data-ttu-id="3cc43-103">Método CQueue. GetQueueObject</span><span class="sxs-lookup"><span data-stu-id="3cc43-103">CQueue.GetQueueObject method</span></span>

<span data-ttu-id="3cc43-104">Recupera o próximo item da fila.</span><span class="sxs-lookup"><span data-stu-id="3cc43-104">Retrieves the next item from the queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cc43-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3cc43-105">Syntax</span></span>


```C++
T GetQueueObject();
```



## <a name="parameters"></a><span data-ttu-id="3cc43-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3cc43-106">Parameters</span></span>

<span data-ttu-id="3cc43-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="3cc43-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3cc43-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3cc43-108">Return value</span></span>

<span data-ttu-id="3cc43-109">Retorna um objeto do tipo **T** (o tipo de modelo).</span><span class="sxs-lookup"><span data-stu-id="3cc43-109">Returns an object of type **T** (the template type).</span></span>

## <a name="remarks"></a><span data-ttu-id="3cc43-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="3cc43-110">Remarks</span></span>

<span data-ttu-id="3cc43-111">Esse método é bloqueado até que um item esteja disponível na fila.</span><span class="sxs-lookup"><span data-stu-id="3cc43-111">This method blocks until an item is available on the queue.</span></span>

## <a name="requirements"></a><span data-ttu-id="3cc43-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3cc43-112">Requirements</span></span>



| <span data-ttu-id="3cc43-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="3cc43-113">Requirement</span></span> | <span data-ttu-id="3cc43-114">Valor</span><span class="sxs-lookup"><span data-stu-id="3cc43-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cc43-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3cc43-115">Header</span></span><br/>  | <dl> <span data-ttu-id="3cc43-116"><dt>Wxutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3cc43-116"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="3cc43-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3cc43-117">Library</span></span><br/> | <dl> <span data-ttu-id="3cc43-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="3cc43-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3cc43-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="3cc43-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cc43-120">**Classe CQueue**</span><span class="sxs-lookup"><span data-stu-id="3cc43-120">**CQueue Class**</span></span>](cqueue.md)
</dt> </dl>

 

 




