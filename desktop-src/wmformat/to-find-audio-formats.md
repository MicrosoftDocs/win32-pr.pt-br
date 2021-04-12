---
title: Para localizar formatos de áudio
description: Para localizar formatos de áudio
ms.assetid: f2001ed5-f07d-45a5-a566-45697024870e
keywords:
- fluxos, localizando formatos de áudio
- fluxos de áudio, localizando formatos de áudio
- fluxos, formatos de áudio
- fluxos de áudio, formatos de áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d85897d4d76a3bdb1e99902eb4f52336a3ad0874
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294265"
---
# <a name="to-find-audio-formats"></a><span data-ttu-id="348c3-107">Para localizar formatos de áudio</span><span class="sxs-lookup"><span data-stu-id="348c3-107">To Find Audio Formats</span></span>

<span data-ttu-id="348c3-108">O código de exemplo a seguir demonstra como localizar um formato de áudio que corresponde aos critérios especificados.</span><span class="sxs-lookup"><span data-stu-id="348c3-108">The following example code demonstrates how to find an audio format that matches criteria you specify.</span></span> <span data-ttu-id="348c3-109">A função **FindAudioFormat** aceita um ponteiro para uma estrutura [**WAVEFORMATEX**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85)) que contém o número de canais, bits por amostra e taxa de amostragem que você deseja usar.</span><span class="sxs-lookup"><span data-stu-id="348c3-109">The **FindAudioFormat** function accepts a pointer to a [**WAVEFORMATEX**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85)) structure that contains the number of channels, bits per sample, and sample rate that you want to use.</span></span> <span data-ttu-id="348c3-110">A função localiza o formato que corresponde a esses requisitos e tem a taxa de bits mais alta que não excede o parâmetro *dwMaxRate* .</span><span class="sxs-lookup"><span data-stu-id="348c3-110">The function finds the format that matches those requirements and has the highest bit rate that does not exceed the *dwMaxRate* parameter.</span></span> <span data-ttu-id="348c3-111">Se você definir *fAVSync* como **true**, a função só validará os formatos que podem ser sincronizados com o vídeo.</span><span class="sxs-lookup"><span data-stu-id="348c3-111">If you set *fAVSync* to **TRUE**, the function only validates formats that can be synchronized with video.</span></span> <span data-ttu-id="348c3-112">Para simplificar, essa função funciona apenas com formatos de CBR de 1 passagem.</span><span class="sxs-lookup"><span data-stu-id="348c3-112">For simplicity, this function only works with 1-pass CBR formats.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="348c3-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="348c3-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="348c3-114">**Configurando fluxos de áudio**</span><span class="sxs-lookup"><span data-stu-id="348c3-114">**Configuring Audio Streams**</span></span>](configuring-audio-streams.md)
</dt> <dt>

[<span data-ttu-id="348c3-115">**Para enumerar formatos de codec**</span><span class="sxs-lookup"><span data-stu-id="348c3-115">**To Enumerate Codec Formats**</span></span>](to-enumerate-codec-formats.md)
</dt> </dl>

 

 