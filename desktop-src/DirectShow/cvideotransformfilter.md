---
description: A classe CVideoTransformFilter é projetada principalmente como uma classe base para filtros de descompactador AVI.
ms.assetid: 8eb87f9f-24b3-4dbe-a390-54db993d2724
title: Classe CVideoTransformFilter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter
api_type:
- COM
api_location: ''
ms.openlocfilehash: 360f46eb7242de01d5e734c5efa17399f23adf7d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103826029"
---
# <a name="cvideotransformfilter-class"></a><span data-ttu-id="ad4ab-103">Classe CVideoTransformFilter</span><span class="sxs-lookup"><span data-stu-id="ad4ab-103">CVideoTransformFilter class</span></span>

![hierarquia de classe CVideoTransformFilter](images/vtsip01.png)

<span data-ttu-id="ad4ab-105">A `CVideoTransformFilter` classe é projetada principalmente como uma classe base para filtros de descompactador AVI.</span><span class="sxs-lookup"><span data-stu-id="ad4ab-105">The `CVideoTransformFilter` class is designed primarily as a base class for AVI decompressor filters.</span></span> <span data-ttu-id="ad4ab-106">Essa classe adiciona suporte para controle de qualidade à classe [**CTransformFilter**](ctransformfilter.md) .</span><span class="sxs-lookup"><span data-stu-id="ad4ab-106">This class adds support for quality control to the [**CTransformFilter**](ctransformfilter.md) class.</span></span> <span data-ttu-id="ad4ab-107">O método **Receive** do filtro pode decidir descartar quadros, com base em mensagens de qualidade do renderizador e medidas de desempenho que o filtro coleta durante o streaming.</span><span class="sxs-lookup"><span data-stu-id="ad4ab-107">The filter's **Receive** method can decide to drop frames, based on quality messages from the renderer and performance measurements that the filter collects while it is streaming.</span></span>

<span data-ttu-id="ad4ab-108">Se o filtro descartar um quadro, ele continuará a descartar os quadros até atingir o próximo quadro-chave.</span><span class="sxs-lookup"><span data-stu-id="ad4ab-108">If the filter drops a frame, it continues to drop frames until it reaches the next key frame.</span></span> <span data-ttu-id="ad4ab-109">Para fluxos MPEG, o filtro não distingue entre os quadros B e P.</span><span class="sxs-lookup"><span data-stu-id="ad4ab-109">For MPEG streams, the filter does not distinguish between B frames and P frames.</span></span>



| <span data-ttu-id="ad4ab-110">Variáveis de membro protegido</span><span class="sxs-lookup"><span data-stu-id="ad4ab-110">Protected Member Variables</span></span>                                                      | <span data-ttu-id="ad4ab-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="ad4ab-111">Description</span></span>                                                                                    |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ad4ab-112">**\_bQualityChanged m**</span><span class="sxs-lookup"><span data-stu-id="ad4ab-112">**m\_bQualityChanged**</span></span>](cvideotransformfilter-m-bqualitychanged.md)           | <span data-ttu-id="ad4ab-113">Indica se o filtro removeu quadros.</span><span class="sxs-lookup"><span data-stu-id="ad4ab-113">Indicates whether the filter has dropped frames.</span></span>                                               |
| [<span data-ttu-id="ad4ab-114">**\_bSkipping m**</span><span class="sxs-lookup"><span data-stu-id="ad4ab-114">**m\_bSkipping**</span></span>](cvideotransformfilter-m-bskipping.md)                       | <span data-ttu-id="ad4ab-115">Indica se o filtro está descartando os quadros no momento.</span><span class="sxs-lookup"><span data-stu-id="ad4ab-115">Indicates whether the filter is currently dropping frames.</span></span>                                     |
| [<span data-ttu-id="ad4ab-116">**\_itrAvgDecode m**</span><span class="sxs-lookup"><span data-stu-id="ad4ab-116">**m\_itrAvgDecode**</span></span>](cvideotransformfilter-m-itravgdecode.md)                 | <span data-ttu-id="ad4ab-117">O período médio de tempo necessário para decodificar um quadro.</span><span class="sxs-lookup"><span data-stu-id="ad4ab-117">Average length of time it has taken to decode a frame.</span></span>                                         |
| [<span data-ttu-id="ad4ab-118">**\_itrLate m**</span><span class="sxs-lookup"><span data-stu-id="ad4ab-118">**m\_itrLate**</span></span>](cvideotransformfilter-m-itrlate.md)                           | <span data-ttu-id="ad4ab-119">Indica o quanto tarde as amostras chegam ao renderizador.</span><span class="sxs-lookup"><span data-stu-id="ad4ab-119">Indicates how late the samples are arriving at the renderer.</span></span>                                   |
| [<span data-ttu-id="ad4ab-120">**\_nFramesSinceKeyFrame m**</span><span class="sxs-lookup"><span data-stu-id="ad4ab-120">**m\_nFramesSinceKeyFrame**</span></span>](cvideotransformfilter-m-nframessincekeyframe.md) | <span data-ttu-id="ad4ab-121">O número de quadros que o filtro recebeu desde o último quadro de chave.</span><span class="sxs-lookup"><span data-stu-id="ad4ab-121">The number of frames that the filter has received since the last key frame.</span></span>                    |
| [<span data-ttu-id="ad4ab-122">**\_nKeyFramePeriod m**</span><span class="sxs-lookup"><span data-stu-id="ad4ab-122">**m\_nKeyFramePeriod**</span></span>](cvideotransformfilter-m-nkeyframeperiod.md)           | <span data-ttu-id="ad4ab-123">O maior intervalo observado entre quadros-chave.</span><span class="sxs-lookup"><span data-stu-id="ad4ab-123">The largest observed interval between key frames.</span></span>                                              |
| [<span data-ttu-id="ad4ab-124">**\_nWaitForKey m**</span><span class="sxs-lookup"><span data-stu-id="ad4ab-124">**m\_nWaitForKey**</span></span>](cvideotransformfilter-m-nwaitforkey.md)                   | <span data-ttu-id="ad4ab-125">O número máximo atual de quadros Delta a serem descartados.</span><span class="sxs-lookup"><span data-stu-id="ad4ab-125">The current maximum number of delta frames to drop.</span></span>                                            |
| [<span data-ttu-id="ad4ab-126">**\_tDecodeStart m**</span><span class="sxs-lookup"><span data-stu-id="ad4ab-126">**m\_tDecodeStart**</span></span>](cvideotransformfilter-m-tdecodestart.md)                 | <span data-ttu-id="ad4ab-127">Período de tempo necessário para decodificar o exemplo mais recente.</span><span class="sxs-lookup"><span data-stu-id="ad4ab-127">Length of time that it took to decode the most recent sample.</span></span>                                  |
| <span data-ttu-id="ad4ab-128">Métodos Protegidos</span><span class="sxs-lookup"><span data-stu-id="ad4ab-128">Protected Methods</span></span>                                                               | <span data-ttu-id="ad4ab-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="ad4ab-129">Description</span></span>                                                                                    |
| [<span data-ttu-id="ad4ab-130">**AbortPlayback**</span><span class="sxs-lookup"><span data-stu-id="ad4ab-130">**AbortPlayback**</span></span>](cvideotransformfilter-abortplayback.md)                    | <span data-ttu-id="ad4ab-131">Usado para sinalizar um erro de streaming.</span><span class="sxs-lookup"><span data-stu-id="ad4ab-131">Used to signal a streaming error.</span></span>                                                              |
| [<span data-ttu-id="ad4ab-132">**AlterQuality**</span><span class="sxs-lookup"><span data-stu-id="ad4ab-132">**AlterQuality**</span></span>](cvideotransformfilter-alterquality.md)                      | <span data-ttu-id="ad4ab-133">Notifica o filtro de que uma alteração de qualidade é solicitada.</span><span class="sxs-lookup"><span data-stu-id="ad4ab-133">Notifies the filter that a quality change is requested.</span></span>                                        |
| [<span data-ttu-id="ad4ab-134">**Recebe**</span><span class="sxs-lookup"><span data-stu-id="ad4ab-134">**Receive**</span></span>](cvideotransformfilter-receive.md)                                | <span data-ttu-id="ad4ab-135">Recebe um exemplo de mídia, processa-o e entrega um exemplo de saída para o filtro downstream.</span><span class="sxs-lookup"><span data-stu-id="ad4ab-135">Receives a media sample, processes it, and delivers an output sample to the downstream filter.</span></span> |
| [<span data-ttu-id="ad4ab-136">**ShouldSkipFrame**</span><span class="sxs-lookup"><span data-stu-id="ad4ab-136">**ShouldSkipFrame**</span></span>](cvideotransformfilter-shouldskipframe.md)                | <span data-ttu-id="ad4ab-137">Determina se o filtro deve descartar um exemplo especificado.</span><span class="sxs-lookup"><span data-stu-id="ad4ab-137">Determines whether the filter should drop a specified sample.</span></span>                                  |
| [<span data-ttu-id="ad4ab-138">**StartStreaming**</span><span class="sxs-lookup"><span data-stu-id="ad4ab-138">**StartStreaming**</span></span>](cvideotransformfilter-startstreaming.md)                  | <span data-ttu-id="ad4ab-139">Chamado quando o filtro alterna para o estado pausado.</span><span class="sxs-lookup"><span data-stu-id="ad4ab-139">Called when the filter switches to the paused state.</span></span>                                           |
| <span data-ttu-id="ad4ab-140">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="ad4ab-140">Public Methods</span></span>                                                                  | <span data-ttu-id="ad4ab-141">Descrição</span><span class="sxs-lookup"><span data-stu-id="ad4ab-141">Description</span></span>                                                                                    |
| [<span data-ttu-id="ad4ab-142">**CVideoTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="ad4ab-142">**CVideoTransformFilter**</span></span>](cvideotransformfilter-cvideotransformfilter.md)    | <span data-ttu-id="ad4ab-143">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="ad4ab-143">Constructor method.</span></span>                                                                            |
| [<span data-ttu-id="ad4ab-144">**EndFlush**</span><span class="sxs-lookup"><span data-stu-id="ad4ab-144">**EndFlush**</span></span>](cvideotransformfilter-endflush.md)                              | <span data-ttu-id="ad4ab-145">Finaliza uma operação de liberação.</span><span class="sxs-lookup"><span data-stu-id="ad4ab-145">Ends a flush operation.</span></span>                                                                        |



 

 

 



