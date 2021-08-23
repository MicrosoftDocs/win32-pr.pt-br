---
title: DoProcessOutput no plug-in de DSP de vídeo de exemplo
description: DoProcessOutput no plug-in de DSP de vídeo de exemplo
ms.assetid: 67536e35-a049-49c8-bd89-fad1fab37e6c
keywords:
- plug-ins Windows Media Player, DSP de vídeo
- plug-ins, DSP de vídeo
- plug-ins de processamento de sinal digital, DoProcessOutput
- Plug-ins do DSP, DoProcessOutput
- plug-ins de DSP de vídeo, DoProcessOutput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b031ecddc4f7a1e4a83d4f8a7d8db3b975957789d7f887bf8b12438407624205
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680596"
---
# <a name="doprocessoutput-in-the-sample-video-dsp-plug-in"></a>DoProcessOutput no plug-in de DSP de vídeo de exemplo

Como um plug-in de DSP de vídeo geralmente dá suporte a vários formatos de vídeo, é conveniente separar o código de implementação de processamento em uma função separada para cada formato. Isso significa que a implementação de plug-ins do **DoProcessOutput** para vídeo DSP é relativamente simples.

A implementação no plug-in de exemplo primeiro testa se o usuário habilitou o plug-in. Se o plug-in estiver desabilitado, o código copiará os dados fornecidos no buffer de entrada para o buffer de saída sem alterá-lo, como demonstra o código a seguir:


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



Se o plug-in estiver habilitado, o código simplesmente executará uma série de verificações no membro **subtipo** de tipo de mídia de entrada para determinar o formato de vídeo atual. Quando uma correspondência é encontrada, o código chama a função de processamento apropriada.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Implementando um plug-in de DSP de vídeo**](implementing-a-video-dsp-plug-in.md)
</dt> </dl>

 

 




