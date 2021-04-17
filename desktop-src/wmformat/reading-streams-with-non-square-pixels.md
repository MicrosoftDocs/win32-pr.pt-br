---
title: Lendo fluxos com pixels não quadrados
description: Lendo fluxos com pixels não quadrados
ms.assetid: 32114c81-cb78-43de-9ea7-f210056f5aab
keywords:
- SDK do Windows Media Format, lendo fluxos de vídeo
- SDK do Windows Media Format, fluxos de vídeo
- SDK do Windows Media Format, pixels não quadrados
- SDK do Windows Media Format, pixels (não quadrado)
- ASF (Advanced Systems Format), lendo fluxos de vídeo
- ASF (formato de sistemas avançados), lendo fluxos de vídeo
- ASF (Advanced Systems Format), fluxos de vídeo
- ASF (formato de sistemas avançados), fluxos de vídeo
- ASF (Advanced Systems Format), pixels não quadrados
- ASF (formato de sistemas avançados), pixels não quadrados
- ASF (Advanced Systems Format), pixels (não quadrado)
- ASF (formato de sistemas avançados), pixels (não quadrado)
- lendo fluxos de vídeo
- fluxos de vídeo, lendo
- fluxos de vídeo, pixels não quadrados
- pixels não quadrados
- pixels (não quadrado)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecfc14019e9822aefedb7600adc4209317293b2f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105813676"
---
# <a name="reading-streams-with-non-square-pixels"></a><span data-ttu-id="4918a-120">Lendo fluxos com pixels não quadrados</span><span class="sxs-lookup"><span data-stu-id="4918a-120">Reading Streams with Non-Square Pixels</span></span>

<span data-ttu-id="4918a-121">Os aplicativos de leitor que precisam lidar corretamente com pixels não quadrados devem examinar os atributos de nível de fluxo no cabeçalho do ASF e as extensões de unidade de dados em cada exemplo.</span><span class="sxs-lookup"><span data-stu-id="4918a-121">Reader applications that need to correctly handle non-square pixels should examine both the stream-level attributes in the ASF header and the data unit extensions on each sample.</span></span> <span data-ttu-id="4918a-122">Há dois casos em que o retângulo de saída deve ser ajustado para compensar os pixels não quadrados.</span><span class="sxs-lookup"><span data-stu-id="4918a-122">There are two cases when the output rectangle must be adjusted to compensate for non-square pixels.</span></span>

<span data-ttu-id="4918a-123">Quando o conteúdo de origem tiver sido capturado de um dispositivo como uma câmera DV (Digital Video) com pixels não quadrados em seu CCD, um aplicativo leitor deverá ajustar seu retângulo de saída de vídeo para que a imagem seja exibida corretamente em um monitor de computador com pixels quadrados.</span><span class="sxs-lookup"><span data-stu-id="4918a-123">When the source content has been captured from a device such as a DV (digital video) camera with non-square pixels in its CCD, a reader application must adjust its video output rectangle so that the image displays correctly on a computer monitor with square pixels.</span></span>

<span data-ttu-id="4918a-124">Quando o aplicativo de leitor gera vídeo que será reproduzido em uma televisão NTSC, por exemplo, por meio de uma conexão de S-Video na placa de vídeo, você deve ajustar o retângulo de vídeo para que a imagem seja exibida corretamente nos pixels não quadrados da televisão.</span><span class="sxs-lookup"><span data-stu-id="4918a-124">When your reader application outputs video that will be played back on an NTSC television, for example through an S-Video out connection on the video card, you must adjust the video rectangle so that the image displays correctly on the television's non-square pixels.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4918a-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4918a-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4918a-126">**Para ler e gravar fluxos de vídeo com pixels não quadrados**</span><span class="sxs-lookup"><span data-stu-id="4918a-126">**To Read and Write Video Streams with Non-Square Pixels**</span></span>](to-read-and-write-video-streams-with-non-square-pixels.md)
</dt> </dl>

 

 




