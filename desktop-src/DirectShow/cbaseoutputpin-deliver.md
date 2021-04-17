---
description: O método de entrega fornece um exemplo de mídia para o pino de entrada conectado.
ms.assetid: b871df84-c69e-42eb-9da9-c25996bf08c3
title: Método CBaseOutputPin. entregue (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.Deliver
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5adc603e4cdd1f49e649264d2d82d6df0fb12569
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769246"
---
# <a name="cbaseoutputpindeliver-method"></a><span data-ttu-id="0893b-103">Método CBaseOutputPin. entregue</span><span class="sxs-lookup"><span data-stu-id="0893b-103">CBaseOutputPin.Deliver method</span></span>

<span data-ttu-id="0893b-104">O `Deliver` método entrega um exemplo de mídia para o pino de entrada conectado.</span><span class="sxs-lookup"><span data-stu-id="0893b-104">The `Deliver` method delivers a media sample to the connected input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="0893b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0893b-105">Syntax</span></span>


```C++
virtual HRESULT Deliver(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="0893b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0893b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0893b-107">*pSample*</span><span class="sxs-lookup"><span data-stu-id="0893b-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="0893b-108">Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do exemplo.</span><span class="sxs-lookup"><span data-stu-id="0893b-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0893b-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0893b-109">Return value</span></span>

<span data-ttu-id="0893b-110">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0893b-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="0893b-111">Os valores possíveis incluem os listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="0893b-111">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="0893b-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="0893b-112">Return code</span></span>                                                                                           | <span data-ttu-id="0893b-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="0893b-113">Description</span></span>                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="0893b-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0893b-114"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="0893b-115">Êxito.</span><span class="sxs-lookup"><span data-stu-id="0893b-115">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="0893b-116"><dt>**VFW \_ E \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="0893b-116"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="0893b-117">O PIN não está conectado.</span><span class="sxs-lookup"><span data-stu-id="0893b-117">Pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0893b-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="0893b-118">Remarks</span></span>

<span data-ttu-id="0893b-119">Esse método chama o método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) no pino de entrada.</span><span class="sxs-lookup"><span data-stu-id="0893b-119">This method calls the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method on the input pin.</span></span> <span data-ttu-id="0893b-120">**Receive** pode bloquear se o método [**IMemInputPin:: ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) retornar S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0893b-120">**Receive** can block if the [**IMemInputPin::ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) method returns S\_OK.</span></span>

<span data-ttu-id="0893b-121">Libere o exemplo depois de chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="0893b-121">Release the sample after calling this method.</span></span> <span data-ttu-id="0893b-122">O PIN de entrada pode conter uma contagem de referência no exemplo, portanto, não reutilize o exemplo.</span><span class="sxs-lookup"><span data-stu-id="0893b-122">The input pin might hold a reference count on the sample, so do not reuse the sample.</span></span> <span data-ttu-id="0893b-123">Sempre chame o método [**CBaseOutputPin:: GetDeliveryBuffer**](cbaseoutputpin-getdeliverybuffer.md) para obter um novo exemplo.</span><span class="sxs-lookup"><span data-stu-id="0893b-123">Always call the [**CBaseOutputPin::GetDeliveryBuffer**](cbaseoutputpin-getdeliverybuffer.md) method to obtain a new sample.</span></span>

<span data-ttu-id="0893b-124">Mantenha a seção crítica do filtro antes de chamar este método.</span><span class="sxs-lookup"><span data-stu-id="0893b-124">Hold the filter's critical section before calling this method.</span></span> <span data-ttu-id="0893b-125">Caso contrário, o PIN poderá ser desconectado durante a chamada do método.</span><span class="sxs-lookup"><span data-stu-id="0893b-125">Otherwise, the pin might get disconnected during the method call.</span></span> <span data-ttu-id="0893b-126">Se o filtro usar um thread de trabalho para entregar exemplos, mantenha a seção crítica quando o filtro estiver pronto para entregar um exemplo.</span><span class="sxs-lookup"><span data-stu-id="0893b-126">If the filter uses a worker thread to deliver samples, hold the critical section when the filter is ready to deliver a sample.</span></span> <span data-ttu-id="0893b-127">Caso contrário, você pode manter a seção crítica no método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) do filtro, em que o filtro processa amostras.</span><span class="sxs-lookup"><span data-stu-id="0893b-127">Otherwise, you can hold the critical section in the filter's [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method, where the filter processes samples.</span></span>

<span data-ttu-id="0893b-128">Os threads de trabalho podem criar um deadlock potencial.</span><span class="sxs-lookup"><span data-stu-id="0893b-128">Worker threads can create a potential deadlock.</span></span> <span data-ttu-id="0893b-129">Quando o thread mantém a seção crítica, ele pode aguardar uma alteração de estado no filtro.</span><span class="sxs-lookup"><span data-stu-id="0893b-129">When the thread holds the critical section, it might wait on a state change in the filter.</span></span> <span data-ttu-id="0893b-130">Ao mesmo tempo, a alteração de estado pode estar aguardando a conclusão do thread.</span><span class="sxs-lookup"><span data-stu-id="0893b-130">At the same time, the state change might be waiting for the thread to complete.</span></span> <span data-ttu-id="0893b-131">Para evitar isso, o código de alteração de Estado deve sinalizar um evento que encerra o thread e, em seguida, esperar que o thread sinalize a conclusão.</span><span class="sxs-lookup"><span data-stu-id="0893b-131">To prevent this, the state-change code should signal an event that terminates the thread, and then wait for the thread to signal completion.</span></span>

## <a name="requirements"></a><span data-ttu-id="0893b-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0893b-132">Requirements</span></span>



| <span data-ttu-id="0893b-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="0893b-133">Requirement</span></span> | <span data-ttu-id="0893b-134">Valor</span><span class="sxs-lookup"><span data-stu-id="0893b-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0893b-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0893b-135">Header</span></span><br/>  | <dl> <span data-ttu-id="0893b-136"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0893b-136"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0893b-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0893b-137">Library</span></span><br/> | <dl> <span data-ttu-id="0893b-138"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="0893b-138"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0893b-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="0893b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0893b-140">**Classe CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="0893b-140">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




