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

 

 




