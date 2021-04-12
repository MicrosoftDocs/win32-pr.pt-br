---
description: Modelo de objeto de origem de mídia
ms.assetid: 88373028-8a34-4bf1-8300-d1a7e4c7dd75
title: Modelo de objeto de origem de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0d05cc9d5341bff433d6276b5ee67505361b78f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104297955"
---
# <a name="media-source-object-model"></a><span data-ttu-id="708e6-103">Modelo de objeto de origem de mídia</span><span class="sxs-lookup"><span data-stu-id="708e6-103">Media Source Object Model</span></span>

<span data-ttu-id="708e6-104">Este tópico descreve o modelo de objeto para fontes de mídia no Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="708e6-104">This topic describes the object model for media sources in Microsoft Media Foundation.</span></span> <span data-ttu-id="708e6-105">Uma fonte de mídia deve implementar dois objetos:</span><span class="sxs-lookup"><span data-stu-id="708e6-105">A media source must implement two objects:</span></span>

-   <span data-ttu-id="708e6-106">Um descritor de apresentação, que descreve o conteúdo da origem, incluindo o número de fluxos e o formato de cada fluxo.</span><span class="sxs-lookup"><span data-stu-id="708e6-106">A presentation descriptor, which describes the contents of the source, including the number of streams and the format of each stream.</span></span> <span data-ttu-id="708e6-107">Para obter mais informações sobre descritores de apresentação, consulte [descritores de apresentação](presentation-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="708e6-107">For more information about presentation descriptors, see [Presentation Descriptors](presentation-descriptors.md).</span></span>
-   <span data-ttu-id="708e6-108">Um ou mais fluxos de mídia, que geram os dados de origem.</span><span class="sxs-lookup"><span data-stu-id="708e6-108">One or more media streams, which generate the source data.</span></span>

<span data-ttu-id="708e6-109">A origem não cria os fluxos até que a reprodução seja iniciada.</span><span class="sxs-lookup"><span data-stu-id="708e6-109">The source does not create the streams until playback starts.</span></span>

## <a name="media-source-interfaces"></a><span data-ttu-id="708e6-110">Interfaces de origem de mídia</span><span class="sxs-lookup"><span data-stu-id="708e6-110">Media Source Interfaces</span></span>

<span data-ttu-id="708e6-111">Uma origem de mídia deve expor as seguintes interfaces por meio de **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="708e6-111">A media source must expose the following interfaces through **QueryInterface**.</span></span>



| <span data-ttu-id="708e6-112">Interface</span><span class="sxs-lookup"><span data-stu-id="708e6-112">Interface</span></span>                                                | <span data-ttu-id="708e6-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="708e6-113">Description</span></span>                                                                                                     |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="708e6-114">**IMFMediaSource**</span><span class="sxs-lookup"><span data-stu-id="708e6-114">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                 | <span data-ttu-id="708e6-115">Necessário para todas as fontes de mídia.</span><span class="sxs-lookup"><span data-stu-id="708e6-115">Required for all media sources.</span></span>                                                                                 |
| [<span data-ttu-id="708e6-116">**IMFMediaEventGenerator**</span><span class="sxs-lookup"><span data-stu-id="708e6-116">**IMFMediaEventGenerator**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) | <span data-ttu-id="708e6-117">Necessário para todas as fontes de mídia.</span><span class="sxs-lookup"><span data-stu-id="708e6-117">Required for all media sources.</span></span> <span data-ttu-id="708e6-118">A interface [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) herda essa interface.</span><span class="sxs-lookup"><span data-stu-id="708e6-118">The [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface inherits this interface.</span></span> |



 

<span data-ttu-id="708e6-119">Opcionalmente, uma fonte de mídia pode implementar a interface [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) e implementar qualquer uma das seguintes interfaces como serviços:</span><span class="sxs-lookup"><span data-stu-id="708e6-119">Optionally, a media source can implement the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface and implement any of the following interfaces as services:</span></span>



| <span data-ttu-id="708e6-120">Interface de serviço</span><span class="sxs-lookup"><span data-stu-id="708e6-120">Service interface</span></span>                                  | <span data-ttu-id="708e6-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="708e6-121">Description</span></span>                                                       |
|----------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="708e6-122">**IMFRateControl**</span><span class="sxs-lookup"><span data-stu-id="708e6-122">**IMFRateControl**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)           | <span data-ttu-id="708e6-123">Controla a taxa de reprodução.</span><span class="sxs-lookup"><span data-stu-id="708e6-123">Controls the playback rate.</span></span>                                       |
| [<span data-ttu-id="708e6-124">**IMFRateSupport**</span><span class="sxs-lookup"><span data-stu-id="708e6-124">**IMFRateSupport**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)           | <span data-ttu-id="708e6-125">Relata o intervalo de taxas de reprodução com suporte.</span><span class="sxs-lookup"><span data-stu-id="708e6-125">Reports the range of playback rates that are supported.</span></span>           |
| [<span data-ttu-id="708e6-126">**IMFQualityAdvise**</span><span class="sxs-lookup"><span data-stu-id="708e6-126">**IMFQualityAdvise**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)       | <span data-ttu-id="708e6-127">Permite que o Gerenciador de qualidade ajuste a qualidade de áudio ou vídeo.</span><span class="sxs-lookup"><span data-stu-id="708e6-127">Enables the quality manager to adjust the audio or video quality.</span></span> |
| [<span data-ttu-id="708e6-128">**IMFMetadataProvider**</span><span class="sxs-lookup"><span data-stu-id="708e6-128">**IMFMetadataProvider**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) | <span data-ttu-id="708e6-129">Fornece metadados.</span><span class="sxs-lookup"><span data-stu-id="708e6-129">Provides metadata.</span></span>                                                |



 

<span data-ttu-id="708e6-130">Se a origem da mídia puder ser executada em taxas diferentes da velocidade normal (1,0), ela deverá expor o serviço de controle de taxa ([**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) e [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)).</span><span class="sxs-lookup"><span data-stu-id="708e6-130">If the media source can play at rates other than normal speed (1.0), it should expose the rate control service ([**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) and [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)).</span></span> <span data-ttu-id="708e6-131">Caso contrário, supõe-se que a origem só dá suporte à reprodução em velocidade normal.</span><span class="sxs-lookup"><span data-stu-id="708e6-131">Otherwise, it is assumed that the source only supports playback at normal speed.</span></span> <span data-ttu-id="708e6-132">Para obter mais informações, consulte [implementando o controle de taxa](implementing-rate-control.md).</span><span class="sxs-lookup"><span data-stu-id="708e6-132">For more information, see [Implementing Rate Control](implementing-rate-control.md).</span></span>

<span data-ttu-id="708e6-133">Para obter mais informações sobre interfaces de serviço e [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice), consulte [interfaces de serviço](service-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="708e6-133">For more information about service interfaces and [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice), see [Service Interfaces](service-interfaces.md).</span></span>

## <a name="media-stream-interfaces"></a><span data-ttu-id="708e6-134">Interfaces de fluxo de mídia</span><span class="sxs-lookup"><span data-stu-id="708e6-134">Media Stream Interfaces</span></span>

<span data-ttu-id="708e6-135">Os fluxos de mídia devem implementar as seguintes interfaces.</span><span class="sxs-lookup"><span data-stu-id="708e6-135">Media streams must implement the following interfaces.</span></span>



| <span data-ttu-id="708e6-136">Interface</span><span class="sxs-lookup"><span data-stu-id="708e6-136">Interface</span></span>                                                | <span data-ttu-id="708e6-137">Descrição</span><span class="sxs-lookup"><span data-stu-id="708e6-137">Description</span></span>                                                                                                     |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="708e6-138">**IMFMediaStream**</span><span class="sxs-lookup"><span data-stu-id="708e6-138">**IMFMediaStream**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)                 | <span data-ttu-id="708e6-139">Necessário para todos os fluxos de mídia.</span><span class="sxs-lookup"><span data-stu-id="708e6-139">Required for all media streams.</span></span>                                                                                 |
| [<span data-ttu-id="708e6-140">**IMFMediaEventGenerator**</span><span class="sxs-lookup"><span data-stu-id="708e6-140">**IMFMediaEventGenerator**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) | <span data-ttu-id="708e6-141">Necessário para todos os fluxos de mídia.</span><span class="sxs-lookup"><span data-stu-id="708e6-141">Required for all media streams.</span></span> <span data-ttu-id="708e6-142">A interface [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) herda essa interface.</span><span class="sxs-lookup"><span data-stu-id="708e6-142">The [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) interface inherits this interface.</span></span> |



 

<span data-ttu-id="708e6-143">No momento, nenhuma interface de serviço é definida para fluxos de mídia.</span><span class="sxs-lookup"><span data-stu-id="708e6-143">Currently no service interfaces are defined for media streams.</span></span>

## <a name="related-topics"></a><span data-ttu-id="708e6-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="708e6-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="708e6-145">Fontes de mídia</span><span class="sxs-lookup"><span data-stu-id="708e6-145">Media Sources</span></span>](media-sources.md)
</dt> </dl>

 

 



