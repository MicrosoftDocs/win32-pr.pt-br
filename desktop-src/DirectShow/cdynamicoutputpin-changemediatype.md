---
description: O método ChangeMediaType altera dinamicamente o tipo de mídia para a conexão.
ms.assetid: 38efdfdc-f636-4cad-b8d3-8c63a277644e
title: Método CDynamicOutputPin. ChangeMediaType (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.ChangeMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 89c15e3076a95f8fee3f2f2970fc59da5cf3bf4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751896"
---
# <a name="cdynamicoutputpinchangemediatype-method"></a><span data-ttu-id="7e0f2-103">Método CDynamicOutputPin. ChangeMediaType</span><span class="sxs-lookup"><span data-stu-id="7e0f2-103">CDynamicOutputPin.ChangeMediaType method</span></span>

<span data-ttu-id="7e0f2-104">O `ChangeMediaType` método altera dinamicamente o tipo de mídia para a conexão.</span><span class="sxs-lookup"><span data-stu-id="7e0f2-104">The `ChangeMediaType` method dynamically changes the media type for the connection.</span></span> <span data-ttu-id="7e0f2-105">A alteração pode ocorrer enquanto o grafo de filtro está em execução.</span><span class="sxs-lookup"><span data-stu-id="7e0f2-105">The change can occur while the filter graph is running.</span></span> <span data-ttu-id="7e0f2-106">Depois que esse método é chamado, os exemplos com o tipo de mídia antigo não podem ser entregues.</span><span class="sxs-lookup"><span data-stu-id="7e0f2-106">Once this method is called, samples with the old media type cannot be delivered.</span></span> <span data-ttu-id="7e0f2-107">O chamador deve garantir que nenhuma amostra antiga esteja pendente.</span><span class="sxs-lookup"><span data-stu-id="7e0f2-107">The caller must ensure that no old samples are pending.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e0f2-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7e0f2-108">Syntax</span></span>


```C++
HRESULT ChangeMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="7e0f2-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7e0f2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e0f2-110">*PMT*</span><span class="sxs-lookup"><span data-stu-id="7e0f2-110">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="7e0f2-111">Ponteiro para uma estrutura de [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) que especifica o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="7e0f2-111">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e0f2-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7e0f2-112">Return value</span></span>

<span data-ttu-id="7e0f2-113">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7e0f2-113">Returns an **HRESULT** value.</span></span> <span data-ttu-id="7e0f2-114">Os valores possíveis incluem os mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="7e0f2-114">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="7e0f2-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="7e0f2-115">Return code</span></span>                                                                                           | <span data-ttu-id="7e0f2-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="7e0f2-116">Description</span></span>                                                                                                                              |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7e0f2-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7e0f2-117"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="7e0f2-118">Êxito.</span><span class="sxs-lookup"><span data-stu-id="7e0f2-118">Success.</span></span><br/>                                                                                                                      |
| <dl> <span data-ttu-id="7e0f2-119"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="7e0f2-119"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="7e0f2-120">Falha.</span><span class="sxs-lookup"><span data-stu-id="7e0f2-120">Failure.</span></span> <span data-ttu-id="7e0f2-121">Possivelmente o filtro proprietário não chamou [**CDynamicOutputPin:: SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md).</span><span class="sxs-lookup"><span data-stu-id="7e0f2-121">Possibly the owning filter did not call [**CDynamicOutputPin::SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md).</span></span><br/> |
| <dl> <span data-ttu-id="7e0f2-122"><dt>**VFW \_ E \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="7e0f2-122"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="7e0f2-123">O PIN não está conectado.</span><span class="sxs-lookup"><span data-stu-id="7e0f2-123">The pin is not connected.</span></span><br/>                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="7e0f2-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="7e0f2-124">Remarks</span></span>

<span data-ttu-id="7e0f2-125">Chame o método [**CDynamicOutputPin:: StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) antes de chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="7e0f2-125">Call the [**CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) method before calling this method.</span></span>

<span data-ttu-id="7e0f2-126">Esse método verifica primeiro se o PIN de entrada downstream pode aceitar o novo formato sem reconectar.</span><span class="sxs-lookup"><span data-stu-id="7e0f2-126">This method first checks whether the downstream input pin can accept the new format without reconnecting.</span></span> <span data-ttu-id="7e0f2-127">Ele consulta o pino de entrada para a interface [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection) .</span><span class="sxs-lookup"><span data-stu-id="7e0f2-127">It queries the input pin for the [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection) interface.</span></span> <span data-ttu-id="7e0f2-128">Se o PIN de entrada der suporte a **IPinConnection**, o método chamará o método [**IPinConnection::D ynamicqueryaccept**](/windows/desktop/api/Strmif/nf-strmif-ipinconnection-dynamicqueryaccept) com o tipo de mídia proposto.</span><span class="sxs-lookup"><span data-stu-id="7e0f2-128">If the input pin supports **IPinConnection**, the method calls the [**IPinConnection::DynamicQueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipinconnection-dynamicqueryaccept) method with the proposed media type.</span></span> <span data-ttu-id="7e0f2-129">Se o PIN de entrada aceitar o novo tipo de mídia, o método chamará o método [**IPin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) e renegociará os requisitos de alocador.</span><span class="sxs-lookup"><span data-stu-id="7e0f2-129">If the input pin accepts the new media type, the method calls the [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) method and renegotiates the allocator requirements.</span></span>

<span data-ttu-id="7e0f2-130">Por outro lado, se o PIN downstream não oferecer suporte a **IPinConnection**, ou se rejeitar o novo tipo de mídia, o método chamará o método [**CDynamicOutputPin::D ynamicreconnect**](cdynamicoutputpin-dynamicreconnect.md) para executar uma reconexão dinâmica.</span><span class="sxs-lookup"><span data-stu-id="7e0f2-130">On the other hand, if the downstream pin does not support **IPinConnection**, or if it rejects the new media type, the method calls the [**CDynamicOutputPin::DynamicReconnect**](cdynamicoutputpin-dynamicreconnect.md) method to perform a dynamic reconnection.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e0f2-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e0f2-131">Requirements</span></span>



| <span data-ttu-id="7e0f2-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e0f2-132">Requirement</span></span> | <span data-ttu-id="7e0f2-133">Valor</span><span class="sxs-lookup"><span data-stu-id="7e0f2-133">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e0f2-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7e0f2-134">Header</span></span><br/>  | <dl> <span data-ttu-id="7e0f2-135"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7e0f2-135"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7e0f2-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7e0f2-136">Library</span></span><br/> | <dl> <span data-ttu-id="7e0f2-137"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="7e0f2-137"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e0f2-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="7e0f2-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e0f2-139">**Classe CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="7e0f2-139">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




