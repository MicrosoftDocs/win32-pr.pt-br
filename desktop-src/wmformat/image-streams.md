---
title: Fluxos de imagem
description: Fluxos de imagem
ms.assetid: 17a945aa-463a-4aac-82cc-68b49c720c0a
keywords:
- SDK do Windows Media Format, fluxos de imagem
- ASF (Advanced Systems Format), fluxos de imagem
- ASF (formato de sistemas avançados), fluxos de imagem
- SDK do Windows Media Format, fluxos
- ASF (Advanced Systems Format), fluxos
- ASF (formato de sistemas avançados), fluxos
- fluxos de imagem, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 280d029715a3c722d05ee335a3a88ae4632cabbb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292591"
---
# <a name="image-streams"></a><span data-ttu-id="abf50-110">Fluxos de imagem</span><span class="sxs-lookup"><span data-stu-id="abf50-110">Image Streams</span></span>

<span data-ttu-id="abf50-111">Um fluxo de imagem é um tipo especial de fluxo que contém imagens ainda atribuídas a tempos de apresentação.</span><span class="sxs-lookup"><span data-stu-id="abf50-111">An image stream is a special type of stream that contains still images assigned to presentation times.</span></span> <span data-ttu-id="abf50-112">Um aplicativo pode exibir as imagens em um fluxo de imagem conforme desejado, mas a implementação típica é exibir cada imagem até que a próxima imagem seja entregue, como uma apresentação de slides.</span><span class="sxs-lookup"><span data-stu-id="abf50-112">An application can display the pictures in an image stream as desired, but the typical implementation is to display each picture until the next picture is delivered, like a slide show.</span></span> <span data-ttu-id="abf50-113">Normalmente, um fluxo de imagem é codificado em um arquivo com um fluxo de áudio para produzir uma apresentação simples de imagens sincronizadas com música ou fala.</span><span class="sxs-lookup"><span data-stu-id="abf50-113">Usually, an image stream is encoded in a file with an audio stream to produce a simple presentation of images synchronized with music or speech.</span></span>

<span data-ttu-id="abf50-114">Os fluxos de imagem são como fluxos de vídeo, pois são criados a partir de exemplos descompactados que são compactados como parte do processo de gravação de arquivo, mas também são como fluxos arbitrários, pois você deve atribuir uma taxa de bits e uma janela de buffer apropriada ao conteúdo sem depender de propriedades atribuídas ao codec.</span><span class="sxs-lookup"><span data-stu-id="abf50-114">Image streams are like video streams in that they are created from uncompressed samples that are compressed as part of the file writing process, but they are also like arbitrary streams because you must assign a bit rate and buffer window appropriate to the content without relying on codec-assigned properties.</span></span>

## <a name="related-topics"></a><span data-ttu-id="abf50-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="abf50-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="abf50-116">**Fluxos arbitrários**</span><span class="sxs-lookup"><span data-stu-id="abf50-116">**Arbitrary Streams**</span></span>](arbitrary-streams.md)
</dt> <dt>

[<span data-ttu-id="abf50-117">**Recursos de arquivo ASF**</span><span class="sxs-lookup"><span data-stu-id="abf50-117">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="abf50-118">**Fluxos de áudio e vídeo**</span><span class="sxs-lookup"><span data-stu-id="abf50-118">**Audio and Video Streams**</span></span>](audio-and-video-streams.md)
</dt> <dt>

[<span data-ttu-id="abf50-119">**Gravando fluxos de imagem**</span><span class="sxs-lookup"><span data-stu-id="abf50-119">**Writing Image Streams**</span></span>](writing-image-streams.md)
</dt> </dl>

 

 




