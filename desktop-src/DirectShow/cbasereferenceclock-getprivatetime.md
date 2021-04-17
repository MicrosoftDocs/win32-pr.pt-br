---
description: O método getprivadotime recupera o tempo real do relógio.
ms.assetid: ce9832cb-4b5a-49a1-9a69-d2fb90b3ed2e
title: Método CBaseReferenceClock. getparticulartime (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.GetPrivateTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 387df10472e4913d33722492bf07601faf08e3ba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754556"
---
# <a name="cbasereferenceclockgetprivatetime-method"></a><span data-ttu-id="26f30-103">Método CBaseReferenceClock. getparticulartime</span><span class="sxs-lookup"><span data-stu-id="26f30-103">CBaseReferenceClock.GetPrivateTime method</span></span>

<span data-ttu-id="26f30-104">O `GetPrivateTime` método recupera o tempo real do relógio.</span><span class="sxs-lookup"><span data-stu-id="26f30-104">The `GetPrivateTime` method retrieves the real time from the clock.</span></span>

## <a name="syntax"></a><span data-ttu-id="26f30-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="26f30-105">Syntax</span></span>


```C++
virtual REFERENCE_TIME GetPrivateTime();
```



## <a name="parameters"></a><span data-ttu-id="26f30-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="26f30-106">Parameters</span></span>

<span data-ttu-id="26f30-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="26f30-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="26f30-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="26f30-108">Return value</span></span>

<span data-ttu-id="26f30-109">Retorna a hora do relógio atual, em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="26f30-109">Returns the current clock time, in 100-nanosecond units.</span></span>

## <a name="remarks"></a><span data-ttu-id="26f30-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="26f30-110">Remarks</span></span>

<span data-ttu-id="26f30-111">Esse método retorna o tempo real relatado pelo relógio.</span><span class="sxs-lookup"><span data-stu-id="26f30-111">This method returns the real time reported by the clock.</span></span> <span data-ttu-id="26f30-112">Os chamadores externos usam o método [**CBaseReferenceClock:: getTime**](cbasereferenceclock-gettime.md) , que chama esse método.</span><span class="sxs-lookup"><span data-stu-id="26f30-112">External callers use the [**CBaseReferenceClock::GetTime**](cbasereferenceclock-gettime.md) method, which calls this method.</span></span> <span data-ttu-id="26f30-113">Ao contrário do método **getTime** , o relógio interno tem permissão para retroceder.</span><span class="sxs-lookup"><span data-stu-id="26f30-113">Unlike the **GetTime** method, the internal clock is allowed to go backward.</span></span> <span data-ttu-id="26f30-114">Se isso acontecer, o método **getTime** continuará retornando a última vez que ele foi relatado, até que o método se ajuste `GetPrivateTime` .</span><span class="sxs-lookup"><span data-stu-id="26f30-114">If that happens, the **GetTime** method continues to return the last time that it reported, until the `GetPrivateTime` method catches up.</span></span>

<span data-ttu-id="26f30-115">Esse método retorna a hora do sistema.</span><span class="sxs-lookup"><span data-stu-id="26f30-115">This method returns the system time.</span></span> <span data-ttu-id="26f30-116">Substitua esse método se o relógio obtiver o tempo de outra fonte.</span><span class="sxs-lookup"><span data-stu-id="26f30-116">Override this method if your clock gets the time from another source.</span></span>

## <a name="requirements"></a><span data-ttu-id="26f30-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26f30-117">Requirements</span></span>



| <span data-ttu-id="26f30-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="26f30-118">Requirement</span></span> | <span data-ttu-id="26f30-119">Valor</span><span class="sxs-lookup"><span data-stu-id="26f30-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26f30-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="26f30-120">Header</span></span><br/>  | <dl> <span data-ttu-id="26f30-121"><dt>Refclock. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="26f30-121"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="26f30-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="26f30-122">Library</span></span><br/> | <dl> <span data-ttu-id="26f30-123"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="26f30-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26f30-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="26f30-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26f30-125">**Classe CBaseReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="26f30-125">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




