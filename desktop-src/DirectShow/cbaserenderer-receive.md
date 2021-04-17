---
description: O método Receive recebe o exemplo de próxima mídia no fluxo.
ms.assetid: b340f76c-2305-444f-bc00-1ef5acdea329
title: Método CBaseRenderer. Receive (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 96abb2ee3d44604c23e9943e086a52312a011e92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770292"
---
# <a name="cbaserendererreceive-method"></a><span data-ttu-id="fdc48-103">Método CBaseRenderer. Receive</span><span class="sxs-lookup"><span data-stu-id="fdc48-103">CBaseRenderer.Receive method</span></span>

<span data-ttu-id="fdc48-104">O `Receive` método recebe o próximo exemplo de mídia no fluxo.</span><span class="sxs-lookup"><span data-stu-id="fdc48-104">The `Receive` method receives the next media sample in the stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="fdc48-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fdc48-105">Syntax</span></span>


```C++
virtual Receive(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="fdc48-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fdc48-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fdc48-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="fdc48-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="fdc48-108">Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do exemplo.</span><span class="sxs-lookup"><span data-stu-id="fdc48-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fdc48-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fdc48-109">Return value</span></span>

<span data-ttu-id="fdc48-110">Retorna S \_ OK se bem-sucedido ou um valor **HRESULT** que indica a causa do erro.</span><span class="sxs-lookup"><span data-stu-id="fdc48-110">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="fdc48-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="fdc48-111">Remarks</span></span>

<span data-ttu-id="fdc48-112">O pino de entrada chama esse método quando ele recebe uma amostra do filtro upstream.</span><span class="sxs-lookup"><span data-stu-id="fdc48-112">The input pin calls this method when it receives a sample from the upstream filter.</span></span>

<span data-ttu-id="fdc48-113">Se o filtro estiver em execução, esse método executará as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="fdc48-113">If the filter is running, this method performs the following steps:</span></span>

1.  <span data-ttu-id="fdc48-114">Agenda o exemplo de renderização ([**CBaseRenderer::P reparereceive**](cbaserenderer-preparereceive.md)).</span><span class="sxs-lookup"><span data-stu-id="fdc48-114">Schedules the sample for rendering ([**CBaseRenderer::PrepareReceive**](cbaserenderer-preparereceive.md)).</span></span>
2.  <span data-ttu-id="fdc48-115">Aguarda o horário agendado ([**CBaseRenderer:: WaitForRenderTime**](cbaserenderer-waitforrendertime.md)).</span><span class="sxs-lookup"><span data-stu-id="fdc48-115">Waits for the scheduled time ([**CBaseRenderer::WaitForRenderTime**](cbaserenderer-waitforrendertime.md)).</span></span>
3.  <span data-ttu-id="fdc48-116">Renderiza o exemplo ([**CBaseRenderer:: render**](cbaserenderer-render.md)).</span><span class="sxs-lookup"><span data-stu-id="fdc48-116">Renders the sample ([**CBaseRenderer::Render**](cbaserenderer-render.md)).</span></span>
4.  <span data-ttu-id="fdc48-117">Libera o exemplo ([**CBaseRenderer:: ClearPendingSample**](cbaserenderer-clearpendingsample.md)).</span><span class="sxs-lookup"><span data-stu-id="fdc48-117">Releases the sample ([**CBaseRenderer::ClearPendingSample**](cbaserenderer-clearpendingsample.md)).</span></span>

<span data-ttu-id="fdc48-118">Se o filtro for pausado, o método executará as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="fdc48-118">If the filter is paused, the method performs the following steps:</span></span>

1.  <span data-ttu-id="fdc48-119">Notifica a classe derivada de que um exemplo está disponível ([**CBaseRenderer:: OnReceiveFirstSample**](cbaserenderer-onreceivefirstsample.md)).</span><span class="sxs-lookup"><span data-stu-id="fdc48-119">Notifies the derived class that a sample is available ([**CBaseRenderer::OnReceiveFirstSample**](cbaserenderer-onreceivefirstsample.md)).</span></span>
2.  <span data-ttu-id="fdc48-120">Aguarda o horário agendado.</span><span class="sxs-lookup"><span data-stu-id="fdc48-120">Waits for the scheduled time.</span></span>
3.  <span data-ttu-id="fdc48-121">Renderiza o exemplo.</span><span class="sxs-lookup"><span data-stu-id="fdc48-121">Renders the sample.</span></span>
4.  <span data-ttu-id="fdc48-122">Libera o exemplo.</span><span class="sxs-lookup"><span data-stu-id="fdc48-122">Releases the sample.</span></span>

<span data-ttu-id="fdc48-123">Enquanto estiver em pausa, o método aguardará na etapa 2 até que o filtro alterne para um estado de execução.</span><span class="sxs-lookup"><span data-stu-id="fdc48-123">While paused, the method waits in step 2 until the filter switches to a running state.</span></span> <span data-ttu-id="fdc48-124">Nesse ponto, o filtro agenda o exemplo.</span><span class="sxs-lookup"><span data-stu-id="fdc48-124">At that point, the filter schedules the sample.</span></span>

<span data-ttu-id="fdc48-125">Na classe base, o método **OnReceiveFirstSample** não faz nada.</span><span class="sxs-lookup"><span data-stu-id="fdc48-125">In the base class, the **OnReceiveFirstSample** method does nothing.</span></span> <span data-ttu-id="fdc48-126">A classe derivada pode substituí-la.</span><span class="sxs-lookup"><span data-stu-id="fdc48-126">The derived class can override it.</span></span> <span data-ttu-id="fdc48-127">Por exemplo, quando um processador de vídeo é pausado, ele exibe a primeira amostra como uma imagem ainda.</span><span class="sxs-lookup"><span data-stu-id="fdc48-127">For example, when a video renderer is paused, it displays the first sample as a still image.</span></span>

## <a name="requirements"></a><span data-ttu-id="fdc48-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fdc48-128">Requirements</span></span>



| <span data-ttu-id="fdc48-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="fdc48-129">Requirement</span></span> | <span data-ttu-id="fdc48-130">Valor</span><span class="sxs-lookup"><span data-stu-id="fdc48-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fdc48-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fdc48-131">Header</span></span><br/>  | <dl> <span data-ttu-id="fdc48-132"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fdc48-132"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fdc48-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fdc48-133">Library</span></span><br/> | <dl> <span data-ttu-id="fdc48-134"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="fdc48-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fdc48-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="fdc48-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdc48-136">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="fdc48-136">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




