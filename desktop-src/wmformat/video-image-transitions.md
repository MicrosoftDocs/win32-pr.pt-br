---
title: Transições de imagem de vídeo
description: Transições de imagem de vídeo
ms.assetid: 201ddbfb-567b-4893-b754-569f1e7d8466
keywords:
- Windows SDK do formato de mídia, transições de imagem de vídeo
- ASF (Advanced Systems Format), transições de imagem de vídeo
- ASF (formato de sistemas avançados), transições de imagem de vídeo
- transições de imagem de vídeo
- Windows Codec de imagem de vídeo de mídia 9 v2
- codecs, Windows codec de imagem de vídeo de mídia 9 v2
- fluxos de vídeo, Windows Media Video 9 Image v2 codec
- fluxos de vídeo, transições de imagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b0a915f34ac9a2dcc00f8bcec739d48051361c1744e8e455166d56238529d9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119771236"
---
# <a name="video-image-transitions"></a>Transições de imagem de vídeo

o codec Windows Media Video 9 Image v2 anima uma série de imagens, resultando em um fluxo de vídeo. O codec pode manipular duas imagens ao mesmo tempo, reuni-las e criar uma transição de uma para a outra de acordo com a configuração que você fornece. Esta seção descreve as transições com suporte e os parâmetros necessários.

As transições são listadas na tabela a seguir por seus identificadores globais.



| Identificador de transição                                                                           | Descrição                                                                                                                                  |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [**gravata WMT de \_ transição de VIDEOIMAGE \_ \_ \_**](wmt-videoimage-transition-bow-tie.md)              | A nova imagem é revelada em um conjunto de triângulos nos lados opostos do quadro.                                                                  |
| [**\_círculo de \_ transição de VIDEOIMAGE WMT \_**](wmt-videoimage-transition-circle.md)                 | A nova imagem é revelada em um círculo.                                                                                                           |
| [**\_ \_ \_ esmaecimento cruzado de transição WMT VIDEOIMAGE \_**](wmt-videoimage-transition-cross-fade.md)        | Sem transição especial, os coeficientes de Blend das duas imagens determinam o esmaecimento cruzado (dissolução).                                         |
| [**\_diagonal de \_ transição WMT VIDEOIMAGE \_**](wmt-videoimage-transition-diagonal.md)             | A nova imagem é revelada ao longo de uma linha diagonal originada em um canto do quadro.                                                          |
| [**\_diamante de \_ transição WMT VIDEOIMAGE \_**](wmt-videoimage-transition-diamond.md)               | A nova imagem é revelada em um losango.                                                                                                          |
| [**WMT \_ \_ transição \_ de VIDEOIMAGE esmaecer \_ para \_ cor**](wmt-videoimage-transition-fade-to-color.md) | Desresolve da imagem para um quadro de cor sólida.                                                                                          |
| [**transição de WMT \_ VIDEOIMAGE \_ \_ preenchida \_**](wmt-videoimage-transition-filled-v.md)            | A nova imagem é revelada em um triângulo proveniente de um lado do quadro.                                                                  |
| [**Inverter WMT de \_ \_ transição VIDEOIMAGE \_**](wmt-videoimage-transition-flip.md)                     | A imagem antiga é girada em um eixo y no centro do quadro. A nova imagem é revelada como a parte traseira da imagem antiga.                    |
| [**\_inserção de \_ transição WMT VIDEOIMAGE \_**](wmt-videoimage-transition-inset.md)                   | A nova imagem é revelada por um retângulo proveniente de um canto do quadro.                                                               |
| [**\_íris de \_ transição WMT VIDEOIMAGE \_**](wmt-videoimage-transition-iris.md)                     | A nova imagem é revelada ao longo de um eixo x e um eixo y.                                                                                          |
| [**Roll WMT de \_ \_ página de transição VIDEOIMAGE \_ \_**](wmt-videoimage-transition-page-roll.md)          | A imagem antiga é transformada em um efeito de inversão de página, revelando a nova imagem abaixo.                                                      |
| [**\_retângulo de \_ transição WMT VIDEOIMAGE \_**](wmt-videoimage-transition-rectangle.md)           | A nova imagem é revelada por um retângulo dentro do quadro.                                                                                       |
| [**WMT \_ de \_ transição VIDEOIMAGE \_ revela**](wmt-videoimage-transition-reveal.md)                 | A nova imagem é revelada ao longo de uma linha reta originada de um lado do quadro.                                                          |
| [**SLIDE de transição do WMT \_ VIDEOIMAGE \_ \_**](wmt-videoimage-transition-slide.md)                   | Imagem antiga fora do quadro, revelando a nova imagem abaixo.                                                                       |
| [**\_divisão de \_ transição WMT VIDEOIMAGE \_**](wmt-videoimage-transition-split.md)                   | A nova imagem é revelada por uma divisão horizontal ou vertical na imagem antiga. A divisão aparece ao longo de uma linha reta começando dentro do quadro. |
| [**\_estrela de \_ transição WMT VIDEOIMAGE \_**](wmt-videoimage-transition-star.md)                     | A nova imagem é revelada por uma estrela de cinco pontas dentro do quadro.                                                                               |
| [**\_roda de \_ transição WMT VIDEOIMAGE \_**](wmt-videoimage-transition-wheel.md)                   | A nova imagem é revelada por quatro spokes giratórias com um ponto dinâmico comum.                                                                     |



 

Cada transição é totalmente descrita em seu próprio tópico.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência de programação**](programming-reference.md)
</dt> <dt>

[**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2)
</dt> </dl>

 

 




