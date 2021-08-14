---
title: Para encontrar formatos de áudio
description: Para encontrar formatos de áudio
ms.assetid: f2001ed5-f07d-45a5-a566-45697024870e
keywords:
- fluxos, localizar formatos de áudio
- fluxos de áudio, localizar formatos de áudio
- fluxos, formatos de áudio
- fluxos de áudio, formatos de áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c596c8efc1fc5315ad68bad51676888823ac4b3518232ec948ce38b2fb77075
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118196502"
---
# <a name="to-find-audio-formats"></a>Para encontrar formatos de áudio

O código de exemplo a seguir demonstra como encontrar um formato de áudio que corresponde aos critérios especificados. A **função FindAudioFormat** aceita um ponteiro para uma estrutura [**WAVEFORMATEX**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85)) que contém o número de canais, bits por exemplo e taxa de amostra que você deseja usar. A função localiza o formato que corresponde a esses requisitos e tem a taxa de bits mais alta que não excede o *parâmetro dwMaxRate.* Se você definir *fAVSync como* **TRUE,** a função validará apenas os formatos que podem ser sincronizados com o vídeo. Para simplificar, essa função funciona apenas com formatos CBR de 1 passagem.


```C++
// This constant is used to determine if an index was found.
#define INVALID_INDEX 0xFFFF

// The FindAudioFormat function finds a compressed audio format that
//  matches the criteria defined by the input parameters.
HRESULT FindAudioFormat(GUID SubType,
                        WAVEFORMATEX* pWaveLimits,
                        DWORD dwMaxRate,
                        BOOL fAVSync,
                        IWMStreamConfig** ppStreamConfig)
{
    HRESULT hr = S_OK;

    IWMProfileManager* pProfileMgr   = NULL;
    IWMCodecInfo3*     pCodecInfo    = NULL;
    IWMStreamConfig*   pStreamConfig = NULL;
    IWMStreamConfig*   pBestMatch    = NULL;
    IWMMediaProps*     pProps        = NULL;
    WM_MEDIA_TYPE*     pType         = NULL;
    DWORD              cbType        = 0;
    WAVEFORMATEX*      pWave         = NULL;

    DWORD index = 0;
    DWORD cEntries = 0;
    DWORD dwBestRate = 0;
    DWORD PacketsPerSecond = 0;

    // This value is beyond the codec indexes 
    // and will be used to verify success.
    DWORD CodecIndex = INVALID_INDEX; 

    // Instantiate a profile manager object.
    hr = WMCreateProfileManager(&pProfileMgr);
    GOTO_EXIT_IF_FAILED(hr);

    // Get the codec information interface.
    hr = pProfileMgr->QueryInterface(IID_IWMCodecInfo3, (void**)&pCodecInfo);
    GOTO_EXIT_IF_FAILED(hr);

    // Get the number of audio codecs for which there is information.
    hr = pCodecInfo->GetCodecInfoCount(WMMEDIATYPE_Audio, &cEntries);
    GOTO_EXIT_IF_FAILED(hr);

    // Find the index of the codec corresponding to the requested subytpe.
    for(index = 0; index < cEntries; index++)
    {
        // Get the first format for each codec. 
        hr = pCodecInfo->GetCodecFormat(WMMEDIATYPE_Audio, index, 0, &pStreamConfig);
        GOTO_EXIT_IF_FAILED(hr);

        // Get the media properties interface.
        hr = pStreamConfig->QueryInterface(IID_IWMMediaProps, (void**)&pProps);
        GOTO_EXIT_IF_FAILED(hr);

        // Get the size required for the media type structure.
        hr = pProps->GetMediaType(NULL, &cbType);
        GOTO_EXIT_IF_FAILED(hr);

        // Allocate memory for the media type structure.
        pType = (WM_MEDIA_TYPE*) new BYTE[cbType];
        if(pType == NULL)
        {
            hr = E_OUTOFMEMORY;
            goto Exit;
        }

        // Get the media type structure.
        hr = pProps->GetMediaType(pType, &cbType);
        GOTO_EXIT_IF_FAILED(hr);

        // Check this codec against the one requested.
        if(pType->subtype == SubType)
            CodecIndex = index;
        
        // The subtypes did not match. Clean up for next iteration.
        SAFE_RELEASE(pStreamConfig);
        SAFE_RELEASE(pProps);
        SAFE_ARRAY_DELETE(pType);

        // Break now if needed. Placing the break here avoids having to
        //  release or delete both inside and outside of the loop.
        if(CodecIndex != INVALID_INDEX)
            break;
    } // for index

    // The subtype is invalid if no codec was found that matches it.
    if(CodecIndex == INVALID_INDEX)
    {
        hr = E_INVALIDARG;
        goto Exit;
    }

    // Get the number of formats supported for the codec.
    hr = pCodecInfo->GetCodecFormatCount(WMMEDIATYPE_Audio, 
                                         CodecIndex, 
                                         &cEntries);
    GOTO_EXIT_IF_FAILED(hr);

    // Loop through the formats for the codec, looking for matches.
    for(index = 0; index < cEntries; index++)
    {
        // Get the next format.
        hr = pCodecInfo->GetCodecFormat(WMMEDIATYPE_Audio, 
                                        CodecIndex, 
                                        index, 
                                        &pStreamConfig);
        GOTO_EXIT_IF_FAILED(hr);

        // Get the media properties interface.
        hr = pStreamConfig->QueryInterface(IID_IWMMediaProps, (void**)&pProps);
        GOTO_EXIT_IF_FAILED(hr);

        // Get the size required for the media type structure.
        hr = pProps->GetMediaType(NULL, &cbType);
        GOTO_EXIT_IF_FAILED(hr);

        // Allocate memory for the media type structure.
        pType = (WM_MEDIA_TYPE*) new BYTE[cbType];
        if(pType == NULL)
        {
            hr = E_OUTOFMEMORY;
            goto Exit;
        }

        // Get the media type structure.
        hr = pProps->GetMediaType(pType, &cbType);
        GOTO_EXIT_IF_FAILED(hr);

        // Check that the format data is present.
        if(pType->cbFormat >= sizeof(WAVEFORMATEX))
            pWave = (WAVEFORMATEX*)pType->pbFormat;
        else
        {
            // The returned media type should always have an attached 
            //  WAVEFORMATEX structure.  
            hr = E_UNEXPECTED;
            goto Exit;
        }

        // Start checking data.

        // Do not check particulars unless the bit rate is in range.
        if((pWave->nAvgBytesPerSec * 8) > dwBestRate &&
           (pWave->nAvgBytesPerSec * 8) <= dwMaxRate)
        {
            // Check the limits.
            if((pWave->nChannels == pWaveLimits->nChannels) &&
               (pWave->wBitsPerSample == pWaveLimits->wBitsPerSample) &&
               (pWave->nSamplesPerSec == pWaveLimits->nSamplesPerSec))
            {
                // If audio/video synchronization requested, check the number
                //  of packets per second (Bps / BlockAlign). The bit rate is
                //  greater than 3200 bps, this value must be 5. 
                //  Otherwise this value is 3.
                // This is an ASF requirement.
                if(fAVSync)
                {
                    if((pWave->nAvgBytesPerSec / pWave->nBlockAlign) >= 
                           ((pWave->nAvgBytesPerSec >= 4000) ? 5.0 : 3.0))
                    {
                        // Release the previous best match.
                        SAFE_RELEASE(pBestMatch);

                        // Set this stream configuration as the new best match.
                        pBestMatch = pStreamConfig;
                        pStreamConfig->AddRef();

                        // Set the best bit rate.
                        dwBestRate = (pWave->nAvgBytesPerSec * 8);

                    }
                } // if fAVSync
                else
                {
                    // Release the previous best match.
                    SAFE_RELEASE(pBestMatch);

                    // Set this stream configuration as the new best match.
                    pBestMatch = pStreamConfig;
                    pStreamConfig->AddRef();

                    // Set the best bit rate.
                    dwBestRate = (pWave->nAvgBytesPerSec * 8);
                } // else
            } // if matching limits
        } // if valid bit rate

        // Clean up for next iteration.
        SAFE_RELEASE(pStreamConfig);
        SAFE_RELEASE(pProps);
        pWave = NULL;
        SAFE_ARRAY_DELETE(pType);
    } // for index

    // If no match was found, the arguments were not valid for the codec.
    if(pBestMatch == NULL)
    {
        hr = E_INVALIDARG;
        goto Exit;
    }

    // Set the pointer to the stream configuration.
    *ppStreamConfig = pBestMatch;
    pBestMatch = NULL;

Exit:
    SAFE_RELEASE(pProfileMgr);
    SAFE_RELEASE(pCodecInfo);
    SAFE_RELEASE(pStreamConfig);
    SAFE_RELEASE(pBestMatch);
    SAFE_RELEASE(pProps);
    SAFE_ARRAY_DELETE(pType);

    return hr;        
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Configurando o Fluxos**](configuring-audio-streams.md)
</dt> <dt>

[**Para enumerar formatos codec**](to-enumerate-codec-formats.md)
</dt> </dl>

 

 