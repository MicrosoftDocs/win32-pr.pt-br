---
title: Para ler e gravar fluxos de vídeo com pixels não quadrados
description: Para ler e gravar fluxos de vídeo com pixels não quadrados
ms.assetid: fe66d13e-61cf-4bb6-9ca2-aafeabe320ec
keywords:
- SDK do Windows Media Format, lendo fluxos de vídeo
- Windows Media Format SDK, gravando fluxos de vídeo
- SDK do Windows Media Format, fluxos de vídeo
- SDK do Windows Media Format, pixels não quadrados
- SDK do Windows Media Format, pixels (não quadrado)
- ASF (Advanced Systems Format), lendo fluxos de vídeo
- ASF (formato de sistemas avançados), lendo fluxos de vídeo
- ASF (Advanced Systems Format), gravando fluxos de vídeo
- ASF (formato de sistemas avançados), gravando fluxos de vídeo
- ASF (Advanced Systems Format), fluxos de vídeo
- ASF (formato de sistemas avançados), fluxos de vídeo
- ASF (Advanced Systems Format), pixels não quadrados
- ASF (formato de sistemas avançados), pixels não quadrados
- ASF (Advanced Systems Format), pixels (não quadrado)
- ASF (formato de sistemas avançados), pixels (não quadrado)
- lendo fluxos de vídeo
- gravando fluxos de vídeo
- fluxos de vídeo, lendo
- fluxos de vídeo, gravando
- fluxos de vídeo, pixels não quadrados
- pixels não quadrados
- pixels (não quadrado)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dd6b3e3ba67ba42dfc144e7f95ddd042dea0f84
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292132"
---
# <a name="to-read-and-write-video-streams-with-non-square-pixels"></a><span data-ttu-id="c9d54-125">Para ler e gravar fluxos de vídeo com pixels não quadrados</span><span class="sxs-lookup"><span data-stu-id="c9d54-125">To Read and Write Video Streams with Non-Square Pixels</span></span>

<span data-ttu-id="c9d54-126">Os monitores de computador têm pixels quadrados, mas outros tipos de telas de vídeo, incluindo televisões NTSC, têm pixels retangulares ou não quadrados.</span><span class="sxs-lookup"><span data-stu-id="c9d54-126">Computer monitors have square pixels, but other types of video screens, including NTSC televisions, have rectangular or non-square pixels.</span></span> <span data-ttu-id="c9d54-127">Além disso, alguns dispositivos de entrada, como câmeras de vídeo digital (DV), têm cobrado dois dispositivos com pixels não quadrados.</span><span class="sxs-lookup"><span data-stu-id="c9d54-127">Also, some input devices, such as Digital Video (DV) cameras, have charged couple devices with non-square pixels.</span></span> <span data-ttu-id="c9d54-128">Quando você está gravando arquivos que são baseados em dados de origem de pixel não quadrado ou que são destinados para exibição em dispositivos com pixels não quadrados, as informações de taxa de proporção de pixel devem ser incluídas no arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="c9d54-128">When you are writing files that are either based on non-square pixel source data or else intended for display on devices with non-square pixels, the pixel aspect ratio information must be included in the ASF file.</span></span> <span data-ttu-id="c9d54-129">Os aplicativos de leitor devem examinar essas informações e usá-las para ajustar a taxa de proporção do retângulo de vídeo conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="c9d54-129">Reader applications must examine that information and use it to adjust the aspect ratio of the video rectangle as necessary.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c9d54-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c9d54-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9d54-131">**Tópicos avançados**</span><span class="sxs-lookup"><span data-stu-id="c9d54-131">**Advanced Topics**</span></span>](advanced-topics.md)
</dt> <dt>

[<span data-ttu-id="c9d54-132">**Lendo fluxos com pixels não quadrados**</span><span class="sxs-lookup"><span data-stu-id="c9d54-132">**Reading Streams with Non-Square Pixels**</span></span>](reading-streams-with-non-square-pixels.md)
</dt> <dt>

[<span data-ttu-id="c9d54-133">**Gravando fluxos com pixels não quadrados**</span><span class="sxs-lookup"><span data-stu-id="c9d54-133">**Writing Streams with Non-Square Pixels**</span></span>](writing-streams-with-non-square-pixels.md)
</dt> </dl>

 

 




