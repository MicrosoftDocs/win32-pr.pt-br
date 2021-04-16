---
description: Formato do fluxo
ms.assetid: 7ed095f2-b541-4b99-8afc-9acba58081cd
title: Formato do fluxo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75413c28f0871db0168e27685de49fd35b682224
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105779227"
---
# <a name="stream-format"></a>Formato do fluxo

O driver MSDV e o UVC podem produzir dois formatos de DV: áudio Intercalado ou vídeo somente. Áudio Intercalado-vídeo é o formato original do dispositivo. O formato somente de vídeo contém os mesmos dados, mas os exemplos são marcados como sem dados de áudio. O formato somente vídeo existe principalmente para compatibilidade com aplicativos que usam vídeo para Windows. Para obter mais informações, consulte [tipos-1 vs. tipo-2 DV AVI files](type-1-vs--type-2-dv-avi-files.md).

**Driver MSDV**

O driver MSDV tem dois pinos de saída. O primeiro pino de saída envia dados intercalados e o segundo PIN de saída envia dados somente de vídeo. Somente um PIN de saída pode ser conectado por vez. Para selecionar um formato, conecte o PIN de saída apropriado. Você pode usar a interface [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) no pino de saída para localizar o formato.

**Driver UVC**

Ao contrário do driver MSDV, o driver UVC fornece os dois formatos do mesmo PIN. O formato padrão é somente vídeo. Para selecionar o formato, use a interface **IAMStreamConfig** no pino de saída. Chame o método **GetStreamCaps** para enumerar os tipos de mídia no pino de saída. Para cada tipo de mídia, se o tipo principal corresponder ao formato desejado, chame **SetFormat** e transmita esse tipo de mídia.



| Formatar                      | Tipo principal             |
|-----------------------------|------------------------|
| Áudio e vídeo intercalados | MEDIATYPE \_ intercalado |
| Somente vídeo                  | Vídeo de MEDIATYPE \_       |



 

A função a seguir define o formato com base no GUID de tipo principal.


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



O driver MSDV também dá suporte a **IAMStreamConfig**, para que você possa escrever código que funcione para ambos os tipos de dispositivo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Controlando uma camcorder DV](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



