---
description: Este tópico descreve dois conceitos relacionados, taxa de proporção de imagem e taxa de proporção de pixel.
ms.assetid: 384bdeaa-5360-42af-9f95-b791af2dcafc
title: Taxa de proporção da imagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71ae59cf213a9d44c9075f33be4bd422b81ced6dea270cf4fc9408990442529e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972939"
---
# <a name="picture-aspect-ratio"></a>Taxa de proporção da imagem

Este tópico descreve dois conceitos relacionados, taxa de proporção de imagem e taxa de proporção de pixel. Em seguida, ele descreve como esses conceitos são expressos em Microsoft Media Foundation usando tipos de mídia.

-   [Taxa de proporção da imagem](#picture-aspect-ratio)
    -   [Letterboxing](#letterboxing)
    -   [Pan-and-Scan](#pan-and-scan)
-   [Taxa de proporção de pixel](#pixel-aspect-ratio)
-   [Trabalhando com taxas de proporção](#working-with-aspect-ratios)
-   [Exemplos de código](#code-examples)
    -   [Localizar a área de exibição](#finding-the-display-area)
    -   [Convertendo entre taxas de proporção de pixel](#converting-between-pixel-aspect-ratios)
    -   [Calculando a área letterbox](#calculating-the-letterbox-area)
-   [Tópicos relacionados](#related-topics)

## <a name="picture-aspect-ratio"></a>Taxa de proporção da imagem

*A taxa de proporção* da imagem define a forma da imagem de vídeo exibida. A taxa de proporção da imagem é notada X:Y, em que X:Y é a proporção da largura da imagem para a altura da imagem. A maioria dos padrões de vídeo usa a taxa de proporção de imagem 4:3 ou 16:9. A taxa de proporção 16:9 normalmente é chamada *de widescreen*. O filme normalmente usa uma taxa de proporção de 1:85:1 ou 1:66:1. A taxa de proporção da imagem também é chamada de DAR *(taxa de proporção de exibição).*

![diagrama mostrando as taxas de proporção 4:3 e 16:9](images/aspect-ratio01.png)

Às vezes, a imagem de vídeo não tem a mesma forma que a área de exibição. Por exemplo, um vídeo 4:3 pode ser mostrado em uma tv de tela larga (16×9). No vídeo do computador, o vídeo pode ser mostrado dentro de uma janela que tem um tamanho arbitrário. Nesse caso, há três maneiras pelas quais a imagem pode ser feita para caber na área de exibição:

-   Alonge a imagem ao longo de um eixo para se ajustar à área de exibição.
-   Dimensione a imagem para se ajustar à área de exibição, mantendo a taxa de proporção da imagem original.
-   Corte a imagem.

Alongar a imagem para se ajustar à área de exibição quase sempre está errado, porque ela não preserva a taxa de proporção de imagem correta.

### <a name="letterboxing"></a>Letterboxing

O processo de dimensionamento de uma imagem widescreen para se ajustar a uma exibição 4:3 é chamado *letterboxing*, mostrado no diagrama a seguir. As áreas retanglulares resultantes na parte superior e inferior da imagem normalmente são preenchidas com preto, embora outras cores possam ser usadas.

![diagrama mostrando a maneira correta de fazer a caixa de texto](images/aspect-ratio02.png)

O caso inverso, dimensionando uma imagem 4:3 para se ajustar a uma tela widescreen, às vezes é chamado *de pillarboxing*. No entanto, o *termo letterbox* também é usado em um sentido geral, para significar o dimensionamento de uma imagem de vídeo para se ajustar a qualquer área de exibição determinada.

![diagrama mostrando pillarboxing](images/aspect-ratio03.png)

### <a name="pan-and-scan"></a>Pan-and-Scan

O painel e a verificação são uma técnica na qual uma imagem de tela larga é cortada para uma área retangular 4×3, para exibição em um dispositivo de exibição 4:3. A imagem resultante preenche toda a exibição, sem exigir áreas de caixa de texto pretas, mas partes da imagem original são cortadas da imagem. A área cortada pode mudar de quadro para quadro, conforme a área de interesse muda. O termo "panorâmico" em *pan-and-scan refere-se* ao efeito de panorâmico causado pela movimentação da área de panorâmico e de verificação.

![diagrama mostrando a pan-and-scan](images/aspect-ratio04.png)

## <a name="pixel-aspect-ratio"></a>Taxa de proporção de pixel

*A PAR (taxa de* proporção de pixel) mede a forma de um pixel.

Quando uma imagem digital é capturada, a imagem é amostrada vertical e horizontalmente, resultando em uma matriz retangular de amostras quantizadas, chamadas *pixels* ou *pels.* A forma da grade de amostragem determina a forma dos pixels na imagem digitalizada.

Aqui está um exemplo que usa números pequenos para manter a matemática simples. Suponha que a imagem original seja quadrada (ou seja, a taxa de proporção da imagem é 1:1); e suponha que a grade de amostragem contenha 12 elementos, organizados em uma grade 4×3. A forma de cada pixel resultante será mais alta do que larga. Especificamente, a forma de cada pixel será 3×4. Pixels que não são quadrados são chamados *de pixels não quadrados.*

![diagrama mostrando uma grade de amostragem não quadrada](images/aspect-ratio05.png)

A taxa de proporção de pixel também se aplica ao dispositivo de exibição. A forma física do dispositivo de exibição e a resolução de pixel físico (entre e para baixo) determinam o PAR do dispositivo de exibição. Os monitores de computador geralmente usam pixels quadrados. Se a imagem PAR e o PAR de exibição não corresponderem, a imagem deverá ser dimensionada em uma dimensão, vertical ou horizontalmente, para ser exibida corretamente. A fórmula a seguir relaciona PAR, DAR (taxa de proporção de exibição) e tamanho da imagem em pixels:

*DAR* = ( largura *da imagem em pixels*  /  *altura da imagem em pixels*) × *PAR*

Observe que a largura da imagem e a altura da imagem nesta fórmula se referem à imagem na memória, não à imagem exibida.

Aqui está um exemplo do mundo real: o vídeo análogo NTSC-M contém 480 linhas de verificação na área de imagem ativa. ITU-R Rec. BT.601 especifica uma taxa de amostragem horizontal de 704 pixels visíveis por linha, ingando uma imagem digital com 704 x 480 pixels. A taxa de proporção da imagem pretendido é de 4:3, ingando um PAR de 10:11.

-   DAR: 4:3
-   Largura em pixels: 704
-   Altura em pixels: 480
-   PAR: 11/10

4/3 = (704/420) x (11/10)

Para exibir essa imagem corretamente em um dispositivo de exibição com pixels quadrados, você deve dimensionar a largura em 10/11 ou a altura em 11/10.

## <a name="working-with-aspect-ratios"></a>Trabalhando com taxas de proporção

A forma correta de um quadro de vídeo é definida pela PAR (taxa de *proporção de pixel)* e pela área *de exibição*.

-   O PAR define a forma dos pixels em uma imagem. Pixels quadrados têm uma taxa de proporção de 1:1. Qualquer outra taxa de proporção descreve um pixel não quadrado. Por exemplo, a tv NTSC usa um PAR 10:11. Supondo que você está apresentando o vídeo em um monitor de computador, a exibição terá pixels quadrados (1:1 PAR). O PAR do conteúdo de origem é dado no atributo [**\_ MF MT \_ PIXEL ASPECT \_ \_ RATIO**](mf-mt-pixel-aspect-ratio-attribute.md) no tipo de mídia.
-   A área de exibição é a região da imagem de vídeo que deve ser mostrada. Há duas áreas de exibição relevantes que podem ser especificadas no tipo de mídia:
    -   Abertura pan-and-scan. A abertura de pan-and-scan é uma região de 4×3 do vídeo que deve ser exibida no modo de verificação/pan. Ele é usado para mostrar conteúdo de tela larga em uma exibição 4×3 sem caixa de texto. A abertura de pan e scan é dada no atributo [**\_ \_ \_ \_ APERTURE MF MT PAN SCAN e**](mf-mt-pan-scan-aperture-attribute.md) deve ser usada somente quando o atributo [**MF \_ MT PAN SCAN \_ \_ \_ ENABLED**](mf-mt-pan-scan-enabled-attribute.md) for **TRUE.**
    -   Exibir a abertura. Essa abertura é definida em alguns padrões de vídeo. Qualquer coisa fora da abertura de exibição é a região de varredura em excesso e não deve ser exibida. Por exemplo, a tv NTSC tem 720×480 pixels com uma abertura de exibição de 704×480. A abertura de exibição é dada no atributo [**\_ MF MT \_ MINIMUM DISPLAY \_ \_ APERTURE.**](mf-mt-minimum-display-aperture-attribute.md) Se estiver presente, ele deverá ser usado quando o modo de pan-and-scan for **FALSE.**

Se o modo pan-and-can for **FALSE** e nenhuma abertura de exibição for definida, todo o quadro de vídeo deverá ser exibido. Na verdade, esse é o caso da maioria dos conteúdos de vídeo que não seja a tv e o vídeo de DVD. A taxa de proporção de toda a imagem é calculada como *(* altura da área de exibição da largura da área de  /  exibição ) × *PAR*.

## <a name="code-examples"></a>Exemplos de código

### <a name="finding-the-display-area"></a>Localizar a área de exibição

O código a seguir mostra como obter a área de exibição do tipo de mídia.


```C++
MFVideoArea MakeArea(float x, float y, DWORD width, DWORD height);

HRESULT GetVideoDisplayArea(IMFMediaType *pType, MFVideoArea *pArea)
{
    HRESULT hr = S_OK;
    BOOL bPanScan = FALSE;
    UINT32 width = 0, height = 0;

    bPanScan = MFGetAttributeUINT32(pType, MF_MT_PAN_SCAN_ENABLED, FALSE);

    // In pan-and-scan mode, try to get the pan-and-scan region.
    if (bPanScan)
    {
        hr = pType->GetBlob(MF_MT_PAN_SCAN_APERTURE, (UINT8*)pArea, 
            sizeof(MFVideoArea), NULL);
    }

    // If not in pan-and-scan mode, or the pan-and-scan region is not set, 
    // get the minimimum display aperture.

    if (!bPanScan || hr == MF_E_ATTRIBUTENOTFOUND)
    {
        hr = pType->GetBlob(MF_MT_MINIMUM_DISPLAY_APERTURE, (UINT8*)pArea, 
            sizeof(MFVideoArea), NULL);

        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            // Minimum display aperture is not set.

            // For backward compatibility with some components, 
            // check for a geometric aperture. 

            hr = pType->GetBlob(MF_MT_GEOMETRIC_APERTURE, (UINT8*)pArea, 
                sizeof(MFVideoArea), NULL);
        }

        // Default: Use the entire video area.

        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            hr = MFGetAttributeSize(pType, MF_MT_FRAME_SIZE, &width, &height);

            if (SUCCEEDED(hr))
            {
                *pArea = MakeArea(0.0, 0.0, width, height);
            }
        }
    }
    return hr;
}
```




```C++
MFOffset MakeOffset(float v)
{
    MFOffset offset;
    offset.value = short(v);
    offset.fract = WORD(65536 * (v-offset.value));
    return offset;
}
```




```C++
MFVideoArea MakeArea(float x, float y, DWORD width, DWORD height)
{
    MFVideoArea area;
    area.OffsetX = MakeOffset(x);
    area.OffsetY = MakeOffset(y);
    area.Area.cx = width;
    area.Area.cy = height;
    return area;
}
```



### <a name="converting-between-pixel-aspect-ratios"></a>Convertendo entre taxas de proporção de pixel

O código a seguir mostra como converter um retângulo de PAR (taxa de proporção) de um pixel para outro, preservando a taxa de proporção da imagem.


```C++
//-----------------------------------------------------------------------------
// Converts a rectangle from one pixel aspect ratio (PAR) to another PAR.
// Returns the corrected rectangle.
//
// For example, a 720 x 486 rect with a PAR of 9:10, when converted to 1x1 PAR,
// must be stretched to 720 x 540.
//-----------------------------------------------------------------------------

RECT CorrectAspectRatio(const RECT& src, const MFRatio& srcPAR, const MFRatio& destPAR)
{
    // Start with a rectangle the same size as src, but offset to (0,0).
    RECT rc = {0, 0, src.right - src.left, src.bottom - src.top};

    // If the source and destination have the same PAR, there is nothing to do.
    // Otherwise, adjust the image size, in two steps:
    //  1. Transform from source PAR to 1:1
    //  2. Transform from 1:1 to destination PAR.

    if ((srcPAR.Numerator != destPAR.Numerator) || 
        (srcPAR.Denominator != destPAR.Denominator))
    {
        // Correct for the source's PAR.

        if (srcPAR.Numerator > srcPAR.Denominator)
        {
            // The source has "wide" pixels, so stretch the width.
            rc.right = MulDiv(rc.right, srcPAR.Numerator, srcPAR.Denominator);
        }
        else if (srcPAR.Numerator < srcPAR.Denominator)
        {
            // The source has "tall" pixels, so stretch the height.
            rc.bottom = MulDiv(rc.bottom, srcPAR.Denominator, srcPAR.Numerator);
        }
        // else: PAR is 1:1, which is a no-op.

        // Next, correct for the target's PAR. This is the inverse operation of 
        // the previous.

        if (destPAR.Numerator > destPAR.Denominator)
        {
            // The destination has "wide" pixels, so stretch the height.
            rc.bottom = MulDiv(rc.bottom, destPAR.Numerator, destPAR.Denominator);
        }
        else if (destPAR.Numerator < destPAR.Denominator)
        {
            // The destination has "tall" pixels, so stretch the width.
            rc.right = MulDiv(rc.right, destPAR.Denominator, destPAR.Numerator);
        }
        // else: PAR is 1:1, which is a no-op.
    }
    return rc;
}
```



### <a name="calculating-the-letterbox-area"></a>Calculando a área letterbox

O código a seguir calcula a área da caixa de texto, considerando um retângulo de origem e de destino. Supõe-se que ambos os retângulos tenham o mesmo PAR.


```C++
RECT LetterBoxRect(const RECT& rcSrc, const RECT& rcDst)
{
    // Compute source/destination ratios.
    int iSrcWidth  = rcSrc.right - rcSrc.left;
    int iSrcHeight = rcSrc.bottom - rcSrc.top;

    int iDstWidth  = rcDst.right - rcDst.left;
    int iDstHeight = rcDst.bottom - rcDst.top;

    int iDstLBWidth;
    int iDstLBHeight;

    if (MulDiv(iSrcWidth, iDstHeight, iSrcHeight) <= iDstWidth) 
    {
        // Column letterboxing ("pillar box")
        iDstLBWidth  = MulDiv(iDstHeight, iSrcWidth, iSrcHeight);
        iDstLBHeight = iDstHeight;
    }
    else 
    {
        // Row letterboxing.
        iDstLBWidth  = iDstWidth;
        iDstLBHeight = MulDiv(iDstWidth, iSrcHeight, iSrcWidth);
    }

    // Create a centered rectangle within the current destination rect

    LONG left = rcDst.left + ((iDstWidth - iDstLBWidth) / 2);
    LONG top = rcDst.top + ((iDstHeight - iDstLBHeight) / 2);

    RECT rc;
    SetRect(&rc, left, top, left + iDstLBWidth, top + iDstLBHeight);
    return rc;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de mídia](media-types.md)
</dt> <dt>

[Tipos de mídia de vídeo](video-media-types.md)
</dt> <dt>

[**MF \_ MT \_ MINIMUM \_ DISPLAY \_ APERTURE**](mf-mt-minimum-display-aperture-attribute.md)
</dt> <dt>

[**ABERTURA DO \_ MF MT \_ PAN \_ SCAN \_**](mf-mt-pan-scan-aperture-attribute.md)
</dt> <dt>

[**MF \_ MT \_ PAN \_ SCAN \_ ENABLED**](mf-mt-pan-scan-enabled-attribute.md)
</dt> <dt>

[**TAXA DE \_ PROPORÇÃO DO PIXEL MT \_ \_ \_ MF**](mf-mt-pixel-aspect-ratio-attribute.md)
</dt> </dl>

 

 



