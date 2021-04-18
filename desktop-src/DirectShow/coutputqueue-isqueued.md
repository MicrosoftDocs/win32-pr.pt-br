---
description: O método isqueueed determina se o objeto está usando um thread de trabalho para fornecer exemplos.
ms.assetid: 8d26661f-6cd7-42ea-bc4b-8746d22a7ca0
title: Método COutputQueue. isqueueed (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.IsQueued
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 47093acedb3a28d633ea2c8b0bbdbba3c1493de7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756591"
---
# <a name="coutputqueueisqueued-method"></a><span data-ttu-id="98f53-103">Método COutputQueue. isqueueed</span><span class="sxs-lookup"><span data-stu-id="98f53-103">COutputQueue.IsQueued method</span></span>

<span data-ttu-id="98f53-104">O `IsQueued` método determina se o objeto está usando um thread de trabalho para fornecer exemplos.</span><span class="sxs-lookup"><span data-stu-id="98f53-104">The `IsQueued` method determines whether the object is using a worker thread to deliver samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="98f53-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="98f53-105">Syntax</span></span>


```C++
BOOL IsQueued();
```



## <a name="parameters"></a><span data-ttu-id="98f53-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="98f53-106">Parameters</span></span>

<span data-ttu-id="98f53-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="98f53-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="98f53-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="98f53-108">Return value</span></span>

<span data-ttu-id="98f53-109">Retornará **true** se o objeto estiver usando um thread de trabalho ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="98f53-109">Returns **TRUE** if the object is using a worker thread, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="98f53-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98f53-110">Requirements</span></span>



| <span data-ttu-id="98f53-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="98f53-111">Requirement</span></span> | <span data-ttu-id="98f53-112">Valor</span><span class="sxs-lookup"><span data-stu-id="98f53-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98f53-113">parâmetro</span><span class="sxs-lookup"><span data-stu-id="98f53-113">Header</span></span><br/>  | <dl> <span data-ttu-id="98f53-114"><dt>Outputq. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="98f53-114"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="98f53-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="98f53-115">Library</span></span><br/> | <dl> <span data-ttu-id="98f53-116"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="98f53-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98f53-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="98f53-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98f53-118">**Classe COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="98f53-118">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




