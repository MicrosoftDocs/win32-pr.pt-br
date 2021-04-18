---
title: Para enumerar todos os codecs de mídia do Windows instalados
description: Para enumerar todos os codecs de mídia do Windows instalados
ms.assetid: 651c8624-0b66-4d0e-a25f-6c4b1a94e849
keywords:
- fluxos, enumerando os codecs de mídia do Windows instalados
- codecs, enumerações
- fluxos, índices de codec
- codecs, índices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6db9a35913dde13f563ee57d54ee5e7de87d82cc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105780379"
---
# <a name="to-enumerate-all-installed-windows-media-codecs"></a><span data-ttu-id="7d558-107">Para enumerar todos os codecs de mídia do Windows instalados</span><span class="sxs-lookup"><span data-stu-id="7d558-107">To Enumerate All Installed Windows Media Codecs</span></span>

<span data-ttu-id="7d558-108">As informações do codec interfaces usam índices de codec para identificar codecs individuais.</span><span class="sxs-lookup"><span data-stu-id="7d558-108">The codec information interfaces all use codec indexes to identify individual codecs.</span></span> <span data-ttu-id="7d558-109">Os codecs são indexados independentemente para áudio e vídeo.</span><span class="sxs-lookup"><span data-stu-id="7d558-109">Codecs are indexed independently for audio and for video.</span></span> <span data-ttu-id="7d558-110">Dentro de um tipo de codec, os índices variam de 0, para um menor que o número de codecs desse tipo.</span><span class="sxs-lookup"><span data-stu-id="7d558-110">Within one type of codec, indexes range from 0, to one less than the number of codecs of that type.</span></span>

<span data-ttu-id="7d558-111">O código de exemplo a seguir mostra como obter o índice associado a cada codec.</span><span class="sxs-lookup"><span data-stu-id="7d558-111">The following example code shows how to get the index associated with each codec.</span></span> <span data-ttu-id="7d558-112">Para compilar esse código em seu aplicativo, inclua stdio. h.</span><span class="sxs-lookup"><span data-stu-id="7d558-112">To compile this code in your application, include stdio.h.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="7d558-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7d558-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d558-114">**Obtendo informações de configuração de fluxo de codecs**</span><span class="sxs-lookup"><span data-stu-id="7d558-114">**Getting Stream Configuration Information from Codecs**</span></span>](getting-stream-configuration-information-from-codecs.md)
</dt> </dl>

 

 




