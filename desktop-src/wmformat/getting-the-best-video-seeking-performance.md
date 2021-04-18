---
title: Obtendo o melhor desempenho de busca de vídeo
description: Obtendo o melhor desempenho de busca de vídeo
ms.assetid: 21269f0c-fc3a-46fc-88b4-f71828b5d5a7
keywords:
- SDK do Windows Media Format, melhor desempenho de busca em vídeo
- ASF (Advanced Systems Format), melhor desempenho de busca de vídeo
- ASF (formato de sistemas avançados), melhor desempenho de busca de vídeo
- ASF (Advanced Systems Format), desempenho de busca em vídeo
- ASF (formato de sistemas avançados), desempenho de busca em vídeo
- ASF (Advanced Systems Format), desempenho
- ASF (formato de sistemas avançados), desempenho
- busca de vídeo
- desempenho, busca de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c95feb9158bbab09ce28024100f3ebbffb56ad9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105811528"
---
# <a name="getting-the-best-video-seeking-performance"></a><span data-ttu-id="3882d-112">Obtendo o melhor desempenho de busca de vídeo</span><span class="sxs-lookup"><span data-stu-id="3882d-112">Getting the Best Video Seeking Performance</span></span>

<span data-ttu-id="3882d-113">Procurar conteúdo em um arquivo é uma operação muito comum que é potencialmente um problema de desempenho.</span><span class="sxs-lookup"><span data-stu-id="3882d-113">Seeking to content in a file is a very common operation that is potentially a performance issue.</span></span> <span data-ttu-id="3882d-114">O vídeo codificado com o codec do Windows Media Video 9 é constituído principalmente por quadros Delta, que registram apenas as alterações em relação ao quadro anterior.</span><span class="sxs-lookup"><span data-stu-id="3882d-114">Video encoded with the Windows Media Video 9 codec is made up primarily of delta frames, which only record the changes in relation to the previous frame.</span></span> <span data-ttu-id="3882d-115">A reconstrução de quadros Delta leva tempo, especialmente se os quadros-chave estiverem muito distantes.</span><span class="sxs-lookup"><span data-stu-id="3882d-115">Reconstructing delta frames takes time, particularly if the key frames are far apart.</span></span> <span data-ttu-id="3882d-116">Para obter mais informações sobre como configurar quadros-chave para busca eficiente, consulte [Configurando fluxos de vídeo para](configuring-video-streams-for-seeking-performance.md)procurar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="3882d-116">For more information about configuring key frames for efficient seeking, see [Configuring Video Streams for Seeking Performance](configuring-video-streams-for-seeking-performance.md).</span></span>

<span data-ttu-id="3882d-117">Além da configuração adequada, você pode melhorar o desempenho de busca usando a indexação de quadros para o fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="3882d-117">In addition to proper configuration, you can improve seeking performance by using frame indexing for the video stream.</span></span> <span data-ttu-id="3882d-118">A busca por um número de quadro é normalmente mais rápida do que a busca de um horário de apresentação.</span><span class="sxs-lookup"><span data-stu-id="3882d-118">Seeking to a frame number is typically faster than seeking to a presentation time.</span></span>

<span data-ttu-id="3882d-119">Se estiver procurando em um arquivo com vários fluxos, você deverá selecionar apenas os fluxos necessários.</span><span class="sxs-lookup"><span data-stu-id="3882d-119">If seeking in a file with multiple streams, you should select only the streams that are needed.</span></span> <span data-ttu-id="3882d-120">Cada fluxo configurado para leitura afetará o desempenho da busca, porque todos os fluxos selecionados são sincronizados quando você busca um ponto em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="3882d-120">Each stream configured for reading will affect the performance of seeking, because all selected streams are synchronized when you seek to a point in a file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3882d-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3882d-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3882d-122">**Lendo arquivos ASF**</span><span class="sxs-lookup"><span data-stu-id="3882d-122">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> <dt>

[<span data-ttu-id="3882d-123">**Para buscar por número de quadro usando o leitor assíncrono**</span><span class="sxs-lookup"><span data-stu-id="3882d-123">**To Seek By Frame Number Using the Asynchronous Reader**</span></span>](to-seek-by-frame-number-using-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="3882d-124">**Para buscar por número de quadro usando o leitor síncrono**</span><span class="sxs-lookup"><span data-stu-id="3882d-124">**To Seek By Frame Number Using the Synchronous Reader**</span></span>](to-seek-by-frame-number-using-the-synchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="3882d-125">**Para procurar por tempo usando o leitor assíncrono**</span><span class="sxs-lookup"><span data-stu-id="3882d-125">**To Seek By Time Using the Asynchronous Reader**</span></span>](to-seek-by-time-using-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="3882d-126">**Para buscar por tempo usando o leitor síncrono**</span><span class="sxs-lookup"><span data-stu-id="3882d-126">**To Seek By Time Using the Synchronous Reader**</span></span>](to-seek-by-time-using-the-synchronous-reader.md)
</dt> </dl>

 

 




