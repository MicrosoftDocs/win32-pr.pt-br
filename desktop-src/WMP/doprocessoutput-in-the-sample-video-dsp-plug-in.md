---
title: DoProcessOutput no plug-in de DSP de vídeo de exemplo
description: DoProcessOutput no plug-in de DSP de vídeo de exemplo
ms.assetid: 67536e35-a049-49c8-bd89-fad1fab37e6c
keywords:
- Plug-ins do Windows Media Player, DSP de vídeo
- plug-ins, DSP de vídeo
- plug-ins de processamento de sinal digital, DoProcessOutput
- Plug-ins do DSP, DoProcessOutput
- plug-ins de DSP de vídeo, DoProcessOutput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff3bc844890930209a1c6007213d3c466f0cd15b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105759723"
---
# <a name="doprocessoutput-in-the-sample-video-dsp-plug-in"></a><span data-ttu-id="c7654-108">DoProcessOutput no plug-in de DSP de vídeo de exemplo</span><span class="sxs-lookup"><span data-stu-id="c7654-108">DoProcessOutput in the Sample Video DSP Plug-in</span></span>

<span data-ttu-id="c7654-109">Como um plug-in de DSP de vídeo geralmente dá suporte a vários formatos de vídeo, é conveniente separar o código de implementação de processamento em uma função separada para cada formato.</span><span class="sxs-lookup"><span data-stu-id="c7654-109">Because a video DSP plug-in typically supports several video formats, it is convenient to separate the processing implementation code into a separate function for each format.</span></span> <span data-ttu-id="c7654-110">Isso significa que a implementação de plug-ins do **DoProcessOutput** para vídeo DSP é relativamente simples.</span><span class="sxs-lookup"><span data-stu-id="c7654-110">This means that the implementation of **DoProcessOutput** for video DSP plug-ins is relatively simple.</span></span>

<span data-ttu-id="c7654-111">A implementação no plug-in de exemplo primeiro testa se o usuário habilitou o plug-in.</span><span class="sxs-lookup"><span data-stu-id="c7654-111">The implementation in the sample plug-in first tests whether the user has enabled the plug-in.</span></span> <span data-ttu-id="c7654-112">Se o plug-in estiver desabilitado, o código copiará os dados fornecidos no buffer de entrada para o buffer de saída sem alterá-lo, como demonstra o código a seguir:</span><span class="sxs-lookup"><span data-stu-id="c7654-112">If the plug-in is disabled, the code copies the data provided in the input buffer to the output buffer without changing it, as the following code demonstrates:</span></span>


```C++
// Test whether the plug-in has been disabled by the user.
if (!m_bEnabled)
{
    // Just copy the data without changing it. You should
    // also do any necessary format conversion here.
    memcpy(pbOutputData, pbInputData, m_dwBufferSize);
    *cbBytesProcessed = m_dwBufferSize;

    return S_OK;
}

```



<span data-ttu-id="c7654-113">Se o plug-in estiver habilitado, o código simplesmente executará uma série de verificações no membro **subtipo** de tipo de mídia de entrada para determinar o formato de vídeo atual.</span><span class="sxs-lookup"><span data-stu-id="c7654-113">If the plug-in is enabled, the code simply performs a series of checks on the input media type **subtype** member to determine the current video format.</span></span> <span data-ttu-id="c7654-114">Quando uma correspondência é encontrada, o código chama a função de processamento apropriada.</span><span class="sxs-lookup"><span data-stu-id="c7654-114">When a match is found, the code calls the appropriate processing function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c7654-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c7654-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7654-116">**Implementando um plug-in de DSP de vídeo**</span><span class="sxs-lookup"><span data-stu-id="c7654-116">**Implementing a Video DSP Plug-in**</span></span>](implementing-a-video-dsp-plug-in.md)
</dt> </dl>

 

 




