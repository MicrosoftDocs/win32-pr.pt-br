---
title: Trabalhando com recursos de streaming
description: Trabalhando com recursos de streaming
ms.assetid: 0258ad24-f1b9-4cb3-921c-068072fd2dbb
keywords:
- Plug-ins do Windows Media Player, recursos de streaming de amostra de eco
- plug-ins, amostras de eco de recursos de streaming
- plug-ins de processamento de sinal digital, Echo amostras de recursos de streaming
- Plug-ins do DSP, amostras de eco de recursos de streaming
- Exemplo de plug-in de eco do DSP, recursos de streaming
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a1df8cc221f3d75c8333b3ffd41a144d28bed7a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105784674"
---
# <a name="working-with-streaming-resources"></a>Trabalhando com recursos de streaming

O projeto de plug-in do DSP de áudio de exemplo gerado pelo assistente de plug-in do Windows Media Player não exige que recursos de streaming sejam alocados pelo plug-in. O exemplo de eco, no entanto, requer um buffer separado para manter os dados de áudio por um período de tempo para criar o efeito de atraso. O buffer é gerenciado por dois métodos: **IMediaObject:: AllocateStreamingResources**, que cria o buffer e **IMediaObject:: FreeStreamingResources**, que libera o buffer. Os métodos **IMediaObject** são implementados em Echo. cpp.

As seções a seguir fornecem mais informações sobre como gerenciar os buffers:

-   [Variáveis para gerenciar o buffer de atraso](variables-to-manage-the-delay-buffer.md)
-   [Implementando IMediaObject:: AllocateStreamingResources](implementing-imediaobject--allocatestreamingresources.md)
-   [Implementando IMediaObject:: FreeStreamingResources](implementing-imediaobject--freestreamingresources.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**O exemplo de eco**](the-echo-sample.md)
</dt> </dl>

 

 




