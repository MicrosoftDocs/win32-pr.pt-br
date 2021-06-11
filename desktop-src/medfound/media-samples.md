---
description: Saiba mais sobre exemplos de mídia no Microsoft Media Foundation. Um exemplo de mídia é um objeto que contém uma lista ordenada de zero ou mais buffers.
ms.assetid: 14389eea-8091-4c10-849e-53db3e98a7c8
title: Amostras de mídia (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef5d29b11fb6db316e3fbf6e33e24218ddbbf062
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989151"
---
# <a name="media-samples-microsoft-media-foundation"></a><span data-ttu-id="08e8d-104">Amostras de mídia (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="08e8d-104">Media Samples (Microsoft Media Foundation)</span></span>

<span data-ttu-id="08e8d-105">Um exemplo de mídia é um objeto que contém uma lista ordenada de zero ou mais buffers.</span><span class="sxs-lookup"><span data-stu-id="08e8d-105">A media sample is an object that contains an ordered list of zero or more buffers.</span></span> <span data-ttu-id="08e8d-106">Amostras de mídia expõem a interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) .</span><span class="sxs-lookup"><span data-stu-id="08e8d-106">Media samples expose the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface.</span></span> <span data-ttu-id="08e8d-107">A quantidade de dados contida em um exemplo depende do componente que cria o exemplo e do tipo de dados nos buffers.</span><span class="sxs-lookup"><span data-stu-id="08e8d-107">The amount of data contained in one sample depends on the component that creates the sample and on the type of data in the buffers.</span></span> <span data-ttu-id="08e8d-108">Para vídeo descompactado, um exemplo geralmente mantém um único quadro de vídeo.</span><span class="sxs-lookup"><span data-stu-id="08e8d-108">For uncompressed video, a sample usually holds a single video frame.</span></span> <span data-ttu-id="08e8d-109">Para áudio descompactado, a quantidade de dados pode variar, mas geralmente um quadro de áudio não abrange dois exemplos.</span><span class="sxs-lookup"><span data-stu-id="08e8d-109">For uncompressed audio, the amount of data can vary, but usually an audio frame does not span two samples.</span></span> <span data-ttu-id="08e8d-110">Para dados compactados, essas diretrizes podem não se aplicar.</span><span class="sxs-lookup"><span data-stu-id="08e8d-110">For compressed data, these guidelines might not apply.</span></span>

<span data-ttu-id="08e8d-111">Um único exemplo pode conter vários buffers por motivos de eficiência.</span><span class="sxs-lookup"><span data-stu-id="08e8d-111">A single sample might contain multiple buffers for reasons of efficiency.</span></span> <span data-ttu-id="08e8d-112">Por exemplo, em um arquivo ASF, um quadro de vídeo geralmente é distribuído entre vários pacotes ASF.</span><span class="sxs-lookup"><span data-stu-id="08e8d-112">For example, in an ASF file, a video frame is often spread out among multiple ASF packets.</span></span> <span data-ttu-id="08e8d-113">A origem da mídia pode ler os pacotes em vários buffers.</span><span class="sxs-lookup"><span data-stu-id="08e8d-113">The media source might read the packets into multiple buffers.</span></span> <span data-ttu-id="08e8d-114">Em vez de copiar cada fragmento em um buffer, a origem simplesmente coloca todos os buffers em uma amostra.</span><span class="sxs-lookup"><span data-stu-id="08e8d-114">Instead of copying each fragment into one buffer, the source simply puts all of the buffers into one sample.</span></span> <span data-ttu-id="08e8d-115">Os componentes downstream podem decidir se os buffers menores devem ser copiados em um buffer contíguo.</span><span class="sxs-lookup"><span data-stu-id="08e8d-115">Downstream components can then decide whether to copy the smaller buffers into one contiguous buffer.</span></span> <span data-ttu-id="08e8d-116">Em geral, se você estiver escrevendo um componente de pipeline, deverá assumir que qualquer exemplo pode conter mais de um buffer.</span><span class="sxs-lookup"><span data-stu-id="08e8d-116">Generally, if you are writing a pipeline component, you should assume that any sample might contain more than one buffer.</span></span>

<span data-ttu-id="08e8d-117">Esta seção contém os seguintes tópicos.</span><span class="sxs-lookup"><span data-stu-id="08e8d-117">This section contains the following topics.</span></span>



| <span data-ttu-id="08e8d-118">Tópico</span><span class="sxs-lookup"><span data-stu-id="08e8d-118">Topic</span></span>                                                        | <span data-ttu-id="08e8d-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="08e8d-119">Description</span></span>                                                                                                              |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="08e8d-120">Trabalhando com exemplos de mídia</span><span class="sxs-lookup"><span data-stu-id="08e8d-120">Working with Media Samples</span></span>](working-with-media-samples.md) | <span data-ttu-id="08e8d-121">Descreve o comportamento geral de amostras de mídia.</span><span class="sxs-lookup"><span data-stu-id="08e8d-121">Describes the general behavior of media samples.</span></span>                                                                         |
| [<span data-ttu-id="08e8d-122">Exemplos de vídeo</span><span class="sxs-lookup"><span data-stu-id="08e8d-122">Video Samples</span></span>](video-samples.md)                           | <span data-ttu-id="08e8d-123">Descreve uma implementação especializada do [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) projetado para conter quadros de vídeo descompactados.</span><span class="sxs-lookup"><span data-stu-id="08e8d-123">Describes a specialized implementation of [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) designed for holding uncompressed video frames.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="08e8d-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="08e8d-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08e8d-125">Buffers de mídia</span><span class="sxs-lookup"><span data-stu-id="08e8d-125">Media Buffers</span></span>](media-buffers.md)
</dt> <dt>

[<span data-ttu-id="08e8d-126">Primitivos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="08e8d-126">Media Foundation Primitives</span></span>](media-foundation-primitives.md)
</dt> </dl>

 

 



