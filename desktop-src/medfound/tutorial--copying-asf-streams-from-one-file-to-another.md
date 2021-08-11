---
description: Uma maneira de criar um arquivo ASF é copiar fluxos ASF de um arquivo existente.
ms.assetid: 158fe3a1-42e6-461d-b56b-5419cd961fca
title: 'Tutorial: copiando Fluxos ASF usando objetos WMContainer'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2149358d216e044f3392b882a997ef4aa455ae799b6ece450bca11f0f22a6781
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118237870"
---
# <a name="tutorial-copying-asf-streams-by-using-wmcontainer-objects"></a>Tutorial: copiando Fluxos ASF usando objetos WMContainer

Uma maneira de criar um arquivo ASF é copiar fluxos ASF de um arquivo existente. Para fazer isso, você pode recuperar os dados de mídia do arquivo de origem e gravar no arquivo de saída. Se o arquivo de origem for um arquivo ASF, você poderá copiar amostras de fluxo sem descompactá-los e recompactá-los.

Este tutorial demonstra esse cenário extraindo o primeiro fluxo de áudio de um arquivo de vídeo de áudio ASF (. wmv) e copiando-o para um novo arquivo de áudio ASF (. WMA). Neste tutorial, você criará um aplicativo de console que usa os nomes de dados de entrada e saída como argumentos. O aplicativo usa o divisor de ASF para analisar os exemplos de fluxo de entrada e, em seguida, os envia para o multiplexador de ASF para gravar os pacotes de dados ASF para o fluxo de áudio.

Este tutorial contém as seguintes etapas:

-   [Pré-requisitos](#prerequisites)
-   [Terminologia](#terminology)
-   [1. configurar o Project](#1-set-up-the-project)
-   [2. declarar funções auxiliares](#2-declare-helper-functions)
-   [3. abrir o arquivo ASF de entrada](#3-open-the-input-asf-file)
-   [4. inicializar objetos para o arquivo de entrada](#4-initialize-objects-for-the-input-file)
-   [5. criar um perfil de áudio](#5-create-an-audio-profile)
-   [6. inicializar objetos para o arquivo de saída](#6-initialize-objects-for-the-output-file)
-   [7. gerar novos pacotes de dados ASF](#7-generate-new-asf-data-packets)
-   [8. gravar os objetos ASF no novo arquivo](#8-write-the-asf-objects-in-the-new-file)
-   [9 gravar a função Entry-Point](#9-write-the-entry-point-function)
-   [Tópicos relacionados](#related-topics)

## <a name="prerequisites"></a>Pré-requisitos

Este tutorial pressupõe o seguinte:

-   Você está familiarizado com a estrutura de um arquivo ASF e os componentes fornecidos pelo Media Foundation para trabalhar com objetos ASF. Esses componentes incluem ContentInfo, Splitter, multiplexador e objetos de perfil. Para obter mais informações, consulte [componentes ASF do WMContainer](wmcontainer-asf-components.md).
-   Você está familiarizado com o processo de análise do objeto de cabeçalho ASF e dos pacotes de dados ASF de um arquivo existente e geração de amostras de fluxo compactados usando o divisor. Para obter mais informações, consulte [tutorial: lendo um arquivo ASF](tutorial--reading-an-asf-file.md).
-   Você está familiarizado com buffers de mídia e fluxos de bytes: especificamente, operações de arquivo usando um fluxo de bytes e gravando o conteúdo de um buffer de mídia em um fluxo de bytes. (Consulte [2. Declarar funções auxiliares](#2-declare-helper-functions).)

## <a name="terminology"></a>Terminologia

Este tutorial usa os seguintes termos:

-   Fluxo de bytes de origem: o objeto de fluxo de bytes, expõe a interface [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) , que contém o conteúdo do arquivo de entrada.
-   Objeto ContentInfo de origem: objeto ContentInfo, expõe a interface [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) , que representa o objeto de cabeçalho ASF do arquivo de entrada.
-   Perfil de áudio: objeto de perfil, expõe a interface [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) , que contém somente fluxos de áudio do arquivo de entrada.
-   Exemplo de fluxo: a amostra de mídia, expõe a interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , gerada pelo separador representa os dados de mídia do fluxo selecionado obtidos do arquivo de entrada no estado compactado.
-   Objeto ContentInfo de saída: objeto ContentInfo, expõe a interface [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) , que representa o objeto de cabeçalho ASF do arquivo de saída.
-   Fluxo de bytes de dados: o objeto de fluxo de bytes, expõe a interface [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) , que representa a parte inteira do objeto de dados ASF do arquivo de saída.
-   Pacote de dados: a amostra de mídia, expõe a interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , gerada pelo multiplexador representa um pacote de dados ASF que será gravado no fluxo de bytes de dados.
-   Fluxo de bytes de saída: objeto de fluxo de bytes, expõe a interface [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) , que contém o conteúdo do arquivo de saída.

## <a name="1-set-up-the-project"></a>1. configurar o Project

Inclua os seguintes cabeçalhos no arquivo de origem:


```C++
#include <stdio.h>       // Standard I/O
#include <windows.h>     // Windows headers
#include <mfapi.h>       // Media Foundation platform
#include <wmcontainer.h> // ASF interfaces
#include <mferror.h>     // Media Foundation error codes
```



Link para os seguintes arquivos de biblioteca:

-   mfplat. lib
-   MF. lib
-   mfuuid. lib

Declare a função [SafeRelease](saferelease.md) :


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



## <a name="2-declare-helper-functions"></a>2. declarar funções auxiliares

Este tutorial usa as seguintes funções auxiliares para ler e gravar a partir de um fluxo de bytes.

A `AllocReadFromByteStream` função lê dados de um fluxo de bytes e aloca um novo buffer de mídia para manter os dados. Para obter mais informações, consulte [**IMFByteStream:: Read**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-read).


```C++
//-------------------------------------------------------------------
// AllocReadFromByteStream
//
// Reads data from a byte stream and returns a media buffer that
// contains the data.
//-------------------------------------------------------------------

HRESULT AllocReadFromByteStream(
    IMFByteStream *pStream,         // Pointer to the byte stream.
    DWORD cbToRead,                 // Number of bytes to read.
    IMFMediaBuffer **ppBuffer       // Receives a pointer to the media buffer. 
    )
{
    HRESULT hr = S_OK;
    BYTE *pData = NULL;
    DWORD cbRead = 0;   // Actual amount of data read.

    IMFMediaBuffer *pBuffer = NULL;

    // Create the media buffer. 
    // This function allocates the memory for the buffer.
    hr = MFCreateMemoryBuffer(cbToRead, &pBuffer);

    // Get a pointer to the memory buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->Lock(&pData, NULL, NULL);
    }

    // Read the data from the byte stream.
    if (SUCCEEDED(hr))
    {
        hr = pStream->Read(pData, cbToRead, &cbRead);
    }

    // Update the size of the valid data in the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->SetCurrentLength(cbRead);
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppBuffer = pBuffer;
        (*ppBuffer)->AddRef();
    }

    if (pData)
    {
        pBuffer->Unlock();
    }
    SafeRelease(&pBuffer);
    return hr;
}
```



A `WriteBufferToByteStream` função grava dados de um buffer de mídia em um fluxo de bytes. Para obter mais informações, consulte [**IMFByteStream:: Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write).


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



A `AppendToByteStream` função acrescenta o conteúdo de um fluxo de bytes para outro:


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



## <a name="3-open-the-input-asf-file"></a>3. abrir o arquivo ASF de entrada

Abra o arquivo de entrada chamando a função [**MFCreateFile**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatefile) . O método retorna um ponteiro para o objeto de fluxo de bytes que contém o conteúdo do arquivo. O nome de arquivo é especificado pelo usuário por meio de argumentos de linha de comando do aplicativo.

O código de exemplo a seguir usa um nome de arquivo e retorna um ponteiro para um objeto de fluxo de bytes que pode ser usado para ler o arquivo.


```C++
        // Open the file.
        hr = MFCreateFile(MF_ACCESSMODE_READ, MF_OPENMODE_FAIL_IF_NOT_EXIST, 
            MF_FILEFLAGS_NONE, pszFileName, &pStream);
```



## <a name="4-initialize-objects-for-the-input-file"></a>4. inicializar objetos para o arquivo de entrada

Em seguida, você criará e inicializará o objeto ContentInfo de origem e o divisor para gerar amostras de fluxo.

Esse fluxo de bytes de origem criado na etapa 2 será usado para analisar o objeto de cabeçalho ASF e preencher o objeto ContentInfo de origem. Esse objeto será usado para inicializar o divisor para facilitar a análise dos pacotes de dados ASF para o fluxo de áudio no arquivo de entrada. Você também irá recuperar o comprimento do objeto de dados ASF no arquivo de entrada e o deslocamento para o primeiro pacote de dados ASF relativo ao início do arquivo. Esses atributos serão usados pelo divisor para gerar amostras de fluxo de áudio.

Para criar e inicializar os componentes do ASF para o arquivo de entrada:

1.  Chame [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) para criar o objeto ContentInfo. Essa função retorna um ponteiro para a interface [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) .
2.  Chame [**IMFASFContentInfo::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) para analisar o cabeçalho ASF. Para obter mais informações sobre essa etapa, consulte [lendo o objeto de cabeçalho ASF de um arquivo existente](reading-the-asf-header-object-of-an-existing-file.md).
3.  Chame [**MFCreateASFSplitter**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) para criar o objeto divisor de ASF. Essa função retorna um ponteiro para a interface [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) .
4.  Chame [**IMFASFSplitter:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize), passando o ponteiro [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo). Para obter mais informações sobre esta etapa, consulte [Creating the ASF Splitter Object](creating-the-asf-splitter-object.md).
5.  Chame [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) para obter um descritor de apresentação para o arquivo asf.
6.  Obtenha o valor do atributo [**de \_ \_ deslocamento de \_ \_ início de \_ dados MF PD ASF**](mf-pd-asf-data-start-offset-attribute.md) do descritor de apresentação. Esse valor é o local do objeto de dados ASF no arquivo, como um deslocamento de bytes a partir do início do arquivo.
7.  Obtenha o valor do atributo [**de \_ \_ comprimento de \_ dados \_ MF PD ASF**](mf-pd-asf-data-length-attribute.md) do descritor de apresentação. Esse valor é o tamanho total do objeto de dados ASF, em bytes. Para obter mais informações, consulte [obtendo informações de objetos de cabeçalho ASF](getting-information-from-asf-header-objects.md).

O código de exemplo a seguir mostra uma função que consolida todas as etapas. Essa função usa um ponteiro para o fluxo de bytes de origem e retorna ponteiros para o objeto ContentInfo de origem e para o divisor. Além disso, ele recebe o comprimento e os deslocamentos para o objeto de dados ASF.


```C++
//-------------------------------------------------------------------
// CreateSourceParsers
//
// Creates the ASF splitter and the ASF Content Info object for the 
// source file.
// 
// This function also calulates the offset and length of the ASF 
// Data Object.
//-------------------------------------------------------------------

HRESULT CreateSourceParsers(
    IMFByteStream *pSourceStream,
    IMFASFContentInfo **ppSourceContentInfo,
    IMFASFSplitter **ppSplitter,
    UINT64 *pcbDataOffset,
    UINT64 *pcbDataLength
    )
{
    const DWORD MIN_ASF_HEADER_SIZE = 30;

    IMFMediaBuffer *pBuffer = NULL;
    IMFPresentationDescriptor *pPD = NULL;
    IMFASFContentInfo *pSourceContentInfo = NULL;
    IMFASFSplitter *pSplitter = NULL;

    QWORD cbHeader = 0;

    /*------- Parse the ASF header. -------*/

    // Create the ASF ContentInfo object.
    HRESULT hr = MFCreateASFContentInfo(&pSourceContentInfo);
    
    // Read the first 30 bytes to find the total header size.
    if (SUCCEEDED(hr))
    {
        hr = AllocReadFromByteStream(
            pSourceStream, 
            MIN_ASF_HEADER_SIZE, 
            &pBuffer
            );
    }

    // Get the header size.
    if (SUCCEEDED(hr))
    {
        hr = pSourceContentInfo->GetHeaderSize(pBuffer, &cbHeader);
    }

    // Release the buffer; we will reuse it.
    SafeRelease(&pBuffer);
    
    // Read the entire header into a buffer.
    if (SUCCEEDED(hr))
    {
        hr = pSourceStream->SetCurrentPosition(0);
    }

    if (SUCCEEDED(hr))
    {
        hr = AllocReadFromByteStream(
            pSourceStream, 
            (DWORD)cbHeader, 
            &pBuffer
            );
    }

    // Parse the buffer and populate the header object.
    if (SUCCEEDED(hr))
    {
        hr = pSourceContentInfo->ParseHeader(pBuffer, 0);
    }

    /*------- Initialize the ASF splitter. -------*/

    // Create the splitter.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateASFSplitter(&pSplitter);
    }
    
    // initialize the splitter with the ContentInfo object.
    if (SUCCEEDED(hr))
    {
        hr = pSplitter->Initialize(pSourceContentInfo);
    }


    /*------- Get the offset and size of the ASF Data Object. -------*/

    // Generate the presentation descriptor.
    if (SUCCEEDED(hr))
    {
        hr =  pSourceContentInfo->GeneratePresentationDescriptor(&pPD);
    }

    // Get the offset to the start of the Data Object.
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_ASF_DATA_START_OFFSET, pcbDataOffset);
    }

    // Get the length of the Data Object.
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_ASF_DATA_LENGTH, pcbDataLength);
    }

    // Return the pointers to the caller.
    if (SUCCEEDED(hr))
    {
        *ppSourceContentInfo = pSourceContentInfo;
        (*ppSourceContentInfo)->AddRef();

        *ppSplitter = pSplitter;
        (*ppSplitter)->AddRef();

    }

    SafeRelease(&pPD);
    SafeRelease(&pBuffer);
    SafeRelease(&pSourceContentInfo);
    SafeRelease(&pSplitter);

    return S_OK;
}
```



## <a name="5-create-an-audio-profile"></a>5. criar um perfil de áudio

Em seguida, você criará um objeto de perfil para o arquivo de entrada obtendo-o do objeto ContentInfo de origem. Em seguida, você irá configurar o perfil para que ele contenha apenas os fluxos de áudio do arquivo de entrada. Para fazer isso, enumere os fluxos e remova os fluxos de não áudio do perfil. O objeto de perfil de áudio será usado posteriormente neste tutorial para inicializar o objeto ContentInfo de saída.

Para criar um perfil de áudio

1.  Obtenha o objeto de perfil para o arquivo de entrada do objeto ContentInfo de origem chamando [**IMFASFContentInfo:: GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile). O método retorna um ponteiro para um objeto de perfil que contém todos os fluxos no arquivo de entrada. Para obter mais informações, consulte [criando um perfil de ASF](creating-an-asf-profile.md).
2.  Remova todos os objetos de exclusão mútua do perfil. Esta etapa é necessária porque os fluxos que não são de áudio serão removidos do perfil, o que pode invalidar os objetos de exclusão mútua.
3.  Remova todos os fluxos de não áudio do perfil, da seguinte maneira:
    -   Chame [**IMFASFProfile:: GetStreamCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount) para obter o número de fluxos.
    -   Em um loop, chame [**IMFASFProfile:: GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) para obter cada fluxo por índice.
    -   Chame [**IMFASFStreamConfig:: Getstreamtype**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getstreamtype) para obter o tipo de fluxo.
    -   Para fluxos sem áudio, chame [**IMFASFProfile:: RemoveStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream) para remover o fluxo.
4.  Armazene o número de fluxo do primeiro fluxo de áudio. Isso será selecionado no divisor para gerar amostras de fluxo. Se o número do fluxo for zero, o chamador poderá pressupor que não havia nenhum arquivo de fluxos de áudio.

O código a seguir segue estas etapas:


```C++
//-------------------------------------------------------------------
// GetAudioProfile
//
// Gets the ASF profile from the source file and removes any video
// streams from the profile.
//-------------------------------------------------------------------

HRESULT GetAudioProfile(
    IMFASFContentInfo *pSourceContentInfo, 
    IMFASFProfile **ppAudioProfile, 
    WORD *pwSelectStreamNumber
    )
{
    IMFASFStreamConfig *pStream = NULL;
    IMFASFProfile *pProfile = NULL;

    DWORD dwTotalStreams = 0;
    WORD  wStreamNumber = 0; 
    GUID guidMajorType = GUID_NULL;
    
    // Get the profile object from the source ContentInfo object.
    HRESULT hr = pSourceContentInfo->GetProfile(&pProfile);

    // Remove mutexes from the profile
    if (SUCCEEDED(hr))
    {
        hr = RemoveMutexes(pProfile);
    }

    // Get the total number of streams on the profile.
    if (SUCCEEDED(hr))
    {
        hr = pProfile->GetStreamCount(&dwTotalStreams);
    }

    // Enumerate the streams and remove the non-audio streams.
    if (SUCCEEDED(hr))
    {
        for (DWORD index = 0; index < dwTotalStreams; )
        {
            hr = pProfile->GetStream(index, &wStreamNumber, &pStream);

            if (FAILED(hr)) { break; }

            hr = pStream->GetStreamType(&guidMajorType);

            SafeRelease(&pStream);

            if (FAILED(hr)) { break; }

            if (guidMajorType != MFMediaType_Audio)
            {
                hr = pProfile->RemoveStream(wStreamNumber);
    
                if (FAILED(hr)) { break; }

                index = 0;
                dwTotalStreams--;
            }
            else
            {
                // Store the first audio stream number. 
                // This will be selected on the splitter.

                if (*pwSelectStreamNumber == 0)
                {
                    *pwSelectStreamNumber = wStreamNumber;
                }

                index++;
            }
        }
    }

    if (SUCCEEDED(hr))
    {
        *ppAudioProfile = pProfile;
        (*ppAudioProfile)->AddRef();
    }

    SafeRelease(&pStream);
    SafeRelease(&pProfile);

    return S_OK;
}
```



A `RemoveMutexes` função remove todos os objetos de exclusão mútua do perfil:


```C++
HRESULT RemoveMutexes(IMFASFProfile *pProfile)
{
    DWORD cMutex = 0;
    HRESULT hr = pProfile->GetMutualExclusionCount(&cMutex);

    if (SUCCEEDED(hr))
    {
        for (DWORD i = 0; i < cMutex; i++)
        {
            hr = pProfile->RemoveMutualExclusion(0);

            if (FAILED(hr))
            {
                break;
            }
        }
    }

    return hr;
}
```



## <a name="6-initialize-objects-for-the-output-file"></a>6. inicializar objetos para o arquivo de saída

Em seguida, você criará o objeto ContentInfo de saída e o multiplexador para gerar pacotes de dados para o arquivo de saída.

O perfil de áudio criado na etapa 4 será usado para preencher o objeto ContentInfo de saída. Esse objeto contém informações como atributos de arquivo global e propriedades de fluxo. O objeto ContentInfo de saída será usado para inicializar o multiplexador que irá gerar pacotes de dados para o arquivo de saída. Depois que os pacotes de dados são gerados, o objeto ContentInfo deve ser atualizado para refletir os novos valores.

Para criar e inicializar componentes do ASF para o arquivo de saída

1.  Crie um objeto ContentInfo vazio chamando [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) e popule-o com informações do perfil de áudio criado na etapa 3 chamando [**IMFASFContentInfo:: setprofile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile). Para obter mais informações, consulte [inicializando o objeto ContentInfo de um novo arquivo ASF](initializing-the-contentinfo-object-of-a-new-asf-file.md).
2.  Crie e inicialize o objeto multiplexador usando o objeto ContentInfo de saída. Para obter mais informações, consulte [criando o objeto multiplexador](creating-the-multiplexer-object.md).

O código de exemplo a seguir mostra uma função que consolida as etapas. Essa função usa um ponteiro para um objeto de perfil e retorna ponteiros para o objeto ContentInfo de saída e o multiplexador.


```C++
//-------------------------------------------------------------------
// CreateOutputGenerators
//
// Creates the ASF mux and the ASF Content Info object for the 
// output file.
//-------------------------------------------------------------------

HRESULT CreateOutputGenerators(
    IMFASFProfile *pProfile, 
    IMFASFContentInfo **ppContentInfo, 
    IMFASFMultiplexer **ppMux
    )
{
    IMFASFContentInfo *pContentInfo = NULL;
    IMFASFMultiplexer *pMux = NULL;

    // Use the ASF profile to create the ContentInfo object.
    HRESULT hr = MFCreateASFContentInfo(&pContentInfo);

    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->SetProfile(pProfile);
    }

    // Create the ASF Multiplexer object.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateASFMultiplexer(&pMux);
    }
    
    // Initialize it using the new ContentInfo object.
    if (SUCCEEDED(hr))
    {
        hr = pMux->Initialize(pContentInfo);
    }

    // Return the pointers to the caller.
    if (SUCCEEDED(hr))
    {
        *ppContentInfo = pContentInfo;
        (*ppContentInfo)->AddRef();

        *ppMux = pMux;
        (*ppMux)->AddRef();
    }

    SafeRelease(&pContentInfo);
    SafeRelease(&pMux);

    return hr;
}
```



## <a name="7-generate-new-asf-data-packets"></a>7. gerar novos pacotes de dados ASF

Em seguida, você vai gerar amostras de fluxo de áudio do fluxo de bytes de origem usando o divisor e enviá-los ao multiplexador para criar pacotes de dados ASF. Esses pacotes de dados constituem o objeto de dados ASF final para o novo arquivo.

Para gerar amostras de fluxo de áudio

1.  Selecione o primeiro fluxo de áudio no divisor chamando [**IMFASFSplitter:: SelectStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams).
2.  Ler blocos de tamanho fixo de dados de mídia do fluxo de bytes de origem em um buffer de mídia.
3.  Colete os exemplos de fluxo como amostras de mídia do divisor chamando [**IMFASFSplitter:: GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) em um loop, contanto que ele receba o \_ sinalizador ASF STATUSFLAGS \_ incompleto no parâmetro *pdwStatusFlags* . Para obter mais informações, consulte Gerando amostras para pacotes de dados ASF "em [gerando amostras de fluxo de um objeto de dados ASF existente](generating-stream-samples-from-an-existing-asf-data-object.md).
4.  Para cada exemplo de mídia, chame [**IMFASFMultiplexer::P rocesssample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) para enviar o exemplo de mídia para o multiplexador. O multiplexador gera os pacotes de dados para o objeto de dados ASF.
5.  Grave o pacote de dados gerado pelo multiplexador no fluxo de bytes de dados.
6.  Depois que todos os pacotes de dados tiverem sido gerados, chame [**IMFASFMultiplexer:: End**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end) para atualizar o objeto ContentInfo de saída com informações coletadas durante a geração de pacotes de dados ASF.

O código de exemplo a seguir gera amostras de fluxo do divisor de ASF e os envia para o multiplexador. O multiplexador gera pacotes de dados ASF e os grava em um fluxo.


```C++
//-------------------------------------------------------------------
// GenerateASFDataObject
// 
// Creates a byte stream that contains the ASF Data Object for the
// output file.
//-------------------------------------------------------------------

HRESULT GenerateASFDataObject(
    IMFByteStream *pSourceStream, 
    IMFASFSplitter *pSplitter, 
    IMFASFMultiplexer *pMux, 
    UINT64   cbDataOffset,
    UINT64   cbDataLength,
    IMFByteStream **ppDataStream
    )
{
    IMFMediaBuffer *pBuffer = NULL;
    IMFByteStream *pDataStream = NULL;
    
    const DWORD READ_SIZE = 1024 * 4;

    // Flush the splitter to remove any pending samples.
    HRESULT hr = pSplitter->Flush();

    if (SUCCEEDED(hr))
    {
        hr = MFCreateTempFile(
            MF_ACCESSMODE_READWRITE, 
            MF_OPENMODE_DELETE_IF_EXIST,
            MF_FILEFLAGS_NONE,
            &pDataStream
            );
    }

    if (SUCCEEDED(hr))
    {
        hr = pSourceStream->SetCurrentPosition(cbDataOffset);
    }

    if (SUCCEEDED(hr))
    {
        while (cbDataLength > 0)
        {
            DWORD cbRead = min(READ_SIZE, (DWORD)cbDataLength);

            hr = AllocReadFromByteStream(
                pSourceStream, 
                cbRead, 
                &pBuffer
                );

            if (FAILED(hr)) 
            { 
                break; 
            }

            cbDataLength -= cbRead;

            // Push data on the splitter.
            hr =  pSplitter->ParseData(pBuffer, 0, 0);

            if (FAILED(hr)) 
            { 
                break; 
            }

            // Get ASF packets from the splitter and feed them to the mux.
            hr = GetPacketsFromSplitter(pSplitter, pMux, pDataStream);

            if (FAILED(hr)) 
            { 
                break; 
            }

            SafeRelease(&pBuffer);
        }
    }

    // Flush the mux and generate any remaining samples.
    if (SUCCEEDED(hr))
    {
        hr = pMux->Flush();
    }

    if (SUCCEEDED(hr))
    {
        hr = GenerateASFDataPackets(pMux, pDataStream);
    }

     // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppDataStream = pDataStream;
        (*ppDataStream)->AddRef();
    }

    SafeRelease(&pBuffer);
    SafeRelease(&pDataStream);
    return hr;
}
```



Para obter pacotes do divisor de ASF, o código anterior chama a `GetPacketsFromSplitter` função, mostrada aqui:


```C++
//-------------------------------------------------------------------
// GetPacketsFromSplitter
//
// Gets samples from the ASF splitter.
//
// This function is called after calling IMFASFSplitter::ParseData.
//-------------------------------------------------------------------

HRESULT GetPacketsFromSplitter(
    IMFASFSplitter *pSplitter,
    IMFASFMultiplexer *pMux,
    IMFByteStream *pDataStream
    )
{
    HRESULT hr = S_OK;
    DWORD   dwStatus = ASF_STATUSFLAGS_INCOMPLETE;
    WORD    wStreamNum = 0;

    IMFSample *pSample = NULL;

    while (dwStatus & ASF_STATUSFLAGS_INCOMPLETE) 
    {
        hr = pSplitter->GetNextSample(&dwStatus, &wStreamNum, &pSample);

        if (FAILED(hr))
        {
            break;
        }

        if (pSample)
        {
            //Send to the multiplexer to convert it into ASF format
            hr = pMux->ProcessSample(wStreamNum, pSample, 0);

            if (FAILED(hr)) 
            { 
                break; 
            }

            hr = GenerateASFDataPackets(pMux, pDataStream);

            if (FAILED(hr)) 
            { 
                break; 
            }
        }

        SafeRelease(&pSample);
    }

    SafeRelease(&pSample);
    return hr;
}
```



A `GenerateDataPackets` função obtém pacotes de dados do Multiplexador. Para obter mais informações, consulte [obtendo pacotes de dados ASF](generating-new-asf-data-packets.md).


```C++
//-------------------------------------------------------------------
// GenerateASFDataPackets
// 
// Gets data packets from the mux. This function is called after 
// calling IMFASFMultiplexer::ProcessSample. 
//-------------------------------------------------------------------

HRESULT GenerateASFDataPackets( 
    IMFASFMultiplexer *pMux, 
    IMFByteStream *pDataStream
    )
{
    HRESULT hr = S_OK;

    IMFSample *pOutputSample = NULL;
    IMFMediaBuffer *pDataPacketBuffer = NULL;

    DWORD dwMuxStatus = ASF_STATUSFLAGS_INCOMPLETE;

    while (dwMuxStatus & ASF_STATUSFLAGS_INCOMPLETE)
    {
        hr = pMux->GetNextPacket(&dwMuxStatus, &pOutputSample);

        if (FAILED(hr))
        {
            break;
        }

        if (pOutputSample)
        {
            //Convert to contiguous buffer
            hr = pOutputSample->ConvertToContiguousBuffer(&pDataPacketBuffer);
            
            if (FAILED(hr))
            {
                break;
            }

            //Write buffer to byte stream
            hr = WriteBufferToByteStream(pDataStream, pDataPacketBuffer, NULL);

            if (FAILED(hr))
            {
                break;
            }
        }

        SafeRelease(&pDataPacketBuffer);
        SafeRelease(&pOutputSample);
    }

    SafeRelease(&pOutputSample);
    SafeRelease(&pDataPacketBuffer);
    return hr;
}
```



## <a name="8-write-the-asf-objects-in-the-new-file"></a>8. gravar os objetos ASF no novo arquivo

Em seguida, você gravará o conteúdo do objeto ContentInfo de saída em um buffer de mídia chamando [**IMFASFContentInfo:: GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader). Esse método converte os dados armazenados no objeto ContentInfo em dados binários no formato de objeto de cabeçalho ASF. Para obter mais informações, consulte [gerando um novo objeto de cabeçalho ASF](generating-a-new-asf-header-object.md).

Depois que o novo objeto de cabeçalho ASF tiver sido gerado, grave o arquivo de saída gravando primeiro o objeto de cabeçalho no fluxo de bytes de saída criado na etapa 2 chamando a função auxiliar WriteBufferToByteStream. Siga o objeto de cabeçalho com o objeto de dados contido no fluxo de bytes de dados. O código de exemplo mostra uma função que transfere o conteúdo do fluxo de bytes de dados para o fluxo de bytes de saída.


```C++
//-------------------------------------------------------------------
// WriteASFFile
//
// Writes the complete ASF file.
//-------------------------------------------------------------------

HRESULT WriteASFFile( 
    IMFASFContentInfo *pContentInfo, // ASF Content Info for the output file.
    IMFByteStream *pDataStream,      // Data stream.
    PCWSTR pszFile                   // Output file name.
    )
{
    
    IMFMediaBuffer *pHeaderBuffer = NULL;
    IMFByteStream *pWmaStream = NULL;

    DWORD cbHeaderSize = 0;
    DWORD cbWritten = 0;

    // Create output file.
    HRESULT hr = MFCreateFile(
        MF_ACCESSMODE_WRITE, 
        MF_OPENMODE_DELETE_IF_EXIST,
        MF_FILEFLAGS_NONE,
        pszFile,
        &pWmaStream
        );

    // Get the size of the ASF Header Object.
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->GenerateHeader(NULL, &cbHeaderSize);
    }

    // Create a media buffer.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateMemoryBuffer(cbHeaderSize, &pHeaderBuffer);
    }

    // Populate the media buffer with the ASF Header Object.
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->GenerateHeader(pHeaderBuffer, &cbHeaderSize);
    }
 
    // Write the header contents to the byte stream for the output file.
    if (SUCCEEDED(hr))
    {
        hr = WriteBufferToByteStream(pWmaStream, pHeaderBuffer, &cbWritten);
    }

    if (SUCCEEDED(hr))
    {
        hr = pDataStream->SetCurrentPosition(0);
    }

    // Append the data stream to the file.

    if (SUCCEEDED(hr))
    {
        hr = AppendToByteStream(pDataStream, pWmaStream);
    }

    SafeRelease(&pHeaderBuffer);
    SafeRelease(&pWmaStream);

    return hr;
}
```



## <a name="9-write-the-entry-point-function"></a>9 gravar a função Entry-Point

Agora você pode colocar as etapas anteriores juntas em um aplicativo completo. Antes de usar qualquer um dos objetos Media Foundation, inicialize a plataforma Media Foundation chamando [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup). Quando terminar, chame [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown). Para obter mais informações, consulte [inicializando Media Foundation](initializing-media-foundation.md).

O código a seguir mostra o aplicativo de console completo. O argumento de linha de comando especifica o nome do arquivo a ser convertido e o nome do novo arquivo de áudio.


```C++
int wmain(int argc, WCHAR* argv[])
{
    if (argc != 3)
    {
        wprintf_s(L"Usage: %s input.wmv, %s output.wma\n");
        return 0;
    }

    HRESULT hr = MFStartup(MF_VERSION);

    if (FAILED(hr))
    {
        wprintf_s(L"MFStartup failed: 0x%X\n", hr);
        return 0;
    }

    PCWSTR pszInputFile = argv[1];      
    PCWSTR pszOutputFile = argv[2];     
    
    IMFByteStream      *pSourceStream = NULL;       
    IMFASFContentInfo  *pSourceContentInfo = NULL;  
    IMFASFProfile      *pAudioProfile = NULL;       
    IMFASFContentInfo  *pOutputContentInfo = NULL;  
    IMFByteStream      *pDataStream = NULL;         
    IMFASFSplitter     *pSplitter = NULL;           
    IMFASFMultiplexer  *pMux = NULL;                

    UINT64  cbDataOffset = 0;           
    UINT64  cbDataLength = 0;           
    WORD    wSelectStreamNumber = 0;    

    // Open the input file.

    hr = OpenFile(pszInputFile, &pSourceStream);

    // Initialize the objects that will parse the source file.

    if (SUCCEEDED(hr))
    {
        hr = CreateSourceParsers(
            pSourceStream, 
            &pSourceContentInfo,    // ASF Header for the source file.
            &pSplitter,             // Generates audio samples.
            &cbDataOffset,          // Offset to the first data packet.
            &cbDataLength           // Length of the ASF Data Object.
            );
    }

    // Create a profile object for the audio streams in the source file.

    if (SUCCEEDED(hr))
    {
        hr = GetAudioProfile(
            pSourceContentInfo, 
            &pAudioProfile,         // ASF profile for the audio stream.
            &wSelectStreamNumber    // Stream number of the first audio stream.
            );
    }

    // Initialize the objects that will generate the output data.

    if (SUCCEEDED(hr))
    {
        hr = CreateOutputGenerators(
            pAudioProfile, 
            &pOutputContentInfo,    // ASF Header for the output file.
            &pMux                   // Generates ASF data packets.
            );
    }

    // Set up the splitter to generate samples for the first
    // audio stream in the source media.

    if (SUCCEEDED(hr))
    {
        hr = pSplitter->SelectStreams(&wSelectStreamNumber, 1);
    }
    
    // Generate ASF Data Packets and store them in a byte stream.

    if (SUCCEEDED(hr))
    {
        hr = GenerateASFDataObject(
               pSourceStream, 
               pSplitter, 
               pMux, 
               cbDataOffset, 
               cbDataLength, 
               &pDataStream    // Byte stream for the ASF data packets.    
               );
    }

    // Update the header with new information if any.

    if (SUCCEEDED(hr))
    {
        hr = pMux->End(pOutputContentInfo);
    }

    //Write the ASF objects to the output file
    if (SUCCEEDED(hr))
    {
        hr = WriteASFFile(pOutputContentInfo, pDataStream, pszOutputFile);
    }

    // Clean up.
    SafeRelease(&pMux);
    SafeRelease(&pSplitter);
    SafeRelease(&pDataStream);
    SafeRelease(&pOutputContentInfo);
    SafeRelease(&pAudioProfile);
    SafeRelease(&pSourceContentInfo);
    SafeRelease(&pSourceStream);

    MFShutdown();

    if (FAILED(hr))
    {
        wprintf_s(L"Could not create the audio file: 0x%X\n", hr);
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

 

 



