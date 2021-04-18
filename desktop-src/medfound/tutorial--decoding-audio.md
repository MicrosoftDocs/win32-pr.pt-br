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
# <a name="tutorial-decoding-audio"></a><span data-ttu-id="82780-103">Tutorial: decodificando áudio</span><span class="sxs-lookup"><span data-stu-id="82780-103">Tutorial: Decoding Audio</span></span>

<span data-ttu-id="82780-104">Este tutorial mostra como usar o [leitor de origem](source-reader.md) para decodificar áudio de um arquivo de mídia e gravar o áudio em um arquivo Wave.</span><span class="sxs-lookup"><span data-stu-id="82780-104">This tutorial shows how to use the [Source Reader](source-reader.md) to decode audio from a media file and write the audio to a WAVE file.</span></span> <span data-ttu-id="82780-105">O tutorial é baseado no exemplo de [clipe de áudio](audio-clip-sample.md) .</span><span class="sxs-lookup"><span data-stu-id="82780-105">The tutorial is based on the [Audio Clip](audio-clip-sample.md) sample.</span></span>

-   [<span data-ttu-id="82780-106">Visão geral</span><span class="sxs-lookup"><span data-stu-id="82780-106">Overview</span></span>](#overview)
-   [<span data-ttu-id="82780-107">Arquivos de cabeçalho e biblioteca</span><span class="sxs-lookup"><span data-stu-id="82780-107">Header and Library Files</span></span>](#header-and-library-files)
-   [<span data-ttu-id="82780-108">Implementar wmain</span><span class="sxs-lookup"><span data-stu-id="82780-108">Implement wmain</span></span>](#implement-wmain)
-   [<span data-ttu-id="82780-109">Gravar o arquivo WAVE</span><span class="sxs-lookup"><span data-stu-id="82780-109">Write the WAVE File</span></span>](#write-the-wave-file)
-   [<span data-ttu-id="82780-110">Configurar o leitor de origem</span><span class="sxs-lookup"><span data-stu-id="82780-110">Configure the Source Reader</span></span>](#configure-the-source-reader)
-   [<span data-ttu-id="82780-111">Gravar o cabeçalho do arquivo WAVE</span><span class="sxs-lookup"><span data-stu-id="82780-111">Write the WAVE File Header</span></span>](#write-the-wave-file-header)
-   [<span data-ttu-id="82780-112">Calcular o tamanho máximo dos dados</span><span class="sxs-lookup"><span data-stu-id="82780-112">Calculate the Maximum Data Size</span></span>](#calculate-the-maximum-data-size)
-   [<span data-ttu-id="82780-113">Decodificar o áudio</span><span class="sxs-lookup"><span data-stu-id="82780-113">Decode the Audio</span></span>](#decode-the-audio)
-   [<span data-ttu-id="82780-114">Finalizar o cabeçalho do arquivo</span><span class="sxs-lookup"><span data-stu-id="82780-114">Finalize the File Header</span></span>](#finalize-the-file-header)
-   [<span data-ttu-id="82780-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="82780-115">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="82780-116">Visão geral</span><span class="sxs-lookup"><span data-stu-id="82780-116">Overview</span></span>

<span data-ttu-id="82780-117">Neste tutorial, você criará um aplicativo de console que usa dois argumentos de linha de comando: o nome de um arquivo de entrada que contém um fluxo de áudio e o nome do arquivo de saída.</span><span class="sxs-lookup"><span data-stu-id="82780-117">In this tutorial, you will create a console application that takes two command-line arguments: The name of an input file that contains an audio stream, and the output file name.</span></span> <span data-ttu-id="82780-118">O aplicativo lê cinco segundos de dados de áudio do arquivo de entrada e grava o áudio no arquivo de saída como dados de onda.</span><span class="sxs-lookup"><span data-stu-id="82780-118">The application reads five seconds of audio data from the input file and writes the audio to the output file as WAVE data.</span></span>

<span data-ttu-id="82780-119">Para obter os dados de áudio decodificados, o aplicativo usa o objeto de leitor de origem.</span><span class="sxs-lookup"><span data-stu-id="82780-119">To get the decoded audio data, the application uses the source reader object.</span></span> <span data-ttu-id="82780-120">O leitor de origem expõe a interface [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) .</span><span class="sxs-lookup"><span data-stu-id="82780-120">The source reader exposes the [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) interface.</span></span> <span data-ttu-id="82780-121">Para gravar o áudio decodificado no arquivo WAVE, os aplicativos usam as funções de e/s do Windows.</span><span class="sxs-lookup"><span data-stu-id="82780-121">To write the decoded audio to the WAVE file, the applications uses Windows I/O functions.</span></span> <span data-ttu-id="82780-122">A imagem a seguir ilustra esse processo.</span><span class="sxs-lookup"><span data-stu-id="82780-122">The following image illustrates this process.</span></span>

![diagrama mostrando o leitor de origem que obtém os dados de áudio do arquivo de origem.](images/audio-clip-tutorial.gif)

<span data-ttu-id="82780-124">Em sua forma mais simples, um arquivo WAVE tem a seguinte estrutura:</span><span class="sxs-lookup"><span data-stu-id="82780-124">In its simplest form, a WAVE file has the following structure:</span></span>



| <span data-ttu-id="82780-125">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="82780-125">Data Type</span></span>                              | <span data-ttu-id="82780-126">Tamanho (Bytes)</span><span class="sxs-lookup"><span data-stu-id="82780-126">Size (Bytes)</span></span> | <span data-ttu-id="82780-127">Valor</span><span class="sxs-lookup"><span data-stu-id="82780-127">Value</span></span>                                                                 |
|----------------------------------------|--------------|-----------------------------------------------------------------------|
| <span data-ttu-id="82780-128">**FOURCC**</span><span class="sxs-lookup"><span data-stu-id="82780-128">**FOURCC**</span></span>                             | <span data-ttu-id="82780-129">4</span><span class="sxs-lookup"><span data-stu-id="82780-129">4</span></span>            | <span data-ttu-id="82780-130">METÁLICA</span><span class="sxs-lookup"><span data-stu-id="82780-130">'RIFF'</span></span>                                                                |
| <span data-ttu-id="82780-131">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="82780-131">**DWORD**</span></span>                              | <span data-ttu-id="82780-132">4</span><span class="sxs-lookup"><span data-stu-id="82780-132">4</span></span>            | <span data-ttu-id="82780-133">Tamanho total do arquivo, sem incluir os primeiros 8 bytes</span><span class="sxs-lookup"><span data-stu-id="82780-133">Total file size, not including the first 8 bytes</span></span>                      |
| <span data-ttu-id="82780-134">**FOURCC**</span><span class="sxs-lookup"><span data-stu-id="82780-134">**FOURCC**</span></span>                             | <span data-ttu-id="82780-135">4</span><span class="sxs-lookup"><span data-stu-id="82780-135">4</span></span>            | <span data-ttu-id="82780-136">ONDA</span><span class="sxs-lookup"><span data-stu-id="82780-136">'WAVE'</span></span>                                                                |
| <span data-ttu-id="82780-137">**FOURCC**</span><span class="sxs-lookup"><span data-stu-id="82780-137">**FOURCC**</span></span>                             | <span data-ttu-id="82780-138">4</span><span class="sxs-lookup"><span data-stu-id="82780-138">4</span></span>            | <span data-ttu-id="82780-139">fmt</span><span class="sxs-lookup"><span data-stu-id="82780-139">'fmt '</span></span>                                                                |
| <span data-ttu-id="82780-140">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="82780-140">**DWORD**</span></span>                              | <span data-ttu-id="82780-141">4</span><span class="sxs-lookup"><span data-stu-id="82780-141">4</span></span>            | <span data-ttu-id="82780-142">Tamanho dos dados de [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) a seguir.</span><span class="sxs-lookup"><span data-stu-id="82780-142">Size of the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) data that follows.</span></span> |
| <span data-ttu-id="82780-143">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="82780-143">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span></span> | <span data-ttu-id="82780-144">Varia</span><span class="sxs-lookup"><span data-stu-id="82780-144">Varies</span></span>       | <span data-ttu-id="82780-145">Cabeçalho do formato de áudio.</span><span class="sxs-lookup"><span data-stu-id="82780-145">Audio format header.</span></span>                                                  |
| <span data-ttu-id="82780-146">**FOURCC**</span><span class="sxs-lookup"><span data-stu-id="82780-146">**FOURCC**</span></span>                             | <span data-ttu-id="82780-147">4</span><span class="sxs-lookup"><span data-stu-id="82780-147">4</span></span>            | <span data-ttu-id="82780-148">dado</span><span class="sxs-lookup"><span data-stu-id="82780-148">'data'</span></span>                                                                |
| <span data-ttu-id="82780-149">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="82780-149">**DWORD**</span></span>                              | <span data-ttu-id="82780-150">4</span><span class="sxs-lookup"><span data-stu-id="82780-150">4</span></span>            | <span data-ttu-id="82780-151">Tamanho dos dados de áudio.</span><span class="sxs-lookup"><span data-stu-id="82780-151">Size of the audio data.</span></span>                                               |
| <span data-ttu-id="82780-152">**MINUCIOSA**\[\]</span><span class="sxs-lookup"><span data-stu-id="82780-152">**BYTE**\[\]</span></span>                           | <span data-ttu-id="82780-153">Varia</span><span class="sxs-lookup"><span data-stu-id="82780-153">Varies</span></span>       | <span data-ttu-id="82780-154">Dados de áudio.</span><span class="sxs-lookup"><span data-stu-id="82780-154">Audio data.</span></span>                                                           |



 

> [!Note]  
> <span data-ttu-id="82780-155">Um **FOURCC** é um **DWORD** formado pela concatenação de quatro caracteres ASCII.</span><span class="sxs-lookup"><span data-stu-id="82780-155">A **FOURCC** is a **DWORD** formed by concatenating four ASCII characters.</span></span>

 

<span data-ttu-id="82780-156">Essa estrutura básica pode ser estendida com a adição de metadados de arquivo e outras informações, que está além do escopo deste tutorial.</span><span class="sxs-lookup"><span data-stu-id="82780-156">This basic structure can be extended by adding file metadata and other information, which is beyond the scope of this tutorial.</span></span>

## <a name="header-and-library-files"></a><span data-ttu-id="82780-157">Arquivos de cabeçalho e biblioteca</span><span class="sxs-lookup"><span data-stu-id="82780-157">Header and Library Files</span></span>

<span data-ttu-id="82780-158">Inclua os seguintes arquivos de cabeçalho em seu projeto:</span><span class="sxs-lookup"><span data-stu-id="82780-158">Include the following header files in your project:</span></span>


```C++
#define WINVER _WIN32_WINNT_WIN7

#include <windows.h>
#include <mfapi.h>
#include <mfidl.h>
#include <mfreadwrite.h>
#include <stdio.h>
#include <mferror.h>
```



<span data-ttu-id="82780-159">Link para as seguintes bibliotecas:</span><span class="sxs-lookup"><span data-stu-id="82780-159">Link to the following libraries:</span></span>

-   <span data-ttu-id="82780-160">mfplat. lib</span><span class="sxs-lookup"><span data-stu-id="82780-160">mfplat.lib</span></span>
-   <span data-ttu-id="82780-161">mfreadwrite. lib</span><span class="sxs-lookup"><span data-stu-id="82780-161">mfreadwrite.lib</span></span>
-   <span data-ttu-id="82780-162">mfuuid. lib</span><span class="sxs-lookup"><span data-stu-id="82780-162">mfuuid.lib</span></span>

## <a name="implement-wmain"></a><span data-ttu-id="82780-163">Implementar wmain</span><span class="sxs-lookup"><span data-stu-id="82780-163">Implement wmain</span></span>

<span data-ttu-id="82780-164">O código a seguir mostra a função de ponto de entrada para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="82780-164">The following code shows the entry-point function for the application.</span></span>


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



<span data-ttu-id="82780-165">Essa função faz o seguinte:</span><span class="sxs-lookup"><span data-stu-id="82780-165">This function does the following:</span></span>

1.  <span data-ttu-id="82780-166">Chama [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) para inicializar a biblioteca com.</span><span class="sxs-lookup"><span data-stu-id="82780-166">Calls [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) to initialize the COM library.</span></span>
2.  <span data-ttu-id="82780-167">Chama [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) para inicializar a plataforma de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="82780-167">Calls [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) to initialize the Media Foundation platform.</span></span>
3.  <span data-ttu-id="82780-168">Chama [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl) para criar o leitor de origem.</span><span class="sxs-lookup"><span data-stu-id="82780-168">Calls [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl) to create the source reader.</span></span> <span data-ttu-id="82780-169">Essa função usa o nome do arquivo de entrada e recebe um ponteiro de interface [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) .</span><span class="sxs-lookup"><span data-stu-id="82780-169">This function takes the name of the input file and receives an [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) interface pointer.</span></span>
4.  <span data-ttu-id="82780-170">Cria o arquivo de saída chamando a função **CreateFile** , que retorna um identificador de arquivo.</span><span class="sxs-lookup"><span data-stu-id="82780-170">Creates the output file by calling the **CreateFile** function, which returns a file handle.</span></span>
5.  <span data-ttu-id="82780-171">Chama a função [WriteWavFile](#write-the-wave-file) definida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="82780-171">Calls the application-defined [WriteWavFile](#write-the-wave-file) function.</span></span> <span data-ttu-id="82780-172">Essa função decodifica o áudio e grava o arquivo WAVE.</span><span class="sxs-lookup"><span data-stu-id="82780-172">This function decodes the audio and writes the WAVE file.</span></span>
6.  <span data-ttu-id="82780-173">Libera o ponteiro [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) e o identificador de arquivo.</span><span class="sxs-lookup"><span data-stu-id="82780-173">Releases the [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) pointer and the file handle.</span></span>
7.  <span data-ttu-id="82780-174">Chama [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) para desligar a plataforma Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="82780-174">Calls [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) to shut down the Media Foundation platform.</span></span>
8.  <span data-ttu-id="82780-175">Chama [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) para liberar a biblioteca com.</span><span class="sxs-lookup"><span data-stu-id="82780-175">Calls [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) to release the COM library.</span></span>

## <a name="write-the-wave-file"></a><span data-ttu-id="82780-176">Gravar o arquivo WAVE</span><span class="sxs-lookup"><span data-stu-id="82780-176">Write the WAVE File</span></span>

<span data-ttu-id="82780-177">A maior parte do trabalho ocorre na `WriteWavFile` função, que é chamada de `wmain` .</span><span class="sxs-lookup"><span data-stu-id="82780-177">Most of the work happens in the `WriteWavFile` function, which is called from `wmain`.</span></span>


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



<span data-ttu-id="82780-178">Essa função chama uma série de outras funções definidas pelo aplicativo:</span><span class="sxs-lookup"><span data-stu-id="82780-178">This function calls a series of other application-defined functions:</span></span>

1.  <span data-ttu-id="82780-179">A função [ConfigureAudioStream](#configure-the-source-reader) Inicializa o leitor de origem.</span><span class="sxs-lookup"><span data-stu-id="82780-179">The [ConfigureAudioStream](#configure-the-source-reader) function initializes the source reader.</span></span> <span data-ttu-id="82780-180">Essa função recebe um ponteiro para a interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) , que é usada para obter uma descrição do formato de áudio decodificado, incluindo taxa de amostra, número de canais e profundidade de bits (bits por amostra).</span><span class="sxs-lookup"><span data-stu-id="82780-180">This function receives a pointer to the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface, which is used to get a description of the decoded audio format, including sample rate, number of channels, and bit depth (bits per sample).</span></span>
2.  <span data-ttu-id="82780-181">A função WriteWaveHeader grava a primeira parte do arquivo WAVE, incluindo o cabeçalho e o início da parte ' data '.</span><span class="sxs-lookup"><span data-stu-id="82780-181">The WriteWaveHeader function writes the first part of the WAVE file, including the header and the start of the 'data' chunk.</span></span>
3.  <span data-ttu-id="82780-182">A função CalculateMaxAudioDataSize calcula a quantidade máxima de áudio a ser gravada no arquivo, em bytes.</span><span class="sxs-lookup"><span data-stu-id="82780-182">The CalculateMaxAudioDataSize function calculates the maximum amount of audio to write to the file, in bytes.</span></span>
4.  <span data-ttu-id="82780-183">A função WriteWaveData grava os dados de áudio do PCM no arquivo.</span><span class="sxs-lookup"><span data-stu-id="82780-183">The WriteWaveData function writes the PCM audio data to the file.</span></span>
5.  <span data-ttu-id="82780-184">A função FixUpChunkSizes grava as informações de tamanho de arquivo que aparecem após os valores **FOURCC** ' riff ' e ' data ' no arquivo Wave.</span><span class="sxs-lookup"><span data-stu-id="82780-184">The FixUpChunkSizes function writes the file-size information that appears after the 'RIFF' and 'data' **FOURCC** values in the WAVE file.</span></span> <span data-ttu-id="82780-185">(Esses valores não são conhecidos até que sejam `WriteWaveData` concluídos.)</span><span class="sxs-lookup"><span data-stu-id="82780-185">(These values are not known until `WriteWaveData` completes.)</span></span>

<span data-ttu-id="82780-186">Essas funções são mostradas nas seções restantes deste tutorial.</span><span class="sxs-lookup"><span data-stu-id="82780-186">These functions are shown in the remaining sections of this tutorial.</span></span>

## <a name="configure-the-source-reader"></a><span data-ttu-id="82780-187">Configurar o leitor de origem</span><span class="sxs-lookup"><span data-stu-id="82780-187">Configure the Source Reader</span></span>

<span data-ttu-id="82780-188">A `ConfigureAudioStream` função configura o leitor de origem para decodificar o fluxo de áudio no arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="82780-188">The `ConfigureAudioStream` function configures the source reader to decode the audio stream in the source file.</span></span> <span data-ttu-id="82780-189">Ele também retorna informações sobre o formato do áudio decodificado.</span><span class="sxs-lookup"><span data-stu-id="82780-189">It also returns information about the format of the decoded audio.</span></span>

<span data-ttu-id="82780-190">No Media Foundation, os formatos de mídia são descritos usando objetos de *tipo de mídia* .</span><span class="sxs-lookup"><span data-stu-id="82780-190">In Media Foundation, media formats are described using *media type* objects.</span></span> <span data-ttu-id="82780-191">Um objeto de tipo de mídia expõe a interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) , que herda a interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="82780-191">A media type object exposes the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface, which inherits the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="82780-192">Essencialmente, um tipo de mídia é uma coleção de propriedades que descreve o formato.</span><span class="sxs-lookup"><span data-stu-id="82780-192">Essentially, a media type is a collection of properties that describe the format.</span></span> <span data-ttu-id="82780-193">Para obter mais informações, consulte [tipos de mídia](media-types.md).</span><span class="sxs-lookup"><span data-stu-id="82780-193">For more information, see [Media Types](media-types.md).</span></span>


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



<span data-ttu-id="82780-194">A `ConfigureAudioStream` função faz o seguinte:</span><span class="sxs-lookup"><span data-stu-id="82780-194">The `ConfigureAudioStream` function does the following:</span></span>

1.  <span data-ttu-id="82780-195">Chama o método [**IMFSourceReader:: SetStreamSelection**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setstreamselection) para selecionar o fluxo de áudio e anular a seleção de todos os outros fluxos.</span><span class="sxs-lookup"><span data-stu-id="82780-195">Calls the [**IMFSourceReader::SetStreamSelection**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setstreamselection) method to select the audio stream and deselect all other streams.</span></span> <span data-ttu-id="82780-196">Essa etapa pode melhorar o desempenho, pois impede que o leitor de origem mantenha em quadros de vídeo que o aplicativo não usa.</span><span class="sxs-lookup"><span data-stu-id="82780-196">This step can improve performance, because it prevents the source reader from holding onto video frames that the application does not use.</span></span>
2.  <span data-ttu-id="82780-197">Cria um tipo de mídia *parcial* que especifica o áudio PCM.</span><span class="sxs-lookup"><span data-stu-id="82780-197">Creates a *partial* media type that specifies PCM audio.</span></span> <span data-ttu-id="82780-198">A função cria o tipo parcial da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="82780-198">The function creates the partial type as follows:</span></span>
    1.  <span data-ttu-id="82780-199">Chama [**MFCreateMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype) para criar um objeto de tipo de mídia vazio.</span><span class="sxs-lookup"><span data-stu-id="82780-199">Calls [**MFCreateMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype) to create an empty media type object.</span></span>
    2.  <span data-ttu-id="82780-200">Define o atributo de [**\_ \_ \_ tipo principal MF MT**](mf-mt-major-type-attribute.md) como **MFMediaType \_ Audio**.</span><span class="sxs-lookup"><span data-stu-id="82780-200">Sets the [**MF\_MT\_MAJOR\_TYPE**](mf-mt-major-type-attribute.md) attribute to **MFMediaType\_Audio**.</span></span>
    3.  <span data-ttu-id="82780-201">Define o atributo de [**\_ \_ subtipo MF MT**](mf-mt-subtype-attribute.md) como **MFAudioFormat \_ PCM**.</span><span class="sxs-lookup"><span data-stu-id="82780-201">Sets the [**MF\_MT\_SUBTYPE**](mf-mt-subtype-attribute.md) attribute to **MFAudioFormat\_PCM**.</span></span>
3.  <span data-ttu-id="82780-202">Chama [**IMFSourceReader:: SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype) para definir o tipo parcial no leitor de origem.</span><span class="sxs-lookup"><span data-stu-id="82780-202">Calls [**IMFSourceReader::SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype) to set the partial type on the source reader.</span></span> <span data-ttu-id="82780-203">Se o arquivo de origem contiver áudio codificado, o leitor de origem carregará automaticamente o decodificador de áudio necessário.</span><span class="sxs-lookup"><span data-stu-id="82780-203">If the source file contains encoded audio, the source reader automatically loads the necessary audio decoder.</span></span>
4.  <span data-ttu-id="82780-204">Chama [**IMFSourceReader:: GetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) para obter o tipo de mídia PCM real.</span><span class="sxs-lookup"><span data-stu-id="82780-204">Calls [**IMFSourceReader::GetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) to get the actual PCM media type.</span></span> <span data-ttu-id="82780-205">Esse método retorna um tipo de mídia com todos os detalhes de formato preenchidos, como a taxa de amostra de áudio e o número de canais.</span><span class="sxs-lookup"><span data-stu-id="82780-205">This method returns a media type with all of the format details filled in, such as the audio sample rate and the number of channels.</span></span>
5.  <span data-ttu-id="82780-206">Chama [**IMFSourceReader:: SetStreamSelection**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setstreamselection) para habilitar o fluxo de áudio.</span><span class="sxs-lookup"><span data-stu-id="82780-206">Calls [**IMFSourceReader::SetStreamSelection**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setstreamselection) to enable the audio stream.</span></span>

## <a name="write-the-wave-file-header"></a><span data-ttu-id="82780-207">Gravar o cabeçalho do arquivo WAVE</span><span class="sxs-lookup"><span data-stu-id="82780-207">Write the WAVE File Header</span></span>

<span data-ttu-id="82780-208">A `WriteWaveHeader` função grava o cabeçalho do arquivo Wave.</span><span class="sxs-lookup"><span data-stu-id="82780-208">The `WriteWaveHeader` function writes the WAVE file header.</span></span>

<span data-ttu-id="82780-209">A única API Media Foundation chamada a partir dessa função é [**MFCreateWaveFormatExFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype), que converte o tipo de mídia em uma estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="82780-209">The only Media Foundation API called from this function is [**MFCreateWaveFormatExFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype), which converts the media type to a [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>


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



<span data-ttu-id="82780-210">A `WriteToFile` função é uma função auxiliar simples que encapsula a função **WriteFile** do Windows e retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="82780-210">The `WriteToFile` function is a simple helper function that wraps the Windows **WriteFile** function and returns an **HRESULT** value.</span></span>


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



## <a name="calculate-the-maximum-data-size"></a><span data-ttu-id="82780-211">Calcular o tamanho máximo dos dados</span><span class="sxs-lookup"><span data-stu-id="82780-211">Calculate the Maximum Data Size</span></span>

<span data-ttu-id="82780-212">Como o tamanho do arquivo é armazenado como um valor de 4 bytes no cabeçalho do arquivo, um arquivo WAVE é limitado a um tamanho máximo de 0xFFFFFFFF bytes – aproximadamente 4 GB.</span><span class="sxs-lookup"><span data-stu-id="82780-212">Because the file size is stored as a 4-byte value in the file header, a WAVE file is limited to a maximum size of 0xFFFFFFFF bytes—approximately 4 GB.</span></span> <span data-ttu-id="82780-213">Esse valor inclui o tamanho do cabeçalho do arquivo.</span><span class="sxs-lookup"><span data-stu-id="82780-213">This value includes the size of the file header.</span></span> <span data-ttu-id="82780-214">O áudio PCM tem uma taxa de bits constante, portanto, você pode calcular o tamanho máximo dos dados do formato de áudio, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="82780-214">PCM audio has a constant bit rate, so you can calculate the maximum data size from the audio format, as follows:</span></span>


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



<span data-ttu-id="82780-215">Para evitar quadros de áudio parciais, o tamanho é arredondado para o alinhamento de bloco, que é armazenado no atributo de [**\_ alinhamento de bloco de \_ áudio \_ \_ MF MT**](mf-mt-audio-block-alignment-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="82780-215">To avoid partial audio frames, the size is rounded to the block alignment, which is stored in the [**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**](mf-mt-audio-block-alignment-attribute.md) attribute.</span></span>

## <a name="decode-the-audio"></a><span data-ttu-id="82780-216">Decodificar o áudio</span><span class="sxs-lookup"><span data-stu-id="82780-216">Decode the Audio</span></span>

<span data-ttu-id="82780-217">A `WriteWaveData` função lê o áudio decodificado do arquivo de origem e grava no arquivo Wave.</span><span class="sxs-lookup"><span data-stu-id="82780-217">The `WriteWaveData` function reads decoded audio from the source file and writes to the WAVE file.</span></span>


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



<span data-ttu-id="82780-218">A `WriteWaveData` função faz o seguinte em um loop:</span><span class="sxs-lookup"><span data-stu-id="82780-218">The `WriteWaveData` function does the following in a loop:</span></span>

1.  <span data-ttu-id="82780-219">Chama [**IMFSourceReader:: ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) para ler áudio do arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="82780-219">Calls [**IMFSourceReader::ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) to read audio from the source file.</span></span> <span data-ttu-id="82780-220">O parâmetro *dwFlags* recebe um **ou** bit de sinalizações da enumeração de sinalizador de [**leitor de \_ origem \_ \_ MF**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_flag) .</span><span class="sxs-lookup"><span data-stu-id="82780-220">The *dwFlags* parameter receives a bitwise **OR** of flags from the [**MF\_SOURCE\_READER\_FLAG**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_flag) enumeration.</span></span> <span data-ttu-id="82780-221">O parâmetro *pSample* recebe um ponteiro para a interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , que é usada para acessar os dados de áudio.</span><span class="sxs-lookup"><span data-stu-id="82780-221">The *pSample* parameter receives a pointer to the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface, which is used to access the audio data.</span></span> <span data-ttu-id="82780-222">Em alguns casos, uma chamada para **ReadSample** não gera dados; nesse caso, o ponteiro **IMFSample** é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="82780-222">In some cases a call to **ReadSample** does not generate data, in which case the **IMFSample** pointer is **NULL**.</span></span>
2.  <span data-ttu-id="82780-223">Verifica *dwFlags* para os seguintes sinalizadores:</span><span class="sxs-lookup"><span data-stu-id="82780-223">Checks *dwFlags* for the following flags:</span></span>
    -   <span data-ttu-id="82780-224">**MF \_ \_READERF \_ CURRENTMEDIATYPECHANGED de origem**.</span><span class="sxs-lookup"><span data-stu-id="82780-224">**MF\_SOURCE\_READERF\_CURRENTMEDIATYPECHANGED**.</span></span> <span data-ttu-id="82780-225">Esse sinalizador indica uma alteração de formato no arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="82780-225">This flag indicates a format change in the source file.</span></span> <span data-ttu-id="82780-226">Os arquivos WAVE não dão suporte a alterações de formato.</span><span class="sxs-lookup"><span data-stu-id="82780-226">WAVE files do not support format changes.</span></span>
    -   <span data-ttu-id="82780-227">**MF \_ \_READERF \_ ENDOFSTREAM de origem**.</span><span class="sxs-lookup"><span data-stu-id="82780-227">**MF\_SOURCE\_READERF\_ENDOFSTREAM**.</span></span> <span data-ttu-id="82780-228">Esse sinalizador indica o fim do fluxo.</span><span class="sxs-lookup"><span data-stu-id="82780-228">This flag indicates the end of the stream.</span></span>
3.  <span data-ttu-id="82780-229">Chama [**IMFSample:: ConvertToContiguousBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-converttocontiguousbuffer) para obter um ponteiro para um objeto de buffer.</span><span class="sxs-lookup"><span data-stu-id="82780-229">Calls [**IMFSample::ConvertToContiguousBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-converttocontiguousbuffer) to get a pointer to a buffer object.</span></span>
4.  <span data-ttu-id="82780-230">Chama [**IMFMediaBuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) para obter um ponteiro para a memória do buffer.</span><span class="sxs-lookup"><span data-stu-id="82780-230">Calls [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) to get a pointer to the buffer memory.</span></span>
5.  <span data-ttu-id="82780-231">Grava os dados de áudio no arquivo de saída.</span><span class="sxs-lookup"><span data-stu-id="82780-231">Writes the audio data to the output file.</span></span>
6.  <span data-ttu-id="82780-232">Chama [**IMFMediaBuffer:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) para desbloquear o objeto buffer.</span><span class="sxs-lookup"><span data-stu-id="82780-232">Calls [**IMFMediaBuffer::Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) to unlock the buffer object.</span></span>

<span data-ttu-id="82780-233">A função divide o loop quando qualquer uma das seguintes ações ocorre:</span><span class="sxs-lookup"><span data-stu-id="82780-233">The function breaks out of the loop when any of the following occur:</span></span>

-   <span data-ttu-id="82780-234">O formato do fluxo é alterado.</span><span class="sxs-lookup"><span data-stu-id="82780-234">The stream format changes.</span></span>
-   <span data-ttu-id="82780-235">O final do fluxo foi atingido.</span><span class="sxs-lookup"><span data-stu-id="82780-235">The end of the stream is reached.</span></span>
-   <span data-ttu-id="82780-236">A quantidade máxima de dados de áudio é gravada no arquivo de saída.</span><span class="sxs-lookup"><span data-stu-id="82780-236">The maximum amount of audio data is written to the output file.</span></span>
-   <span data-ttu-id="82780-237">Ocorre um erro.</span><span class="sxs-lookup"><span data-stu-id="82780-237">An error occurs.</span></span>

## <a name="finalize-the-file-header"></a><span data-ttu-id="82780-238">Finalizar o cabeçalho do arquivo</span><span class="sxs-lookup"><span data-stu-id="82780-238">Finalize the File Header</span></span>

<span data-ttu-id="82780-239">Os valores de tamanho que são armazenados no cabeçalho de onda não são conhecidos até que a função anterior seja concluída.</span><span class="sxs-lookup"><span data-stu-id="82780-239">The size values that are stored in the WAVE header are not known until the previous function completes.</span></span> <span data-ttu-id="82780-240">O `FixUpChunkSizes` preenche esses valores:</span><span class="sxs-lookup"><span data-stu-id="82780-240">The `FixUpChunkSizes` fills in these values:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="82780-241">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="82780-241">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82780-242">Tipos de mídia de áudio</span><span class="sxs-lookup"><span data-stu-id="82780-242">Audio Media Types</span></span>](audio-media-types.md)
</dt> <dt>

[<span data-ttu-id="82780-243">Leitor de origem</span><span class="sxs-lookup"><span data-stu-id="82780-243">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="82780-244">**IMFSourceReader**</span><span class="sxs-lookup"><span data-stu-id="82780-244">**IMFSourceReader**</span></span>](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader)
</dt> </dl>

 

 
