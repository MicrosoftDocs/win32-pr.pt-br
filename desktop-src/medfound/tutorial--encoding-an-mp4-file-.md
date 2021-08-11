---
description: Este tutorial mostra como usar a API transcódigo para codificar um arquivo MP4 usando H.264 para o fluxo de vídeo e o AAC para o fluxo de áudio.
ms.assetid: 60873aa6-46ec-4a73-94b9-0d8ac602f850
title: 'Tutorial: Codificando um arquivo MP4'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 242777f04015f5444be5e0d8424ca06fc4b95cd84ca88c2b997d7b7466c734af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118237619"
---
# <a name="tutorial-encoding-an-mp4-file"></a>Tutorial: Codificando um arquivo MP4

Este tutorial mostra como usar a [API transcódigo](transcode-api.md) para codificar um arquivo MP4 usando H.264 para o fluxo de vídeo e o AAC para o fluxo de áudio.

-   [Arquivos de biblioteca e de headers](#headers-and-library-files)
-   [Definir os perfis de codificação](#define-the-encoding-profiles)
-   [Gravar a função wmain](#write-the-wmain-function)
-   [Codificar o arquivo](#encode-the-file)
    -   [Criar a fonte de mídia](#create-the-media-source)
    -   [Obter a duração da origem](#get-the-source-duration)
    -   [Criar o perfil transcódigo](#create-the-transcode-profile)
    -   [Executar a sessão de codificação](#run-the-encoding-session)
-   [Auxiliar de Sessão de Mídia](#media-session-helper)
-   [Tópicos relacionados](#related-topics)

## <a name="headers-and-library-files"></a>Arquivos de biblioteca e de headers

Inclua os seguintes arquivos de header.


```C++
#include <new>
#include <iostream>
#include <windows.h>
#include <mfapi.h>
#include <Mfidl.h>
#include <shlwapi.h>
```



Vincule os seguintes arquivos de biblioteca.


```C++
#pragma comment(lib, "mfplat")
#pragma comment(lib, "mf")
#pragma comment(lib, "mfuuid")
#pragma comment(lib, "shlwapi")
```



## <a name="define-the-encoding-profiles"></a>Definir os perfis de codificação

Uma abordagem para codificação é definir uma lista de perfis de codificação de destino conhecidos com antecedência. Para este tutorial, fazemos uma abordagem relativamente simples e armazenamos uma lista de formatos de codificação para vídeo H.264 e áudio AAC.

Para H.264, os atributos de formato mais importantes são o perfil H.264, a taxa de quadros, o tamanho do quadro e a taxa de bits codificada. A matriz a seguir contém uma lista de formatos de codificação H.264.


```C++
struct H264ProfileInfo
{
    UINT32  profile;
    MFRatio fps;
    MFRatio frame_size;
    UINT32  bitrate;
};

H264ProfileInfo h264_profiles[] = 
{
    { eAVEncH264VProfile_Base, { 15, 1 },       { 176, 144 },   128000 },
    { eAVEncH264VProfile_Base, { 15, 1 },       { 352, 288 },   384000 },
    { eAVEncH264VProfile_Base, { 30, 1 },       { 352, 288 },   384000 },
    { eAVEncH264VProfile_Base, { 29970, 1000 }, { 320, 240 },   528560 },
    { eAVEncH264VProfile_Base, { 15, 1 },       { 720, 576 },  4000000 },
    { eAVEncH264VProfile_Main, { 25, 1 },       { 720, 576 }, 10000000 },
    { eAVEncH264VProfile_Main, { 30, 1 },       { 352, 288 }, 10000000 },
};
```



Os perfis H.264 são especificados usando a enumeração [**eAVEncH264VProfile.**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) Você também pode especificar o nível H.264, mas o Codificador de Vídeo [**H.264**](h-264-video-encoder.md) do Microsoft Media Foundation pode derivar o nível adequado para um determinado fluxo de vídeo, portanto, é recomendável não substituir o nível selecionado do codificador. Para conteúdo entrelaçado, você também especificaria o modo de intercalação (consulte [Intercalação de vídeo).](video-interlacing.md)

Para áudio AAC, os atributos de formato mais importantes são a taxa de amostra de áudio, o número de canais, o número de bits por exemplo e a taxa de bits codificada. Opcionalmente, você pode definir a indicação de nível de perfil de áudio do AAC. Para obter mais informações, consulte [**Codificador AAC**](aac-encoder.md). A matriz a seguir contém uma lista de formatos de codificação AAC.


```C++
struct AACProfileInfo
{
    UINT32  samplesPerSec;
    UINT32  numChannels;
    UINT32  bitsPerSample;
    UINT32  bytesPerSec;
    UINT32  aacProfile;
};

AACProfileInfo aac_profiles[] = 
{
    { 96000, 2, 16, 24000, 0x29}, 
    { 48000, 2, 16, 24000, 0x29}, 
    { 44100, 2, 16, 16000, 0x29}, 
    { 44100, 2, 16, 12000, 0x29}, 
};
```



> [!Note]  
> As `H264ProfileInfo` `AACProfileInfo` estruturas e definidas aqui não fazem parte da API Media Foundation dados.

 

## <a name="write-the-wmain-function"></a>Gravar a função wmain

O código a seguir mostra o ponto de entrada para o aplicativo de console.


```C++
int video_profile = 0;
int audio_profile = 0;

int wmain(int argc, wchar_t* argv[])
{
    HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);

    if (argc < 3 || argc > 5)
    {
        std::cout << "Usage:" << std::endl;
        std::cout << "input output [ audio_profile video_profile ]" << std::endl;
        return 1;
    }

    if (argc > 3)
    {
        audio_profile = _wtoi(argv[3]);
    }
    if (argc > 4)
    {
        video_profile = _wtoi(argv[4]);
    }

    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
    if (SUCCEEDED(hr))
    {
        hr = MFStartup(MF_VERSION);
        if (SUCCEEDED(hr))
        {
            hr = EncodeFile(argv[1], argv[2]);
            MFShutdown();
        }
        CoUninitialize();
    }

    if (SUCCEEDED(hr))
    {
        std::cout << "Done." << std::endl;
    }
    else
    {
        std::cout << "Error: " << std::hex << hr << std::endl;
    }

    return 0;
}
```



A `wmain` função faz o seguinte:

1.  Chama a [**função CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) para inicializar a biblioteca COM.
2.  Chama a [**função MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) para inicializar Media Foundation.
3.  Chama a função definida pelo `EncodeFile` aplicativo. Essa função transcodifica o arquivo de entrada para o arquivo de saída e é mostrada na próxima seção.
4.  Chama a [**função MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) para desligar Media Foundation.
5.  Chame a [**função CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) para não reinicializar a biblioteca COM.

## <a name="encode-the-file"></a>Codificar o arquivo

O código a seguir `EncodeFile` mostra a função , que executa a transcodificação. Essa função consiste principalmente em chamadas para outras funções definidas pelo aplicativo, que são mostradas posteriormente neste tópico.


```C++
HRESULT EncodeFile(PCWSTR pszInput, PCWSTR pszOutput)
{
    IMFTranscodeProfile *pProfile = NULL;
    IMFMediaSource *pSource = NULL;
    IMFTopology *pTopology = NULL;
    CSession *pSession = NULL;

    MFTIME duration = 0;

    HRESULT hr = CreateMediaSource(pszInput, &pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = GetSourceDuration(pSource, &duration);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = CreateTranscodeProfile(&pProfile);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFCreateTranscodeTopology(pSource, pszOutput, pProfile, &pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = CSession::Create(&pSession);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSession->StartEncodingSession(pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = RunEncodingSession(pSession, duration);

done:            
    if (pSource)
    {
        pSource->Shutdown();
    }

    SafeRelease(&pSession);
    SafeRelease(&pProfile);
    SafeRelease(&pSource);
    SafeRelease(&pTopology);
    return hr;
}
```



A `EncodeFile` função executa as etapas a seguir.

1.  Cria uma fonte de mídia para o arquivo de entrada, usando a URL ou o caminho do arquivo de entrada. (Consulte [Criar a fonte de mídia](#create-the-media-source).)
2.  Obtém a duração do arquivo de entrada. (Consulte [Obter a duração da origem](#get-the-source-duration).)
3.  Crie o perfil de transcodificar. (Consulte [Criar o perfil transcódigo](#create-the-transcode-profile).)
4.  Chame [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) para criar a topologia de transcódigo parcial.
5.  Crie um objeto auxiliar que gerencia a Sessão de Mídia. (Consulte Auxiliar de Sessão de Mídia).
6.  Execute a sessão de codificação e aguarde até que ela seja concluída. (Consulte [Executar a sessão de codificação](#run-the-encoding-session).)
7.  Chame [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) para desligar a fonte de mídia.
8.  Ponteiros da interface de versão. Esse código usa a [função SafeRelease](saferelease.md) para liberar ponteiros de interface. Outra opção é usar uma classe de ponteiro inteligente COM, como **CComPtr**.

### <a name="create-the-media-source"></a>Criar a fonte de mídia

A origem da mídia é o objeto que lê e analisado o arquivo de entrada. Para criar a fonte de mídia, passe a URL do arquivo de entrada para o [Resolvedor de Origem](source-resolver.md). O código a seguir mostra como fazer isso.


```C++
HRESULT CreateMediaSource(PCWSTR pszURL, IMFMediaSource **ppSource)
{
    MF_OBJECT_TYPE ObjectType = MF_OBJECT_INVALID;

    IMFSourceResolver* pResolver = NULL;
    IUnknown* pSource = NULL;

    // Create the source resolver.
    HRESULT hr = MFCreateSourceResolver(&pResolver);
    if (FAILED(hr))
    {
        goto done;
    }

    // Use the source resolver to create the media source
    hr = pResolver->CreateObjectFromURL(pszURL, MF_RESOLUTION_MEDIASOURCE, 
        NULL, &ObjectType, &pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the IMFMediaSource interface from the media source.
    hr = pSource->QueryInterface(IID_PPV_ARGS(ppSource));

done:
    SafeRelease(&pResolver);
    SafeRelease(&pSource);
    return hr;
}
```



Para obter mais informações, consulte [Usando o resolvedor de origem](using-the-source-resolver.md).

### <a name="get-the-source-duration"></a>Obter a duração da origem

Embora não seja necessário, é útil consultar a fonte de mídia durante o arquivo de entrada. Esse valor pode ser usado para acompanhar o progresso da codificação. A duração é armazenada no atributo [**MF \_ PD \_ DURATION**](mf-pd-duration-attribute.md) do descritor de apresentação. Obter o descritor de apresentação chamando [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).


```C++
HRESULT GetSourceDuration(IMFMediaSource *pSource, MFTIME *pDuration)
{
    *pDuration = 0;

    IMFPresentationDescriptor *pPD = NULL;

    HRESULT hr = pSource->CreatePresentationDescriptor(&pPD);
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_DURATION, (UINT64*)pDuration);
        pPD->Release();
    }
    return hr;
}
```



### <a name="create-the-transcode-profile"></a>Criar o perfil transcódigo

O perfil de transcódigo descreve os parâmetros de codificação. Para obter mais informações sobre como criar um perfil de transcódigo, [consulte Usando a API transcode](fast-transcode-objects.md). Para criar o perfil, execute as etapas a seguir.

1.  Chame [**MFCreateTranscodeProfile**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) para criar o perfil vazio.
2.  Crie um tipo de mídia para o fluxo de áudio do AAC. Adicione-o ao perfil chamando [**IMFTranscodeProfile::SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes).
3.  Crie um tipo de mídia para o fluxo de vídeo H.264. Adicione-o ao perfil chamando [**IMFTranscodeProfile::SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes).
4.  Chame [**MFCreateAttributes para**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) criar um armazenamento de atributos para os atributos no nível do contêiner.
5.  De definir o [atributo \_ \_ CONTAINERTYPE MF TRANSCODE.](mf-transcode-containertype.md) Esse é o único atributo de nível de contêiner necessário. Para a saída do arquivo MP4, de definido esse atributo como **MFTranscodeContainerType \_ MPEG4**.
6.  Chame [**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes) para definir os atributos no nível do contêiner.

O código a seguir mostra estas etapas.


```C++
HRESULT CreateTranscodeProfile(IMFTranscodeProfile **ppProfile)
{
    IMFTranscodeProfile *pProfile = NULL;
    IMFAttributes *pAudio = NULL;
    IMFAttributes *pVideo = NULL;
    IMFAttributes *pContainer = NULL;

    HRESULT hr = MFCreateTranscodeProfile(&pProfile);
    if (FAILED(hr)) 
    {
        goto done;
    }

    // Audio attributes.
    hr = CreateAACProfile(audio_profile, &pAudio);
    if (FAILED(hr)) 
    {
        goto done;
    }

    hr = pProfile->SetAudioAttributes(pAudio);
    if (FAILED(hr)) 
    {
        goto done;
    }

    // Video attributes.
    hr = CreateH264Profile(video_profile, &pVideo);
    if (FAILED(hr)) 
    {
        goto done;
    }

    hr = pProfile->SetVideoAttributes(pVideo);
    if (FAILED(hr)) 
    {
        goto done;
    }

    // Container attributes.
    hr = MFCreateAttributes(&pContainer, 1);
    if (FAILED(hr)) 
    {
        goto done;
    }

    hr = pContainer->SetGUID(MF_TRANSCODE_CONTAINERTYPE, MFTranscodeContainerType_MPEG4);
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
    SafeRelease(&pAudio);
    SafeRelease(&pVideo);
    SafeRelease(&pContainer);
    return hr;
}
```



Para especificar os atributos para o fluxo de vídeo H.264, crie um armazenamento de atributos e de definir os seguintes atributos:



| Atributo                                                       | Descrição                      |
|-----------------------------------------------------------------|---------------------------------|
| [**SUBTIPO \_ MF MT \_**](mf-mt-subtype-attribute.md)              | Definido como **MFVideoFormat \_ H264.** |
| [**PERFIL \_ MF MT \_ MPEG2 \_**](mf-mt-mpeg2-profile-attribute.md) | Perfil H.264.                  |
| [**TAMANHO DO \_ QUADRO MT MF \_ \_**](mf-mt-frame-size-attribute.md)       | Tamanho do quadro.                     |
| [**TAXA DE \_ QUADROS MT \_ \_ MF**](mf-mt-frame-rate-attribute.md)       | Taxa de quadros.                     |
| [**MF \_ MT \_ AVG \_ BITRATE**](mf-mt-avg-bitrate-attribute.md)     | Taxa de bits codificada.               |



 

Para especificar os atributos para o fluxo de áudio do AAC, crie um armazenamento de atributos e de definir os seguintes atributos:



| Atributo                                                                                      | Descrição                               |
|------------------------------------------------------------------------------------------------|------------------------------------------|
| [**SUBTIPO \_ MF MT \_**](mf-mt-subtype-attribute.md)                                             | Definido como **MFAudioFormat \_ AAC**            |
| [**AMOSTRAS \_ DE ÁUDIO MT \_ \_ MT POR \_ \_ SEGUNDO**](mf-mt-audio-samples-per-second-attribute.md)        | Taxa de amostra de áudio.                       |
| [**BITS DE \_ ÁUDIO MT \_ MT \_ POR \_ \_ EXEMPLO**](mf-mt-audio-bits-per-sample-attribute.md)              | Bits por exemplo de áudio.                   |
| [**CANAIS NUM DE ÁUDIO \_ MF MT \_ \_ \_**](mf-mt-audio-num-channels-attribute.md)                     | Número de canais de áudio.                |
| [**BYTES MF \_ MT \_ AUDIO \_ AVG \_ POR \_ \_ SEGUNDO**](mf-mt-audio-avg-bytes-per-second-attribute.md)   | Taxa de bits codificada.                        |
| [**ALINHAMENTO DO \_ BLOCO DE ÁUDIO MT \_ \_ \_ MT**](mf-mt-audio-block-alignment-attribute.md)               | defina como 1.                                |
| [MF \_ MT \_ AAC \_ AUDIO \_ PROFILE \_ LEVEL \_ INDICATION](mf-mt-aac-audio-profile-level-indication.md) | Indicação de nível de perfil do AAC (opcional). |



 

O código a seguir cria os atributos de fluxo de vídeo.


```C++
HRESULT CreateH264Profile(DWORD index, IMFAttributes **ppAttributes)
{
    if (index >= ARRAYSIZE(h264_profiles))
    {
        return E_INVALIDARG;
    }

    IMFAttributes *pAttributes = NULL;

    const H264ProfileInfo& profile = h264_profiles[index];

    HRESULT hr = MFCreateAttributes(&pAttributes, 5);
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetGUID(MF_MT_SUBTYPE, MFVideoFormat_H264);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(MF_MT_MPEG2_PROFILE, profile.profile);
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeSize(
            pAttributes, MF_MT_FRAME_SIZE, 
            profile.frame_size.Numerator, profile.frame_size.Numerator);
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(
            pAttributes, MF_MT_FRAME_RATE, 
            profile.fps.Numerator, profile.fps.Denominator);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(MF_MT_AVG_BITRATE, profile.bitrate);
    }
    if (SUCCEEDED(hr))
    {
        *ppAttributes = pAttributes;
        (*ppAttributes)->AddRef();
    }
    SafeRelease(&pAttributes);
    return hr;
}
```



O código a seguir cria os atributos de fluxo de áudio.


```C++
HRESULT CreateAACProfile(DWORD index, IMFAttributes **ppAttributes)
{
    if (index >= ARRAYSIZE(h264_profiles))
    {
        return E_INVALIDARG;
    }

    const AACProfileInfo& profile = aac_profiles[index];

    IMFAttributes *pAttributes = NULL;

    HRESULT hr = MFCreateAttributes(&pAttributes, 7);
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetGUID(MF_MT_SUBTYPE, MFAudioFormat_AAC);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(
            MF_MT_AUDIO_BITS_PER_SAMPLE, profile.bitsPerSample);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(
            MF_MT_AUDIO_SAMPLES_PER_SECOND, profile.samplesPerSec);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(
            MF_MT_AUDIO_NUM_CHANNELS, profile.numChannels);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(
            MF_MT_AUDIO_AVG_BYTES_PER_SECOND, profile.bytesPerSec);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(MF_MT_AUDIO_BLOCK_ALIGNMENT, 1);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(
            MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION, profile.aacProfile);
    }
    if (SUCCEEDED(hr))
    {
        *ppAttributes = pAttributes;
        (*ppAttributes)->AddRef();
    }
    SafeRelease(&pAttributes);
    return hr;
}
```



Observe que a API de transcodificar não requer um tipo de mídia verdadeiro, embora use atributos de tipo de mídia. Em particular, o atributo [**\_ MT \_ MAJOR \_ TYPE**](mf-mt-major-type-attribute.md) não é necessário, pois os métodos [**SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes) e [**SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes) implicam o tipo principal. No entanto, também é válido passar um tipo de mídia real para esses métodos. (A interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) herda [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes).)

### <a name="run-the-encoding-session"></a>Executar a sessão de codificação

O código a seguir executa a sessão de codificação. Ele usa a classe auxiliar de Sessão de Mídia, que é mostrada na próxima seção.


```C++
HRESULT RunEncodingSession(CSession *pSession, MFTIME duration)
{
    const DWORD WAIT_PERIOD = 500;
    const int   UPDATE_INCR = 5;

    HRESULT hr = S_OK;
    MFTIME pos;
    LONGLONG prev = 0;
    while (1)
    {
        hr = pSession->Wait(WAIT_PERIOD);
        if (hr == E_PENDING)
        {
            hr = pSession->GetEncodingPosition(&pos);

            LONGLONG percent = (100 * pos) / duration ;
            if (percent >= prev + UPDATE_INCR)
            {
                std::cout << percent << "% .. ";  
                prev = percent;
            }
        }
        else
        {
            std::cout << std::endl;
            break;
        }
    }
    return hr;
}
```



## <a name="media-session-helper"></a>Auxiliar de Sessão de Mídia

A [Sessão de](media-session.md) Mídia é descrita mais totalmente na seção Media Foundation [arquitetura](media-foundation-architecture.md) desta documentação. A Sessão de Mídia usa um modelo de evento assíncrono. Em um aplicativo de GUI, você deve responder a eventos de sessão sem bloquear o thread da interface do usuário para aguardar o próximo evento. O tutorial [Como reproduzir arquivos de mídia desprotegidos](how-to-play-unprotected-media-files.md) mostra como fazer isso em um aplicativo de reprodução. Para codificação, o princípio é o mesmo, mas menos eventos são relevantes:



| Evento                                  | Descrição                                                                                                                                                       |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MESessionEnded](mesessionended.md)   | Gerado quando a codificação é concluída.                                                                                                                            |
| [MESessionClosed](mesessionclosed.md) | Gerado quando o [**método IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) é concluído. Depois que esse evento é gerado, é seguro desligar a Sessão de Mídia. |



 

Para um aplicativo de console, é razoável bloquear e aguardar eventos. Dependendo do arquivo de origem e das configurações de codificação, pode levar algum tempo para concluir a codificação. Você pode obter atualizações de progresso da seguinte forma:

1.  Chame [**IMFMediaSession::GetClock para**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getclock) obter o relógio de apresentação.
2.  Consulte o relógio para a interface [**IMFPresentationClock.**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock)
3.  Chame [**IMFPresentationClock::GetTime**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-gettime) para obter a posição atual.
4.  A posição é dada em unidades de tempo. Para obter a porcentagem concluída, use o valor `(100 * position) / duration` .

Aqui está a declaração da `CSession` classe .


```C++
class CSession  : public IMFAsyncCallback 
{
public:
    static HRESULT Create(CSession **ppSession);

    // IUnknown methods
    STDMETHODIMP QueryInterface(REFIID riid, void** ppv);
    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();

    // IMFAsyncCallback methods
    STDMETHODIMP GetParameters(DWORD* pdwFlags, DWORD* pdwQueue)
    {
        // Implementation of this method is optional.
        return E_NOTIMPL;
    }
    STDMETHODIMP Invoke(IMFAsyncResult *pResult);

    // Other methods
    HRESULT StartEncodingSession(IMFTopology *pTopology);
    HRESULT GetEncodingPosition(MFTIME *pTime);
    HRESULT Wait(DWORD dwMsec);

private:
    CSession() : m_cRef(1), m_pSession(NULL), m_pClock(NULL), m_hrStatus(S_OK), m_hWaitEvent(NULL)
    {
    }
    virtual ~CSession()
    {
        if (m_pSession)
        {
            m_pSession->Shutdown();
        }

        SafeRelease(&m_pClock);
        SafeRelease(&m_pSession);
        CloseHandle(m_hWaitEvent);
    }

    HRESULT Initialize();

private:
    IMFMediaSession      *m_pSession;
    IMFPresentationClock *m_pClock;
    HRESULT m_hrStatus;
    HANDLE  m_hWaitEvent;
    long    m_cRef;
};
```



O código a seguir mostra a implementação completa da `CSession` classe .


```C++
HRESULT CSession::Create(CSession **ppSession)
{
    *ppSession = NULL;

    CSession *pSession = new (std::nothrow) CSession();
    if (pSession == NULL)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = pSession->Initialize();
    if (FAILED(hr))
    {
        pSession->Release();
        return hr;
    }
    *ppSession = pSession;
    return S_OK;
}

STDMETHODIMP CSession::QueryInterface(REFIID riid, void** ppv)
{
    static const QITAB qit[] = 
    {
        QITABENT(CSession, IMFAsyncCallback),
        { 0 }
    };
    return QISearch(this, qit, riid, ppv);
}

STDMETHODIMP_(ULONG) CSession::AddRef()
{
    return InterlockedIncrement(&m_cRef);
}

STDMETHODIMP_(ULONG) CSession::Release()
{
    long cRef = InterlockedDecrement(&m_cRef);
    if (cRef == 0)
    {
        delete this;
    }
    return cRef;
}

HRESULT CSession::Initialize()
{
    IMFClock *pClock = NULL;

    HRESULT hr = MFCreateMediaSession(NULL, &m_pSession);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = m_pSession->GetClock(&pClock);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pClock->QueryInterface(IID_PPV_ARGS(&m_pClock));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = m_pSession->BeginGetEvent(this, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    m_hWaitEvent = CreateEvent(NULL, FALSE, FALSE, NULL);  
    if (m_hWaitEvent == NULL)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
    }
done:
    SafeRelease(&pClock);
    return hr;
}

// Implements IMFAsyncCallback::Invoke
STDMETHODIMP CSession::Invoke(IMFAsyncResult *pResult)
{
    IMFMediaEvent* pEvent = NULL;
    MediaEventType meType = MEUnknown;
    HRESULT hrStatus = S_OK;

    HRESULT hr = m_pSession->EndGetEvent(pResult, &pEvent);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pEvent->GetType(&meType);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pEvent->GetStatus(&hrStatus);
    if (FAILED(hr))
    {
        goto done;
    }

    if (FAILED(hrStatus))
    {
        hr = hrStatus;
        goto done;
    }

    switch (meType)
    {
    case MESessionEnded:
        hr = m_pSession->Close();
        if (FAILED(hr))
        {
            goto done;
        }
        break;

    case MESessionClosed:
        SetEvent(m_hWaitEvent);
        break;
    }

    if (meType != MESessionClosed)
    {
        hr = m_pSession->BeginGetEvent(this, NULL);
    }

done:
    if (FAILED(hr))
    {
        m_hrStatus = hr;
        m_pSession->Close();
    }

    SafeRelease(&pEvent);
    return hr;
}

HRESULT CSession::StartEncodingSession(IMFTopology *pTopology)
{
    HRESULT hr = m_pSession->SetTopology(0, pTopology);
    if (SUCCEEDED(hr))
    {
        PROPVARIANT varStart;
        PropVariantClear(&varStart);
        hr = m_pSession->Start(&GUID_NULL, &varStart);
    }
    return hr;
}

HRESULT CSession::GetEncodingPosition(MFTIME *pTime)
{
    return m_pClock->GetTime(pTime);
}

HRESULT CSession::Wait(DWORD dwMsec)
{
    HRESULT hr = S_OK;

    DWORD dwTimeoutStatus = WaitForSingleObject(m_hWaitEvent, dwMsec);
    if (dwTimeoutStatus != WAIT_OBJECT_0)
    {
        hr = E_PENDING;
    }
    else
    {
        hr = m_hrStatus;
    }
    return hr;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Codificador AAC**](aac-encoder.md)
</dt> <dt>

[**Codificador de vídeo H.264**](h-264-video-encoder.md)
</dt> <dt>

[Sessão de mídia](media-session.md)
</dt> <dt>

[Tipos de mídia](media-types.md)
</dt> <dt>

[API de transcodificar](transcode-api.md)
</dt> </dl>

 

 
