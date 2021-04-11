---
title: Implementando um plug-in de DSP de vídeo
description: Implementando um plug-in de DSP de vídeo
ms.assetid: 36c06c57-7623-430b-8280-9dba7b0a2e9b
keywords:
- Plug-ins do Windows Media Player, DSP de vídeo
- plug-ins, DSP de vídeo
- plug-ins de processamento de sinal digital, implementando código
- Plug-ins do DSP, implementando código
- plug-ins de processamento de sinal digital, modificando código de exemplo
- Plug-ins do DSP, modificando código de exemplo
- plug-ins de processamento de sinal digital, implementação de vídeo
- Plug-ins do DSP, implementação de vídeo
- plug-ins de DSP de vídeo, implementando código
- plug-ins de DSP de vídeo, modificando código de exemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43f1b819f328fc586d21208c00b6f0d03dca4fe9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292298"
---
# <a name="implementing-a-video-dsp-plug-in"></a>Implementando um plug-in de DSP de vídeo

Os adaptadores de vídeo do computador dão suporte a um conjunto de formatos de vídeo. Os codecs de vídeo digital também dão suporte a um conjunto de formatos de vídeo. Ao tentar reproduzir um arquivo de vídeo específico, o Windows Media Player deve escolher um formato a ser usado para renderização. O Player tenta encontrar a melhor correspondência entre os formatos suportados pelo codec de vídeo e os formatos suportados pelo adaptador de vídeo, ou seja, aquele que produz a qualidade mais alta.

Para criar um plug-in de DSP do Windows Media Player que processa vídeo, primeiro você precisará decidir quais formatos de vídeo deseja que seu plug-in processe. O plug-in DSP de vídeo de exemplo funciona com os seguintes formatos de vídeo:

-   NV12
-   YV12
-   YUY2
-   UYVY
-   RGB32
-   RGB24
-   RGB555
-   RGB565

Quais formatos você escolherá para processar cabe a você. Você pode remover formatos do plug-in de exemplo para que eles não sejam mais suportados e você possa adicionar código para processar formatos adicionais.

As seções a seguir fornecem informações adicionais que você deve saber antes de criar seu próprio plug-in de DSP de vídeo para o Windows Media Player:

-   [Negociação de formato de vídeo no plug-in de DSP de vídeo de exemplo](video-format-negotiation-in-the-sample-video-dsp-plug-in.md)
-   [DoProcessOutput no plug-in de DSP de vídeo de exemplo](doprocessoutput-in-the-sample-video-dsp-plug-in.md)
-   [Processando o vídeo](processing-the-video.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Implementando seu código do DSP**](implementing-your-dsp-code.md)
</dt> </dl>

 

 




