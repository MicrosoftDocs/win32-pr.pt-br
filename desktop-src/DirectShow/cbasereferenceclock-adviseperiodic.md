---
description: 'O método AdvisePeriodic cria uma solicitação de aviso periódica. Esse método implementa o método IReferenceClock:: AdvisePeriodic.'
ms.assetid: ddaf0861-df11-4008-8e9c-a0c53929cd3f
title: Método CBaseReferenceClock. AdvisePeriodic (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.AdvisePeriodic
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a582e05756e8d034e5b2d0a1cd8f7eb569dbb842
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754999"
---
# <a name="cbasereferenceclockadviseperiodic-method"></a><span data-ttu-id="9f980-104">Método CBaseReferenceClock. AdvisePeriodic</span><span class="sxs-lookup"><span data-stu-id="9f980-104">CBaseReferenceClock.AdvisePeriodic method</span></span>

<span data-ttu-id="9f980-105">O `AdvisePeriodic` método cria uma solicitação de aviso periódica.</span><span class="sxs-lookup"><span data-stu-id="9f980-105">The `AdvisePeriodic` method creates a periodic advise request.</span></span> <span data-ttu-id="9f980-106">Esse método implementa o método [**IReferenceClock:: AdvisePeriodic**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-adviseperiodic) .</span><span class="sxs-lookup"><span data-stu-id="9f980-106">This method implements the [**IReferenceClock::AdvisePeriodic**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-adviseperiodic) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f980-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9f980-107">Syntax</span></span>


```C++
HRESULT AdvisePeriodic(
   REFERENCE_TIME StartTime,
   REFERENCE_TIME PeriodTime,
   HSEMAPHORE     hSemaphore,
   DWORD_PTR      *pdwAdviseToken
);
```



## <a name="parameters"></a><span data-ttu-id="9f980-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9f980-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f980-109">*StartTime*</span><span class="sxs-lookup"><span data-stu-id="9f980-109">*StartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="9f980-110">Hora da primeira notificação, em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="9f980-110">Time of the first notification, in 100-nanosecond units.</span></span> <span data-ttu-id="9f980-111">Deve ser maior que zero e menor que o \_ tempo máximo.</span><span class="sxs-lookup"><span data-stu-id="9f980-111">Must be greater than zero and less than MAX\_TIME.</span></span>

</dd> <dt>

<span data-ttu-id="9f980-112">*Período de tempo*</span><span class="sxs-lookup"><span data-stu-id="9f980-112">*PeriodTime*</span></span> 
</dt> <dd>

<span data-ttu-id="9f980-113">Tempo entre notificações, em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="9f980-113">Time between notifications, in 100-nanosecond units.</span></span> <span data-ttu-id="9f980-114">Deve ser maior que zero.</span><span class="sxs-lookup"><span data-stu-id="9f980-114">Must be greater than zero.</span></span>

</dd> <dt>

<span data-ttu-id="9f980-115">*hSemaphore*</span><span class="sxs-lookup"><span data-stu-id="9f980-115">*hSemaphore*</span></span> 
</dt> <dd>

<span data-ttu-id="9f980-116">Identificador para um semáforo, criado pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="9f980-116">Handle to a semaphore, created by the caller.</span></span>

</dd> <dt>

<span data-ttu-id="9f980-117">*pdwAdviseToken*</span><span class="sxs-lookup"><span data-stu-id="9f980-117">*pdwAdviseToken*</span></span> 
</dt> <dd>

<span data-ttu-id="9f980-118">Ponteiro para uma variável que recebe um identificador para a solicitação de aviso.</span><span class="sxs-lookup"><span data-stu-id="9f980-118">Pointer to a variable that receives an identifier for the advise request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f980-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9f980-119">Return value</span></span>

<span data-ttu-id="9f980-120">Retorna um dos valores **HRESULT** mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="9f980-120">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="9f980-121">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="9f980-121">Return code</span></span>                                                                                   | <span data-ttu-id="9f980-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="9f980-122">Description</span></span>                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="9f980-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9f980-123"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="9f980-124">Sucesso</span><span class="sxs-lookup"><span data-stu-id="9f980-124">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="9f980-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="9f980-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="9f980-126">Valores de tempo inválidos</span><span class="sxs-lookup"><span data-stu-id="9f980-126">Invalid time values</span></span><br/>       |
| <dl> <span data-ttu-id="9f980-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="9f980-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="9f980-128">Falha</span><span class="sxs-lookup"><span data-stu-id="9f980-128">Failure</span></span><br/>                   |
| <dl> <span data-ttu-id="9f980-129"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="9f980-129"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="9f980-130">Argumento de ponteiro **nulo**</span><span class="sxs-lookup"><span data-stu-id="9f980-130">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9f980-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="9f980-131">Remarks</span></span>

<span data-ttu-id="9f980-132">Em cada hora de notificação, o relógio libera o semáforo especificado no parâmetro *hSemaphore* .</span><span class="sxs-lookup"><span data-stu-id="9f980-132">At each notification time, the clock releases the semaphore specified in the *hSemaphore* parameter.</span></span> <span data-ttu-id="9f980-133">Quando nenhuma notificação adicional for necessária, chame o método [**CBaseReferenceClock:: Unadvise**](cbasereferenceclock-unadvise.md) e passe o valor de *pdwAdviseToken* retornado dessa chamada.</span><span class="sxs-lookup"><span data-stu-id="9f980-133">When no further notifications are required, call the [**CBaseReferenceClock::Unadvise**](cbasereferenceclock-unadvise.md) method and pass the *pdwAdviseToken* value returned from this call.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f980-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f980-134">Requirements</span></span>



| <span data-ttu-id="9f980-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f980-135">Requirement</span></span> | <span data-ttu-id="9f980-136">Valor</span><span class="sxs-lookup"><span data-stu-id="9f980-136">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f980-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9f980-137">Header</span></span><br/>  | <dl> <span data-ttu-id="9f980-138"><dt>Refclock. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9f980-138"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9f980-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9f980-139">Library</span></span><br/> | <dl> <span data-ttu-id="9f980-140"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="9f980-140"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f980-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="9f980-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f980-142">**Classe CBaseReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="9f980-142">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




