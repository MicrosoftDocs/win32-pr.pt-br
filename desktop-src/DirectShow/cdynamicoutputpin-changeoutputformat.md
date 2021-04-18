---
description: O método ChangeOutputFormat altera dinamicamente o tipo de mídia para a conexão e fornece novas informações de segmento.
ms.assetid: d1204ca0-a489-48a0-8fe5-3ade04f51c93
title: Método CDynamicOutputPin. ChangeOutputFormat (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.ChangeOutputFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 57421b2fd9624d9798037151a5656343e386a497
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755351"
---
# <a name="cdynamicoutputpinchangeoutputformat-method"></a><span data-ttu-id="b64a8-103">Método CDynamicOutputPin. ChangeOutputFormat</span><span class="sxs-lookup"><span data-stu-id="b64a8-103">CDynamicOutputPin.ChangeOutputFormat method</span></span>

<span data-ttu-id="b64a8-104">O `ChangeOutputFormat` método altera dinamicamente o tipo de mídia para a conexão e fornece novas informações de segmento.</span><span class="sxs-lookup"><span data-stu-id="b64a8-104">The `ChangeOutputFormat` method dynamically changes the media type for the connection, and delivers new segment information.</span></span> <span data-ttu-id="b64a8-105">A alteração pode ocorrer enquanto o grafo de filtro está em execução.</span><span class="sxs-lookup"><span data-stu-id="b64a8-105">The change can occur while the filter graph is running.</span></span> <span data-ttu-id="b64a8-106">Depois que esse método é chamado, os exemplos com o tipo de mídia antigo não podem ser entregues.</span><span class="sxs-lookup"><span data-stu-id="b64a8-106">Once this method is called, samples with the old media type cannot be delivered.</span></span> <span data-ttu-id="b64a8-107">O chamador deve garantir que nenhuma amostra antiga esteja pendente.</span><span class="sxs-lookup"><span data-stu-id="b64a8-107">The caller must ensure that no old samples are pending.</span></span>

## <a name="syntax"></a><span data-ttu-id="b64a8-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b64a8-108">Syntax</span></span>


```C++
HRESULT ChangeOutputFormat(
   const AM_MEDIA_TYPE  *pmt,
         REFERENCE_TIME tSegmentStart,
         REFERENCE_TIME tSegmentStop,
         double         dSegmentRate
);
```



## <a name="parameters"></a><span data-ttu-id="b64a8-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b64a8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b64a8-110">*PMT*</span><span class="sxs-lookup"><span data-stu-id="b64a8-110">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="b64a8-111">Ponteiro para uma estrutura de [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) que especifica o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="b64a8-111">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that specifies the media type.</span></span>

</dd> <dt>

<span data-ttu-id="b64a8-112">*tSegmentStart*</span><span class="sxs-lookup"><span data-stu-id="b64a8-112">*tSegmentStart*</span></span> 
</dt> <dd>

<span data-ttu-id="b64a8-113">Hora de início do segmento.</span><span class="sxs-lookup"><span data-stu-id="b64a8-113">Start time of the segment.</span></span>

</dd> <dt>

<span data-ttu-id="b64a8-114">*tSegmentStop*</span><span class="sxs-lookup"><span data-stu-id="b64a8-114">*tSegmentStop*</span></span> 
</dt> <dd>

<span data-ttu-id="b64a8-115">Hora de parada do segmento.</span><span class="sxs-lookup"><span data-stu-id="b64a8-115">Stop time of the segment.</span></span>

</dd> <dt>

<span data-ttu-id="b64a8-116">*dSegmentRate*</span><span class="sxs-lookup"><span data-stu-id="b64a8-116">*dSegmentRate*</span></span> 
</dt> <dd>

<span data-ttu-id="b64a8-117">Taxa de segmento.</span><span class="sxs-lookup"><span data-stu-id="b64a8-117">Segment rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b64a8-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b64a8-118">Return value</span></span>

<span data-ttu-id="b64a8-119">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b64a8-119">Returns an **HRESULT** value.</span></span> <span data-ttu-id="b64a8-120">Os valores possíveis incluem os mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="b64a8-120">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="b64a8-121">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="b64a8-121">Return code</span></span>                                                                                           | <span data-ttu-id="b64a8-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="b64a8-122">Description</span></span>                                                                                                                              |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b64a8-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b64a8-123"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="b64a8-124">Êxito.</span><span class="sxs-lookup"><span data-stu-id="b64a8-124">Success.</span></span><br/>                                                                                                                      |
| <dl> <span data-ttu-id="b64a8-125"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="b64a8-125"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="b64a8-126">Falha.</span><span class="sxs-lookup"><span data-stu-id="b64a8-126">Failure.</span></span> <span data-ttu-id="b64a8-127">Possivelmente o filtro proprietário não chamou [**CDynamicOutputPin:: SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md).</span><span class="sxs-lookup"><span data-stu-id="b64a8-127">Possibly the owning filter did not call [**CDynamicOutputPin::SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md).</span></span><br/> |
| <dl> <span data-ttu-id="b64a8-128"><dt>**VFW \_ E \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="b64a8-128"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="b64a8-129">O PIN não está conectado.</span><span class="sxs-lookup"><span data-stu-id="b64a8-129">The pin is not connected.</span></span><br/>                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="b64a8-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="b64a8-130">Remarks</span></span>

<span data-ttu-id="b64a8-131">Esse método altera o tipo de formato enquanto o filtro está em execução.</span><span class="sxs-lookup"><span data-stu-id="b64a8-131">This method changes the format type while the filter is running.</span></span> <span data-ttu-id="b64a8-132">Se o PIN downstream aceitar o novo formato, nenhuma reconexão será necessária.</span><span class="sxs-lookup"><span data-stu-id="b64a8-132">If the downstream pin accepts the new format, no reconnection is necessary.</span></span> <span data-ttu-id="b64a8-133">Caso contrário, o método tentará reconectar o PIN.</span><span class="sxs-lookup"><span data-stu-id="b64a8-133">Otherwise, the method attempts to reconnect the pin.</span></span> <span data-ttu-id="b64a8-134">Se o método alterar o formato com êxito, ele entregará as novas informações de segmento.</span><span class="sxs-lookup"><span data-stu-id="b64a8-134">If the method successfully changes the format, it delivers the new segment information.</span></span> <span data-ttu-id="b64a8-135">Esse método chama o método [**CDynamicOutputPin:: ChangeMediaType**](cdynamicoutputpin-changemediatype.md) para executar a alteração de formato.</span><span class="sxs-lookup"><span data-stu-id="b64a8-135">This method calls the [**CDynamicOutputPin::ChangeMediaType**](cdynamicoutputpin-changemediatype.md) method to perform the format change.</span></span>

<span data-ttu-id="b64a8-136">Você deve chamar o método [**CDynamicOutputPin:: StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) antes de chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="b64a8-136">You must call the [**CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) method before calling this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b64a8-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b64a8-137">Requirements</span></span>



| <span data-ttu-id="b64a8-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="b64a8-138">Requirement</span></span> | <span data-ttu-id="b64a8-139">Valor</span><span class="sxs-lookup"><span data-stu-id="b64a8-139">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b64a8-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b64a8-140">Header</span></span><br/>  | <dl> <span data-ttu-id="b64a8-141"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b64a8-141"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b64a8-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b64a8-142">Library</span></span><br/> | <dl> <span data-ttu-id="b64a8-143"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="b64a8-143"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b64a8-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="b64a8-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b64a8-145">**Classe CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="b64a8-145">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




