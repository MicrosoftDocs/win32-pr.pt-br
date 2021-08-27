---
description: Enumerando tipos de mídia
ms.assetid: 7878885f-c285-4744-8eab-445678dcfd49
title: Enumerando tipos de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4e2f063fc243d081b930a1bf47f85904dfbc2fc7eef00fb595d5f0fb3a451ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102796"
---
# <a name="enumerating-media-types"></a>Enumerando tipos de mídia

Os Pins dão suporte ao método [**IPin:: EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) , que enumera os tipos de mídia preferenciais de um PIN. Ele retorna um ponteiro para a interface [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) . O método [**IEnumMediaTypes:: Next**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-next) recupera ponteiros para as estruturas do [**\_ \_ tipo mídia**](/windows/win32/api/strmif/ns-strmif-am_media_type) que descrevem os tipos de mídia.

o enumerador de tipo de mídia existe principalmente para ajudar o filtro Graph Manager a fazer conexões inteligentes e seus aplicativos provavelmente não o usarão. Um PIN não retorna necessariamente nenhum tipo de mídia preferencial. Além disso, os tipos de mídia que ele retorna podem depender do status da conexão do filtro. Por exemplo, o PIN de saída de um filtro pode retornar um conjunto diferente de tipos de mídia, dependendo de qual tipo de mídia foi definido para o PIN de entrada do filtro.

O exemplo a seguir localiza um tipo de mídia preferencial que corresponde a um tipo principal, subtipo ou tipo de formato especificado.


```C++
// Given a pin, find a preferred media type 
//
// pPin         Pointer to the pin.
// majorType    Preferred major type (GUID_NULL = don't care).
// subType      Preferred subtype (GUID_NULL = don't care).
// formatType   Preferred format type (GUID_NULL = don't care).
// ppmt         Receives a pointer to the media type. Can be NULL.
//
// Note: If you want to check whether a pin supports a desired media type,
//       but do not need the format details, set ppmt to NULL.
//
//       If ppmt is not NULL and the method succeeds, the caller must
//       delete the media type, including the format block. 

HRESULT GetPinMediaType(
    IPin *pPin,             // pointer to the pin
    REFGUID majorType,      // desired major type, or GUID_NULL = don't care
    REFGUID subType,        // desired subtype, or GUID_NULL = don't care
    REFGUID formatType,     // desired format type, of GUID_NULL = don't care
    AM_MEDIA_TYPE **ppmt    // Receives a pointer to the media type. (Can be NULL)
    )
{
    *ppmt = NULL;

    IEnumMediaTypes *pEnum = NULL;
    AM_MEDIA_TYPE *pmt = NULL;
    BOOL bFound = FALSE;
    
    HRESULT hr = pPin->EnumMediaTypes(&pEnum);
    if (FAILED(hr))
    {
        return hr;
    }

    while (hr = pEnum->Next(1, &pmt, NULL), hr == S_OK)
    {
        if ((majorType == GUID_NULL) || (majorType == pmt->majortype))
        {
            if ((subType == GUID_NULL) || (subType == pmt->subtype))
            {
                if ((formatType == GUID_NULL) || 
                    (formatType == pmt->formattype))
                {
                    // Found a match. 
                    if (ppmt)
                    {
                        *ppmt = pmt;  // Return it to the caller
                    }
                    else
                    {
                        _DeleteMediaType(pmt);
                    }
                    bFound = TRUE;
                    break;
                }
            }
        }
        _DeleteMediaType(pmt);
    }

    SafeRelease(&pEnum);
    if (SUCCEEDED(hr))
    {
        if (!bFound)
        {
            hr = VFW_E_NOT_FOUND;
        }
    }
    return hr;
}
```



> [!Note]  
> Este exemplo usa a função [SafeRelease](/windows/desktop/medfound/saferelease) para liberar ponteiros de interface.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Enumerando objetos em um filtro Graph](enumerating-objects-in-a-filter-graph.md)
</dt> <dt>

[**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes)
</dt> </dl>

 

 
