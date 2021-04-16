---
description: Este tópico é uma visão geral das APIs de codificação de arquivo fornecidas no Microsoft Media Foundation.
ms.assetid: 69dbef63-e272-4ad2-8d04-ae9366f79b33
title: Visão geral da codificação no Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81882bd6da43f4040614347b662d988844c7b7a6
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104558069"
---
# <a name="overview-of-encoding-in-media-foundation"></a><span data-ttu-id="76f5e-103">Visão geral da codificação no Media Foundation</span><span class="sxs-lookup"><span data-stu-id="76f5e-103">Overview of Encoding in Media Foundation</span></span>

<span data-ttu-id="76f5e-104">Este tópico é uma visão geral das APIs de codificação de arquivo fornecidas no Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="76f5e-104">This topic is an overview of the file encoding APIs provided in Microsoft Media Foundation.</span></span>

## <a name="terminology"></a><span data-ttu-id="76f5e-105">Terminologia</span><span class="sxs-lookup"><span data-stu-id="76f5e-105">Terminology</span></span>

<span data-ttu-id="76f5e-106">A *codificação* é um termo geral que abrange vários processos distintos:</span><span class="sxs-lookup"><span data-stu-id="76f5e-106">*Encoding* is a general term that covers several distinct processes:</span></span>

1.  <span data-ttu-id="76f5e-107">Codificação de um fluxo de áudio ou vídeo em formatos compactados.</span><span class="sxs-lookup"><span data-stu-id="76f5e-107">Encoding an audio or video stream into a compressed formats.</span></span> <span data-ttu-id="76f5e-108">Por exemplo, codificar um fluxo de vídeo para o vídeo H. 264.</span><span class="sxs-lookup"><span data-stu-id="76f5e-108">For example, encoding a video stream to H.264 video.</span></span>
2.  <span data-ttu-id="76f5e-109">Multiplexação ("muxing") de um ou mais fluxos em um único fluxo de bytes.</span><span class="sxs-lookup"><span data-stu-id="76f5e-109">Multiplexing ("muxing") one or more streams into a single byte stream.</span></span> <span data-ttu-id="76f5e-110">Normalmente, os fluxos de entrada são codificados primeiro.</span><span class="sxs-lookup"><span data-stu-id="76f5e-110">Typically, the incoming streams are encoded first.</span></span> <span data-ttu-id="76f5e-111">Essa etapa pode envolver o pacote de fluxos codificados.</span><span class="sxs-lookup"><span data-stu-id="76f5e-111">This step might involve packetizing the encoded streams.</span></span>
3.  <span data-ttu-id="76f5e-112">Gravar um fluxo de bytes multiplexados em um arquivo, como um arquivo MP4 ou um formato de sistema avançado (ASF).</span><span class="sxs-lookup"><span data-stu-id="76f5e-112">Writing a multiplexed byte stream to a file, such as an MP4 or Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="76f5e-113">Como alternativa, o fluxo multiplexado pode ser enviado pela rede.</span><span class="sxs-lookup"><span data-stu-id="76f5e-113">Alternatively, the multiplexed stream can be sent over the network.</span></span>

<span data-ttu-id="76f5e-114">O diagrama a seguir mostra esses três processos:</span><span class="sxs-lookup"><span data-stu-id="76f5e-114">The following diagram shows these three processes:</span></span>

![diagrama mostrando os processos de codificação e multiplexação](images/encoding03.png)

<span data-ttu-id="76f5e-116">As variações desse processo incluem transcodificação e remuxing:</span><span class="sxs-lookup"><span data-stu-id="76f5e-116">Variations of this process include transcoding and remuxing:</span></span>

-   <span data-ttu-id="76f5e-117">*Transcodificação* significa decodificar um arquivo existente, codificar novamente os fluxos e remultiplexar os fluxos codificados.</span><span class="sxs-lookup"><span data-stu-id="76f5e-117">*Transcoding* means decoding an existing file, re-encoding the streams, and re-multiplexing the encoded streams.</span></span> <span data-ttu-id="76f5e-118">A transcodificação pode ser feita para converter um arquivo de um tipo de codificação para outro; por exemplo, para converter o vídeo H. 264 no vídeo do Windows Media (WMV).</span><span class="sxs-lookup"><span data-stu-id="76f5e-118">Transcoding might be done to convert a file from one encoding type to another; for example, to convert H.264 video to Windows Media Video (WMV).</span></span> <span data-ttu-id="76f5e-119">Também pode ser feito para alterar a taxa de bits codificada; o tamanho do quadro do vídeo; a taxa de quadros; ou outros parâmetros de formato.</span><span class="sxs-lookup"><span data-stu-id="76f5e-119">It can also be done to change the encoded bit rate; the video frame size; the frame rate; or other format parameters.</span></span>
-   <span data-ttu-id="76f5e-120">A *remultiplexação* ou *remuxing* significa demultiplexar um arquivo e remultiplexar os fluxos, sem nenhuma etapa de decodificação/codificação.</span><span class="sxs-lookup"><span data-stu-id="76f5e-120">*Remultiplexing* or *remuxing* means demultiplexing a file and re-multiplexing the streams, with no decode/encode step.</span></span> <span data-ttu-id="76f5e-121">Isso pode ser feito para alterar como os pacotes de áudio/vídeo são multiplexados, para remover um fluxo ou para combinar fluxos de dois arquivos de origem diferentes.</span><span class="sxs-lookup"><span data-stu-id="76f5e-121">This might be done to change how the audio/video packets are multiplexed, to remove a stream, or to combine streams from two different source files.</span></span>
-   <span data-ttu-id="76f5e-122">A *transclassificação* é um caso especial de transcodificação, em que a taxa de bits é alterada sem alterar o tipo de compactação.</span><span class="sxs-lookup"><span data-stu-id="76f5e-122">*Transrating* is a special case of transcoding, where the bit-rate is changed without changing the compression type.</span></span> <span data-ttu-id="76f5e-123">Por exemplo, você pode converter um arquivo de alta taxa de bits em uma taxa de bits inferior.</span><span class="sxs-lookup"><span data-stu-id="76f5e-123">For example, you might convert a high-bit-rate file to a lower bit-rate.</span></span> <span data-ttu-id="76f5e-124">Um cenário típico no qual a transclassificação pode ser usada é ao sincronizar o conteúdo de mídia de um PC para um dispositivo portátil.</span><span class="sxs-lookup"><span data-stu-id="76f5e-124">A typical scenario in which transrating might be used is when synchronizing media content from a PC to a portable device.</span></span> <span data-ttu-id="76f5e-125">Se o dispositivo portátil não oferecer suporte a uma taxa de bits alta, o arquivo poderá ser transformado antes de ser copiado para o dispositivo portátil.</span><span class="sxs-lookup"><span data-stu-id="76f5e-125">If the portable device does not support a high bit rate, the file might be transrated before it is copied to the portable device.</span></span>

<span data-ttu-id="76f5e-126">O diagrama de bloco a seguir mostra o processo de transcodificação.</span><span class="sxs-lookup"><span data-stu-id="76f5e-126">The following block diagram shows the transcoding process.</span></span>

![diagrama mostrando o processo de transcodificação](images/encoding05.png)

<span data-ttu-id="76f5e-128">O diagrama de bloco a seguir mostra o processo remuxing.</span><span class="sxs-lookup"><span data-stu-id="76f5e-128">The following block diagram shows the remuxing process.</span></span>

![diagrama mostrando o processo remuxing](images/encoding06.png)

<span data-ttu-id="76f5e-130">Essa documentação às vezes usa a *codificação* de termo para incluir transcodificação e remuxing.</span><span class="sxs-lookup"><span data-stu-id="76f5e-130">This documentation sometimes uses the term *encoding* to include both transcoding and remuxing.</span></span> <span data-ttu-id="76f5e-131">Quando for importante distinguir entre eles, a documentação notará a diferença.</span><span class="sxs-lookup"><span data-stu-id="76f5e-131">When it is important to distinguish between them, the documentation will note the difference.</span></span>

<span data-ttu-id="76f5e-132">Consulte também: [Media Foundation: conceitos essenciais](media-foundation-programming--essential-concepts.md).</span><span class="sxs-lookup"><span data-stu-id="76f5e-132">See also: [Media Foundation: Essential Concepts](media-foundation-programming--essential-concepts.md).</span></span>

## <a name="media-foundation-encoding-architecture"></a><span data-ttu-id="76f5e-133">Arquitetura de codificação de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="76f5e-133">Media Foundation Encoding Architecture</span></span>

<span data-ttu-id="76f5e-134">Na camada mais baixa da arquitetura de Media Foundation, os seguintes tipos de componente são usados para codificação:</span><span class="sxs-lookup"><span data-stu-id="76f5e-134">At the lowest layer of the Media Foundation architecture, the following types of component are used for encoding:</span></span>

-   <span data-ttu-id="76f5e-135">Para transcodificação, as [fontes de mídia](media-sources.md) são usadas para demultiplexar o arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="76f5e-135">For transcoding, [Media Sources](media-sources.md) are used to demultiplex the source file.</span></span>
-   <span data-ttu-id="76f5e-136">Para o processo de codificação, [Media Foundation transformações](media-foundation-transforms.md) são usadas para decodificar e codificar fluxos.</span><span class="sxs-lookup"><span data-stu-id="76f5e-136">For the encoding process, [Media Foundation Transforms](media-foundation-transforms.md) are used to decode and encode streams.</span></span>
-   <span data-ttu-id="76f5e-137">Para o processo de multiplexação, os [coletores de mídia](media-sinks.md) são usados para multiplexar os fluxos e gravar o fluxo multiplexado em um arquivo ou rede.</span><span class="sxs-lookup"><span data-stu-id="76f5e-137">For the multiplexing process, [Media Sinks](media-sinks.md) are used to multiplex the streams and write the multiplexed stream to a file or network.</span></span>

<span data-ttu-id="76f5e-138">O diagrama a seguir mostra o fluxo de dados entre esses componentes em um cenário de transcodificação:</span><span class="sxs-lookup"><span data-stu-id="76f5e-138">The following diagram shows the data flow between these components in a transcoding scenario:</span></span>

![diagrama mostrando os componentes usados na transcodificação](images/encoding04.png)

<span data-ttu-id="76f5e-140">A maioria dos aplicativos não usará esses componentes diretamente.</span><span class="sxs-lookup"><span data-stu-id="76f5e-140">Most applications will not use these components directly.</span></span> <span data-ttu-id="76f5e-141">Em vez disso, um aplicativo usará APIs de nível superior que gerenciam esses componentes de nível inferior.</span><span class="sxs-lookup"><span data-stu-id="76f5e-141">Instead, an application will use higher-level APIs that manage these lower-level components.</span></span> <span data-ttu-id="76f5e-142">Media Foundation fornece duas APIs de nível superior para codificação:</span><span class="sxs-lookup"><span data-stu-id="76f5e-142">Media Foundation provides two higher-level APIs for encoding:</span></span>

<dl> <dt>

<span data-ttu-id="76f5e-143"><span id="Media_Session"></span><span id="media_session"></span><span id="MEDIA_SESSION"></span>[Sessão de mídia](media-session.md)</span><span class="sxs-lookup"><span data-stu-id="76f5e-143"><span id="Media_Session"></span><span id="media_session"></span><span id="MEDIA_SESSION"></span>[Media Session](media-session.md)</span></span>
</dt> <dd>

<span data-ttu-id="76f5e-144">A sessão de mídia fornece um pipeline de ponta a ponta que move dados da origem de mídia, por meio dos codecs e, por fim, para o coletor de mídia.</span><span class="sxs-lookup"><span data-stu-id="76f5e-144">The Media Session provides an end-to-end pipeline that moves data from the media source, through the codecs, and finally to the media sink.</span></span> <span data-ttu-id="76f5e-145">O aplicativo controla a sessão de mídia e recebe eventos de status da sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="76f5e-145">The application controls the Media Session and receives status events from the Media Session.</span></span>

</dd> <dt>

<span data-ttu-id="76f5e-146"><span id="Source_Reader_plus_Sink_Writer"></span><span id="source_reader_plus_sink_writer"></span><span id="SOURCE_READER_PLUS_SINK_WRITER"></span>[Leitor de origem](source-reader.md) mais [gravador de coletor](sink-writer.md)</span><span class="sxs-lookup"><span data-stu-id="76f5e-146"><span id="Source_Reader_plus_Sink_Writer"></span><span id="source_reader_plus_sink_writer"></span><span id="SOURCE_READER_PLUS_SINK_WRITER"></span>[Source Reader](source-reader.md) plus [Sink Writer](sink-writer.md)</span></span>
</dt> <dd>

<span data-ttu-id="76f5e-147">O leitor de origem encapsula a fonte de mídia e, opcionalmente, os decodificadores.</span><span class="sxs-lookup"><span data-stu-id="76f5e-147">The Source Reader wraps the media source and optionally the decoders.</span></span> <span data-ttu-id="76f5e-148">Ele fornece amostras codificadas ou decodificadas do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="76f5e-148">It delivers either encoded or decoded samples the application.</span></span> <span data-ttu-id="76f5e-149">O gravador do coletor encapsula o coletor de mídia e, opcionalmente, os codificadores.</span><span class="sxs-lookup"><span data-stu-id="76f5e-149">The Sink Writer wraps the media sink and optionally the encoders.</span></span> <span data-ttu-id="76f5e-150">O aplicativo passa amostras para o gravador do coletor.</span><span class="sxs-lookup"><span data-stu-id="76f5e-150">The application passes samples to the Sink Writer.</span></span>

</dd> </dl>

<span data-ttu-id="76f5e-151">O diagrama a seguir mostra a sessão de mídia:</span><span class="sxs-lookup"><span data-stu-id="76f5e-151">The following diagram shows the Media Session:</span></span>

![diagrama mostrando como a sessão de mídia executa transcodificação](images/encoding01.png)

<span data-ttu-id="76f5e-153">A [API de transcodificação](transcode-api.md) (a caixa sombreada azul) é um conjunto de APIs introduzidas no Windows 7, que facilitam a configuração da sessão de mídia para codificação.</span><span class="sxs-lookup"><span data-stu-id="76f5e-153">The [Transcode API](transcode-api.md) (the blue shaded box) is a set of APIs introduced in Windows 7, which make it easier to configure the Media Session for encoding.</span></span>

<span data-ttu-id="76f5e-154">O próximo diagrama mostra o leitor de fonte e o gravador de coletor:</span><span class="sxs-lookup"><span data-stu-id="76f5e-154">The next diagram shows the Source Reader and Sink Writer:</span></span>

![diagrama mostrando transcodificação com o leitor de fonte e o gravador de coletor](images/encoding02.png)

## <a name="related-topics"></a><span data-ttu-id="76f5e-156">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="76f5e-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76f5e-157">Codificando e criando arquivos</span><span class="sxs-lookup"><span data-stu-id="76f5e-157">Encoding and File Authoring</span></span>](encoding-and-file-authoring.md)
</dt> <dt>

[<span data-ttu-id="76f5e-158">Programação de Media Foundation: conceitos essenciais</span><span class="sxs-lookup"><span data-stu-id="76f5e-158">Media Foundation Programming: Essential Concepts</span></span>](media-foundation-programming--essential-concepts.md)
</dt> </dl>

 

 



