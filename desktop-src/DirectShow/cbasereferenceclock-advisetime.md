---
description: 'O método Aconselhetime cria uma solicitação de aviso de uma amostra. Esse método implementa o método IReferenceClock:: Aconselhetime.'
ms.assetid: 4849a04d-35f2-4a24-bf5d-f20e541f5e99
title: Método CBaseReferenceClock. AdviseTime (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.AdviseTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 326fc5e0939803ab66e0466fbf32351387977019
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749029"
---
# <a name="cbasereferenceclockadvisetime-method"></a><span data-ttu-id="196e2-104">Método CBaseReferenceClock. AdviseTime</span><span class="sxs-lookup"><span data-stu-id="196e2-104">CBaseReferenceClock.AdviseTime method</span></span>

<span data-ttu-id="196e2-105">O `AdviseTime` método cria uma solicitação de aviso de uma imagem.</span><span class="sxs-lookup"><span data-stu-id="196e2-105">The `AdviseTime` method creates a one-shot advise request.</span></span> <span data-ttu-id="196e2-106">Esse método implementa o método [**IReferenceClock:: aconselhetime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) .</span><span class="sxs-lookup"><span data-stu-id="196e2-106">This method implements the [**IReferenceClock::AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="196e2-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="196e2-107">Syntax</span></span>


```C++
HRESULT AdviseTime(
   REFERENCE_TIME baseTime,
   REFERENCE_TIME streamTime,
   HEVENT         hEvent,
   DWORD_PTR      *pdwAdviseToken
);
```



## <a name="parameters"></a><span data-ttu-id="196e2-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="196e2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="196e2-109">*baseTime*</span><span class="sxs-lookup"><span data-stu-id="196e2-109">*baseTime*</span></span> 
</dt> <dd>

<span data-ttu-id="196e2-110">Tempo de referência base, em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="196e2-110">Base reference time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="196e2-111">*fluxo de transmissão*</span><span class="sxs-lookup"><span data-stu-id="196e2-111">*streamTime*</span></span> 
</dt> <dd>

<span data-ttu-id="196e2-112">Tempo de deslocamento de fluxo, em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="196e2-112">Stream offset time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="196e2-113">*hEvent*</span><span class="sxs-lookup"><span data-stu-id="196e2-113">*hEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="196e2-114">Identificador para um evento, criado pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="196e2-114">Handle to an event, created by the caller.</span></span>

</dd> <dt>

<span data-ttu-id="196e2-115">*pdwAdviseToken*</span><span class="sxs-lookup"><span data-stu-id="196e2-115">*pdwAdviseToken*</span></span> 
</dt> <dd>

<span data-ttu-id="196e2-116">Ponteiro para uma variável que recebe um identificador para a solicitação de aviso.</span><span class="sxs-lookup"><span data-stu-id="196e2-116">Pointer to a variable that receives an identifier for the advise request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="196e2-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="196e2-117">Return value</span></span>

<span data-ttu-id="196e2-118">Retorna um dos valores **HRESULT** mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="196e2-118">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="196e2-119">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="196e2-119">Return code</span></span>                                                                                   | <span data-ttu-id="196e2-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="196e2-120">Description</span></span>                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="196e2-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="196e2-121"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="196e2-122">Sucesso</span><span class="sxs-lookup"><span data-stu-id="196e2-122">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="196e2-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="196e2-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="196e2-124">Valores de tempo inválidos</span><span class="sxs-lookup"><span data-stu-id="196e2-124">Invalid time values</span></span><br/>       |
| <dl> <span data-ttu-id="196e2-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="196e2-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="196e2-126">Falha</span><span class="sxs-lookup"><span data-stu-id="196e2-126">Failure</span></span><br/>                   |
| <dl> <span data-ttu-id="196e2-127"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="196e2-127"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="196e2-128">Argumento de ponteiro **nulo**</span><span class="sxs-lookup"><span data-stu-id="196e2-128">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="196e2-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="196e2-129">Remarks</span></span>

<span data-ttu-id="196e2-130">Esse método cria uma solicitação de aviso de uma imagem para o tempo de referência de *baseTime*  +  *streamtime*.</span><span class="sxs-lookup"><span data-stu-id="196e2-130">This method creates a one-shot advise request for the reference time *baseTime* + *streamTime*.</span></span> <span data-ttu-id="196e2-131">A soma deve ser maior que zero e menor que \_ o tempo máximo, ou o método retorna E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="196e2-131">The sum must be greater than zero and less than MAX\_TIME, or the method returns E\_INVALIDARG.</span></span> <span data-ttu-id="196e2-132">Na hora solicitada, o relógio sinaliza o evento especificado no parâmetro *hEvent* .</span><span class="sxs-lookup"><span data-stu-id="196e2-132">At the requested time, the clock signals the event specified in the *hEvent* parameter.</span></span>

<span data-ttu-id="196e2-133">Para cancelar a notificação antes da hora ser atingida, chame o método [**CBaseReferenceClock:: Unadvise**](cbasereferenceclock-unadvise.md) e passe o valor de *pdwAdviseToken* retornado dessa chamada.</span><span class="sxs-lookup"><span data-stu-id="196e2-133">To cancel the notification before the time is reached, call the [**CBaseReferenceClock::Unadvise**](cbasereferenceclock-unadvise.md) method and pass the *pdwAdviseToken* value returned from this call.</span></span> <span data-ttu-id="196e2-134">Depois que a notificação tiver ocorrido, o relógio a limpará automaticamente, portanto, não é necessário chamar **Unadvise**.</span><span class="sxs-lookup"><span data-stu-id="196e2-134">After the notification has occurred, the clock automatically clears it, so it is not necessary to call **Unadvise**.</span></span> <span data-ttu-id="196e2-135">No entanto, não é um erro fazer isso.</span><span class="sxs-lookup"><span data-stu-id="196e2-135">However, it is not an error to do so.</span></span>

## <a name="requirements"></a><span data-ttu-id="196e2-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="196e2-136">Requirements</span></span>



| <span data-ttu-id="196e2-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="196e2-137">Requirement</span></span> | <span data-ttu-id="196e2-138">Valor</span><span class="sxs-lookup"><span data-stu-id="196e2-138">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="196e2-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="196e2-139">Header</span></span><br/>  | <dl> <span data-ttu-id="196e2-140"><dt>Refclock. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="196e2-140"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="196e2-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="196e2-141">Library</span></span><br/> | <dl> <span data-ttu-id="196e2-142"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="196e2-142"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="196e2-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="196e2-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="196e2-144">**Classe CBaseReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="196e2-144">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




