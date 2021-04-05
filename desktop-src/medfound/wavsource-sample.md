---
description: Exemplo de WavSource
ms.assetid: 905fbba5-0a04-4048-80bd-f8707c4879da
title: Exemplo de WavSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 050edb9df75032384f93c6e1f37c52e89f14a748
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827791"
---
# <a name="wavsource-sample"></a><span data-ttu-id="30b7d-103">Exemplo de WavSource</span><span class="sxs-lookup"><span data-stu-id="30b7d-103">WavSource Sample</span></span>

<span data-ttu-id="30b7d-104">Mostra como criar uma fonte de mídia personalizada no Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="30b7d-104">Shows how to create a custom media source in Microsoft Media Foundation.</span></span> <span data-ttu-id="30b7d-105">O exemplo implementa uma fonte de mídia que analisa arquivos de áudio. wav.</span><span class="sxs-lookup"><span data-stu-id="30b7d-105">The sample implements a media source that parses .wav audio files.</span></span>

<span data-ttu-id="30b7d-106">Este exemplo é um exemplo relativamente simples de uma fonte de mídia:</span><span class="sxs-lookup"><span data-stu-id="30b7d-106">This sample is a relatively simple example of a media source:</span></span>

-   <span data-ttu-id="30b7d-107">Há apenas um fluxo, portanto, não há nenhum código para implementar a seleção de fluxo.</span><span class="sxs-lookup"><span data-stu-id="30b7d-107">There is only one stream, so there is no code to implement stream selection.</span></span>
-   <span data-ttu-id="30b7d-108">A origem da mídia não implementa o controle de taxa (isto é, reprodução rápida ou inversa).</span><span class="sxs-lookup"><span data-stu-id="30b7d-108">The media source does not implement rate control (that is, fast forward or reverse playback).</span></span>
-   <span data-ttu-id="30b7d-109">Todos os métodos de origem e de fluxo são implementados como métodos síncronos.</span><span class="sxs-lookup"><span data-stu-id="30b7d-109">All source and stream methods are implemented as synchronous methods.</span></span>
-   <span data-ttu-id="30b7d-110">Como a parte de dados de um arquivo. wav é um único bloco de áudio PCM descompactado, a origem da mídia não precisa ler cabeçalhos de pacote ou analisar o fluxo durante a reprodução, além de ler o cabeçalho [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat) inicial.</span><span class="sxs-lookup"><span data-stu-id="30b7d-110">Because the data portion of a .wav file is a single block of uncompressed PCM audio, the media source does not need to read packet headers or otherwise parse the stream during playback, other than reading the initial [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat) header.</span></span>

<span data-ttu-id="30b7d-111">Para obter um exemplo mais avançado de uma fonte de mídia, consulte o [exemplo MPEG1Source](mpeg1source-sample.md).</span><span class="sxs-lookup"><span data-stu-id="30b7d-111">For a more advanced example of a media source, see the [MPEG1Source Sample](mpeg1source-sample.md).</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="30b7d-112">APIs demonstradas</span><span class="sxs-lookup"><span data-stu-id="30b7d-112">APIs Demonstrated</span></span>

<span data-ttu-id="30b7d-113">Este exemplo demonstra as seguintes interfaces de Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="30b7d-113">This sample demonstrates the following Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="30b7d-114">**IMFByteStreamHandler**</span><span class="sxs-lookup"><span data-stu-id="30b7d-114">**IMFByteStreamHandler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)
-   [<span data-ttu-id="30b7d-115">**IMFMediaSource**</span><span class="sxs-lookup"><span data-stu-id="30b7d-115">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
-   [<span data-ttu-id="30b7d-116">**IMFMediaStream**</span><span class="sxs-lookup"><span data-stu-id="30b7d-116">**IMFMediaStream**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)

## <a name="usage"></a><span data-ttu-id="30b7d-117">Uso</span><span class="sxs-lookup"><span data-stu-id="30b7d-117">Usage</span></span>

<span data-ttu-id="30b7d-118">O exemplo WavSource cria uma DLL que é um servidor COM para o manipulador de fluxo de bytes de origem de mídia e de mídia.</span><span class="sxs-lookup"><span data-stu-id="30b7d-118">The WavSource sample builds a DLL that is a COM server for both the media source and media source's byte-stream handler.</span></span> <span data-ttu-id="30b7d-119">Antes de usar a origem de mídia, você deve registrar a DLL.</span><span class="sxs-lookup"><span data-stu-id="30b7d-119">Before using the media source, you must register the DLL.</span></span>

<span data-ttu-id="30b7d-120">Para usar a origem de mídia, você pode executar o [BasicPlayback](/previous-versions//bb970475(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="30b7d-120">To use the media source, you can run the [BasicPlayback](/previous-versions//bb970475(v=vs.85)).</span></span> <span data-ttu-id="30b7d-121">O resolvedor de origem carregará automaticamente a origem de mídia se você selecionar um arquivo. wav para reprodução.</span><span class="sxs-lookup"><span data-stu-id="30b7d-121">The source resolver will automatically load the media source if you select a .wav file for playback.</span></span> <span data-ttu-id="30b7d-122">(Se ocorrer um erro, verifique se você registrou com êxito a DLL WavSource.)</span><span class="sxs-lookup"><span data-stu-id="30b7d-122">(If an error occurs, make sure that you successfully registered the WavSource DLL.)</span></span>

<span data-ttu-id="30b7d-123">Você também pode usar a ferramenta TopoEdit para criar uma topologia de reprodução que contenha a origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="30b7d-123">You can also use the TopoEdit tool to build a playback topology that contains the media source.</span></span> <span data-ttu-id="30b7d-124">Para obter mais informações sobre TopoEdit, consulte [TopoEdit](topoedit.md).</span><span class="sxs-lookup"><span data-stu-id="30b7d-124">For more information about TopoEdit, see [TopoEdit](topoedit.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="30b7d-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30b7d-125">Requirements</span></span>



| <span data-ttu-id="30b7d-126">Produto</span><span class="sxs-lookup"><span data-stu-id="30b7d-126">Product</span></span>                                                        | <span data-ttu-id="30b7d-127">Versão</span><span class="sxs-lookup"><span data-stu-id="30b7d-127">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="30b7d-128">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="30b7d-128">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="30b7d-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="30b7d-129">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="30b7d-130">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="30b7d-130">Downloading the Sample</span></span>

<span data-ttu-id="30b7d-131">Este exemplo está disponível no [repositório GitHub de exemplos clássicos do Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/wavsource).</span><span class="sxs-lookup"><span data-stu-id="30b7d-131">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/wavsource).</span></span>

## <a name="related-topics"></a><span data-ttu-id="30b7d-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="30b7d-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30b7d-133">Exemplos de SDK do Media Foundation</span><span class="sxs-lookup"><span data-stu-id="30b7d-133">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="30b7d-134">Fontes de mídia</span><span class="sxs-lookup"><span data-stu-id="30b7d-134">Media Sources</span></span>](media-sources.md)
</dt> <dt>

[<span data-ttu-id="30b7d-135">Exemplo de MPEG1Source</span><span class="sxs-lookup"><span data-stu-id="30b7d-135">MPEG1Source Sample</span></span>](mpeg1source-sample.md)
</dt> <dt>

[<span data-ttu-id="30b7d-136">Manipuladores de esquema e manipuladores de Byte-Stream</span><span class="sxs-lookup"><span data-stu-id="30b7d-136">Scheme Handlers and Byte-Stream Handlers</span></span>](scheme-handlers-and-byte-stream-handlers.md)
</dt> <dt>

[<span data-ttu-id="30b7d-137">Gravando uma fonte de mídia personalizada</span><span class="sxs-lookup"><span data-stu-id="30b7d-137">Writing a Custom Media Source</span></span>](writing-a-custom-media-source.md)
</dt> </dl>

 

 
