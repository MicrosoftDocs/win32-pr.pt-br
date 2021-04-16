---
description: O método DoBufferProcessingLoop gera dados de mídia e os entrega para o pino de entrada downstream.
ms.assetid: a8dce761-eed6-402d-9115-e21822d7a853
title: Método CSourceStream. DoBufferProcessingLoop (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.DoBufferProcessingLoop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 809694cacf0c30acf88ddf7d14c7f5ea1f654436
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105787145"
---
# <a name="csourcestreamdobufferprocessingloop-method"></a><span data-ttu-id="058ff-103">Método CSourceStream. DoBufferProcessingLoop</span><span class="sxs-lookup"><span data-stu-id="058ff-103">CSourceStream.DoBufferProcessingLoop method</span></span>

<span data-ttu-id="058ff-104">O `DoBufferProcessingLoop` método gera dados de mídia e os entrega para o pino de entrada downstream.</span><span class="sxs-lookup"><span data-stu-id="058ff-104">The `DoBufferProcessingLoop` method generates media data and delivers it to the downstream input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="058ff-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="058ff-105">Syntax</span></span>


```C++
virtual HRESULT DoBufferProcessingLoop();
```



## <a name="parameters"></a><span data-ttu-id="058ff-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="058ff-106">Parameters</span></span>

<span data-ttu-id="058ff-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="058ff-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="058ff-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="058ff-108">Return value</span></span>

<span data-ttu-id="058ff-109">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="058ff-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="058ff-110">Os valores possíveis incluem os mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="058ff-110">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="058ff-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="058ff-111">Return code</span></span>                                                                             | <span data-ttu-id="058ff-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="058ff-112">Description</span></span>                                                             |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="058ff-113"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="058ff-113"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="058ff-114">O thread recebeu uma solicitação de interrupção.</span><span class="sxs-lookup"><span data-stu-id="058ff-114">Thread received a stop request.</span></span><br/>                              |
| <dl> <span data-ttu-id="058ff-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="058ff-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="058ff-116">O fluxo terminou ou o filtro downstream não está aceitando exemplos.</span><span class="sxs-lookup"><span data-stu-id="058ff-116">Stream ended, or downstream filter is not accepting samples.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="058ff-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="058ff-117">Remarks</span></span>

<span data-ttu-id="058ff-118">Esse método implementa o loop principal que processa os dados e os entrega por downstream.</span><span class="sxs-lookup"><span data-stu-id="058ff-118">This method implements the main loop that processes data and delivers it downstream.</span></span> <span data-ttu-id="058ff-119">Cada vez que passa pelo loop, o método recupera um exemplo de mídia vazio do alocador.</span><span class="sxs-lookup"><span data-stu-id="058ff-119">Each time through the loop, the method retrieves an empty media sample from the allocator.</span></span> <span data-ttu-id="058ff-120">Ele passa o exemplo para o método [**CSourceStream:: FillBuffer**](csourcestream-fillbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="058ff-120">It passes the sample to the [**CSourceStream::FillBuffer**](csourcestream-fillbuffer.md) method.</span></span> <span data-ttu-id="058ff-121">O método **FillBuffer** , que a classe derivada deve implementar, gera dados de mídia e os coloca no buffer de exemplo.</span><span class="sxs-lookup"><span data-stu-id="058ff-121">The **FillBuffer** method, which the derived class must implement, generates media data and places it in the sample buffer.</span></span>

<span data-ttu-id="058ff-122">O loop termina quando ocorre um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="058ff-122">The loop ends when any of the following occurs:</span></span>

-   <span data-ttu-id="058ff-123">O método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) do pino de entrada rejeita um exemplo.</span><span class="sxs-lookup"><span data-stu-id="058ff-123">The input pin's [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method rejects a sample.</span></span>
-   <span data-ttu-id="058ff-124">O método **FillBuffer** retorna S \_ false, indicando o final do fluxo ou retorna um código de erro.</span><span class="sxs-lookup"><span data-stu-id="058ff-124">The **FillBuffer** method returns S\_FALSE, indicating the end of the stream, or returns an error code.</span></span>
-   <span data-ttu-id="058ff-125">O thread recebe uma solicitação [**CSourceStream:: Stop**](csourcestream-stop.md) .</span><span class="sxs-lookup"><span data-stu-id="058ff-125">The thread receives a [**CSourceStream::Stop**](csourcestream-stop.md) request.</span></span>

<span data-ttu-id="058ff-126">O `DoBufferProcessingLoop` método manipula a notificação de fim de fluxo.</span><span class="sxs-lookup"><span data-stu-id="058ff-126">The `DoBufferProcessingLoop` method handles the end-of-stream notification.</span></span> <span data-ttu-id="058ff-127">Se ocorrer um erro, ele enviará um evento [**\_ ERRORABORT do EC**](ec-errorabort.md) para o Gerenciador do grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="058ff-127">If an error occurs, it sends an [**EC\_ERRORABORT**](ec-errorabort.md) event to the filter graph manager.</span></span>

## <a name="requirements"></a><span data-ttu-id="058ff-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="058ff-128">Requirements</span></span>



| <span data-ttu-id="058ff-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="058ff-129">Requirement</span></span> | <span data-ttu-id="058ff-130">Valor</span><span class="sxs-lookup"><span data-stu-id="058ff-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="058ff-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="058ff-131">Header</span></span><br/>  | <dl> <span data-ttu-id="058ff-132"><dt>Source. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="058ff-132"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="058ff-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="058ff-133">Library</span></span><br/> | <dl> <span data-ttu-id="058ff-134"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="058ff-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="058ff-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="058ff-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="058ff-136">**Classe CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="058ff-136">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




