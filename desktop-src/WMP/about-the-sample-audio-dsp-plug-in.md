---
title: Sobre o plug-in de DSP de áudio de exemplo
description: Sobre o plug-in de DSP de áudio de exemplo
ms.assetid: e60b055b-77e6-470e-91f6-9882827cf238
keywords:
- Plug-ins do Windows Media Player, exemplos
- plug-ins, amostras
- plug-ins de processamento de sinal digital, amostras
- Plug-ins do DSP, amostras
- Plug-ins do Windows Media Player, DSP de áudio
- plug-ins, DSP de áudio
- plug-ins de processamento de sinal digital, amostras de áudio
- Plug-ins do DSP, amostras de áudio
- exemplos, plug-ins do DSP
- plug-ins do DSP de áudio, amostras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0edc3a5860c0c52837bfece16d2e709bf16d836d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292217"
---
# <a name="about-the-sample-audio-dsp-plug-in"></a><span data-ttu-id="ac641-113">Sobre o plug-in de DSP de áudio de exemplo</span><span class="sxs-lookup"><span data-stu-id="ac641-113">About the Sample Audio DSP Plug-in</span></span>

<span data-ttu-id="ac641-114">O plug-in DSP de áudio de exemplo fornece uma implementação de processamento simples que dimensiona a amplitude do áudio por um fator fornecido pelo usuário na página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="ac641-114">The sample audio DSP plug-in provides a simple processing implementation that scales the amplitude of the audio by a factor provided by the user in the property page.</span></span> <span data-ttu-id="ac641-115">O plug-in aceita valores entre zero e 1.</span><span class="sxs-lookup"><span data-stu-id="ac641-115">The plug-in accepts values between zero and 1.</span></span> <span data-ttu-id="ac641-116">O valor padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="ac641-116">The default value is 1.</span></span> <span data-ttu-id="ac641-117">Um valor de 1 não tem nenhum efeito sobre o som; outros fatores de escala são multiplicadores para os exemplos de áudio.</span><span class="sxs-lookup"><span data-stu-id="ac641-117">A value of 1 has no effect upon the sound; other scale factors are multipliers for the audio samples.</span></span> <span data-ttu-id="ac641-118">Por exemplo, um valor de 0,5 resultaria em uma diminuição de 6 decibéis no volume.</span><span class="sxs-lookup"><span data-stu-id="ac641-118">For instance, a value of .5 would result in a 6 decibel decrease in volume.</span></span> <span data-ttu-id="ac641-119">Um valor de zero resulta em silêncio.</span><span class="sxs-lookup"><span data-stu-id="ac641-119">A value of zero results in silence.</span></span>

<span data-ttu-id="ac641-120">O plug-in DSP de áudio de exemplo funciona com áudio PCM estéreo ou mono.</span><span class="sxs-lookup"><span data-stu-id="ac641-120">The sample audio DSP plug-in works with stereo or mono PCM audio.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ac641-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ac641-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac641-122">**Criando um plug-in do DSP**</span><span class="sxs-lookup"><span data-stu-id="ac641-122">**Building a DSP Plug-in**</span></span>](building-a-dsp-plug-in.md)
</dt> </dl>

 

 




