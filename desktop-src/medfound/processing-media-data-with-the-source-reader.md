---
description: Este tópico descreve como usar o leitor de origem para processar dados de mídia.
ms.assetid: 583f5736-f767-47c5-8fdc-b3645aed59f6
title: Usando o leitor de origem para processar dados de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b19bce4d83298693825037aef92a220d78ed7c7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104297885"
---
# <a name="using-the-source-reader-to-process-media-data"></a><span data-ttu-id="e0231-103">Usando o leitor de origem para processar dados de mídia</span><span class="sxs-lookup"><span data-stu-id="e0231-103">Using the Source Reader to Process Media Data</span></span>

<span data-ttu-id="e0231-104">Este tópico descreve como usar o [leitor de origem](source-reader.md) para processar dados de mídia.</span><span class="sxs-lookup"><span data-stu-id="e0231-104">This topic describes how to use the [Source Reader](source-reader.md) to process media data.</span></span>

<span data-ttu-id="e0231-105">Para usar o leitor de origem, siga estas etapas básicas:</span><span class="sxs-lookup"><span data-stu-id="e0231-105">To use the Source Reader, follow these basic steps:</span></span>

1.  <span data-ttu-id="e0231-106">Crie uma instância do leitor de origem.</span><span class="sxs-lookup"><span data-stu-id="e0231-106">Create an instance of the Source Reader.</span></span>
2.  <span data-ttu-id="e0231-107">Enumere os formatos de saída possíveis.</span><span class="sxs-lookup"><span data-stu-id="e0231-107">Enumerate the possible output formats.</span></span>
3.  <span data-ttu-id="e0231-108">Defina o formato de saída real para cada fluxo.</span><span class="sxs-lookup"><span data-stu-id="e0231-108">Set the actual output format for each stream.</span></span>
4.  <span data-ttu-id="e0231-109">Processar dados da origem.</span><span class="sxs-lookup"><span data-stu-id="e0231-109">Process data from the source.</span></span>

<span data-ttu-id="e0231-110">O restante deste tópico descreve detalhadamente essas etapas.</span><span class="sxs-lookup"><span data-stu-id="e0231-110">The remainder of this topic describes these steps in detail.</span></span>

-   [<span data-ttu-id="e0231-111">Criando o leitor de origem</span><span class="sxs-lookup"><span data-stu-id="e0231-111">Creating the Source Reader</span></span>](#creating-the-source-reader)
-   [<span data-ttu-id="e0231-112">Enumerando formatos de saída</span><span class="sxs-lookup"><span data-stu-id="e0231-112">Enumerating Output Formats</span></span>](#enumerating-output-formats)
-   [<span data-ttu-id="e0231-113">Definindo formatos de saída</span><span class="sxs-lookup"><span data-stu-id="e0231-113">Setting Output Formats</span></span>](#setting-output-formats)
-   [<span data-ttu-id="e0231-114">Processando dados de mídia</span><span class="sxs-lookup"><span data-stu-id="e0231-114">Processing Media Data</span></span>](#using-the-source-reader-to-process-media-data)
-   [<span data-ttu-id="e0231-115">Drenando o pipeline de dados</span><span class="sxs-lookup"><span data-stu-id="e0231-115">Draining the Data Pipeline</span></span>](#draining-the-data-pipeline)
-   [<span data-ttu-id="e0231-116">Obtendo a duração do arquivo</span><span class="sxs-lookup"><span data-stu-id="e0231-116">Getting the File Duration</span></span>](#getting-the-file-duration)
-   [<span data-ttu-id="e0231-117">Atingir</span><span class="sxs-lookup"><span data-stu-id="e0231-117">Seeking</span></span>](#seeking)
-   [<span data-ttu-id="e0231-118">Taxa de reprodução</span><span class="sxs-lookup"><span data-stu-id="e0231-118">Playback Rate</span></span>](#playback-rate)
-   [<span data-ttu-id="e0231-119">Aceleração de hardware</span><span class="sxs-lookup"><span data-stu-id="e0231-119">Hardware Acceleration</span></span>](#hardware-acceleration)
-   [<span data-ttu-id="e0231-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e0231-120">Related topics</span></span>](#related-topics)

## <a name="creating-the-source-reader"></a><span data-ttu-id="e0231-121">Criando o leitor de origem</span><span class="sxs-lookup"><span data-stu-id="e0231-121">Creating the Source Reader</span></span>

<span data-ttu-id="e0231-122">Para criar uma instância do leitor de origem, chame uma das seguintes funções:</span><span class="sxs-lookup"><span data-stu-id="e0231-122">To create an instance of the Source Reader, call one of the following functions:</span></span>



| <span data-ttu-id="e0231-123">Função</span><span class="sxs-lookup"><span data-stu-id="e0231-123">Function</span></span>                                                                                                                                                                                                                                                        | <span data-ttu-id="e0231-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="e0231-124">Description</span></span>                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0231-125"><span id="MFCreateSourceReaderFromURL"></span><span id="mfcreatesourcereaderfromurl"></span><span id="MFCREATESOURCEREADERFROMURL"></span>[**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)</span><span class="sxs-lookup"><span data-stu-id="e0231-125"><span id="MFCreateSourceReaderFromURL"></span><span id="mfcreatesourcereaderfromurl"></span><span id="MFCREATESOURCEREADERFROMURL"></span>[**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)</span></span><br/>                                         | <span data-ttu-id="e0231-126">Usa uma URL como entrada.</span><span class="sxs-lookup"><span data-stu-id="e0231-126">Takes a URL as input.</span></span> <span data-ttu-id="e0231-127">Essa função usa o [resolvedor de origem](source-resolver.md) para criar uma fonte de mídia a partir da URL.</span><span class="sxs-lookup"><span data-stu-id="e0231-127">This function uses the [Source Resolver](source-resolver.md) to create a media source from the URL.</span></span><br/>                                                                       |
| <span data-ttu-id="e0231-128"><span id="MFCreateSourceReaderFromByteStream"></span><span id="mfcreatesourcereaderfrombytestream"></span><span id="MFCREATESOURCEREADERFROMBYTESTREAM"></span>[**MFCreateSourceReaderFromByteStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)</span><span class="sxs-lookup"><span data-stu-id="e0231-128"><span id="MFCreateSourceReaderFromByteStream"></span><span id="mfcreatesourcereaderfrombytestream"></span><span id="MFCREATESOURCEREADERFROMBYTESTREAM"></span>[**MFCreateSourceReaderFromByteStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)</span></span><br/>      | <span data-ttu-id="e0231-129">Usa um ponteiro para um fluxo de bytes.</span><span class="sxs-lookup"><span data-stu-id="e0231-129">Takes a pointer to a byte stream.</span></span> <span data-ttu-id="e0231-130">Essa função também usa o resolvedor de origem para criar a origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="e0231-130">This function also uses the Source Resolver to create the media source.</span></span><br/>                                                                                        |
| <span data-ttu-id="e0231-131"><span id="MFCreateSourceReaderFromMediaSource"></span><span id="mfcreatesourcereaderfrommediasource"></span><span id="MFCREATESOURCEREADERFROMMEDIASOURCE"></span>[**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)</span><span class="sxs-lookup"><span data-stu-id="e0231-131"><span id="MFCreateSourceReaderFromMediaSource"></span><span id="mfcreatesourcereaderfrommediasource"></span><span id="MFCREATESOURCEREADERFROMMEDIASOURCE"></span>[**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)</span></span><br/> | <span data-ttu-id="e0231-132">Usa um ponteiro para uma fonte de mídia que já foi criada.</span><span class="sxs-lookup"><span data-stu-id="e0231-132">Takes a pointer to a media source that has already been created.</span></span> <span data-ttu-id="e0231-133">Essa função é útil para fontes de mídia que o resolvedor de origem não pode criar, como dispositivos de captura ou fontes de mídia personalizadas.</span><span class="sxs-lookup"><span data-stu-id="e0231-133">This function is useful for media sources that the Source Resolver cannot create, such capture devices or custom media sources.</span></span><br/> |



 

<span data-ttu-id="e0231-134">Normalmente, para arquivos de mídia, use [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl).</span><span class="sxs-lookup"><span data-stu-id="e0231-134">Typically, for media files, use [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl).</span></span> <span data-ttu-id="e0231-135">Para dispositivos, como webcams, use [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource).</span><span class="sxs-lookup"><span data-stu-id="e0231-135">For devices, such as webcams, use [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource).</span></span> <span data-ttu-id="e0231-136">(Para obter mais informações sobre como capturar dispositivos no Microsoft Media Foundation, consulte [captura de áudio/vídeo](audio-video-capture.md).)</span><span class="sxs-lookup"><span data-stu-id="e0231-136">(For more information about capture devices in Microsoft Media Foundation, see [Audio/Video Capture](audio-video-capture.md).)</span></span>

<span data-ttu-id="e0231-137">Cada uma dessas funções usa um ponteiro [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) opcional, que é usado para definir várias opções no leitor de origem, conforme descrito nos tópicos de referência para essas funções.</span><span class="sxs-lookup"><span data-stu-id="e0231-137">Each of these functions takes an optional [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer, which is used to set various options on the Source Reader, as described in the reference topics for these functions.</span></span> <span data-ttu-id="e0231-138">Para obter o comportamento padrão, defina esse parâmetro como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="e0231-138">To get the default behavior, set this parameter to **NULL**.</span></span> <span data-ttu-id="e0231-139">Cada função retorna um ponteiro [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) como um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="e0231-139">Each function returns an [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) pointer as an output parameter.</span></span> <span data-ttu-id="e0231-140">Você deve chamar o **CoInitialize (ex)** e a função [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) antes de chamar qualquer uma dessas funções.</span><span class="sxs-lookup"><span data-stu-id="e0231-140">You must call **CoInitialize(Ex)** and [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) function before calling any of these functions.</span></span>

<span data-ttu-id="e0231-141">O código a seguir cria o leitor de origem de uma URL.</span><span class="sxs-lookup"><span data-stu-id="e0231-141">The following code creates the Source Reader from a URL.</span></span>


```C++
int __cdecl wmain(int argc, __in_ecount(argc) PCWSTR* argv)
{
    if (argc < 2)
    {
        return 1;
    }

    const WCHAR *pszURL = argv[1];

    // Initialize the COM runtime.
    HRESULT hr = CoInitializeEx(0, COINIT_MULTITHREADED);
    if (SUCCEEDED(hr))
    {
        // Initialize the Media Foundation platform.
        hr = MFStartup(MF_VERSION);
        if (SUCCEEDED(hr))
        {
            // Create the source reader.
            IMFSourceReader *pReader;
            hr = MFCreateSourceReaderFromURL(pszURL, NULL, &pReader);
            if (SUCCEEDED(hr))
            {
                ReadMediaFile(pReader);
                pReader->Release();
            }
            // Shut down Media Foundation.
            MFShutdown();
        }
        CoUninitialize();
    }
}
```



## <a name="enumerating-output-formats"></a><span data-ttu-id="e0231-142">Enumerando formatos de saída</span><span class="sxs-lookup"><span data-stu-id="e0231-142">Enumerating Output Formats</span></span>

<span data-ttu-id="e0231-143">Cada fonte de mídia tem pelo menos um fluxo.</span><span class="sxs-lookup"><span data-stu-id="e0231-143">Every media source has at least one stream.</span></span> <span data-ttu-id="e0231-144">Por exemplo, um arquivo de vídeo pode conter um fluxo de vídeo e um fluxo de áudio.</span><span class="sxs-lookup"><span data-stu-id="e0231-144">For example, a video file might contain a video stream and an audio stream.</span></span> <span data-ttu-id="e0231-145">O formato de cada fluxo é descrito usando um tipo de mídia, representado pela interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) .</span><span class="sxs-lookup"><span data-stu-id="e0231-145">The format of each stream is described using a media type, represented by the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface.</span></span> <span data-ttu-id="e0231-146">Para obter mais informações sobre tipos de mídia, consulte [tipos de mídia](media-types.md).</span><span class="sxs-lookup"><span data-stu-id="e0231-146">For more information about media types, see [Media Types](media-types.md).</span></span> <span data-ttu-id="e0231-147">Você deve examinar o tipo de mídia para entender o formato dos dados obtidos do leitor de origem.</span><span class="sxs-lookup"><span data-stu-id="e0231-147">You must examine the media type to understand the format of the data that you get from the Source Reader.</span></span>

<span data-ttu-id="e0231-148">Inicialmente, cada fluxo tem um formato padrão, que você pode encontrar chamando o método [**IMFSourceReader:: GetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) :</span><span class="sxs-lookup"><span data-stu-id="e0231-148">Initially, every stream has a default format, which you can find by calling the [**IMFSourceReader::GetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) method:</span></span>

<span data-ttu-id="e0231-149">Para cada fluxo, a origem de mídia oferece uma lista de possíveis tipos de mídia para esse fluxo.</span><span class="sxs-lookup"><span data-stu-id="e0231-149">For each stream, the media source offers a list of possible media types for that stream.</span></span> <span data-ttu-id="e0231-150">O número de tipos depende da origem.</span><span class="sxs-lookup"><span data-stu-id="e0231-150">The number of types depends on the source.</span></span> <span data-ttu-id="e0231-151">Se a origem representar um arquivo de mídia, normalmente haverá apenas um tipo por fluxo.</span><span class="sxs-lookup"><span data-stu-id="e0231-151">If the source represents a media file, there is typically only one type per stream.</span></span> <span data-ttu-id="e0231-152">Uma webcam, por outro lado, pode ser capaz de transmitir vídeo em vários formatos diferentes.</span><span class="sxs-lookup"><span data-stu-id="e0231-152">A webcam, on the other hand, might be able to stream video in several different formats.</span></span> <span data-ttu-id="e0231-153">Nesse caso, o aplicativo pode selecionar qual formato usar na lista de tipos de mídia.</span><span class="sxs-lookup"><span data-stu-id="e0231-153">In that case, the application can select which format to use from the list of media types.</span></span>

<span data-ttu-id="e0231-154">Para obter um dos tipos de mídia para um fluxo, chame o método [**IMFSourceReader:: GetNativeMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype) .</span><span class="sxs-lookup"><span data-stu-id="e0231-154">To get one of the media types for a stream, call the [**IMFSourceReader::GetNativeMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype) method.</span></span> <span data-ttu-id="e0231-155">Esse método usa dois parâmetros de índice: o índice do fluxo e um índice na lista de tipos de mídia para o fluxo.</span><span class="sxs-lookup"><span data-stu-id="e0231-155">This method takes two index parameters: The index of the stream, and an index into the list of media types for the stream.</span></span> <span data-ttu-id="e0231-156">Para enumerar todos os tipos de um fluxo, aumente o índice da lista enquanto mantém a constante de índice de fluxo.</span><span class="sxs-lookup"><span data-stu-id="e0231-156">To enumerate all the types for a stream, increment the list index while keeping the stream index constant.</span></span> <span data-ttu-id="e0231-157">Quando o índice da lista sai dos limites, **GetNativeMediaType** retorna **MF \_ E \_ não \_ mais \_ tipos**.</span><span class="sxs-lookup"><span data-stu-id="e0231-157">When the list index goes out of bounds, **GetNativeMediaType** returns **MF\_E\_NO\_MORE\_TYPES**.</span></span>


```C++
HRESULT EnumerateTypesForStream(IMFSourceReader *pReader, DWORD dwStreamIndex)
{
    HRESULT hr = S_OK;
    DWORD dwMediaTypeIndex = 0;

    while (SUCCEEDED(hr))
    {
        IMFMediaType *pType = NULL;
        hr = pReader->GetNativeMediaType(dwStreamIndex, dwMediaTypeIndex, &pType);
        if (hr == MF_E_NO_MORE_TYPES)
        {
            hr = S_OK;
            break;
        }
        else if (SUCCEEDED(hr))
        {
            // Examine the media type. (Not shown.)

            pType->Release();
        }
        ++dwMediaTypeIndex;
    }
    return hr;
}
```



<span data-ttu-id="e0231-158">Para enumerar os tipos de mídia para cada fluxo, aumente o índice de fluxo.</span><span class="sxs-lookup"><span data-stu-id="e0231-158">To enumerate the media types for every stream, increment the stream index.</span></span> <span data-ttu-id="e0231-159">Quando o índice de fluxo sai dos limites, [**GetNativeMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype) retorna **MF \_ E \_ INVALIDSTREAMNUMBER**.</span><span class="sxs-lookup"><span data-stu-id="e0231-159">When the stream index goes out of bounds, [**GetNativeMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype) returns **MF\_E\_INVALIDSTREAMNUMBER**.</span></span>


```C++
HRESULT EnumerateTypesForStream(IMFSourceReader *pReader, DWORD dwStreamIndex)
{
    HRESULT hr = S_OK;
    DWORD dwMediaTypeIndex = 0;

    while (SUCCEEDED(hr))
    {
        IMFMediaType *pType = NULL;
        hr = pReader->GetNativeMediaType(dwStreamIndex, dwMediaTypeIndex, &pType);
        if (hr == MF_E_NO_MORE_TYPES)
        {
            hr = S_OK;
            break;
        }
        else if (SUCCEEDED(hr))
        {
            // Examine the media type. (Not shown.)

            pType->Release();
        }
        ++dwMediaTypeIndex;
    }
    return hr;
}
```



## <a name="setting-output-formats"></a><span data-ttu-id="e0231-160">Definindo formatos de saída</span><span class="sxs-lookup"><span data-stu-id="e0231-160">Setting Output Formats</span></span>

<span data-ttu-id="e0231-161">Para alterar o formato de saída, chame o método [**IMFSourceReader:: SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype) .</span><span class="sxs-lookup"><span data-stu-id="e0231-161">To change the output format, call the [**IMFSourceReader::SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype) method.</span></span> <span data-ttu-id="e0231-162">Esse método usa o índice de fluxo e um tipo de mídia:</span><span class="sxs-lookup"><span data-stu-id="e0231-162">This method takes the stream index and a media type:</span></span>

``` syntax
hr = pReader->SetCurrentMediaType(dwStreamIndex, pMediaType);
```

<span data-ttu-id="e0231-163">Para o tipo de mídia, depende se você deseja inserir um decodificador.</span><span class="sxs-lookup"><span data-stu-id="e0231-163">For the media type, it depends on whether you want to insert a decoder.</span></span>

-   <span data-ttu-id="e0231-164">Para obter dados diretamente da fonte sem decodificá-los, use um dos tipos retornados por [**GetNativeMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype).</span><span class="sxs-lookup"><span data-stu-id="e0231-164">To get data directly from the source without decoding it, use one of the types returned by [**GetNativeMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype).</span></span>
-   <span data-ttu-id="e0231-165">Para decodificar o fluxo, crie um novo tipo de mídia que descreva o formato descompactado desejado.</span><span class="sxs-lookup"><span data-stu-id="e0231-165">To decode the stream, create a new media type that describes the desired uncompressed format.</span></span>

<span data-ttu-id="e0231-166">No caso do decodificador, crie o tipo de mídia da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="e0231-166">In the case of the decoder, create the media type as follows:</span></span>

1.  <span data-ttu-id="e0231-167">Chame [**MFCreateMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype) para criar um novo tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="e0231-167">Call [**MFCreateMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype) to create a new media type.</span></span>
2.  <span data-ttu-id="e0231-168">Defina o atributo de [**\_ \_ \_ tipo principal MF MT**](mf-mt-major-type-attribute.md) para especificar áudio ou vídeo.</span><span class="sxs-lookup"><span data-stu-id="e0231-168">Set the [**MF\_MT\_MAJOR\_TYPE**](mf-mt-major-type-attribute.md) attribute to specify audio or video.</span></span>
3.  <span data-ttu-id="e0231-169">Defina o atributo de [**\_ \_ subtipo MF MT**](mf-mt-subtype-attribute.md) para especificar o subtipo do formato de decodificação.</span><span class="sxs-lookup"><span data-stu-id="e0231-169">Set the [**MF\_MT\_SUBTYPE**](mf-mt-subtype-attribute.md) attribute to specify the subtype of the decoding format.</span></span> <span data-ttu-id="e0231-170">(Consulte GUIDs de [subtipo de áudio](audio-subtype-guids.md) e [GUIDs de subtipo de vídeo](video-subtype-guids.md).)</span><span class="sxs-lookup"><span data-stu-id="e0231-170">(See [Audio Subtype GUIDs](audio-subtype-guids.md) and [Video Subtype GUIDs](video-subtype-guids.md).)</span></span>
4.  <span data-ttu-id="e0231-171">Chame [**IMFSourceReader:: SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype).</span><span class="sxs-lookup"><span data-stu-id="e0231-171">Call [**IMFSourceReader::SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype).</span></span>

<span data-ttu-id="e0231-172">O leitor de origem carregará automaticamente o decodificador.</span><span class="sxs-lookup"><span data-stu-id="e0231-172">The Source Reader will automatically load the decoder.</span></span> <span data-ttu-id="e0231-173">Para obter os detalhes completos do formato decodificado, chame [**IMFSourceReader:: GetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) após a chamada para [**SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype)</span><span class="sxs-lookup"><span data-stu-id="e0231-173">To get the complete details of the decoded format, call [**IMFSourceReader::GetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) after the call to [**SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype)</span></span>

<span data-ttu-id="e0231-174">O código a seguir configura o fluxo de vídeo para RGB-32 e o fluxo de áudio para áudio PCM.</span><span class="sxs-lookup"><span data-stu-id="e0231-174">The following code configures the video stream for RGB-32 and the audio stream for PCM audio.</span></span>


```C++
HRESULT ConfigureDecoder(IMFSourceReader *pReader, DWORD dwStreamIndex)
{
    IMFMediaType *pNativeType = NULL;
    IMFMediaType *pType = NULL;

    // Find the native format of the stream.
    HRESULT hr = pReader->GetNativeMediaType(dwStreamIndex, 0, &pNativeType);
    if (FAILED(hr))
    {
        return hr;
    }

    GUID majorType, subtype;

    // Find the major type.
    hr = pNativeType->GetGUID(MF_MT_MAJOR_TYPE, &majorType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Define the output type.
    hr = MFCreateMediaType(&pType);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetGUID(MF_MT_MAJOR_TYPE, majorType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Select a subtype.
    if (majorType == MFMediaType_Video)
    {
        subtype= MFVideoFormat_RGB32;
    }
    else if (majorType == MFMediaType_Audio)
    {
        subtype = MFAudioFormat_PCM;
    }
    else
    {
        // Unrecognized type. Skip.
        goto done;
    }

    hr = pType->SetGUID(MF_MT_SUBTYPE, subtype);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the uncompressed format.
    hr = pReader->SetCurrentMediaType(dwStreamIndex, NULL, pType);
    if (FAILED(hr))
    {
        goto done;
    }

done:
    SafeRelease(&pNativeType);
    SafeRelease(&pType);
    return hr;
}
```



## <a name="processing-media-data"></a><span data-ttu-id="e0231-175">Processando dados de mídia</span><span class="sxs-lookup"><span data-stu-id="e0231-175">Processing Media Data</span></span>

<span data-ttu-id="e0231-176">Para obter dados de mídia da origem, chame o método [**IMFSourceReader:: ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) , conforme mostrado no código a seguir.</span><span class="sxs-lookup"><span data-stu-id="e0231-176">To get media data from the source, call the [**IMFSourceReader::ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) method, as shown in the following code.</span></span>


```C++
        DWORD streamIndex, flags;
        LONGLONG llTimeStamp;

        hr = pReader->ReadSample(
            MF_SOURCE_READER_ANY_STREAM,    // Stream index.
            0,                              // Flags.
            &streamIndex,                   // Receives the actual stream index. 
            &flags,                         // Receives status flags.
            &llTimeStamp,                   // Receives the time stamp.
            &pSample                        // Receives the sample or NULL.
            );
```



<span data-ttu-id="e0231-177">O primeiro parâmetro é o índice do fluxo para o qual você deseja obter dados.</span><span class="sxs-lookup"><span data-stu-id="e0231-177">The first parameter is the index of the stream for which you want to get data.</span></span> <span data-ttu-id="e0231-178">Você também pode especificar **o \_ leitor de origem MF \_ \_ qualquer \_ fluxo** para obter os próximos dados disponíveis de qualquer fluxo.</span><span class="sxs-lookup"><span data-stu-id="e0231-178">You can also specify **MF\_SOURCE\_READER\_ANY\_STREAM** to get the next available data from any stream.</span></span> <span data-ttu-id="e0231-179">O segundo parâmetro contém sinalizadores opcionais; consulte [**\_ sinalizador de \_ \_ controle de \_ leitor de origem MF**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_control_flag) para obter uma lista desses.</span><span class="sxs-lookup"><span data-stu-id="e0231-179">The second parameter contains optional flags; see [**MF\_SOURCE\_READER\_CONTROL\_FLAG**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_control_flag) for a list of these.</span></span> <span data-ttu-id="e0231-180">O terceiro parâmetro recebe o índice do fluxo que realmente produz os dados.</span><span class="sxs-lookup"><span data-stu-id="e0231-180">The third parameter receives the index of the stream that actually produces the data.</span></span> <span data-ttu-id="e0231-181">Você precisará dessas informações se definir o primeiro parâmetro para o **\_ leitor de origem MF \_ \_ qualquer \_ fluxo**.</span><span class="sxs-lookup"><span data-stu-id="e0231-181">You will need this information if you set the first parameter to **MF\_SOURCE\_READER\_ANY\_STREAM**.</span></span> <span data-ttu-id="e0231-182">O quarto parâmetro recebe sinalizadores de status, indicando vários eventos que podem ocorrer durante a leitura dos dados, como alterações de formato no fluxo.</span><span class="sxs-lookup"><span data-stu-id="e0231-182">The fourth parameter receives status flags, indicating various events that can occur while reading the data, such as format changes in the stream.</span></span> <span data-ttu-id="e0231-183">Para obter uma lista de sinalizadores de status, consulte [**\_ sinalizador do \_ leitor \_ de origem MF**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_flag).</span><span class="sxs-lookup"><span data-stu-id="e0231-183">For a list of status flags, see [**MF\_SOURCE\_READER\_FLAG**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_flag).</span></span>

<span data-ttu-id="e0231-184">Se a origem da mídia for capaz de produzir dados para o fluxo solicitado, o último parâmetro de [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) receberá um ponteiro para a interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) de um objeto de exemplo de mídia.</span><span class="sxs-lookup"><span data-stu-id="e0231-184">If the media source is able to produce data for the requested stream, the last parameter of [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) receives a pointer to the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface of a media sample object.</span></span> <span data-ttu-id="e0231-185">Use o exemplo de mídia para:</span><span class="sxs-lookup"><span data-stu-id="e0231-185">Use the media sample to:</span></span>

-   <span data-ttu-id="e0231-186">Obtenha um ponteiro para os dados de mídia.</span><span class="sxs-lookup"><span data-stu-id="e0231-186">Get a pointer to the media data.</span></span>
-   <span data-ttu-id="e0231-187">Obtenha a hora da apresentação e a duração da amostra.</span><span class="sxs-lookup"><span data-stu-id="e0231-187">Get the presentation time and sample duration.</span></span>
-   <span data-ttu-id="e0231-188">Obtenha atributos que descrevem o entrelaçamento, o campo predominância e outros aspectos do exemplo.</span><span class="sxs-lookup"><span data-stu-id="e0231-188">Get attributes that describe interlacing, field dominance, and other aspects of the sample.</span></span>

<span data-ttu-id="e0231-189">O conteúdo dos dados de mídia depende do formato do fluxo.</span><span class="sxs-lookup"><span data-stu-id="e0231-189">The contents of the media data depend on the format of the stream.</span></span> <span data-ttu-id="e0231-190">Para um fluxo de vídeo descompactado, cada amostra de mídia contém um único quadro de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e0231-190">For an uncompressed video stream, each media sample contains a single video frame.</span></span> <span data-ttu-id="e0231-191">Para um fluxo de áudio descompactado, cada amostra de mídia contém uma sequência de quadros de áudio.</span><span class="sxs-lookup"><span data-stu-id="e0231-191">For an uncompressed audio stream, each media sample contains a sequence of audio frames.</span></span>

<span data-ttu-id="e0231-192">O método [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) pode retornar **S \_ OK** e, ainda assim, não retornar um exemplo de mídia no parâmetro *pSample* .</span><span class="sxs-lookup"><span data-stu-id="e0231-192">The [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) method can return **S\_OK** and yet not return a media sample in the *pSample* parameter.</span></span> <span data-ttu-id="e0231-193">Por exemplo, quando você chega ao final do arquivo, **ReadSample** define o sinalizador **\_ \_ READERF \_ ENDOFSTREAM de origem MF** em *dwFlags* e define *pSample* como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="e0231-193">For example, when you reach the end of the file, **ReadSample** sets the **MF\_SOURCE\_READERF\_ENDOFSTREAM** flag in *dwFlags* and sets *pSample* to **NULL**.</span></span> <span data-ttu-id="e0231-194">Nesse caso, o método **ReadSample** retorna **S \_ OK** porque nenhum erro ocorreu, mesmo que o parâmetro *pSample* esteja definido como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="e0231-194">In this case, the **ReadSample** method returns **S\_OK** because no error has occurred, even though the *pSample* parameter is set to **NULL**.</span></span> <span data-ttu-id="e0231-195">Portanto, sempre verifique o valor de *pSample* antes de desreferenciá-lo.</span><span class="sxs-lookup"><span data-stu-id="e0231-195">Therefore, always check the value of *pSample* before you dereference it.</span></span>

<span data-ttu-id="e0231-196">O código a seguir mostra como chamar [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) em um loop e verificar as informações retornadas pelo método, até que o final do arquivo de mídia seja atingido.</span><span class="sxs-lookup"><span data-stu-id="e0231-196">The following code shows how to call [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) in a loop and check the information returned by the method, until the end of the media file is reached.</span></span>


```C++
HRESULT ProcessSamples(IMFSourceReader *pReader)
{
    HRESULT hr = S_OK;
    IMFSample *pSample = NULL;
    size_t  cSamples = 0;

    bool quit = false;
    while (!quit)
    {
        DWORD streamIndex, flags;
        LONGLONG llTimeStamp;

        hr = pReader->ReadSample(
            MF_SOURCE_READER_ANY_STREAM,    // Stream index.
            0,                              // Flags.
            &streamIndex,                   // Receives the actual stream index. 
            &flags,                         // Receives status flags.
            &llTimeStamp,                   // Receives the time stamp.
            &pSample                        // Receives the sample or NULL.
            );

        if (FAILED(hr))
        {
            break;
        }

        wprintf(L"Stream %d (%I64d)\n", streamIndex, llTimeStamp);
        if (flags & MF_SOURCE_READERF_ENDOFSTREAM)
        {
            wprintf(L"\tEnd of stream\n");
            quit = true;
        }
        if (flags & MF_SOURCE_READERF_NEWSTREAM)
        {
            wprintf(L"\tNew stream\n");
        }
        if (flags & MF_SOURCE_READERF_NATIVEMEDIATYPECHANGED)
        {
            wprintf(L"\tNative type changed\n");
        }
        if (flags & MF_SOURCE_READERF_CURRENTMEDIATYPECHANGED)
        {
            wprintf(L"\tCurrent type changed\n");
        }
        if (flags & MF_SOURCE_READERF_STREAMTICK)
        {
            wprintf(L"\tStream tick\n");
        }

        if (flags & MF_SOURCE_READERF_NATIVEMEDIATYPECHANGED)
        {
            // The format changed. Reconfigure the decoder.
            hr = ConfigureDecoder(pReader, streamIndex);
            if (FAILED(hr))
            {
                break;
            }
        }

        if (pSample)
        {
            ++cSamples;
        }

        SafeRelease(&pSample);
    }

    if (FAILED(hr))
    {
        wprintf(L"ProcessSamples FAILED, hr = 0x%x\n", hr);
    }
    else
    {
        wprintf(L"Processed %d samples\n", cSamples);
    }
    SafeRelease(&pSample);
    return hr;
}
```



## <a name="draining-the-data-pipeline"></a><span data-ttu-id="e0231-197">Drenando o pipeline de dados</span><span class="sxs-lookup"><span data-stu-id="e0231-197">Draining the Data Pipeline</span></span>

<span data-ttu-id="e0231-198">Durante o processamento de dados, um decodificador ou outra transformação pode armazenar em buffer exemplos de entrada.</span><span class="sxs-lookup"><span data-stu-id="e0231-198">During data processing, a decoder or other transform might buffer input samples.</span></span> <span data-ttu-id="e0231-199">No diagrama a seguir, o aplicativo chama [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) e recebe um exemplo com um tempo de apresentação igual a *T1*.</span><span class="sxs-lookup"><span data-stu-id="e0231-199">In the following diagram, the application calls [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) and receives a sample with a presentation time equal to *t1*.</span></span> <span data-ttu-id="e0231-200">O decodificador está mantendo amostras para *T2* e *T3*.</span><span class="sxs-lookup"><span data-stu-id="e0231-200">The decoder is holding samples for *t2* and *t3*.</span></span>

![uma ilustração que mostra o armazenamento em buffer em um decodificador.](images/sourcereader02.png)

<span data-ttu-id="e0231-202">Na próxima chamada para [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample), o leitor de origem pode fornecer o *T4* ao decodificador e retornar *T2* ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e0231-202">On the next call to [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample), the Source Reader might give *t4* to the decoder and return *t2* to the application.</span></span>

<span data-ttu-id="e0231-203">Se você quiser decodificar todos os exemplos que estão atualmente em buffer no decodificador, sem passar quaisquer novas amostras para o decodificador, defina o sinalizador de **\_ \_ \_ \_ drenagem CONTROLF do leitor de origem MF** no parâmetro *dwControlFlags* de [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample).</span><span class="sxs-lookup"><span data-stu-id="e0231-203">If you want to decode all of the samples that are currently buffered in the decoder, without passing any new samples to the decoder, set the **MF\_SOURCE\_READER\_CONTROLF\_DRAIN** flag in the *dwControlFlags* parameter of [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample).</span></span> <span data-ttu-id="e0231-204">Continue a fazer isso em um loop até que **ReadSample** retorne um ponteiro de exemplo **nulo** .</span><span class="sxs-lookup"><span data-stu-id="e0231-204">Continue to do this in a loop until **ReadSample** returns a **NULL** sample pointer.</span></span> <span data-ttu-id="e0231-205">Dependendo de como o decodificador armazena em buffer exemplos, isso pode acontecer imediatamente ou após várias chamadas para **ReadSample**.</span><span class="sxs-lookup"><span data-stu-id="e0231-205">Depending on how the decoder buffers samples, that might happen immediately or after several calls to **ReadSample**.</span></span>

## <a name="getting-the-file-duration"></a><span data-ttu-id="e0231-206">Obtendo a duração do arquivo</span><span class="sxs-lookup"><span data-stu-id="e0231-206">Getting the File Duration</span></span>

<span data-ttu-id="e0231-207">Para obter a duração de um arquivo de mídia, chame o método [**IMFSourceReader:: Getpresentationattribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) e solicite o atributo de [**\_ \_ duração de PD de MF**](mf-pd-duration-attribute.md) , conforme mostrado no código a seguir.</span><span class="sxs-lookup"><span data-stu-id="e0231-207">To get the duration of a media file, call the [**IMFSourceReader::GetPresentationAttribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) method and request the [**MF\_PD\_DURATION**](mf-pd-duration-attribute.md) attribute, as shown in the following code.</span></span>


```C++
HRESULT GetDuration(IMFSourceReader *pReader, LONGLONG *phnsDuration)
{
    PROPVARIANT var;
    HRESULT hr = pReader->GetPresentationAttribute(MF_SOURCE_READER_MEDIASOURCE, 
        MF_PD_DURATION, &var);
    if (SUCCEEDED(hr))
    {
        hr = PropVariantToInt64(var, phnsDuration);
        PropVariantClear(&var);
    }
    return hr;
}
```



<span data-ttu-id="e0231-208">A função mostrada aqui Obtém a duração em unidades de 100 nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="e0231-208">The function shown here gets the duration in 100-nanosecond units.</span></span> <span data-ttu-id="e0231-209">Divida por 10 milhões para obter a duração em segundos.</span><span class="sxs-lookup"><span data-stu-id="e0231-209">Divide by 10,000,000 to get the duration in seconds.</span></span>

## <a name="seeking"></a><span data-ttu-id="e0231-210">Atingir</span><span class="sxs-lookup"><span data-stu-id="e0231-210">Seeking</span></span>

<span data-ttu-id="e0231-211">Uma fonte de mídia que obtém dados de um arquivo local geralmente pode buscar posições arbitrárias no arquivo.</span><span class="sxs-lookup"><span data-stu-id="e0231-211">A media source that gets data from a local file can usually seek to arbitrary positions in the file.</span></span> <span data-ttu-id="e0231-212">Dispositivos de captura, como webcams, geralmente não podem buscar, porque os dados estão ativos.</span><span class="sxs-lookup"><span data-stu-id="e0231-212">Capture devices such as webcams generally cannot seek, because the data is live.</span></span> <span data-ttu-id="e0231-213">Uma fonte que transmite dados em uma rede pode ser capaz de buscar, dependendo do protocolo de streaming de rede.</span><span class="sxs-lookup"><span data-stu-id="e0231-213">A source that streams data over a network might be able to seek, depending on the network streaming protocol.</span></span>

<span data-ttu-id="e0231-214">Para descobrir se uma fonte de mídia pode buscar, chame [**IMFSourceReader:: Getpresentationattribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) e solicite o atributo de [ \_ \_ \_ \_ características mediary do leitor de origem MF](mf-source-reader-mediasource-characteristics.md) , conforme mostrado no código a seguir:</span><span class="sxs-lookup"><span data-stu-id="e0231-214">To find out whether a media source can seek, call [**IMFSourceReader::GetPresentationAttribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) and request the [MF\_SOURCE\_READER\_MEDIASOURCE\_CHARACTERISTICS](mf-source-reader-mediasource-characteristics.md) attribute, as shown in the following code:</span></span>


```C++
HRESULT GetSourceFlags(IMFSourceReader *pReader, ULONG *pulFlags)
{
    ULONG flags = 0;

    PROPVARIANT var;
    PropVariantInit(&var);

    HRESULT hr = pReader->GetPresentationAttribute(
        MF_SOURCE_READER_MEDIASOURCE, 
        MF_SOURCE_READER_MEDIASOURCE_CHARACTERISTICS, 
        &var);

    if (SUCCEEDED(hr))
    {
        hr = PropVariantToUInt32(var, &flags);
    }
    if (SUCCEEDED(hr))
    {
        *pulFlags = flags;
    }

    PropVariantClear(&var);
    return hr;
}
```



<span data-ttu-id="e0231-215">Essa função obtém um conjunto de sinalizadores de recursos da origem.</span><span class="sxs-lookup"><span data-stu-id="e0231-215">This function gets a set of capabilities flags from the source.</span></span> <span data-ttu-id="e0231-216">Esses sinalizadores são definidos na enumeração [**de \_ características do MFMEDIASOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) .</span><span class="sxs-lookup"><span data-stu-id="e0231-216">These flags are defined in the [**MFMEDIASOURCE\_CHARACTERISTICS**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) enumeration.</span></span> <span data-ttu-id="e0231-217">Dois sinalizadores estão relacionados à busca:</span><span class="sxs-lookup"><span data-stu-id="e0231-217">Two flags relate to seeking:</span></span>



| <span data-ttu-id="e0231-218">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="e0231-218">Flag</span></span>                                                                                                                                      | <span data-ttu-id="e0231-219">Descrição</span><span class="sxs-lookup"><span data-stu-id="e0231-219">Description</span></span>                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0231-220"><span id="MFMEDIASOURCE_CAN_SEEK"></span><span id="mfmediasource_can_seek"></span>**MFMEDIASOURCE \_ pode \_ buscar**</span><span class="sxs-lookup"><span data-stu-id="e0231-220"><span id="MFMEDIASOURCE_CAN_SEEK"></span><span id="mfmediasource_can_seek"></span>**MFMEDIASOURCE\_CAN\_SEEK**</span></span><br/>                 | <span data-ttu-id="e0231-221">A origem pode buscar.</span><span class="sxs-lookup"><span data-stu-id="e0231-221">The source can seek.</span></span><br/>                                                                                                                                                                            |
| <span data-ttu-id="e0231-222"><span id="MFMEDIASOURCE_HAS_SLOW_SEEK"></span><span id="mfmediasource_has_slow_seek"></span>**MFMEDIASOURCE \_ tem \_ uma \_ busca lenta**</span><span class="sxs-lookup"><span data-stu-id="e0231-222"><span id="MFMEDIASOURCE_HAS_SLOW_SEEK"></span><span id="mfmediasource_has_slow_seek"></span>**MFMEDIASOURCE\_HAS\_SLOW\_SEEK**</span></span><br/> | <span data-ttu-id="e0231-223">A busca pode levar muito tempo para ser concluída.</span><span class="sxs-lookup"><span data-stu-id="e0231-223">Seeking might take a long time to complete.</span></span> <span data-ttu-id="e0231-224">Por exemplo, a origem pode precisar baixar o arquivo inteiro antes que ele possa ser buscado.</span><span class="sxs-lookup"><span data-stu-id="e0231-224">For example, the source might need to download the entire file before it can seek.</span></span> <span data-ttu-id="e0231-225">(Não há critérios estritos para uma origem retornar esse sinalizador.)</span><span class="sxs-lookup"><span data-stu-id="e0231-225">(There are no strict criteria for a source to return this flag.)</span></span><br/> |



 

<span data-ttu-id="e0231-226">Os testes de código a seguir para o **MFMEDIASOURCE \_ podem \_ buscar** o sinalizador.</span><span class="sxs-lookup"><span data-stu-id="e0231-226">The following code tests for the **MFMEDIASOURCE\_CAN\_SEEK** flag.</span></span>


```C++
BOOL SourceCanSeek(IMFSourceReader *pReader)
{
    BOOL bCanSeek = FALSE;
    ULONG flags;
    if (SUCCEEDED(GetSourceFlags(pReader, &flags)))
    {
        bCanSeek = ((flags & MFMEDIASOURCE_CAN_SEEK) == MFMEDIASOURCE_CAN_SEEK);
    }
    return bCanSeek;
}
```



<span data-ttu-id="e0231-227">Para buscar, chame o método [**IMFSourceReader:: SetCurrentPosition**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentposition) , conforme mostrado no código a seguir.</span><span class="sxs-lookup"><span data-stu-id="e0231-227">To seek, call the [**IMFSourceReader::SetCurrentPosition**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentposition) method, as shown in the following code.</span></span>


```C++
HRESULT SetPosition(IMFSourceReader *pReader, const LONGLONG& hnsPosition)
{
    PROPVARIANT var;
    HRESULT hr = InitPropVariantFromInt64(hnsPosition, &var);
    if (SUCCEEDED(hr))
    {
        hr = pReader->SetCurrentPosition(GUID_NULL, var);
        PropVariantClear(&var);
    }
    return hr;
}
```



<span data-ttu-id="e0231-228">O primeiro parâmetro fornece o formato de hora que você está usando para especificar a posição de busca.</span><span class="sxs-lookup"><span data-stu-id="e0231-228">The first parameter gives the time format that you are using to specify the seek position.</span></span> <span data-ttu-id="e0231-229">Todas as fontes de mídia no Media Foundation são necessárias para dar suporte a unidades de 100 nanossegundos, indicadas pelo valor **GUID \_ NULL**.</span><span class="sxs-lookup"><span data-stu-id="e0231-229">All media sources in Media Foundation are required to support 100-nanosecond units, indicated by the value **GUID\_NULL**.</span></span> <span data-ttu-id="e0231-230">O segundo parâmetro é um **PROPVARIANT** que contém a posição de busca.</span><span class="sxs-lookup"><span data-stu-id="e0231-230">The second parameter is a **PROPVARIANT** that contains the seek position.</span></span> <span data-ttu-id="e0231-231">Para unidades de tempo de 100 a nanossegundos, o tipo de dados é **LONGLONG**.</span><span class="sxs-lookup"><span data-stu-id="e0231-231">For 100-nanosecond time units, the data type is **LONGLONG**.</span></span>

<span data-ttu-id="e0231-232">Lembre-se de que nem todas as fontes de mídia fornecem busca com precisão de quadro.</span><span class="sxs-lookup"><span data-stu-id="e0231-232">Be aware that not every media source provides frame-accurate seeking.</span></span> <span data-ttu-id="e0231-233">A precisão da busca depende de vários fatores, como o intervalo de quadros-chave, se o arquivo de mídia contém um índice e se os dados têm uma taxa de bits constante ou variável.</span><span class="sxs-lookup"><span data-stu-id="e0231-233">The accuracy of seeking depends on several factors, such as the key frame interval, whether the media file contains an index, and whether the data has a constant or variable bit rate.</span></span> <span data-ttu-id="e0231-234">Portanto, depois de buscar uma posição em um arquivo, não há nenhuma garantia de que o carimbo de data/hora no próximo exemplo corresponderá exatamente à posição solicitada.</span><span class="sxs-lookup"><span data-stu-id="e0231-234">Therefore, after you seek to a position in a file, there is no guarantee that the time stamp on the next sample will exactly match the requested position.</span></span> <span data-ttu-id="e0231-235">Em geral, a posição real não será posterior à posição solicitada, para que você possa descartar amostras até atingir o ponto desejado no fluxo.</span><span class="sxs-lookup"><span data-stu-id="e0231-235">Generally, the actual position will not be later than the requested position, so you can discard samples until you reach the desired point in the stream.</span></span>

## <a name="playback-rate"></a><span data-ttu-id="e0231-236">Taxa de reprodução</span><span class="sxs-lookup"><span data-stu-id="e0231-236">Playback Rate</span></span>

<span data-ttu-id="e0231-237">Embora você possa definir a taxa de reprodução usando o leitor de origem, normalmente isso não é muito útil, pelos seguintes motivos:</span><span class="sxs-lookup"><span data-stu-id="e0231-237">Although you can set the playback rate using the Source Reader, doing is typically not very useful, for the following reasons:</span></span>

-   <span data-ttu-id="e0231-238">O leitor de origem não dá suporte à reprodução inversa, mesmo se a origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="e0231-238">The Source Reader does not support reverse playback, even if the media source does.</span></span>
-   <span data-ttu-id="e0231-239">O aplicativo controla os tempos de apresentação, para que o aplicativo possa implementar uma reprodução rápida ou lenta sem definir a taxa na origem.</span><span class="sxs-lookup"><span data-stu-id="e0231-239">The application controls the presentation times, so the application can implement fast or slow play without setting the rate on the source.</span></span>
-   <span data-ttu-id="e0231-240">Algumas fontes de mídia dão suporte ao modo de *finamento* , em que a fonte fornece menos amostras — normalmente apenas os quadros-chave.</span><span class="sxs-lookup"><span data-stu-id="e0231-240">Some media sources support *thinning* mode, where the source delivers fewer samples—typically just the key frames.</span></span> <span data-ttu-id="e0231-241">No entanto, se você quiser descartar quadros não-chave, poderá verificar cada exemplo para o atributo [MFSampleExtension \_ CleanPoint](mfsampleextension-cleanpoint-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="e0231-241">However, if you want to drop non-key frames, you can check each sample for the [MFSampleExtension\_CleanPoint](mfsampleextension-cleanpoint-attribute.md) attribute.</span></span>

<span data-ttu-id="e0231-242">Para definir a taxa de reprodução usando o leitor de origem, chame o método [**IMFSourceReader:: GetServiceForStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getserviceforstream) para obter as interfaces [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) e [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) da origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="e0231-242">To set the playback rate using the Source Reader, call the [**IMFSourceReader::GetServiceForStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getserviceforstream) method to get the [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) and [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) interfaces from the media source.</span></span>

## <a name="hardware-acceleration"></a><span data-ttu-id="e0231-243">Aceleração de hardware</span><span class="sxs-lookup"><span data-stu-id="e0231-243">Hardware Acceleration</span></span>

<span data-ttu-id="e0231-244">O leitor de origem é compatível com o Microsoft DirectX Video Acceleration (DXVA) 2,0 para decodificação de vídeo acelerada por hardware.</span><span class="sxs-lookup"><span data-stu-id="e0231-244">The Source Reader is compatible with Microsoft DirectX Video Acceleration (DXVA) 2.0 for hardware accelerated video decoding.</span></span> <span data-ttu-id="e0231-245">Para usar o DXVA com o leitor de origem, execute as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="e0231-245">To use DXVA with the Source Reader, perform the following steps.</span></span>

1.  <span data-ttu-id="e0231-246">Crie um dispositivo Microsoft Direct3D.</span><span class="sxs-lookup"><span data-stu-id="e0231-246">Create a Microsoft Direct3D device.</span></span>
2.  <span data-ttu-id="e0231-247">Chame a função [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9) para criar o Gerenciador de dispositivos do Direct3D.</span><span class="sxs-lookup"><span data-stu-id="e0231-247">Call the [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9) function to create the Direct3D device manager.</span></span> <span data-ttu-id="e0231-248">Essa função obtém um ponteiro para a interface [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) .</span><span class="sxs-lookup"><span data-stu-id="e0231-248">This function gets a pointer to the [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) interface.</span></span>
3.  <span data-ttu-id="e0231-249">Chame o método [**IDirect3DDeviceManager9:: ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) com um ponteiro para o dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="e0231-249">Call the [**IDirect3DDeviceManager9::ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) method with a pointer to the Direct3D device.</span></span>
4.  <span data-ttu-id="e0231-250">Crie um repositório de atributos chamando a função [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) .</span><span class="sxs-lookup"><span data-stu-id="e0231-250">Create an attribute store by calling the [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) function.</span></span>
5.  <span data-ttu-id="e0231-251">Crie o leitor de origem.</span><span class="sxs-lookup"><span data-stu-id="e0231-251">Create the Source Reader.</span></span> <span data-ttu-id="e0231-252">Passe o repositório de atributos no parâmetro *pAttributes* da função de criação.</span><span class="sxs-lookup"><span data-stu-id="e0231-252">Pass the attribute store in the *pAttributes* parameter of the creation function.</span></span>

<span data-ttu-id="e0231-253">Quando você fornece um dispositivo Direct3D, o leitor de origem aloca exemplos de vídeo compatíveis com a API do processador de vídeo DXVA.</span><span class="sxs-lookup"><span data-stu-id="e0231-253">When you provide a Direct3D device, the Source Reader allocates video samples that are compatible with the DXVA video processor API.</span></span> <span data-ttu-id="e0231-254">Você pode usar o processamento de vídeo DXVA para realizar o desentrelaçamento de hardware ou a mixagem de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e0231-254">You can use DXVA video processing to perform hardware deinterlacing or video mixing.</span></span> <span data-ttu-id="e0231-255">Para obter mais informações, consulte [processamento de vídeo de DXVA](dxva-video-processing.md).</span><span class="sxs-lookup"><span data-stu-id="e0231-255">For more information, see [DXVA Video Processing](dxva-video-processing.md).</span></span> <span data-ttu-id="e0231-256">Além disso, se o decodificador der suporte a DXVA 2,0, ele usará o dispositivo Direct3D para executar a decodificação acelerada por hardware.</span><span class="sxs-lookup"><span data-stu-id="e0231-256">Also, if the decoder supports DXVA 2.0, it will use the Direct3D device to perform hardware-accelerated decoding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e0231-257">A partir do Windows 8, o [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) pode ser usado em vez do [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9).</span><span class="sxs-lookup"><span data-stu-id="e0231-257">Beginning in Windows 8, [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) can be used instead of the [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9).</span></span> <span data-ttu-id="e0231-258">Para aplicativos da Windows Store, você deve usar **IMFDXGIDeviceManager**.</span><span class="sxs-lookup"><span data-stu-id="e0231-258">For Windows Store apps, you must use **IMFDXGIDeviceManager**.</span></span> <span data-ttu-id="e0231-259">Para obter mais informações, consulte as [APIs de vídeo do Direct3D 11](direct3d-11-video-apis.md).</span><span class="sxs-lookup"><span data-stu-id="e0231-259">For more info, see the [Direct3D 11 Video APIs](direct3d-11-video-apis.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="e0231-260">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e0231-260">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0231-261">Leitor de origem</span><span class="sxs-lookup"><span data-stu-id="e0231-261">Source Reader</span></span>](source-reader.md)
</dt> </dl>

 

 




