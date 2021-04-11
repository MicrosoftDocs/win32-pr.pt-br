---
description: Este tópico descreve as etapas para popular as estruturas necessárias para reproduzir dados de áudio no XAudio2.
ms.assetid: caeb522e-d4f6-91e2-5e85-ea0af0f61300
title: 'Como: Carregar arquivos de dados de áudio no XAudio2'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 659b4d8e106b6f0b2eb942505f99562f56fdada7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090679"
---
# <a name="how-to-load-audio-data-files-in-xaudio2"></a><span data-ttu-id="f6788-103">Como: Carregar arquivos de dados de áudio no XAudio2</span><span class="sxs-lookup"><span data-stu-id="f6788-103">How to: Load Audio Data Files in XAudio2</span></span>

> [!Note]  
> <span data-ttu-id="f6788-104">Esse conteúdo se aplica somente a aplicativos da área de trabalho e exigirá revisão para funcionar em um aplicativo da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="f6788-104">This content applies only to desktop apps and will require revision to function in a Windows Store app.</span></span> <span data-ttu-id="f6788-105">Veja a documentação de [**createfile2**](/windows/win32/api/fileapi/nf-fileapi-createfile2), [**CreateEventEx**](/windows/win32/api/synchapi/nf-synchapi-createeventexa), [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex), [**SetFilePointerEx**](/windows/win32/api/fileapi/nf-fileapi-setfilepointerex)e [**GetOverlappedResultEx**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresultex).</span><span class="sxs-lookup"><span data-stu-id="f6788-105">Please refer to the documentation for [**CreateFile2**](/windows/win32/api/fileapi/nf-fileapi-createfile2), [**CreateEventEx**](/windows/win32/api/synchapi/nf-synchapi-createeventexa), [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex), [**SetFilePointerEx**](/windows/win32/api/fileapi/nf-fileapi-setfilepointerex), and [**GetOverlappedResultEx**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresultex).</span></span> <span data-ttu-id="f6788-106">Consulte SoundFileReader. h/. cpp no exemplo do Windows 8 do BasicSound na [Galeria de exemplos SDK do Windows](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/XAudio2%20audio%20file%20playback%20sample%20(Windows%208)).</span><span class="sxs-lookup"><span data-stu-id="f6788-106">See SoundFileReader.h/.cpp in the BasicSound Windows 8 sample from the [Windows SDK Samples Gallery](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/XAudio2%20audio%20file%20playback%20sample%20(Windows%208)).</span></span>

 

<span data-ttu-id="f6788-107">Este tópico descreve as etapas para popular as estruturas necessárias para reproduzir dados de áudio no XAudio2.</span><span class="sxs-lookup"><span data-stu-id="f6788-107">This topic describes the steps to populate the structures required to play audio data in XAudio2.</span></span> <span data-ttu-id="f6788-108">As etapas a seguir carregam as partes ' fmt ' e ' data ' de um arquivo de áudio e as usam para preencher uma estrutura **WAVEFORMATEXTENSIBLE** e uma estrutura de [**\_ buffer XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) .</span><span class="sxs-lookup"><span data-stu-id="f6788-108">The following steps load the 'fmt ' and 'data' chunks of an audio file, and uses them to populate a **WAVEFORMATEXTENSIBLE** structure and an [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure.</span></span>

-   [<span data-ttu-id="f6788-109">Preparando para analisar o arquivo de áudio.</span><span class="sxs-lookup"><span data-stu-id="f6788-109">Preparing to parse the audio file.</span></span>](#preparing-to-parse-the-audio-file)
-   [<span data-ttu-id="f6788-110">Populando estruturas XAudio2 com o conteúdo de partes de RIFF.</span><span class="sxs-lookup"><span data-stu-id="f6788-110">Populating XAudio2 structures with the contents of RIFF chunks.</span></span>](#populating-xaudio2-structures-with-the-contents-of-riff-chunks)

## <a name="preparing-to-parse-the-audio-file"></a><span data-ttu-id="f6788-111">Preparando para analisar o arquivo de áudio</span><span class="sxs-lookup"><span data-stu-id="f6788-111">Preparing to parse the audio file</span></span>

<span data-ttu-id="f6788-112">Os arquivos de áudio com suporte pelo XAudio2 usam o formato de arquivo de intercâmbio de recursos (RIFF).</span><span class="sxs-lookup"><span data-stu-id="f6788-112">Audio files supported by XAudio2 use the Resource Interchange File Format (RIFF).</span></span> <span data-ttu-id="f6788-113">O RIFF é descrito na visão geral do [riff (formato de arquivo de intercâmbio de recursos)](resource-interchange-file-format--riff-.md) .</span><span class="sxs-lookup"><span data-stu-id="f6788-113">RIFF is described in the [Resource Interchange File Format (RIFF)](resource-interchange-file-format--riff-.md) overview.</span></span> <span data-ttu-id="f6788-114">Os dados de áudio em um arquivo RIFF são carregados encontrando a parte do RIFF e, em seguida, fazendo um loop pela parte para localizar partes individuais contidas na parte do RIFF.</span><span class="sxs-lookup"><span data-stu-id="f6788-114">Audio data in a RIFF file is loaded by finding the RIFF chunk and then looping through the chunk to find individual chunks contained in the RIFF chunk.</span></span> <span data-ttu-id="f6788-115">As funções a seguir são exemplos de código para localizar partes e carregar dados contidos nas partes.</span><span class="sxs-lookup"><span data-stu-id="f6788-115">The following functions are examples of code to find chunks and load data contained in the chunks.</span></span>

-   <span data-ttu-id="f6788-116">Para localizar uma parte em um arquivo RIFF:</span><span class="sxs-lookup"><span data-stu-id="f6788-116">To find a chunk in a RIFF file:</span></span>

    ```
    #ifdef _XBOX //Big-Endian
    #define fourccRIFF 'RIFF'
    #define fourccDATA 'data'
    #define fourccFMT 'fmt '
    #define fourccWAVE 'WAVE'
    #define fourccXWMA 'XWMA'
    #define fourccDPDS 'dpds'
    #endif

    #ifndef _XBOX //Little-Endian
    #define fourccRIFF 'FFIR'
    #define fourccDATA 'atad'
    #define fourccFMT ' tmf'
    #define fourccWAVE 'EVAW'
    #define fourccXWMA 'AMWX'
    #define fourccDPDS 'sdpd'
    #endif
    HRESULT FindChunk(HANDLE hFile, DWORD fourcc, DWORD & dwChunkSize, DWORD & dwChunkDataPosition)
    {
        HRESULT hr = S_OK;
        if( INVALID_SET_FILE_POINTER == SetFilePointer( hFile, 0, NULL, FILE_BEGIN ) )
            return HRESULT_FROM_WIN32( GetLastError() );

        DWORD dwChunkType;
        DWORD dwChunkDataSize;
        DWORD dwRIFFDataSize = 0;
        DWORD dwFileType;
        DWORD bytesRead = 0;
        DWORD dwOffset = 0;

        while (hr == S_OK)
        {
            DWORD dwRead;
            if( 0 == ReadFile( hFile, &dwChunkType, sizeof(DWORD), &dwRead, NULL ) )
                hr = HRESULT_FROM_WIN32( GetLastError() );

            if( 0 == ReadFile( hFile, &dwChunkDataSize, sizeof(DWORD), &dwRead, NULL ) )
                hr = HRESULT_FROM_WIN32( GetLastError() );

            switch (dwChunkType)
            {
            case fourccRIFF:
                dwRIFFDataSize = dwChunkDataSize;
                dwChunkDataSize = 4;
                if( 0 == ReadFile( hFile, &dwFileType, sizeof(DWORD), &dwRead, NULL ) )
                    hr = HRESULT_FROM_WIN32( GetLastError() );
                break;

            default:
                if( INVALID_SET_FILE_POINTER == SetFilePointer( hFile, dwChunkDataSize, NULL, FILE_CURRENT ) )
                return HRESULT_FROM_WIN32( GetLastError() );            
            }

            dwOffset += sizeof(DWORD) * 2;
            
            if (dwChunkType == fourcc)
            {
                dwChunkSize = dwChunkDataSize;
                dwChunkDataPosition = dwOffset;
                return S_OK;
            }

            dwOffset += dwChunkDataSize;
            
            if (bytesRead >= dwRIFFDataSize) return S_FALSE;

        }

        return S_OK;
        
    }
    ```

    

-   <span data-ttu-id="f6788-117">Para ler dados em uma parte após sua localização.</span><span class="sxs-lookup"><span data-stu-id="f6788-117">To read data in a chunk after it has been located.</span></span>

    <span data-ttu-id="f6788-118">Depois que uma parte desejada é encontrada, seus dados podem ser lidos ajustando o ponteiro do arquivo para o início da seção de dados da parte.</span><span class="sxs-lookup"><span data-stu-id="f6788-118">Once a desired chunk is found, its data can be read by adjusting the file pointer to the beginning of the data section of the chunk.</span></span> <span data-ttu-id="f6788-119">Uma função para ler os dados de uma parte assim que ela for encontrada pode ser parecida com esta.</span><span class="sxs-lookup"><span data-stu-id="f6788-119">A function to read the data from a chunk once it is found might look like this.</span></span>

    ```
    HRESULT ReadChunkData(HANDLE hFile, void * buffer, DWORD buffersize, DWORD bufferoffset)
    {
        HRESULT hr = S_OK;
        if( INVALID_SET_FILE_POINTER == SetFilePointer( hFile, bufferoffset, NULL, FILE_BEGIN ) )
            return HRESULT_FROM_WIN32( GetLastError() );
        DWORD dwRead;
        if( 0 == ReadFile( hFile, buffer, buffersize, &dwRead, NULL ) )
            hr = HRESULT_FROM_WIN32( GetLastError() );
        return hr;
    }
    ```

    

## <a name="populating-xaudio2-structures-with-the-contents-of-riff-chunks"></a><span data-ttu-id="f6788-120">Populando estruturas XAudio2 com o conteúdo de partes RIFF</span><span class="sxs-lookup"><span data-stu-id="f6788-120">Populating XAudio2 structures with the contents of RIFF chunks</span></span>

<span data-ttu-id="f6788-121">Para que o XAudio2 reproduza áudio com uma voz de origem, ele precisa de uma estrutura **WAVEFORMATEX** e uma estrutura de [**\_ buffer XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) .</span><span class="sxs-lookup"><span data-stu-id="f6788-121">In order for XAudio2 to play audio with a source voice, it needs a **WAVEFORMATEX** structure and an [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure.</span></span> <span data-ttu-id="f6788-122">A estrutura **WAVEFORMATEX** pode ser uma estrutura maior, como **WAVEFORMATEXTENSIBLE** que contém uma estrutura **WAVEFORMATEX** como seu primeiro membro.</span><span class="sxs-lookup"><span data-stu-id="f6788-122">The **WAVEFORMATEX** structure may be a larger structure such as **WAVEFORMATEXTENSIBLE** that contains a **WAVEFORMATEX** structure as its first member.</span></span> <span data-ttu-id="f6788-123">Consulte a página de referência do **WAVEFORMATEX** para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="f6788-123">See the **WAVEFORMATEX** reference page for more information.</span></span>

<span data-ttu-id="f6788-124">Neste exemplo, um **WAVEFORMATEXTENSIBLE** está sendo usado para permitir o carregamento de arquivos de áudio PCM com mais de dois canais.</span><span class="sxs-lookup"><span data-stu-id="f6788-124">In this example a **WAVEFORMATEXTENSIBLE** is being used to allow loading of PCM audio files with more than two channels.</span></span>

<span data-ttu-id="f6788-125">As etapas a seguir ilustram o uso das funções descritas acima para popular uma estrutura de **WAVEFORMATEXTENSIBLE** e uma estrutura de [**\_ buffer XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) .</span><span class="sxs-lookup"><span data-stu-id="f6788-125">The following steps illustrate using the functions described above to populate a **WAVEFORMATEXTENSIBLE** structure and an [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure.</span></span> <span data-ttu-id="f6788-126">Nesse caso, o arquivo de áudio que está sendo carregado contém dados PCM e só conterá um bloco ' RIFF ', ' fmt ' e ' dados '.</span><span class="sxs-lookup"><span data-stu-id="f6788-126">In this case, the audio file being loaded contains PCM data, and will only contain a 'RIFF', 'fmt ', and 'data' chunk.</span></span> <span data-ttu-id="f6788-127">Outros formatos podem conter tipos de bloco adicionais, conforme descrito em [formato de arquivo de intercâmbio de recursos (riff)](resource-interchange-file-format--riff-.md).</span><span class="sxs-lookup"><span data-stu-id="f6788-127">Other formats may contain additional chunk types as described in [Resource Interchange File Format (RIFF)](resource-interchange-file-format--riff-.md).</span></span>

1.  <span data-ttu-id="f6788-128">Declare as estruturas [**de \_ buffer**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) **WAVEFORMATEXTENSIBLE** e XAudio2.</span><span class="sxs-lookup"><span data-stu-id="f6788-128">Declare **WAVEFORMATEXTENSIBLE** and [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structures.</span></span>
    ```
    WAVEFORMATEXTENSIBLE wfx = {0};
    XAUDIO2_BUFFER buffer = {0};
    ```

    

2.  <span data-ttu-id="f6788-129">Abra o arquivo de áudio com CreateFile.</span><span class="sxs-lookup"><span data-stu-id="f6788-129">Open the audio file with CreateFile.</span></span>
    ```
    #ifdef _XBOX
    char * strFileName = "game:\\media\\MusicMono.wav";
    #else
    TCHAR * strFileName = _TEXT("media\\MusicMono.wav");
    #endif
    // Open the file
    HANDLE hFile = CreateFile(
        strFileName,
        GENERIC_READ,
        FILE_SHARE_READ,
        NULL,
        OPEN_EXISTING,
        0,
        NULL );

    if( INVALID_HANDLE_VALUE == hFile )
        return HRESULT_FROM_WIN32( GetLastError() );

    if( INVALID_SET_FILE_POINTER == SetFilePointer( hFile, 0, NULL, FILE_BEGIN ) )
        return HRESULT_FROM_WIN32( GetLastError() );
    ```

    

3.  <span data-ttu-id="f6788-130">Localize a parte ' RIFF ' no arquivo de áudio e verifique o tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="f6788-130">Locate the 'RIFF' chunk in the audio file, and check the file type.</span></span>
    ```
    DWORD dwChunkSize;
    DWORD dwChunkPosition;
    //check the file type, should be fourccWAVE or 'XWMA'
    FindChunk(hFile,fourccRIFF,dwChunkSize, dwChunkPosition );
    DWORD filetype;
    ReadChunkData(hFile,&filetype,sizeof(DWORD),dwChunkPosition);
    if (filetype != fourccWAVE)
        return S_FALSE;
    ```

    

4.  <span data-ttu-id="f6788-131">Localize a parte ' fmt ' e copie seu conteúdo em uma estrutura **WAVEFORMATEXTENSIBLE** .</span><span class="sxs-lookup"><span data-stu-id="f6788-131">Locate the 'fmt ' chunk, and copy its contents into a **WAVEFORMATEXTENSIBLE** structure.</span></span>
    ```
    FindChunk(hFile,fourccFMT, dwChunkSize, dwChunkPosition );
    ReadChunkData(hFile, &wfx, dwChunkSize, dwChunkPosition );
    ```

    

5.  <span data-ttu-id="f6788-132">Localize a parte ' dados ' e leia seu conteúdo em um buffer.</span><span class="sxs-lookup"><span data-stu-id="f6788-132">Locate the 'data' chunk, and read its contents into a buffer.</span></span>
    ```
    //fill out the audio data buffer with the contents of the fourccDATA chunk
    FindChunk(hFile,fourccDATA,dwChunkSize, dwChunkPosition );
    BYTE * pDataBuffer = new BYTE[dwChunkSize];
    ReadChunkData(hFile, pDataBuffer, dwChunkSize, dwChunkPosition);
    ```

    

6.  <span data-ttu-id="f6788-133">Popular uma estrutura de [**\_ buffer XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) .</span><span class="sxs-lookup"><span data-stu-id="f6788-133">Populate an [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure.</span></span>
    ```
    buffer.AudioBytes = dwChunkSize;  //size of the audio buffer in bytes
    buffer.pAudioData = pDataBuffer;  //buffer containing audio data
    buffer.Flags = XAUDIO2_END_OF_STREAM; // tell the source voice not to expect any data after this buffer
    ```

    

## <a name="related-topics"></a><span data-ttu-id="f6788-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f6788-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6788-135">Introdução</span><span class="sxs-lookup"><span data-stu-id="f6788-135">Getting Started</span></span>](getting-started.md)
</dt> <dt>

[<span data-ttu-id="f6788-136">Como: Reproduzir um som com o XAudio2</span><span class="sxs-lookup"><span data-stu-id="f6788-136">How to: Play a Sound with XAudio2</span></span>](how-to--play-a-sound-with-xaudio2.md)
</dt> <dt>

[<span data-ttu-id="f6788-137">Referência de programação em XAudio2</span><span class="sxs-lookup"><span data-stu-id="f6788-137">XAudio2 Programming Reference</span></span>](programming-reference.md)
</dt> </dl>

 

 
