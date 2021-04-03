---
title: Sobre a alocação de recursos de streaming
description: Sobre a alocação de recursos de streaming
ms.assetid: b09633c4-58f7-4e3e-bb4d-007845baaccf
keywords:
- Plug-ins do Windows Media Player, DSP de áudio
- plug-ins, DSP de áudio
- plug-ins de processamento de sinal digital, recursos de streaming de áudio
- Plug-ins do DSP, recursos de streaming de áudio
- plug-ins do DSP de áudio, recursos de streaming
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ba82f150908e7b96f4e6e56c2161e1b2fdfe145
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104084103"
---
# <a name="about-allocating-streaming-resources"></a>Sobre a alocação de recursos de streaming

O plug-in DSP de exemplo gerado pelo assistente de plug-in do Windows Media Player não requer buffers de streaming adicionais. No entanto, talvez você queira alocar recursos de memória para o plug-in do DSP. Por exemplo, um plug-in que produz um efeito de eco exigiria um buffer secundário para criar o atraso de tempo necessário.

A interface **IMediaObject** contém dois métodos para lidar com essa situação. O Windows Media Player chama **IMediaObject:: AllocateStreamingResources** para lhe dar a oportunidade de criar os buffers necessários. Posteriormente, o Windows Media Player chama **IMediaObject:: FreeStreamingResources** para permitir que você libere memória que você alocou anteriormente. A implementação do plug-in DSP de exemplo também chama **FreeStreamingResources** de *CProjectName*::**FinalRelease** para garantir que todos os recursos sejam liberados antes que o objeto de plug-in seja destruído.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Implementando um plug-in do DSP de áudio**](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




