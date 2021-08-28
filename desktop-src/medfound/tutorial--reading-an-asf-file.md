---
description: Este tutorial mostra como obter pacotes de dados de um arquivo ASF (Advanced Systems Format) usando o divisor de ASF.
ms.assetid: e3a55275-e8f0-4ab7-98db-a2f2c54d5a51
title: 'Tutorial: lendo um arquivo ASF usando objetos WMContainer'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e456f9e0061be97198623c2422801b5fd9fc196874cd8aa1a467692277319c9e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713286"
---
# <a name="tutorial-reading-an-asf-file-by-using-wmcontainer-objects"></a>Tutorial: lendo um arquivo ASF usando objetos WMContainer

Este tutorial mostra como obter pacotes de dados de um arquivo ASF (Advanced Systems Format) usando o [divisor de ASF](asf-splitter.md). Neste tutorial, você criará um aplicativo de console simples que lê um arquivo ASF e gera amostras de mídia compactadas para o primeiro fluxo de vídeo no arquivo. O aplicativo exibe informações sobre os quadros-chave no fluxo de vídeo.

Este tutorial contém as seguintes etapas:

-   [Pré-requisitos](#prerequisites)
-   [1. configurar o Project](#1-set-up-the-project)
-   [2. abrir um arquivo ASF](#2-open-an-asf-file)
-   [3. ler o objeto de cabeçalho ASF](#3-read-the-asf-header-object)
-   [4. criar o divisor de ASF](#4-create-the-asf-splitter)
-   [5. selecionar um fluxo para análise](#5-select-a-stream-for-parsing)
-   [6. gerar amostras de mídia compactadas](#6-generate-compressed-media-samples)
-   [7. gravar a função Entry-Point](#7-write-the-entry-point-function)
-   [Listagem de programas](#program-listing)
-   [Tópicos relacionados](#related-topics)

O tutorial não aborda como decodificar os dados compactados que o aplicativo obtém do divisor de ASF.

## <a name="prerequisites"></a>Pré-requisitos

Este tutorial pressupõe o seguinte:

-   Você está familiarizado com a estrutura de um arquivo ASF e os componentes fornecidos pelo Media Foundation para trabalhar com objetos ASF. Esses componentes incluem o objeto ContentInfo, o Splitter, o multiplexador e o perfil. Para obter mais informações, consulte [componentes ASF do WMContainer](wmcontainer-asf-components.md).
-   Você está familiarizado com [buffers de mídia](media-buffers.md) e fluxos de bytes: especificamente, operações de arquivo usando um fluxo de bytes, lendo de um fluxo de bytes em um buffer de mídia e gravando o conteúdo de um buffer de mídia em um fluxo de bytes.

## <a name="1-set-up-the-project"></a>1. configurar o Project

Inclua os seguintes cabeçalhos no arquivo de origem:


```C++
#include <stdio.h>       // Standard I/O
#include <windows.h>     // Windows headers
#include <mfapi.h>       // Media Foundation platform
#include <wmcontainer.h> // ASF interfaces
#include <Mferror.h>
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



## <a name="2-open-an-asf-file"></a>2. abrir um arquivo ASF

Em seguida, abra o arquivo especificado chamando a função [**MFCreateFile**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatefile) . O método retorna um ponteiro para o objeto de fluxo de bytes que contém o conteúdo do arquivo. O nome de arquivo é especificado pelo usuário por meio de argumentos de linha de comando do aplicativo.

O código de exemplo a seguir usa um nome de arquivo e retorna um ponteiro para um objeto de fluxo de bytes que pode ser usado para ler o arquivo.


```C++
        // Open the file.
        hr = MFCreateFile(MF_ACCESSMODE_READ, MF_OPENMODE_FAIL_IF_NOT_EXIST, 
            MF_FILEFLAGS_NONE, pszFileName, &pStream);
```



## <a name="3-read-the-asf-header-object"></a>3. ler o objeto de cabeçalho ASF

Em seguida, crie o [objeto ContentInfo do ASF](asf-contentinfo-object.md) e use-o para analisar o objeto de cabeçalho ASF do arquivo especificado. O objeto ContentInfo armazena informações do cabeçalho ASF, incluindo atributos de arquivo global e informações sobre cada fluxo. Você usará o objeto ContentInfo posteriormente no tutorial para inicializar o divisor de ASF e obter o número de fluxo do fluxo de vídeo.

Para criar o objeto ContentInfo do ASF:

1.  Chame a função [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) para criar um objeto ContentInfo. O método retorna um ponteiro para a interface [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) .
2.  Leia os primeiros 30 bytes de dados do arquivo ASF em um buffer de mídia.
3.  Passe o buffer de mídia para o método [**IMFASFContentInfo:: Getheadize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) . Esse método retorna o tamanho total do objeto de cabeçalho no arquivo ASF.
4.  Passe o mesmo buffer de mídia para o método [**IMFASFContentInfo::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) .
5.  Leia o restante do objeto de cabeçalho em um novo buffer de mídia.
6.  Passe o segundo buffer para o método [**ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) . Especifique o deslocamento de 30 bytes no parâmetro *cbOffsetWithinHeader* de **ParseHeader**. O método **ParseHeader** Inicializa o objeto ContentInfo com informações coletadas dos vários objetos ASF contidos no objeto header.


```C++
// Read the ASF Header Object from a byte stream and return a pointer to the 
// populated ASF ContentInfo object.
//
// The current read position of the byte stream must be at the start of the
// ASF Header Object.

HRESULT CreateContentInfo(IMFByteStream *pStream, 
    IMFASFContentInfo **ppContentInfo)
{
    const DWORD MIN_ASF_HEADER_SIZE = 30;
    
    QWORD cbHeader = 0;
    DWORD cbBuffer = 0;

    IMFASFContentInfo *pContentInfo = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    // Create the ASF ContentInfo object.
    HRESULT hr = MFCreateASFContentInfo(&pContentInfo);
    
    // Read the first 30 bytes to find the total header size.

    if (SUCCEEDED(hr))
    {
        hr = MFCreateMemoryBuffer(MIN_ASF_HEADER_SIZE, &pBuffer);
    }
    if (SUCCEEDED(hr))
    {
        hr = ReadFromByteStream(pStream, pBuffer,MIN_ASF_HEADER_SIZE);
    }
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->GetHeaderSize(pBuffer, &cbHeader);
    }

    // Pass the first 30 bytes to the ContentInfo object.
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->ParseHeader(pBuffer, 0);
    }

    SafeRelease(&pBuffer);

    if (SUCCEEDED(hr))
    {
        cbBuffer = (DWORD)(cbHeader - MIN_ASF_HEADER_SIZE);

        hr = MFCreateMemoryBuffer(cbBuffer, &pBuffer);
    }

    // Read the rest of the header and finish parsing the header.
    if (SUCCEEDED(hr))
    {
        hr = ReadFromByteStream(pStream, pBuffer, cbBuffer);
    }
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->ParseHeader(pBuffer, MIN_ASF_HEADER_SIZE);
    }
    if (SUCCEEDED(hr))
    {
        // Return the pointer to the caller.
        *ppContentInfo = pContentInfo;
        (*ppContentInfo)->AddRef();
    }
    SafeRelease(&pBuffer);
    SafeRelease(&pContentInfo);
    return hr;
} 
```



Essa função usa a `ReadFromByteStream` função para ler de um fluxo de bytes em um buffer de mídia:


```C++
// Read data from a byte stream into a media buffer.
//
// This function reads a maximum of cbMax bytes, or up to the size size of the 
// buffer, whichever is smaller. If the end of the byte stream is reached, the 
// actual amount of data read might be less than either of these values.
//
// To find out how much data was read, call IMFMediaBuffer::GetCurrentLength.

HRESULT ReadFromByteStream(
    IMFByteStream *pStream,     // Pointer to the byte stream.
    IMFMediaBuffer *pBuffer,    // Pointer to the media buffer.
    DWORD cbMax                 // Maximum amount to read.
    )
{
    DWORD cbBufferMax = 0;
    DWORD cbRead = 0;
    BYTE *pData= NULL;

    HRESULT hr = pBuffer->Lock(&pData, &cbBufferMax, NULL);

    // Do not exceed the maximum size of the buffer.
    if (SUCCEEDED(hr))
    {
        if (cbMax > cbBufferMax)
        {
            cbMax = cbBufferMax;
        }

        // Read up to cbMax bytes.
        hr = pStream->Read(pData, cbMax, &cbRead);
    }

    // Update the size of the valid data in the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->SetCurrentLength(cbRead);
    }
    if (pData)
    {
        pBuffer->Unlock();
    }
    return hr;
}
```



## <a name="4-create-the-asf-splitter"></a>4. criar o divisor de ASF

Em seguida, crie o objeto [divisor de ASF](asf-splitter.md) . Você usará o divisor de ASF para analisar o objeto de dados ASF, que contém dados de mídia em pacotes para o arquivo ASF.

Para criar um objeto divisor para o arquivo ASF:

1.  Chame a função [**MFCreateASFSplitter**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) para criar o divisor de ASF. A função retorna um ponteiro para a interface [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) .
2.  Chame [**IMFASFSplitter:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) para inicializar o divisor de ASF. Esse método usa um ponteiro para o objeto ContentInfo, que foi criado no procedimento 3.


```C++
// Create and initialize the ASF splitter.

HRESULT CreateASFSplitter (IMFASFContentInfo* pContentInfo, 
    IMFASFSplitter** ppSplitter)
{
    IMFASFSplitter *pSplitter = NULL;

    // Create the splitter object.
    HRESULT hr = MFCreateASFSplitter(&pSplitter);

    // Initialize the splitter to work with specific ASF data.
    if (SUCCEEDED(hr))
    {
        hr = pSplitter->Initialize(pContentInfo);
    }
    if (SUCCEEDED(hr))
    {
        // Return the object to the caller.
        *ppSplitter = pSplitter;
        (*ppSplitter)->AddRef();
    }
    SafeRelease(&pSplitter);
    return hr;
}
```



## <a name="5-select-a-stream-for-parsing"></a>5. selecionar um fluxo para análise

Em seguida, enumere os fluxos no arquivo ASF e selecione o primeiro fluxo de vídeo para análise. Para enumerar os fluxos, você usará um objeto de perfil ASF e pesquisará os fluxos que têm um tipo de mídia de vídeo.

Para selecionar o fluxo de vídeo:

1.  Chame [**IMFASFContentInfo:: GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile) no objeto ContentInfo para criar um perfil de ASF. Entre outras informações, o perfil descreve os fluxos no arquivo ASF.
2.  Chame [**IMFASFProfile:: GetStreamCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount) para obter o número de fluxos no arquivo asf.
3.  Chame [**IMFASFProfile:: GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) em um loop para enumerar os fluxos. O método retorna um ponteiro para a interface [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) . Ele também retorna o identificador de fluxo.
4.  Chame [**IMFASFStreamConfig:: Getstreamtype**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getstreamtype) para obter o GUID de tipo principal para o fluxo. Se o GUID de tipo principal for MFMediaType \_ Video, o fluxo conterá vídeo.
5.  Se você encontrar um fluxo de vídeo na etapa 4, chame [**IMFASFSplitter:: SelectStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams) para selecionar o fluxo. Esse método usa uma matriz de identificadores de fluxo. Para este tutorial, o tamanho da matriz é 1 porque o aplicativo analisará um único fluxo.

O código de exemplo a seguir enumera os fluxos no arquivo ASF e seleciona o primeiro fluxo de vídeo no divisor de ASF:


```C++
// Select the first video stream for parsing with the ASF splitter.

HRESULT SelectVideoStream(IMFASFContentInfo *pContentInfo, 
    IMFASFSplitter *pSplitter, BOOL *pbHasVideo)
{
    DWORD   cStreams = 0;
    WORD    wStreamID = 0;

    IMFASFProfile *pProfile = NULL;
    IMFASFStreamConfig *pStream = NULL;

    // Get the ASF profile from the ContentInfo object.
    HRESULT hr = pContentInfo->GetProfile(&pProfile);

    // Loop through all of the streams in the profile.
    if (SUCCEEDED(hr))
    {
        hr = pProfile->GetStreamCount(&cStreams);
    }

    if (SUCCEEDED(hr))
    {
        for (DWORD i = 0; i < cStreams; i++)
        {
            GUID    streamType = GUID_NULL;

            // Get the stream type and stream identifier.
            hr = pProfile->GetStream(i, &wStreamID, &pStream);
            if (FAILED(hr)) 
            {
                break;
            }

            hr = pStream->GetStreamType(&streamType);
            if (FAILED(hr)) 
            {
                break;
            }

            if (streamType == MFMediaType_Video)
            {
                *pbHasVideo = TRUE;
                break;
            }
            SafeRelease(&pStream);
        }
    }

    // Select the video stream, if found.
    if (SUCCEEDED(hr))
    {
        if (*pbHasVideo)
        {
            // SelectStreams takes an array of stream identifiers.
            hr = pSplitter->SelectStreams(&wStreamID, 1);
        }
    }
    SafeRelease(&pStream);
    SafeRelease(&pProfile);
    return hr;
}
```



## <a name="6-generate-compressed-media-samples"></a>6. gerar amostras de mídia compactadas

Em seguida, use o divisor de ASF para analisar o objeto de dados ASF e obter os pacotes de dados para o fluxo de vídeo selecionado. O aplicativo lê os dados do arquivo ASF em blocos de tamanho fixo e passa os dados para o divisor de ASF. O divisor analisa os dados e gera amostras de [mídia](media-samples.md) que contêm os dados de vídeo compactados. O aplicativo verifica se cada amostra representa um quadro-chave. Nesse caso, o aplicativo exibe algumas informações básicas sobre o exemplo:

-   Número de buffers de mídia
-   Tamanho total dos dados
-   Carimbo de data/hora

Para gerar amostras de mídia compactadas:

1.  Aloque um novo buffer de mídia.
2.  Ler dados do fluxo de bytes no buffer de mídia.
3.  Passe o buffer de mídia para o método [**IMFASFSplitter::P arsedata**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) . O método analisa os dados do ASF no buffer.
4.  Em um loop, obtenha amostras de mídia do divisor chamando [**IMFASFSplitter:: GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample). Se o parâmetro *ppISample* receber um ponteiro [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) válido, isso significará que o divisor de ASF analisou um ou mais pacotes de dados. Se *ppISample* receber o valor **NULL**, interrompa do loop e volte para a etapa 1.
5.  Exiba informações sobre o exemplo.
6.  Interromper do loop nas seguintes condições:
    -   O parâmetro *ppISample* recebe o valor **NULL**.
    -   O parâmetro *pdwStatusFlags* não recebe o sinalizador **ASF \_ STATUSFLAGS \_ incompleto** .

Repita essas etapas até chegar ao final do arquivo. O código a seguir mostra essas etapas:


```C++
// Parse the video stream and display information about the video samples.
//
// The current read position of the byte stream must be at the start of the ASF
// Data Object.

HRESULT DisplayKeyFrames(IMFByteStream *pStream, IMFASFSplitter *pSplitter)
{
    const DWORD cbReadSize = 2048;  // Read size (arbitrary value)

    IMFMediaBuffer *pBuffer = NULL;
    IMFSample *pSample = NULL;

    HRESULT hr = S_OK;
    while (SUCCEEDED(hr))
    {
        // The parser must get a newly allocated buffer each time.
        hr = MFCreateMemoryBuffer(cbReadSize, &pBuffer);
        if (FAILED(hr))
        {
            break;
        }

        // Read data into the buffer.
        hr = ReadFromByteStream(pStream, pBuffer, cbReadSize);
        if (FAILED(hr)) 
        {
            break; 
        }

        // Get the amound of data that was read.
        DWORD cbData;
        hr = pBuffer->GetCurrentLength(&cbData);
        if (FAILED(hr)) 
        { 
            break; 
        }

        if (cbData == 0)
        {
            break; // End of file.
        }

        // Send the data to the ASF splitter.
        hr = pSplitter->ParseData(pBuffer, 0, 0);
        SafeRelease(&pBuffer);
        if (FAILED(hr)) 
        { 
            break; 
        }

        // Pull samples from the splitter.
        DWORD parsingStatus = 0;
        do
        {
            WORD streamID;
            hr = pSplitter->GetNextSample(&parsingStatus, &streamID, &pSample);
            if (FAILED(hr)) 
            { 
                break; 
            }
            if (pSample == NULL)
            {
                // No samples yet. Parse more data.
                break;
            }
            if (IsRandomAccessPoint(pSample))
            {
                DisplayKeyFrame(pSample);
            }
            SafeRelease(&pSample);
            
        } while (parsingStatus & ASF_STATUSFLAGS_INCOMPLETE);
    }
    SafeRelease(&pSample);
    SafeRelease(&pBuffer);
    return hr;
}
```



A função iskeyframe testa se um exemplo é um quadro-chave, obtendo o valor do atributo [**MFSampleExtension \_ CleanPoint**](mfsampleextension-cleanpoint-attribute.md) .


```C++
inline BOOL IsRandomAccessPoint(IMFSample *pSample)
{
    // Check for the "clean point" attribute. Default to FALSE.
    return MFGetAttributeUINT32(pSample, MFSampleExtension_CleanPoint, FALSE);
}
```



Para fins de ilustração, este tutorial exibe algumas informações para cada quadro de chave de vídeo, chamando a seguinte função:


```C++
void DisplayKeyFrame(IMFSample *pSample)
{
    DWORD   cBuffers = 0;           // Buffer count
    DWORD   cbTotalLength = 0;      // Buffer length
    MFTIME  hnsTime = 0;            // Time stamp

    // Print various information about the key frame.
    if (SUCCEEDED(pSample->GetBufferCount(&cBuffers)))
    {
        wprintf_s(L"Buffer count: %d\n", cBuffers);
    }
    if (SUCCEEDED(pSample->GetTotalLength(&cbTotalLength)))
    {
        wprintf_s(L"Length: %d bytes\n", cbTotalLength);
    }
    if (SUCCEEDED(pSample->GetSampleTime(&hnsTime)))
    {
        // Convert the time stamp to seconds.
        double sec = static_cast<double>(hnsTime / 10000) / 1000;
        wprintf_s(L"Time stamp: %f sec.\n", sec);
    }
    wprintf_s(L"\n");
}
```



Um aplicativo típico usaria os pacotes de dados para decodificação, remuxing, envio pela rede ou alguma outra tarefa.

## <a name="7-write-the-entry-point-function"></a>7. gravar a função Entry-Point

Agora você pode colocar as etapas anteriores juntas em um aplicativo completo. Antes de usar qualquer um dos objetos Media Foundation, inicialize a plataforma Media Foundation chamando [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup). Quando terminar, chame [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown). Para obter mais informações, [inicializando Media Foundation](initializing-media-foundation.md).


```C++
int wmain(int argc, WCHAR* argv[])
{
    if (argc != 2)
    {
        _s(L"Usage: %s input.wmv");
        return 0;
    }

    // Start the Media Foundation platform.
    HRESULT hr = MFStartup(MF_VERSION);
    if (SUCCEEDED(hr))
    {
        PCWSTR pszFileName = argv[1]; 
        BOOL   bHasVideo = FALSE;

        IMFByteStream       *pStream = NULL;
        IMFASFContentInfo   *pContentInfo = NULL;
        IMFASFSplitter      *pSplitter = NULL;

        // Open the file.
        hr = MFCreateFile(MF_ACCESSMODE_READ, MF_OPENMODE_FAIL_IF_NOT_EXIST, 
            MF_FILEFLAGS_NONE, pszFileName, &pStream);

        // Read the ASF header.
        if (SUCCEEDED(hr))
        {
            hr = CreateContentInfo(pStream, &pContentInfo);
        }

        // Create the ASF splitter.
        if (SUCCEEDED(hr))
        {
            hr = CreateASFSplitter(pContentInfo, &pSplitter);
        }

        // Select the first video stream.
        if (SUCCEEDED(hr))
        {
            hr = SelectVideoStream(pContentInfo, pSplitter, &bHasVideo);
        }

        // Parse the ASF file.
        if (SUCCEEDED(hr))
        {
            if (bHasVideo)
            {
                hr = DisplayKeyFrames(pStream, pSplitter);
            }
            else
            {
                wprintf_s(L"No video stream.\n");
            }
        }
        SafeRelease(&pSplitter);
        SafeRelease(&pContentInfo);
        SafeRelease(&pStream);
    
        // Shut down the Media Foundation platform.
        MFShutdown();
    }
    if (FAILED(hr))
    {
        wprintf_s(L"Error: 0x%X\n", hr);
    }
    return 0;
}
```



## <a name="program-listing"></a>Listagem de programas

O código a seguir mostra a listagem completa para o tutorial.


```C++
#include <stdio.h>       // Standard I/O
#include <windows.h>     // Windows headers
#include <mfapi.h>       // Media Foundation platform
#include <wmcontainer.h> // ASF interfaces
#include <Mferror.h>

#pragma comment(lib, "mfplat")
#pragma comment(lib, "mf")
#pragma comment(lib, "mfuuid")

template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}

// Read data from a byte stream into a media buffer.
//
// This function reads a maximum of cbMax bytes, or up to the size size of the 
// buffer, whichever is smaller. If the end of the byte stream is reached, the 
// actual amount of data read might be less than either of these values.
//
// To find out how much data was read, call IMFMediaBuffer::GetCurrentLength.

HRESULT ReadFromByteStream(
    IMFByteStream *pStream,     // Pointer to the byte stream.
    IMFMediaBuffer *pBuffer,    // Pointer to the media buffer.
    DWORD cbMax                 // Maximum amount to read.
    )
{
    DWORD cbBufferMax = 0;
    DWORD cbRead = 0;
    BYTE *pData= NULL;

    HRESULT hr = pBuffer->Lock(&pData, &cbBufferMax, NULL);

    // Do not exceed the maximum size of the buffer.
    if (SUCCEEDED(hr))
    {
        if (cbMax > cbBufferMax)
        {
            cbMax = cbBufferMax;
        }

        // Read up to cbMax bytes.
        hr = pStream->Read(pData, cbMax, &cbRead);
    }

    // Update the size of the valid data in the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->SetCurrentLength(cbRead);
    }
    if (pData)
    {
        pBuffer->Unlock();
    }
    return hr;
}


// Read the ASF Header Object from a byte stream and return a pointer to the 
// populated ASF ContentInfo object.
//
// The current read position of the byte stream must be at the start of the
// ASF Header Object.

HRESULT CreateContentInfo(IMFByteStream *pStream, 
    IMFASFContentInfo **ppContentInfo)
{
    const DWORD MIN_ASF_HEADER_SIZE = 30;
    
    QWORD cbHeader = 0;
    DWORD cbBuffer = 0;

    IMFASFContentInfo *pContentInfo = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    // Create the ASF ContentInfo object.
    HRESULT hr = MFCreateASFContentInfo(&pContentInfo);
    
    // Read the first 30 bytes to find the total header size.

    if (SUCCEEDED(hr))
    {
        hr = MFCreateMemoryBuffer(MIN_ASF_HEADER_SIZE, &pBuffer);
    }
    if (SUCCEEDED(hr))
    {
        hr = ReadFromByteStream(pStream, pBuffer,MIN_ASF_HEADER_SIZE);
    }
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->GetHeaderSize(pBuffer, &cbHeader);
    }

    // Pass the first 30 bytes to the ContentInfo object.
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->ParseHeader(pBuffer, 0);
    }

    SafeRelease(&pBuffer);

    if (SUCCEEDED(hr))
    {
        cbBuffer = (DWORD)(cbHeader - MIN_ASF_HEADER_SIZE);

        hr = MFCreateMemoryBuffer(cbBuffer, &pBuffer);
    }

    // Read the rest of the header and finish parsing the header.
    if (SUCCEEDED(hr))
    {
        hr = ReadFromByteStream(pStream, pBuffer, cbBuffer);
    }
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->ParseHeader(pBuffer, MIN_ASF_HEADER_SIZE);
    }
    if (SUCCEEDED(hr))
    {
        // Return the pointer to the caller.
        *ppContentInfo = pContentInfo;
        (*ppContentInfo)->AddRef();
    }
    SafeRelease(&pBuffer);
    SafeRelease(&pContentInfo);
    return hr;
} 

// Create and initialize the ASF splitter.

HRESULT CreateASFSplitter (IMFASFContentInfo* pContentInfo, 
    IMFASFSplitter** ppSplitter)
{
    IMFASFSplitter *pSplitter = NULL;

    // Create the splitter object.
    HRESULT hr = MFCreateASFSplitter(&pSplitter);

    // Initialize the splitter to work with specific ASF data.
    if (SUCCEEDED(hr))
    {
        hr = pSplitter->Initialize(pContentInfo);
    }
    if (SUCCEEDED(hr))
    {
        // Return the object to the caller.
        *ppSplitter = pSplitter;
        (*ppSplitter)->AddRef();
    }
    SafeRelease(&pSplitter);
    return hr;
}


// Select the first video stream for parsing with the ASF splitter.

HRESULT SelectVideoStream(IMFASFContentInfo *pContentInfo, 
    IMFASFSplitter *pSplitter, BOOL *pbHasVideo)
{
    DWORD   cStreams = 0;
    WORD    wStreamID = 0;

    IMFASFProfile *pProfile = NULL;
    IMFASFStreamConfig *pStream = NULL;

    // Get the ASF profile from the ContentInfo object.
    HRESULT hr = pContentInfo->GetProfile(&pProfile);

    // Loop through all of the streams in the profile.
    if (SUCCEEDED(hr))
    {
        hr = pProfile->GetStreamCount(&cStreams);
    }

    if (SUCCEEDED(hr))
    {
        for (DWORD i = 0; i < cStreams; i++)
        {
            GUID    streamType = GUID_NULL;

            // Get the stream type and stream identifier.
            hr = pProfile->GetStream(i, &wStreamID, &pStream);
            if (FAILED(hr)) 
            {
                break;
            }

            hr = pStream->GetStreamType(&streamType);
            if (FAILED(hr)) 
            {
                break;
            }

            if (streamType == MFMediaType_Video)
            {
                *pbHasVideo = TRUE;
                break;
            }
            SafeRelease(&pStream);
        }
    }

    // Select the video stream, if found.
    if (SUCCEEDED(hr))
    {
        if (*pbHasVideo)
        {
            // SelectStreams takes an array of stream identifiers.
            hr = pSplitter->SelectStreams(&wStreamID, 1);
        }
    }
    SafeRelease(&pStream);
    SafeRelease(&pProfile);
    return hr;
}

inline BOOL IsRandomAccessPoint(IMFSample *pSample)
{
    // Check for the "clean point" attribute. Default to FALSE.
    return MFGetAttributeUINT32(pSample, MFSampleExtension_CleanPoint, FALSE);
}

void DisplayKeyFrame(IMFSample *pSample)
{
    DWORD   cBuffers = 0;           // Buffer count
    DWORD   cbTotalLength = 0;      // Buffer length
    MFTIME  hnsTime = 0;            // Time stamp

    // Print various information about the key frame.
    if (SUCCEEDED(pSample->GetBufferCount(&cBuffers)))
    {
        wprintf_s(L"Buffer count: %d\n", cBuffers);
    }
    if (SUCCEEDED(pSample->GetTotalLength(&cbTotalLength)))
    {
        wprintf_s(L"Length: %d bytes\n", cbTotalLength);
    }
    if (SUCCEEDED(pSample->GetSampleTime(&hnsTime)))
    {
        // Convert the time stamp to seconds.
        double sec = static_cast<double>(hnsTime / 10000) / 1000;
        wprintf_s(L"Time stamp: %f sec.\n", sec);
    }
    wprintf_s(L"\n");
}


// Parse the video stream and display information about the video samples.
//
// The current read position of the byte stream must be at the start of the ASF
// Data Object.

HRESULT DisplayKeyFrames(IMFByteStream *pStream, IMFASFSplitter *pSplitter)
{
    const DWORD cbReadSize = 2048;  // Read size (arbitrary value)

    IMFMediaBuffer *pBuffer = NULL;
    IMFSample *pSample = NULL;

    HRESULT hr = S_OK;
    while (SUCCEEDED(hr))
    {
        // The parser must get a newly allocated buffer each time.
        hr = MFCreateMemoryBuffer(cbReadSize, &pBuffer);
        if (FAILED(hr))
        {
            break;
        }

        // Read data into the buffer.
        hr = ReadFromByteStream(pStream, pBuffer, cbReadSize);
        if (FAILED(hr)) 
        {
            break; 
        }

        // Get the amound of data that was read.
        DWORD cbData;
        hr = pBuffer->GetCurrentLength(&cbData);
        if (FAILED(hr)) 
        { 
            break; 
        }

        if (cbData == 0)
        {
            break; // End of file.
        }

        // Send the data to the ASF splitter.
        hr = pSplitter->ParseData(pBuffer, 0, 0);
        SafeRelease(&pBuffer);
        if (FAILED(hr)) 
        { 
            break; 
        }

        // Pull samples from the splitter.
        DWORD parsingStatus = 0;
        do
        {
            WORD streamID;
            hr = pSplitter->GetNextSample(&parsingStatus, &streamID, &pSample);
            if (FAILED(hr)) 
            { 
                break; 
            }
            if (pSample == NULL)
            {
                // No samples yet. Parse more data.
                break;
            }
            if (IsRandomAccessPoint(pSample))
            {
                DisplayKeyFrame(pSample);
            }
            SafeRelease(&pSample);
            
        } while (parsingStatus & ASF_STATUSFLAGS_INCOMPLETE);
    }
    SafeRelease(&pSample);
    SafeRelease(&pBuffer);
    return hr;
}

int wmain(int argc, WCHAR* argv[])
{
    if (argc != 2)
    {
        _s(L"Usage: %s input.wmv");
        return 0;
    }

    // Start the Media Foundation platform.
    HRESULT hr = MFStartup(MF_VERSION);
    if (SUCCEEDED(hr))
    {
        PCWSTR pszFileName = argv[1]; 
        BOOL   bHasVideo = FALSE;

        IMFByteStream       *pStream = NULL;
        IMFASFContentInfo   *pContentInfo = NULL;
        IMFASFSplitter      *pSplitter = NULL;

        // Open the file.
        hr = MFCreateFile(MF_ACCESSMODE_READ, MF_OPENMODE_FAIL_IF_NOT_EXIST, 
            MF_FILEFLAGS_NONE, pszFileName, &pStream);

        // Read the ASF header.
        if (SUCCEEDED(hr))
        {
            hr = CreateContentInfo(pStream, &pContentInfo);
        }

        // Create the ASF splitter.
        if (SUCCEEDED(hr))
        {
            hr = CreateASFSplitter(pContentInfo, &pSplitter);
        }

        // Select the first video stream.
        if (SUCCEEDED(hr))
        {
            hr = SelectVideoStream(pContentInfo, pSplitter, &bHasVideo);
        }

        // Parse the ASF file.
        if (SUCCEEDED(hr))
        {
            if (bHasVideo)
            {
                hr = DisplayKeyFrames(pStream, pSplitter);
            }
            else
            {
                wprintf_s(L"No video stream.\n");
            }
        }
        SafeRelease(&pSplitter);
        SafeRelease(&pContentInfo);
        SafeRelease(&pStream);
    
        // Shut down the Media Foundation platform.
        MFShutdown();
    }
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

 

 



