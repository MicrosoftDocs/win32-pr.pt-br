---
description: O método Unlock desbloqueia o objeto da seção crítica.
ms.assetid: 61811e0e-df77-48e9-96d5-b7dff8c8db9b
title: Método CCritSec. Unlock (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec.Unlock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ca84ce452d71d0d3111039d7a95d8f5dd3155058
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749840"
---
# <a name="ccritsecunlock-method"></a><span data-ttu-id="6196f-103">Método CCritSec. Unlock</span><span class="sxs-lookup"><span data-stu-id="6196f-103">CCritSec.Unlock method</span></span>

<span data-ttu-id="6196f-104">O método **Unlock** desbloqueia o objeto da seção crítica.</span><span class="sxs-lookup"><span data-stu-id="6196f-104">The **Unlock** method unlocks the critical section object.</span></span>

## <a name="syntax"></a><span data-ttu-id="6196f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6196f-105">Syntax</span></span>


```C++
void Unlock();
```



## <a name="parameters"></a><span data-ttu-id="6196f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6196f-106">Parameters</span></span>

<span data-ttu-id="6196f-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="6196f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6196f-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6196f-108">Return value</span></span>

<span data-ttu-id="6196f-109">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="6196f-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6196f-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="6196f-110">Remarks</span></span>

<span data-ttu-id="6196f-111">Esse método chama a função [**LeaveCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-leavecriticalsection) .</span><span class="sxs-lookup"><span data-stu-id="6196f-111">This method calls the [**LeaveCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-leavecriticalsection) function.</span></span> <span data-ttu-id="6196f-112">Chame esse método uma vez para cada chamada para o método [**CCritSec:: Lock**](ccritsec-lock.md) .</span><span class="sxs-lookup"><span data-stu-id="6196f-112">Call this method once for each call to the [**CCritSec::Lock**](ccritsec-lock.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="6196f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6196f-113">Requirements</span></span>



| <span data-ttu-id="6196f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6196f-114">Requirement</span></span> | <span data-ttu-id="6196f-115">Valor</span><span class="sxs-lookup"><span data-stu-id="6196f-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6196f-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6196f-116">Header</span></span><br/>  | <dl> <span data-ttu-id="6196f-117"><dt>Wxutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6196f-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="6196f-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6196f-118">Library</span></span><br/> | <dl> <span data-ttu-id="6196f-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="6196f-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6196f-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="6196f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6196f-121">**Classe CCritSec**</span><span class="sxs-lookup"><span data-stu-id="6196f-121">**CCritSec Class**</span></span>](ccritsec.md)
</dt> </dl>

 

