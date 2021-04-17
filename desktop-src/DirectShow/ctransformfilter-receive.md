---
description: O método Receive recebe um exemplo de mídia, processa-o e entrega um exemplo de saída para o filtro downstream.
ms.assetid: 036b209a-3535-4922-b7e9-dbed25b812f5
title: Método CTransformFilter. Receive (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 67924bffc4d4d80b998e686d80d0e50afcd040ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748618"
---
# <a name="ctransformfilterreceive-method"></a><span data-ttu-id="7a754-103">Método CTransformFilter. Receive</span><span class="sxs-lookup"><span data-stu-id="7a754-103">CTransformFilter.Receive method</span></span>

<span data-ttu-id="7a754-104">O `Receive` método recebe um exemplo de mídia, processa-o e entrega um exemplo de saída para o filtro downstream.</span><span class="sxs-lookup"><span data-stu-id="7a754-104">The `Receive` method receives a media sample, processes it, and delivers an output sample to the downstream filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a754-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7a754-105">Syntax</span></span>


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="7a754-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7a754-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a754-107">*pSample*</span><span class="sxs-lookup"><span data-stu-id="7a754-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="7a754-108">Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) no exemplo de entrada.</span><span class="sxs-lookup"><span data-stu-id="7a754-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface on the input sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a754-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7a754-109">Return value</span></span>

<span data-ttu-id="7a754-110">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7a754-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="7a754-111">Os possíveis valores incluem os seguintes:</span><span class="sxs-lookup"><span data-stu-id="7a754-111">Possible values include the following:</span></span>



| <span data-ttu-id="7a754-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="7a754-112">Return code</span></span>                                                                             | <span data-ttu-id="7a754-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="7a754-113">Description</span></span>                                                 |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="7a754-114"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="7a754-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="7a754-115">O filtro upstream deve parar de enviar amostras.</span><span class="sxs-lookup"><span data-stu-id="7a754-115">The upstream filter should stop sending samples.</span></span><br/> |
| <dl> <span data-ttu-id="7a754-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7a754-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="7a754-117">Êxito.</span><span class="sxs-lookup"><span data-stu-id="7a754-117">Success.</span></span><br/>                                         |



 

## <a name="remarks"></a><span data-ttu-id="7a754-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="7a754-118">Remarks</span></span>

<span data-ttu-id="7a754-119">O pino de entrada do filtro chama esse método quando recebe um exemplo.</span><span class="sxs-lookup"><span data-stu-id="7a754-119">The filter's input pin calls this method when it receives a sample.</span></span> <span data-ttu-id="7a754-120">Esse método chama o método [**CTransformFilter:: InitializeOutputSample**](ctransformfilter-initializeoutputsample.md) , que prepara um novo exemplo de saída.</span><span class="sxs-lookup"><span data-stu-id="7a754-120">This method calls the [**CTransformFilter::InitializeOutputSample**](ctransformfilter-initializeoutputsample.md) method, which prepares a new output sample.</span></span> <span data-ttu-id="7a754-121">Em seguida, ele chama o método [**CTransformFilter:: Transform**](ctransformfilter-transform.md) , que a classe derivada deve implementar.</span><span class="sxs-lookup"><span data-stu-id="7a754-121">Then it calls the [**CTransformFilter::Transform**](ctransformfilter-transform.md) method, which the derived class must implement.</span></span> <span data-ttu-id="7a754-122">O método **Transform** processa os dados de entrada e produz dados de saída.</span><span class="sxs-lookup"><span data-stu-id="7a754-122">The **Transform** method processes the input data and produces output data.</span></span>

<span data-ttu-id="7a754-123">Se o método **Transform** retornar S \_ false, o `Receive` método descartará esse exemplo.</span><span class="sxs-lookup"><span data-stu-id="7a754-123">If the **Transform** method returns S\_FALSE, the `Receive` method drops this sample.</span></span> <span data-ttu-id="7a754-124">Na primeira amostra descartada, o filtro envia um evento de [**\_ \_ alteração de qualidade do EC**](ec-quality-change.md) para o Gerenciador do grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="7a754-124">On the first dropped sample, the filter sends an [**EC\_QUALITY\_CHANGE**](ec-quality-change.md) event to the filter graph manager.</span></span> <span data-ttu-id="7a754-125">Caso contrário, se o método **Transform** retornar S \_ OK, o filtro entregará o exemplo de saída.</span><span class="sxs-lookup"><span data-stu-id="7a754-125">Otherwise, if the **Transform** method returns S\_OK, the filter delivers the output sample.</span></span> <span data-ttu-id="7a754-126">Para fazer isso, ele chama o método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) no pino de entrada downstream.</span><span class="sxs-lookup"><span data-stu-id="7a754-126">To do so, it calls the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method on the downstream input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a754-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a754-127">Requirements</span></span>



| <span data-ttu-id="7a754-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a754-128">Requirement</span></span> | <span data-ttu-id="7a754-129">Valor</span><span class="sxs-lookup"><span data-stu-id="7a754-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a754-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7a754-130">Header</span></span><br/>  | <dl> <span data-ttu-id="7a754-131"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7a754-131"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7a754-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7a754-132">Library</span></span><br/> | <dl> <span data-ttu-id="7a754-133"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="7a754-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a754-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="7a754-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a754-135">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="7a754-135">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




