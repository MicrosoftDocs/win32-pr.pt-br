---
description: 'O método getTime recupera o tempo de referência atual. Esse método implementa o método IReferenceClock:: getTime.'
ms.assetid: 4e4e5954-b899-4741-8b7c-7bc98a3f0404
title: Método CBaseReferenceClock. getTime (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.GetTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a91f0015756d2ccfb545c4039d67434eb6d3c403
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753348"
---
# <a name="cbasereferenceclockgettime-method"></a><span data-ttu-id="e3b73-104">Método CBaseReferenceClock. getTime</span><span class="sxs-lookup"><span data-stu-id="e3b73-104">CBaseReferenceClock.GetTime method</span></span>

<span data-ttu-id="e3b73-105">O `GetTime` método recupera o tempo de referência atual.</span><span class="sxs-lookup"><span data-stu-id="e3b73-105">The `GetTime` method retrieves the current reference time.</span></span> <span data-ttu-id="e3b73-106">Esse método implementa o método [**IReferenceClock:: getTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) .</span><span class="sxs-lookup"><span data-stu-id="e3b73-106">This method implements the [**IReferenceClock::GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3b73-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e3b73-107">Syntax</span></span>


```C++
HRESULT GetTime(
   REFERENCE_TIME *pTime
);
```



## <a name="parameters"></a><span data-ttu-id="e3b73-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e3b73-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3b73-109">*pTime*</span><span class="sxs-lookup"><span data-stu-id="e3b73-109">*pTime*</span></span> 
</dt> <dd>

<span data-ttu-id="e3b73-110">Ponteiro para uma variável que recebe a hora atual, em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="e3b73-110">Pointer to a variable that receives the current time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3b73-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e3b73-111">Return value</span></span>

<span data-ttu-id="e3b73-112">Retorna um dos valores **HRESULT** mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="e3b73-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="e3b73-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="e3b73-113">Return code</span></span>                                                                               | <span data-ttu-id="e3b73-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3b73-114">Description</span></span>                                                 |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="e3b73-115"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="e3b73-115"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="e3b73-116">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="e3b73-116">**NULL** pointer argument.</span></span><br/>                       |
| <dl> <span data-ttu-id="e3b73-117"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="e3b73-117"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="e3b73-118">A hora retornada é igual ao valor anterior.</span><span class="sxs-lookup"><span data-stu-id="e3b73-118">Returned time is the same as the previous value.</span></span><br/> |
| <dl> <span data-ttu-id="e3b73-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e3b73-119"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="e3b73-120">Êxito.</span><span class="sxs-lookup"><span data-stu-id="e3b73-120">Success.</span></span><br/>                                         |



 

## <a name="remarks"></a><span data-ttu-id="e3b73-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="e3b73-121">Remarks</span></span>

<span data-ttu-id="e3b73-122">Esse método chama o método [**CBaseReferenceClock:: Getparticulartime**](cbasereferenceclock-getprivatetime.md) para determinar o tempo real do relógio.</span><span class="sxs-lookup"><span data-stu-id="e3b73-122">This method calls the [**CBaseReferenceClock::GetPrivateTime**](cbasereferenceclock-getprivatetime.md) method to determine the real clock time.</span></span> <span data-ttu-id="e3b73-123">Se a hora do relógio for estritamente maior que o valor anterior, o `GetTime` usará a hora do relógio e retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e3b73-123">If the clock time is strictly greater than the previous value, `GetTime` uses the clock time and returns S\_OK.</span></span> <span data-ttu-id="e3b73-124">Caso contrário, `GetTime` o usará o valor anterior e retornará S \_ false.</span><span class="sxs-lookup"><span data-stu-id="e3b73-124">Otherwise, `GetTime` uses the previous value and returns S\_FALSE.</span></span> <span data-ttu-id="e3b73-125">Portanto, o relógio interno pode ficar recuado por um curto período, sem fazer com que o tempo de referência seja executado retroativamente.</span><span class="sxs-lookup"><span data-stu-id="e3b73-125">Therefore, the internal clock can run backward for a short period, without causing the reference time to run backward.</span></span> <span data-ttu-id="e3b73-126">Em vez disso, o tempo de referência será "paralisado" no mesmo valor até que o relógio interno seja atualizado.</span><span class="sxs-lookup"><span data-stu-id="e3b73-126">Instead, the reference time will "stall" at the same value until the internal clock catches up.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3b73-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3b73-127">Requirements</span></span>



| <span data-ttu-id="e3b73-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3b73-128">Requirement</span></span> | <span data-ttu-id="e3b73-129">Valor</span><span class="sxs-lookup"><span data-stu-id="e3b73-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3b73-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e3b73-130">Header</span></span><br/>  | <dl> <span data-ttu-id="e3b73-131"><dt>Refclock. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e3b73-131"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e3b73-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e3b73-132">Library</span></span><br/> | <dl> <span data-ttu-id="e3b73-133"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="e3b73-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3b73-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="e3b73-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3b73-135">**Classe CBaseReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="e3b73-135">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




