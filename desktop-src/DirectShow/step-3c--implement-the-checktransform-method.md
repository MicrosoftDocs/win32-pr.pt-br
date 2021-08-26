---
description: Etapa 3C.
ms.assetid: e780df46-bf47-4334-b788-05ad8179f051
title: Etapa 3C. Implementar o método CheckTransform
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 430ad933acfa7fc41a8b075183080e0b710a5d4780b55fa89cd4bf80984c1edc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075586"
---
# <a name="step-3c-implement-the-checktransform-method"></a>Etapa 3C. Implementar o método CheckTransform

Esta é a etapa 3C do tutorial [escrevendo filtros de transformação](writing-transform-filters.md).

> [!Note]  
> Esta etapa não é necessária para filtros que derivam de **CTransInPlaceFilter**.

 

O método [**CTransformFilter:: CheckTransform**](ctransformfilter-checktransform.md) verifica se um tipo de saída proposto é compatível com o tipo de entrada atual. O método também será chamado se o PIN de entrada se reconectar após a conexão do pino de saída.

O exemplo a seguir verifica se o formato é RLE8 vídeo; as dimensões da imagem correspondem ao formato de entrada; e as entradas da paleta são as mesmas. Ele também rejeita os retângulos de origem e destino que não correspondem ao tamanho da imagem.


```C++
HRESULT CRleFilter::CheckTransform(
    const CMediaType *mtIn, const CMediaType *mtOut)
{
    // Check the major type.
    if (mtOut->majortype != MEDIATYPE_Video)
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Check the subtype and format type.
    FOURCCMap fccMap = FCC('MRLE'); 
    if (mtOut->subtype != static_cast<GUID>(fccMap))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }
    if ((mtOut->formattype != FORMAT_VideoInfo) || 
        (mtOut->cbFormat < sizeof(VIDEOINFOHEADER)))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Compare the bitmap information against the input type.
    ASSERT(mtIn->formattype == FORMAT_VideoInfo);
    BITMAPINFOHEADER *pBmiOut = HEADER(mtOut->pbFormat);
    BITMAPINFOHEADER *pBmiIn = HEADER(mtIn->pbFormat);
    if ((pBmiOut->biPlanes != 1) ||
        (pBmiOut->biBitCount != 8) ||
        (pBmiOut->biCompression != BI_RLE8) ||
        (pBmiOut->biWidth != pBmiIn->biWidth) ||
        (pBmiOut->biHeight != pBmiIn->biHeight))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Compare source and target rectangles.
    RECT rcImg;
    SetRect(&rcImg, 0, 0, pBmiIn->biWidth, pBmiIn->biHeight);
    RECT *prcSrc = &((VIDEOINFOHEADER*)(mtIn->pbFormat))->rcSource;
    RECT *prcTarget = &((VIDEOINFOHEADER*)(mtOut->pbFormat))->rcTarget;
    if (!IsRectEmpty(prcSrc) && !EqualRect(prcSrc, &rcImg))
    {
        return VFW_E_INVALIDMEDIATYPE;
    }
    if (!IsRectEmpty(prcTarget) && !EqualRect(prcTarget, &rcImg))
    {
        return VFW_E_INVALIDMEDIATYPE;
    }

    // Check the palette table.
    if (pBmiOut->biClrUsed != pBmiIn->biClrUsed)
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }
    DWORD cbPalette = pBmiOut->biClrUsed * sizeof(RGBQUAD);
    if (mtOut->cbFormat < sizeof(VIDEOINFOHEADER) + cbPalette)
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }
    if (0 != memcmp(pBmiOut + 1, pBmiIn + 1, cbPalette))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Everything is good.
    return S_OK;
}
```



**Fixar reconexões**

Os aplicativos podem se desconectar e reconectar Pins. Suponha que um aplicativo conecte ambos os Pins, desconecte o PIN de entrada e, em seguida, reconecte o PIN de entrada usando um novo tamanho de imagem. Nesse caso, **CheckTransform** falhará porque as dimensões da imagem não correspondem mais. Esse comportamento é razoável, embora o filtro também possa tentar reconectar o pino de saída com um novo tipo de mídia.

Em seguida: [etapa 4. Definir propriedades de alocador](step-4--set-allocator-properties.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Reconectando Pins](reconnecting-pins.md)
</dt> <dt>

[Retângulos de origem e de destino em renderizadores de vídeo](source-and-target-rectangles-in-video-renderers.md)
</dt> <dt>

[gravando filtros de DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



