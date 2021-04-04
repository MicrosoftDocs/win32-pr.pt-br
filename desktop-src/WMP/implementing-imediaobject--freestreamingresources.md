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
# <a name="implementing-imediaobjectfreestreamingresources"></a>Implementando IMediaObject:: FreeStreamingResources

É importante que o código libere qualquer memória alocada antes que o objeto de plug-in seja destruído. O Windows Media Player chama **FreeStreamingResources** para permitir que você faça isso. Para segurança, o exemplo criado pelo assistente de plug-in inclui uma chamada para **FreeStreamingResources** no método **FinalRelease** para garantir que a memória seja liberada. Você deve adicionar o seguinte código a **FreeStreamingResources** para o exemplo de eco:


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Trabalhando com recursos de streaming**](working-with-streaming-resources.md)
</dt> </dl>

 

 




