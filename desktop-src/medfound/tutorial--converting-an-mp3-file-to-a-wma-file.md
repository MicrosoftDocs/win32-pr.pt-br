---
description: Este tutorial mostra como usar a API de transcodificação para codificar um arquivo de áudio do Windows Media (WMA).
ms.assetid: 2397ca78-edb5-4756-bd07-00529db28f76
title: 'Tutorial: codificando um arquivo WMA'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f491a9d460771dae91a49ab42982fbe97b24c42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781378"
---
# <a name="tutorial-encoding-a-wma-file"></a>Tutorial: codificando um arquivo WMA

Este tutorial mostra como usar a [API de transcodificação](transcode-api.md) para codificar um arquivo de áudio do Windows Media (WMA).

Este tutorial reutiliza a maior parte do código do tutorial [codificando um arquivo MP4](tutorial--encoding-an-mp4-file-.md), portanto, você deve ler o tutorial primeiro. O único código que difere é a função `CreateTranscodeProfile` , que cria o perfil transcodificar.

## <a name="create-the-transcode-profile"></a>Criar o perfil transcodificar

Um *perfil de transcodificação* descreve os parâmetros de codificação e o contêiner de arquivo. Para o WMA, o contêiner de arquivo é um arquivo ASF (Advanced Streaming Format). O arquivo ASF contém um fluxo de áudio, que é codificado usando o [**codificador de áudio do Windows Media**](windowsmediaaudioencoder.md).

Para criar a topologia de transcodificação, crie o perfil transcodificar e especifique os parâmetros para o fluxo de áudio e o contêiner. Em seguida, crie a topologia especificando a fonte de entrada, a URL de saída e o perfil de transcodificação.

Para criar o perfil, execute as etapas a seguir.

1.  Chame a função [**MFCreateTranscodeProfile**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) para criar um perfil de transcodificação vazio.
2.  Chame [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) para obter uma lista de tipos de mídia de áudio do codificador. Essa função retorna um ponteiro [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) que representa uma coleção de ponteiros [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) .
3.  Escolha o tipo de mídia de áudio que corresponde aos seus requisitos de transcodificação e copie os atributos para um repositório de atributos. Para este tutorial, o primeiro tipo de mídia na lista é usado.
    -   Chame [**IMFCollection:: GetElement**](/windows/desktop/api/mfobjects/nf-mfobjects-imfcollection-getelement) para selecionar um tipo de mídia de áudio na lista.
    -   Consulte o tipo de mídia para obter um ponteiro para a interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) do repositório de atributos do tipo de mídia.
    -   Chame [**IMFAttributes:: GetCount**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getcount) para obter o número de atributos contidos no tipo de mídia.
    -   Chame [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) para criar um novo repositório de atributos.
    -   Chame [**IMFAttributes:: CopyAllItems**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-copyallitems) para copiar os atributos do tipo de mídia para o novo repositório de atributos.
4.  Chame [**IMFTranscodeProfile:: Setaudioattributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes) para definir os atributos para o fluxo de áudio.
5.  Chame [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) para criar um repositório de atributos para os atributos de nível de contêiner.
6.  Defina o [atributo \_ \_ ContainerType de transcodificar MF](mf-transcode-containertype.md) como **MFTranscodeContainerType \_ ASF**, que especifica um contêiner de arquivo asf.
7.  Chame [**IMFTranscodeProfile:: Setcontêinerattributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes) para definir os atributos de nível de contêiner no perfil.


```C++
template <class Q>
HRESULT GetCollectionObject(IMFCollection *pCollection, DWORD index, Q **ppObj)
{
    IUnknown *pUnk;
    HRESULT hr = pCollection->GetElement(index, &pUnk);
    if (SUCCEEDED(hr))
    {
        hr = pUnk->QueryInterface(IID_PPV_ARGS(ppObj));
        pUnk->Release();
    }
    return hr;
}

HRESULT CreateTranscodeProfile(IMFTranscodeProfile **ppProfile)
{
    IMFTranscodeProfile *pProfile = NULL;     // Transcode profile.
    IMFCollection   *pAvailableTypes = NULL;  // List of audio media types.
    IMFMediaType    *pAudioType = NULL;       // Audio media type.
    IMFAttributes   *pAudioAttrs = NULL;      // Copy of the audio media type.
    IMFAttributes   *pContainer = NULL;       // Container attributes.

    DWORD dwMTCount = 0;
    
    // Create an empty transcode profile.
    HRESULT hr = MFCreateTranscodeProfile(&pProfile);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get output media types for the Windows Media audio encoder.

    // Enumerate all codecs except for codecs with field-of-use restrictions.
    // Sort the results.

    DWORD dwFlags = 
        (MFT_ENUM_FLAG_ALL & (~MFT_ENUM_FLAG_FIELDOFUSE)) | 
        MFT_ENUM_FLAG_SORTANDFILTER;

    hr = MFTranscodeGetAudioOutputAvailableTypes(MFAudioFormat_WMAudioV9, 
        dwFlags, NULL, &pAvailableTypes);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pAvailableTypes->GetElementCount(&dwMTCount);
    if (FAILED(hr))
    {
        goto done;
    }
    if (dwMTCount == 0)
    {
        hr = E_FAIL;
        goto done;
    }

    // Get the first audio type in the collection and make a copy.
    hr = GetCollectionObject(pAvailableTypes, 0, &pAudioType);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFCreateAttributes(&pAudioAttrs, 0);       
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pAudioType->CopyAllItems(pAudioAttrs);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the audio attributes on the profile.
    hr = pProfile->SetAudioAttributes(pAudioAttrs);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the container attributes.
    hr = MFCreateAttributes(&pContainer, 1);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pContainer->SetGUID(MF_TRANSCODE_CONTAINERTYPE, MFTranscodeContainerType_ASF);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pProfile->SetContainerAttributes(pContainer);
    if (FAILED(hr))
    {
        goto done;
    }

    *ppProfile = pProfile;
    (*ppProfile)->AddRef();

done:
    SafeRelease(&pProfile);
    SafeRelease(&pAvailableTypes);
    SafeRelease(&pAudioType);
    SafeRelease(&pAudioAttrs);
    SafeRelease(&pContainer);
    return hr;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[API de transcodificação](transcode-api.md)
</dt> </dl>

 

 



