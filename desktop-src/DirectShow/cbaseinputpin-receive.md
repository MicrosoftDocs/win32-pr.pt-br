---
description: 'O método Receive recebe o exemplo de próxima mídia no fluxo. Esse método implementa o método IMemInputPin:: Receive.'
ms.assetid: 30fefc7b-7c9c-44cd-b58b-2b275dfa2520
title: Método CBaseInputPin. Receive (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 10306d5568ae1754105a4367952cef82f931be99
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747611"
---
# <a name="cbaseinputpinreceive-method"></a><span data-ttu-id="c1c9e-104">Método CBaseInputPin. Receive</span><span class="sxs-lookup"><span data-stu-id="c1c9e-104">CBaseInputPin.Receive method</span></span>

<span data-ttu-id="c1c9e-105">O `Receive` método recebe o próximo exemplo de mídia no fluxo.</span><span class="sxs-lookup"><span data-stu-id="c1c9e-105">The `Receive` method receives the next media sample in the stream.</span></span> <span data-ttu-id="c1c9e-106">Esse método implementa o método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) .</span><span class="sxs-lookup"><span data-stu-id="c1c9e-106">This method implements the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1c9e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c1c9e-107">Syntax</span></span>


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="c1c9e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c1c9e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1c9e-109">*pSample*</span><span class="sxs-lookup"><span data-stu-id="c1c9e-109">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="c1c9e-110">Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do exemplo.</span><span class="sxs-lookup"><span data-stu-id="c1c9e-110">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1c9e-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c1c9e-111">Return value</span></span>

<span data-ttu-id="c1c9e-112">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c1c9e-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="c1c9e-113">Os valores possíveis incluem os listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="c1c9e-113">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="c1c9e-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="c1c9e-114">Return code</span></span>                                                                                             | <span data-ttu-id="c1c9e-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1c9e-115">Description</span></span>                                                |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="c1c9e-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c1c9e-116"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="c1c9e-117">Êxito.</span><span class="sxs-lookup"><span data-stu-id="c1c9e-117">Success.</span></span><br/>                                        |
| <dl> <span data-ttu-id="c1c9e-118"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="c1c9e-118"><dt>**S\_FALSE**</dt></span></span> </dl>                 | <span data-ttu-id="c1c9e-119">O PIN está sendo liberado no momento; o exemplo foi rejeitado.</span><span class="sxs-lookup"><span data-stu-id="c1c9e-119">Pin is currently flushing; sample was rejected.</span></span><br/> |
| <dl> <span data-ttu-id="c1c9e-120"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="c1c9e-120"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="c1c9e-121">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="c1c9e-121">**NULL** pointer argument.</span></span><br/>                      |
| <dl> <span data-ttu-id="c1c9e-122"><dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt></span><span class="sxs-lookup"><span data-stu-id="c1c9e-122"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl> | <span data-ttu-id="c1c9e-123">Tipo de mídia inválido.</span><span class="sxs-lookup"><span data-stu-id="c1c9e-123">Invalid media type.</span></span><br/>                             |
| <dl> <span data-ttu-id="c1c9e-124"><dt>**VFW \_ E \_ erro de tempo de execução \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c1c9e-124"><dt>**VFW\_E\_RUNTIME\_ERROR**</dt></span></span> </dl>   | <span data-ttu-id="c1c9e-125">Ocorreu um erro em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="c1c9e-125">A run-time error occurred.</span></span><br/>                      |
| <dl> <span data-ttu-id="c1c9e-126"><dt>**VFW \_ E \_ estado incorreto \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c1c9e-126"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl>     | <span data-ttu-id="c1c9e-127">O PIN foi interrompido.</span><span class="sxs-lookup"><span data-stu-id="c1c9e-127">The pin is stopped.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="c1c9e-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="c1c9e-128">Remarks</span></span>

<span data-ttu-id="c1c9e-129">O pino de saída upstream chama esse método para entregar um exemplo ao pino de entrada.</span><span class="sxs-lookup"><span data-stu-id="c1c9e-129">The upstream output pin calls this method to deliver a sample to the input pin.</span></span> <span data-ttu-id="c1c9e-130">O PIN de entrada deve seguir um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="c1c9e-130">The input pin must do one of the following:</span></span>

-   <span data-ttu-id="c1c9e-131">Processe o exemplo antes de retornar.</span><span class="sxs-lookup"><span data-stu-id="c1c9e-131">Process the sample before returning.</span></span>
-   <span data-ttu-id="c1c9e-132">Retorne e processe o exemplo em um thread de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c1c9e-132">Return, and process the sample in a worker thread.</span></span>
-   <span data-ttu-id="c1c9e-133">Rejeite o exemplo.</span><span class="sxs-lookup"><span data-stu-id="c1c9e-133">Reject the sample.</span></span>

<span data-ttu-id="c1c9e-134">Se o PIN usar um thread de trabalho para processar o exemplo, adicione uma contagem de referência ao exemplo dentro desse método.</span><span class="sxs-lookup"><span data-stu-id="c1c9e-134">If the pin uses a worker thread to process the sample, add a reference count to the sample inside this method.</span></span> <span data-ttu-id="c1c9e-135">Depois que o método retorna, o pino upstream libera o exemplo.</span><span class="sxs-lookup"><span data-stu-id="c1c9e-135">After the method returns, the upstream pin releases the sample.</span></span> <span data-ttu-id="c1c9e-136">Quando a contagem de referência do exemplo chega a zero, o exemplo retorna ao alocador para reutilização.</span><span class="sxs-lookup"><span data-stu-id="c1c9e-136">When the sample's reference count reaches zero, the sample returns to the allocator for re-use.</span></span>

<span data-ttu-id="c1c9e-137">Esse método é síncrono e pode ser bloqueado.</span><span class="sxs-lookup"><span data-stu-id="c1c9e-137">This method is synchronous and can block.</span></span> <span data-ttu-id="c1c9e-138">Se o método puder ser bloqueado, o método [**CBaseInputPin:: ReceiveCanBlock**](cbaseinputpin-receivecanblock.md) do PIN deverá retornar s \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c1c9e-138">If the method might block, the pin's [**CBaseInputPin::ReceiveCanBlock**](cbaseinputpin-receivecanblock.md) method should return S\_OK.</span></span>

<span data-ttu-id="c1c9e-139">Na classe base, esse método executa as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="c1c9e-139">In the base class, this method performs the following steps:</span></span>

1.  <span data-ttu-id="c1c9e-140">Chama o método [**CBaseInputPin:: CheckStreaming**](cbaseinputpin-checkstreaming.md) para verificar se o PIN pode processar amostras agora.</span><span class="sxs-lookup"><span data-stu-id="c1c9e-140">Calls the [**CBaseInputPin::CheckStreaming**](cbaseinputpin-checkstreaming.md) method to verify that the pin can process samples now.</span></span> <span data-ttu-id="c1c9e-141">Se não puder, por exemplo, se o PIN for interrompido, o método falhará.</span><span class="sxs-lookup"><span data-stu-id="c1c9e-141">If it cannot for example, if the pin is stopped the method fails.</span></span>
2.  <span data-ttu-id="c1c9e-142">Recupera as propriedades de exemplo e verifica se o formato foi alterado (veja abaixo).</span><span class="sxs-lookup"><span data-stu-id="c1c9e-142">Retrieves the sample properties and checks whether the format has changed (see below).</span></span>
3.  <span data-ttu-id="c1c9e-143">Se o formato for alterado, o método chamará o método [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md) para determinar se o novo formato é aceitável.</span><span class="sxs-lookup"><span data-stu-id="c1c9e-143">If the format has changed, the method calls the [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method to determine whether the new format is acceptable.</span></span>
4.  <span data-ttu-id="c1c9e-144">Se o novo formato não for aceitável, o método chamará o método [**CBasePin:: EndOfStream**](cbasepin-endofstream.md) , lançará um \_ evento ERRORABORT do EC e retornará um código de erro.</span><span class="sxs-lookup"><span data-stu-id="c1c9e-144">If the new format is not acceptable, the method calls the [**CBasePin::EndOfStream**](cbasepin-endofstream.md) method, posts an EC\_ERRORABORT event, and returns an error code.</span></span>
5.  <span data-ttu-id="c1c9e-145">Supondo que não houvesse erros, o método retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c1c9e-145">Assuming there were no errors, the method returns S\_OK.</span></span>

<span data-ttu-id="c1c9e-146">Teste para uma alteração de formato da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="c1c9e-146">Test for a format change as follows:</span></span>

-   <span data-ttu-id="c1c9e-147">Se o exemplo der suporte à interface [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) , verifique o membro **dwSampleFlags** da estrutura de [**\_ \_ Propriedades am SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) .</span><span class="sxs-lookup"><span data-stu-id="c1c9e-147">If the sample supports the [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) interface, check the **dwSampleFlags** member of the [**AM\_SAMPLE2\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) structure.</span></span> <span data-ttu-id="c1c9e-148">Se o \_ \_ sinalizador tipochanged de exemplo am estiver presente, o formato será alterado.</span><span class="sxs-lookup"><span data-stu-id="c1c9e-148">If the AM\_SAMPLE\_TYPECHANGED flag is present, the format has changed.</span></span>
-   <span data-ttu-id="c1c9e-149">Caso contrário, se o exemplo não oferecer suporte a **IMediaSample2**, chame o método [**IMediaSample:: GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) .</span><span class="sxs-lookup"><span data-stu-id="c1c9e-149">Otherwise, if the sample does not support **IMediaSample2**, call the [**IMediaSample::GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) method.</span></span> <span data-ttu-id="c1c9e-150">Se o método retornar um valor não **nulo** , o formato terá mudado.</span><span class="sxs-lookup"><span data-stu-id="c1c9e-150">If the method returns a non-**NULL** value, the format has changed.</span></span>

<span data-ttu-id="c1c9e-151">Na classe base, esse método não processa o exemplo.</span><span class="sxs-lookup"><span data-stu-id="c1c9e-151">In the base class, this method does not process the sample.</span></span> <span data-ttu-id="c1c9e-152">A classe derivada deve substituir esse método para executar o processamento.</span><span class="sxs-lookup"><span data-stu-id="c1c9e-152">The derived class must override this method to perform the processing.</span></span> <span data-ttu-id="c1c9e-153">(O que isso envolve depende inteiramente do filtro.) A classe derivada deve chamar o método de classe base, para verificar os erros descritos anteriormente.</span><span class="sxs-lookup"><span data-stu-id="c1c9e-153">(What this entails depends entirely on the filter.) The derived class should call the base-class method, to check for the errors described previously.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1c9e-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1c9e-154">Requirements</span></span>



| <span data-ttu-id="c1c9e-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1c9e-155">Requirement</span></span> | <span data-ttu-id="c1c9e-156">Valor</span><span class="sxs-lookup"><span data-stu-id="c1c9e-156">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1c9e-157">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c1c9e-157">Header</span></span><br/>  | <dl> <span data-ttu-id="c1c9e-158"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c1c9e-158"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c1c9e-159">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c1c9e-159">Library</span></span><br/> | <dl> <span data-ttu-id="c1c9e-160"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="c1c9e-160"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1c9e-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="c1c9e-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1c9e-162">**Classe CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="c1c9e-162">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




