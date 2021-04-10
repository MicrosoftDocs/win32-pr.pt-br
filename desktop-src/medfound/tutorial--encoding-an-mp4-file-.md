---
description: Este tutorial mostra como usar a API de transcodificação para codificar um arquivo MP4, usando H. 264 para o fluxo de vídeo e o AAC para o fluxo de áudio.
ms.assetid: 60873aa6-46ec-4a73-94b9-0d8ac602f850
title: 'Tutorial: codificando um arquivo MP4'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae895ef321b35f080bf946384ee32d83c2c539fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165286"
---
# <a name="tutorial-encoding-an-mp4-file"></a><span data-ttu-id="31dc3-103">Tutorial: codificando um arquivo MP4</span><span class="sxs-lookup"><span data-stu-id="31dc3-103">Tutorial: Encoding an MP4 File</span></span>

<span data-ttu-id="31dc3-104">Este tutorial mostra como usar a [API de transcodificação](transcode-api.md) para codificar um arquivo MP4, usando H. 264 para o fluxo de vídeo e o AAC para o fluxo de áudio.</span><span class="sxs-lookup"><span data-stu-id="31dc3-104">This tutorial shows how to use the [Transcode API](transcode-api.md) to encode an MP4 file, using H.264 for the video stream and AAC for the audio stream.</span></span>

-   [<span data-ttu-id="31dc3-105">Cabeçalhos e arquivos de biblioteca</span><span class="sxs-lookup"><span data-stu-id="31dc3-105">Headers and Library Files</span></span>](#headers-and-library-files)
-   [<span data-ttu-id="31dc3-106">Definir os perfis de codificação</span><span class="sxs-lookup"><span data-stu-id="31dc3-106">Define the Encoding Profiles</span></span>](#define-the-encoding-profiles)
-   [<span data-ttu-id="31dc3-107">Gravar a função wmain</span><span class="sxs-lookup"><span data-stu-id="31dc3-107">Write the wmain Function</span></span>](#write-the-wmain-function)
-   [<span data-ttu-id="31dc3-108">Codificar o arquivo</span><span class="sxs-lookup"><span data-stu-id="31dc3-108">Encode the File</span></span>](#encode-the-file)
    -   [<span data-ttu-id="31dc3-109">Criar a origem da mídia</span><span class="sxs-lookup"><span data-stu-id="31dc3-109">Create the Media Source</span></span>](#create-the-media-source)
    -   [<span data-ttu-id="31dc3-110">Obter a duração da origem</span><span class="sxs-lookup"><span data-stu-id="31dc3-110">Get the Source Duration</span></span>](#get-the-source-duration)
    -   [<span data-ttu-id="31dc3-111">Criar o perfil transcodificar</span><span class="sxs-lookup"><span data-stu-id="31dc3-111">Create the Transcode Profile</span></span>](#create-the-transcode-profile)
    -   [<span data-ttu-id="31dc3-112">Executar a sessão de codificação</span><span class="sxs-lookup"><span data-stu-id="31dc3-112">Run the Encoding Session</span></span>](#run-the-encoding-session)
-   [<span data-ttu-id="31dc3-113">Auxiliar de sessão de mídia</span><span class="sxs-lookup"><span data-stu-id="31dc3-113">Media Session Helper</span></span>](#media-session-helper)
-   [<span data-ttu-id="31dc3-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="31dc3-114">Related topics</span></span>](#related-topics)

## <a name="headers-and-library-files"></a><span data-ttu-id="31dc3-115">Cabeçalhos e arquivos de biblioteca</span><span class="sxs-lookup"><span data-stu-id="31dc3-115">Headers and Library Files</span></span>

<span data-ttu-id="31dc3-116">Inclua os seguintes arquivos de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="31dc3-116">Include the following header files.</span></span>


```C++
#include <new>
#include <iostream>
#include <windows.h>
#include <mfapi.h>
#include <Mfidl.h>
#include <shlwapi.h>
```



<span data-ttu-id="31dc3-117">Vincule os seguintes arquivos de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="31dc3-117">Link the following library files.</span></span>


```C++
#pragma comment(lib, "mfplat")
#pragma comment(lib, "mf")
#pragma comment(lib, "mfuuid")
#pragma comment(lib, "shlwapi")
```



## <a name="define-the-encoding-profiles"></a><span data-ttu-id="31dc3-118">Definir os perfis de codificação</span><span class="sxs-lookup"><span data-stu-id="31dc3-118">Define the Encoding Profiles</span></span>

<span data-ttu-id="31dc3-119">Uma abordagem de codificação é definir uma lista de perfis de codificação de destino que são conhecidos com antecedência.</span><span class="sxs-lookup"><span data-stu-id="31dc3-119">One approach to encoding is to define a list of target encoding profiles that are known in advance.</span></span> <span data-ttu-id="31dc3-120">Para este tutorial, pegamos uma abordagem relativamente simples e armazenamos uma lista de formatos de codificação para vídeo H. 264 e áudio AAC.</span><span class="sxs-lookup"><span data-stu-id="31dc3-120">For this tutorial, we take a relatively simple approach, and store a list of encoding formats for H.264 video and AAC audio.</span></span>

<span data-ttu-id="31dc3-121">Para H. 264, os atributos de formato mais importantes são o perfil H. 264, a taxa de quadros, o tamanho do quadro e a taxa de bits codificada.</span><span class="sxs-lookup"><span data-stu-id="31dc3-121">For H.264, the most important format attributes are the H.264 profile, the frame rate, the frame size, and the encoded bit rate.</span></span> <span data-ttu-id="31dc3-122">A matriz a seguir contém uma lista de formatos de codificação H. 264.</span><span class="sxs-lookup"><span data-stu-id="31dc3-122">The following array contains a list of H.264 encoding formats.</span></span>


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



<span data-ttu-id="31dc3-123">Os perfis H. 264 são especificados usando a enumeração [**eAVEncH264VProfile**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) .</span><span class="sxs-lookup"><span data-stu-id="31dc3-123">H.264 profiles are specified using the [**eAVEncH264VProfile**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) enumeration.</span></span> <span data-ttu-id="31dc3-124">Você também pode especificar o nível H. 264, mas o [**codificador de vídeo Microsoft Media Foundation H. 264**](h-264-video-encoder.md) pode derivar o nível apropriado para um determinado fluxo de vídeo, portanto, é recomendável não substituir o nível selecionado do codificador.</span><span class="sxs-lookup"><span data-stu-id="31dc3-124">You could also specify the H.264 level, but the Microsoft Media Foundation [**H.264 Video Encoder**](h-264-video-encoder.md) can derive the proper level for a given video stream, so it is recommended not to override the encoder's selected level.</span></span> <span data-ttu-id="31dc3-125">Para conteúdo entrelaçado, você também especificaria o modo de entrelaçamento (consulte [entrelaçamento de vídeo](video-interlacing.md)).</span><span class="sxs-lookup"><span data-stu-id="31dc3-125">For interlaced content, you would also specify the interlace mode (see [Video Interlacing](video-interlacing.md)).</span></span>

<span data-ttu-id="31dc3-126">Para áudio AAC, os atributos de formato mais importantes são a taxa de amostra de áudio, o número de canais, o número de bits por amostra e a taxa de bits codificada.</span><span class="sxs-lookup"><span data-stu-id="31dc3-126">For AAC audio, the most important format attributes are the audio sample rate, the number of channels, the number of bits per sample, and the encoded bit rate.</span></span> <span data-ttu-id="31dc3-127">Opcionalmente, você pode definir a indicação de nível de perfil de áudio AAC.</span><span class="sxs-lookup"><span data-stu-id="31dc3-127">Optionally, you can set the AAC audio profile level indication.</span></span> <span data-ttu-id="31dc3-128">Para obter mais informações, consulte [**codificador AAC**](aac-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="31dc3-128">For more information, see [**AAC Encoder**](aac-encoder.md).</span></span> <span data-ttu-id="31dc3-129">A matriz a seguir contém uma lista de formatos de codificação AAC.</span><span class="sxs-lookup"><span data-stu-id="31dc3-129">The following array contains a list of AAC encoding formats.</span></span>


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
> <span data-ttu-id="31dc3-130">As `H264ProfileInfo` `AACProfileInfo` estruturas e definidas aqui não fazem parte da API de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="31dc3-130">The `H264ProfileInfo` and `AACProfileInfo` structures defined here are not part of the Media Foundation API.</span></span>

 

## <a name="write-the-wmain-function"></a><span data-ttu-id="31dc3-131">Gravar a função wmain</span><span class="sxs-lookup"><span data-stu-id="31dc3-131">Write the wmain Function</span></span>

<span data-ttu-id="31dc3-132">O código a seguir mostra o ponto de entrada para o aplicativo de console.</span><span class="sxs-lookup"><span data-stu-id="31dc3-132">The following code shows the entry point for the console application.</span></span>


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



<span data-ttu-id="31dc3-133">A `wmain` função faz o seguinte:</span><span class="sxs-lookup"><span data-stu-id="31dc3-133">The `wmain` function does the following:</span></span>

1.  <span data-ttu-id="31dc3-134">Chama a função [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) para inicializar a biblioteca com.</span><span class="sxs-lookup"><span data-stu-id="31dc3-134">Calls the [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) function to initialize the COM library.</span></span>
2.  <span data-ttu-id="31dc3-135">Chama a função [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) para inicializar Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="31dc3-135">Calls the [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) function to initialize Media Foundation.</span></span>
3.  <span data-ttu-id="31dc3-136">Chama a função definida pelo aplicativo `EncodeFile` .</span><span class="sxs-lookup"><span data-stu-id="31dc3-136">Calls the application-defined `EncodeFile` function.</span></span> <span data-ttu-id="31dc3-137">Essa função codifica o arquivo de entrada para o arquivo de saída e é mostrada na próxima seção.</span><span class="sxs-lookup"><span data-stu-id="31dc3-137">This function transcodes the input file to the output file, and is shown in the next section.</span></span>
4.  <span data-ttu-id="31dc3-138">Chama a função [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) para desligar Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="31dc3-138">Calls the [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) function to shut down Media Foundation.</span></span>
5.  <span data-ttu-id="31dc3-139">Chame a função [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) para cancelar a inicialização da biblioteca com.</span><span class="sxs-lookup"><span data-stu-id="31dc3-139">Call the [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) function to uninitialize the COM library.</span></span>

## <a name="encode-the-file"></a><span data-ttu-id="31dc3-140">Codificar o arquivo</span><span class="sxs-lookup"><span data-stu-id="31dc3-140">Encode the File</span></span>

<span data-ttu-id="31dc3-141">O código a seguir mostra `EncodeFile` a função, que executa a transcodificação.</span><span class="sxs-lookup"><span data-stu-id="31dc3-141">The following code shows `EncodeFile` function, which performs the transcoding.</span></span> <span data-ttu-id="31dc3-142">Essa função consiste principalmente em chamadas para outras funções definidas pelo aplicativo, que são mostradas mais adiante neste tópico.</span><span class="sxs-lookup"><span data-stu-id="31dc3-142">This function consists mostly of calls to other application-defined functions, which are shown later in this topic.</span></span>


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



<span data-ttu-id="31dc3-143">A `EncodeFile` função executa as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="31dc3-143">The `EncodeFile` function performs the following steps.</span></span>

1.  <span data-ttu-id="31dc3-144">Cria uma origem de mídia para o arquivo de entrada, usando a URL ou o caminho do arquivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="31dc3-144">Creates a media source for the input file, using the URL or file path of the input file.</span></span> <span data-ttu-id="31dc3-145">(Consulte [criar a origem da mídia](#create-the-media-source).)</span><span class="sxs-lookup"><span data-stu-id="31dc3-145">(See [Create the Media Source](#create-the-media-source).)</span></span>
2.  <span data-ttu-id="31dc3-146">Obtém a duração do arquivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="31dc3-146">Gets the duration of the input file.</span></span> <span data-ttu-id="31dc3-147">(Veja [obter a duração da origem](#get-the-source-duration).)</span><span class="sxs-lookup"><span data-stu-id="31dc3-147">(See [Get the Source Duration](#get-the-source-duration).)</span></span>
3.  <span data-ttu-id="31dc3-148">Crie o perfil transcodificar.</span><span class="sxs-lookup"><span data-stu-id="31dc3-148">Create the transcode profile.</span></span> <span data-ttu-id="31dc3-149">(Consulte [criar o perfil transcodificar](#create-the-transcode-profile).)</span><span class="sxs-lookup"><span data-stu-id="31dc3-149">(See [Create the Transcode Profile](#create-the-transcode-profile).)</span></span>
4.  <span data-ttu-id="31dc3-150">Chame [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) para criar a topologia de transcodificação parcial.</span><span class="sxs-lookup"><span data-stu-id="31dc3-150">Call [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) to create the partial transcode topology.</span></span>
5.  <span data-ttu-id="31dc3-151">Crie um objeto auxiliar que gerencia a sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="31dc3-151">Create a helper object that manages the Media Session.</span></span> <span data-ttu-id="31dc3-152">(Consulte auxiliar de sessão de mídia).</span><span class="sxs-lookup"><span data-stu-id="31dc3-152">(See Media Session Helper).</span></span>
6.  <span data-ttu-id="31dc3-153">Execute a sessão de codificação e aguarde sua conclusão.</span><span class="sxs-lookup"><span data-stu-id="31dc3-153">Run the encoding session and wait for it to complete.</span></span> <span data-ttu-id="31dc3-154">(Consulte [executar a sessão de codificação](#run-the-encoding-session).)</span><span class="sxs-lookup"><span data-stu-id="31dc3-154">(See [Run the Encoding Session](#run-the-encoding-session).)</span></span>
7.  <span data-ttu-id="31dc3-155">Chame [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) para desligar a origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="31dc3-155">Call [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) to shut down the media source.</span></span>
8.  <span data-ttu-id="31dc3-156">Ponteiros de interface de versão.</span><span class="sxs-lookup"><span data-stu-id="31dc3-156">Release interface pointers.</span></span> <span data-ttu-id="31dc3-157">Esse código usa a função [SafeRelease](saferelease.md) para liberar ponteiros de interface.</span><span class="sxs-lookup"><span data-stu-id="31dc3-157">This code uses the [SafeRelease](saferelease.md) function to release interface pointers.</span></span> <span data-ttu-id="31dc3-158">Outra opção é usar uma classe de ponteiro inteligente COM, como **CComPtr**.</span><span class="sxs-lookup"><span data-stu-id="31dc3-158">Another option is to use a COM smart pointer class, such as **CComPtr**.</span></span>

### <a name="create-the-media-source"></a><span data-ttu-id="31dc3-159">Criar a origem da mídia</span><span class="sxs-lookup"><span data-stu-id="31dc3-159">Create the Media Source</span></span>

<span data-ttu-id="31dc3-160">A origem da mídia é o objeto que lê e analisa o arquivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="31dc3-160">The media source is the object that reads and parses the input file.</span></span> <span data-ttu-id="31dc3-161">Para criar a origem da mídia, passe a URL do arquivo de entrada para o [resolvedor de origem](source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="31dc3-161">To create the media source, pass the URL of the input file to the [Source Resolver](source-resolver.md).</span></span> <span data-ttu-id="31dc3-162">O código a seguir mostra como fazer isso.</span><span class="sxs-lookup"><span data-stu-id="31dc3-162">The following code shows how to do this.</span></span>


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



<span data-ttu-id="31dc3-163">Para obter mais informações, consulte [usando o resolvedor de origem](using-the-source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="31dc3-163">For more information, see [Using the Source Resolver](using-the-source-resolver.md).</span></span>

### <a name="get-the-source-duration"></a><span data-ttu-id="31dc3-164">Obter a duração da origem</span><span class="sxs-lookup"><span data-stu-id="31dc3-164">Get the Source Duration</span></span>

<span data-ttu-id="31dc3-165">Embora não seja necessário, é útil consultar a origem da mídia para a duração do arquivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="31dc3-165">Although not required, it is useful to query the media source for the duration of the input file.</span></span> <span data-ttu-id="31dc3-166">Esse valor pode ser usado para acompanhar o progresso da codificação.</span><span class="sxs-lookup"><span data-stu-id="31dc3-166">This value can be used to track the encoding progress.</span></span> <span data-ttu-id="31dc3-167">A duração é armazenada no atributo de [**\_ \_ duração de PD de MF**](mf-pd-duration-attribute.md) do descritor de apresentação.</span><span class="sxs-lookup"><span data-stu-id="31dc3-167">The duration is stored in the [**MF\_PD\_DURATION**](mf-pd-duration-attribute.md) attribute of the presentation descriptor.</span></span> <span data-ttu-id="31dc3-168">Obtenha o descritor de apresentação chamando [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="31dc3-168">Get the presentation descriptor by calling [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span></span>


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



### <a name="create-the-transcode-profile"></a><span data-ttu-id="31dc3-169">Criar o perfil transcodificar</span><span class="sxs-lookup"><span data-stu-id="31dc3-169">Create the Transcode Profile</span></span>

<span data-ttu-id="31dc3-170">O perfil transcodificar descreve os parâmetros de codificação.</span><span class="sxs-lookup"><span data-stu-id="31dc3-170">The transcode profile describes the encoding parameters.</span></span> <span data-ttu-id="31dc3-171">Para obter mais informações sobre como criar um perfil transcodificar, consulte [usando a API transcodificar](fast-transcode-objects.md).</span><span class="sxs-lookup"><span data-stu-id="31dc3-171">For more information about creating a transcode profile, see [Using the Transcode API](fast-transcode-objects.md).</span></span> <span data-ttu-id="31dc3-172">Para criar o perfil, execute as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="31dc3-172">To create the profile, perform the following steps.</span></span>

1.  <span data-ttu-id="31dc3-173">Chame [**MFCreateTranscodeProfile**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) para criar o perfil vazio.</span><span class="sxs-lookup"><span data-stu-id="31dc3-173">Call [**MFCreateTranscodeProfile**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) to create the empty profile.</span></span>
2.  <span data-ttu-id="31dc3-174">Crie um tipo de mídia para o fluxo de áudio AAC.</span><span class="sxs-lookup"><span data-stu-id="31dc3-174">Create a media type for the AAC audio stream.</span></span> <span data-ttu-id="31dc3-175">Adicione-o ao perfil chamando [**IMFTranscodeProfile:: Setaudioattributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes).</span><span class="sxs-lookup"><span data-stu-id="31dc3-175">Add it to the profile by calling [**IMFTranscodeProfile::SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes).</span></span>
3.  <span data-ttu-id="31dc3-176">Crie um tipo de mídia para o fluxo de vídeo H. 264.</span><span class="sxs-lookup"><span data-stu-id="31dc3-176">Create a media type for the H.264 video stream.</span></span> <span data-ttu-id="31dc3-177">Adicione-o ao perfil chamando [**IMFTranscodeProfile:: Setvideoattributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes).</span><span class="sxs-lookup"><span data-stu-id="31dc3-177">Add it to the profile by calling [**IMFTranscodeProfile::SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes).</span></span>
4.  <span data-ttu-id="31dc3-178">Chame [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) para criar um repositório de atributos para os atributos de nível de contêiner.</span><span class="sxs-lookup"><span data-stu-id="31dc3-178">Call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create an attribute store for the container-level attributes.</span></span>
5.  <span data-ttu-id="31dc3-179">Defina o [atributo \_ \_ ContainerType de transcodificação MF](mf-transcode-containertype.md) .</span><span class="sxs-lookup"><span data-stu-id="31dc3-179">Set the [MF\_TRANSCODE\_CONTAINERTYPE](mf-transcode-containertype.md) attribute.</span></span> <span data-ttu-id="31dc3-180">Esse é o único atributo de nível de contêiner necessário.</span><span class="sxs-lookup"><span data-stu-id="31dc3-180">This is the only required container-level attribute.</span></span> <span data-ttu-id="31dc3-181">Para saída de arquivo MP4, defina esse atributo como **MFTranscodeContainerType \_ MPEG4**.</span><span class="sxs-lookup"><span data-stu-id="31dc3-181">For MP4 file output, set this attribute to **MFTranscodeContainerType\_MPEG4**.</span></span>
6.  <span data-ttu-id="31dc3-182">Chame [**IMFTranscodeProfile:: Setcontêinerattributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes) para definir os atributos de nível de contêiner.</span><span class="sxs-lookup"><span data-stu-id="31dc3-182">Call [**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes) to set the container-level attributes.</span></span>

<span data-ttu-id="31dc3-183">O código a seguir mostra essas etapas.</span><span class="sxs-lookup"><span data-stu-id="31dc3-183">The following code shows these steps.</span></span>


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



<span data-ttu-id="31dc3-184">Para especificar os atributos para o fluxo de vídeo H. 264, crie um repositório de atributos e defina os seguintes atributos:</span><span class="sxs-lookup"><span data-stu-id="31dc3-184">To specify the attributes for the H.264 video stream, create an attribute store and set the following attributes:</span></span>



| <span data-ttu-id="31dc3-185">Atributo</span><span class="sxs-lookup"><span data-stu-id="31dc3-185">Attribute</span></span>                                                       | <span data-ttu-id="31dc3-186">Descrição</span><span class="sxs-lookup"><span data-stu-id="31dc3-186">Desription</span></span>                      |
|-----------------------------------------------------------------|---------------------------------|
| [<span data-ttu-id="31dc3-187">**subtipo MF \_ MT \_**</span><span class="sxs-lookup"><span data-stu-id="31dc3-187">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)              | <span data-ttu-id="31dc3-188">Defina como **MFVideoFormat \_ H264**.</span><span class="sxs-lookup"><span data-stu-id="31dc3-188">Set to **MFVideoFormat\_H264**.</span></span> |
| [<span data-ttu-id="31dc3-189">**\_Perfil MF \_ MT \_**</span><span class="sxs-lookup"><span data-stu-id="31dc3-189">**MF\_MT\_MPEG2\_PROFILE**</span></span>](mf-mt-mpeg2-profile-attribute.md) | <span data-ttu-id="31dc3-190">Perfil H. 264.</span><span class="sxs-lookup"><span data-stu-id="31dc3-190">H.264 profile.</span></span>                  |
| [<span data-ttu-id="31dc3-191">**\_tamanho do \_ quadro MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="31dc3-191">**MF\_MT\_FRAME\_SIZE**</span></span>](mf-mt-frame-size-attribute.md)       | <span data-ttu-id="31dc3-192">Tamanho do quadro.</span><span class="sxs-lookup"><span data-stu-id="31dc3-192">Frame size.</span></span>                     |
| [<span data-ttu-id="31dc3-193">**\_taxa de \_ quadros MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="31dc3-193">**MF\_MT\_FRAME\_RATE**</span></span>](mf-mt-frame-rate-attribute.md)       | <span data-ttu-id="31dc3-194">Taxa de quadros.</span><span class="sxs-lookup"><span data-stu-id="31dc3-194">Frame rate.</span></span>                     |
| [<span data-ttu-id="31dc3-195">**\_taxa de \_ \_ bits média de MF MT**</span><span class="sxs-lookup"><span data-stu-id="31dc3-195">**MF\_MT\_AVG\_BITRATE**</span></span>](mf-mt-avg-bitrate-attribute.md)     | <span data-ttu-id="31dc3-196">Taxa de bits codificada.</span><span class="sxs-lookup"><span data-stu-id="31dc3-196">Encoded bit rate.</span></span>               |



 

<span data-ttu-id="31dc3-197">Para especificar os atributos para o fluxo de áudio AAC, crie um repositório de atributos e defina os seguintes atributos:</span><span class="sxs-lookup"><span data-stu-id="31dc3-197">To specify the attributes for the AAC audio stream, create an attribute store and set the following attributes:</span></span>



| <span data-ttu-id="31dc3-198">Atributo</span><span class="sxs-lookup"><span data-stu-id="31dc3-198">Attribute</span></span>                                                                                      | <span data-ttu-id="31dc3-199">Descrição</span><span class="sxs-lookup"><span data-stu-id="31dc3-199">Desription</span></span>                               |
|------------------------------------------------------------------------------------------------|------------------------------------------|
| [<span data-ttu-id="31dc3-200">**subtipo MF \_ MT \_**</span><span class="sxs-lookup"><span data-stu-id="31dc3-200">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                             | <span data-ttu-id="31dc3-201">Definir como **MFAudioFormat \_ AAC**</span><span class="sxs-lookup"><span data-stu-id="31dc3-201">Set to **MFAudioFormat\_AAC**</span></span>            |
| [<span data-ttu-id="31dc3-202">**\_amostras de áudio MF MT \_ \_ \_ por \_ segundo**</span><span class="sxs-lookup"><span data-stu-id="31dc3-202">**MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)        | <span data-ttu-id="31dc3-203">Taxa de amostra de áudio.</span><span class="sxs-lookup"><span data-stu-id="31dc3-203">Audio sample rate.</span></span>                       |
| [<span data-ttu-id="31dc3-204">**\_bits de áudio MF MT \_ \_ \_ por \_ amostra**</span><span class="sxs-lookup"><span data-stu-id="31dc3-204">**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**</span></span>](mf-mt-audio-bits-per-sample-attribute.md)              | <span data-ttu-id="31dc3-205">Bits por amostra de áudio.</span><span class="sxs-lookup"><span data-stu-id="31dc3-205">Bits per audio sample.</span></span>                   |
| [<span data-ttu-id="31dc3-206">**\_canais de \_ número de áudio MF MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="31dc3-206">**MF\_MT\_AUDIO\_NUM\_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                     | <span data-ttu-id="31dc3-207">Número de canais de áudio.</span><span class="sxs-lookup"><span data-stu-id="31dc3-207">Number of audio channels.</span></span>                |
| [<span data-ttu-id="31dc3-208">**áudio do MF \_ MT \_ média de \_ \_ bytes \_ por \_ segundo**</span><span class="sxs-lookup"><span data-stu-id="31dc3-208">**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md)   | <span data-ttu-id="31dc3-209">Taxa de bits codificada.</span><span class="sxs-lookup"><span data-stu-id="31dc3-209">Encoded bit rate.</span></span>                        |
| [<span data-ttu-id="31dc3-210">**\_alinhamento de \_ bloco de áudio MF MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="31dc3-210">**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)               | <span data-ttu-id="31dc3-211">defina como 1.</span><span class="sxs-lookup"><span data-stu-id="31dc3-211">Set to 1.</span></span>                                |
| [<span data-ttu-id="31dc3-212">\_indicação de \_ \_ nível de \_ perfil de áudio \_ \_ MF MT AAC</span><span class="sxs-lookup"><span data-stu-id="31dc3-212">MF\_MT\_AAC\_AUDIO\_PROFILE\_LEVEL\_INDICATION</span></span>](mf-mt-aac-audio-profile-level-indication.md) | <span data-ttu-id="31dc3-213">Indicação de nível de perfil AAC (opcional).</span><span class="sxs-lookup"><span data-stu-id="31dc3-213">AAC profile level indication (optional).</span></span> |



 

<span data-ttu-id="31dc3-214">O código a seguir cria os atributos de fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="31dc3-214">The following code creates the video stream attributes.</span></span>


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



<span data-ttu-id="31dc3-215">O código a seguir cria os atributos de fluxo de áudio.</span><span class="sxs-lookup"><span data-stu-id="31dc3-215">The following code creates the audio stream attributes.</span></span>


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



<span data-ttu-id="31dc3-216">Observe que a API de transcodificação não requer um tipo de mídia verdadeiro, embora use atributos de tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="31dc3-216">Note that the transcode API does not require a true media type, although it uses media-type attributes.</span></span> <span data-ttu-id="31dc3-217">Em particular, o atributo de [**\_ \_ \_ tipo principal MF MT**](mf-mt-major-type-attribute.md) não é necessário, pois os métodos [**setvideoattributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes) e [**setaudioattributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes) sugerem o tipo principal.</span><span class="sxs-lookup"><span data-stu-id="31dc3-217">In particular, the [**MF\_MT\_MAJOR\_TYPE**](mf-mt-major-type-attribute.md) attribute it not required, because the [**SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes) and [**SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes) methods imply the major type.</span></span> <span data-ttu-id="31dc3-218">No entanto, também é válido passar um tipo de mídia real para esses métodos.</span><span class="sxs-lookup"><span data-stu-id="31dc3-218">However, it also valid to pass an actual media type to these methods.</span></span> <span data-ttu-id="31dc3-219">(A interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) herda [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes).)</span><span class="sxs-lookup"><span data-stu-id="31dc3-219">(The [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface inherits [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes).)</span></span>

### <a name="run-the-encoding-session"></a><span data-ttu-id="31dc3-220">Executar a sessão de codificação</span><span class="sxs-lookup"><span data-stu-id="31dc3-220">Run the Encoding Session</span></span>

<span data-ttu-id="31dc3-221">O código a seguir executa a sessão de codificação.</span><span class="sxs-lookup"><span data-stu-id="31dc3-221">The following code runs the encoding session.</span></span> <span data-ttu-id="31dc3-222">Ele usa a classe auxiliar de sessão de mídia, que é mostrada na próxima seção.</span><span class="sxs-lookup"><span data-stu-id="31dc3-222">It uses the Media Session helper class, which is shown in the next section.</span></span>


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



## <a name="media-session-helper"></a><span data-ttu-id="31dc3-223">Auxiliar de sessão de mídia</span><span class="sxs-lookup"><span data-stu-id="31dc3-223">Media Session Helper</span></span>

<span data-ttu-id="31dc3-224">A [sessão de mídia](media-session.md) é descrita mais completamente na seção [arquitetura de Media Foundation](media-foundation-architecture.md) desta documentação.</span><span class="sxs-lookup"><span data-stu-id="31dc3-224">The [Media Session](media-session.md) is described more fully in the [Media Foundation Architecture](media-foundation-architecture.md) section of this documentation.</span></span> <span data-ttu-id="31dc3-225">A sessão de mídia usa um modelo de evento assíncrono.</span><span class="sxs-lookup"><span data-stu-id="31dc3-225">The Media Session uses an asynchronous event model.</span></span> <span data-ttu-id="31dc3-226">Em um aplicativo de GUI, você deve responder a eventos de sessão sem bloquear o thread da interface do usuário para aguardar o próximo evento.</span><span class="sxs-lookup"><span data-stu-id="31dc3-226">In a GUI application, you should respond to session events without blocking the UI thread to wait for the next event.</span></span> <span data-ttu-id="31dc3-227">O tutorial [como reproduzir arquivos de mídia desprotegidos](how-to-play-unprotected-media-files.md) mostra como fazer isso em um aplicativo de reprodução.</span><span class="sxs-lookup"><span data-stu-id="31dc3-227">The tutorial [How to Play Unprotected Media Files](how-to-play-unprotected-media-files.md) shows how to do this in a playback application.</span></span> <span data-ttu-id="31dc3-228">Para codificação, o princípio é o mesmo, mas menos eventos são relevantes:</span><span class="sxs-lookup"><span data-stu-id="31dc3-228">For encoding, the principle is the same, but fewer events are relevant:</span></span>



| <span data-ttu-id="31dc3-229">Evento</span><span class="sxs-lookup"><span data-stu-id="31dc3-229">Event</span></span>                                  | <span data-ttu-id="31dc3-230">Descrição</span><span class="sxs-lookup"><span data-stu-id="31dc3-230">Desription</span></span>                                                                                                                                                       |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="31dc3-231">MESessionEnded</span><span class="sxs-lookup"><span data-stu-id="31dc3-231">MESessionEnded</span></span>](mesessionended.md)   | <span data-ttu-id="31dc3-232">Gerado quando a codificação é concluída.</span><span class="sxs-lookup"><span data-stu-id="31dc3-232">Raised when the encoding is complete.</span></span>                                                                                                                            |
| [<span data-ttu-id="31dc3-233">MESessionClosed</span><span class="sxs-lookup"><span data-stu-id="31dc3-233">MESessionClosed</span></span>](mesessionclosed.md) | <span data-ttu-id="31dc3-234">Gerado quando o método [**IMFMediaSession:: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) é concluído.</span><span class="sxs-lookup"><span data-stu-id="31dc3-234">Raised when the [**IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) method completes.</span></span> <span data-ttu-id="31dc3-235">Depois que esse evento é gerado, é seguro desligar a sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="31dc3-235">After this event is raised, it is safe to shut down the Media Session.</span></span> |



 

<span data-ttu-id="31dc3-236">Para um aplicativo de console, é razoável bloquear e aguardar eventos.</span><span class="sxs-lookup"><span data-stu-id="31dc3-236">For a console application, it is reasonable to block and wait for events.</span></span> <span data-ttu-id="31dc3-237">Dependendo do arquivo de origem e das configurações de codificação, pode levar algum tempo para concluir a codificação.</span><span class="sxs-lookup"><span data-stu-id="31dc3-237">Depending on the source file and the encoding settings, it might take awhile to complete the encoding.</span></span> <span data-ttu-id="31dc3-238">Você pode obter atualizações de progresso da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="31dc3-238">You can get progress updates as follows:</span></span>

1.  <span data-ttu-id="31dc3-239">Chame [**IMFMediaSession:: getclock**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getclock) para obter o relógio de apresentação.</span><span class="sxs-lookup"><span data-stu-id="31dc3-239">Call [**IMFMediaSession::GetClock**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getclock) to get the presentation clock.</span></span>
2.  <span data-ttu-id="31dc3-240">Consulte o relógio para a interface [**IMFPresentationClock**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock) .</span><span class="sxs-lookup"><span data-stu-id="31dc3-240">Query the clock for the [**IMFPresentationClock**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock) interface.</span></span>
3.  <span data-ttu-id="31dc3-241">Chame [**IMFPresentationClock:: getTime**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-gettime) para obter a posição atual.</span><span class="sxs-lookup"><span data-stu-id="31dc3-241">Call [**IMFPresentationClock::GetTime**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-gettime) to get the current position.</span></span>
4.  <span data-ttu-id="31dc3-242">A posição é fornecida em unidades de tempo.</span><span class="sxs-lookup"><span data-stu-id="31dc3-242">The position is given in units of time.</span></span> <span data-ttu-id="31dc3-243">Para obter a porcentagem concluída, use o valor `(100 * position) / duration` .</span><span class="sxs-lookup"><span data-stu-id="31dc3-243">To get the percentage completed, use the value `(100 * position) / duration`.</span></span>

<span data-ttu-id="31dc3-244">Aqui está a declaração da `CSession` classe.</span><span class="sxs-lookup"><span data-stu-id="31dc3-244">Here is the declaration of the `CSession` class.</span></span>


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



<span data-ttu-id="31dc3-245">O código a seguir mostra a implementação completa da `CSession` classe.</span><span class="sxs-lookup"><span data-stu-id="31dc3-245">The following code shows the complete implementation of the `CSession` class.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="31dc3-246">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="31dc3-246">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31dc3-247">**Codificador AAC**</span><span class="sxs-lookup"><span data-stu-id="31dc3-247">**AAC Encoder**</span></span>](aac-encoder.md)
</dt> <dt>

[<span data-ttu-id="31dc3-248">**Codificador de vídeo H. 264**</span><span class="sxs-lookup"><span data-stu-id="31dc3-248">**H.264 Video Encoder**</span></span>](h-264-video-encoder.md)
</dt> <dt>

[<span data-ttu-id="31dc3-249">Sessão de mídia</span><span class="sxs-lookup"><span data-stu-id="31dc3-249">Media Session</span></span>](media-session.md)
</dt> <dt>

[<span data-ttu-id="31dc3-250">Tipos de mídia</span><span class="sxs-lookup"><span data-stu-id="31dc3-250">Media Types</span></span>](media-types.md)
</dt> <dt>

[<span data-ttu-id="31dc3-251">API de transcodificação</span><span class="sxs-lookup"><span data-stu-id="31dc3-251">Transcode API</span></span>](transcode-api.md)
</dt> </dl>

 

 
