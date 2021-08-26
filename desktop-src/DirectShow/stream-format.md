---
description: Formato de fluxo
ms.assetid: 7ed095f2-b541-4b99-8afc-9acba58081cd
title: Formato de fluxo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a01ed1ac4501a2d8f081c12fef75baf15aaebd442fc182a116db1038c2a73523
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903986"
---
# <a name="stream-format"></a>Formato de fluxo

O MSDV e o driver UVC podem saída de dois formatos DV: áudio-vídeo intercalado ou somente vídeo. Áudio-vídeo intercalado é o formato original do dispositivo. O formato somente vídeo contém os mesmos dados, mas os exemplos são marcados como sem dados de áudio. O formato somente vídeo existe principalmente para compatibilidade com aplicativos que usam o Video para Windows. Para obter mais informações, [consulte Type-1 vs. Type-2 DV AVI Files](type-1-vs--type-2-dv-avi-files.md).

**MSDV Driver**

O driver MSDV tem dois pinos de saída. O primeiro pino de saída envia dados intercalados e o segundo pino de saída envia dados somente vídeo. Somente um pino de saída pode ser conectado por vez. Para selecionar um formato, conecte o pino de saída apropriado. Você pode usar a interface [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) no pino de saída para encontrar o formato.

**UVC Driver**

Ao contrário do driver MSDV, o driver UVC entrega os dois formatos do mesmo pin. O formato padrão é somente vídeo. Para selecionar o formato, use a interface **IAMStreamConfig** no pino de saída. Chame o **método GetStreamCaps** para enumerar os tipos de mídia no pino de saída. Para cada tipo de mídia, se o tipo principal corresponde ao formato desejado, chame **SetFormat** e passe esse tipo de mídia.



| Formatar                      | Tipo principal             |
|-----------------------------|------------------------|
| Áudio e vídeo intercalados | MEDIATYPE \_ intercalado |
| Somente vídeo                  | Vídeo \_ MEDIATYPE       |



 

A função a seguir define o formato com base no GUID do tipo principal.


```C++
HRESULT SetStreamFormat(IAMStreamConfig *pConfig, const GUID& majorType)
{
    if (pConfig == NULL)
    {
        return E_POINTER;
    }

    // Get the number of stream capabilities.
    int count = 0, size = 0;
    HRESULT hr = pConfig->GetNumberOfCapabilities(&count, &size);
    if (FAILED(hr))
    {
        return hr;
    }

    // Allocate memory for the stream capabilities structure.
    BYTE *pCaps = new BYTE[size];
    if (pCaps == NULL)
    {
        return E_OUTOFMEMORY;
    }
    
    // Enumerate the stream capabilities.
    bool bFoundType = false;
    for (int ix = 0; ix < count; ix++)
    {
        AM_MEDIA_TYPE *pmt;
        hr = pConfig->GetStreamCaps(ix, &pmt, pCaps);
        if (FAILED(hr))
        {
            break;
        }
        else if (pmt->majortype == majorType)
        {
            // This is the media type we want.
            bFoundType = true;
            hr = pConfig->SetFormat(pmt);
            DeleteMediaType(pmt);
            break;
        }
        DeleteMediaType(pmt);
    }
    delete [] pCaps;
    if (FAILED(hr))
    {
        return hr;
    }
    return bFoundType ? S_OK : E_FAIL;
}
```



O driver MSDV também dá suporte **a IAMStreamConfig,** para que você possa escrever código que funcione para ambos os tipos de dispositivo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Controlando uma dvcorder](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



