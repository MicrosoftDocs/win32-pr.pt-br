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
# <a name="how-to-load-audio-data-files-in-xaudio2"></a>Como: Carregar arquivos de dados de áudio no XAudio2

> [!Note]  
> Esse conteúdo se aplica somente a aplicativos da área de trabalho e exigirá revisão para funcionar em um aplicativo da Windows Store. Veja a documentação de [**createfile2**](/windows/win32/api/fileapi/nf-fileapi-createfile2), [**CreateEventEx**](/windows/win32/api/synchapi/nf-synchapi-createeventexa), [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex), [**SetFilePointerEx**](/windows/win32/api/fileapi/nf-fileapi-setfilepointerex)e [**GetOverlappedResultEx**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresultex). Consulte SoundFileReader. h/. cpp no exemplo do Windows 8 do BasicSound na [Galeria de exemplos SDK do Windows](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/XAudio2%20audio%20file%20playback%20sample%20(Windows%208)).

 

Este tópico descreve as etapas para popular as estruturas necessárias para reproduzir dados de áudio no XAudio2. As etapas a seguir carregam as partes ' fmt ' e ' data ' de um arquivo de áudio e as usam para preencher uma estrutura **WAVEFORMATEXTENSIBLE** e uma estrutura de [**\_ buffer XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) .

-   [Preparando para analisar o arquivo de áudio.](#preparing-to-parse-the-audio-file)
-   [Populando estruturas XAudio2 com o conteúdo de partes de RIFF.](#populating-xaudio2-structures-with-the-contents-of-riff-chunks)

## <a name="preparing-to-parse-the-audio-file"></a>Preparando para analisar o arquivo de áudio

Os arquivos de áudio com suporte pelo XAudio2 usam o formato de arquivo de intercâmbio de recursos (RIFF). O RIFF é descrito na visão geral do [riff (formato de arquivo de intercâmbio de recursos)](resource-interchange-file-format--riff-.md) . Os dados de áudio em um arquivo RIFF são carregados encontrando a parte do RIFF e, em seguida, fazendo um loop pela parte para localizar partes individuais contidas na parte do RIFF. As funções a seguir são exemplos de código para localizar partes e carregar dados contidos nas partes.

-   Para localizar uma parte em um arquivo RIFF:

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

    

-   Para ler dados em uma parte após sua localização.

    Depois que uma parte desejada é encontrada, seus dados podem ser lidos ajustando o ponteiro do arquivo para o início da seção de dados da parte. Uma função para ler os dados de uma parte assim que ela for encontrada pode ser parecida com esta.

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

    

## <a name="populating-xaudio2-structures-with-the-contents-of-riff-chunks"></a>Populando estruturas XAudio2 com o conteúdo de partes RIFF

Para que o XAudio2 reproduza áudio com uma voz de origem, ele precisa de uma estrutura **WAVEFORMATEX** e uma estrutura de [**\_ buffer XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) . A estrutura **WAVEFORMATEX** pode ser uma estrutura maior, como **WAVEFORMATEXTENSIBLE** que contém uma estrutura **WAVEFORMATEX** como seu primeiro membro. Consulte a página de referência do **WAVEFORMATEX** para obter mais informações.

Neste exemplo, um **WAVEFORMATEXTENSIBLE** está sendo usado para permitir o carregamento de arquivos de áudio PCM com mais de dois canais.

As etapas a seguir ilustram o uso das funções descritas acima para popular uma estrutura de **WAVEFORMATEXTENSIBLE** e uma estrutura de [**\_ buffer XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) . Nesse caso, o arquivo de áudio que está sendo carregado contém dados PCM e só conterá um bloco ' RIFF ', ' fmt ' e ' dados '. Outros formatos podem conter tipos de bloco adicionais, conforme descrito em [formato de arquivo de intercâmbio de recursos (riff)](resource-interchange-file-format--riff-.md).

1.  Declare as estruturas [**de \_ buffer**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) **WAVEFORMATEXTENSIBLE** e XAudio2.
    ```
    WAVEFORMATEXTENSIBLE wfx = {0};
    XAUDIO2_BUFFER buffer = {0};
    ```

    

2.  Abra o arquivo de áudio com CreateFile.
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

    

3.  Localize a parte ' RIFF ' no arquivo de áudio e verifique o tipo de arquivo.
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

    

4.  Localize a parte ' fmt ' e copie seu conteúdo em uma estrutura **WAVEFORMATEXTENSIBLE** .
    ```
    FindChunk(hFile,fourccFMT, dwChunkSize, dwChunkPosition );
    ReadChunkData(hFile, &wfx, dwChunkSize, dwChunkPosition );
    ```

    

5.  Localize a parte ' dados ' e leia seu conteúdo em um buffer.
    ```
    //fill out the audio data buffer with the contents of the fourccDATA chunk
    FindChunk(hFile,fourccDATA,dwChunkSize, dwChunkPosition );
    BYTE * pDataBuffer = new BYTE[dwChunkSize];
    ReadChunkData(hFile, pDataBuffer, dwChunkSize, dwChunkPosition);
    ```

    

6.  Popular uma estrutura de [**\_ buffer XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) .
    ```
    buffer.AudioBytes = dwChunkSize;  //size of the audio buffer in bytes
    buffer.pAudioData = pDataBuffer;  //buffer containing audio data
    buffer.Flags = XAUDIO2_END_OF_STREAM; // tell the source voice not to expect any data after this buffer
    ```

    

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Introdução](getting-started.md)
</dt> <dt>

[Como: Reproduzir um som com o XAudio2](how-to--play-a-sound-with-xaudio2.md)
</dt> <dt>

[Referência de programação em XAudio2](programming-reference.md)
</dt> </dl>

 

 
