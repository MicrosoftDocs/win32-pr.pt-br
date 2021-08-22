---
description: Etapa 3B.
ms.assetid: 0ec57083-b192-404a-938f-bc6bb1cf0ddb
title: Etapa 3B. Implementar o método GetMediaType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f386c16e3166f910e8221d139af519363d1b49279a412603e0cfddfa41773ede
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583106"
---
# <a name="step-3b-implement-the-getmediatype-method"></a>Etapa 3B. Implementar o método GetMediaType

Esta é a etapa 3B do tutorial [escrevendo filtros de transformação](writing-transform-filters.md).

> [!Note]  
> Esta etapa não é necessária para filtros que derivam de **CTransInPlaceFilter**.

 

O método [**CTransformFilter:: GetMediaType**](ctransformfilter-getmediatype.md) retorna um dos tipos de saída preferenciais do filtro, referenciado pelo número de índice. Esse método nunca é chamado a menos que o PIN de entrada do filtro já esteja conectado. Portanto, você pode usar o tipo de mídia da conexão upstream para determinar os tipos de saída preferenciais.

Um codificador normalmente oferece um único tipo preferencial, representando o formato de destino. Os decodificadores geralmente dão suporte a uma variedade de formatos de saída e os oferecem em ordem de qualidade ou eficiência decrescente. Por exemplo, a lista pode ser UYVY, Y211, RGB-24, RGB-565, RGB-555 e RGB-8, nessa ordem. Filtros de efeito podem exigir uma correspondência exata entre o formato de saída e o formato de entrada.

O exemplo a seguir retorna um único tipo de saída, que é construído modificando o tipo de entrada para especificar a compactação RLE8:


```C++
HRESULT CRleFilter::GetMediaType(int iPosition, CMediaType *pMediaType)
{
    ASSERT(m_pInput->IsConnected());
    if (iPosition < 0)
    {
        return E_INVALIDARG;
    }
    if (iPosition == 0)
    {
        HRESULT hr = m_pInput->ConnectionMediaType(pMediaType);
        if (FAILED(hr))
        {
            return hr;
        }
        FOURCCMap fccMap = FCC('MRLE'); 
        pMediaType->subtype = static_cast<GUID>(fccMap);
        pMediaType->SetVariableSize();
        pMediaType->SetTemporalCompression(FALSE);

        ASSERT(pMediaType->formattype == FORMAT_VideoInfo);
        VIDEOINFOHEADER *pVih =
            reinterpret_cast<VIDEOINFOHEADER*>(pMediaType->pbFormat);
        pVih->bmiHeader.biCompression = BI_RLE8;
        pVih->bmiHeader.biSizeImage = DIBSIZE(pVih->bmiHeader); 
        return S_OK;
    }
    // else
    return VFW_S_NO_MORE_ITEMS;
}
```



Neste exemplo, o método chama [**IPin:: ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) para obter o tipo de entrada do pino de entrada. Em seguida, ele altera alguns dos campos para indicar o formato de compactação, da seguinte maneira:

-   Ele atribui um novo GUID de subtipo, que é construído a partir do código FOURCC ' MRLE ', usando a classe [**FOURCCMap**](fourccmap.md) .
-   Ele chama o método [**CMediaType:: Setvariables**](cmediatype-setvariablesize.md) , que define o sinalizador **bFixedSizeSamples** como **false** e o membro **lSampleSize** como zero, indicando exemplos de tamanho variável.
-   Ele chama o método [**CMediaType:: SetTemporalCompression**](cmediatype-settemporalcompression.md) com o valor **false**, indicando que cada quadro é um quadro-chave. (Esse campo é apenas informativo, portanto, você pode ignorá-lo com segurança.)
-   Ele define o campo de **Bicompactação** como bi \_ RLE8.
-   Ele define o campo **biSizeImage** para o tamanho da imagem.

Em seguida: [etapa 3C. implemente o método CheckTransform](step-3c--implement-the-checktransform-method.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[gravando filtros de DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



