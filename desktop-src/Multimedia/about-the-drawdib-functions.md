---
title: Sobre as funções DrawDib
description: Sobre as funções DrawDib
ms.assetid: 0ae993df-8393-479e-aa11-14301384715d
keywords:
- vídeo para Windows (VFW), DrawDib
- VFW (vídeo para Windows), DrawDib
- DrawDib, sobre
- DrawDib, tabelas de cores
- DrawDib, modo de transferência
- DrawDib, adaptadores de vídeo
- DrawDib, alongamento de imagem
- DrawDib, imagens compactadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18e03b41d5af776c39f7d100e9478bd408011d61d8e3d661cb80bd9ab52f08c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942084"
---
# <a name="about-the-drawdib-functions"></a>Sobre as funções DrawDib

Coletivamente, as funções DrawDib são semelhantes à função [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) , pois fornecem recursos de alargamento de imagem e pontilhamento. No entanto, as funções DrawDib dão suporte à descompactação de imagem, ao streaming de dados e a um número maior de adaptadores de vídeo.

Você achará útil usar as funções DrawDib em algumas circunstâncias. Ainda assim, [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) é mais diversificado do que as funções DrawDib e deve ser usado quando as funções DrawDib não puderem fornecer a funcionalidade desejada. A lista a seguir descreve os fatores a serem considerados ao decidir se deve usar as funções DrawDib ou **StretchDIBits**.

-   Formato de informações da tabela de cores. As funções DrawDib exibem imagens que usam o formato de **\_ \_ cores de DIB RGB** para sua tabela de cores. Se as imagens em seu aplicativo armazenarem informações da tabela de cores com o formato **DIB \_ PAL \_ Colors** ou **DIB \_ PAL \_ indics** , você deverá usar [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) para exibi-las.
-   Modo de transferência. As funções DrawDib exigem que seu aplicativo use o modo de transferência **SRCCOPY** . Se seu aplicativo usar [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) com um modo de transferência diferente de **SRCCOPY**, você deverá continuar a usar o **StretchDIBits**. Da mesma forma, se você precisar usar outras operações de varredura em seu aplicativo, como um XOR, use **StretchDIBits**.
-   Qualidade da reprodução de vídeo e animação. Você pode usar as funções DrawDib para aplicativos de streaming de dados, como aqueles que reproduzem clipes de vídeo e sequências animadas. As funções DrawDib superaram o [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) , pois fornecem imagens de qualidade superior e melhoram o movimento durante a reprodução.
-   Adaptadores de vídeo. As funções DrawDib dão suporte a um número maior de adaptadores de vídeo que o [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) dá suporte. As funções DrawDib dão suporte a adaptadores de cores VGA que fornecem paletas de 16 cores usando profundidade de imagem de 4 bits, adaptadores SVGA que fornecem paletas de cor de 256 usando profundidade de imagem de 8 bits e adaptadores de exibição de cor verdadeira que fornecem milhares de cores usando profundidades de imagem de 16 bits, 24 bits e 32 bits.

    As funções DrawDib também melhoram a velocidade e a qualidade da exibição de imagens em adaptadores de vídeo com recursos mais limitados. Por exemplo, ao usar um adaptador de vídeo de 8 bits, as funções DrawDib pontilham com eficiência imagens true-color para 256 cores. Eles também pontilham imagens de 8 bits ao usar adaptadores de vídeo de 4 bits.

-   Alongamento de imagem. Como [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits), as funções DrawDib usam retângulos de origem e de destino para controlar a parte de uma imagem exibida. Você pode cortar partes indesejadas de uma imagem ou alongar uma imagem, variando a posição e o tamanho dos retângulos de origem e de destino. Se um driver de vídeo não oferecer suporte ao alongamento de imagem, as funções DrawDib fornecerão recursos de ampliação mais eficientes do que o **StretchDIBits**.
-   Imagens compactadas. As funções DrawDib desenharão qualquer formato para o qual você tenha um descompactador, incluindo a RLE (codificação de comprimento de execução), Cinepak e 411 YUV. Windows inclui descompactadores de RLE e Cinepak que podem ser instalados opcionalmente.
-   O codec Indeo não tem mais suporte no Windows.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DrawDib](drawdib.md)
</dt> </dl>

 

 