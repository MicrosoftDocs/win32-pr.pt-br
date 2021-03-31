---
description: Este tutorial demonstra como gravar um novo arquivo de áudio (. WMA) extraindo o conteúdo de mídia de um arquivo de áudio descompactado (. wav) e, em seguida, compactando-o no formato ASF.
ms.assetid: f310c6ed-52e7-4828-9d4c-2f7ced9080c5
title: 'Tutorial: gravando um arquivo WMA usando objetos WMContainer'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d156b75ced6cde2953ec90362ed13b0cc53bb83c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827798"
---
# <a name="tutorial-writing-a-wma-file-by-using-wmcontainer-objects"></a>Tutorial: gravando um arquivo WMA usando objetos WMContainer

Este tutorial demonstra como gravar um novo arquivo de áudio (. WMA) extraindo o conteúdo de mídia de um arquivo de áudio descompactado (. wav) e, em seguida, compactando-o no formato ASF. O modo de codificação usado para a conversão é [constante de codificação de taxa de bits](constant-bit-rate-encoding.md) (CBR). Nesse modo, antes da sessão de codificação, o aplicativo especifica uma taxa de bits de destino que o codificador deve atingir.

Neste tutorial, você criará um aplicativo de console que usa os nomes de dados de entrada e saída como argumentos. O aplicativo obtém os exemplos de mídia descompactados de um aplicativo de análise de arquivo Wave, que é fornecido com este tutorial. Esses exemplos são enviados para o codificador para conversão no formato Windows Media Audio 9. O codificador está configurado para codificação de CBR e usa a primeira taxa de bits disponível durante a negociação do tipo de mídia como a taxa de bits de destino. Os exemplos codificados são enviados para o multiplexador para pacotes no formato de dados ASF. Esses pacotes serão gravados em um fluxo de bytes que representa o objeto de dados ASF. Depois que a seção de dados estiver pronta, você criará um arquivo de áudio ASF e gravará o novo objeto de cabeçalho ASF que consolida todas as informações de cabeçalho e, em seguida, acrescentará o fluxo de bytes do objeto de dados ASF.

Este tutorial contém as seguintes seções:

-   [Pré-requisitos](#prerequisites)
-   [Terminologia](#terminology)
-   [1. configurar o projeto](#1-set-up-the-project)
-   [2. declarar funções auxiliares](#2-declare-helper-functions)
-   [3. abrir um arquivo de áudio](#3-open-an-audio-file)
-   [4. configurar o codificador](#4-configure-the-encoder)
-   [5. Crie o objeto ContentInfo do ASF.](#5-create-the-asf-contentinfo-object)
-   [6. criar o multiplexador de ASF](#6-create-the-asf-multiplexer)
-   [7. gerar novos pacotes de dados ASF](#7-generate-new-asf-data-packets)
-   [8. gravar o arquivo ASF](#8-write-the-asf-file)
-   [9. definir a função de Entry-Point](#9-define-the-entry-point-function)
-   [Tópicos relacionados](#related-topics)

## <a name="prerequisites"></a>Pré-requisitos

Este tutorial pressupõe o seguinte:

-   Você está familiarizado com a estrutura de um arquivo ASF e os componentes fornecidos pelo Media Foundation para trabalhar com objetos ASF. Esses componentes incluem ContentInfo, Splitter, multiplexador e objetos de perfil. Para obter mais informações, consulte [componentes ASF do WMContainer](wmcontainer-asf-components.md).
-   Você está familiarizado com os codificadores de mídia do Windows e os vários tipos de codificação, particularmente CBR. Para obter mais informações, consulte [codificadores de mídia do Windows](windows-media-encoders.md) .
-   Você está familiarizado com [buffers de mídia](media-buffers.md) e fluxos de bytes: especificamente, operações de arquivo usando um fluxo de bytes e gravando o conteúdo de um buffer de mídia em um fluxo de bytes.

## <a name="terminology"></a>Terminologia

Este tutorial usa os seguintes termos:

-   Tipo de mídia de origem: objeto de tipo de mídia, expõe a interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) , que descreve o conteúdo do arquivo de entrada.
-   Perfil de áudio: objeto de perfil, expõe a interface [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) , que contém somente fluxos de áudio do arquivo de saída.
-   Exemplo de fluxo: a amostra de mídia, expõe a interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , representa os dados de mídia do arquivo de entrada obtidos do codificador em um estado compactado.
-   Objeto ContentInfo: o [objeto ASF ContentInfo](asf-contentinfo-object.md), expõe a interface [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) , que representa o objeto de cabeçalho ASF do arquivo de saída.
-   Fluxo de bytes de dados: o objeto de fluxo de bytes, expõe a interface [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) , que representa a parte inteira do objeto de dados ASF do arquivo de saída.
-   Pacote de dados: exemplo de mídia, expõe a interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , gerada pelo [Multiplexador de ASF](asf-multiplexer.md); representa um pacote de dados ASF que será gravado no fluxo de bytes de dados.
-   Fluxo de bytes de saída: objeto de fluxo de bytes, expõe a interface [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) , que contém o conteúdo do arquivo de saída.

## <a name="1-set-up-the-project"></a>1. configurar o projeto

1.  Inclua os seguintes cabeçalhos no arquivo de origem:

    ```C++
    #include <new>
    #include <stdio.h>       // Standard I/O
    #include <windows.h>     // Windows headers
    #include <mfapi.h>       // Media Foundation platform
    #include <wmcontainer.h> // ASF interfaces
    #include <mferror.h>     // Media Foundation error codes
    ```

    

2.  Link para os seguintes arquivos de biblioteca:

    -   mfplat. lib
    -   MF. lib
    -   mfuuid. lib

3.  Declare a função [SafeRelease](saferelease.md) .
4.  Inclua a classe CWmaEncoder em seu projeto. Para obter o código-fonte completo dessa classe, consulte [código de exemplo do codificador](encoder-example-code.md).

## <a name="2-declare-helper-functions"></a>2. declarar funções auxiliares

Este tutorial usa as seguintes funções auxiliares para ler e gravar a partir de um fluxo de bytes.

-   `AppendToByteStream`: Anexa o conteúdo de um fluxo de bytes a outro fluxo de bytes.
-   WriteBufferToByteStream: grava dados de um buffer de mídia em um fluxo de bytes.

Para obter mais informações, consulte [**IMFByteStream:: Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write). O código a seguir mostra essas funções auxiliares:


```C++
//-------------------------------------------------------------------
// AppendToByteStream
//
// Reads the contents of pSrc and writes them to pDest.
//-------------------------------------------------------------------

HRESULT AppendToByteStream(IMFByteStream *pSrc, IMFByteStream *pDest)
{
    HRESULT hr = S_OK;

    const DWORD READ_SIZE = 1024;

    BYTE buffer[READ_SIZE];

    while (1)
    {
        ULONG cbRead;

        hr = pSrc->Read(buffer, READ_SIZE, &cbRead);

        if (FAILED(hr)) { break; }

        if (cbRead == 0)
        {
            break;
        }

        hr = pDest->Write(buffer, cbRead, &cbRead);

        if (FAILED(hr)) { break; }
    }

    return hr;
}
```




```C++
//-------------------------------------------------------------------
// WriteBufferToByteStream
//
// Writes data from a media buffer to a byte stream.
//-------------------------------------------------------------------

HRESULT WriteBufferToByteStream(
    IMFByteStream *pStream,   // Pointer to the byte stream.
    IMFMediaBuffer *pBuffer,  // Pointer to the media buffer.
    DWORD *pcbWritten         // Receives the number of bytes written.
    )
{
    HRESULT hr = S_OK;
    DWORD cbData = 0;
    DWORD cbWritten = 0;
    BYTE *pMem = NULL;

    hr = pBuffer->Lock(&pMem, NULL, &cbData);

    if (SUCCEEDED(hr))
    {
        hr = pStream->Write(pMem, cbData, &cbWritten);
    }

    if (SUCCEEDED(hr))
    {
        if (pcbWritten)
        {
            *pcbWritten = cbWritten;
        }
    }

    if (pMem)
    {
        pBuffer->Unlock();
    }
    return hr;
}
```



## <a name="3-open-an-audio-file"></a>3. abrir um arquivo de áudio

Este tutorial pressupõe que seu aplicativo irá gerar áudio descompactado para codificação. Para essa finalidade, duas funções são declaradas neste tutorial:


```C++
HRESULT OpenAudioFile(PCWSTR pszURL, IMFMediaType **ppAudioFormat);
HRESULT GetNextAudioSample(BOOL *pbEOS, IMFSample **ppSample);
```



A implementação dessas funções é deixada para o leitor.

-   A `OpenAudioFile` função deve abrir o arquivo de mídia especificado por *pszURL* e retornar um ponteiro para um tipo de mídia que descreve um fluxo de áudio.
-   A `GetNextAudioSample` função deve ler áudio PCM não compactado do arquivo que foi aberto pelo `OpenAudioFile` . Quando o final do arquivo for atingido, *pbEOS* receberá o valor **true**. Caso contrário, o *ppSample* receberá um exemplo de mídia que contém o buffer de áudio.

## <a name="4-configure-the-encoder"></a>4. configurar o codificador

Em seguida, crie o codificador, configure-o para produzir exemplos de fluxo codificados em CBR e negocie os tipos de mídia de entrada e saída.

Em Media Foundation, os codificadores (expõem a interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) ) são implementados como [transformações de Media Foundation](media-foundation-transforms.md) (MFT).

Neste tutorial, o codificador é implementado na `CWmaEncoder` classe que fornece um wrapper para o MFT. Para obter o código-fonte completo dessa classe, consulte [código de exemplo do codificador](encoder-example-code.md).

> [!Note]  
> Opcionalmente, você pode especificar o tipo de codificação como CBR. Por padrão, o codificador está configurado para usar a codificação CBR. Para obter mais informações, consulte [codificação de taxa de bits constante](constant-bit-rate-encoding.md). Você pode definir propriedades adicionais dependendo do tipo de codificação, para obter informações sobre as propriedades que são específicas para um modo de codificação, consulte [codificação de taxa de bits variável baseada em qualidade](quality-based-variable-bit-rate--vbr--encoding.md), [codificação de taxa de bits variável irrestrita](unconstrained-variable-bit-rate--vbr--encoding.md)e [codificação de taxa de bits variável com restrição de pico](peak-constrained-variable-bit-rate--vbr--encoding.md).

 


```C++
    CWmaEncoder* pEncoder = NULL; //Pointer to the Encoder object.

    hr = OpenAudioFile(sInputFileName, &pInputType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Initialize the WMA encoder wrapper.

    pEncoder = new (std::nothrow) CWmaEncoder();
    if (pEncoder == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    hr = pEncoder->Initialize();
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pEncoder->SetEncodingType(EncodeMode_CBR);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pEncoder->SetInputType(pInputType);
    if (FAILED(hr))
    {
        goto done;
    }
```



## <a name="5-create-the-asf-contentinfo-object"></a>5. Crie o objeto ContentInfo do ASF.

O [objeto ASF ContentInfo](asf-contentinfo-object.md) contém informações sobre os vários objetos de cabeçalho do arquivo de saída.

Primeiro, crie um perfil de ASF para o fluxo de áudio:

1.  Chame [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) para criar um objeto de perfil ASF vazio. O perfil ASF expõe a interface [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) . Para obter mais informações, consulte [criando e configurando fluxos ASF](creating-and-configuring-asf-streams.md).
2.  Obtenha o formato de áudio codificado do `CWmaEncoder` objeto.
3.  Chame [**IMFASFProfile:: CreateStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream) para criar um novo fluxo para o perfil ASF. Passe um ponteiro para a interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) , que representa o formato de fluxo.
4.  Chame [**IMFASFStreamConfig:: SetStreamNumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setstreamnumber) para atribuir um identificador de fluxo.
5.  Defina os parâmetros de "Bucket de vazamentos" definindo o atributo [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) no objeto de fluxo.
6.  Chame [**IMFASFProfile:: SetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream) para adicionar o novo fluxo ao perfil.

Agora, crie o objeto ContentInfo do ASF da seguinte maneira:

1.  Chame [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) para criar um objeto ContentInfo vazio.
2.  Chame [**IMFASFContentInfo:: setprofile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) para definir o perfil de ASF.

O código a seguir mostra estas etapas:


```C++
HRESULT CreateASFContentInfo(
    CWmaEncoder* pEncoder,
    IMFASFContentInfo** ppContentInfo
    )
{
    HRESULT hr = S_OK;
    
    IMFASFProfile* pProfile = NULL;
    IMFMediaType* pMediaType = NULL;
    IMFASFStreamConfig* pStream = NULL;
    IMFASFContentInfo* pContentInfo = NULL;

    // Create the ASF profile object.

    hr = MFCreateASFProfile(&pProfile); 
    if (FAILED(hr))
    {
        goto done;
    }

    // Create a stream description for the encoded audio.

    hr = pEncoder->GetOutputType(&pMediaType); 
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pProfile->CreateStream(pMediaType, &pStream); 
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pStream->SetStreamNumber(DEFAULT_STREAM_NUMBER); 
    if (FAILED(hr))
    {
        goto done;
    }

    // Set "leaky bucket" values.

    LeakyBucket bucket;

    hr = pEncoder->GetLeakyBucket1(&bucket);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pStream->SetBlob(
        MF_ASFSTREAMCONFIG_LEAKYBUCKET1, 
        (UINT8*)&bucket, 
        sizeof(bucket)
        );

    if (FAILED(hr))
    {
        goto done;
    }

    //Add the stream to the profile

    hr = pProfile->SetStream(pStream);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the ASF ContentInfo object.

    hr = MFCreateASFContentInfo(&pContentInfo); 
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pContentInfo->SetProfile(pProfile); 
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.

    *ppContentInfo = pContentInfo;
    (*ppContentInfo)->AddRef();

done:
    SafeRelease(&pProfile);
    SafeRelease(&pStream);
    SafeRelease(&pMediaType);
    SafeRelease(&pContentInfo);
    return hr;
}
```



## <a name="6-create-the-asf-multiplexer"></a>6. criar o multiplexador de ASF

O [multiplexador ASF](asf-multiplexer.md) gera pacotes de dados ASF.

1.  Chame [**MFCreateASFMultiplexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmultiplexer) para criar o multiplexador de ASF.
2.  Chame [**IMFASFMultiplexer:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) para inicializar o multiplexador. Passe um ponteiro para o objeto de informações de conteúdo do ASF, que foi criado na seção anterior.
3.  Chame [**IMFASFMultiplexer:: SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags) para definir o sinalizador **de \_ taxa de \_ \_ bits de AutoAjuste do Multiplexador MFASF** . Quando essa configuração é usada, o multiplexador ajusta automaticamente a taxa de bits do conteúdo ASF para corresponder às características dos fluxos que estão sendo multiplexados.


```C++
HRESULT CreateASFMux( 
    IMFASFContentInfo* pContentInfo,
    IMFASFMultiplexer** ppMultiplexer
    )
{
    HRESULT hr = S_OK;
    
    IMFMediaType* pMediaType = NULL;
    IMFASFMultiplexer *pMultiplexer = NULL;

    // Create and initialize the ASF Multiplexer object.

    hr = MFCreateASFMultiplexer(&pMultiplexer);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pMultiplexer->Initialize(pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }

    // Enable automatic bit-rate adjustment.

    hr = pMultiplexer->SetFlags(MFASF_MULTIPLEXER_AUTOADJUST_BITRATE);
    if (FAILED(hr))
    {
        goto done;
    }

    *ppMultiplexer = pMultiplexer;
    (*ppMultiplexer)->AddRef();

done:
    SafeRelease(&pMultiplexer);
    return hr;
}
```



## <a name="7-generate-new-asf-data-packets"></a>7. gerar novos pacotes de dados ASF

Em seguida, gere pacotes de dados ASF para o novo arquivo. Esses pacotes de dados constituem o objeto de dados ASF final para o novo arquivo. Para gerar novos pacotes de dados ASF:

1.  Chame [**MFCreateTempFile**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatetempfile) para criar um fluxo de bytes temporário para manter os pacotes de dados ASF.
2.  Chame a função definida pelo aplicativo `GetNextAudioSample` para obter dados de áudio não compactados para o codificador.
3.  Passe o áudio descompactado para o codificador para compactação. Para obter mais informações, consulte [processando dados no codificador](processing-data-in-the-encoder.md)
4.  Chame [**IMFASFMultiplexer::P rocesssample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) para enviar os exemplos de áudio compactados para o multiplexador de ASF para pacotes.
5.  Obtenha os pacotes ASF do Multiplexador e grave-os no fluxo de bytes temporário. Para obter mais informações, consulte [gerando novos pacotes de dados ASF](generating-new-asf-data-packets.md).
6.  Quando você chegar ao final do fluxo de origem, dissipe o codificador e extraia as amostras compactadas restantes do codificador. Para obter mais informações sobre como descarregar uma MFT, consulte [modelo básico de processamento de MFT](basic-mft-processing-model.md).
7.  Depois que todas as amostras forem enviadas ao Multiplexador, chame [**IMFASFMultiplexer:: flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-flush) e receba os pacotes ASF restantes do Multiplexador.
8.  Chame [**IMFASFMultiplexer:: End**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end).

O código a seguir gera pacotes de dados ASF. A função retorna um ponteiro para um fluxo de bytes que contém o objeto de dados ASF.


```C++
HRESULT EncodeData(
    CWmaEncoder* pEncoder, 
    IMFASFContentInfo* pContentInfo,
    IMFASFMultiplexer* pMux, 
    IMFByteStream** ppDataStream) 
{
    HRESULT hr = S_OK;

    IMFByteStream* pStream = NULL;
    IMFSample* pInputSample = NULL;
    IMFSample* pWmaSample = NULL;

    BOOL bEOF = FALSE;

   // Create a temporary file to hold the data stream.
   hr = MFCreateTempFile(
        MF_ACCESSMODE_READWRITE, 
        MF_OPENMODE_DELETE_IF_EXIST,
        MF_FILEFLAGS_NONE,
        &pStream
        );

   if (FAILED(hr))
   {
       goto done;
   }

    BOOL bNeedInput = TRUE;

    while (TRUE)
    {
        if (bNeedInput)
        {
            hr = GetNextAudioSample(&bEOF, &pInputSample);
            if (FAILED(hr))
            {
                goto done;
            }

            if (bEOF)
            {
                // Reached the end of the input file.
                break;
            }

            // Encode the uncompressed audio sample.
            hr = pEncoder->ProcessInput(pInputSample);
            if (FAILED(hr))
            {
                goto done;
            }

            bNeedInput = FALSE;
        }

        if (bNeedInput == FALSE)
        {
            // Get data from the encoder.

            hr = pEncoder->ProcessOutput(&pWmaSample);
            if (FAILED(hr))
            {
                goto done;
            }

            // pWmaSample can be NULL if the encoder needs more input.

            if (pWmaSample)
            {
                hr = pMux->ProcessSample(DEFAULT_STREAM_NUMBER, pWmaSample, 0);
                if (FAILED(hr))
                {
                    goto done;
                }

                //Collect the data packets and write them to a stream
                hr = GenerateASFDataPackets(pMux, pStream);
                if (FAILED(hr))
                {
                    goto done;
                }
            }
            else
            {
                bNeedInput = TRUE;
            }
        }
        
        SafeRelease(&pInputSample);
        SafeRelease(&pWmaSample);
    }

    // Drain the MFT and pull any remaining samples from the encoder.

    hr = pEncoder->Drain();
    if (FAILED(hr))
    {
        goto done;
    }

    while (TRUE)
    {
        hr = pEncoder->ProcessOutput(&pWmaSample);
        if (FAILED(hr))
        {
            goto done;
        }

        if (pWmaSample == NULL)
        {
            break;
        }

        hr = pMux->ProcessSample(DEFAULT_STREAM_NUMBER, pWmaSample, 0);
        if (FAILED(hr))
        {
            goto done;
        }

        //Collect the data packets and write them to a stream
        hr = GenerateASFDataPackets(pMux, pStream);
        if (FAILED(hr))
        {
            goto done;
        }

        SafeRelease(&pWmaSample);
    }

    // Flush the mux and get any pending ASF data packets.
    hr = pMux->Flush();
    if (FAILED(hr))
    {
        goto done;
    }

    hr = GenerateASFDataPackets(pMux, pStream);
    if (FAILED(hr))
    {
        goto done;
    }
    
    // Update the ContentInfo object
    hr = pMux->End(pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }

    //Return stream to the caller that contains the ASF encoded data.
    *ppDataStream = pStream;
    (*ppDataStream)->AddRef();

done:
    SafeRelease(&pStream);
    SafeRelease(&pInputSample);
    SafeRelease(&pWmaSample);
    return hr;
}
```



O código para a `GenerateASFDataPackets` função é mostrado no tópico [gerando novos pacotes de dados ASF](generating-new-asf-data-packets.md).

## <a name="8-write-the-asf-file"></a>8. gravar o arquivo ASF

Em seguida, grave o cabeçalho ASF em um buffer de mídia chamando [**IMFASFContentInfo:: GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader). Esse método converte os dados armazenados no objeto ContentInfo em dados binários no formato de objeto de cabeçalho ASF. Para obter mais informações, consulte [gerando um novo objeto de cabeçalho ASF](generating-a-new-asf-header-object.md).

Depois que o novo objeto de cabeçalho ASF tiver sido gerado, crie um fluxo de bytes para o arquivo de saída. Primeiro, grave o objeto de cabeçalho no fluxo de bytes de saída. Siga o objeto de cabeçalho com o objeto de dados contido no fluxo de bytes de dados.


```C++
HRESULT WriteASFFile( 
     IMFASFContentInfo *pContentInfo, 
     IMFByteStream *pDataStream,
     PCWSTR pszFile
     )
{
    HRESULT hr = S_OK;
    
    IMFMediaBuffer* pHeaderBuffer = NULL;
    IMFByteStream* pWmaStream = NULL;

    DWORD cbHeaderSize = 0;
    DWORD cbWritten = 0;

    //Create output file
    hr = MFCreateFile(MF_ACCESSMODE_WRITE, MF_OPENMODE_DELETE_IF_EXIST,
        MF_FILEFLAGS_NONE, pszFile, &pWmaStream);

    if (FAILED(hr))
    {
        goto done;
    }


    // Get the size of the ASF Header Object.
    hr = pContentInfo->GenerateHeader (NULL, &cbHeaderSize);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create a media buffer.
    hr = MFCreateMemoryBuffer(cbHeaderSize, &pHeaderBuffer);
    if (FAILED(hr))
    {
        goto done;
    }

    // Populate the media buffer with the ASF Header Object.
    hr = pContentInfo->GenerateHeader(pHeaderBuffer, &cbHeaderSize);
    if (FAILED(hr))
    {
        goto done;
    }

    // Write the ASF header to the output file.
    hr = WriteBufferToByteStream(pWmaStream, pHeaderBuffer, &cbWritten);
    if (FAILED(hr))
    {
        goto done;
    }

    // Append the data stream to the file.

    hr = pDataStream->SetCurrentPosition(0);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = AppendToByteStream(pDataStream, pWmaStream);

done:
    SafeRelease(&pHeaderBuffer);
    SafeRelease(&pWmaStream);
    return hr;
}
```



## <a name="9-define-the-entry-point-function"></a>9. definir a função de Entry-Point

Agora você pode colocar as etapas anteriores juntas em um aplicativo completo. Antes de usar qualquer um dos objetos Media Foundation, inicialize a plataforma Media Foundation chamando [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup). Quando terminar, chame [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown). Para obter mais informações, consulte [inicializando Media Foundation](initializing-media-foundation.md).

O código a seguir mostra o aplicativo de console completo. O argumento de linha de comando especifica o nome do arquivo a ser convertido e o nome do novo arquivo de áudio.


```C++
int wmain(int argc, WCHAR* argv[])
{
    HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);

    if (argc != 3)
    {
        wprintf_s(L"Usage: %s input.wmv, %s output.wma");
        return 0;
    }

    const WCHAR* sInputFileName = argv[1];    // Source file name
    const WCHAR* sOutputFileName = argv[2];  // Output file name
    
    IMFMediaType* pInputType = NULL;
    IMFASFContentInfo* pContentInfo = NULL;
    IMFASFMultiplexer* pMux = NULL;
    IMFByteStream* pDataStream = NULL;

    CWmaEncoder* pEncoder = NULL; //Pointer to the Encoder object.

    HRESULT hr = CoInitializeEx(
        NULL, COINIT_APARTMENTTHREADED | COINIT_DISABLE_OLE1DDE);

    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFStartup(MF_VERSION);
    if (FAILED(hr))
    {
        goto done;
    }

    CWmaEncoder* pEncoder = NULL; //Pointer to the Encoder object.

    hr = OpenAudioFile(sInputFileName, &pInputType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Initialize the WMA encoder wrapper.

    pEncoder = new (std::nothrow) CWmaEncoder();
    if (pEncoder == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    hr = pEncoder->Initialize();
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pEncoder->SetEncodingType(EncodeMode_CBR);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pEncoder->SetInputType(pInputType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the WMContainer objects.
    hr = CreateASFContentInfo(pEncoder, &pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = CreateASFMux(pContentInfo, &pMux);
    if (FAILED(hr))
    {
        goto done;
    }

    // Convert uncompressed data to ASF format.
    hr = EncodeData(pEncoder, pContentInfo, pMux, &pDataStream);
    if (FAILED(hr))
    {
        goto done;
    }

    // Write the ASF objects to the output file.
    hr = WriteASFFile(pContentInfo, pDataStream, sOutputFileName);

done:
    SafeRelease(&pInputType);
    SafeRelease(&pContentInfo);
    SafeRelease(&pMux);
    SafeRelease(&pDataStream);
    delete pEncoder;

    MFShutdown();
    CoUninitialize();

    if (FAILED(hr))
    {
        wprintf_s(L"Error: 0x%X\n", hr);
    }

    return 0;
} 
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Componentes ASF WMContainer](wmcontainer-asf-components.md)
</dt> <dt>

[Suporte a ASF no Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



