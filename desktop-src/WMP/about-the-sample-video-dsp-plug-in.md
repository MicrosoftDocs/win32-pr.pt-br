---
title: Sobre o plug-in de DSP de vídeo de exemplo
description: Sobre o plug-in de DSP de vídeo de exemplo
ms.assetid: f2ba8e9d-a0e4-4679-99dc-2bfe9e451ffd
keywords:
- plug-ins Windows Media Player, amostras
- plug-ins, amostras
- plug-ins de processamento de sinal digital, amostras
- Plug-ins do DSP, amostras
- plug-ins Windows Media Player, DSP de vídeo
- plug-ins, DSP de vídeo
- plug-ins de processamento de sinal digital, amostras de vídeo
- Plug-ins do DSP, amostras de vídeo
- exemplos, plug-ins do DSP
- plug-ins de DSP de vídeo, amostras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbb771bb87ffb53cf46022fc17ee2588e7cdac0b6b2c821f98fe6cf86799434c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119470246"
---
# <a name="about-the-sample-video-dsp-plug-in"></a>Sobre o plug-in de DSP de vídeo de exemplo

O plug-in de DSP de vídeo de exemplo fornece uma implementação de processamento simples que dimensiona a saturação de cor do vídeo por um fator fornecido pelo usuário na página de propriedades. O plug-in aceita valores entre zero e 1. O valor padrão é 1. Um valor de 1 não tem efeito sobre a imagem de vídeo; outros fatores de escala dessaturam a cor da imagem. Por exemplo, um valor de 0,5 resultaria em uma saturação de cor de 50%. Um valor de zero resulta em vídeo em escala de cinza.

O plug-in DSP de vídeo de exemplo funciona com os seguintes formatos de vídeo:

-   NV12
-   YV12
-   YUY2
-   UYVY
-   RGB32
-   RGB24
-   RGB555
-   RGB565

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando um plug-in do DSP**](building-a-dsp-plug-in.md)
</dt> </dl>

 

 




