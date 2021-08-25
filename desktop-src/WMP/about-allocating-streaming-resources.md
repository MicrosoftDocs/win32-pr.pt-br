---
title: Sobre como alocar recursos de streaming
description: Sobre como alocar recursos de streaming
ms.assetid: b09633c4-58f7-4e3e-bb4d-007845baaccf
keywords:
- Windows Media Player plug-ins, DSP de áudio
- plug-ins, DSP de áudio
- plug-ins de processamento de sinal digital, recursos de streaming de áudio
- Plug-ins do DSP, recursos de streaming de áudio
- plug-ins DSP de áudio, recursos de streaming
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f815fe9875f2e93e140b577da6e00dd7c684c1fedbad13234ecfbf87ca84ddb9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903726"
---
# <a name="about-allocating-streaming-resources"></a>Sobre como alocar recursos de streaming

O plug-in DSP de exemplo gerado pelo assistente Windows Media Player plug-in não requer buffers de streaming adicionais. No entanto, talvez você queira alocar recursos de memória para o plug-in DSP. Por exemplo, um plug-in que produz um efeito de eco exigiria um buffer secundário para criar o atraso de tempo necessário.

A interface **IMediaObject** contém dois métodos para lidar com essa situação. Windows Media Player chama **IMediaObject::AllocateStreamingResources** para dar a você a oportunidade de criar quaisquer buffers necessários. Windows Media Player posteriormente chama **IMediaObject::FreeStreamingResources** para permitir que você liberar qualquer memória alocada anteriormente. A implementação de plug-in DSP de exemplo também chama **FreeStreamingResources** de *CProjectName*::**FinalRelease** para garantir que todos os recursos sejam liberados antes que o objeto de plug-in seja destruído.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Implementando um plug-in DSP de áudio**](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




