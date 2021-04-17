---
description: Etapa 3A.
ms.assetid: 774fcb12-8928-4667-8ef6-dce86717cc29
title: Etapa 3A. Implementar o método CheckInputType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5eb6ff440838d7a4b65b586e5dba963ff254eef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105770062"
---
# <a name="step-3a-implement-the-checkinputtype-method"></a>Etapa 3A. Implementar o método CheckInputType

Esta é a etapa 3A do tutorial [escrevendo filtros de transformação](writing-transform-filters.md).

O método [**CTransformFilter:: CheckInputType**](ctransformfilter-checkinputtype.md) é chamado quando o filtro upstream propõe um tipo de mídia para o filtro de transformação. Esse método usa um ponteiro para um objeto [**CMediaType**](cmediatype.md) , que é um wrapper fino para a estrutura do [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) . Nesse método, você deve examinar todos os campos relevantes da estrutura **do \_ \_ tipo de mídia am** , incluindo os campos no bloco de formato. Você pode usar os métodos de acessadores definidos em **CMediaType** ou fazer referência diretamente aos membros da estrutura. Se qualquer campo não for válido, retornará VFW \_ E \_ tipo \_ não \_ aceito. Se o tipo de mídia inteiro for válido, retorne S \_ OK.

Por exemplo, no filtro do codificador RLE, o tipo de entrada deve ser vídeo RGB descompactado de 8 ou 4 bits. Não há motivo para dar suporte a outros formatos de entrada, como o RGB de 16 ou 24 bits, porque o filtro teria que convertê-los em uma profundidade de bits inferior, e o DirectShow já fornece um filtro de [conversor de espaço de cor](color-space-converter-filter.md) para essa finalidade. O exemplo a seguir pressupõe que o codificador dá suporte a vídeo de 8 bits, mas não vídeo de 4 bits:


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



Neste exemplo, o método primeiro verifica o tipo principal e subtipo. Em seguida, ele verifica o tipo de formato para verificar se o bloco de formato é uma estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) . O filtro também pode dar suporte a [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2), mas, nesse caso, não haveria nenhum benefício real. A estrutura **VIDEOINFOHEADER2** adiciona suporte para entrelaçamento e pixels não quadrados, que provavelmente não serão relevantes no vídeo de 8 bits.

Se o tipo de formato estiver correto, o exemplo verificará os membros **biBitCount** e **biCompression** da estrutura **VIDEOINFOHEADER** , para verificar se o formato é RGB não compactado de 8 bits. Como mostra este exemplo, você deve forçar o


```C++
pbFormat
```



Ponteiro para a estrutura correta, com base no tipo de formato. Sempre verifique o tipo de formato GUID (**formatType**) e o tamanho do bloco de formato (**cbFormat**) antes de converter o ponteiro.

O exemplo também verifica se o número de entradas da paleta é compatível com a profundidade de bits e o bloco de formato é grande o suficiente para manter as entradas da paleta. Se todas essas informações estiverem corretas, o método retornará S \_ OK.

Em seguida: [etapa 3B. implemente o método GetMediaType](step-3b--implement-the-getmediatype-method.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gravando filtros do DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



