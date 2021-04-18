---
description: Usando o filtro EVR do DirectShow
ms.assetid: 4d85aed0-4b11-4c5f-bfc0-cad0a7d2f490
title: Usando o filtro EVR do DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02568a5ea9cbaa0310409a5a0966a2bea1bbfffe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782864"
---
# <a name="using-the-directshow-evr-filter"></a><span data-ttu-id="b7e8c-103">Usando o filtro EVR do DirectShow</span><span class="sxs-lookup"><span data-stu-id="b7e8c-103">Using the DirectShow EVR Filter</span></span>

<span data-ttu-id="b7e8c-104">Para criar o filtro EVR (processador de vídeo avançado), chame **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="b7e8c-104">To create the enhanced video renderer (EVR) filter, call **CoCreateInstance**.</span></span> <span data-ttu-id="b7e8c-105">O CLSID é CLSID \_ EnhancedVideoRenderer, definido em UUIDs. h.</span><span class="sxs-lookup"><span data-stu-id="b7e8c-105">The CLSID is CLSID\_EnhancedVideoRenderer, defined in uuids.h.</span></span> <span data-ttu-id="b7e8c-106">Você não precisa chamar [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) ou [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) para usar o filtro EVR.</span><span class="sxs-lookup"><span data-stu-id="b7e8c-106">You do not have to call [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) or [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) to use the EVR filter.</span></span>

<span data-ttu-id="b7e8c-107">Para obter mais informações sobre como usar o filtro EVR em um aplicativo do DirectShow, consulte [reprodução de áudio/vídeo no DirectShow](../directshow/audio-video-playback-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="b7e8c-107">For more information about using the EVR filter in a DirectShow application, see [Audio/Video Playback in DirectShow](../directshow/audio-video-playback-in-directshow.md).</span></span>

<span data-ttu-id="b7e8c-108">O filtro EVR começa com um PIN de entrada, que corresponde ao fluxo de referência.</span><span class="sxs-lookup"><span data-stu-id="b7e8c-108">The EVR filter starts with one input pin, which corresponds to the reference stream.</span></span> <span data-ttu-id="b7e8c-109">Para adicionar Pins para subfluxos, consulte o filtro para a interface [**IEVRFilterConfig**](/windows/desktop/api/evr/nn-evr-ievrfilterconfig) e chame [**IEVRFilterConfig:: SetNumberOfStreams**](/windows/desktop/api/evr/nf-evr-ievrfilterconfig-setnumberofstreams).</span><span class="sxs-lookup"><span data-stu-id="b7e8c-109">To add pins for substreams, query the filter for the [**IEVRFilterConfig**](/windows/desktop/api/evr/nn-evr-ievrfilterconfig) interface and call [**IEVRFilterConfig::SetNumberOfStreams**](/windows/desktop/api/evr/nf-evr-ievrfilterconfig-setnumberofstreams).</span></span> <span data-ttu-id="b7e8c-110">Chame esse método antes de conectar qualquer pino de entrada.</span><span class="sxs-lookup"><span data-stu-id="b7e8c-110">Call this method before connecting any input pins.</span></span> <span data-ttu-id="b7e8c-111">O PIN 0 é sempre o fluxo de referência.</span><span class="sxs-lookup"><span data-stu-id="b7e8c-111">Pin 0 is always the reference stream.</span></span> <span data-ttu-id="b7e8c-112">Conecte este pin antes de quaisquer outros Pins, pois o formato do fluxo de referência pode limitar quais formatos de Subfluxo estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="b7e8c-112">Connect this pin before any other pins, because the format of the reference stream might limit which substream formats are available.</span></span>

<span data-ttu-id="b7e8c-113">Antes de iniciar o grafo, defina a janela de recorte de vídeo e o retângulo de destino.</span><span class="sxs-lookup"><span data-stu-id="b7e8c-113">Before starting the graph, set the video clipping window and the destination rectangle.</span></span> <span data-ttu-id="b7e8c-114">Para obter mais informações, consulte [usando os controles de exibição de vídeo](using-the-video-display-controls.md).</span><span class="sxs-lookup"><span data-stu-id="b7e8c-114">For more information, see [Using the Video Display Controls](using-the-video-display-controls.md).</span></span>

<span data-ttu-id="b7e8c-115">Ao contrário do VMR (Video Misturation Renderer), o EVR não tem modos operacionais (janelas, sem janelas e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="b7e8c-115">Unlike the Video Mixing Renderer (VMR), the EVR does not have operational modes (windowed, windowless, and so forth).</span></span> <span data-ttu-id="b7e8c-116">Especialmente:</span><span class="sxs-lookup"><span data-stu-id="b7e8c-116">In particular:</span></span>

-   <span data-ttu-id="b7e8c-117">O EVR não dá suporte ao modo de janela.</span><span class="sxs-lookup"><span data-stu-id="b7e8c-117">The EVR does not support windowed mode.</span></span> <span data-ttu-id="b7e8c-118">O aplicativo deve fornecer a janela de recorte.</span><span class="sxs-lookup"><span data-stu-id="b7e8c-118">The application must provide the clipping window.</span></span>
-   <span data-ttu-id="b7e8c-119">O EVR não tem um modo sem processamento.</span><span class="sxs-lookup"><span data-stu-id="b7e8c-119">The EVR does not have a renderless mode.</span></span> <span data-ttu-id="b7e8c-120">Para substituir o apresentador padrão, chame [**IMFVideoRenderer:: InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).</span><span class="sxs-lookup"><span data-stu-id="b7e8c-120">To replace the default presenter, call [**IMFVideoRenderer::InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).</span></span>
-   <span data-ttu-id="b7e8c-121">O EVR não tem um modo de combinação.</span><span class="sxs-lookup"><span data-stu-id="b7e8c-121">The EVR does not have a mixing mode.</span></span> <span data-ttu-id="b7e8c-122">O EVR sempre cria o mixer.</span><span class="sxs-lookup"><span data-stu-id="b7e8c-122">The EVR always creates the mixer.</span></span> <span data-ttu-id="b7e8c-123">Se você tiver um fluxo de entrada, não será necessário chamar [**SetNumberOfStreams**](/windows/desktop/api/evr/nf-evr-ievrfilterconfig-setnumberofstreams) para forçar o EVR a usar o mixer.</span><span class="sxs-lookup"><span data-stu-id="b7e8c-123">If you have one input stream, it is not necessary to call [**SetNumberOfStreams**](/windows/desktop/api/evr/nf-evr-ievrfilterconfig-setnumberofstreams) to force the EVR to use the mixer.</span></span>

## <a name="filter-interfaces"></a><span data-ttu-id="b7e8c-124">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="b7e8c-124">Filter Interfaces</span></span>

<span data-ttu-id="b7e8c-125">O filtro EVR expõe as interfaces a seguir.</span><span class="sxs-lookup"><span data-stu-id="b7e8c-125">The EVR filter exposes the following interfaces.</span></span> <span data-ttu-id="b7e8c-126">Algumas dessas interfaces estão documentadas no SDK do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="b7e8c-126">Some of these interfaces are documented in the DirectShow SDK.</span></span> <span data-ttu-id="b7e8c-127">Use **QueryInterface** para recuperar ponteiros para essas interfaces:</span><span class="sxs-lookup"><span data-stu-id="b7e8c-127">Use **QueryInterface** to retrieve pointers to these interfaces:</span></span>

-   <span data-ttu-id="b7e8c-128">[**IAMCertifiedOutputProtection**](/windows/win32/api/strmif/nn-strmif-iamcertifiedoutputprotection) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="b7e8c-128">[**IAMCertifiedOutputProtection**](/windows/win32/api/strmif/nn-strmif-iamcertifiedoutputprotection) (DirectShow)</span></span>
-   <span data-ttu-id="b7e8c-129">[**IAMFilterMiscFlags**](/windows/win32/api/strmif/nn-strmif-iamfiltermiscflags) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="b7e8c-129">[**IAMFilterMiscFlags**](/windows/win32/api/strmif/nn-strmif-iamfiltermiscflags) (DirectShow)</span></span>
-   <span data-ttu-id="b7e8c-130">[**IBaseFilter**](/windows/win32/api/strmif/nn-strmif-ibasefilter) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="b7e8c-130">[**IBaseFilter**](/windows/win32/api/strmif/nn-strmif-ibasefilter) (DirectShow)</span></span>
-   [<span data-ttu-id="b7e8c-131">**IEVRFilterConfig**</span><span class="sxs-lookup"><span data-stu-id="b7e8c-131">**IEVRFilterConfig**</span></span>](/windows/desktop/api/evr/nn-evr-ievrfilterconfig)
-   <span data-ttu-id="b7e8c-132">[**IKsPropertySet**](../directshow/ikspropertyset.md) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="b7e8c-132">[**IKsPropertySet**](../directshow/ikspropertyset.md) (DirectShow)</span></span>
-   <span data-ttu-id="b7e8c-133">[**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="b7e8c-133">[**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) (DirectShow)</span></span>
-   [<span data-ttu-id="b7e8c-134">**IMFGetService**</span><span class="sxs-lookup"><span data-stu-id="b7e8c-134">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [<span data-ttu-id="b7e8c-135">**IMFVideoPositionMapper**</span><span class="sxs-lookup"><span data-stu-id="b7e8c-135">**IMFVideoPositionMapper**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)
-   [<span data-ttu-id="b7e8c-136">**IMFVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="b7e8c-136">**IMFVideoRenderer**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideorenderer)
-   <span data-ttu-id="b7e8c-137">**IPersistStream**</span><span class="sxs-lookup"><span data-stu-id="b7e8c-137">**IPersistStream**</span></span>
-   <span data-ttu-id="b7e8c-138">[**IQualityControl**](/windows/win32/api/strmif/nn-strmif-iqualitycontrol) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="b7e8c-138">[**IQualityControl**](/windows/win32/api/strmif/nn-strmif-iqualitycontrol) (DirectShow)</span></span>
-   <span data-ttu-id="b7e8c-139">[**IQualProp**](/previous-versions/windows/desktop/api/amvideo/nn-amvideo-iqualprop) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="b7e8c-139">[**IQualProp**](/previous-versions/windows/desktop/api/amvideo/nn-amvideo-iqualprop) (DirectShow)</span></span>
-   <span data-ttu-id="b7e8c-140">**ISpecifyPropertyPages**</span><span class="sxs-lookup"><span data-stu-id="b7e8c-140">**ISpecifyPropertyPages**</span></span>

## <a name="input-pin-interfaces"></a><span data-ttu-id="b7e8c-141">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="b7e8c-141">Input Pin Interfaces</span></span>

<span data-ttu-id="b7e8c-142">Os Pins de entrada no filtro EVR expõem as interfaces a seguir.</span><span class="sxs-lookup"><span data-stu-id="b7e8c-142">The input pins on the EVR filter expose the following interfaces.</span></span> <span data-ttu-id="b7e8c-143">Use **QueryInterface** para recuperar ponteiros para essas interfaces:</span><span class="sxs-lookup"><span data-stu-id="b7e8c-143">Use **QueryInterface** to retrieve pointers to these interfaces:</span></span>

-   [<span data-ttu-id="b7e8c-144">**IEVRVideoStreamControl**</span><span class="sxs-lookup"><span data-stu-id="b7e8c-144">**IEVRVideoStreamControl**</span></span>](/windows/desktop/api/evr9/nn-evr9-ievrvideostreamcontrol)
-   <span data-ttu-id="b7e8c-145">[**IMemInputPin**](/windows/win32/api/strmif/nn-strmif-imeminputpin) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="b7e8c-145">[**IMemInputPin**](/windows/win32/api/strmif/nn-strmif-imeminputpin) (DirectShow)</span></span>
-   [<span data-ttu-id="b7e8c-146">**IMFGetService**</span><span class="sxs-lookup"><span data-stu-id="b7e8c-146">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   <span data-ttu-id="b7e8c-147">[**IPin**](/windows/win32/api/strmif/nn-strmif-ipin) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="b7e8c-147">[**IPin**](/windows/win32/api/strmif/nn-strmif-ipin) (DirectShow)</span></span>
-   <span data-ttu-id="b7e8c-148">[**IQualityControl**](/windows/win32/api/strmif/nn-strmif-iqualitycontrol) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="b7e8c-148">[**IQualityControl**](/windows/win32/api/strmif/nn-strmif-iqualitycontrol) (DirectShow)</span></span>

<span data-ttu-id="b7e8c-149">Além disso, você pode usar a interface [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) para recuperar a seguinte interface:</span><span class="sxs-lookup"><span data-stu-id="b7e8c-149">In addition, you can use the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface to retrieve the following interface:</span></span>

-   [<span data-ttu-id="b7e8c-150">**IDirectXVideoMemoryConfiguration**</span><span class="sxs-lookup"><span data-stu-id="b7e8c-150">**IDirectXVideoMemoryConfiguration**</span></span>](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration)

## <a name="related-topics"></a><span data-ttu-id="b7e8c-151">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b7e8c-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7e8c-152">Reprodução de áudio/vídeo no DirectShow</span><span class="sxs-lookup"><span data-stu-id="b7e8c-152">Audio/Video Playback in DirectShow</span></span>](../directshow/audio-video-playback-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="b7e8c-153">Processador de vídeo aprimorado</span><span class="sxs-lookup"><span data-stu-id="b7e8c-153">Enhanced Video Renderer</span></span>](enhanced-video-renderer.md)
</dt> </dl>

 

 
