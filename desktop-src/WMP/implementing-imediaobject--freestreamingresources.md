---
title: Implementando IMediaObject FreeStreamingResources
description: Implementando IMediaObject FreeStreamingResources
ms.assetid: 970dd10b-a7a0-4ba0-97e3-725d5c914500
keywords:
- Plug-ins do Windows Media Player, recursos de streaming de amostra de eco
- plug-ins, amostras de eco de recursos de streaming
- plug-ins de processamento de sinal digital, Echo amostras de recursos de streaming
- Plug-ins do DSP, amostras de eco de recursos de streaming
- Exemplo de plug-in de eco do DSP, recursos de streaming
- Exemplo de plug-in de eco do DSP, liberando memória
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a31a293cfc68caf43496d031426de2441c9c1d05
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822461"
---
# <a name="implementing-imediaobjectfreestreamingresources"></a><span data-ttu-id="afa77-109">Implementando IMediaObject:: FreeStreamingResources</span><span class="sxs-lookup"><span data-stu-id="afa77-109">Implementing IMediaObject::FreeStreamingResources</span></span>

<span data-ttu-id="afa77-110">É importante que o código libere qualquer memória alocada antes que o objeto de plug-in seja destruído.</span><span class="sxs-lookup"><span data-stu-id="afa77-110">It is important that your code releases any allocated memory before the plug-in object is destroyed.</span></span> <span data-ttu-id="afa77-111">O Windows Media Player chama **FreeStreamingResources** para permitir que você faça isso.</span><span class="sxs-lookup"><span data-stu-id="afa77-111">Windows Media Player calls **FreeStreamingResources** to allow you to do this.</span></span> <span data-ttu-id="afa77-112">Para segurança, o exemplo criado pelo assistente de plug-in inclui uma chamada para **FreeStreamingResources** no método **FinalRelease** para garantir que a memória seja liberada.</span><span class="sxs-lookup"><span data-stu-id="afa77-112">For safety, the sample created by the plug-in wizard includes a call to **FreeStreamingResources** in the **FinalRelease** method to ensure that the memory is freed.</span></span> <span data-ttu-id="afa77-113">Você deve adicionar o seguinte código a **FreeStreamingResources** para o exemplo de eco:</span><span class="sxs-lookup"><span data-stu-id="afa77-113">You must add the following code to **FreeStreamingResources** for the Echo sample:</span></span>


```
// Test whether a buffer exists.
if (m_pbDelayBuffer)
{
    delete m_pbDelayBuffer;
    m_pbDelayBuffer = NULL;
    m_pbDelayPointer = NULL;
    m_cbDelayBuffer = 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="afa77-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="afa77-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="afa77-115">**Trabalhando com recursos de streaming**</span><span class="sxs-lookup"><span data-stu-id="afa77-115">**Working with Streaming Resources**</span></span>](working-with-streaming-resources.md)
</dt> </dl>

 

 




