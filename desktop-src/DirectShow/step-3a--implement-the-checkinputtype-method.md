---
description: Etapa 3A.
ms.assetid: 774fcb12-8928-4667-8ef6-dce86717cc29
title: Etapa 3A. Implementar o método CheckInputType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 692175e0def453f86b618a355044e4a117a4343fed56f029704091134e8bc31f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118652136"
---
# <a name="step-3a-implement-the-checkinputtype-method"></a>Etapa 3A. Implementar o método CheckInputType

Esta é a etapa 3A do tutorial Escrevendo [filtros de transformação.](writing-transform-filters.md)

O [**método CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) é chamado quando o filtro upstream propõe um tipo de mídia para o filtro de transformação. Esse método leva um ponteiro para um [**objeto CMediaType,**](cmediatype.md) que é um wrapper fino para a estrutura [**AM MEDIA \_ \_ TYPE.**](/windows/win32/api/strmif/ns-strmif-am_media_type) Nesse método, você deve examinar todos os campos relevantes da estrutura **AM \_ MEDIA \_ TYPE,** incluindo os campos no bloco de formato. Você pode usar os métodos de acessador definidos **em CMediaType** ou referenciar os membros da estrutura diretamente. Se algum campo não for válido, retorne VFW \_ E \_ TYPE NOT \_ \_ ACCEPTED. Se todo o tipo de mídia for válido, retorne S \_ OK.

Por exemplo, no filtro do codificador RLE, o tipo de entrada deve ser um vídeo RGB de 8 ou 4 bits descompactado. Não há motivo para dar suporte a outros formatos de entrada, como RGB de 16 ou 24 bits, porque o [](color-space-converter-filter.md) filtro teria que convertê-los em uma profundidade de bits inferior e DirectShow já fornece um filtro conversor de espaço de cor para essa finalidade. O exemplo a seguir pressupo que o codificador dá suporte a vídeo de 8 bits, mas não vídeo de 4 bits:


```C++
HRESULT CRleFilter::CheckInputType(const CMediaType *mtIn)
{
    if ((mtIn->majortype != MEDIATYPE_Video) ||
        (mtIn->subtype != MEDIASUBTYPE_RGB8) ||
        (mtIn->formattype != FORMAT_VideoInfo) || 
        (mtIn->cbFormat < sizeof(VIDEOINFOHEADER)))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    VIDEOINFOHEADER *pVih = 
        reinterpret_cast<VIDEOINFOHEADER*>(mtIn->pbFormat);
    if ((pVih->bmiHeader.biBitCount != 8) ||
        (pVih->bmiHeader.biCompression != BI_RGB))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Check the palette table.
    if (pVih->bmiHeader.biClrUsed > PALETTE_ENTRIES(pVih))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }
    DWORD cbPalette = pVih->bmiHeader.biClrUsed * sizeof(RGBQUAD);
    if (mtIn->cbFormat < sizeof(VIDEOINFOHEADER) + cbPalette)
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Everything is good.
    return S_OK;
}
```



Neste exemplo, o método primeiro verifica o tipo principal e o subtipo. Em seguida, ele verifica o tipo de formato para verificar se o bloco de formato é uma [**estrutura VIDEOINFOHEADER.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) O filtro também pode dar [**suporte a VIDEOINFOHEADER2,**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)mas, nesse caso, não haverá nenhum benefício real. A **estrutura VIDEOINFOHEADER2** adiciona suporte para entrelaçamento e pixels não quadrados, que provavelmente não serão relevantes em um vídeo de 8 bits.

Se o tipo de formato estiver correto, o exemplo verificará os membros **biBitCount** e **biCompression** da estrutura **VIDEOINFOHEADER** para verificar se o formato é RGB descompactado de 8 bits. Como este exemplo mostra, você deve coerção do


```C++
pbFormat
```



ponteiro para a estrutura correta, com base no tipo de formato. Sempre verifique o tipo de formato GUID (**formattype**) e o tamanho do bloco de formato (**cbFormat**) antes de lançar o ponteiro.

O exemplo também verifica se o número de entradas da paleta é compatível com a profundidade do bit e o bloco de formato é grande o suficiente para manter as entradas da paleta. Se todas essas informações estão corretas, o método retorna S \_ OK.

Próximo: [Etapa 3B. Implementar o método GetMediaType](step-3b--implement-the-getmediatype-method.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Escrevendo DirectShow filtros](writing-directshow-filters.md)
</dt> </dl>

 

 



