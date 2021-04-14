---
description: O leitor de origem é uma alternativa ao uso da sessão de mídia e do Microsoft Media Foundation pipeline para processar dados de mídia.
ms.assetid: 8a17a754-53ef-4c05-9189-7978d864b17a
title: Leitor de origem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ba67b32fba7fcf899f339e9e2d0512d2574bad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502248"
---
# <a name="source-reader"></a><span data-ttu-id="ca180-103">Leitor de origem</span><span class="sxs-lookup"><span data-stu-id="ca180-103">Source Reader</span></span>

<span data-ttu-id="ca180-104">O leitor de origem é uma alternativa ao uso da [sessão de mídia](media-session.md) e do Microsoft Media Foundation pipeline para processar dados de mídia.</span><span class="sxs-lookup"><span data-stu-id="ca180-104">The Source Reader is an alternative to using the [Media Session](media-session.md) and the Microsoft Media Foundation pipeline to process media data.</span></span>

## <a name="why-use-the-source-reader"></a><span data-ttu-id="ca180-105">Por que usar o leitor de origem?</span><span class="sxs-lookup"><span data-stu-id="ca180-105">Why Use the Source Reader?</span></span>

<span data-ttu-id="ca180-106">Media Foundation fornece um pipeline otimizado para reprodução.</span><span class="sxs-lookup"><span data-stu-id="ca180-106">Media Foundation provides a pipeline that is optimized for playback.</span></span> <span data-ttu-id="ca180-107">O pipeline é de ponta a ponta, o que significa que ele lida com o fluxo de dados da fonte (como um arquivo de vídeo) até o destino (como a exibição de gráficos).</span><span class="sxs-lookup"><span data-stu-id="ca180-107">The pipeline is end-to-end, meaning it handles data flow from the source (such as a video file) all the way to the destination (such as the graphics display).</span></span> <span data-ttu-id="ca180-108">No entanto, se você quiser ler ou modificar os dados conforme eles passam pelo pipeline, deverá escrever um plug-in personalizado.</span><span class="sxs-lookup"><span data-stu-id="ca180-108">However, if you want to read or modify the data as it goes through the pipeline, you must write a custom plug-in.</span></span> <span data-ttu-id="ca180-109">Isso requer um conhecimento bastante profundo do pipeline de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="ca180-109">That requires a fairly deep knowledge of the Media Foundation pipeline.</span></span> <span data-ttu-id="ca180-110">Para determinadas tarefas, a criação de um novo plug-in é muita sobrecarga.</span><span class="sxs-lookup"><span data-stu-id="ca180-110">For certain tasks, creating a new plug-in is too much overhead.</span></span> <span data-ttu-id="ca180-111">O leitor de origem foi projetado para esse tipo de situação, quando você deseja obter os dados brutos de uma fonte sem a sobrecarga de todo o pipeline.</span><span class="sxs-lookup"><span data-stu-id="ca180-111">The source reader is designed for this type of situation, when you want to get the raw data from a source without the overhead of the entire pipeline.</span></span>

<span data-ttu-id="ca180-112">Internamente, o leitor de origem mantém um ponteiro para uma fonte de mídia.</span><span class="sxs-lookup"><span data-stu-id="ca180-112">Internally, the source reader holds a pointer to a media source.</span></span> <span data-ttu-id="ca180-113">Uma *origem de mídia* é um objeto Media Foundation que gera dados de mídia de uma fonte externa, como um arquivo de mídia ou dispositivo de captura de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ca180-113">A *media source* is a Media Foundation object that generates media data from an external source, such as a media file or video capture device.</span></span> <span data-ttu-id="ca180-114">O leitor de origem gerencia todas as chamadas de método para a origem de mídia.</span><span class="sxs-lookup"><span data-stu-id="ca180-114">The source reader manages all of the method calls to the media source.</span></span> <span data-ttu-id="ca180-115">(Para obter mais informações sobre fontes de mídia, consulte [fontes de mídia](media-sources.md).)</span><span class="sxs-lookup"><span data-stu-id="ca180-115">(For more information about media sources, see [Media Sources](media-sources.md).)</span></span>

<span data-ttu-id="ca180-116">Se a origem da mídia fornecer dados compactados, você poderá usar o leitor de origem para decodificar os dados.</span><span class="sxs-lookup"><span data-stu-id="ca180-116">If the media source delivers compressed data, you can use the source reader to decode the data.</span></span> <span data-ttu-id="ca180-117">Nesse caso, o leitor de origem carregará o decodificador correto e gerenciará o fluxo de dados entre a origem e o decodificador de mídia.</span><span class="sxs-lookup"><span data-stu-id="ca180-117">In that case, the source reader will load the correct decoder and manage the data flow between the media source and the decoder.</span></span> <span data-ttu-id="ca180-118">O leitor de origem também pode executar algum processamento de vídeo limitado: conversão de cores de YUV para RGB-32 e desentrelaçamento de software, embora essas operações não sejam recomendadas para renderização de vídeo em tempo real.</span><span class="sxs-lookup"><span data-stu-id="ca180-118">The source reader can also perform some limited video processing: color conversion from YUV to RGB-32, and software deinterlacing, although these operations are not recommended for real-time video rendering.</span></span> <span data-ttu-id="ca180-119">A imagem a seguir ilustra esse processo.</span><span class="sxs-lookup"><span data-stu-id="ca180-119">The following image illustrates this process.</span></span>

![diagrama do leitor de origem](images/sourcereader.png)

<span data-ttu-id="ca180-121">O leitor de origem não envia os dados para um destino; cabe ao aplicativo consumir os dados.</span><span class="sxs-lookup"><span data-stu-id="ca180-121">The source reader does not send the data to a destination; it is up to the application to consume the data.</span></span> <span data-ttu-id="ca180-122">Por exemplo, o leitor de origem pode ler um arquivo de vídeo, mas ele não renderizará o vídeo na tela.</span><span class="sxs-lookup"><span data-stu-id="ca180-122">For example, the source reader can read a video file, but it will not render the video to the screen.</span></span> <span data-ttu-id="ca180-123">Além disso, o leitor de origem não gerencia um relógio de apresentação, manipula problemas de tempo ou sincroniza vídeo com áudio.</span><span class="sxs-lookup"><span data-stu-id="ca180-123">Also, the source reader does not manage a presentation clock, handle timing issues, or synchronize video with audio.</span></span>

<span data-ttu-id="ca180-124">Considere usar o leitor de origem quando:</span><span class="sxs-lookup"><span data-stu-id="ca180-124">Consider using the source reader when:</span></span>

-   <span data-ttu-id="ca180-125">Você deseja obter dados de um arquivo de mídia sem se preocupar com a estrutura de arquivos subjacente.</span><span class="sxs-lookup"><span data-stu-id="ca180-125">You want to get data from a media file without worrying about the underlying file structure.</span></span>
-   <span data-ttu-id="ca180-126">Você deseja obter dados de um dispositivo de captura de áudio ou vídeo.</span><span class="sxs-lookup"><span data-stu-id="ca180-126">You want to get data from an audio or video capture device.</span></span>
-   <span data-ttu-id="ca180-127">Suas tarefas de processamento de dados não são sensíveis a tempo ou você não precisa de um relógio de apresentação.</span><span class="sxs-lookup"><span data-stu-id="ca180-127">Your data-processing tasks are not time sensitive, or you do not require a presentation clock.</span></span>
-   <span data-ttu-id="ca180-128">Você já tem um pipeline de mídia que não é baseado em Media Foundation e você deseja incorporar as fontes de mídia de Media Foundation em seu próprio pipeline.</span><span class="sxs-lookup"><span data-stu-id="ca180-128">You already have a media pipeline that is not based on Media Foundation, and you want to incorporate the Media Foundation media sources into your own pipeline.</span></span>

<span data-ttu-id="ca180-129">O leitor de origem não é recomendado nas seguintes situações:</span><span class="sxs-lookup"><span data-stu-id="ca180-129">The source reader is not recommended in the following situations:</span></span>

-   <span data-ttu-id="ca180-130">Para conteúdo protegido.</span><span class="sxs-lookup"><span data-stu-id="ca180-130">For protected content.</span></span> <span data-ttu-id="ca180-131">O leitor de origem não dá suporte ao DRM (gerenciamento de direitos digitais).</span><span class="sxs-lookup"><span data-stu-id="ca180-131">The source reader does not support digital rights management (DRM).</span></span>
-   <span data-ttu-id="ca180-132">Se você se preocupa com os detalhes da estrutura de arquivos subjacente.</span><span class="sxs-lookup"><span data-stu-id="ca180-132">If you care about the details of the underlying file structure.</span></span> <span data-ttu-id="ca180-133">O leitor de origem oculta esse tipo de detalhe.</span><span class="sxs-lookup"><span data-stu-id="ca180-133">The source reader hides that type of detail.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ca180-134">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="ca180-134">In this section</span></span>



| <span data-ttu-id="ca180-135">Tópico</span><span class="sxs-lookup"><span data-stu-id="ca180-135">Topic</span></span>                                                                                                        | <span data-ttu-id="ca180-136">Descrição</span><span class="sxs-lookup"><span data-stu-id="ca180-136">Description</span></span>                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ca180-137">Usando o leitor de origem para processar dados de mídia</span><span class="sxs-lookup"><span data-stu-id="ca180-137">Using the Source Reader to Process Media Data</span></span>](processing-media-data-with-the-source-reader.md)<br/> | <span data-ttu-id="ca180-138">Este tópico descreve como usar o leitor de origem para processar dados de mídia.</span><span class="sxs-lookup"><span data-stu-id="ca180-138">This topic describes how to use the Source Reader to process media data.</span></span><br/>                                               |
| [<span data-ttu-id="ca180-139">Usando o leitor de origem no modo assíncrono</span><span class="sxs-lookup"><span data-stu-id="ca180-139">Using the Source Reader in Asynchronous Mode</span></span>](using-the-source-reader-in-asynchronous-mode.md)<br/>  | <span data-ttu-id="ca180-140">Este tópico descreve como usar o leitor de origem no modo assíncrono.</span><span class="sxs-lookup"><span data-stu-id="ca180-140">This topic describes how to use the Source Reader in asynchronous mode.</span></span><br/>                                                |
| [<span data-ttu-id="ca180-141">Tutorial: decodificando áudio</span><span class="sxs-lookup"><span data-stu-id="ca180-141">Tutorial: Decoding Audio</span></span>](tutorial--decoding-audio.md)<br/>                                          | <span data-ttu-id="ca180-142">Este tutorial mostra como usar o leitor de origem para decodificar áudio de um arquivo de mídia e gravar o áudio em um arquivo WAVE.</span><span class="sxs-lookup"><span data-stu-id="ca180-142">This tutorial shows how to use the Source Reader to decode audio from a media file and write the audio to a WAVE file.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="ca180-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ca180-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca180-144">Arquitetura Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ca180-144">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> <dt>

[<span data-ttu-id="ca180-145">Guia de programação Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ca180-145">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> <dt>

[<span data-ttu-id="ca180-146">**IMFSourceReader**</span><span class="sxs-lookup"><span data-stu-id="ca180-146">**IMFSourceReader**</span></span>](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader)
</dt> </dl>

 

 




