---
description: A codificação refere-se ao processo de conversão de mídia digital de um formato para outro. Por exemplo, converter áudio MP3 no formato de áudio do Windows Media, conforme definido pela especificação ASF (Advanced Systems Format).
ms.assetid: 4fe202d8-c8f5-4e9a-ad40-1aea8f767362
title: 'Tutorial: 1-transmitir codificação de mídia do Windows'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d670b107f315966a048a2f847183431f9a57bd4
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103663809"
---
# <a name="tutorial-1-pass-windows-media-encoding"></a>Tutorial: 1-transmitir codificação de mídia do Windows

A codificação refere-se ao processo de conversão de mídia digital de um formato para outro. Por exemplo, converter áudio MP3 no formato de áudio do Windows Media, conforme definido pela especificação ASF (Advanced Systems Format).

**Observação**  A especificação de ASF define um tipo de contêiner para o arquivo de saída (. WMA ou. wmv) que pode conter dados de mídia em qualquer formato, compactado ou descompactado. Por exemplo, um contêiner ASF, como um arquivo. WMA, pode conter dados de mídia no formato MP3. O processo de codificação converte o formato real dos dados contidos no arquivo.

Este tutorial demonstra a fonte de entrada codificar conteúdo claro (não protegido por DRM) no conteúdo do Windows Media e gravar os dados em um novo arquivo ASF (. WM \* ) usando componentes ASF da camada de pipeline. Esses componentes serão usados para criar uma topologia de codificação parcial, que será controlada por uma instância da sessão de mídia.

Neste tutorial, você criará um aplicativo de console que usa os nomes de dados de entrada e saída e o modo de codificação como argumentos. O arquivo de entrada pode estar em um formato de mídia compactado ou não compactado. Os modos de codificação válidos são "CBR" (taxa de bits constante) ou "VBR" (taxa de bits variável). O aplicativo cria uma origem de mídia para representar a origem especificada pelo nome de arquivo de entrada e o coletor de arquivos ASF para arquivar o conteúdo codificado do arquivo de origem em um arquivo ASF. Para manter o cenário simples de implementar, o arquivo de saída terá apenas um fluxo de áudio e um fluxo de vídeo. O aplicativo insere o codec Windows Media Audio 9,1 Professional para a conversão de formato de fluxo de áudio e o codec do Windows Media Video 9 para o fluxo de vídeo.

Para a codificação de taxa de bits constante, antes do início da sessão de codificação, o codificador deve saber a taxa de bits de destino que ela deve atingir. Neste tutorial, para o modo "CBR", o aplicativo usa a taxa de bits disponível com o primeiro tipo de mídia de saída que é recuperado do codificador durante a negociação do tipo de mídia como a taxa de bits de destino. Para a codificação de taxa de bits variável, este tutorial demonstra a codificação com a taxa de bits variável, definindo um nível de qualidade. Os fluxos de áudio são codificados no nível de qualidade de 98 e fluxos de vídeo no nível de qualidade de 95.

O procedimento a seguir resume as etapas para codificar o conteúdo do Windows Media em um contêiner ASF usando um modo de codificação de 1 passagem.

1.  Crie uma origem de mídia para o especificado usando o resolvedor de origem.
2.  Enumere os fluxos na origem da mídia.
3.  Crie o coletor de mídia ASF e adicione coletores de fluxo dependendo dos fluxos na origem de mídia que precisam ser codificados.
4.  Configure o coletor de mídia com as propriedades de codificação necessárias.
5.  Crie os codificadores de mídia do Windows para os fluxos no arquivo de saída.
6.  Configure os codificadores com as propriedades definidas no coletor de mídia.
7.  Crie uma topologia de codificação parcial.
8.  Crie uma instância da sessão de mídia e defina a topologia na sessão de mídia.
9.  Inicie a sessão de codificação controlando a sessão de mídia e obtendo todos os eventos relevantes da sessão de mídia.
10. Para a codificação de VBR, obtenha os valores de propriedade de codificação do codificador e defina-os no coletor de mídia.
11. Feche e desligue a sessão de codificação.

Este tutorial contém as seguintes seções:

-   [Pré-requisitos](#prerequisites)
-   [Configurar o projeto](#set-up-the-project)
-   [Criar a origem da mídia](#create-the-media-source)
-   [Criar o coletor de arquivo ASF](#create-the-asf-file-sink)
    -   [Criar o objeto de perfil ASF](#create-the-asf-profile-object)
    -   [Criar um tipo de mídia de áudio compactado](#create-a-compressed-audio-media-type)
    -   [Criar um tipo de mídia de vídeo compactado](#create-a-compressed-video-media-type)
    -   [Criar o objeto ContentInfo do ASF](#create-the-asf-contentinfo-object)
    -   [Criar o coletor de arquivo ASF](#create-the-asf-file-sink)
-   [Criar a topologia de codificação parcial](#build-the-partial-encoding-topology)
    -   [Criar o nó de topologia de origem para a origem de mídia](#create-the-source-topology-node-for-the-media-source)
    -   [Instanciar os codificadores necessários e criar os nós de transformação](#instantiate-the-required-encoders-and-create-the-transform-nodes)
    -   [Criar os nós de topologia de saída para o coletor de arquivos](#create-the-output-topology-nodes-for-the-file-sink)
    -   [Conectar os nós de origem, transformação e coletor](#connect-the-source-transform-and-sink-nodes)
-   [Manipulando a sessão de codificação](#handling-the-encoding-session)
-   [Atualizar propriedades de codificação no coletor de arquivos](#update-encoding-properties-in-the-file-sink)
-   [Implementar principal](#implement-main)
-   [Testar o arquivo de saída](#test-the-output-file)
-   [Códigos de erro comuns e dicas de depuração](#common-error-codes-and-debugging-tips)
-   [Tópicos relacionados](#related-topics)

## <a name="prerequisites"></a>Pré-requisitos

Este tutorial pressupõe o seguinte:

-   Você está familiarizado com a [estrutura do arquivo ASF](asf-file-structure.md), os [componentes ASF da camada de Pipeline](pipeline-layer-asf-components.md) fornecidos pelo Media Foundation para trabalhar com objetos ASF. Esses componentes incluem os seguintes objetos:
    -   [Fontes de mídia](media-sources.md)

        **Observação**  Se você estiver executando transclassificação (convertendo um arquivo de taxa de bits maior em um arquivo de taxa de bits inferior sem alterar os formatos), você usará a [fonte de mídia do ASF](asf-media-source.md).

    -   [Codificadores de mídia do Windows](windows-media-encoders.md)
    -   [Coletores de mídia ASF](asf-media-sinks.md)
    -   [Objeto ASF ContentInfo](asf-contentinfo-object.md)
    -   [Perfil ASF](asf-profile.md)

-   Você está familiarizado com os codificadores de mídia do Windows e os vários tipos de codificação, especialmente a [codificação de taxa de bits constante](constant-bit-rate-encoding.md) e a [codificação de taxa de bits variável baseada em qualidade](quality-based-variable-bit-rate--vbr--encoding.md).
-   Você está familiarizado com as operações de MFT do codificador. Especificamente, a criação de uma instância do codificador e a configuração de tipos de entrada e saída no codificador.
-   Você está familiarizado com objetos de topologia e como criar uma topologia de codificação. Para obter mais informações sobre topologias e nós de topologia, consulte [criando topologias](creating-topologies.md).
-   Você está familiarizado com o modelo de evento da [sessão de mídia](media-session.md)e as operações de controle de fluxo. Para obter informações, consulte [eventos de sessão de mídia](media-session-events.md).

## <a name="set-up-the-project"></a>Configurar o projeto

1.  Inclua os seguintes cabeçalhos no arquivo de origem:

    ```C++
    #include <new>
    #include <mfidl.h>            // Media Foundation interfaces
    #include <mfapi.h>            // Media Foundation platform APIs
    #include <mferror.h>        // Media Foundation error codes
    #include <wmcontainer.h>    // ASF-specific components
    #include <wmcodecdsp.h>        // Windows Media DSP interfaces
    #include <Dmo.h>            // DMO objects
    #include <uuids.h>            // Definition for FORMAT_VideoInfo
    #include <propvarutil.h>
    
    ```

    

2.  Link para os seguintes arquivos de biblioteca:

    ```C++
    // The required link libraries 
    #pragma comment(lib, "mfplat")
    #pragma comment(lib, "mf")
    #pragma comment(lib, "mfuuid")
    #pragma comment(lib, "msdmo")
    #pragma comment(lib, "strmiids")
    #pragma comment(lib, "propsys")
    
    ```

    

3.  Declare a função [SafeRelease](saferelease.md) .

    ```C++
    template <class T> void SafeRelease(T **ppT)
    {
        if (*ppT)
        {
            (*ppT)->Release();
            *ppT = NULL;
        }
    }
    ```

    

4.  Declare a enumeração do modo de codificação \_ para definir os tipos de codificação CBR e VBR.

    ```C++
    // Encoding mode
    typedef enum ENCODING_MODE {
      NONE  = 0x00000000,
      CBR   = 0x00000001,
      VBR   = 0x00000002,
    } ;
    
    ```

    

5.  Defina uma constante para a janela de buffer para um fluxo de vídeo.

    ```C++
    // Video buffer window
    const INT32 VIDEO_WINDOW_MSEC = 3000;
    
    ```

    

## <a name="create-the-media-source"></a>Criar a origem da mídia

Crie uma origem de mídia para a fonte de entrada. O Media Foundation fornece fontes de mídia internas para vários formatos de mídia: MP3, MP4/3GP, AVI/WAVE. Para obter informações sobre os formatos com suporte pelo Media Foundation, consulte [formatos de mídia com suporte no Media Foundation](supported-media-formats-in-media-foundation.md).

Para criar a origem de mídia, use o [resolvedor de origem](source-resolver.md). Esse objeto analisa a URL que foi especificada para o arquivo de origem e cria a origem de mídia apropriada.

Faça as seguintes chamadas:

-   [**MFCreateSourceResolver**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesourceresolver)
-   [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl)

    Para obter mais informações sobre essas chamadas, consulte [usando o resolvedor de origem](using-the-source-resolver.md).

    Se o arquivo de entrada estiver no formato ASF e você quiser convertê-lo em um arquivo de taxa de bits diferente sem alterar os formatos, o resolvedor de origem criará uma instância da [fonte de mídia ASF](asf-media-source.md).

O exemplo de código a seguir mostra uma função createmedianame que cria uma origem de mídia para o arquivo especificado.


```C++
//  Create a media source from a URL.
HRESULT CreateMediaSource(PCWSTR sURL, IMFMediaSource **ppSource)
{
    MF_OBJECT_TYPE ObjectType = MF_OBJECT_INVALID;

    IMFSourceResolver* pSourceResolver = NULL;
    IUnknown* pSource = NULL;

    // Create the source resolver.
    HRESULT hr = MFCreateSourceResolver(&pSourceResolver);
    if (FAILED(hr))
    {
        goto done;
    }

    // Use the source resolver to create the media source.

    // Note: For simplicity this sample uses the synchronous method to create 
    // the media source. However, creating a media source can take a noticeable
    // amount of time, especially for a network source. For a more responsive 
    // UI, use the asynchronous BeginCreateObjectFromURL method.

    hr = pSourceResolver->CreateObjectFromURL(
        sURL,                       // URL of the source.
        MF_RESOLUTION_MEDIASOURCE,  // Create a source object.
        NULL,                       // Optional property store.
        &ObjectType,        // Receives the created object type. 
        &pSource            // Receives a pointer to the media source.
        );
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the IMFMediaSource interface from the media source.
    hr = pSource->QueryInterface(IID_PPV_ARGS(ppSource));

done:
    SafeRelease(&pSourceResolver);
    SafeRelease(&pSource);
    return hr;
}
```



## <a name="create-the-asf-file-sink"></a>Criar o coletor de arquivo ASF

Crie uma instância do coletor de arquivo ASF que arquivará dados de mídia codificados em um arquivo ASF no final da sessão de codificação.

Neste tutorial, você criará um objeto de ativação para o coletor de arquivos ASF. O coletor de arquivos precisa das seguintes informações para criar os coletores de fluxo necessários.

-   Os fluxos a serem codificados e gravados no arquivo final.
-   As propriedades de codificação que são usadas para codificar o conteúdo de mídia, como, tipo de codificação, número de passagens de codificação e as propriedades relacionadas.
-   As propriedades de arquivo global que indicam ao coletor de mídia se ele deve ajustar os parâmetros de Bucket de vazamento (taxa de bits e tamanho do buffer) automaticamente.

As informações de fluxo são configuradas no objeto de perfil ASF e a codificação e as propriedades globais são definidas em um repositório de propriedades gerenciado pelo objeto ASF ContentInfo.

Para obter uma visão geral do coletor de arquivos ASF, consulte [coletores de mídia ASF](asf-media-sinks.md).

### <a name="create-the-asf-profile-object"></a>Criar o objeto de perfil ASF

Para que o coletor de arquivos ASF grave dados de mídia codificados em um arquivo ASF, o coletor precisa saber o número de fluxos e o tipo de fluxos para os quais criar coletores de fluxo. Neste tutorial, você extrairá essas informações da origem de mídia e criará os fluxos de saída correspondentes. Restrinja os fluxos de saída para um fluxo de áudio e um fluxo de vídeo. Para cada fluxo selecionado na origem, crie um fluxo de destino e adicione-o ao perfil.

Para implementar essa etapa, você precisa dos seguintes objetos.

-   [Perfil ASF](asf-profile.md)
-   Descritor de apresentação para a origem de mídia
-   Os descritores de fluxo para os fluxos selecionados na origem da mídia.
-   Tipos de mídia para os fluxos selecionados.

As etapas a seguir descrevem o processo de criação do perfil ASF e dos fluxos de destino.

**Para criar o perfil ASF**

1.  Chame [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) para criar um objeto de perfil vazio.
2.  Chame [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) para criar o descritor de apresentação para a origem de mídia criada na etapa descrita na seção "criar fonte de mídia" deste tutorial.
3.  Chame [**IMFPresentationDescriptor:: GetStreamDescriptorCount**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount) para obter o número de fluxos na origem da mídia.
4.  Chame [**IMFPresentationDescriptor:: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) para cada fluxo na origem da mídia, obtenha o descritor de fluxo do fluxo.
5.  Chame [**IMFStreamDescriptor:: GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) seguido por [**IMFMediaTypeHandler:: GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) e obtenha o primeiro tipo de mídia para o fluxo.

    **Observação**   Para evitar chamadas complexas, suponha que apenas um tipo de mídia exista por fluxo e selecione o primeiro tipo de mídia do fluxo. Para fluxos complexos, você precisa enumerar cada tipo de mídia do manipulador de tipo de mídia e escolher o tipo de mídia que deseja codificar.

6.  Chame I [**IMFMediaType:: Getmajortype**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype) para obter o tipo principal do fluxo para determinar se o fluxo contém áudio ou vídeo.
7.  Dependendo do tipo principal do fluxo, crie tipos de mídia de destino. Esses tipos de mídia irão conter informações de formato que o codificador usará durante a sessão de codificação. As seções a seguir deste tutorial descrevem o processo de criação dos tipos de mídia de destino.
    -   Criar um tipo de mídia de áudio compactado
    -   Criar um tipo de mídia de vídeo compactado
8.  Crie um fluxo com base no tipo de mídia de destino, configure o fluxo de acordo com os requisitos do aplicativo e adicione o fluxo ao perfil. Para obter mais informações, consulte [adicionando informações de fluxo ao coletor de arquivo ASF](adding-stream-information-to-the-asf-file-sink.md).

    1.  Chame [**IMFASFProfile:: CreateStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream) e passe o tipo de mídia de destino para criar o fluxo de saída. O método recupera a interface IMFASFStreamConfig do objeto Stream.
    2.  Configure o fluxo.
        -   Chame [**IMFASFStreamConfig:: SetStreamNumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setstreamnumber) para atribuir um número ao fluxo. Essa configuração é obrigatória.
        -   Opcionalmente, configure os parâmetros de Bucket vazado, a extensão de carga, a exclusão mútua em cada fluxo chamando métodos [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) e atributos de configuração de fluxo relevantes.
    3.  Adicione as propriedades de codificação de nível de fluxo usando o objeto ContentInfo do ASF. Para obter mais informações sobre esta etapa, consulte a seção "criar o objeto ASF ContentInfo" neste tutorial.
    4.  Chame [**IMFASFProfile:: SetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream) para adicionar o fluxo ao perfil.

    O exemplo de código a seguir cria um fluxo de áudio de saída.

    ```C++
    //-------------------------------------------------------------------
    //  CreateAudioStream
    //  Create an audio stream and add it to the profile.
    //
    //  pProfile: A pointer to the ASF profile.
    //  wStreamNumber: Stream number to assign for the new stream.
    //-------------------------------------------------------------------

    HRESULT CreateAudioStream(IMFASFProfile* pProfile, WORD wStreamNumber)
    {
        if (!pProfile)
        {
            return E_INVALIDARG;
        }
        if (wStreamNumber < 1 || wStreamNumber > 127 )
        {
            return MF_E_INVALIDSTREAMNUMBER;
        }

        IMFMediaType* pAudioType = NULL;
        IMFASFStreamConfig* pAudioStream = NULL;
        
        //Create an output type from the encoder
        HRESULT hr = GetOutputTypeFromWMAEncoder(&pAudioType);
        if (FAILED(hr))
        {
            goto done;
        }
        
        //Create a new stream with the audio type
        hr = pProfile->CreateStream(pAudioType, &pAudioStream);
        if (FAILED(hr))
        {
            goto done;
        }

        //Set stream number
        hr = pAudioStream->SetStreamNumber(wStreamNumber);
        if (FAILED(hr))
        {
            goto done;
        }
        
        //Add the stream to the profile
        hr = pProfile->SetStream(pAudioStream);
        if (FAILED(hr))
        {
            goto done;
        }

        wprintf_s(L"Audio Stream created. Stream Number: %d.\n", wStreamNumber);

    done:
        SafeRelease(&pAudioStream);
        SafeRelease(&pAudioType);
        return hr;
    }
    ```

    

    O exemplo de código a seguir cria um fluxo de vídeo de saída.

    ```C++
    //-------------------------------------------------------------------
    //  CreateVideoStream
    //  Create an video stream and add it to the profile.
    //
    //  pProfile: A pointer to the ASF profile.
    //  wStreamNumber: Stream number to assign for the new stream.
    //    pType: A pointer to the source's video media type.
    //-------------------------------------------------------------------

    HRESULT CreateVideoStream(IMFASFProfile* pProfile, WORD wStreamNumber, IMFMediaType* pType)
    {
        if (!pProfile)
        {
            return E_INVALIDARG;
        }
        if (wStreamNumber < 1 || wStreamNumber > 127 )
        {
            return MF_E_INVALIDSTREAMNUMBER;
        }

        HRESULT hr = S_OK;

        
        IMFMediaType* pVideoType = NULL;
        IMFASFStreamConfig* pVideoStream = NULL;

        UINT32 dwBitRate = 0;
            
        //Create a new video type from the source type
        hr = CreateCompressedVideoType(pType, &pVideoType);
        if (FAILED(hr))
        {
            goto done;
        }

        //Create a new stream with the video type
        hr = pProfile->CreateStream(pVideoType, &pVideoStream);
        if (FAILED(hr))
        {
            goto done;
        }
        

        //Set a valid stream number
        hr = pVideoStream->SetStreamNumber(wStreamNumber);
        if (FAILED(hr))
        {
            goto done;
        }

        //Add the stream to the profile
        hr = pProfile->SetStream(pVideoStream);
        if (FAILED(hr))
        {
            goto done;
        }

        wprintf_s(L"Video Stream created. Stream Number: %d .\n", wStreamNumber);

    done:

        SafeRelease(&pVideoStream);
        SafeRelease(&pVideoType);

        return hr;
    }
    ```

    

O exemplo de código a seguir cria fluxos de saída dependendo dos fluxos na origem.


```C++
    //For each stream in the source, add target stream information in the profile
    for (DWORD iStream = 0; iStream < dwSrcStream; iStream++)
    {
        hr = pPD->GetStreamDescriptorByIndex(
            iStream, &fSelected, &pStreamDesc);
        if (FAILED(hr))
        {
            goto done;
        }

        if (!fSelected)
        {
            continue;
        }

        //Get the media type handler
        hr = pStreamDesc->GetMediaTypeHandler(&pHandler);
        if (FAILED(hr))
        {
            goto done;
        }

        //Get the first media type 
        hr = pHandler->GetMediaTypeByIndex(0, &pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }

        //Get the major type
        hr = pMediaType->GetMajorType(&guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }

        // If this is a video stream, create the target video stream
        if (guidMajor == MFMediaType_Video)
        {
            //The stream level encoding properties will be set in this call
            hr = CreateVideoStream(pProfile, wStreamID, pMediaType);

            if (FAILED(hr))
            {
                goto done;
            }
        }
        
        // If this is an audio stream, create the target audio stream
        if (guidMajor == MFMediaType_Audio)
        {
            //The stream level encoding properties will be set in this call
            hr = CreateAudioStream(pProfile, wStreamID);

            if (FAILED(hr))
            {
                goto done;
            }
        }

        //Get stream's encoding property
        hr = pContentInfo->GetEncodingConfigurationPropertyStore(wStreamID, &pContentInfoProps);
        if (FAILED(hr))
        {
            goto done;
        }

        //Set the stream-level encoding properties
        hr = SetEncodingProperties(guidMajor, pContentInfoProps);       
        if (FAILED(hr))
        {
            goto done;
        }


        SafeRelease(&pMediaType);
        SafeRelease(&pStreamDesc);
        SafeRelease(&pContentInfoProps);
        wStreamID++;
    }
```



### <a name="create-a-compressed-audio-media-type"></a>Criar um tipo de mídia de áudio compactado

Se você quiser incluir um fluxo de áudio no arquivo de saída, crie um tipo de áudio especificando as características do tipo codificado definindo os atributos necessários. Para garantir que o tipo de áudio seja compatível com o codificador de áudio do Windows Media, crie uma instância do MFT do codificador, defina as propriedades de codificação e obtenha um tipo de mídia chamando [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype). Obtenha o tipo de saída necessário fazendo um loop por todos os tipos disponíveis, obtendo os atributos de cada tipo de mídia e selecionando o tipo mais próximo de seus requisitos. Neste tutorial, obtenha o primeiro tipo disponível da lista de tipos de mídia de saída com suporte pelo codificador.

**Observação**  Para o Windows 7, Media Foundation fornece uma nova função, [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) que recupera uma lista dos tipos de áudio compatíveis. Essa função só obtém tipos de mídia para codificação de CBR.

Um tipo de áudio completo deve ter os seguintes atributos definidos:

-   [**\_ \_ tipo principal MF \_ MT**](mf-mt-major-type-attribute.md)
-   [**subtipo MF \_ MT \_**](mf-mt-subtype-attribute.md)
-   [**\_canais de \_ número de áudio MF MT \_ \_**](mf-mt-audio-num-channels-attribute.md)
-   [**\_amostras de áudio MF MT \_ \_ \_ por \_ segundo**](mf-mt-audio-samples-per-second-attribute.md)
-   [**\_alinhamento de \_ bloco de áudio MF MT \_ \_**](mf-mt-audio-block-alignment-attribute.md)
-   [**áudio do MF \_ MT \_ média de \_ \_ bytes \_ por \_ segundo**](mf-mt-audio-avg-bytes-per-second-attribute.md)
-   [**\_bits de áudio MF MT \_ \_ \_ por \_ amostra**](mf-mt-audio-bits-per-sample-attribute.md)

O exemplo de código a seguir cria um tipo de áudio compactado obtendo um tipo compatível do codificador de áudio do Windows Media. A implementação de setencodingproperties é mostrada na seção "criar o objeto ASF ContentInfo" deste tutorial.


```C++
//-------------------------------------------------------------------
//  GetOutputTypeFromWMAEncoder
//  Gets a compatible output type from the Windows Media audio encoder.
//
//  ppAudioType: Receives a pointer to the media type.
//-------------------------------------------------------------------

HRESULT GetOutputTypeFromWMAEncoder(IMFMediaType** ppAudioType)
{
    if (!ppAudioType)
    {
        return E_POINTER;
    }

    IMFTransform* pMFT = NULL;
    IMFMediaType* pType = NULL;
    IPropertyStore* pProps = NULL;

    //We need to find a suitable output media type
    //We need to create the encoder to get the available output types
    //and discard the instance.

    CLSID *pMFTCLSIDs = NULL;   // Pointer to an array of CLISDs. 
    UINT32 cCLSID = 0;            // Size of the array.

    MFT_REGISTER_TYPE_INFO tinfo;
    
    tinfo.guidMajorType = MFMediaType_Audio;
    tinfo.guidSubtype = MFAudioFormat_WMAudioV9;

    // Look for an encoder.
    HRESULT hr = MFTEnum(
        MFT_CATEGORY_AUDIO_ENCODER,
        0,                  // Reserved
        NULL,                // Input type to match. None.
        &tinfo,             // WMV encoded type.
        NULL,               // Attributes to match. (None.)
        &pMFTCLSIDs,        // Receives a pointer to an array of CLSIDs.
        &cCLSID             // Receives the size of the array.
        );
    if (FAILED(hr))
    {
        goto done;
    }

    // MFTEnum can return zero matches.
    if (cCLSID == 0)
    {
        hr = MF_E_TOPO_CODEC_NOT_FOUND;
        goto done;
    }
    else
    {
        // Create the MFT decoder
        hr = CoCreateInstance(pMFTCLSIDs[0], NULL,
            CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pMFT));

        if (FAILED(hr))
        {
            goto done;
        }

    }

    // Get the encoder's property store

    hr = pMFT->QueryInterface(IID_PPV_ARGS(&pProps));
    if (FAILED(hr))
    {
        goto done;
    }
    
    //Set encoding properties
    hr = SetEncodingProperties(MFMediaType_Audio, pProps);
    if (FAILED(hr))
    {
        goto done;
    }

    //Get the first output type
    //You can loop through the available output types to choose 
    //the one that meets your target requirements
    hr = pMFT->GetOutputAvailableType(0, 0, &pType);
    if (FAILED(hr))
    {
        goto done;
    }

    //Return to the caller
    *ppAudioType = pType;
    (*ppAudioType)->AddRef();
    
done:
    SafeRelease(&pProps);
    SafeRelease(&pType);
    SafeRelease(&pMFT);
    CoTaskMemFree(pMFTCLSIDs);
    return hr;
}
```



### <a name="create-a-compressed-video-media-type"></a>Criar um tipo de mídia de vídeo compactado

Se você quiser incluir um fluxo de vídeo no arquivo de saída, crie um tipo de vídeo codificado completo. O tipo de mídia completo deve incluir a taxa de bits e os dados privados do codec desejados.

Há duas maneiras de criar um tipo de mídia de vídeo completo.

-   Crie um tipo de mídia vazio e copie os atributos do tipo de mídia do tipo de vídeo de origem e substitua o atributo de [**\_ \_ subtipo MF MT**](mf-mt-subtype-attribute.md) pela constante de GUID MFVideoFormat \_ WMV3.

    Um tipo de vídeo completo deve ter os seguintes atributos definidos:

    -   \_ \_ tipo principal MF \_ MT
    -   subtipo MF \_ MT \_
    -   \_taxa de \_ quadros MF MT \_
    -   \_tamanho do \_ quadro MF MT \_
    -   \_modo de \_ entrelaçamento do MF MT \_
    -   taxa de proporção de pixel do MF \_ MT \_ \_ \_
    -   \_taxa de \_ \_ bits média de MF MT
    -   dados de usuário do MF \_ MT \_ \_

    O exemplo de código a seguir cria um tipo de vídeo compactado do tipo de vídeo da origem.

    ```C++
    //-------------------------------------------------------------------
    //  CreateCompressedVideoType
    //  Creates an output type from source's video media type.
    //
    //    pType: A pointer to the source's video media type.
    //  ppVideoType: Receives a pointer to the media type.
    //-------------------------------------------------------------------

    HRESULT CreateCompressedVideoType(
            IMFMediaType* pType, 
            IMFMediaType** ppVideoType)
    {
        if (!pType)
        {
            return E_INVALIDARG;
        }
        if (!ppVideoType)
        {
            return E_POINTER;
        }
        
        HRESULT hr = S_OK;
        MFRatio fps = { 0 };
        MFRatio par = { 0 };
        UINT32 width = 0, height = 0;
        UINT32 interlace = MFVideoInterlace_Unknown;
        UINT32 fSamplesIndependent = 0;
        UINT32 cBitrate = 0;

        IMFMediaType* pMediaType = NULL;

        GUID guidMajor = GUID_NULL;

        hr = pType->GetMajorType(&guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }

        if (guidMajor != MFMediaType_Video )
        {
            hr = MF_E_INVALID_FORMAT;
            goto done;
        }

        hr = MFCreateMediaType(&pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pType->CopyAllItems(pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }

        //Fill the missing attributes
        //1. Frame rate
        hr = MFGetAttributeRatio(pMediaType, MF_MT_FRAME_RATE, (UINT32*)&fps.Numerator, (UINT32*)&fps.Denominator);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            fps.Numerator = 30000;
            fps.Denominator = 1001;

            hr = MFSetAttributeRatio(pMediaType, MF_MT_FRAME_RATE, fps.Numerator, fps.Denominator);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        ////2. Frame size
        hr = MFGetAttributeSize(pMediaType, MF_MT_FRAME_SIZE, &width, &height);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            width = 1280;
            height = 720;
                
            hr = MFSetAttributeSize(pMediaType, MF_MT_FRAME_SIZE, width, height);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        ////3. Interlace mode
        
        if (FAILED(pMediaType->GetUINT32(MF_MT_INTERLACE_MODE, &interlace)))
        {
            hr = pMediaType->SetUINT32(MF_MT_INTERLACE_MODE, MFVideoInterlace_Progressive);
            if (FAILED(hr))
            {
                goto done;
            }

        }

        ////4. Pixel aspect Ratio
        hr = MFGetAttributeRatio(pMediaType, MF_MT_PIXEL_ASPECT_RATIO, (UINT32*)&par.Numerator, (UINT32*)&par.Denominator);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            par.Numerator = par.Denominator = 1;
            hr = MFSetAttributeRatio(pMediaType, MF_MT_PIXEL_ASPECT_RATIO, (UINT32)par.Numerator, (UINT32)par.Denominator);
            if (FAILED(hr))
            {
                goto done;
            }

        }

        //6. bit rate
        if (FAILED(pMediaType->GetUINT32(MF_MT_AVG_BITRATE, &cBitrate)))
        {
            hr = pMediaType->SetUINT32(MF_MT_AVG_BITRATE, 1000000);
            if (FAILED(hr))
            {
                goto done;
            }

        }

        hr = pMediaType->SetGUID(MF_MT_SUBTYPE, MFVideoFormat_WMV3);
        if (FAILED(hr))
        {
            goto done;
        }

        // Return the pointer to the caller.
        *ppVideoType = pMediaType;
        (*ppVideoType)->AddRef();


    done:
        SafeRelease(&pMediaType);
        return hr;
    }
    
    ```

    

-   Obtenha um tipo de mídia compatível do codificador de vídeo do Windows Media definindo as propriedades de codificação e, em seguida, chamando [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype). Esse método retorna o tipo parcial. Certifique-se de converter o tipo parcial para um tipo completo adicionando as seguintes informações:

    -   Defina a taxa de bits do vídeo no atributo de taxa de bits [**\_ \_ média \_ MF MT**](mf-mt-avg-bitrate-attribute.md) .
    -   Adicione dados privados de codec definindo o atributo de [**\_ dados de \_ usuário \_ MF MT**](mf-mt-user-data-attribute.md) . Para obter instruções detalhadas, consulte "dados de codec privado" em [Configurando um codificador WMV](configuring-a-wmv-encoder.md).

    Como [**IWMCodecPrivateData:: GetPrivateData**](../wmformat/iwmcodecprivatedata-getprivatedata.md) verifica a taxa de bits antes de retornar os dados privados do codec, certifique-se de definir a taxa de bits antes de obter os dados privados do codec.

    O exemplo de código a seguir cria um tipo de vídeo compactado obtendo um tipo compatível do codificador de vídeo do Windows Media. Ele também cria um tipo de vídeo descompactado e o define como a entrada do codificador. Isso é implementado na função auxiliar CreateUncompressedVideoType. GetOutputTypeFromWMVEncoder converte o tipo parcial retornado em um tipo completo adicionando dados privados do codec. A implementação de setencodingproperties é mostrada na seção "criar o objeto ASF ContentInfo" deste tutorial.

    ```C++
    //-------------------------------------------------------------------
    //  GetOutputTypeFromWMVEncoder
    //  Gets a compatible output type from the Windows Media video encoder.
    //
    //  pType: A pointer to the source video stream's media type.
    //  ppVideoType: Receives a pointer to the media type.
    //-------------------------------------------------------------------

    HRESULT GetOutputTypeFromWMVEncoder(IMFMediaType* pType, IMFMediaType** ppVideoType)
    {
        if (!ppVideoType)
        {
            return E_POINTER;
        }

        IMFTransform* pMFT = NULL;
        IPropertyStore* pProps = NULL;
        IMFMediaType* pInputType = NULL;
        IMFMediaType* pOutputType = NULL;
        
        UINT32 cBitrate = 0;

        //We need to find a suitable output media type
        //We need to create the encoder to get the available output types
        //and discard the instance.

        CLSID *pMFTCLSIDs = NULL;   // Pointer to an array of CLISDs. 
        UINT32 cCLSID = 0;          // Size of the array.

        MFT_REGISTER_TYPE_INFO tinfo;
        
        tinfo.guidMajorType = MFMediaType_Video;
        tinfo.guidSubtype = MFVideoFormat_WMV3;

        // Look for an encoder.
        HRESULT hr = MFTEnum(
            MFT_CATEGORY_VIDEO_ENCODER,
            0,                  // Reserved
            NULL,               // Input type to match. None.
            &tinfo,             // WMV encoded type.
            NULL,               // Attributes to match. (None.)
            &pMFTCLSIDs,        // Receives a pointer to an array of CLSIDs.
            &cCLSID             // Receives the size of the array.
            );
        if (FAILED(hr))
        {
            goto done;
        }

        // MFTEnum can return zero matches.
        if (cCLSID == 0)
        {
            hr = MF_E_TOPO_CODEC_NOT_FOUND;
            goto done;
        }
        else
        {
            //Create the MFT decoder
            hr = CoCreateInstance(pMFTCLSIDs[0], NULL,
                CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pMFT));
            if (FAILED(hr))
            {
                goto done;
            }

        }
        
        //Get the video encoder property store
        hr = pMFT->QueryInterface(IID_PPV_ARGS(&pProps));
        if (FAILED(hr))
        {
            goto done;
        }

        //Set encoding properties
        hr = SetEncodingProperties(MFMediaType_Video, pProps);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = CreateUncompressedVideoType(pType, &pInputType);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pMFT->SetInputType(0, pInputType, 0);

        //Get the first output type
        //You can loop through the available output types to choose 
        //the one that meets your target requirements
        hr =  pMFT->GetOutputAvailableType(0, 0, &pOutputType);
        if (FAILED(hr))
        {
            goto done;
        }
        
        hr = pType->GetUINT32(MF_MT_AVG_BITRATE, &cBitrate);
        if (FAILED(hr))
        {
            goto done;
        }

        //Now set the bit rate
        hr = pOutputType->SetUINT32(MF_MT_AVG_BITRATE, cBitrate);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = AddPrivateData(pMFT, pOutputType);
        if (FAILED(hr))
        {
            goto done;
        }

        //Return to the caller
        *ppVideoType = pOutputType;
        (*ppVideoType)->AddRef();
        
    done:
        SafeRelease(&pProps);
        SafeRelease(&pOutputType);
        SafeRelease(&pInputType);
        SafeRelease(&pMFT);
        CoTaskMemFree(pMFTCLSIDs);
        return hr;
    }
    ```

    

    O exemplo de código a seguir cria um tipo de vídeo descompactado.

    ```C++
    //-------------------------------------------------------------------
    //  CreateUncompressedVideoType
    //  Creates an uncompressed video type.
    //
    //    pType: A pointer to the source's video media type.
    //  ppVideoType: Receives a pointer to the media type.
    //-------------------------------------------------------------------

    HRESULT CreateUncompressedVideoType(IMFMediaType* pType, IMFMediaType** ppMediaType)
    {
        if (!pType)
        {
            return E_INVALIDARG;
        }
        if (!ppMediaType)
        {
            return E_POINTER;
        }
        
        MFRatio fps = { 0 };
        MFRatio par = { 0 };
        UINT32 width = 0, height = 0;
        UINT32 interlace = MFVideoInterlace_Unknown;
        UINT32 cBitrate = 0;

        IMFMediaType* pMediaType = NULL;

        GUID guidMajor = GUID_NULL;

        HRESULT hr = pType->GetMajorType(&guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }

        if (guidMajor != MFMediaType_Video )
        {
            hr = MF_E_INVALID_FORMAT;
            goto done;
        }

        hr = MFGetAttributeRatio(pType, MF_MT_FRAME_RATE, (UINT32*)&fps.Numerator, (UINT32*)&fps.Denominator);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            fps.Numerator = 30000;
            fps.Denominator = 1001;

        }
        hr = MFGetAttributeSize(pType, MF_MT_FRAME_SIZE, &width, &height);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            width = 1280;
            height = 720;

        }

        interlace = MFGetAttributeUINT32(pType, MF_MT_INTERLACE_MODE, MFVideoInterlace_Progressive);

        hr = MFGetAttributeRatio(pType, MF_MT_PIXEL_ASPECT_RATIO, (UINT32*)&par.Numerator, (UINT32*)&par.Denominator);
        if (FAILED(hr))
        {
            par.Numerator = par.Denominator = 1;
        }

        cBitrate = MFGetAttributeUINT32(pType, MF_MT_AVG_BITRATE, 1000000);

        hr = MFCreateMediaType(&pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pMediaType->SetGUID(MF_MT_MAJOR_TYPE, guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pMediaType->SetGUID(MF_MT_SUBTYPE, MFVideoFormat_RGB32);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = MFSetAttributeRatio(pMediaType, MF_MT_FRAME_RATE, fps.Numerator, fps.Denominator);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = MFSetAttributeSize(pMediaType, MF_MT_FRAME_SIZE, width, height);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pMediaType->SetUINT32(MF_MT_INTERLACE_MODE, 2);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pMediaType->SetUINT32(MF_MT_ALL_SAMPLES_INDEPENDENT, TRUE);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pMediaType->SetUINT32(MF_MT_AVG_BITRATE, cBitrate);
        if (FAILED(hr))
        {
            goto done;
        }

        // Return the pointer to the caller.
        *ppMediaType = pMediaType;
        (*ppMediaType)->AddRef();


    done:
        SafeRelease(&pMediaType);
        return hr;
    }
    ```

    

    O exemplo de código a seguir adiciona dados privados de codec ao tipo de mídia de vídeo especificado.

    ```C++
    //
    // AddPrivateData
    // Appends the private codec data to a media type.
    //
    // pMFT: The video encoder
    // pTypeOut: A video type from the encoder's type list.
    //
    // The function modifies pTypeOut by adding the codec data.
    //

    HRESULT AddPrivateData(IMFTransform *pMFT, IMFMediaType *pTypeOut)
    {
        HRESULT hr = S_OK;
        ULONG cbData = 0;
        BYTE *pData = NULL;

        IWMCodecPrivateData *pPrivData = NULL;

        DMO_MEDIA_TYPE mtOut = { 0 };

        // Convert the type to a DMO type.
        hr = MFInitAMMediaTypeFromMFMediaType(
            pTypeOut, 
            FORMAT_VideoInfo, 
            (AM_MEDIA_TYPE*)&mtOut
            );
        
        if (SUCCEEDED(hr))
        {
            hr = pMFT->QueryInterface(IID_PPV_ARGS(&pPrivData));
        }

        if (SUCCEEDED(hr))
        {
            hr = pPrivData->SetPartialOutputType(&mtOut);
        }

        //
        // Get the private codec data
        //

        // First get the buffer size.
        if (SUCCEEDED(hr))
        {
            hr = pPrivData->GetPrivateData(NULL, &cbData);
        }

        if (SUCCEEDED(hr))
        {
            pData = new BYTE[cbData];

            if (pData == NULL)
            {
                hr = E_OUTOFMEMORY;
            }
        }

        // Now get the data.
        if (SUCCEEDED(hr))
        {
            hr = pPrivData->GetPrivateData(pData, &cbData);
        }

        // Add the data to the media type.
        if (SUCCEEDED(hr))
        {
            hr = pTypeOut->SetBlob(MF_MT_USER_DATA, pData, cbData);
        }

        delete [] pData;
        MoFreeMediaType(&mtOut);
        SafeRelease(&pPrivData);
        return hr;
    }
    ```

    

### <a name="create-the-asf-contentinfo-object"></a>Criar o objeto ContentInfo do ASF

O objeto ASF ContentInfo é um componente de nível WMContainer que é projetado principalmente para armazenar informações de objeto de cabeçalho ASF. O coletor de arquivo ASF implementa o objeto ContentInfo para armazenar informações (em um repositório de propriedades) que serão usadas para gravar o objeto de cabeçalho ASF do arquivo codificado. Para fazer isso, você deve criar e configurar o seguinte conjunto de informações no objeto ContentInfo antes de iniciar a sessão de codificação.

1.  Chame [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) para criar um objeto ContentInfo vazio.

    O exemplo de código a seguir cria um objeto ContentInfo vazio.

    ```C++
        // Create an empty ContentInfo object
        hr = MFCreateASFContentInfo(&pContentInfo);
        if (FAILED(hr))
        {
            goto done;
        }
    
    ```

    

2.  Chame [**IMFASFContentInfo:: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) para obter o armazenamento de propriedades no nível de fluxo do coletor de arquivo. Nesta chamada, você precisa passar o número de fluxo que você atribuiu para o fluxo ao criar o perfil ASF.
3.  Defina as [Propriedades de codificação](configuring-the-encoder.md) no nível de fluxo no repositório de propriedades de fluxo do coletor de arquivos. Para obter mais informações, consulte "Propriedades de codificação de fluxo" em [Propriedades de configuração no coletor de arquivos](setting-properties-in-the-file-sink.md).

    O exemplo de código a seguir define as propriedades de nível de fluxo no repositório de propriedades do coletor de arquivos.

    ```C++
            //Get stream's encoding property
            hr = pContentInfo->GetEncodingConfigurationPropertyStore(wStreamID, &pContentInfoProps);
            if (FAILED(hr))
            {
                goto done;
            }

            //Set the stream-level encoding properties
            hr = SetEncodingProperties(guidMajor, pContentInfoProps);       
            if (FAILED(hr))
            {
                goto done;
            }

    
    ```

    

    O exemplo de código a seguir mostra a implementação de setencodingproperties. Essa função define as propriedades de codificação de nível de fluxo para CBR e VBR.

    ```C++
    //-------------------------------------------------------------------
    //  SetEncodingProperties
    //  Create a media source from a URL.
    //
    //  guidMT:  Major type of the stream, audio or video
    //  pProps:  A pointer to the property store in which 
    //           to set the required encoding properties.
    //-------------------------------------------------------------------

    HRESULT SetEncodingProperties (const GUID guidMT, IPropertyStore* pProps)
    {
        if (!pProps)
        {
            return E_INVALIDARG;
        }

        if (EncodingMode == NONE)
        {
            return MF_E_NOT_INITIALIZED;
        }
       
        HRESULT hr = S_OK;

        PROPVARIANT var;

        switch (EncodingMode)
        {
            case CBR:
                // Set VBR to false.
                hr = InitPropVariantFromBoolean(FALSE, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_VBRENABLED, var);
                if (FAILED(hr))
                {
                    goto done;
                }

                // Set the video buffer window.
                if (guidMT == MFMediaType_Video)
                {
                    hr = InitPropVariantFromInt32(VIDEO_WINDOW_MSEC, &var);
                    if (FAILED(hr))
                    {
                        goto done;
                    }

                    hr = pProps->SetValue(MFPKEY_VIDEOWINDOW, var);    
                    if (FAILED(hr))
                    {
                        goto done;
                    }
                }
                break;

            case VBR:
                //Set VBR to true.
                hr = InitPropVariantFromBoolean(TRUE, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_VBRENABLED, var);
                if (FAILED(hr))
                {
                    goto done;
                }

                // Number of encoding passes is 1.

                hr = InitPropVariantFromInt32(1, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_PASSESUSED, var);
                if (FAILED(hr))
                {
                    goto done;
                }

                // Set the quality level.

                if (guidMT == MFMediaType_Audio)
                {
                    hr = InitPropVariantFromUInt32(98, &var);
                    if (FAILED(hr))
                    {
                        goto done;
                    }

                    hr = pProps->SetValue(MFPKEY_DESIRED_VBRQUALITY, var);    
                    if (FAILED(hr))
                    {
                        goto done;
                    }
                }
                else if (guidMT == MFMediaType_Video)
                {
                    hr = InitPropVariantFromUInt32(95, &var);
                    if (FAILED(hr))
                    {
                        goto done;
                    }

                    hr = pProps->SetValue(MFPKEY_VBRQUALITY, var);    
                    if (FAILED(hr))
                    {
                        goto done;
                    }
                }
                break;

            default:
                hr = E_UNEXPECTED;
                break;
        }    

    done:
        PropVariantClear(&var);
        return hr;
    }
    ```

    

4.  Chame [**IMFASFContentInfo:: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) para obter o repositório de propriedades globais do coletor de arquivos. Nesta chamada, você precisa passar 0 no primeiro parâmetro. Para obter mais informações, consulte "Propriedades do coletor de arquivo global" em [definindo propriedades no coletor de arquivos](setting-properties-in-the-file-sink.md).
5.  Defina a [**\_ taxa de \_ \_ bits de ajuste de MFPKEY ASFMEDIASINK**](mfpkey-asfmediasink-autoadjust-bitrate-property.md) para Variant \_ true para garantir que os valores de Bucket de vazamento no Multiplexador de ASF sejam ajustados corretamente. Para obter informações sobre essa propriedade, consulte "inicialização do Multiplexador e configurações de Bucket de vazamentos" em [criando o objeto multiplexador](creating-the-multiplexer-object.md).

    O exemplo de código a seguir define as propriedades de nível de fluxo no repositório de propriedades do coletor de arquivos.

    ```C++
        //Now we need to set global properties that will be set on the media sink
        hr = pContentInfo->GetEncodingConfigurationPropertyStore(0, &pContentInfoProps);
        if (FAILED(hr))
        {
            goto done;
        }

        //Auto adjust Bitrate
        var.vt = VT_BOOL;
        var.boolVal = VARIANT_TRUE;

        hr = pContentInfoProps->SetValue(MFPKEY_ASFMEDIASINK_AUTOADJUST_BITRATE, var);
        
        //Initialize with the profile
        hr = pContentInfo->SetProfile(pProfile);
        if (FAILED(hr))
        {
            goto done;
        }
    ```

    

    > [!Note]  
    > Há outras propriedades que você pode definir no nível global do coletor de arquivos. Para obter mais informações, consulte "Configurando o objeto ContentInfo com as configurações do codificador" em [definindo propriedades no objeto ContentInfo](setting-properties-in-the-contentinfo-object.md).

     

Você usará o ContentInfo do ASF configurado para criar um objeto de ativação para o coletor de arquivos ASF (descrito na próxima seção).

Se você estiver criando um [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate)(coletor de arquivos fora de processo), ou seja, usando um objeto de ativação, poderá usar o objeto ContentInfo configurado para instanciar o coletor de mídia ASF (descrito na próxima seção). Se você estiver criando um coletor de arquivos em processo ([**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink)), em vez de criar o objeto ContentInfo vazio, conforme descrito na etapa 1, obtenha uma referência à interface [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) chamando **IMFMediaSink:: QueryInterface** no coletor de arquivos. Em seguida, você deve configurar o objeto ContentInfo conforme descrito nesta seção.

### <a name="create-the-asf-file-sink"></a>Criar o coletor de arquivo ASF

Nesta etapa do tutorial, você usará o ASF ContentInfo configurado, que você criou na etapa anterior, para criar um objeto de ativação para o coletor de arquivo ASF chamando a função [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate) . Para obter mais informações, consulte [criando o coletor de arquivo ASF](creating-the-asf-file-sink.md).

O exemplo de código a seguir cria o objeto de ativação para o coletor de arquivos.


```C++
    //Create the activation object for the  file sink
    hr = MFCreateASFMediaSinkActivate(sURL, pContentInfo, &pActivate);
    if (FAILED(hr))
    {
        goto done;
    }

```



## <a name="build-the-partial-encoding-topology"></a>Criar a topologia de codificação parcial

Em seguida, você criará uma topologia de codificação parcial criando nós de topologia para a origem de mídia, os codificadores de mídia do Windows necessários e o coletor de arquivos ASF. Depois de adicionar os nós de topologia, você conectará os nós de origem, transformação e coletor. Antes de adicionar nós de topologia, você deve criar um objeto de topologia vazio chamando [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology).

### <a name="create-the-source-topology-node-for-the-media-source"></a>Criar o nó de topologia de origem para a origem de mídia

Nesta etapa, você criará o nó de topologia de origem para a origem da mídia.

Para criar esse nó, você precisará das seguintes referências:

-   Um ponteiro para a origem de mídia que você criou na etapa descrita na seção "criar a fonte de mídia" deste tutorial.
-   Um ponteiro para o descritor de apresentação para a origem da mídia. Você pode obter uma referência à interface IMFPresentationDescriptor da origem da mídia chamando [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).
-   Um ponteiro para o descritor de fluxo para cada fluxo na origem de mídia para o qual você criou um fluxo de destino na etapa descrita na seção "criar o objeto de perfil ASF" deste tutorial.

Para obter mais informações sobre como criar nós de origem e código de exemplo, consulte [criando nós de origem](creating-source-nodes.md).

O exemplo de código a seguir cria uma topologia parcial adicionando o nó de origem e os nós de transformação necessários. Esse código chama as funções auxiliares AddSourceNode e AddTransformOutputNodes. Essas funções são incluídas posteriormente neste tutorial.


```C++
//-------------------------------------------------------------------
//  BuildPartialTopology
//  Create a partial encoding topology by adding the source and the sink.
//
//  pSource:  A pointer to the media source to enumerate the source streams.
//  pSinkActivate: A pointer to the activation object for ASF file sink.
//  ppTopology:  Receives a pointer to the topology.
//-------------------------------------------------------------------

HRESULT BuildPartialTopology(
       IMFMediaSource *pSource, 
       IMFActivate* pSinkActivate,
       IMFTopology** ppTopology)
{
    if (!pSource || !pSinkActivate)
    {
        return E_INVALIDARG;
    }
    if (!ppTopology)
    {
        return E_POINTER;
    }

    HRESULT hr = S_OK;

    IMFPresentationDescriptor* pPD = NULL;
    IMFStreamDescriptor *pStreamDesc = NULL;
    IMFMediaTypeHandler* pMediaTypeHandler = NULL;
    IMFMediaType* pSrcType = NULL;

    IMFTopology* pTopology = NULL;
    IMFTopologyNode* pSrcNode = NULL;
    IMFTopologyNode* pEncoderNode = NULL;
    IMFTopologyNode* pOutputNode = NULL;


    DWORD cElems = 0;
    DWORD dwSrcStream = 0;
    DWORD StreamID = 0;
    GUID guidMajor = GUID_NULL;
    BOOL fSelected = FALSE;


    //Create the topology that represents the encoding pipeline
    hr = MFCreateTopology (&pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

        
    hr = pSource->CreatePresentationDescriptor(&pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pPD->GetStreamDescriptorCount(&dwSrcStream);
    if (FAILED(hr))
    {
        goto done;
    }

    for (DWORD iStream = 0; iStream < dwSrcStream; iStream++)
    {
        hr = pPD->GetStreamDescriptorByIndex(
            iStream, &fSelected, &pStreamDesc);
        if (FAILED(hr))
        {
            goto done;
        }

        if (!fSelected)
        {
            continue;
        }

        hr = AddSourceNode(pTopology, pSource, pPD, pStreamDesc, &pSrcNode);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pStreamDesc->GetMediaTypeHandler (&pMediaTypeHandler);
        if (FAILED(hr))
        {
            goto done;
        }
        
        hr = pStreamDesc->GetStreamIdentifier(&StreamID);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pMediaTypeHandler->GetMediaTypeByIndex(0, &pSrcType);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pSrcType->GetMajorType(&guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = AddTransformOutputNodes(pTopology, pSinkActivate, pSrcType, &pEncoderNode);
        if (FAILED(hr))
        {
            goto done;
        }

        //now we have the transform node, connect it to the source node
        hr = pSrcNode->ConnectOutput(0, pEncoderNode, 0);
        if (FAILED(hr))
        {
            goto done;
        }
                

        SafeRelease(&pStreamDesc);
        SafeRelease(&pMediaTypeHandler);
        SafeRelease(&pSrcType);
        SafeRelease(&pEncoderNode);
        SafeRelease(&pOutputNode);
        guidMajor = GUID_NULL;
    }

    *ppTopology = pTopology;
   (*ppTopology)->AddRef();


    wprintf_s(L"Partial Topology Built.\n");

done:
    SafeRelease(&pStreamDesc);
    SafeRelease(&pMediaTypeHandler);
    SafeRelease(&pSrcType);
    SafeRelease(&pEncoderNode);
    SafeRelease(&pOutputNode);
    SafeRelease(&pTopology);

    return hr;
}
```



O exemplo de código a seguir cria e adiciona o nó de topologia de origem à topologia de codificação. Ele usa ponteiros para um objeto de topologia anteriormente, a origem de mídia para enumerar os fluxos de origem, o descritor de apresentação da origem de mídia e o descritor de fluxo da origem de mídia. O chamador recebe um ponteiro para o nó de topologia de origem.


```C++
// Add a source node to a topology.
HRESULT AddSourceNode(
    IMFTopology *pTopology,           // Topology.
    IMFMediaSource *pSource,          // Media source.
    IMFPresentationDescriptor *pPD,   // Presentation descriptor.
    IMFStreamDescriptor *pSD,         // Stream descriptor.
    IMFTopologyNode **ppNode)         // Receives the node pointer.
{
    IMFTopologyNode *pNode = NULL;

    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_SOURCESTREAM_NODE, &pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the attributes.
    hr = pNode->SetUnknown(MF_TOPONODE_SOURCE, pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pNode->SetUnknown(MF_TOPONODE_PRESENTATION_DESCRIPTOR, pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pNode->SetUnknown(MF_TOPONODE_STREAM_DESCRIPTOR, pSD);
    if (FAILED(hr))
    {
        goto done;
    }
    
    // Add the node to the topology.
    hr = pTopology->AddNode(pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.
    *ppNode = pNode;
    (*ppNode)->AddRef();

done:
    SafeRelease(&pNode);
    return hr;
}
```



### <a name="instantiate-the-required-encoders-and-create-the-transform-nodes"></a>Instanciar os codificadores necessários e criar os nós de transformação

O pipeline de Media Foundation não insere automaticamente os codificadores do Windows Media necessários para os fluxos que ele deve codificar. O aplicativo deve adicionar os codificadores manualmente. Para fazer isso, enumere os fluxos no perfil ASF que você criou na etapa descrita na seção "criar o objeto de perfil ASF" deste tutorial. Para cada fluxo na origem e o fluxo correspondente no perfil, crie uma instância dos codificadores necessários. Para esta etapa, você precisa de um ponteiro para o objeto de ativação do coletor de arquivos que você criou na etapa descrita na seção "criar o coletor de arquivo ASF" deste tutorial.

Para obter uma visão geral sobre a criação de codificadores por meio de objetos de ativação, consulte [usando objetos de ativação de um codificador](using-an-encoder-s-activation-objects.md).

O procedimento a seguir descreve as etapas necessárias para criar uma instância dos codificadores necessários.

1.  Obtenha uma referência ao objeto ContentInfo do coletor chamando [**IMFActivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) no coletor de arquivos ativar e, em seguida, consultando o [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) no coletor de arquivos chamando **QueryInterface**.
2.  Obtenha o perfil de ASF associado ao objeto ContentInfo chamando [**IMFASFContentInfo:: GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).
3.  Enumere os fluxos no perfil. Para isso, você precisará da contagem de fluxos e de uma referência para a interface [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) de cada fluxo.

    Chame os seguintes métodos:

    -   [**IMFASFProfile::GetStreamCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount)
    -   [**IMFASFProfile:: GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream)

4.  Para cada fluxo, obtenha o tipo principal e as propriedades de codificação do fluxo do objeto ContentInfo.

    Chame os seguintes métodos:

    -   [**IMFASFStreamConfig:: GetMediaType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getmediatype)
    -   [**IMFMediaType:: getmajortype**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype)
    -   [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore)

        Para essa chamada, você precisa do número de fluxo recuperado pela chamada [**IMFASFProfile:: GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) .

5.  Dependendo do tipo de fluxo, áudio ou vídeo, instancie o objeto de ativação para o codificador chamando [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) ou [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate).

    Para chamar essas funções, você precisará das seguintes referências:

    -   Um ponteiro para o tipo de mídia do fluxo recuperado por [**IMFASFStreamConfig:: GetMediaType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getmediatype) na etapa anterior.
    -   Um ponteiro para o armazenamento de propriedade de codificação do fluxo recuperado por [**IMFASFContentInfo:: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore). Ao passar um ponteiro para o repositório de propriedades, as propriedades do fluxo definidas no coletor de arquivos são copiadas no MFT do codificador.

6.  Atualize o parâmetro de Bucket de vazamento para o fluxo de áudio.

    [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) define o tipo de saída no MFT do codificador subjacente para o codec de áudio do Windows Media. Depois que o tipo de mídia de saída é definido, o codificador Obtém a taxa média de bits do tipo de mídia de saída, calcula a taxa de bits da janela de buffer Rage e define os valores de Bucket de vazamento que serão usados durante a sessão de codificação. Você pode atualizar esses valores no coletor de arquivos consultando o codificador ou definindo valores personalizados. Para atualizar os valores, você precisará do seguinte conjunto de informações:

    -   Taxa média de bits: Obtenha a taxa média de bits do conjunto de atributos de [**\_ \_ \_ \_ bytes \_ por \_ segundo de áudio MF MT**](mf-mt-audio-avg-bytes-per-second-attribute.md) definido no tipo de mídia de saída selecionado durante a negociação do tipo de mídia.
    -   Janela buffer: você pode recuperá-la chamando [**IWMCodecLeakyBucket:: GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md).
    -   Tamanho do buffer inicial: Defina como 0.

    Crie uma matriz de DWORDs e defina o valor na propriedade [**MFPKEY \_ ASFSTREAMSINK \_ corrigida de \_ LEAKYBUCKET**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) do coletor de fluxo de áudio. Se você não fornecer os valores atualizados, a sessão de mídia os definirá adequadamente.

    Para obter mais informações, consulte [o modelo de buffer de buckets de vazamento](the-leaky-bucket-buffer-model.md).

Os objetos de ativação criados na etapa 5 devem ser adicionados à topologia como nós de topologia de transformação. Para obter mais informações e código de exemplo, consulte "criando um nó de transformação de um objeto de ativação" em [criando nós de transformação](creating-transform-nodes.md).

O exemplo de código a seguir cria e adiciona o codificador necessário ativa. Ele usa ponteiros para um objeto de topologia criado anteriormente, o objeto de ativação do coletor de arquivos e o tipo de mídia do fluxo de origem. Ele também chama AddOutputNode (consulte o próximo exemplo de código) que cria e adiciona o nó do coletor à topologia de codificação. O chamador recebe um ponteiro para o nó de topologia de origem.


```C++
//-------------------------------------------------------------------
//  AddTransformOutputNodes
//  Creates and adds the sink node to the encoding topology.
//  Creates and adds the required encoder activates.

//  pTopology:  A pointer to the topology.
//  pSinkActivate:  A pointer to the file sink's activation object.
//  pSourceType: A pointer to the source stream's media type.
//  ppNode:  Receives a pointer to the topology node.
//-------------------------------------------------------------------

HRESULT AddTransformOutputNodes(
    IMFTopology* pTopology,
    IMFActivate* pSinkActivate,
    IMFMediaType* pSourceType,
    IMFTopologyNode **ppNode    // Receives the node pointer.
    )
{
    if (!pTopology || !pSinkActivate || !pSourceType)
    {
        return E_INVALIDARG;
    }

    IMFTopologyNode* pEncNode = NULL;
    IMFTopologyNode* pOutputNode = NULL;
    IMFASFContentInfo* pContentInfo = NULL;
    IMFASFProfile* pProfile = NULL;
    IMFASFStreamConfig* pStream = NULL;
    IMFMediaType* pMediaType = NULL;
    IPropertyStore* pProps = NULL;
    IMFActivate *pEncoderActivate = NULL;
    IMFMediaSink *pSink = NULL; 

    GUID guidMT = GUID_NULL;
    GUID guidMajor = GUID_NULL;

    DWORD cStreams = 0;
    WORD wStreamNumber = 0;

    HRESULT hr = S_OK;
        
    hr = pSourceType->GetMajorType(&guidMajor);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the node.
    hr = MFCreateTopologyNode(MF_TOPOLOGY_TRANSFORM_NODE, &pEncNode);
    if (FAILED(hr))
    {
        goto done;
    }
    
    //Activate the sink
    hr = pSinkActivate->ActivateObject(__uuidof(IMFMediaSink), (void**)&pSink);
    if (FAILED(hr))
    {
        goto done;
    }
    //find the media type in the sink
    //Get content info from the sink
    hr = pSink->QueryInterface(__uuidof(IMFASFContentInfo), (void**)&pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }
    

    hr = pContentInfo->GetProfile(&pProfile);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pProfile->GetStreamCount(&cStreams);
    if (FAILED(hr))
    {
        goto done;
    }

    for(DWORD index = 0; index < cStreams ; index++)
    {
        hr = pProfile->GetStream(index, &wStreamNumber, &pStream);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pStream->GetMediaType(&pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pMediaType->GetMajorType(&guidMT);
        if (FAILED(hr))
        {
            goto done;
        }
        if (guidMT!=guidMajor)
        {
            SafeRelease(&pStream);
            SafeRelease(&pMediaType);
            guidMT = GUID_NULL;

            continue;
        }
        //We need to activate the encoder
        hr = pContentInfo->GetEncodingConfigurationPropertyStore(wStreamNumber, &pProps);
        if (FAILED(hr))
        {
            goto done;
        }

        if (guidMT == MFMediaType_Audio)
        {
             hr = MFCreateWMAEncoderActivate(pMediaType, pProps, &pEncoderActivate);
            if (FAILED(hr))
            {
                goto done;
            }
            wprintf_s(L"Audio Encoder created. Stream Number: %d .\n", wStreamNumber);

            break;
        }
        if (guidMT == MFMediaType_Video)
        {
            hr = MFCreateWMVEncoderActivate(pMediaType, pProps, &pEncoderActivate);
            if (FAILED(hr))
            {
                goto done;
            }
            wprintf_s(L"Video Encoder created. Stream Number: %d .\n", wStreamNumber);

            break;
        }
    }

    // Set the object pointer.
    hr = pEncNode->SetObject(pEncoderActivate);
    if (FAILED(hr))
    {
        goto done;
    }

    // Add the node to the topology.
    hr = pTopology->AddNode(pEncNode);
    if (FAILED(hr))
    {
        goto done;
    }

    //Add the output node to this node.
    hr = AddOutputNode(pTopology, pSinkActivate, wStreamNumber, &pOutputNode);
    if (FAILED(hr))
    {
        goto done;
    }

    //now we have the output node, connect it to the transform node
    hr = pEncNode->ConnectOutput(0, pOutputNode, 0);
    if (FAILED(hr))
    {
        goto done;
    }

   // Return the pointer to the caller.
    *ppNode = pEncNode;
    (*ppNode)->AddRef();


done:
    SafeRelease(&pEncNode);
    SafeRelease(&pOutputNode);
    SafeRelease(&pEncoderActivate);
    SafeRelease(&pMediaType);
    SafeRelease(&pProps);
    SafeRelease(&pStream);
    SafeRelease(&pProfile);
    SafeRelease(&pContentInfo);
    SafeRelease(&pSink);
    return hr;
}
```



### <a name="create-the-output-topology-nodes-for-the-file-sink"></a>Criar os nós de topologia de saída para o coletor de arquivos

Nesta etapa, você criará o nó de topologia de saída para o coletor de arquivo ASF.

Para criar esse nó, você precisará das seguintes referências:

-   Um ponteiro para o objeto de ativação que você criou na etapa descrita na seção "criar o coletor de arquivo ASF" deste tutorial.
-   Os números de fluxo para identificar os coletores de fluxo adicionados ao coletor de arquivos. Os números de fluxo correspondem à identificação do fluxo que foi definido durante a criação do fluxo.

Para obter mais informações sobre como criar nós de saída e um exemplo de código, consulte "criando um nó de saída de um objeto de ativação" em [criando nós de saída](creating-output-nodes.md).

Se você não estiver usando o objeto de ativação para o coletor de arquivos, deverá enumerar os coletores de fluxo no coletor de arquivos ASF e definir cada coletor de fluxo como o nó de saída na topologia. Para obter informações sobre a enumeração do coletor de fluxo, consulte "enumerando coletores de fluxo" em [adicionando informações de fluxo ao coletor de arquivo ASF](adding-stream-information-to-the-asf-file-sink.md).

O exemplo de código a seguir cria e adiciona o nó do coletor à topologia de codificação. Ele usa ponteiros para um objeto de topologia criado anteriormente, o objeto de ativação do coletor de arquivos e o número de identificação do fluxo. O chamador recebe um ponteiro para o nó de topologia de origem.


```C++
// Add an output node to a topology.
HRESULT AddOutputNode(
    IMFTopology *pTopology,     // Topology.
    IMFActivate *pActivate,     // Media sink activation object.
    DWORD dwId,                 // Identifier of the stream sink.
    IMFTopologyNode **ppNode)   // Receives the node pointer.
{
    IMFTopologyNode *pNode = NULL;

    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_OUTPUT_NODE, &pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the object pointer.
    hr = pNode->SetObject(pActivate);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the stream sink ID attribute.
    hr = pNode->SetUINT32(MF_TOPONODE_STREAMID, dwId);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pNode->SetUINT32(MF_TOPONODE_NOSHUTDOWN_ON_REMOVE, FALSE);
    if (FAILED(hr))
    {
        goto done;
    }

    // Add the node to the topology.
    hr = pTopology->AddNode(pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.
    *ppNode = pNode;
    (*ppNode)->AddRef();

done:
    SafeRelease(&pNode);
    return hr;
}
```



O exemplo de código a seguir enumera os coletores de fluxo para um determinado coletor de mídia.


```C++
//-------------------------------------------------------------------
//  EnumerateStreamSinks
//  Enumerates the stream sinks within the specified media sink.
//
//  pSink:  A pointer to the media sink.
//-------------------------------------------------------------------
HRESULT EnumerateStreamSinks (IMFMediaSink* pSink)
{
    if (!pSink)
    {
        return E_INVALIDARG;
    }
    
    IMFStreamSink* pStreamSink = NULL;
    DWORD cStreamSinks = 0;

    HRESULT hr = pSink->GetStreamSinkCount(&cStreamSinks);
    if (FAILED(hr))
    {
        goto done;
    }

    for(DWORD index = 0; index < cStreamSinks; index++)
    {
        hr = pSink->GetStreamSinkByIndex (index, &pStreamSink);
        if (FAILED(hr))
        {
            goto done;
        }

        //Use the stream sink
        //Not shown.
    }
done:
    SafeRelease(&pStreamSink);

    return hr;
}
```



### <a name="connect-the-source-transform-and-sink-nodes"></a>Conectar os nós de origem, transformação e coletor

Nesta etapa, você conectará o nó de origem ao nó de transformação que faz referência à codificação ativada que você criou na etapa descrita na seção "instanciar os codificadores necessários e criar os nós de transformação" deste tutorial. O nó de transformação será conectado ao nó de saída que contém o objeto de ativação para o coletor de arquivos.

## <a name="handling-the-encoding-session"></a>Manipulando a sessão de codificação

Na etapa, você executará as seguintes etapas:

1.  Chame [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) para criar uma sessão de codificação.
2.  Chame [**IMFMediaSession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) para definir a topologia de codificação na sessão. Se a chamada for concluída, a sessão de mídia avaliará os nós de topologia e inserirá objetos de transformação adicionais, como um decodificador que converte a origem compactada especificada em amostras não compactadas para alimentar como entrada para o codificador.
3.  Chame [**IMFMediaSession:: GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent) para solicitar os eventos gerados pela sessão de mídia.

    No loop de eventos, você iniciará e fechará a sessão de codificação dependendo dos eventos gerados pela sessão de mídia. A chamada [**IMFMediaSession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) resulta na sessão de mídia que gera o evento [MESessionTopologyStatus](mesessiontopologystatus.md) com o \_ sinalizador MF TOPOSTATUS \_ Ready definido. Todos os eventos são gerados de forma assíncrona e um aplicativo pode recuperar esses eventos de forma síncrona ou assíncrona. Como o aplicativo neste tutorial é um aplicativo de console e o bloqueio de threads de interface do usuário não é uma preocupação, obteremos os eventos da sessão de mídia de forma síncrona.

    Para obter os eventos de forma assíncrona, seu aplicativo deve implementar a interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) . Para obter mais informações e um exemplo de implementação dessa interface, consulte "manipulando eventos de sessão" em [How to Play Media files with Media Foundation](how-to-play-unprotected-media-files.md).

No loop de eventos para obter eventos de sessão de mídia, aguarde o evento [MESessionTopologyStatus](mesessiontopologystatus.md) que é gerado quando a topologia [**IMFMediaSession::**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) Seté concluída e a topologia é resolvida. Após obter o evento MESessionTopologyStatus, inicie a sessão de codificação chamando [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start). A sessão de mídia gera o evento [MEEndOfPresentation](meendofpresentation.md) quando todas as operações de codificação são concluídas. Esse evento deve ser tratado para codificação de VBR e é discutido na próxima seção "atualizar propriedades de codificação no coletor de arquivos para codificação de VBR" deste tutorial.

A sessão de mídia gera o objeto de cabeçalho ASF e finaliza o arquivo quando a sessão de codificação é concluída e, em seguida, gera o evento [MESessionClosed](mesessionclosed.md) . Esse evento deve ser tratado com a execução de operações de desligamento apropriadas na sessão de mídia. Para iniciar as operações de desligamento, chame [**IMFMediaSession:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown). Depois que a sessão de codificação for fechada, você não poderá definir outra topologia para codificação na mesma instância de sessão de mídia. Para codificar outro arquivo, a sessão de mídia atual deve ser fechada e liberada e a nova topologia deve ser definida em uma sessão de mídia recém-criada. O exemplo de código a seguir cria a sessão de mídia, define a topologia de codificação e manipula os eventos de sessão de mídia.

O exemplo de código a seguir cria a sessão de mídia, define a topologia de codificação e controla a sessão de codificação manipulando eventos da sessão de mídia.


```C++
//-------------------------------------------------------------------
//  Encode
//  Controls the encoding session and handles events from the media session.
//
//  pTopology:  A pointer to the encoding topology.
//-------------------------------------------------------------------

HRESULT Encode(IMFTopology *pTopology)
{
    if (!pTopology)
    {
        return E_INVALIDARG;
    }
    
    IMFMediaSession *pSession = NULL;
    IMFMediaEvent* pEvent = NULL;
    IMFTopology* pFullTopology = NULL;
    IUnknown* pTopoUnk = NULL;


    MediaEventType meType = MEUnknown;  // Event type

    HRESULT hr = S_OK;
    HRESULT hrStatus = S_OK;            // Event status
                
    MF_TOPOSTATUS TopoStatus = MF_TOPOSTATUS_INVALID; // Used with MESessionTopologyStatus event.    
        

    hr = MFCreateMediaSession(NULL, &pSession);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSession->SetTopology(MFSESSION_SETTOPOLOGY_IMMEDIATE, pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    //Get media session events synchronously
    while (1)
    {
        hr = pSession->GetEvent(0, &pEvent);
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

       switch(meType)
        {
            case MESessionTopologyStatus:
                {
                    // Get the status code.
                    MF_TOPOSTATUS status = (MF_TOPOSTATUS)MFGetAttributeUINT32(
                                             pEvent, MF_EVENT_TOPOLOGY_STATUS, MF_TOPOSTATUS_INVALID);

                    if (status == MF_TOPOSTATUS_READY)
                    {
                        PROPVARIANT var;
                        PropVariantInit(&var);
                        wprintf_s(L"Topology resolved and set on the media session.\n");

                        hr = pSession->Start(NULL, &var);
                        if (FAILED(hr))
                        {
                            goto done;
                        }

                    }
                    if (status == MF_TOPOSTATUS_STARTED_SOURCE)
                    {
                        wprintf_s(L"Encoding started.\n");
                        break;
                    }
                    if (status == MF_TOPOSTATUS_ENDED)
                    {
                        wprintf_s(L"Encoding complete.\n");
                        hr = pSession->Close();
                        if (FAILED(hr))
                        {
                            goto done;
                        }

                        break;
                    }
                }
                break;


            case MESessionEnded:
                wprintf_s(L"Encoding complete.\n");
                hr = pSession->Close();
                if (FAILED(hr))
                {
                    goto done;
                }
                break;

            case MEEndOfPresentation:
                {
                    if (EncodingMode == VBR)
                    {
                        hr = pSession->GetFullTopology(MFSESSION_GETFULLTOPOLOGY_CURRENT, 0, &pFullTopology);
                        if (FAILED(hr))
                        {
                            goto done;
                        }
                        hr = PostEncodingUpdate(pFullTopology);
                        if (FAILED(hr))
                        {
                            goto done;
                        }
                        wprintf_s(L"Updated sinks for VBR. \n");
                    }
                }
                break;

            case MESessionClosed:
                wprintf_s(L"Encoding session closed.\n");

                hr = pSession->Shutdown();
                goto done;
        }
        if (FAILED(hr))
        {
            goto done;
        }

        SafeRelease(&pEvent);

    }
done:
    SafeRelease(&pEvent);
    SafeRelease(&pSession);
    SafeRelease(&pFullTopology);
    SafeRelease(&pTopoUnk);
    return hr;
}
```



## <a name="update-encoding-properties-in-the-file-sink"></a>Atualizar propriedades de codificação no coletor de arquivos

Determinadas propriedades de codificação, como a taxa de bits de codificação e os valores de buckets de vazamento precisos, não são conhecidas até que a codificação seja concluída, especialmente para a codificação de VBR. Para obter os valores corretos, o aplicativo deve aguardar o evento [MEEndOfPresentation](meendofpresentation.md) que indica que a sessão de codificação foi concluída. Os valores de Bucket de vazamento devem ser atualizados no coletor para que o objeto de cabeçalho ASF possa refletir os valores precisos.

O procedimento a seguir descreve as etapas necessárias para percorrer os nós na topologia de codificação para obter o nó de coletor de arquivo e definir as propriedades de Bucket de vazamento necessárias.

**Para atualizar os valores da propriedade post Encoding no coletor de arquivo ASF**

1.  Chame [**IMFTopology:: GetOutputNodeCollection**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getoutputnodecollection) para obter a coleção de nós de saída da topologia de codificação.
2.  Para cada nó, obtenha um ponteiro para o coletor de fluxo no nó chamando [**IMFTopologyNode:: GetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getobject). Consulta para a interface [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) no ponteiro [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) retornado por **IMFTopologyNode:: GetObject**.
3.  Para cada coletor de fluxo, obtenha o nó downstream (codificador) chamando [**IMFTopologyNode:: getinput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getinput).
4.  Consulte o nó para obter o ponteiro [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) do nó do codificador.
5.  Consulte o codificador para o ponteiro [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para obter o armazenamento de propriedade de codificação do codificador.
6.  Consulte o coletor de fluxo para o ponteiro [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para obter o repositório de propriedades do coletor de fluxo.
7.  Chame [**IPropertyStore:: GetValue**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para obter os valores de propriedade necessários do repositório de propriedades do codificador e copie-os para o repositório de propriedades do coletor de fluxo chamando **IPropertyStore:: SetValue**.

A tabela a seguir mostra os valores de propriedade de codificação post que devem ser definidos no coletor de fluxo para o fluxo de vídeo.



| Tipo de codificação                                                                                  | Nome da propriedade (GetValue)                                                                        | Nome da propriedade (DefinirValor)                                                                                                |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [Codificação de taxa de bits constante](constant-bit-rate-encoding.md)                                   | MFPKEY \_ BAVG<br/> MFPKEY \_ RAVG<br/>                                                 | MFPKEY \_ stat \_ BAVG<br/> MFPKEY \_ stat \_ RAVG<br/>                                                             |
| [Codificação de taxa de bits variável baseada em qualidade](quality-based-variable-bit-rate--vbr--encoding.md) | MFPKEY \_ BAVG<br/> MFPKEY \_ RAVG<br/> MFPKEY \_ BMAX<br/> MFPKEY \_ RMAX<br/> | MFPKEY \_ stat \_ BAVG<br/> MFPKEY \_ stat \_ RAVG<br/> MFPKEY \_ stat \_ BMAX<br/> MFPKEY \_ stat \_ RMAX<br/> |



 

O exemplo de código a seguir define os valores de propriedade de pós-codificação.


```C++
//-------------------------------------------------------------------
//  PostEncodingUpdate
//  Updates the file sink with encoding properties set on the encoder
//  during the encoding session.
    //1. Get the output nodes
    //2. For each node, get the downstream node
    //3. For the downstream node, get the MFT
    //4. Get the property store
    //5. Get the required values
    //6. Set them on the stream sink
//
//  pTopology: A pointer to the full topology retrieved from the media session.
//-------------------------------------------------------------------

HRESULT PostEncodingUpdate(IMFTopology *pTopology)
{
    if (!pTopology)
    {
        return E_INVALIDARG;
    }

    HRESULT hr = S_OK;

    IMFCollection* pOutputColl = NULL;
    IUnknown* pNodeUnk = NULL;
    IMFMediaType* pType = NULL;
    IMFTopologyNode* pNode = NULL;
    IUnknown* pSinkUnk = NULL;
    IMFStreamSink* pStreamSink = NULL;
    IMFTopologyNode* pEncoderNode = NULL;
    IUnknown* pEncoderUnk = NULL;
    IMFTransform* pEncoder = NULL;
    IPropertyStore* pStreamSinkProps = NULL;
    IPropertyStore* pEncoderProps = NULL;

    GUID guidMajorType = GUID_NULL;

    PROPVARIANT var;
    PropVariantInit( &var );

    DWORD cElements = 0;

    hr = pTopology->GetOutputNodeCollection( &pOutputColl);
    if (FAILED(hr))
    {
        goto done;
    }


    hr = pOutputColl->GetElementCount(&cElements);
    if (FAILED(hr))
    {
        goto done;
    }


    for(DWORD index = 0; index < cElements; index++)
    {
        hr = pOutputColl->GetElement(index, &pNodeUnk);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pNodeUnk->QueryInterface(IID_IMFTopologyNode, (void**)&pNode);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pNode->GetInputPrefType(0, &pType);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pType->GetMajorType( &guidMajorType );
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pNode->GetObject(&pSinkUnk);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pSinkUnk->QueryInterface(IID_IMFStreamSink, (void**)&pStreamSink);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pNode->GetInput( 0, &pEncoderNode, NULL );
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pEncoderNode->GetObject(&pEncoderUnk);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pEncoderUnk->QueryInterface(IID_IMFTransform, (void**)&pEncoder);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pStreamSink->QueryInterface(IID_IPropertyStore, (void**)&pStreamSinkProps);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pEncoder->QueryInterface(IID_IPropertyStore, (void**)&pEncoderProps);
        if (FAILED(hr))
        {
            goto done;
        }

        if( guidMajorType == MFMediaType_Video )
        {            
            hr = pEncoderProps->GetValue( MFPKEY_BAVG, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_BAVG, var );
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_RAVG, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_RAVG, var);
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_BMAX, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_BMAX, var);
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_RMAX, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_RMAX, var);
            if (FAILED(hr))
            {
                goto done;
            }
        }
        else if( guidMajorType == MFMediaType_Audio )
        {      
            hr = pEncoderProps->GetValue( MFPKEY_STAT_BAVG, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_BAVG, var );
            if (FAILED(hr))
            {
                goto done;
            }
            
            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_STAT_RAVG, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_RAVG, var );
            if (FAILED(hr))
            {
                goto done;
            }
            
            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_STAT_BMAX, &var);
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_BMAX, var);
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_STAT_RMAX, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_RMAX, var );         
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_WMAENC_AVGBYTESPERSEC, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_WMAENC_AVGBYTESPERSEC, var );         
            if (FAILED(hr))
            {
                goto done;
            }
        } 
        PropVariantClear( &var ); 
   }
done:
    SafeRelease (&pOutputColl);
    SafeRelease (&pNodeUnk);
    SafeRelease (&pType);
    SafeRelease (&pNode);
    SafeRelease (&pSinkUnk);
    SafeRelease (&pStreamSink);
    SafeRelease (&pEncoderNode);
    SafeRelease (&pEncoderUnk);
    SafeRelease (&pEncoder);
    SafeRelease (&pStreamSinkProps);
    SafeRelease (&pEncoderProps);

    return hr;
   
}
```



## <a name="implement-main"></a>Implementar principal

O exemplo de código a seguir mostra a função main do seu aplicativo de console.


```C++
int wmain(int argc, wchar_t* argv[])
{
    HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);

    if (argc != 4)
    {
        wprintf_s(L"Usage: %s inputaudio.mp3, %s output.wm*, %Encoding Type: CBR, VBR\n");
        return 0;
    }


    HRESULT             hr = S_OK;

    IMFMediaSource* pSource = NULL;
    IMFTopology* pTopology = NULL;
    IMFActivate* pFileSinkActivate = NULL;

    hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | COINIT_DISABLE_OLE1DDE);
    if (FAILED(hr))
    {
        goto done;
    }

    //Set the requested encoding mode
    if (wcscmp(argv[3], L"CBR")==0)
    {
        EncodingMode = CBR;
    }
    else if (wcscmp(argv[3], L"VBR")==0)
    {
        EncodingMode = VBR;
    }
    else
    {
        EncodingMode = CBR;
    }

    // Start up Media Foundation platform.
    hr = MFStartup(MF_VERSION);
    if (FAILED(hr))
    {
        goto done;
    }

    //Create the media source
    hr = CreateMediaSource(argv[1], &pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    //Create the file sink activate
    hr = CreateMediaSink(argv[2], pSource, &pFileSinkActivate);
    if (FAILED(hr))
    {
        goto done;
    }

    //Build the encoding topology.
    hr = BuildPartialTopology(pSource, pFileSinkActivate, &pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    //Instantiate the media session and start encoding
    hr = Encode(pTopology);
    if (FAILED(hr))
    {
        goto done;
    }


done:
    // Clean up.
    SafeRelease(&pSource);
    SafeRelease(&pTopology);
    SafeRelease(&pFileSinkActivate);

    MFShutdown();
    CoUninitialize();

    if (FAILED(hr))
    {
        wprintf_s(L"Could not create the output file due to 0x%X\n", hr);
    }
    return 0;
}
```



## <a name="test-the-output-file"></a>Testar o arquivo de saída

A lista a seguir descreve uma lista de verificação para testar o arquivo codificado. Esses valores podem ser verificados na caixa de diálogo Propriedades do arquivo que você pode exibir clicando com o botão direito do mouse no arquivo codificado e selecionando **Propriedades** no menu de contexto.

-   O caminho do arquivo codificado é preciso.
-   O tamanho do arquivo é maior que zero KB e a duração da reprodução corresponde à duração do arquivo de origem.
-   Para o fluxo de vídeo, verifique a largura e a altura do quadro, taxa de quadros. Esses valores devem corresponder aos valores que você especificou no perfil ASF criado na etapa descrita na seção "criar o objeto de perfil ASF".
-   Para o fluxo de áudio, a taxa de bits deve ser próxima ao valor especificado no tipo de mídia de destino.
-   Abra o arquivo no Windows Media Player e verifique a qualidade da codificação.
-   Abra o arquivo ASF no ASFViewer para ver a estrutura de um arquivo ASF. Essa ferramenta pode ser baixada deste [site da Microsoft](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea).

## <a name="common-error-codes-and-debugging-tips"></a>Códigos de erro comuns e dicas de depuração

A lista a seguir descreve os códigos de erro comuns que você pode receber e as dicas de depuração.

-   A chamada para [**IMFSourceResolver:: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) interrompe o aplicativo.

    Verifique se você inicializou a plataforma Media Foundation chamando [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup). Essa função configura a plataforma assíncrona que é usada por todos os métodos que iniciam operações assíncronas, como [**IMFSourceResolver:: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl), internamente.

-   [**IMFSourceResolver:: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) retorna HRESULT 0x80070002 "o sistema não pode localizar o arquivo especificado.

    Verifique se o nome do arquivo de entrada especificado pelo usuário no primeiro argumento existe.

-   HRESULT 0x80070020 "o processo não pode acessar o arquivo porque ele está sendo usado por outro processo. "

    Certifique-se de que a entrada e os arquivos de saída não estejam atualmente em uso por outro recurso no sistema.

-   Chamadas para métodos [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) retornam MF \_ E \_ INVALIDMEDIATYPE.

    Certifique-se de que as seguintes condições sejam verdadeiras:

    -   O tipo de entrada ou o tipo de saída especificado é compatível com os tipos de mídia aos quais o codificador dá suporte.
    -   Os tipos de mídia que você especificou estão completos. Para que os tipos de mídia sejam concluídos, consulte os atributos necessários nas seções "criar um tipo de mídia de áudio compactado" e "criar um tipo de mídia de vídeo compactado" deste tutorial.
    -   Verifique se você definiu a taxa de bits de destino no tipo de mídia parcial ao qual está adicionando os dados privados do codec.

-   A sessão de mídia retorna MF \_ E \_ não há suporte para \_ \_ o tipo de D3D no status do evento.

    Esse erro é retornado quando o tipo de mídia da origem indica um modo de entrelaçamento misto sem suporte pelo codificador de vídeo do Windows Media. Se o tipo de mídia de vídeo compactado estiver definido para usar o modo progressivo, o pipeline deverá usar uma transformação de desentrelaçamento. Como o pipeline não consegue encontrar uma correspondência (indicada por esse código de erro), você deve inserir um desentrelaçador (processador de vídeo transcodificar) entre os nós do decodificador e do codificador manualmente.

-   A sessão de mídia retorna E \_ INVALIDARG no status do evento.

    Esse erro é retornado quando os atributos de tipo de mídia da origem não são compatíveis com os atributos do tipo de mídia de saída definido no codificador de mídia do Windows.

-   [**IWMCodecPrivateData:: GetPrivateData**](../wmformat/iwmcodecprivatedata-getprivatedata.md) retorna HRESULT 0x80040203 "ocorreu um erro de sintaxe ao tentar avaliar uma cadeia de caracteres de consulta"

    Verifique se o tipo de entrada está definido no MFT do codificador.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Componentes ASF da camada de pipeline](pipeline-layer-asf-components.md)
</dt> </dl>

 

 
