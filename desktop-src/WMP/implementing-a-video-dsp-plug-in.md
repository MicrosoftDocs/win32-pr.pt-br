---
title: Implementando um plug-in DSP de vídeo
description: Implementando um plug-in DSP de vídeo
ms.assetid: 36c06c57-7623-430b-8280-9dba7b0a2e9b
keywords:
- Windows Media Player plug-ins,DSP de vídeo
- plug-ins, DSP de vídeo
- plug-ins de processamento de sinal digital, implementando código
- Plug-ins DSP, implementando código
- plug-ins de processamento de sinal digital, modificando o código de exemplo
- Plug-ins DSP, modificando o código de exemplo
- plug-ins de processamento de sinal digital, implementação de vídeo
- Plug-ins DSP, implementação de vídeo
- plug-ins DSP de vídeo, implementando código
- plug-ins DSP de vídeo, modificando o código de exemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4afdbabd36167c11ef7c1c57aeccb475605f9365c550c572422af3440d760ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135699"
---
# <a name="implementing-a-video-dsp-plug-in"></a>Implementando um plug-in DSP de vídeo

Os adaptadores de vídeo do computador são suportados por um conjunto de formatos de vídeo. Os codecs de vídeo digital também são suportados por um conjunto de formatos de vídeo. Ao tentar reproduzir um arquivo de vídeo específico, Windows Media Player deve escolher um formato a ser usado para renderização. O Player tenta encontrar a melhor combinação entre os formatos com suporte pelo codec de vídeo e os formatos com suporte pelo adaptador de exibição de vídeo, ou seja, aquele que produz a qualidade mais alta.

Para criar um Windows Media Player plug-in DSP que processa o vídeo, primeiro você precisará decidir quais formatos de vídeo você gostaria que seu plug-in processasse. O plug-in DSP de vídeo de exemplo funciona com os seguintes formatos de vídeo:

-   NV12
-   YV12
-   YUY2
-   UYVY
-   RGB32
-   RGB24
-   RGB555
-   RGB565

Quais formatos você escolhe para processar são seus. Você pode remover formatos do plug-in de exemplo para que eles não sejam mais suportados e você pode adicionar código para processar formatos adicionais.

As seções a seguir fornecem informações adicionais que você deve saber antes de criar seu próprio plug-in DSP de vídeo para Windows Media Player:

-   [Negociação de formato de vídeo no plug-in DSP de vídeo de exemplo](video-format-negotiation-in-the-sample-video-dsp-plug-in.md)
-   [DoProcessOutput no plug-in DSP de vídeo de exemplo](doprocessoutput-in-the-sample-video-dsp-plug-in.md)
-   [Processamento do vídeo](processing-the-video.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Implementando seu código DSP**](implementing-your-dsp-code.md)
</dt> </dl>

 

 




