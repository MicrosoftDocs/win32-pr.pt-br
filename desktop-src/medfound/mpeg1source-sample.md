---
description: Exemplo de MPEG1Source
ms.assetid: c9f131ff-0b79-487c-9a46-a9b1350553a1
title: Exemplo de MPEG1Source
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c71bd541a7bd01621ca7359eb9e229a08e91a04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105748948"
---
# <a name="mpeg1source-sample"></a><span data-ttu-id="408b1-103">Exemplo de MPEG1Source</span><span class="sxs-lookup"><span data-stu-id="408b1-103">MPEG1Source Sample</span></span>

<span data-ttu-id="408b1-104">Mostra como gravar uma fonte de mídia personalizada no Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="408b1-104">Shows how to write a custom media source in Microsoft Media Foundation.</span></span> <span data-ttu-id="408b1-105">O exemplo implementa uma fonte de mídia que analisa os fluxos de camada de sistemas MPEG-1 e gera exemplos que contêm cargas MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="408b1-105">The sample implements a media source that parses MPEG-1 systems-layer streams and generates samples that contain MPEG-1 payloads.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="408b1-106">APIs demonstradas</span><span class="sxs-lookup"><span data-stu-id="408b1-106">APIs Demonstrated</span></span>

<span data-ttu-id="408b1-107">Este exemplo demonstra as seguintes interfaces de Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="408b1-107">This sample demonstrates the following Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="408b1-108">**IMFByteStreamHandler**</span><span class="sxs-lookup"><span data-stu-id="408b1-108">**IMFByteStreamHandler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)
-   [<span data-ttu-id="408b1-109">**IMFMediaSource**</span><span class="sxs-lookup"><span data-stu-id="408b1-109">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
-   [<span data-ttu-id="408b1-110">**IMFMediaStream**</span><span class="sxs-lookup"><span data-stu-id="408b1-110">**IMFMediaStream**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)

<span data-ttu-id="408b1-111">Antes de examinar este exemplo, talvez você queira examinar o [exemplo WavSource](wavsource-sample.md), que fornece uma implementação mais simples de uma fonte de mídia.</span><span class="sxs-lookup"><span data-stu-id="408b1-111">Before examining this sample, you might want to review the [WavSource Sample](wavsource-sample.md), which provides a simpler implementation of a media source.</span></span> <span data-ttu-id="408b1-112">O exemplo MPEG1Source adiciona alguns recursos que seriam encontrados na maioria das implementações do mundo real de uma fonte de mídia:</span><span class="sxs-lookup"><span data-stu-id="408b1-112">The MPEG1Source sample adds some features that would be found in most real-world implementations of a media source:</span></span>

-   <span data-ttu-id="408b1-113">Vários fluxos</span><span class="sxs-lookup"><span data-stu-id="408b1-113">Multiple streams</span></span>
-   <span data-ttu-id="408b1-114">Métodos assíncronos</span><span class="sxs-lookup"><span data-stu-id="408b1-114">Asynchronous methods</span></span>
-   <span data-ttu-id="408b1-115">E/s assíncrona</span><span class="sxs-lookup"><span data-stu-id="408b1-115">Asynchronous I/O</span></span>

<span data-ttu-id="408b1-116">No SDK do Windows para o Windows Server 2008, este exemplo também inclui um decodificador de vídeo MPEG-1 de exemplo que exibe o código de tempo para cada quadro de vídeo.</span><span class="sxs-lookup"><span data-stu-id="408b1-116">In the Windows SDK for Windows Server 2008, this sample also includes a sample MPEG-1 video decoder that displays the time code for each video frame.</span></span> <span data-ttu-id="408b1-117">(Na verdade, ele não decodifica o fragmentado MPEG-1.)</span><span class="sxs-lookup"><span data-stu-id="408b1-117">(It does not actually decode the MPEG-1 bitstream.)</span></span>

<span data-ttu-id="408b1-118">A partir do SDK do Windows para o Windows 7, o decodificador foi movido para um exemplo separado.</span><span class="sxs-lookup"><span data-stu-id="408b1-118">Starting in the Windows SDK for Windows 7, the decoder has been moved to a separate sample.</span></span> <span data-ttu-id="408b1-119">Consulte o [exemplo de decodificador](decoder-sample.md).</span><span class="sxs-lookup"><span data-stu-id="408b1-119">See [Decoder Sample](decoder-sample.md).</span></span>

## <a name="usage"></a><span data-ttu-id="408b1-120">Uso</span><span class="sxs-lookup"><span data-stu-id="408b1-120">Usage</span></span>

<span data-ttu-id="408b1-121">O exemplo MPEG1Source cria uma DLL que é um servidor COM para a origem de mídia, o manipulador de fluxo de bytes de origem de mídia e o MFT do decodificador.</span><span class="sxs-lookup"><span data-stu-id="408b1-121">The MPEG1Source sample builds a DLL that is a COM server for the media source, media source's byte-stream handler, and the decoder MFT.</span></span> <span data-ttu-id="408b1-122">Antes de usar a origem de mídia, você deve registrar a DLL.</span><span class="sxs-lookup"><span data-stu-id="408b1-122">Before using the media source, you must register the DLL.</span></span>

<span data-ttu-id="408b1-123">Para usar a origem de mídia, você pode executar o [exemplo BasicPlayback](/previous-versions//bb970475(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="408b1-123">To use the media source, you can run the [BasicPlayback Sample](/previous-versions//bb970475(v=vs.85)).</span></span> <span data-ttu-id="408b1-124">O resolvedor de origem carregará automaticamente a origem de mídia se você selecionar um arquivo MPEG-1 para reprodução.</span><span class="sxs-lookup"><span data-stu-id="408b1-124">The source resolver will automatically load the media source if you select an MPEG-1 file for playback.</span></span> <span data-ttu-id="408b1-125">(Se ocorrer um erro, verifique se você registrou com êxito a DLL MPEG1Source.)</span><span class="sxs-lookup"><span data-stu-id="408b1-125">(If an error occurs, make sure that you successfully registered the MPEG1Source DLL.)</span></span>

<span data-ttu-id="408b1-126">Você também pode usar a ferramenta TopoEdit para criar uma topologia de reprodução que contenha a origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="408b1-126">You can also use the TopoEdit tool to build a playback topology that contains the media source.</span></span> <span data-ttu-id="408b1-127">Para obter mais informações sobre TopoEdit, consulte [TopoEdit](topoedit.md).</span><span class="sxs-lookup"><span data-stu-id="408b1-127">For more information about TopoEdit, see [TopoEdit](topoedit.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="408b1-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="408b1-128">Requirements</span></span>



| <span data-ttu-id="408b1-129">Produto</span><span class="sxs-lookup"><span data-stu-id="408b1-129">Product</span></span>                                                        | <span data-ttu-id="408b1-130">Versão</span><span class="sxs-lookup"><span data-stu-id="408b1-130">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="408b1-131">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="408b1-131">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="408b1-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="408b1-132">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="408b1-133">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="408b1-133">Downloading the Sample</span></span>

<span data-ttu-id="408b1-134">Este exemplo está disponível no [repositório GitHub de exemplos clássicos do Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mpeg1source).</span><span class="sxs-lookup"><span data-stu-id="408b1-134">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mpeg1source).</span></span>

## <a name="related-topics"></a><span data-ttu-id="408b1-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="408b1-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="408b1-136">Exemplos de SDK do Media Foundation</span><span class="sxs-lookup"><span data-stu-id="408b1-136">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="408b1-137">Fontes de mídia</span><span class="sxs-lookup"><span data-stu-id="408b1-137">Media Sources</span></span>](media-sources.md)
</dt> <dt>

[<span data-ttu-id="408b1-138">Manipuladores de esquema e manipuladores de Byte-Stream</span><span class="sxs-lookup"><span data-stu-id="408b1-138">Scheme Handlers and Byte-Stream Handlers</span></span>](scheme-handlers-and-byte-stream-handlers.md)
</dt> <dt>

[<span data-ttu-id="408b1-139">Tutorial: escrevendo uma fonte de mídia personalizada</span><span class="sxs-lookup"><span data-stu-id="408b1-139">Tutorial: Writing a Custom Media Source</span></span>](tutorial--writing-a-custom-media-source.md)
</dt> <dt>

[<span data-ttu-id="408b1-140">Exemplo de WavSource</span><span class="sxs-lookup"><span data-stu-id="408b1-140">WavSource Sample</span></span>](wavsource-sample.md)
</dt> </dl>

 

 
