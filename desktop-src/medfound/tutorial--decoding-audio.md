---
description: Este tutorial mostra como usar o leitor de origem para decodificar áudio de um arquivo de mídia e gravar o áudio em um arquivo WAVE.
ms.assetid: ed40e201-c6ed-444f-bdaa-a5f33d1cc068
title: 'Tutorial: decodificando áudio'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 539eb6d9f48419b62fa1c379c636abaf2bb0a63a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104554742"
---
# <a name="tutorial-decoding-audio"></a>Tutorial: decodificando áudio

Este tutorial mostra como usar o [leitor de origem](source-reader.md) para decodificar áudio de um arquivo de mídia e gravar o áudio em um arquivo Wave. O tutorial é baseado no exemplo de [clipe de áudio](audio-clip-sample.md) .

-   [Visão geral](#overview)
-   [Arquivos de cabeçalho e biblioteca](#header-and-library-files)
-   [Implementar wmain](#implement-wmain)
-   [Gravar o arquivo WAVE](#write-the-wave-file)
-   [Configurar o leitor de origem](#configure-the-source-reader)
-   [Gravar o cabeçalho do arquivo WAVE](#write-the-wave-file-header)
-   [Calcular o tamanho máximo dos dados](#calculate-the-maximum-data-size)
-   [Decodificar o áudio](#decode-the-audio)
-   [Finalizar o cabeçalho do arquivo](#finalize-the-file-header)
-   [Tópicos relacionados](#related-topics)

## <a name="overview"></a>Visão geral

Neste tutorial, você criará um aplicativo de console que usa dois argumentos de linha de comando: o nome de um arquivo de entrada que contém um fluxo de áudio e o nome do arquivo de saída. O aplicativo lê cinco segundos de dados de áudio do arquivo de entrada e grava o áudio no arquivo de saída como dados de onda.

Para obter os dados de áudio decodificados, o aplicativo usa o objeto de leitor de origem. O leitor de origem expõe a interface [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) . Para gravar o áudio decodificado no arquivo WAVE, os aplicativos usam as funções de e/s do Windows. A imagem a seguir ilustra esse processo.

![diagrama mostrando o leitor de origem que obtém os dados de áudio do arquivo de origem.](images/audio-clip-tutorial.gif)

Em sua forma mais simples, um arquivo WAVE tem a seguinte estrutura:



| Tipo de Dados                              | Tamanho (Bytes) | Valor                                                                 |
|----------------------------------------|--------------|-----------------------------------------------------------------------|
| **FOURCC**                             | 4            | METÁLICA                                                                |
| **DWORD**                              | 4            | Tamanho total do arquivo, sem incluir os primeiros 8 bytes                      |
| **FOURCC**                             | 4            | ONDA                                                                |
| **FOURCC**                             | 4            | fmt                                                                |
| **DWORD**                              | 4            | Tamanho dos dados de [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) a seguir. |
| [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) | Varia       | Cabeçalho do formato de áudio.                                                  |
| **FOURCC**                             | 4            | dado                                                                |
| **DWORD**                              | 4            | Tamanho dos dados de áudio.                                               |
| **MINUCIOSA**\[\]                           | Varia       | Dados de áudio.                                                           |



 

> [!Note]  
> Um **FOURCC** é um **DWORD** formado pela concatenação de quatro caracteres ASCII.

 

Essa estrutura básica pode ser estendida com a adição de metadados de arquivo e outras informações, que está além do escopo deste tutorial.

## <a name="header-and-library-files"></a>Arquivos de cabeçalho e biblioteca

Inclua os seguintes arquivos de cabeçalho em seu projeto:


```C++
#define WINVER _WIN32_WINNT_WIN7

#include <windows.h>
#include <mfapi.h>
#include <mfidl.h>
#include <mfreadwrite.h>
#include <stdio.h>
#include <mferror.h>
```



Link para as seguintes bibliotecas:

-   mfplat. lib
-   mfreadwrite. lib
-   mfuuid. lib

## <a name="implement-wmain"></a>Implementar wmain

O código a seguir mostra a função de ponto de entrada para o aplicativo.


```C++
int wmain(int argc, wchar_t* argv[])
{
    HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);

    if (argc != 3)
    {
        printf("arguments: input_file output_file.wav\n");
        return 1;
    }

    const WCHAR *wszSourceFile = argv[1];
    const WCHAR *wszTargetFile = argv[2];

    const LONG MAX_AUDIO_DURATION_MSEC = 5000; // 5 seconds

    HRESULT hr = S_OK;

    IMFSourceReader *pReader = NULL;
    HANDLE hFile = INVALID_HANDLE_VALUE;

    // Initialize the COM library.
    hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | COINIT_DISABLE_OLE1DDE);

    // Initialize the Media Foundation platform.
    if (SUCCEEDED(hr))
    {
        hr = MFStartup(MF_VERSION);
    }

    // Create the source reader to read the input file.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateSourceReaderFromURL(wszSourceFile, NULL, &pReader);
        if (FAILED(hr))
        {
            printf("Error opening input file: %S\n", wszSourceFile, hr);
        }
    }

    // Open the output file for writing.
    if (SUCCEEDED(hr))
    {
        hFile = CreateFile(wszTargetFile, GENERIC_WRITE, FILE_SHARE_READ, NULL,
            CREATE_ALWAYS, 0, NULL);

        if (hFile == INVALID_HANDLE_VALUE)
        {
            hr = HRESULT_FROM_WIN32(GetLastError());
            printf("Cannot create output file: %S\n", wszTargetFile, hr);
        }
    }

    // Write the WAVE file.
    if (SUCCEEDED(hr))
    {
        hr = WriteWaveFile(pReader, hFile, MAX_AUDIO_DURATION_MSEC);
    }

    if (FAILED(hr))
    {
        printf("Failed, hr = 0x%X\n", hr);
    }

    // Clean up.
    if (hFile != INVALID_HANDLE_VALUE)
    {
        CloseHandle(hFile);
    }

    SafeRelease(&pReader);
    MFShutdown();
    CoUninitialize();

    return SUCCEEDED(hr) ? 0 : 1;
};
```



Essa função faz o seguinte:

1.  Chama [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) para inicializar a biblioteca com.
2.  Chama [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) para inicializar a plataforma de Media Foundation.
3.  Chama [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl) para criar o leitor de origem. Essa função usa o nome do arquivo de entrada e recebe um ponteiro de interface [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) .
4.  Cria o arquivo de saída chamando a função **CreateFile** , que retorna um identificador de arquivo.
5.  Chama a função [WriteWavFile](#write-the-wave-file) definida pelo aplicativo. Essa função decodifica o áudio e grava o arquivo WAVE.
6.  Libera o ponteiro [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) e o identificador de arquivo.
7.  Chama [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) para desligar a plataforma Media Foundation.
8.  Chama [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) para liberar a biblioteca com.

## <a name="write-the-wave-file"></a>Gravar o arquivo WAVE

A maior parte do trabalho ocorre na `WriteWavFile` função, que é chamada de `wmain` .


```C++
//-------------------------------------------------------------------
// WriteWaveFile
//
// Writes a WAVE file by getting audio data from the source reader.
//
//-------------------------------------------------------------------

HRESULT WriteWaveFile(
    IMFSourceReader *pReader,   // Pointer to the source reader.
    HANDLE hFile,               // Handle to the output file.
    LONG msecAudioData          // Maximum amount of audio data to write, in msec.
    )
{
    HRESULT hr = S_OK;

    DWORD cbHeader = 0;         // Size of the WAVE file header, in bytes.
    DWORD cbAudioData = 0;      // Total bytes of PCM audio data written to the file.
    DWORD cbMaxAudioData = 0;

    IMFMediaType *pAudioType = NULL;    // Represents the PCM audio format.

    // Configure the source reader to get uncompressed PCM audio from the source file.

    hr = ConfigureAudioStream(pReader, &pAudioType);

    // Write the WAVE file header.
    if (SUCCEEDED(hr))
    {
        hr = WriteWaveHeader(hFile, pAudioType, &cbHeader);
    }

    // Calculate the maximum amount of audio to decode, in bytes.
    if (SUCCEEDED(hr))
    {
        cbMaxAudioData = CalculateMaxAudioDataSize(pAudioType, cbHeader, msecAudioData);

        // Decode audio data to the file.
        hr = WriteWaveData(hFile, pReader, cbMaxAudioData, &cbAudioData);
    }

    // Fix up the RIFF headers with the correct sizes.
    if (SUCCEEDED(hr))
    {
        hr = FixUpChunkSizes(hFile, cbHeader, cbAudioData);
    }

    SafeRelease(&pAudioType);
    return hr;
}
```



Essa função chama uma série de outras funções definidas pelo aplicativo:

1.  A função [ConfigureAudioStream](#configure-the-source-reader) Inicializa o leitor de origem. Essa função recebe um ponteiro para a interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) , que é usada para obter uma descrição do formato de áudio decodificado, incluindo taxa de amostra, número de canais e profundidade de bits (bits por amostra).
2.  A função WriteWaveHeader grava a primeira parte do arquivo WAVE, incluindo o cabeçalho e o início da parte ' data '.
3.  A função CalculateMaxAudioDataSize calcula a quantidade máxima de áudio a ser gravada no arquivo, em bytes.
4.  A função WriteWaveData grava os dados de áudio do PCM no arquivo.
5.  A função FixUpChunkSizes grava as informações de tamanho de arquivo que aparecem após os valores **FOURCC** ' riff ' e ' data ' no arquivo Wave. (Esses valores não são conhecidos até que sejam `WriteWaveData` concluídos.)

Essas funções são mostradas nas seções restantes deste tutorial.

## <a name="configure-the-source-reader"></a>Configurar o leitor de origem

A `ConfigureAudioStream` função configura o leitor de origem para decodificar o fluxo de áudio no arquivo de origem. Ele também retorna informações sobre o formato do áudio decodificado.

No Media Foundation, os formatos de mídia são descritos usando objetos de *tipo de mídia* . Um objeto de tipo de mídia expõe a interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) , que herda a interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) . Essencialmente, um tipo de mídia é uma coleção de propriedades que descreve o formato. Para obter mais informações, consulte [tipos de mídia](media-types.md).


```C++
//-------------------------------------------------------------------
// ConfigureAudioStream
//
// Selects an audio stream from the source file, and configures the
// stream to deliver decoded PCM audio.
//-------------------------------------------------------------------

HRESULT ConfigureAudioStream(
    IMFSourceReader *pReader,   // Pointer to the source reader.
    IMFMediaType **ppPCMAudio   // Receives the audio format.
    )
{
    IMFMediaType *pUncompressedAudioType = NULL;
    IMFMediaType *pPartialType = NULL;

    // Select the first audio stream, and deselect all other streams.
    HRESULT hr = pReader->SetStreamSelection(
        (DWORD)MF_SOURCE_READER_ALL_STREAMS, FALSE);

    if (SUCCEEDED(hr))
    {
        hr = pReader->SetStreamSelection(
            (DWORD)MF_SOURCE_READER_FIRST_AUDIO_STREAM, TRUE);
    }

    // Create a partial media type that specifies uncompressed PCM audio.
    hr = MFCreateMediaType(&pPartialType);

    if (SUCCEEDED(hr))
    {
        hr = pPartialType->SetGUID(MF_MT_MAJOR_TYPE, MFMediaType_Audio);
    }

    if (SUCCEEDED(hr))
    {
        hr = pPartialType->SetGUID(MF_MT_SUBTYPE, MFAudioFormat_PCM);
    }

    // Set this type on the source reader. The source reader will
    // load the necessary decoder.
    if (SUCCEEDED(hr))
    {
        hr = pReader->SetCurrentMediaType(
            (DWORD)MF_SOURCE_READER_FIRST_AUDIO_STREAM,
            NULL, pPartialType);
    }

    // Get the complete uncompressed format.
    if (SUCCEEDED(hr))
    {
        hr = pReader->GetCurrentMediaType(
            (DWORD)MF_SOURCE_READER_FIRST_AUDIO_STREAM,
            &pUncompressedAudioType);
    }

    // Ensure the stream is selected.
    if (SUCCEEDED(hr))
    {
        hr = pReader->SetStreamSelection(
            (DWORD)MF_SOURCE_READER_FIRST_AUDIO_STREAM,
            TRUE);
    }

    // Return the PCM format to the caller.
    if (SUCCEEDED(hr))
    {
        *ppPCMAudio = pUncompressedAudioType;
        (*ppPCMAudio)->AddRef();
    }

    SafeRelease(&pUncompressedAudioType);
    SafeRelease(&pPartialType);
    return hr;
}
```



A `ConfigureAudioStream` função faz o seguinte:

1.  Chama o método [**IMFSourceReader:: SetStreamSelection**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setstreamselection) para selecionar o fluxo de áudio e anular a seleção de todos os outros fluxos. Essa etapa pode melhorar o desempenho, pois impede que o leitor de origem mantenha em quadros de vídeo que o aplicativo não usa.
2.  Cria um tipo de mídia *parcial* que especifica o áudio PCM. A função cria o tipo parcial da seguinte maneira:
    1.  Chama [**MFCreateMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype) para criar um objeto de tipo de mídia vazio.
    2.  Define o atributo de [**\_ \_ \_ tipo principal MF MT**](mf-mt-major-type-attribute.md) como **MFMediaType \_ Audio**.
    3.  Define o atributo de [**\_ \_ subtipo MF MT**](mf-mt-subtype-attribute.md) como **MFAudioFormat \_ PCM**.
3.  Chama [**IMFSourceReader:: SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype) para definir o tipo parcial no leitor de origem. Se o arquivo de origem contiver áudio codificado, o leitor de origem carregará automaticamente o decodificador de áudio necessário.
4.  Chama [**IMFSourceReader:: GetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) para obter o tipo de mídia PCM real. Esse método retorna um tipo de mídia com todos os detalhes de formato preenchidos, como a taxa de amostra de áudio e o número de canais.
5.  Chama [**IMFSourceReader:: SetStreamSelection**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setstreamselection) para habilitar o fluxo de áudio.

## <a name="write-the-wave-file-header"></a>Gravar o cabeçalho do arquivo WAVE

A `WriteWaveHeader` função grava o cabeçalho do arquivo Wave.

A única API Media Foundation chamada a partir dessa função é [**MFCreateWaveFormatExFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype), que converte o tipo de mídia em uma estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .


```C++
//-------------------------------------------------------------------
// WriteWaveHeader
//
// Write the WAVE file header.
//
// Note: This function writes placeholder values for the file size
// and data size, as these values will need to be filled in later.
//-------------------------------------------------------------------

HRESULT WriteWaveHeader(
    HANDLE hFile,               // Output file.
    IMFMediaType *pMediaType,   // PCM audio format.
    DWORD *pcbWritten           // Receives the size of the header.
    )
{
    HRESULT hr = S_OK;
    UINT32 cbFormat = 0;

    WAVEFORMATEX *pWav = NULL;

    *pcbWritten = 0;

    // Convert the PCM audio format into a WAVEFORMATEX structure.
    hr = MFCreateWaveFormatExFromMFMediaType(pMediaType, &pWav, &cbFormat);

    // Write the 'RIFF' header and the start of the 'fmt ' chunk.
    if (SUCCEEDED(hr))
    {
        DWORD header[] = {
            // RIFF header
            FCC('RIFF'),
            0,
            FCC('WAVE'),
            // Start of 'fmt ' chunk
            FCC('fmt '),
            cbFormat
        };

        DWORD dataHeader[] = { FCC('data'), 0 };

        hr = WriteToFile(hFile, header, sizeof(header));

        // Write the WAVEFORMATEX structure.
        if (SUCCEEDED(hr))
        {
            hr = WriteToFile(hFile, pWav, cbFormat);
        }

        // Write the start of the 'data' chunk

        if (SUCCEEDED(hr))
        {
            hr = WriteToFile(hFile, dataHeader, sizeof(dataHeader));
        }

        if (SUCCEEDED(hr))
        {
            *pcbWritten = sizeof(header) + cbFormat + sizeof(dataHeader);
        }
    }


    CoTaskMemFree(pWav);
    return hr;
}
```



A `WriteToFile` função é uma função auxiliar simples que encapsula a função **WriteFile** do Windows e retorna um valor **HRESULT** .


```C++
//-------------------------------------------------------------------
//
// Writes a block of data to a file
//
// hFile: Handle to the file.
// p: Pointer to the buffer to write.
// cb: Size of the buffer, in bytes.
//
//-------------------------------------------------------------------

HRESULT WriteToFile(HANDLE hFile, void* p, DWORD cb)
{
    DWORD cbWritten = 0;
    HRESULT hr = S_OK;

    BOOL bResult = WriteFile(hFile, p, cb, &cbWritten, NULL);
    if (!bResult)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
    }
    return hr;
}
```



## <a name="calculate-the-maximum-data-size"></a>Calcular o tamanho máximo dos dados

Como o tamanho do arquivo é armazenado como um valor de 4 bytes no cabeçalho do arquivo, um arquivo WAVE é limitado a um tamanho máximo de 0xFFFFFFFF bytes – aproximadamente 4 GB. Esse valor inclui o tamanho do cabeçalho do arquivo. O áudio PCM tem uma taxa de bits constante, portanto, você pode calcular o tamanho máximo dos dados do formato de áudio, da seguinte maneira:


```C++
//-------------------------------------------------------------------
// CalculateMaxAudioDataSize
//
// Calculates how much audio to write to the WAVE file, given the
// audio format and the maximum duration of the WAVE file.
//-------------------------------------------------------------------

DWORD CalculateMaxAudioDataSize(
    IMFMediaType *pAudioType,    // The PCM audio format.
    DWORD cbHeader,              // The size of the WAVE file header.
    DWORD msecAudioData          // Maximum duration, in milliseconds.
    )
{
    UINT32 cbBlockSize = 0;         // Audio frame size, in bytes.
    UINT32 cbBytesPerSecond = 0;    // Bytes per second.

    // Get the audio block size and number of bytes/second from the audio format.

    cbBlockSize = MFGetAttributeUINT32(pAudioType, MF_MT_AUDIO_BLOCK_ALIGNMENT, 0);
    cbBytesPerSecond = MFGetAttributeUINT32(pAudioType, MF_MT_AUDIO_AVG_BYTES_PER_SECOND, 0);

    // Calculate the maximum amount of audio data to write.
    // This value equals (duration in seconds x bytes/second), but cannot
    // exceed the maximum size of the data chunk in the WAVE file.

        // Size of the desired audio clip in bytes:
    DWORD cbAudioClipSize = (DWORD)MulDiv(cbBytesPerSecond, msecAudioData, 1000);

    // Largest possible size of the data chunk:
    DWORD cbMaxSize = MAXDWORD - cbHeader;

    // Maximum size altogether.
    cbAudioClipSize = min(cbAudioClipSize, cbMaxSize);

    // Round to the audio block size, so that we do not write a partial audio frame.
    cbAudioClipSize = (cbAudioClipSize / cbBlockSize) * cbBlockSize;

    return cbAudioClipSize;
}
```



Para evitar quadros de áudio parciais, o tamanho é arredondado para o alinhamento de bloco, que é armazenado no atributo de [**\_ alinhamento de bloco de \_ áudio \_ \_ MF MT**](mf-mt-audio-block-alignment-attribute.md) .

## <a name="decode-the-audio"></a>Decodificar o áudio

A `WriteWaveData` função lê o áudio decodificado do arquivo de origem e grava no arquivo Wave.


```C++
//-------------------------------------------------------------------
// WriteWaveData
//
// Decodes PCM audio data from the source file and writes it to
// the WAVE file.
//-------------------------------------------------------------------

HRESULT WriteWaveData(
    HANDLE hFile,               // Output file.
    IMFSourceReader *pReader,   // Source reader.
    DWORD cbMaxAudioData,       // Maximum amount of audio data (bytes).
    DWORD *pcbDataWritten       // Receives the amount of data written.
    )
{
    HRESULT hr = S_OK;
    DWORD cbAudioData = 0;
    DWORD cbBuffer = 0;
    BYTE *pAudioData = NULL;

    IMFSample *pSample = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    // Get audio samples from the source reader.
    while (true)
    {
        DWORD dwFlags = 0;

        // Read the next sample.
        hr = pReader->ReadSample(
            (DWORD)MF_SOURCE_READER_FIRST_AUDIO_STREAM,
            0, NULL, &dwFlags, NULL, &pSample );

        if (FAILED(hr)) { break; }

        if (dwFlags & MF_SOURCE_READERF_CURRENTMEDIATYPECHANGED)
        {
            printf("Type change - not supported by WAVE file format.\n");
            break;
        }
        if (dwFlags & MF_SOURCE_READERF_ENDOFSTREAM)
        {
            printf("End of input file.\n");
            break;
        }

        if (pSample == NULL)
        {
            printf("No sample\n");
            continue;
        }

        // Get a pointer to the audio data in the sample.

        hr = pSample->ConvertToContiguousBuffer(&pBuffer);

        if (FAILED(hr)) { break; }


        hr = pBuffer->Lock(&pAudioData, NULL, &cbBuffer);

        if (FAILED(hr)) { break; }


        // Make sure not to exceed the specified maximum size.
        if (cbMaxAudioData - cbAudioData < cbBuffer)
        {
            cbBuffer = cbMaxAudioData - cbAudioData;
        }

        // Write this data to the output file.
        hr = WriteToFile(hFile, pAudioData, cbBuffer);

        if (FAILED(hr)) { break; }

        // Unlock the buffer.
        hr = pBuffer->Unlock();
        pAudioData = NULL;

        if (FAILED(hr)) { break; }

        // Update running total of audio data.
        cbAudioData += cbBuffer;

        if (cbAudioData >= cbMaxAudioData)
        {
            break;
        }

        SafeRelease(&pSample);
        SafeRelease(&pBuffer);
    }

    if (SUCCEEDED(hr))
    {
        printf("Wrote %d bytes of audio data.\n", cbAudioData);

        *pcbDataWritten = cbAudioData;
    }

    if (pAudioData)
    {
        pBuffer->Unlock();
    }

    SafeRelease(&pBuffer);
    SafeRelease(&pSample);
    return hr;
}
```



A `WriteWaveData` função faz o seguinte em um loop:

1.  Chama [**IMFSourceReader:: ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) para ler áudio do arquivo de origem. O parâmetro *dwFlags* recebe um **ou** bit de sinalizações da enumeração de sinalizador de [**leitor de \_ origem \_ \_ MF**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_flag) . O parâmetro *pSample* recebe um ponteiro para a interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , que é usada para acessar os dados de áudio. Em alguns casos, uma chamada para **ReadSample** não gera dados; nesse caso, o ponteiro **IMFSample** é **nulo**.
2.  Verifica *dwFlags* para os seguintes sinalizadores:
    -   **MF \_ \_READERF \_ CURRENTMEDIATYPECHANGED de origem**. Esse sinalizador indica uma alteração de formato no arquivo de origem. Os arquivos WAVE não dão suporte a alterações de formato.
    -   **MF \_ \_READERF \_ ENDOFSTREAM de origem**. Esse sinalizador indica o fim do fluxo.
3.  Chama [**IMFSample:: ConvertToContiguousBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-converttocontiguousbuffer) para obter um ponteiro para um objeto de buffer.
4.  Chama [**IMFMediaBuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) para obter um ponteiro para a memória do buffer.
5.  Grava os dados de áudio no arquivo de saída.
6.  Chama [**IMFMediaBuffer:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) para desbloquear o objeto buffer.

A função divide o loop quando qualquer uma das seguintes ações ocorre:

-   O formato do fluxo é alterado.
-   O final do fluxo foi atingido.
-   A quantidade máxima de dados de áudio é gravada no arquivo de saída.
-   Ocorre um erro.

## <a name="finalize-the-file-header"></a>Finalizar o cabeçalho do arquivo

Os valores de tamanho que são armazenados no cabeçalho de onda não são conhecidos até que a função anterior seja concluída. O `FixUpChunkSizes` preenche esses valores:


```C++
//-------------------------------------------------------------------
// FixUpChunkSizes
//
// Writes the file-size information into the WAVE file header.
//
// WAVE files use the RIFF file format. Each RIFF chunk has a data
// size, and the RIFF header has a total file size.
//-------------------------------------------------------------------

HRESULT FixUpChunkSizes(
    HANDLE hFile,           // Output file.
    DWORD cbHeader,         // Size of the 'fmt ' chuck.
    DWORD cbAudioData       // Size of the 'data' chunk.
    )
{
    HRESULT hr = S_OK;

    LARGE_INTEGER ll;
    ll.QuadPart = cbHeader - sizeof(DWORD);

    if (0 == SetFilePointerEx(hFile, ll, NULL, FILE_BEGIN))
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
    }

    // Write the data size.

    if (SUCCEEDED(hr))
    {
        hr = WriteToFile(hFile, &cbAudioData, sizeof(cbAudioData));
    }

    if (SUCCEEDED(hr))
    {
        // Write the file size.
        ll.QuadPart = sizeof(FOURCC);

        if (0 == SetFilePointerEx(hFile, ll, NULL, FILE_BEGIN))
        {
            hr = HRESULT_FROM_WIN32(GetLastError());
        }
    }

    if (SUCCEEDED(hr))
    {
        DWORD cbRiffFileSize = cbHeader + cbAudioData - 8;

        // NOTE: The "size" field in the RIFF header does not include
        // the first 8 bytes of the file. (That is, the size of the
        // data that appears after the size field.)

        hr = WriteToFile(hFile, &cbRiffFileSize, sizeof(cbRiffFileSize));
    }

    return hr;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de mídia de áudio](audio-media-types.md)
</dt> <dt>

[Leitor de origem](source-reader.md)
</dt> <dt>

[**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader)
</dt> </dl>

 

 
