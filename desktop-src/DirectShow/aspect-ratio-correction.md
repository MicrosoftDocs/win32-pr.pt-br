---
description: Correção de taxa de proporção
ms.assetid: 0ed6010b-9168-44b1-be49-0c9d5d77ce3f
title: Correção de taxa de proporção
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2460f7ecce1513394d941eafe8bdf8a7a80e9727
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105771676"
---
# <a name="aspect-ratio-correction"></a>Correção de taxa de proporção

Este tópico aplica-se ao Windows XP Service Pack 2 ou posterior.

No modo de combinação, o VMR dimensiona o vídeo para a taxa de proporção correta. (Exceção: consulte [mixagem sem quadrados](non-square-mixing.md).) Isso pode exigir o alongamento do vídeo se a taxa de proporção preferida não for igual à taxa de proporção física da imagem. Por exemplo, o formato DV (Digital Video) é 720 x 480 pixels (3:2), mas deve ser exibido a uma taxa de proporção de 4:3.

O VMR dá suporte a dois comportamentos diferentes para correção de taxa de proporção:

-   Ajuste o tamanho horizontal ou vertical, para que a imagem sempre seja ampliada, nunca reduzida. Esse agora é o comportamento padrão.
-   Ajuste o tamanho horizontal, alongando ou reduzindo o vídeo.

Como o segundo comportamento (somente ajuste horizontal) pode envolver a redução do vídeo, a imagem de saída pode ter menos resolução. Por esse motivo, o primeiro comportamento é preferencial. Por exemplo, no caso do vídeo 720 x 480 na taxa de proporção 4:3, o comportamento padrão produz uma imagem 720 x 550, enquanto o ajuste horizontal produz uma imagem menor de 640 x 480.

**VMR-7**: para definir a preferência de correção de taxa de proporção, chame [**IVMRMixerControl:: SetMixingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect). Defina o \_ sinalizador MixerPref ARAdjustXorY para o comportamento padrão ou desmarque este sinalizador apenas para ajuste horizontal.

**VMR-9**: para definir a preferência de correção de taxa de proporção, chame [**IVMRMixerControl9:: SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs). Defina o \_ sinalizador MixerPref9 ARAdjustXorY para o comportamento padrão ou desmarque este sinalizador apenas para ajuste horizontal.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o modo de mixagem do VMR](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



