---
title: Sobre o plug-in de DSP de vídeo de exemplo
description: Sobre o plug-in de DSP de vídeo de exemplo
ms.assetid: f2ba8e9d-a0e4-4679-99dc-2bfe9e451ffd
keywords:
- Plug-ins do Windows Media Player, exemplos
- plug-ins, amostras
- plug-ins de processamento de sinal digital, amostras
- Plug-ins do DSP, amostras
- Plug-ins do Windows Media Player, DSP de vídeo
- plug-ins, DSP de vídeo
- plug-ins de processamento de sinal digital, amostras de vídeo
- Plug-ins do DSP, amostras de vídeo
- exemplos, plug-ins do DSP
- plug-ins de DSP de vídeo, amostras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ede2eda82c834cefad0e31009805f24941cd4a6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105781288"
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

 

 




