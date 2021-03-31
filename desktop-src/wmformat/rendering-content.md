---
title: Renderizando conteúdo
description: Renderizando conteúdo
ms.assetid: 9a3baa33-dac4-4742-8f80-33b05caada09
keywords:
- SDK do Windows Media Format, Renderizando conteúdo
- Formato de sistema avançado (ASF), renderização de conteúdo
- ASF (formato de sistemas avançados), Renderizando conteúdo
- ASF (Advanced Systems Format), renderização de conteúdo
- ASF (formato de sistemas avançados), renderização de conteúdo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d6a171ce9b404c4cc16862ffd64b53ada5821b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822984"
---
# <a name="rendering-content"></a><span data-ttu-id="5160f-108">Renderizando conteúdo</span><span class="sxs-lookup"><span data-stu-id="5160f-108">Rendering Content</span></span>

<span data-ttu-id="5160f-109">O Windows Media Format SDK não fornece nenhuma rotina para renderizar o conteúdo fornecido pelo objeto Reader.</span><span class="sxs-lookup"><span data-stu-id="5160f-109">The Windows Media Format SDK does not provide any routines for rendering content delivered by the reader object.</span></span> <span data-ttu-id="5160f-110">Se você escrever aplicativos para reproduzir o conteúdo em arquivos ASF, deverá implementar suas próprias rotinas de renderização.</span><span class="sxs-lookup"><span data-stu-id="5160f-110">If you write applications to play back the content in ASF files, you must implement your own rendering routines.</span></span>

<span data-ttu-id="5160f-111">Você deve ter cuidado ao renderizar conteúdo para garantir que os exemplos sejam renderizados em ordem de tempo de apresentação e que os exemplos de fluxos diferentes sejam sincronizados durante a renderização.</span><span class="sxs-lookup"><span data-stu-id="5160f-111">You must be careful when rendering content to ensure that samples are rendered in order of presentation time and that samples from different streams are synchronized when rendering.</span></span> <span data-ttu-id="5160f-112">O método que você emprega para garantir a sincronização de fluxo dependerá da técnica de renderização usada para seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5160f-112">The method you employ to ensure stream synchronization will depend upon the rendering technique you use for your application.</span></span> <span data-ttu-id="5160f-113">Em geral, se você tiver fluxos de áudio e vídeo, deverá sincronizar com o fluxo de áudio, pois a inconsistência no fluxo de áudio é mais perceptível do que alguns quadros descartados em um fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="5160f-113">In general, if you have audio and video streams, you should synchronize to the audio stream, because inconsistency in the audio stream is more noticeable than a few dropped frames in a video stream.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5160f-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5160f-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5160f-115">**Lendo arquivos ASF**</span><span class="sxs-lookup"><span data-stu-id="5160f-115">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> <dt>

[<span data-ttu-id="5160f-116">**Para recuperar amostras de mídia com o leitor assíncrono**</span><span class="sxs-lookup"><span data-stu-id="5160f-116">**To Retrieve Media Samples with the Asynchronous Reader**</span></span>](to-retrieve-media-samples-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="5160f-117">**Para recuperar amostras de mídia com o leitor síncrono**</span><span class="sxs-lookup"><span data-stu-id="5160f-117">**To Retrieve Media Samples with the Synchronous Reader**</span></span>](to-retrieve-media-samples-with-the-synchronous-reader.md)
</dt> </dl>

 

 




