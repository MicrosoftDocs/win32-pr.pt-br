---
title: Implementando IMediaObject FreeStreamingResources
description: Implementando IMediaObject FreeStreamingResources
ms.assetid: 970dd10b-a7a0-4ba0-97e3-725d5c914500
keywords:
- Windows Media Player plug-ins, recursos de streaming de exemplo de eco
- plug-ins, recursos de streaming de exemplo de eco
- plug-ins de processamento de sinal digital, recursos de streaming de exemplo de eco
- Plug-ins do DSP, recursos de streaming de exemplo de eco
- Exemplo de plug-in do DSP de eco, recursos de streaming
- Exemplo de plug-in do DSP de eco, liberando memória
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30da5f92ec8420ccc90f74256003aae02664a57a8ffad3470901f672cf37aa73
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119617316"
---
# <a name="implementing-imediaobjectfreestreamingresources"></a>Implementando IMediaObject::FreeStreamingResources

É importante que seu código libere qualquer memória alocada antes que o objeto de plug-in seja destruído. Windows Media Player chama **FreeStreamingResources** para permitir que você faça isso. Por segurança, o exemplo criado pelo assistente de plug-in inclui uma chamada para **FreeStreamingResources** no método **FinalRelease** para garantir que a memória seja liberada. Você deve adicionar o seguinte código a **FreeStreamingResources** para o exemplo de Eco:


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

 

 




