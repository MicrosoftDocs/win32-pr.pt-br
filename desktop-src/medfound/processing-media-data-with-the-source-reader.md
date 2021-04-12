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
# <a name="using-the-source-reader-to-process-media-data"></a>Usando o leitor de origem para processar dados de mídia

Este tópico descreve como usar o [leitor de origem](source-reader.md) para processar dados de mídia.

Para usar o leitor de origem, siga estas etapas básicas:

1.  Crie uma instância do leitor de origem.
2.  Enumere os formatos de saída possíveis.
3.  Defina o formato de saída real para cada fluxo.
4.  Processar dados da origem.

O restante deste tópico descreve detalhadamente essas etapas.

-   [Criando o leitor de origem](#creating-the-source-reader)
-   [Enumerando formatos de saída](#enumerating-output-formats)
-   [Definindo formatos de saída](#setting-output-formats)
-   [Processando dados de mídia](#using-the-source-reader-to-process-media-data)
-   [Drenando o pipeline de dados](#draining-the-data-pipeline)
-   [Obtendo a duração do arquivo](#getting-the-file-duration)
-   [Atingir](#seeking)
-   [Taxa de reprodução](#playback-rate)
-   [Aceleração de hardware](#hardware-acceleration)
-   [Tópicos relacionados](#related-topics)

## <a name="creating-the-source-reader"></a>Criando o leitor de origem

Para criar uma instância do leitor de origem, chame uma das seguintes funções:



| Função                                                                                                                                                                                                                                                        | Descrição                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFCreateSourceReaderFromURL"></span><span id="mfcreatesourcereaderfromurl"></span><span id="MFCREATESOURCEREADERFROMURL"></span>[**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)<br/>                                         | Usa uma URL como entrada. Essa função usa o [resolvedor de origem](source-resolver.md) para criar uma fonte de mídia a partir da URL.<br/>                                                                       |
| <span id="MFCreateSourceReaderFromByteStream"></span><span id="mfcreatesourcereaderfrombytestream"></span><span id="MFCREATESOURCEREADERFROMBYTESTREAM"></span>[**MFCreateSourceReaderFromByteStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)<br/>      | Usa um ponteiro para um fluxo de bytes. Essa função também usa o resolvedor de origem para criar a origem da mídia.<br/>                                                                                        |
| <span id="MFCreateSourceReaderFromMediaSource"></span><span id="mfcreatesourcereaderfrommediasource"></span><span id="MFCREATESOURCEREADERFROMMEDIASOURCE"></span>[**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)<br/> | Usa um ponteiro para uma fonte de mídia que já foi criada. Essa função é útil para fontes de mídia que o resolvedor de origem não pode criar, como dispositivos de captura ou fontes de mídia personalizadas.<br/> |



 

Normalmente, para arquivos de mídia, use [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl). Para dispositivos, como webcams, use [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource). (Para obter mais informações sobre como capturar dispositivos no Microsoft Media Foundation, consulte [captura de áudio/vídeo](audio-video-capture.md).)

Cada uma dessas funções usa um ponteiro [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) opcional, que é usado para definir várias opções no leitor de origem, conforme descrito nos tópicos de referência para essas funções. Para obter o comportamento padrão, defina esse parâmetro como **NULL**. Cada função retorna um ponteiro [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) como um parâmetro de saída. Você deve chamar o **CoInitialize (ex)** e a função [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) antes de chamar qualquer uma dessas funções.

O código a seguir cria o leitor de origem de uma URL.


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



## <a name="enumerating-output-formats"></a>Enumerando formatos de saída

Cada fonte de mídia tem pelo menos um fluxo. Por exemplo, um arquivo de vídeo pode conter um fluxo de vídeo e um fluxo de áudio. O formato de cada fluxo é descrito usando um tipo de mídia, representado pela interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) . Para obter mais informações sobre tipos de mídia, consulte [tipos de mídia](media-types.md). Você deve examinar o tipo de mídia para entender o formato dos dados obtidos do leitor de origem.

Inicialmente, cada fluxo tem um formato padrão, que você pode encontrar chamando o método [**IMFSourceReader:: GetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) :

Para cada fluxo, a origem de mídia oferece uma lista de possíveis tipos de mídia para esse fluxo. O número de tipos depende da origem. Se a origem representar um arquivo de mídia, normalmente haverá apenas um tipo por fluxo. Uma webcam, por outro lado, pode ser capaz de transmitir vídeo em vários formatos diferentes. Nesse caso, o aplicativo pode selecionar qual formato usar na lista de tipos de mídia.

Para obter um dos tipos de mídia para um fluxo, chame o método [**IMFSourceReader:: GetNativeMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype) . Esse método usa dois parâmetros de índice: o índice do fluxo e um índice na lista de tipos de mídia para o fluxo. Para enumerar todos os tipos de um fluxo, aumente o índice da lista enquanto mantém a constante de índice de fluxo. Quando o índice da lista sai dos limites, **GetNativeMediaType** retorna **MF \_ E \_ não \_ mais \_ tipos**.


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



Para enumerar os tipos de mídia para cada fluxo, aumente o índice de fluxo. Quando o índice de fluxo sai dos limites, [**GetNativeMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype) retorna **MF \_ E \_ INVALIDSTREAMNUMBER**.


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



## <a name="setting-output-formats"></a>Definindo formatos de saída

Para alterar o formato de saída, chame o método [**IMFSourceReader:: SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype) . Esse método usa o índice de fluxo e um tipo de mídia:

``` syntax
hr = pReader->SetCurrentMediaType(dwStreamIndex, pMediaType);
```

Para o tipo de mídia, depende se você deseja inserir um decodificador.

-   Para obter dados diretamente da fonte sem decodificá-los, use um dos tipos retornados por [**GetNativeMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype).
-   Para decodificar o fluxo, crie um novo tipo de mídia que descreva o formato descompactado desejado.

No caso do decodificador, crie o tipo de mídia da seguinte maneira:

1.  Chame [**MFCreateMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype) para criar um novo tipo de mídia.
2.  Defina o atributo de [**\_ \_ \_ tipo principal MF MT**](mf-mt-major-type-attribute.md) para especificar áudio ou vídeo.
3.  Defina o atributo de [**\_ \_ subtipo MF MT**](mf-mt-subtype-attribute.md) para especificar o subtipo do formato de decodificação. (Consulte GUIDs de [subtipo de áudio](audio-subtype-guids.md) e [GUIDs de subtipo de vídeo](video-subtype-guids.md).)
4.  Chame [**IMFSourceReader:: SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype).

O leitor de origem carregará automaticamente o decodificador. Para obter os detalhes completos do formato decodificado, chame [**IMFSourceReader:: GetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) após a chamada para [**SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype)

O código a seguir configura o fluxo de vídeo para RGB-32 e o fluxo de áudio para áudio PCM.


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



## <a name="processing-media-data"></a>Processando dados de mídia

Para obter dados de mídia da origem, chame o método [**IMFSourceReader:: ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) , conforme mostrado no código a seguir.


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



O primeiro parâmetro é o índice do fluxo para o qual você deseja obter dados. Você também pode especificar **o \_ leitor de origem MF \_ \_ qualquer \_ fluxo** para obter os próximos dados disponíveis de qualquer fluxo. O segundo parâmetro contém sinalizadores opcionais; consulte [**\_ sinalizador de \_ \_ controle de \_ leitor de origem MF**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_control_flag) para obter uma lista desses. O terceiro parâmetro recebe o índice do fluxo que realmente produz os dados. Você precisará dessas informações se definir o primeiro parâmetro para o **\_ leitor de origem MF \_ \_ qualquer \_ fluxo**. O quarto parâmetro recebe sinalizadores de status, indicando vários eventos que podem ocorrer durante a leitura dos dados, como alterações de formato no fluxo. Para obter uma lista de sinalizadores de status, consulte [**\_ sinalizador do \_ leitor \_ de origem MF**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_flag).

Se a origem da mídia for capaz de produzir dados para o fluxo solicitado, o último parâmetro de [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) receberá um ponteiro para a interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) de um objeto de exemplo de mídia. Use o exemplo de mídia para:

-   Obtenha um ponteiro para os dados de mídia.
-   Obtenha a hora da apresentação e a duração da amostra.
-   Obtenha atributos que descrevem o entrelaçamento, o campo predominância e outros aspectos do exemplo.

O conteúdo dos dados de mídia depende do formato do fluxo. Para um fluxo de vídeo descompactado, cada amostra de mídia contém um único quadro de vídeo. Para um fluxo de áudio descompactado, cada amostra de mídia contém uma sequência de quadros de áudio.

O método [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) pode retornar **S \_ OK** e, ainda assim, não retornar um exemplo de mídia no parâmetro *pSample* . Por exemplo, quando você chega ao final do arquivo, **ReadSample** define o sinalizador **\_ \_ READERF \_ ENDOFSTREAM de origem MF** em *dwFlags* e define *pSample* como **NULL**. Nesse caso, o método **ReadSample** retorna **S \_ OK** porque nenhum erro ocorreu, mesmo que o parâmetro *pSample* esteja definido como **NULL**. Portanto, sempre verifique o valor de *pSample* antes de desreferenciá-lo.

O código a seguir mostra como chamar [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) em um loop e verificar as informações retornadas pelo método, até que o final do arquivo de mídia seja atingido.


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



## <a name="draining-the-data-pipeline"></a>Drenando o pipeline de dados

Durante o processamento de dados, um decodificador ou outra transformação pode armazenar em buffer exemplos de entrada. No diagrama a seguir, o aplicativo chama [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) e recebe um exemplo com um tempo de apresentação igual a *T1*. O decodificador está mantendo amostras para *T2* e *T3*.

![uma ilustração que mostra o armazenamento em buffer em um decodificador.](images/sourcereader02.png)

Na próxima chamada para [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample), o leitor de origem pode fornecer o *T4* ao decodificador e retornar *T2* ao aplicativo.

Se você quiser decodificar todos os exemplos que estão atualmente em buffer no decodificador, sem passar quaisquer novas amostras para o decodificador, defina o sinalizador de **\_ \_ \_ \_ drenagem CONTROLF do leitor de origem MF** no parâmetro *dwControlFlags* de [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample). Continue a fazer isso em um loop até que **ReadSample** retorne um ponteiro de exemplo **nulo** . Dependendo de como o decodificador armazena em buffer exemplos, isso pode acontecer imediatamente ou após várias chamadas para **ReadSample**.

## <a name="getting-the-file-duration"></a>Obtendo a duração do arquivo

Para obter a duração de um arquivo de mídia, chame o método [**IMFSourceReader:: Getpresentationattribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) e solicite o atributo de [**\_ \_ duração de PD de MF**](mf-pd-duration-attribute.md) , conforme mostrado no código a seguir.


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



A função mostrada aqui Obtém a duração em unidades de 100 nanossegundos. Divida por 10 milhões para obter a duração em segundos.

## <a name="seeking"></a>Atingir

Uma fonte de mídia que obtém dados de um arquivo local geralmente pode buscar posições arbitrárias no arquivo. Dispositivos de captura, como webcams, geralmente não podem buscar, porque os dados estão ativos. Uma fonte que transmite dados em uma rede pode ser capaz de buscar, dependendo do protocolo de streaming de rede.

Para descobrir se uma fonte de mídia pode buscar, chame [**IMFSourceReader:: Getpresentationattribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) e solicite o atributo de [ \_ \_ \_ \_ características mediary do leitor de origem MF](mf-source-reader-mediasource-characteristics.md) , conforme mostrado no código a seguir:


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



Essa função obtém um conjunto de sinalizadores de recursos da origem. Esses sinalizadores são definidos na enumeração [**de \_ características do MFMEDIASOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) . Dois sinalizadores estão relacionados à busca:



| Sinalizador                                                                                                                                      | Descrição                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFMEDIASOURCE_CAN_SEEK"></span><span id="mfmediasource_can_seek"></span>**MFMEDIASOURCE \_ pode \_ buscar**<br/>                 | A origem pode buscar.<br/>                                                                                                                                                                            |
| <span id="MFMEDIASOURCE_HAS_SLOW_SEEK"></span><span id="mfmediasource_has_slow_seek"></span>**MFMEDIASOURCE \_ tem \_ uma \_ busca lenta**<br/> | A busca pode levar muito tempo para ser concluída. Por exemplo, a origem pode precisar baixar o arquivo inteiro antes que ele possa ser buscado. (Não há critérios estritos para uma origem retornar esse sinalizador.)<br/> |



 

Os testes de código a seguir para o **MFMEDIASOURCE \_ podem \_ buscar** o sinalizador.


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



Para buscar, chame o método [**IMFSourceReader:: SetCurrentPosition**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentposition) , conforme mostrado no código a seguir.


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



O primeiro parâmetro fornece o formato de hora que você está usando para especificar a posição de busca. Todas as fontes de mídia no Media Foundation são necessárias para dar suporte a unidades de 100 nanossegundos, indicadas pelo valor **GUID \_ NULL**. O segundo parâmetro é um **PROPVARIANT** que contém a posição de busca. Para unidades de tempo de 100 a nanossegundos, o tipo de dados é **LONGLONG**.

Lembre-se de que nem todas as fontes de mídia fornecem busca com precisão de quadro. A precisão da busca depende de vários fatores, como o intervalo de quadros-chave, se o arquivo de mídia contém um índice e se os dados têm uma taxa de bits constante ou variável. Portanto, depois de buscar uma posição em um arquivo, não há nenhuma garantia de que o carimbo de data/hora no próximo exemplo corresponderá exatamente à posição solicitada. Em geral, a posição real não será posterior à posição solicitada, para que você possa descartar amostras até atingir o ponto desejado no fluxo.

## <a name="playback-rate"></a>Taxa de reprodução

Embora você possa definir a taxa de reprodução usando o leitor de origem, normalmente isso não é muito útil, pelos seguintes motivos:

-   O leitor de origem não dá suporte à reprodução inversa, mesmo se a origem da mídia.
-   O aplicativo controla os tempos de apresentação, para que o aplicativo possa implementar uma reprodução rápida ou lenta sem definir a taxa na origem.
-   Algumas fontes de mídia dão suporte ao modo de *finamento* , em que a fonte fornece menos amostras — normalmente apenas os quadros-chave. No entanto, se você quiser descartar quadros não-chave, poderá verificar cada exemplo para o atributo [MFSampleExtension \_ CleanPoint](mfsampleextension-cleanpoint-attribute.md) .

Para definir a taxa de reprodução usando o leitor de origem, chame o método [**IMFSourceReader:: GetServiceForStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getserviceforstream) para obter as interfaces [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) e [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) da origem da mídia.

## <a name="hardware-acceleration"></a>Aceleração de hardware

O leitor de origem é compatível com o Microsoft DirectX Video Acceleration (DXVA) 2,0 para decodificação de vídeo acelerada por hardware. Para usar o DXVA com o leitor de origem, execute as etapas a seguir.

1.  Crie um dispositivo Microsoft Direct3D.
2.  Chame a função [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9) para criar o Gerenciador de dispositivos do Direct3D. Essa função obtém um ponteiro para a interface [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) .
3.  Chame o método [**IDirect3DDeviceManager9:: ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) com um ponteiro para o dispositivo Direct3D.
4.  Crie um repositório de atributos chamando a função [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) .
5.  Crie o leitor de origem. Passe o repositório de atributos no parâmetro *pAttributes* da função de criação.

Quando você fornece um dispositivo Direct3D, o leitor de origem aloca exemplos de vídeo compatíveis com a API do processador de vídeo DXVA. Você pode usar o processamento de vídeo DXVA para realizar o desentrelaçamento de hardware ou a mixagem de vídeo. Para obter mais informações, consulte [processamento de vídeo de DXVA](dxva-video-processing.md). Além disso, se o decodificador der suporte a DXVA 2,0, ele usará o dispositivo Direct3D para executar a decodificação acelerada por hardware.

> [!IMPORTANT]
> A partir do Windows 8, o [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) pode ser usado em vez do [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9). Para aplicativos da Windows Store, você deve usar **IMFDXGIDeviceManager**. Para obter mais informações, consulte as [APIs de vídeo do Direct3D 11](direct3d-11-video-apis.md).

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Leitor de origem](source-reader.md)
</dt> </dl>

 

 




