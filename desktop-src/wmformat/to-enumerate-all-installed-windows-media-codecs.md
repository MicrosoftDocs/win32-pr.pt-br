---
title: para enumerar todos os codecs de mídia do Windows instalados
description: para enumerar todos os codecs de mídia do Windows instalados
ms.assetid: 651c8624-0b66-4d0e-a25f-6c4b1a94e849
keywords:
- fluxos, enumerando os codecs de mídia instalados Windows
- codecs, enumerações
- fluxos, índices de codec
- codecs, índices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b63f58f94cf36e18fcbaa31bb9cff0dd8b5ab4717cc88e6f05657c7a2c72b429
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118699808"
---
# <a name="to-enumerate-all-installed-windows-media-codecs"></a>para enumerar todos os codecs de mídia do Windows instalados

As informações do codec interfaces usam índices de codec para identificar codecs individuais. Os codecs são indexados independentemente para áudio e vídeo. Dentro de um tipo de codec, os índices variam de 0, para um menor que o número de codecs desse tipo.

O código de exemplo a seguir mostra como obter o índice associado a cada codec. Para compilar esse código em seu aplicativo, inclua stdio. h.


```C++
HRESULT GetCodecNames(IWMCodecInfo3* pCodecInfo)
{
    HRESULT hr = S_OK;
    DWORD   cCodecs  = 0;
    WCHAR*  pwszCodecName  = NULL;
    DWORD   cchCodecName     = 0;
    
    // Retrieve the number of supported audio codecs on the system.
    hr = pCodecInfo->GetCodecInfoCount(WMMEDIATYPE_Audio, &cCodecs);

    if(SUCCEEDED(hr))
        printf("Number of audio codecs: %d\n\n", cCodecs);
    else
    {
        printf("Could not get the count of audio codecs.\n");
        return hr;
    }

    // Loop through all the audio codecs.
    for(DWORD dwCodecIndex = 0; dwCodecIndex < cCodecs; dwCodecIndex++)
    {
        // Get the codec name:
        // First, get the size of the name.
        hr = pCodecInfo->GetCodecName(WMMEDIATYPE_Audio, 
                                      dwCodecIndex, 
                                      NULL, 
                                      &cchCodecName);
        if(FAILED(hr))
        {
            printf("Could not get the size of the codec name.\n");
            return hr;
        }

        // Allocate a string of the appropriate size.
        pwszCodecName = new WCHAR[cchCodecName];
        if(pwszCodecName == NULL)
        {
            printf("Could not allocate memory.\n");
            return E_OUTOFMEMORY;
        }

        // Retrieve the codec name.
        hr = pCodecInfo->GetCodecName(WMMEDIATYPE_Audio, 
                                      dwCodecIndex, 
                                      pwszCodecName, 
                                      &cchCodecName);
        if(FAILED(hr))
        {
            delete[] pwszCodecName;
            printf("Could not get the codec name.\n");
            return hr;
        }

        // Print the codec name.
        printf("%d %S\n", dwCodecIndex, pwszCodecName);

        // Clean up for the next iteration.
        delete[] pwszCodecName;
        pwszCodecName = NULL;
        cchCodecName  = 0;
    }

    // Retrieve the number of supported video codecs on the system.
    hr = pCodecInfo->GetCodecInfoCount(WMMEDIATYPE_Video, &cCodecs);

    if(SUCCEEDED(hr))
        printf("\n\nNumber of video codecs: %d.\n\n", cCodecs);
    else
    {
        printf("Could not get the count of video codecs.\n");
        return hr;
    }

    // Loop through all the video codecs.
    for(dwCodecIndex = 0; dwCodecIndex < cCodecs; dwCodecIndex++)
    {
        // Get the codec name:
        // First, get the size of the name.
        hr = pCodecInfo->GetCodecName(WMMEDIATYPE_Video, 
                                      dwCodecIndex, 
                                      NULL, 
                                      &cchCodecName);
        if(FAILED(hr))
        {
            printf("Could not get the size of the codec name.\n");
            return hr;
        }

        // Allocate a string of the appropriate size.
        pwszCodecName = new WCHAR[cchCodecName];
        if(pwszCodecName == NULL)
        {
            printf("Could not allocate memory.\n");
            return E_OUTOFMEMORY;
        }

        // Retrieve the codec name.
        hr = pCodecInfo->GetCodecName(WMMEDIATYPE_Video, 
                                      dwCodecIndex, 
                                      pwszCodecName, 
                                      &cchCodecName);
        if(FAILED(hr))
        {
            printf("Could not get the codec name.\n");
            return hr;
        }

        // Print the codec name.
        printf("%d %S\n", dwCodecIndex, pwszCodecName);

        delete[] pwszCodecName;
        pwszCodecName = NULL;
        cchCodecName  = 0;
    }
    return S_OK;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Obtendo informações de configuração de fluxo de codecs**](getting-stream-configuration-information-from-codecs.md)
</dt> </dl>

 

 




