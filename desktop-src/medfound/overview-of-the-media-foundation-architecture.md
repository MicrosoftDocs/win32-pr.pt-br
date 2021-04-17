---
description: Este tópico descreve o design geral do Microsoft Media Foundation. Para obter informações sobre como usar Media Foundation para tarefas de programação específicas, consulte Media Foundation Guia de programação.
ms.assetid: DEA2B19A-CF15-4BF4-84C3-9A6417C942E2
title: Visão geral da arquitetura de Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0944eae1a74c1a5ba3dda8d94b69088128237f1
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104553206"
---
# <a name="overview-of-the-media-foundation-architecture"></a><span data-ttu-id="9fe3a-104">Visão geral da arquitetura de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9fe3a-104">Overview of the Media Foundation Architecture</span></span>

<span data-ttu-id="9fe3a-105">Este tópico descreve o design geral do Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="9fe3a-105">This topic describes the general design of Microsoft Media Foundation.</span></span> <span data-ttu-id="9fe3a-106">Para obter informações sobre como usar Media Foundation para tarefas de programação específicas, consulte [Media Foundation Guia de programação](media-foundation-programming-guide.md).</span><span class="sxs-lookup"><span data-stu-id="9fe3a-106">For information about using Media Foundation for specific programming tasks, see [Media Foundation Programming Guide](media-foundation-programming-guide.md).</span></span>

<span data-ttu-id="9fe3a-107">O diagrama a seguir mostra uma exibição de alto nível da arquitetura de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="9fe3a-107">The following diagram shows a high-level view of the Media Foundation architecture.</span></span>

![diagrama mostrando uma exibição de alto nível da arquitetura do Media Foundation.](images/mfarch01.png)

<span data-ttu-id="9fe3a-109">Media Foundation fornece dois modelos de programação distintos.</span><span class="sxs-lookup"><span data-stu-id="9fe3a-109">Media Foundation provides two distinct programming models.</span></span> <span data-ttu-id="9fe3a-110">O primeiro modelo, mostrado no lado esquerdo do diagrama, usa um pipeline de ponta a ponta para dados de mídia.</span><span class="sxs-lookup"><span data-stu-id="9fe3a-110">The first model, shown on the left side of the diagram, uses an end-to-end pipeline for media data.</span></span> <span data-ttu-id="9fe3a-111">O aplicativo Inicializa o pipeline — por exemplo, fornecendo a URL de um arquivo a ser reproduzido — e depois chama métodos para controlar o streaming.</span><span class="sxs-lookup"><span data-stu-id="9fe3a-111">The application initializes the pipeline—for example, by providing the URL of a file to play—and then calls methods to control streaming.</span></span> <span data-ttu-id="9fe3a-112">No segundo modelo, mostrado no lado direito do diagrama, o aplicativo obtém dados de uma fonte ou envia-os por push para um destino (ou ambos).</span><span class="sxs-lookup"><span data-stu-id="9fe3a-112">In the second model, shown on the right side of the diagram, the application either pulls data from a source, or pushes it to a destination (or both).</span></span> <span data-ttu-id="9fe3a-113">Esse modelo é particularmente útil se você precisar processar os dados, pois o aplicativo tem acesso direto ao fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="9fe3a-113">This model is particularly useful if you need to process the data, because the application has direct access to the data stream.</span></span>

### <a name="primitives-and-platform"></a><span data-ttu-id="9fe3a-114">Primitivas e plataforma</span><span class="sxs-lookup"><span data-stu-id="9fe3a-114">Primitives and Platform</span></span>

<span data-ttu-id="9fe3a-115">Começando na parte inferior do diagrama, os *primitivos* são objetos auxiliares usados em toda a API de Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="9fe3a-115">Starting from the bottom of the diagram, the *primitives* are helper objects used throughout the Media Foundation API:</span></span>

-   <span data-ttu-id="9fe3a-116">Os [atributos](attributes-and-properties.md) são uma maneira genérica de armazenar informações dentro de um objeto, como uma lista de pares de chave/valor.</span><span class="sxs-lookup"><span data-stu-id="9fe3a-116">[Attributes](attributes-and-properties.md) are a generic way to store information inside an object, as a list of key/value pairs.</span></span>
-   <span data-ttu-id="9fe3a-117">Os [tipos de mídia](media-types.md) descrevem o formato de um fluxo de dados de mídia.</span><span class="sxs-lookup"><span data-stu-id="9fe3a-117">[Media Types](media-types.md) describe the format of a media data stream.</span></span>
-   <span data-ttu-id="9fe3a-118">Os [buffers de mídia](media-buffers.md) armazenam partes de dados de mídia, como quadros de vídeo e amostras de áudio, e são usados para transportar dados entre objetos.</span><span class="sxs-lookup"><span data-stu-id="9fe3a-118">[Media Buffers](media-buffers.md) hold chunks of media data, such as video frames and audio samples, and are used to transport data between objects.</span></span>
-   <span data-ttu-id="9fe3a-119">[Exemplos de mídia](media-samples.md) são contêineres para buffers de mídia.</span><span class="sxs-lookup"><span data-stu-id="9fe3a-119">[Media Samples](media-samples.md) are containers for media buffers.</span></span> <span data-ttu-id="9fe3a-120">Eles também contêm metadados sobre os buffers, como carimbos de data/hora.</span><span class="sxs-lookup"><span data-stu-id="9fe3a-120">They also contain metadata about the buffers, such as time stamps.</span></span>

<span data-ttu-id="9fe3a-121">As [APIs da plataforma Media Foundation](media-foundation-platform-apis.md) fornecem algumas funcionalidades básicas que são usadas pelo pipeline de Media Foundation, como retornos de chamada e filas de trabalho assíncronos.</span><span class="sxs-lookup"><span data-stu-id="9fe3a-121">The [Media Foundation Platform APIs](media-foundation-platform-apis.md) provide some core functionality that is used by the Media Foundation pipeline, such as asynchronous callbacks and work queues.</span></span> <span data-ttu-id="9fe3a-122">Alguns aplicativos podem precisar chamar essas APIs diretamente; Além disso, você precisará delas se implementar uma fonte, transformação ou coletor personalizado para Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="9fe3a-122">Certain applications might need to call these APIs directly; also, you will need them if you implement a custom source, transform, or sink for Media Foundation.</span></span>

### <a name="media-pipeline"></a><span data-ttu-id="9fe3a-123">Pipeline de mídia</span><span class="sxs-lookup"><span data-stu-id="9fe3a-123">Media Pipeline</span></span>

<span data-ttu-id="9fe3a-124">O pipeline de mídia contém três tipos de objeto que geram ou processam dados de mídia:</span><span class="sxs-lookup"><span data-stu-id="9fe3a-124">The media pipeline contains three types of object that generate or process media data:</span></span>

-   <span data-ttu-id="9fe3a-125">As [fontes de mídia](media-sources.md) introduzem dados no pipeline.</span><span class="sxs-lookup"><span data-stu-id="9fe3a-125">[Media Sources](media-sources.md) introduce data into the pipeline.</span></span> <span data-ttu-id="9fe3a-126">Uma fonte de mídia pode obter dados de um arquivo local, como um arquivo de vídeo; de um fluxo de rede; ou de um dispositivo de captura de hardware.</span><span class="sxs-lookup"><span data-stu-id="9fe3a-126">A media source might get data from a local file, such as a video file; from a network stream; or from a hardware capture device.</span></span>
-   <span data-ttu-id="9fe3a-127">[Media Foundation transformações](media-foundation-transforms.md) (MFTs) processam dados de um fluxo.</span><span class="sxs-lookup"><span data-stu-id="9fe3a-127">[Media Foundation Transforms](media-foundation-transforms.md) (MFTs) process data from a stream.</span></span> <span data-ttu-id="9fe3a-128">Os codificadores e os decodificadores são implementados como MFTs.</span><span class="sxs-lookup"><span data-stu-id="9fe3a-128">Encoders and decoders are implemented as MFTs.</span></span>
-   <span data-ttu-id="9fe3a-129">Os [coletores de mídia](media-sinks.md) consomem os dados; por exemplo, mostrando o vídeo na exibição, reproduzindo áudio ou gravando os dados em um arquivo de mídia.</span><span class="sxs-lookup"><span data-stu-id="9fe3a-129">[Media Sinks](media-sinks.md) consume the data; for example, by showing video on the display, playing audio, or writing the data to a media file.</span></span>

<span data-ttu-id="9fe3a-130">Terceiros podem implementar suas próprias fontes personalizadas, coletores e MFTs; por exemplo, para dar suporte a novos formatos de arquivo de mídia.</span><span class="sxs-lookup"><span data-stu-id="9fe3a-130">Third parties can implement their own custom sources, sinks, and MFTs; for example, to support new media file formats.</span></span>

<span data-ttu-id="9fe3a-131">A [sessão de mídia](media-session.md) controla o fluxo de dados por meio do pipeline e manipula tarefas como controle de qualidade, sincronização de áudio/vídeo e resposta a alterações de formato.</span><span class="sxs-lookup"><span data-stu-id="9fe3a-131">The [Media Session](media-session.md) controls the flow of data through the pipeline, and handles tasks such as quality control, audio/video synchronization, and responding to format changes.</span></span>

### <a name="source-reader-and-sink-writer"></a><span data-ttu-id="9fe3a-132">Leitor de fonte e gravador de coletor</span><span class="sxs-lookup"><span data-stu-id="9fe3a-132">Source Reader and Sink Writer</span></span>

<span data-ttu-id="9fe3a-133">O [leitor de origem](source-reader.md) e o [gravador do coletor](sink-writer.md) fornecem uma maneira alternativa de usar os componentes básicos do Media Foundation (fontes de mídia, transformações e coletores de mídia).</span><span class="sxs-lookup"><span data-stu-id="9fe3a-133">The [Source Reader](source-reader.md) and [Sink Writer](sink-writer.md) provide an alternative way to use the basic Media Foundation components (media sources, transforms, and media sinks).</span></span> <span data-ttu-id="9fe3a-134">O leitor de origem hospeda uma fonte de mídia e zero ou mais decodificadores, enquanto o gravador de coletor hospeda um coletor de mídia e zero ou mais codificadores.</span><span class="sxs-lookup"><span data-stu-id="9fe3a-134">The source reader hosts a media source and zero or more decoders, while the sink writer hosts a media sink and zero or more encoders.</span></span> <span data-ttu-id="9fe3a-135">Você pode usar o leitor de origem para obter dados compactados ou descompactados de uma fonte de mídia e usar o gravador de coletor para codificar dados e enviar os dados para um coletor de mídia.</span><span class="sxs-lookup"><span data-stu-id="9fe3a-135">You can use the source reader to get compressed or uncompressed data from a media source, and use the sink writer to encode data and send the data to a media sink.</span></span>

> [!Note]  
> <span data-ttu-id="9fe3a-136">O leitor de fonte e o gravador de coletor estão disponíveis no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9fe3a-136">The source reader and sink writer are available in Windows 7.</span></span>

 

<span data-ttu-id="9fe3a-137">Esse modelo de programação fornece ao aplicativo mais controle sobre o fluxo de dados e também fornece ao aplicativo acesso direto aos dados da origem.</span><span class="sxs-lookup"><span data-stu-id="9fe3a-137">This programming model gives the application more control over the flow of data, and also gives the application direct access to the data from the source.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9fe3a-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9fe3a-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9fe3a-139">Media Foundation: conceitos essenciais</span><span class="sxs-lookup"><span data-stu-id="9fe3a-139">Media Foundation: Essential Concepts</span></span>](media-foundation-programming--essential-concepts.md)
</dt> <dt>

[<span data-ttu-id="9fe3a-140">Arquitetura Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9fe3a-140">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> </dl>

 

 



