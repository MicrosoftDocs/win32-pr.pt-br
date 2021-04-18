---
title: Sobre o plug-in de DSP de vídeo de exemplo
description: Sobre o plug-in de DSP de vídeo de exemplo
ms.assetid: f2ba8e9d-a0e4-4679-99dc-2bfe9e451ffd
keywords:
- Plug-ins do Windows Media Player, exemplos
- plug-ins, amostras
- plug-ins de processamento de sinal digital, amostras
- Plug-ins do DSP, amostras
- Plug-ins do Windows Media Player, DSP de vídeo
- plug-ins, DSP de vídeo
- plug-ins de processamento de sinal digital, amostras de vídeo
- Plug-ins do DSP, amostras de vídeo
- exemplos, plug-ins do DSP
- plug-ins de DSP de vídeo, amostras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ede2eda82c834cefad0e31009805f24941cd4a6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105781288"
---
# <a name="about-the-sample-video-dsp-plug-in"></a><span data-ttu-id="bfc3f-113">Sobre o plug-in de DSP de vídeo de exemplo</span><span class="sxs-lookup"><span data-stu-id="bfc3f-113">About the Sample Video DSP Plug-in</span></span>

<span data-ttu-id="bfc3f-114">O plug-in de DSP de vídeo de exemplo fornece uma implementação de processamento simples que dimensiona a saturação de cor do vídeo por um fator fornecido pelo usuário na página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="bfc3f-114">The sample video DSP plug-in provides a simple processing implementation that scales the color saturation of the video by a factor provided by the user in the property page.</span></span> <span data-ttu-id="bfc3f-115">O plug-in aceita valores entre zero e 1.</span><span class="sxs-lookup"><span data-stu-id="bfc3f-115">The plug-in accepts values between zero and 1.</span></span> <span data-ttu-id="bfc3f-116">O valor padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="bfc3f-116">The default value is 1.</span></span> <span data-ttu-id="bfc3f-117">Um valor de 1 não tem efeito sobre a imagem de vídeo; outros fatores de escala dessaturam a cor da imagem.</span><span class="sxs-lookup"><span data-stu-id="bfc3f-117">A value of 1 has no effect upon the video image; other scale factors desaturate the image color.</span></span> <span data-ttu-id="bfc3f-118">Por exemplo, um valor de 0,5 resultaria em uma saturação de cor de 50%.</span><span class="sxs-lookup"><span data-stu-id="bfc3f-118">For instance, a value of .5 would result in 50 percent color saturation.</span></span> <span data-ttu-id="bfc3f-119">Um valor de zero resulta em vídeo em escala de cinza.</span><span class="sxs-lookup"><span data-stu-id="bfc3f-119">A value of zero results in grayscale video.</span></span>

<span data-ttu-id="bfc3f-120">O plug-in DSP de vídeo de exemplo funciona com os seguintes formatos de vídeo:</span><span class="sxs-lookup"><span data-stu-id="bfc3f-120">The sample video DSP plug-in works with the following video formats:</span></span>

-   <span data-ttu-id="bfc3f-121">NV12</span><span class="sxs-lookup"><span data-stu-id="bfc3f-121">NV12</span></span>
-   <span data-ttu-id="bfc3f-122">YV12</span><span class="sxs-lookup"><span data-stu-id="bfc3f-122">YV12</span></span>
-   <span data-ttu-id="bfc3f-123">YUY2</span><span class="sxs-lookup"><span data-stu-id="bfc3f-123">YUY2</span></span>
-   <span data-ttu-id="bfc3f-124">UYVY</span><span class="sxs-lookup"><span data-stu-id="bfc3f-124">UYVY</span></span>
-   <span data-ttu-id="bfc3f-125">RGB32</span><span class="sxs-lookup"><span data-stu-id="bfc3f-125">RGB32</span></span>
-   <span data-ttu-id="bfc3f-126">RGB24</span><span class="sxs-lookup"><span data-stu-id="bfc3f-126">RGB24</span></span>
-   <span data-ttu-id="bfc3f-127">RGB555</span><span class="sxs-lookup"><span data-stu-id="bfc3f-127">RGB555</span></span>
-   <span data-ttu-id="bfc3f-128">RGB565</span><span class="sxs-lookup"><span data-stu-id="bfc3f-128">RGB565</span></span>

## <a name="related-topics"></a><span data-ttu-id="bfc3f-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bfc3f-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bfc3f-130">**Criando um plug-in do DSP**</span><span class="sxs-lookup"><span data-stu-id="bfc3f-130">**Building a DSP Plug-in**</span></span>](building-a-dsp-plug-in.md)
</dt> </dl>

 

 




