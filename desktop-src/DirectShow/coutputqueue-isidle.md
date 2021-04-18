---
description: O método IsIdle determina se o objeto está aguardando dados.
ms.assetid: be1b5633-f9e9-497e-8b6f-5634eae91273
title: Método COutputQueue. IsIdle (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.IsIdle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9bf8b42189e356659e74398eaa3eefeb5f771a8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754532"
---
# <a name="coutputqueueisidle-method"></a><span data-ttu-id="07650-103">Método COutputQueue. IsIdle</span><span class="sxs-lookup"><span data-stu-id="07650-103">COutputQueue.IsIdle method</span></span>

<span data-ttu-id="07650-104">O `IsIdle` método determina se o objeto está aguardando dados.</span><span class="sxs-lookup"><span data-stu-id="07650-104">The `IsIdle` method determines whether the object is waiting for data.</span></span>

## <a name="syntax"></a><span data-ttu-id="07650-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="07650-105">Syntax</span></span>


```C++
BOOL IsIdle();
```



## <a name="parameters"></a><span data-ttu-id="07650-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="07650-106">Parameters</span></span>

<span data-ttu-id="07650-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="07650-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="07650-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="07650-108">Return value</span></span>

<span data-ttu-id="07650-109">Retornará **true** se o thread estiver aguardando e a matriz de exemplo estiver vazia.</span><span class="sxs-lookup"><span data-stu-id="07650-109">Returns **TRUE** if the thread is waiting and the sample array is empty.</span></span> <span data-ttu-id="07650-110">Caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="07650-110">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="07650-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07650-111">Requirements</span></span>



| <span data-ttu-id="07650-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="07650-112">Requirement</span></span> | <span data-ttu-id="07650-113">Valor</span><span class="sxs-lookup"><span data-stu-id="07650-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07650-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="07650-114">Header</span></span><br/>  | <dl> <span data-ttu-id="07650-115"><dt>Outputq. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="07650-115"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="07650-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="07650-116">Library</span></span><br/> | <dl> <span data-ttu-id="07650-117"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="07650-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07650-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="07650-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07650-119">**Classe COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="07650-119">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




