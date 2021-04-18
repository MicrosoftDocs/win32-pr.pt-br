---
description: Se o fim do fluxo for atingido, o método SendEndOfStream agendará um \_ evento de conclusão do EC para o Gerenciador do grafo de filtro.
ms.assetid: 3c10c956-e352-4796-a8cd-cc69a02066f2
title: Método CBaseRenderer. SendEndOfStream (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SendEndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f04e4c8c90796aafb64870a9d59d38b0a33e7435
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769236"
---
# <a name="cbaserenderersendendofstream-method"></a><span data-ttu-id="09eb1-103">Método CBaseRenderer. SendEndOfStream</span><span class="sxs-lookup"><span data-stu-id="09eb1-103">CBaseRenderer.SendEndOfStream method</span></span>

<span data-ttu-id="09eb1-104">Se o fim do fluxo for atingido, o `SendEndOfStream` método agendará um \_ evento de conclusão do EC para o Gerenciador do grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="09eb1-104">If end-of-stream was reached, the `SendEndOfStream` method schedules an EC\_COMPLETE event for the filter graph manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="09eb1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="09eb1-105">Syntax</span></span>


```C++
virtual HRESULT SendEndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="09eb1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="09eb1-106">Parameters</span></span>

<span data-ttu-id="09eb1-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="09eb1-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="09eb1-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="09eb1-108">Return value</span></span>

<span data-ttu-id="09eb1-109">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="09eb1-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="09eb1-110">Os valores possíveis incluem os da tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="09eb1-110">Possible values include those in the following table.</span></span>



| <span data-ttu-id="09eb1-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="09eb1-111">Return code</span></span>                                                                             | <span data-ttu-id="09eb1-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="09eb1-112">Description</span></span>                                                               |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="09eb1-113"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="09eb1-113"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="09eb1-114">O Gerenciador do grafo de filtro não está aceitando notificações de eventos.</span><span class="sxs-lookup"><span data-stu-id="09eb1-114">The filter graph manager is not accepting event notifications.</span></span><br/> |
| <dl> <span data-ttu-id="09eb1-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="09eb1-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="09eb1-116">Êxito.</span><span class="sxs-lookup"><span data-stu-id="09eb1-116">Success.</span></span><br/>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="09eb1-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="09eb1-117">Remarks</span></span>

<span data-ttu-id="09eb1-118">O filtro pode receber uma notificação de fim de fluxo antes da hora de parada do exemplo atual.</span><span class="sxs-lookup"><span data-stu-id="09eb1-118">The filter might receive an end-of-stream notification before the current sample's stop time.</span></span> <span data-ttu-id="09eb1-119">Nesse caso, o filtro deve aguardar antes de lançar uma notificação de [**\_ conclusão do EC**](ec-complete.md) para o Gerenciador do grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="09eb1-119">If so, the filter should wait before posting an [**EC\_COMPLETE**](ec-complete.md) notification to the filter graph manager.</span></span>

<span data-ttu-id="09eb1-120">Portanto:</span><span class="sxs-lookup"><span data-stu-id="09eb1-120">Therefore:</span></span>

-   <span data-ttu-id="09eb1-121">Se o filtro tiver recebido uma notificação de fim de fluxo (EOS) antecipada, esse método agendará um evento de temporizador.</span><span class="sxs-lookup"><span data-stu-id="09eb1-121">If the filter has received an early end-of-stream (EOS) notification, this method schedules a timer event.</span></span> <span data-ttu-id="09eb1-122">Quando o evento de timer é ativado, o filtro posta o \_ evento de conclusão do EC.</span><span class="sxs-lookup"><span data-stu-id="09eb1-122">When the timer event is activated, the filter posts the EC\_COMPLETE event.</span></span>
-   <span data-ttu-id="09eb1-123">Se o filtro tiver recebido uma notificação de EOS que não foi cedo, esse método lançará o evento de conclusão do EC \_ imediatamente.</span><span class="sxs-lookup"><span data-stu-id="09eb1-123">If the filter has received an EOS notification that was not early, this method posts the EC\_COMPLETE event immediately.</span></span>
-   <span data-ttu-id="09eb1-124">Se o filtro não tiver nenhuma notificação de EOS pendente, o método retornará sem fazer nada.</span><span class="sxs-lookup"><span data-stu-id="09eb1-124">If the filter does not have any pending EOS notification, the method returns without doing anything.</span></span>

<span data-ttu-id="09eb1-125">O método de retorno de chamada do temporizador é [**CBaseRenderer:: TimerCallback**](cbaserenderer-timercallback.md).</span><span class="sxs-lookup"><span data-stu-id="09eb1-125">The timer callback method is [**CBaseRenderer::TimerCallback**](cbaserenderer-timercallback.md).</span></span> <span data-ttu-id="09eb1-126">Para entregar o \_ evento EC Complete, o filtro chama o método [**CBaseRenderer:: NotifyEndOfStream**](cbaserenderer-notifyendofstream.md) .</span><span class="sxs-lookup"><span data-stu-id="09eb1-126">To deliver the EC\_COMPLETE event, the filter calls the [**CBaseRenderer::NotifyEndOfStream**](cbaserenderer-notifyendofstream.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="09eb1-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09eb1-127">Requirements</span></span>



| <span data-ttu-id="09eb1-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="09eb1-128">Requirement</span></span> | <span data-ttu-id="09eb1-129">Valor</span><span class="sxs-lookup"><span data-stu-id="09eb1-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09eb1-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="09eb1-130">Header</span></span><br/>  | <dl> <span data-ttu-id="09eb1-131"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="09eb1-131"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="09eb1-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="09eb1-132">Library</span></span><br/> | <dl> <span data-ttu-id="09eb1-133"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="09eb1-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09eb1-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="09eb1-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09eb1-135">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="09eb1-135">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




