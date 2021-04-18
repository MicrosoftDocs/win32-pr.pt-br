---
description: 'O método Receive recebe um exemplo de mídia, processa-o e entrega um exemplo de saída para o filtro downstream. Esse método substitui o método CTransformFilter:: Receive.'
ms.assetid: 35e22a63-471e-4ca8-be3b-d84920cec7cb
title: Método CVideoTransformFilter. Receive (Vtrans. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bdc33773a31a7c9ddfd7adb0f3fb20f8fcf6d520
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759082"
---
# <a name="cvideotransformfilterreceive-method"></a><span data-ttu-id="c315b-104">Método CVideoTransformFilter. Receive</span><span class="sxs-lookup"><span data-stu-id="c315b-104">CVideoTransformFilter.Receive method</span></span>

<span data-ttu-id="c315b-105">O `Receive` método recebe um exemplo de mídia, processa-o e entrega um exemplo de saída para o filtro downstream.</span><span class="sxs-lookup"><span data-stu-id="c315b-105">The `Receive` method receives a media sample, processes it, and delivers an output sample to the downstream filter.</span></span> <span data-ttu-id="c315b-106">Esse método substitui o método [**CTransformFilter:: Receive**](ctransformfilter-receive.md) .</span><span class="sxs-lookup"><span data-stu-id="c315b-106">This method overrides the [**CTransformFilter::Receive**](ctransformfilter-receive.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c315b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c315b-107">Syntax</span></span>


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="c315b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c315b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c315b-109">*pSample*</span><span class="sxs-lookup"><span data-stu-id="c315b-109">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="c315b-110">Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) no exemplo de entrada.</span><span class="sxs-lookup"><span data-stu-id="c315b-110">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface on the input sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c315b-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c315b-111">Return value</span></span>

<span data-ttu-id="c315b-112">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c315b-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="c315b-113">Os possíveis valores incluem os seguintes:</span><span class="sxs-lookup"><span data-stu-id="c315b-113">Possible values include the following:</span></span>



| <span data-ttu-id="c315b-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="c315b-114">Return code</span></span>                                                                             | <span data-ttu-id="c315b-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="c315b-115">Description</span></span>                                                 |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="c315b-116"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="c315b-116"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="c315b-117">O filtro upstream deve parar de enviar amostras.</span><span class="sxs-lookup"><span data-stu-id="c315b-117">The upstream filter should stop sending samples.</span></span><br/> |
| <dl> <span data-ttu-id="c315b-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c315b-118"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="c315b-119">Êxito.</span><span class="sxs-lookup"><span data-stu-id="c315b-119">Success.</span></span><br/>                                         |



 

## <a name="remarks"></a><span data-ttu-id="c315b-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="c315b-120">Remarks</span></span>

<span data-ttu-id="c315b-121">Esse método chama [**CVideoTransformFilter:: ShouldSkipFrame**](cvideotransformfilter-shouldskipframe.md) para determinar se ele deve entregar esse exemplo ou simplesmente descartá-lo.</span><span class="sxs-lookup"><span data-stu-id="c315b-121">This method calls [**CVideoTransformFilter::ShouldSkipFrame**](cvideotransformfilter-shouldskipframe.md) to determine whether it should deliver this sample or simply discard it.</span></span> <span data-ttu-id="c315b-122">Se **ShouldSkipFrame** retornar **false** (indicando que o exemplo deve ser entregue), o método fará o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c315b-122">If **ShouldSkipFrame** returns **FALSE** (indicating the sample should be delivered), the method does the following:</span></span>

1.  <span data-ttu-id="c315b-123">Chama [**CTransformFilter:: InitializeOutputSample**](ctransformfilter-initializeoutputsample.md) para preparar o exemplo de saída</span><span class="sxs-lookup"><span data-stu-id="c315b-123">Calls [**CTransformFilter::InitializeOutputSample**](ctransformfilter-initializeoutputsample.md) to prepare the output sample</span></span>
2.  <span data-ttu-id="c315b-124">Chama [**CTransformFilter:: Transform**](ctransformfilter-transform.md) para processar o exemplo de entrada.</span><span class="sxs-lookup"><span data-stu-id="c315b-124">Calls [**CTransformFilter::Transform**](ctransformfilter-transform.md) to process the input sample.</span></span> <span data-ttu-id="c315b-125">Esse método é virtual puro e deve ser implementado na classe derivada.</span><span class="sxs-lookup"><span data-stu-id="c315b-125">This method is pure virtual, and must be implemented in the derived class.</span></span>
3.  <span data-ttu-id="c315b-126">Chama [**CBaseOutputPin::D eliver**](cbaseoutputpin-deliver.md) para entregar o exemplo de saída.</span><span class="sxs-lookup"><span data-stu-id="c315b-126">Calls [**CBaseOutputPin::Deliver**](cbaseoutputpin-deliver.md) to deliver the output sample.</span></span>

<span data-ttu-id="c315b-127">Além disso, esse método verifica as alterações de formato no exemplo de entrada ou saída, chamando [**IMediaSample:: GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype).</span><span class="sxs-lookup"><span data-stu-id="c315b-127">Also, this method checks for format changes on the input or output sample, by calling [**IMediaSample::GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype).</span></span> <span data-ttu-id="c315b-128">Se houver uma alteração de formato, o método definirá o tipo de conexão no PIN correspondente.</span><span class="sxs-lookup"><span data-stu-id="c315b-128">If there is a format change, the method sets the connection type on the corresponding pin.</span></span> <span data-ttu-id="c315b-129">Antes de definir o novo tipo, ele chama **StopStreaming**.</span><span class="sxs-lookup"><span data-stu-id="c315b-129">Before it sets the new type, it calls **StopStreaming**.</span></span> <span data-ttu-id="c315b-130">Depois de definir o novo tipo, ele chama **StartStreaming**.</span><span class="sxs-lookup"><span data-stu-id="c315b-130">After it sets the new type, it calls **StartStreaming**.</span></span> <span data-ttu-id="c315b-131">A classe derivada pode usar esses métodos para atualizar seu estado interno.</span><span class="sxs-lookup"><span data-stu-id="c315b-131">The derived class can use these methods to update its internal state.</span></span> <span data-ttu-id="c315b-132">A classe derivada também pode precisar verificar o novo formato em seu método de **transformação** .</span><span class="sxs-lookup"><span data-stu-id="c315b-132">The derived class might also need to check for the new format in its **Transform** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c315b-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c315b-133">Requirements</span></span>



| <span data-ttu-id="c315b-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="c315b-134">Requirement</span></span> | <span data-ttu-id="c315b-135">Valor</span><span class="sxs-lookup"><span data-stu-id="c315b-135">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c315b-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c315b-136">Header</span></span><br/>  | <dl> <span data-ttu-id="c315b-137"><dt>Vtrans. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c315b-137"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="c315b-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c315b-138">Library</span></span><br/> | <dl> <span data-ttu-id="c315b-139"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="c315b-139"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c315b-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="c315b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c315b-141">**Classe CVideoTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="c315b-141">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




