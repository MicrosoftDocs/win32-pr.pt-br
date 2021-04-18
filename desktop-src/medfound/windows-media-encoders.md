---
description: Um codificador converte áudio ou vídeo descompactado em pacotes compactados no formato especificado pelo aplicativo. Para converter arquivos de mídia em formato ASF, você pode usar os codecs de áudio e vídeo do Windows Media.
ms.assetid: 6dcf12d0-ea37-446b-a807-2b27fd1f6124
title: Codificadores de mídia do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a642702562cbb6a70b0380deb196c70c4f8207b6
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105763856"
---
# <a name="windows-media-encoders"></a><span data-ttu-id="11dfe-104">Codificadores de mídia do Windows</span><span class="sxs-lookup"><span data-stu-id="11dfe-104">Windows Media Encoders</span></span>

<span data-ttu-id="11dfe-105">Um codificador converte áudio ou vídeo descompactado em pacotes compactados no formato especificado pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="11dfe-105">An encoder converts uncompressed audio or video into compressed packets in the format specified by the application.</span></span> <span data-ttu-id="11dfe-106">Para converter arquivos de mídia em formato ASF, você pode usar os codecs de áudio e vídeo do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="11dfe-106">For converting media files into ASF format, you can use the Windows Media audio and video codecs.</span></span>

<span data-ttu-id="11dfe-107">Um codificador é identificado pelo GUID que representa a categoria: áudio ou vídeo.</span><span class="sxs-lookup"><span data-stu-id="11dfe-107">An encoder is identified by the GUID that represents the category: audio or video.</span></span> <span data-ttu-id="11dfe-108">O tipo de saída do codificador é representado por um tipo de mídia principal e o GUID de subtipo.</span><span class="sxs-lookup"><span data-stu-id="11dfe-108">The encoder's output type is represented by a media type's major and the sub type GUID.</span></span>

-   <span data-ttu-id="11dfe-109">Codecs de áudio do Windows Media</span><span class="sxs-lookup"><span data-stu-id="11dfe-109">Windows Media audio codecs</span></span>

    <span data-ttu-id="11dfe-110">Categoria: **\_ \_ \_ codificador de áudio de categoria de MFT**</span><span class="sxs-lookup"><span data-stu-id="11dfe-110">Category: **MFT\_CATEGORY\_AUDIO\_ENCODER**</span></span>

    <span data-ttu-id="11dfe-111">Tipo principal: \_ áudio MFMediaType</span><span class="sxs-lookup"><span data-stu-id="11dfe-111">Major type: MFMediaType\_Audio</span></span>

    <span data-ttu-id="11dfe-112">Subtipo: MFAudioFormat \_ WMAudioV9, MFAudioFormat \_ WMAudioV8, MFAudioFormat \_ WMAudio \_ Lossless, MFAudioFormat \_ WMASPDIF</span><span class="sxs-lookup"><span data-stu-id="11dfe-112">SubType: MFAudioFormat\_WMAudioV9, MFAudioFormat\_WMAudioV8, MFAudioFormat\_WMAudio\_Lossless, MFAudioFormat\_WMASPDIF</span></span>

-   <span data-ttu-id="11dfe-113">Codecs de vídeo do Windows Media</span><span class="sxs-lookup"><span data-stu-id="11dfe-113">Windows Media video codecs</span></span>

    <span data-ttu-id="11dfe-114">Categoria: **\_ \_ \_ codificador de vídeo de categoria MFT**</span><span class="sxs-lookup"><span data-stu-id="11dfe-114">Category: **MFT\_CATEGORY\_VIDEO\_ENCODER**</span></span>

    <span data-ttu-id="11dfe-115">Tipo principal: \_ vídeo MFMediaType</span><span class="sxs-lookup"><span data-stu-id="11dfe-115">Major type: MFMediaType\_Video</span></span>

    <span data-ttu-id="11dfe-116">Subtipo: MFVideoFormat \_ WVC1, MFVideoFormat \_ WMV3, MFVideoFormat \_ WMV2, MFVideoFormat \_ WMV1</span><span class="sxs-lookup"><span data-stu-id="11dfe-116">SubType: MFVideoFormat\_WVC1, MFVideoFormat\_WMV3, MFVideoFormat\_WMV2, MFVideoFormat\_WMV1</span></span>

<span data-ttu-id="11dfe-117">Esses codificadores são implementados como [Media Foundation transformação](media-foundation-transforms.md) (MFT) e Media Foundation fornece acesso ao aplicativo por meio da interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) do codificador.</span><span class="sxs-lookup"><span data-stu-id="11dfe-117">These encoders are implemented as [Media Foundation transform](media-foundation-transforms.md) (MFT) and Media Foundation provides access to the application through the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface of the encoder.</span></span> <span data-ttu-id="11dfe-118">Se você estiver usando componentes da camada de pipeline para codificação ASF, o MFT do codificador será inserido no pipeline como um nó de transformação porque é responsável por transformar dados de mídia que fluem pela origem para o coletor.</span><span class="sxs-lookup"><span data-stu-id="11dfe-118">If you are using pipeline layer components for ASF encoding, the encoder MFT is inserted into the pipeline as a transform node because it is responsible for transforming media data that flows through the source to the sink.</span></span> <span data-ttu-id="11dfe-119">Se a origem for um tipo compactado, o pipeline adicionará os decodificadores necessários para converter a origem em um tipo descompactado.</span><span class="sxs-lookup"><span data-stu-id="11dfe-119">If the source is a compressed type, then the pipeline adds the required decoders to convert the source into an uncompressed type.</span></span> <span data-ttu-id="11dfe-120">Um codificador tem um fluxo de entrada e um fluxo de saída.</span><span class="sxs-lookup"><span data-stu-id="11dfe-120">An encoder has one input stream and one output stream.</span></span> <span data-ttu-id="11dfe-121">O codificador recebe dados de entrada e produz dados codificados de acordo com a configuração e o formato definidos pelo aplicativo antes da sessão de codificação.</span><span class="sxs-lookup"><span data-stu-id="11dfe-121">The encoder receives input data and produces encoded data according to the configuration and format set by the application prior to the encoding session.</span></span> <span data-ttu-id="11dfe-122">O formato do fluxo de saída é descrito por um tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="11dfe-122">The format of the output stream is described by a media type.</span></span>

<span data-ttu-id="11dfe-123">Esta seção contém os seguintes tópicos.</span><span class="sxs-lookup"><span data-stu-id="11dfe-123">This section contains the following topics.</span></span>



| <span data-ttu-id="11dfe-124">Tópico</span><span class="sxs-lookup"><span data-stu-id="11dfe-124">Topic</span></span>                                                                              | <span data-ttu-id="11dfe-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="11dfe-125">Description</span></span>                                                                                 |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="11dfe-126">Criando uma instância de um MFT do codificador</span><span class="sxs-lookup"><span data-stu-id="11dfe-126">Instantiating an Encoder MFT</span></span>](instantiating-the-encoder-mft.md)                  | <span data-ttu-id="11dfe-127">Explica como criar o codificador.</span><span class="sxs-lookup"><span data-stu-id="11dfe-127">Explains how to create the encoder.</span></span>                                                         |
| [<span data-ttu-id="11dfe-128">Propriedades de codificação</span><span class="sxs-lookup"><span data-stu-id="11dfe-128">Encoding Properties</span></span>](configuring-the-encoder.md)                                 | <span data-ttu-id="11dfe-129">Explica como configurar o codificador definindo as propriedades apropriadas no MFT do codificador.</span><span class="sxs-lookup"><span data-stu-id="11dfe-129">Explains how to configure the encoder by setting appropriate properties on the encoder MFT.</span></span> |
| [<span data-ttu-id="11dfe-130">Negociação de tipo de mídia no codificador</span><span class="sxs-lookup"><span data-stu-id="11dfe-130">Media Type Negotiation on the Encoder</span></span>](media-type-negotiation-on-the-encoder.md) | <span data-ttu-id="11dfe-131">Explica como definir tipos de mídia de entrada e saída no codificador.</span><span class="sxs-lookup"><span data-stu-id="11dfe-131">Explains how to set input and output media types on the encoder.</span></span>                            |
| [<span data-ttu-id="11dfe-132">Configurando um codificador WMV</span><span class="sxs-lookup"><span data-stu-id="11dfe-132">Configuring a WMV Encoder</span></span>](configuring-a-wmv-encoder.md)                         | <span data-ttu-id="11dfe-133">Explica como configurar um codificador de vídeo do Windows Media (WMV).</span><span class="sxs-lookup"><span data-stu-id="11dfe-133">Explains how to configure a Windows Media Video (WMV) encoder.</span></span>                              |
| [<span data-ttu-id="11dfe-134">Configurando um tipo de saída para um codificador WMA</span><span class="sxs-lookup"><span data-stu-id="11dfe-134">Setting an Output Type for a WMA Encoder</span></span>](configuring-a-wma-encoder.md)          | <span data-ttu-id="11dfe-135">Explica como definir um tipo de saída em um codificador de áudio do Windows Media (WMA).</span><span class="sxs-lookup"><span data-stu-id="11dfe-135">Explains how to set an output type on a Windows Media Audio (WMA) encoder.</span></span>                  |



 

## <a name="related-topics"></a><span data-ttu-id="11dfe-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="11dfe-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11dfe-137">Componentes ASF da camada de pipeline</span><span class="sxs-lookup"><span data-stu-id="11dfe-137">Pipeline Layer ASF Components</span></span>](pipeline-layer-asf-components.md)
</dt> </dl>

 

 



