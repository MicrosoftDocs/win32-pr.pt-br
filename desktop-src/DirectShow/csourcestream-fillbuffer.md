---
description: O método FillBuffer preenche um exemplo de mídia com dados.
ms.assetid: dddad8c7-44f1-4ba3-8fb1-7e7e88e40941
title: Método CSourceStream. FillBuffer (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.FillBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3611ad8b590bb823abccdecf9d3d138c70441a07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761769"
---
# <a name="csourcestreamfillbuffer-method"></a><span data-ttu-id="57fb7-103">Método CSourceStream. FillBuffer</span><span class="sxs-lookup"><span data-stu-id="57fb7-103">CSourceStream.FillBuffer method</span></span>

<span data-ttu-id="57fb7-104">O `FillBuffer` método preenche um exemplo de mídia com dados.</span><span class="sxs-lookup"><span data-stu-id="57fb7-104">The `FillBuffer` method fills a media sample with data.</span></span>

## <a name="syntax"></a><span data-ttu-id="57fb7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="57fb7-105">Syntax</span></span>


```C++
virtual HRESULT FillBuffer(
   IMediaSample *pSample
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="57fb7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="57fb7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57fb7-107">*pSample*</span><span class="sxs-lookup"><span data-stu-id="57fb7-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="57fb7-108">Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do exemplo.</span><span class="sxs-lookup"><span data-stu-id="57fb7-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57fb7-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="57fb7-109">Return value</span></span>

<span data-ttu-id="57fb7-110">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="57fb7-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="57fb7-111">Os valores possíveis incluem os mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="57fb7-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="57fb7-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="57fb7-112">Return code</span></span>                                                                             | <span data-ttu-id="57fb7-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="57fb7-113">Description</span></span>              |
|-----------------------------------------------------------------------------------------|--------------------------|
| <dl> <span data-ttu-id="57fb7-114"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="57fb7-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="57fb7-115">Fim do fluxo</span><span class="sxs-lookup"><span data-stu-id="57fb7-115">End of stream</span></span><br/> |
| <dl> <span data-ttu-id="57fb7-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="57fb7-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="57fb7-117">Sucesso</span><span class="sxs-lookup"><span data-stu-id="57fb7-117">Success</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="57fb7-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="57fb7-118">Remarks</span></span>

<span data-ttu-id="57fb7-119">A classe derivada deve implementar esse método.</span><span class="sxs-lookup"><span data-stu-id="57fb7-119">The derived class must implement this method.</span></span>

<span data-ttu-id="57fb7-120">O exemplo de mídia fornecido a esse método não tem carimbos de data/hora.</span><span class="sxs-lookup"><span data-stu-id="57fb7-120">The media sample given to this method has no time stamps.</span></span> <span data-ttu-id="57fb7-121">A classe derivada deve chamar o método [**IMediaSample:: SetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) para definir os carimbos de data/hora.</span><span class="sxs-lookup"><span data-stu-id="57fb7-121">The derived class should call the [**IMediaSample::SetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) method to set the time stamps.</span></span> <span data-ttu-id="57fb7-122">Se apropriado para o tipo de mídia, a classe derivada também deve definir os tempos de mídia, chamando o método [**IMediaSample:: SetMediaTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatime) .</span><span class="sxs-lookup"><span data-stu-id="57fb7-122">If appropriate for the media type, the derived class should also set the media times, by calling the [**IMediaSample::SetMediaTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatime) method.</span></span> <span data-ttu-id="57fb7-123">Para obter mais informações, consulte [tempo e relógios no DirectShow](time-and-clocks-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="57fb7-123">For more information, see [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span></span>

<span data-ttu-id="57fb7-124">Retorna S \_ false no final do fluxo.</span><span class="sxs-lookup"><span data-stu-id="57fb7-124">Return S\_FALSE at the end of the stream.</span></span> <span data-ttu-id="57fb7-125">Isso faz com que a classe **CSourceStream** envie a notificação de fim de fluxo e pare o loop de processamento de buffer.</span><span class="sxs-lookup"><span data-stu-id="57fb7-125">This causes the **CSourceStream** class to send the end-of-stream notification and halt the buffer processing loop.</span></span> <span data-ttu-id="57fb7-126">Consulte [**CSourceStream::D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="57fb7-126">See [**CSourceStream::DoBufferProcessingLoop**](csourcestream-dobufferprocessingloop.md) for more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="57fb7-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57fb7-127">Requirements</span></span>



| <span data-ttu-id="57fb7-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="57fb7-128">Requirement</span></span> | <span data-ttu-id="57fb7-129">Valor</span><span class="sxs-lookup"><span data-stu-id="57fb7-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57fb7-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="57fb7-130">Header</span></span><br/>  | <dl> <span data-ttu-id="57fb7-131"><dt>Source. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="57fb7-131"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="57fb7-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="57fb7-132">Library</span></span><br/> | <dl> <span data-ttu-id="57fb7-133"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="57fb7-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57fb7-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="57fb7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57fb7-135">**Classe CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="57fb7-135">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




