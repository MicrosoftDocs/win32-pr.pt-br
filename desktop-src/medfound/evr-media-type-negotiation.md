---
description: Negociação de tipo de mídia EVR
ms.assetid: 3a12b80d-7aac-437d-b515-aab37c1e81b2
title: Negociação de tipo de mídia EVR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bb1f87a24db866c9e80b211b0385c12dcd6b594
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104297940"
---
# <a name="evr-media-type-negotiation"></a><span data-ttu-id="ff20f-103">Negociação de tipo de mídia EVR</span><span class="sxs-lookup"><span data-stu-id="ff20f-103">EVR Media Type Negotiation</span></span>

<span data-ttu-id="ff20f-104">Este tópico descreve como o processador de vídeo avançado (EVR) valida os tipos de mídia.</span><span class="sxs-lookup"><span data-stu-id="ff20f-104">This topic describes how the enhanced video renderer (EVR) validates media types.</span></span>

-   <span data-ttu-id="ff20f-105">Para o filtro EVR do DirectShow, a negociação do tipo ocorre quando os Pins do filtro são conectados.</span><span class="sxs-lookup"><span data-stu-id="ff20f-105">For the DirectShow EVR filter, type negotiation occurs when the filter's pins are connected.</span></span>

-   <span data-ttu-id="ff20f-106">Para o coletor de mídia do EVR, os tipos de mídia são definidos por meio da interface [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) nos coletores de fluxo.</span><span class="sxs-lookup"><span data-stu-id="ff20f-106">For the EVR media sink, the media types are set through the [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) interface on the stream sinks.</span></span> <span data-ttu-id="ff20f-107">Normalmente, o carregador de topologia negocia os tipos de mídia, embora o aplicativo também possa definir os tipos de mídia diretamente.</span><span class="sxs-lookup"><span data-stu-id="ff20f-107">Typically the topology loader negotiates the media types, although the application can also set the media types directly.</span></span>

<span data-ttu-id="ff20f-108">O EVR não relata nenhum tipo de mídia preferencial.</span><span class="sxs-lookup"><span data-stu-id="ff20f-108">The EVR does not report any preferred media types.</span></span> <span data-ttu-id="ff20f-109">O cliente deve testar os tipos de mídia até encontrar um tipo aceitável.</span><span class="sxs-lookup"><span data-stu-id="ff20f-109">The client must test media types until it finds an acceptable type.</span></span> <span data-ttu-id="ff20f-110">O tipo de mídia para o fluxo de referência deve ser definido antes que os tipos possam ser definidos em qualquer um dos subfluxos.</span><span class="sxs-lookup"><span data-stu-id="ff20f-110">The media type for the reference stream must be set before the types can be set on any of the substreams.</span></span>

<span data-ttu-id="ff20f-111">Para o fluxo de referência, o mixer EVR Obtém uma lista de formatos de destino de renderização DXVA (DirectX Video Acceleration) compatíveis.</span><span class="sxs-lookup"><span data-stu-id="ff20f-111">For the reference stream, the EVR mixer gets a list of compatible DirectX Video Acceleration (DXVA) render target formats.</span></span> <span data-ttu-id="ff20f-112">O apresentador EVR usa essa lista para selecionar o formato da cadeia de permuta do Direct3D.</span><span class="sxs-lookup"><span data-stu-id="ff20f-112">The EVR presenter uses this list to select the format for the Direct3D swap chain.</span></span> <span data-ttu-id="ff20f-113">Se nenhum formato de destino de renderização compatível puder ser encontrado, o EVR rejeitará o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="ff20f-113">If no compatible render target format can be found, the EVR rejects the media type.</span></span>

<span data-ttu-id="ff20f-114">Para os subfluxos, o mixer EVR consulta se o dispositivo DXVA dá suporte a esse formato de Subfluxo em combinação com o formato de destino de renderização selecionado para o fluxo de referência.</span><span class="sxs-lookup"><span data-stu-id="ff20f-114">For the substreams, the EVR mixer queries whether the DXVA device supports that substream format in combination with the render target format that was selected for the reference stream.</span></span> <span data-ttu-id="ff20f-115">Como resultado, os formatos de Subfluxo disponíveis podem mudar dependendo do fluxo de referência.</span><span class="sxs-lookup"><span data-stu-id="ff20f-115">As a result, the available substream formats might change depending on the reference stream.</span></span>

<span data-ttu-id="ff20f-116">Aqui está o processo em mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="ff20f-116">Here is the process in more detail.</span></span> <span data-ttu-id="ff20f-117">Esses detalhes não são importantes para a maioria dos aplicativos, mas podem ser úteis se você estiver escrevendo um mixer ou apresentador personalizado.</span><span class="sxs-lookup"><span data-stu-id="ff20f-117">These details are not important for most applications, but might be helpful if you are writing a custom mixer or presenter.</span></span>

<span data-ttu-id="ff20f-118">Para o fluxo de referência, a negociação ocorre da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="ff20f-118">For the reference stream, negotiation happens as follows:</span></span>

1.  <span data-ttu-id="ff20f-119">O EVR chama [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) no mixer.</span><span class="sxs-lookup"><span data-stu-id="ff20f-119">The EVR calls [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) on the mixer.</span></span>

2.  <span data-ttu-id="ff20f-120">O mixer converte o tipo de mídia em uma descrição de DXVA 2,0, usando a estrutura [**DXVA2 \_ VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) .</span><span class="sxs-lookup"><span data-stu-id="ff20f-120">The mixer converts the media type to a DXVA 2.0 description, using the [**DXVA2\_VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) structure.</span></span>

3.  <span data-ttu-id="ff20f-121">O mixer chama [**IDirectXVideoProcessorService:: GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) para obter uma lista de GUIDs de processador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ff20f-121">The mixer calls [**IDirectXVideoProcessorService::GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) to get a list of video processor GUIDs.</span></span>

4.  <span data-ttu-id="ff20f-122">Para cada GUID de processador de vídeo, o mixer chama [**IDirectXVideoProcessorService:: GetVideoProcessorRenderTargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorrendertargets) para obter os formatos de destino de renderização com suporte.</span><span class="sxs-lookup"><span data-stu-id="ff20f-122">For each video processor GUID, the mixer calls [**IDirectXVideoProcessorService::GetVideoProcessorRenderTargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorrendertargets) to get the supported render target formats.</span></span>

5.  <span data-ttu-id="ff20f-123">O EVR chama [**IMFVideoPresenter::P rocessmessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) no apresentador com a mensagem MFVP \_ Message \_ INVALIDATEMEDIATYPE.</span><span class="sxs-lookup"><span data-stu-id="ff20f-123">The EVR calls [**IMFVideoPresenter::ProcessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) on the presenter with the MFVP\_MESSAGE\_INVALIDATEMEDIATYPE message.</span></span> <span data-ttu-id="ff20f-124">Essa mensagem faz com que o apresentador selecione um novo formato.</span><span class="sxs-lookup"><span data-stu-id="ff20f-124">This message causes the presenter to select a new format.</span></span>

6.  <span data-ttu-id="ff20f-125">O apresentador chama [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) para obter uma lista de formatos de saída disponíveis do mixer.</span><span class="sxs-lookup"><span data-stu-id="ff20f-125">The presenter calls [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) to get a list of available output formats from the mixer.</span></span> <span data-ttu-id="ff20f-126">O mixer gera essa lista com base nos formatos obtidos na etapa 4.</span><span class="sxs-lookup"><span data-stu-id="ff20f-126">The mixer generates this list from the formats obtained in step 4.</span></span>

7.  <span data-ttu-id="ff20f-127">O apresentador seleciona um formato e chama [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) no mixer.</span><span class="sxs-lookup"><span data-stu-id="ff20f-127">The presenter selects a format and calls [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) on the mixer.</span></span>

<span data-ttu-id="ff20f-128">Para subfluxos, o processo é mais simples:</span><span class="sxs-lookup"><span data-stu-id="ff20f-128">For substreams, the process is simpler:</span></span>

1.  <span data-ttu-id="ff20f-129">O EVR chama [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) no mixer.</span><span class="sxs-lookup"><span data-stu-id="ff20f-129">The EVR calls [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) on the mixer.</span></span>

2.  <span data-ttu-id="ff20f-130">O mixer chama [**IDirectXVideoProcessorService:: GetVideoProcessorSubStreamFormats**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorsubstreamformats) para obter uma lista de formatos de Subfluxo disponíveis.</span><span class="sxs-lookup"><span data-stu-id="ff20f-130">The mixer calls [**IDirectXVideoProcessorService::GetVideoProcessorSubStreamFormats**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorsubstreamformats) to get a list of available substream formats.</span></span>

3.  <span data-ttu-id="ff20f-131">Se o formato proposto estiver contido nessa lista, o EVR aceitará o tipo de entrada.</span><span class="sxs-lookup"><span data-stu-id="ff20f-131">If the proposed format is contained in this list, the EVR accepts the input type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ff20f-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ff20f-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff20f-133">Processador de vídeo aprimorado</span><span class="sxs-lookup"><span data-stu-id="ff20f-133">Enhanced Video Renderer</span></span>](enhanced-video-renderer.md)
</dt> </dl>

 

 



