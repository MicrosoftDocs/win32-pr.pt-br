---
description: No modelo de pipeline do Media Foundations, uma fonte de mídia é conectada a uma transformação que é ainda mais conectada a um coletor de mídia.
ms.assetid: 55ab3a53-d9fd-438c-998c-8888f99958ce
title: Componentes ASF da camada de pipeline
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b3b6eb2d00404d193e50cebf174210a1c25655e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105808214"
---
# <a name="pipeline-layer-asf-components"></a><span data-ttu-id="955ff-103">Componentes ASF da camada de pipeline</span><span class="sxs-lookup"><span data-stu-id="955ff-103">Pipeline Layer ASF Components</span></span>

<span data-ttu-id="955ff-104">No modelo de pipeline do Media Foundation, uma fonte de mídia é conectada a uma transformação que está mais conectada a um coletor de mídia.</span><span class="sxs-lookup"><span data-stu-id="955ff-104">In Media Foundation's pipeline model, a media source is connected to a transform which is further connected to a media sink.</span></span> <span data-ttu-id="955ff-105">Os dados contidos na origem fluem pela transformação e gera amostras de mídia de saída no coletor para fins de reprodução ou codificação.</span><span class="sxs-lookup"><span data-stu-id="955ff-105">The data contained in the source flows through the transform and generates output media samples in the sink for the purpose of playback or encoding.</span></span> <span data-ttu-id="955ff-106">Dependendo se o aplicativo deseja reproduzir o conteúdo ASF ou codificar em um arquivo ASF, o aplicativo deve criar o pipeline de forma diferente.</span><span class="sxs-lookup"><span data-stu-id="955ff-106">Depending on whether the application wants to playback ASF content or encode to an ASF file, the application must build the pipeline differently.</span></span>

<span data-ttu-id="955ff-107">Os tópicos a seguir contêm informações sobre os componentes da camada de pipeline.</span><span class="sxs-lookup"><span data-stu-id="955ff-107">The following topics contain information about the pipeline layer components.</span></span>

-   [<span data-ttu-id="955ff-108">Fonte de mídia ASF</span><span class="sxs-lookup"><span data-stu-id="955ff-108">ASF Media Source</span></span>](asf-media-source.md)
-   [<span data-ttu-id="955ff-109">Codificadores de mídia do Windows</span><span class="sxs-lookup"><span data-stu-id="955ff-109">Windows Media Encoders</span></span>](windows-media-encoders.md)
-   [<span data-ttu-id="955ff-110">Coletores de mídia ASF</span><span class="sxs-lookup"><span data-stu-id="955ff-110">ASF Media Sinks</span></span>](asf-media-sinks.md)

<span data-ttu-id="955ff-111">Os três componentes principais de um pipeline ASF para reprodução são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="955ff-111">The three main components of an ASF pipeline for playback are as follows:</span></span>

-   <span data-ttu-id="955ff-112">A fonte de mídia ASF é fornecida por Media Foundation que representa um arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="955ff-112">ASF media source is provided by Media Foundation that represents an ASF file.</span></span>
-   <span data-ttu-id="955ff-113">Reamostragens de áudio, redimensionadores de imagem de vídeo, etc., (transformação)</span><span class="sxs-lookup"><span data-stu-id="955ff-113">Audio resamplers, video image resizers, etc., (transform)</span></span>
-   <span data-ttu-id="955ff-114">Renderizador de áudio e vídeo (coletores)</span><span class="sxs-lookup"><span data-stu-id="955ff-114">Audio and Video renderer (sinks)</span></span>

<span data-ttu-id="955ff-115">Para obter informações sobre como criar um pipeline de reprodução, consulte [criando topologias de reprodução](creating-playback-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="955ff-115">For information about building a playback pipeline, see [Creating Playback Topologies](creating-playback-topologies.md).</span></span>

<span data-ttu-id="955ff-116">Os três componentes principais de um pipeline ASF para codificação são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="955ff-116">The three main components of an ASF pipeline for encoding are as follows:</span></span>

-   <span data-ttu-id="955ff-117">Fonte de mídia que representa os dados em um formato que precisa ser convertido.</span><span class="sxs-lookup"><span data-stu-id="955ff-117">Media source representing the data in a format that needs to be converted.</span></span> <span data-ttu-id="955ff-118">Esse componente pode ser uma das fontes de mídia padrão fornecidas pelo Media Foundation ou uma fonte personalizada que expõe a interface [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) .</span><span class="sxs-lookup"><span data-stu-id="955ff-118">This component can be one of the default media sources provided by Media Foundation or a custom source that exposes the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface.</span></span>
-   <span data-ttu-id="955ff-119">Codificadores de mídia do Windows (transformação) que executam a conversão de formato.</span><span class="sxs-lookup"><span data-stu-id="955ff-119">Windows Media encoders (transform) that perform the format conversion.</span></span>
-   <span data-ttu-id="955ff-120">Coletores de mídia ASF fornecidos por Media Foundation que gravam objetos ASF e amostras de mídia em um arquivo de saída especificado pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="955ff-120">ASF media sinks provided by Media Foundation that write ASF objects and media samples in an output file specified by the application.</span></span>

<span data-ttu-id="955ff-121">O pipeline é representado em uma topologia e cada objeto no pipeline é representado por um nó de topologia.</span><span class="sxs-lookup"><span data-stu-id="955ff-121">The pipeline is represented in a topology and each object in the pipeline is represented by a topology node.</span></span> <span data-ttu-id="955ff-122">Para reprodução e codificação, todas as operações de pipeline são tratadas pela sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="955ff-122">Both for playback and encoding, all of the pipeline operations are handled by the Media Session.</span></span> <span data-ttu-id="955ff-123">Uma das responsabilidades da sessão de mídia é garantir que o pipeline tenha todos os componentes necessários para gerar a saída.</span><span class="sxs-lookup"><span data-stu-id="955ff-123">One of responsibilities of the Media Session is to make sure that the pipeline has all the components required to generate output.</span></span> <span data-ttu-id="955ff-124">Por exemplo, em um pipeline de codificação, se o formato de fonte de áudio for diferente do formato de destino, a sessão de mídia inserirá componentes de transformação adicionais, como o reamostrador que executa conversões de taxa de amostra apropriadas.</span><span class="sxs-lookup"><span data-stu-id="955ff-124">For example, in an encoding pipeline, if the audio source format is different than the target format, the Media Session inserts additional transform components such as the resampler that performs appropriate sample rate conversions.</span></span> <span data-ttu-id="955ff-125">O controle de fluxo de dados por meio do pipeline também é gerenciado pela sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="955ff-125">The data flow control through the pipeline is also managed by the Media Session.</span></span> <span data-ttu-id="955ff-126">Em um cenário de reprodução, iniciar a sessão de mídia a sessão de mídia envia amostras para SAR e EVR, que as renderiza no dispositivo de saída.</span><span class="sxs-lookup"><span data-stu-id="955ff-126">In a playback scenario, starting the Media Session the Media Session sends samples to SAR and EVR, which renders them on the output device.</span></span> <span data-ttu-id="955ff-127">Para codificação, iniciar a sessão de mídia inicia o processo de codificação.</span><span class="sxs-lookup"><span data-stu-id="955ff-127">For encoding, starting the Media Session begins the encoding process.</span></span> <span data-ttu-id="955ff-128">A sessão notifica de forma assíncrona o aplicativo quando a codificação é concluída.</span><span class="sxs-lookup"><span data-stu-id="955ff-128">The session asynchronously notifies the application when the encoding is complete.</span></span>

<span data-ttu-id="955ff-129">O tópico a seguir contém instruções passo a passo sobre como usar os componentes da camada de pipeline para criar uma topologia de codificação.</span><span class="sxs-lookup"><span data-stu-id="955ff-129">The following topic contains step-by-step instructions about using the pipeline layer components to build an encoding topology.</span></span> <span data-ttu-id="955ff-130">componentes para leitura e gravação de arquivos ASF.</span><span class="sxs-lookup"><span data-stu-id="955ff-130">components for reading and writing ASF files.</span></span>

-   [<span data-ttu-id="955ff-131">Tutorial: 1-transmitir codificação de mídia do Windows</span><span class="sxs-lookup"><span data-stu-id="955ff-131">Tutorial: 1-Pass Windows Media Encoding</span></span>](tutorial--1-pass-windows-media-encoding.md)

## <a name="related-topics"></a><span data-ttu-id="955ff-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="955ff-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="955ff-133">Suporte a ASF no Media Foundation</span><span class="sxs-lookup"><span data-stu-id="955ff-133">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



