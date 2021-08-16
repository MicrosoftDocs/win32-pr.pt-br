---
title: Trabalhando com recursos de streaming
description: Trabalhando com recursos de streaming
ms.assetid: 0258ad24-f1b9-4cb3-921c-068072fd2dbb
keywords:
- Windows Media Player plug-ins, recursos de streaming de exemplo de eco
- plug-ins, recursos de streaming de exemplo de eco
- plug-ins de processamento de sinal digital, recursos de streaming de exemplo de eco
- Plug-ins do DSP, recursos de streaming de exemplo de eco
- Exemplo de plug-in do DSP de eco, recursos de streaming
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 268dc57bfad71f8ee46a3b934e671e478ca6a78a6b05fc30b7123e7b3f7f6ba0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118567165"
---
# <a name="working-with-streaming-resources"></a>Trabalhando com recursos de streaming

O projeto de plug-in DSP de áudio de exemplo gerado pelo assistente de plug-in Windows Media Player não exige que nenhum recurso de streaming seja alocado pelo plug-in. O exemplo de Eco, no entanto, requer um buffer separado para manter os dados de áudio por um período de tempo para criar o efeito de atraso. O buffer é gerenciado por dois métodos: **IMediaObject::AllocateStreamingResources**, que cria o buffer e **IMediaObject::FreeStreamingResources,** que libera o buffer. Os **métodos IMediaObject** são implementados em Echo.cpp.

As seções a seguir fornecem mais informações sobre como gerenciar os buffers:

-   [Variáveis para gerenciar o buffer de atraso](variables-to-manage-the-delay-buffer.md)
-   [Implementando IMediaObject::AllocateStreamingResources](implementing-imediaobject--allocatestreamingresources.md)
-   [Implementando IMediaObject::FreeStreamingResources](implementing-imediaobject--freestreamingresources.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**O exemplo de eco**](the-echo-sample.md)
</dt> </dl>

 

 




