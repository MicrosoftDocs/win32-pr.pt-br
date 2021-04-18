---
description: Uma maneira de criar um arquivo ASF é copiar fluxos ASF de um arquivo existente.
ms.assetid: 158fe3a1-42e6-461d-b56b-5419cd961fca
title: 'Tutorial: copiando fluxos ASF usando objetos WMContainer'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44bac13626a8c80f474eeb029db4eb1351273910
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105790498"
---
# <a name="tutorial-copying-asf-streams-by-using-wmcontainer-objects"></a><span data-ttu-id="e15dd-103">Tutorial: copiando fluxos ASF usando objetos WMContainer</span><span class="sxs-lookup"><span data-stu-id="e15dd-103">Tutorial: Copying ASF Streams by Using WMContainer Objects</span></span>

<span data-ttu-id="e15dd-104">Uma maneira de criar um arquivo ASF é copiar fluxos ASF de um arquivo existente.</span><span class="sxs-lookup"><span data-stu-id="e15dd-104">One way to create an ASF file is to copy ASF streams from an existing file.</span></span> <span data-ttu-id="e15dd-105">Para fazer isso, você pode recuperar os dados de mídia do arquivo de origem e gravar no arquivo de saída.</span><span class="sxs-lookup"><span data-stu-id="e15dd-105">To do this, you can retrieve the media data from the source file and write to the output file.</span></span> <span data-ttu-id="e15dd-106">Se o arquivo de origem for um arquivo ASF, você poderá copiar amostras de fluxo sem descompactá-los e recompactá-los.</span><span class="sxs-lookup"><span data-stu-id="e15dd-106">If the source file is an ASF file, you can copy stream samples without decompressing and recompressing them.</span></span>

<span data-ttu-id="e15dd-107">Este tutorial demonstra esse cenário extraindo o primeiro fluxo de áudio de um arquivo de vídeo de áudio ASF (. wmv) e copiando-o para um novo arquivo de áudio ASF (. WMA).</span><span class="sxs-lookup"><span data-stu-id="e15dd-107">This tutorial demonstrates this scenario by extracting the first audio stream from an ASF audio-video file (.wmv) and copying it to a new ASF audio file (.wma).</span></span> <span data-ttu-id="e15dd-108">Neste tutorial, você criará um aplicativo de console que usa os nomes de dados de entrada e saída como argumentos.</span><span class="sxs-lookup"><span data-stu-id="e15dd-108">In this tutorial, you will create a console application that takes the input and output filenames as arguments.</span></span> <span data-ttu-id="e15dd-109">O aplicativo usa o divisor de ASF para analisar os exemplos de fluxo de entrada e, em seguida, os envia para o multiplexador de ASF para gravar os pacotes de dados ASF para o fluxo de áudio.</span><span class="sxs-lookup"><span data-stu-id="e15dd-109">The application uses the ASF Splitter to parse the input stream samples and then sends them to the ASF Multiplexer to write the ASF data packets for the audio stream.</span></span>

<span data-ttu-id="e15dd-110">Este tutorial contém as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="e15dd-110">This tutorial contains the following steps:</span></span>

-   [<span data-ttu-id="e15dd-111">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="e15dd-111">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="e15dd-112">Terminologia</span><span class="sxs-lookup"><span data-stu-id="e15dd-112">Terminology</span></span>](#terminology)
-   [<span data-ttu-id="e15dd-113">1. configurar o projeto</span><span class="sxs-lookup"><span data-stu-id="e15dd-113">1. Set up the Project</span></span>](#1-set-up-the-project)
-   [<span data-ttu-id="e15dd-114">2. declarar funções auxiliares</span><span class="sxs-lookup"><span data-stu-id="e15dd-114">2. Declare Helper Functions</span></span>](#2-declare-helper-functions)
-   [<span data-ttu-id="e15dd-115">3. abrir o arquivo ASF de entrada</span><span class="sxs-lookup"><span data-stu-id="e15dd-115">3. Open the Input ASF File</span></span>](#3-open-the-input-asf-file)
-   [<span data-ttu-id="e15dd-116">4. inicializar objetos para o arquivo de entrada</span><span class="sxs-lookup"><span data-stu-id="e15dd-116">4. Initialize Objects for the Input File</span></span>](#4-initialize-objects-for-the-input-file)
-   [<span data-ttu-id="e15dd-117">5. criar um perfil de áudio</span><span class="sxs-lookup"><span data-stu-id="e15dd-117">5. Create an Audio Profile</span></span>](#5-create-an-audio-profile)
-   [<span data-ttu-id="e15dd-118">6. inicializar objetos para o arquivo de saída</span><span class="sxs-lookup"><span data-stu-id="e15dd-118">6. Initialize Objects for the Output File</span></span>](#6-initialize-objects-for-the-output-file)
-   [<span data-ttu-id="e15dd-119">7. gerar novos pacotes de dados ASF</span><span class="sxs-lookup"><span data-stu-id="e15dd-119">7. Generate New ASF Data Packets</span></span>](#7-generate-new-asf-data-packets)
-   [<span data-ttu-id="e15dd-120">8. gravar os objetos ASF no novo arquivo</span><span class="sxs-lookup"><span data-stu-id="e15dd-120">8. Write the ASF Objects in the New File</span></span>](#8-write-the-asf-objects-in-the-new-file)
-   [<span data-ttu-id="e15dd-121">9 gravar a função Entry-Point</span><span class="sxs-lookup"><span data-stu-id="e15dd-121">9 Write the Entry-Point Function</span></span>](#9-write-the-entry-point-function)
-   [<span data-ttu-id="e15dd-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e15dd-122">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="e15dd-123">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="e15dd-123">Prerequisites</span></span>

<span data-ttu-id="e15dd-124">Este tutorial pressupõe o seguinte:</span><span class="sxs-lookup"><span data-stu-id="e15dd-124">This tutorial assumes the following:</span></span>

-   <span data-ttu-id="e15dd-125">Você está familiarizado com a estrutura de um arquivo ASF e os componentes fornecidos pelo Media Foundation para trabalhar com objetos ASF.</span><span class="sxs-lookup"><span data-stu-id="e15dd-125">You are familiar with the structure of an ASF file and the components provided by Media Foundation to work with ASF Objects.</span></span> <span data-ttu-id="e15dd-126">Esses componentes incluem ContentInfo, Splitter, multiplexador e objetos de perfil.</span><span class="sxs-lookup"><span data-stu-id="e15dd-126">These components include ContentInfo, splitter, multiplexer, and profile objects.</span></span> <span data-ttu-id="e15dd-127">Para obter mais informações, consulte [componentes ASF do WMContainer](wmcontainer-asf-components.md).</span><span class="sxs-lookup"><span data-stu-id="e15dd-127">For more information, see [WMContainer ASF Components](wmcontainer-asf-components.md).</span></span>
-   <span data-ttu-id="e15dd-128">Você está familiarizado com o processo de análise do objeto de cabeçalho ASF e dos pacotes de dados ASF de um arquivo existente e geração de amostras de fluxo compactados usando o divisor.</span><span class="sxs-lookup"><span data-stu-id="e15dd-128">You are familiar with the process of parsing the ASF Header Object and the ASF data packets of an existing file and generating compressed stream samples by using the splitter.</span></span> <span data-ttu-id="e15dd-129">Para obter mais informações, consulte [tutorial: lendo um arquivo ASF](tutorial--reading-an-asf-file.md).</span><span class="sxs-lookup"><span data-stu-id="e15dd-129">For more information see [Tutorial: Reading an ASF File](tutorial--reading-an-asf-file.md).</span></span>
-   <span data-ttu-id="e15dd-130">Você está familiarizado com buffers de mídia e fluxos de bytes: especificamente, operações de arquivo usando um fluxo de bytes e gravando o conteúdo de um buffer de mídia em um fluxo de bytes.</span><span class="sxs-lookup"><span data-stu-id="e15dd-130">You are familiar with media buffers and byte streams: Specifically, file operations using a byte stream, and writing the contents of a media buffer into a byte stream.</span></span> <span data-ttu-id="e15dd-131">(Consulte [2. Declarar funções auxiliares](#2-declare-helper-functions).)</span><span class="sxs-lookup"><span data-stu-id="e15dd-131">(See [2. Declare Helper Functions](#2-declare-helper-functions).)</span></span>

## <a name="terminology"></a><span data-ttu-id="e15dd-132">Terminologia</span><span class="sxs-lookup"><span data-stu-id="e15dd-132">Terminology</span></span>

<span data-ttu-id="e15dd-133">Este tutorial usa os seguintes termos:</span><span class="sxs-lookup"><span data-stu-id="e15dd-133">This tutorial uses the following terms:</span></span>

-   <span data-ttu-id="e15dd-134">Fluxo de bytes de origem: o objeto de fluxo de bytes, expõe a interface [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) , que contém o conteúdo do arquivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="e15dd-134">Source byte stream: Byte stream object, exposes [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) interface, which contains the contents of the input file.</span></span>
-   <span data-ttu-id="e15dd-135">Objeto ContentInfo de origem: objeto ContentInfo, expõe a interface [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) , que representa o objeto de cabeçalho ASF do arquivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="e15dd-135">Source ContentInfo object: ContentInfo object, exposes [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) interface, which represents the ASF Header Object of the input file.</span></span>
-   <span data-ttu-id="e15dd-136">Perfil de áudio: objeto de perfil, expõe a interface [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) , que contém somente fluxos de áudio do arquivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="e15dd-136">Audio profile: Profile object, exposes [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) interface, which contains only audio streams of the input file.</span></span>
-   <span data-ttu-id="e15dd-137">Exemplo de fluxo: a amostra de mídia, expõe a interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , gerada pelo separador representa os dados de mídia do fluxo selecionado obtidos do arquivo de entrada no estado compactado.</span><span class="sxs-lookup"><span data-stu-id="e15dd-137">Stream sample: Media sample, exposes [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface, generated by the splitter represents the selected stream's media data obtained from the input file in compressed state.</span></span>
-   <span data-ttu-id="e15dd-138">Objeto ContentInfo de saída: objeto ContentInfo, expõe a interface [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) , que representa o objeto de cabeçalho ASF do arquivo de saída.</span><span class="sxs-lookup"><span data-stu-id="e15dd-138">Output ContentInfo object: ContentInfo object, exposes [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) interface, which represents the ASF Header Object of the output file.</span></span>
-   <span data-ttu-id="e15dd-139">Fluxo de bytes de dados: o objeto de fluxo de bytes, expõe a interface [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) , que representa a parte inteira do objeto de dados ASF do arquivo de saída.</span><span class="sxs-lookup"><span data-stu-id="e15dd-139">Data byte stream: Byte stream object, exposes [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) interface, which represents the entire ASF Data Object portion of the output file.</span></span>
-   <span data-ttu-id="e15dd-140">Pacote de dados: a amostra de mídia, expõe a interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , gerada pelo multiplexador representa um pacote de dados ASF que será gravado no fluxo de bytes de dados.</span><span class="sxs-lookup"><span data-stu-id="e15dd-140">Data packet: Media sample, exposes [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface, generated by the multiplexer represents an ASF data packet that will be written to the data byte stream.</span></span>
-   <span data-ttu-id="e15dd-141">Fluxo de bytes de saída: objeto de fluxo de bytes, expõe a interface [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) , que contém o conteúdo do arquivo de saída.</span><span class="sxs-lookup"><span data-stu-id="e15dd-141">Output byte stream: Byte stream object, exposes [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) interface, which contains the contents of the output file.</span></span>

## <a name="1-set-up-the-project"></a><span data-ttu-id="e15dd-142">1. configurar o projeto</span><span class="sxs-lookup"><span data-stu-id="e15dd-142">1. Set up the Project</span></span>

<span data-ttu-id="e15dd-143">Inclua os seguintes cabeçalhos no arquivo de origem:</span><span class="sxs-lookup"><span data-stu-id="e15dd-143">Include the following headers in your source file:</span></span>


```C++
#include <stdio.h>       // Standard I/O
#include <windows.h>     // Windows headers
#include <mfapi.h>       // Media Foundation platform
#include <wmcontainer.h> // ASF interfaces
#include <mferror.h>     // Media Foundation error codes
```



<span data-ttu-id="e15dd-144">Link para os seguintes arquivos de biblioteca:</span><span class="sxs-lookup"><span data-stu-id="e15dd-144">Link to the following library files:</span></span>

-   <span data-ttu-id="e15dd-145">mfplat. lib</span><span class="sxs-lookup"><span data-stu-id="e15dd-145">mfplat.lib</span></span>
-   <span data-ttu-id="e15dd-146">MF. lib</span><span class="sxs-lookup"><span data-stu-id="e15dd-146">mf.lib</span></span>
-   <span data-ttu-id="e15dd-147">mfuuid. lib</span><span class="sxs-lookup"><span data-stu-id="e15dd-147">mfuuid.lib</span></span>

<span data-ttu-id="e15dd-148">Declare a função [SafeRelease](saferelease.md) :</span><span class="sxs-lookup"><span data-stu-id="e15dd-148">Declare the [SafeRelease](saferelease.md) function:</span></span>


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



## <a name="2-declare-helper-functions"></a><span data-ttu-id="e15dd-149">2. declarar funções auxiliares</span><span class="sxs-lookup"><span data-stu-id="e15dd-149">2. Declare Helper Functions</span></span>

<span data-ttu-id="e15dd-150">Este tutorial usa as seguintes funções auxiliares para ler e gravar a partir de um fluxo de bytes.</span><span class="sxs-lookup"><span data-stu-id="e15dd-150">This tutorial uses the following helper functions to read and write from a byte stream.</span></span>

<span data-ttu-id="e15dd-151">A `AllocReadFromByteStream` função lê dados de um fluxo de bytes e aloca um novo buffer de mídia para manter os dados.</span><span class="sxs-lookup"><span data-stu-id="e15dd-151">The `AllocReadFromByteStream` function reads data from a byte stream and allocates a new media buffer to hold the data.</span></span> <span data-ttu-id="e15dd-152">Para obter mais informações, consulte [**IMFByteStream:: Read**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-read).</span><span class="sxs-lookup"><span data-stu-id="e15dd-152">For more information, see [**IMFByteStream::Read**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-read).</span></span>


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



<span data-ttu-id="e15dd-153">A `WriteBufferToByteStream` função grava dados de um buffer de mídia em um fluxo de bytes.</span><span class="sxs-lookup"><span data-stu-id="e15dd-153">The `WriteBufferToByteStream` function writes data from a media buffer to a byte stream.</span></span> <span data-ttu-id="e15dd-154">Para obter mais informações, consulte [**IMFByteStream:: Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write).</span><span class="sxs-lookup"><span data-stu-id="e15dd-154">For more information, see [**IMFByteStream::Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write).</span></span>


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



<span data-ttu-id="e15dd-155">A `AppendToByteStream` função acrescenta o conteúdo de um fluxo de bytes para outro:</span><span class="sxs-lookup"><span data-stu-id="e15dd-155">The `AppendToByteStream` function appends the contents of one byte stream to another:</span></span>


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



## <a name="3-open-the-input-asf-file"></a><span data-ttu-id="e15dd-156">3. abrir o arquivo ASF de entrada</span><span class="sxs-lookup"><span data-stu-id="e15dd-156">3. Open the Input ASF File</span></span>

<span data-ttu-id="e15dd-157">Abra o arquivo de entrada chamando a função [**MFCreateFile**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatefile) .</span><span class="sxs-lookup"><span data-stu-id="e15dd-157">Open the input file by calling the [**MFCreateFile**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatefile) function.</span></span> <span data-ttu-id="e15dd-158">O método retorna um ponteiro para o objeto de fluxo de bytes que contém o conteúdo do arquivo.</span><span class="sxs-lookup"><span data-stu-id="e15dd-158">The method returns a pointer to the byte stream object that contains the contents of the file.</span></span> <span data-ttu-id="e15dd-159">O nome de arquivo é especificado pelo usuário por meio de argumentos de linha de comando do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e15dd-159">The filename is specified by the user through command line arguments of the application.</span></span>

<span data-ttu-id="e15dd-160">O código de exemplo a seguir usa um nome de arquivo e retorna um ponteiro para um objeto de fluxo de bytes que pode ser usado para ler o arquivo.</span><span class="sxs-lookup"><span data-stu-id="e15dd-160">The following example code takes a file name and returns a pointer to a byte stream object that can be used to read the file.</span></span>


```C++
        // Open the file.
        hr = MFCreateFile(MF_ACCESSMODE_READ, MF_OPENMODE_FAIL_IF_NOT_EXIST, 
            MF_FILEFLAGS_NONE, pszFileName, &pStream);
```



## <a name="4-initialize-objects-for-the-input-file"></a><span data-ttu-id="e15dd-161">4. inicializar objetos para o arquivo de entrada</span><span class="sxs-lookup"><span data-stu-id="e15dd-161">4. Initialize Objects for the Input File</span></span>

<span data-ttu-id="e15dd-162">Em seguida, você criará e inicializará o objeto ContentInfo de origem e o divisor para gerar amostras de fluxo.</span><span class="sxs-lookup"><span data-stu-id="e15dd-162">Next, you will create and initialize the source ContentInfo object and the splitter for generating stream samples.</span></span>

<span data-ttu-id="e15dd-163">Esse fluxo de bytes de origem criado na etapa 2 será usado para analisar o objeto de cabeçalho ASF e preencher o objeto ContentInfo de origem.</span><span class="sxs-lookup"><span data-stu-id="e15dd-163">This source byte stream created in step 2 will be used to parse the ASF Header Object and populate the source ContentInfo object.</span></span> <span data-ttu-id="e15dd-164">Esse objeto será usado para inicializar o divisor para facilitar a análise dos pacotes de dados ASF para o fluxo de áudio no arquivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="e15dd-164">This object will be used to initialize the splitter to facilitate the parsing of the ASF data packets for the audio stream in the input file.</span></span> <span data-ttu-id="e15dd-165">Você também irá recuperar o comprimento do objeto de dados ASF no arquivo de entrada e o deslocamento para o primeiro pacote de dados ASF relativo ao início do arquivo.</span><span class="sxs-lookup"><span data-stu-id="e15dd-165">You will also retrieve the length of the ASF Data Object in the input file and the offset to the first ASF data packet relative to the start of the file.</span></span> <span data-ttu-id="e15dd-166">Esses atributos serão usados pelo divisor para gerar amostras de fluxo de áudio.</span><span class="sxs-lookup"><span data-stu-id="e15dd-166">These attributes will be used by the splitter to generate audio stream samples.</span></span>

<span data-ttu-id="e15dd-167">Para criar e inicializar os componentes do ASF para o arquivo de entrada:</span><span class="sxs-lookup"><span data-stu-id="e15dd-167">To create and initialize ASF components for the input file:</span></span>

1.  <span data-ttu-id="e15dd-168">Chame [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) para criar o objeto ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="e15dd-168">Call [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) to create the ContentInfo object.</span></span> <span data-ttu-id="e15dd-169">Essa função retorna um ponteiro para a interface [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) .</span><span class="sxs-lookup"><span data-stu-id="e15dd-169">This function returns a pointer to the [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) interface.</span></span>
2.  <span data-ttu-id="e15dd-170">Chame [**IMFASFContentInfo::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) para analisar o cabeçalho ASF.</span><span class="sxs-lookup"><span data-stu-id="e15dd-170">Call [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) to parse the ASF Header.</span></span> <span data-ttu-id="e15dd-171">Para obter mais informações sobre essa etapa, consulte [lendo o objeto de cabeçalho ASF de um arquivo existente](reading-the-asf-header-object-of-an-existing-file.md).</span><span class="sxs-lookup"><span data-stu-id="e15dd-171">For more information about this step, see [Reading the ASF Header Object of an Existing File](reading-the-asf-header-object-of-an-existing-file.md).</span></span>
3.  <span data-ttu-id="e15dd-172">Chame [**MFCreateASFSplitter**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) para criar o objeto divisor de ASF.</span><span class="sxs-lookup"><span data-stu-id="e15dd-172">Call [**MFCreateASFSplitter**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) to create the ASF splitter object.</span></span> <span data-ttu-id="e15dd-173">Essa função retorna um ponteiro para a interface [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) .</span><span class="sxs-lookup"><span data-stu-id="e15dd-173">This function returns a pointer to the [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) interface.</span></span>
4.  <span data-ttu-id="e15dd-174">Chame [**IMFASFSplitter:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize), passando o ponteiro [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo).</span><span class="sxs-lookup"><span data-stu-id="e15dd-174">Call [**IMFASFSplitter::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize), passing in the [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo)pointer.</span></span> <span data-ttu-id="e15dd-175">Para obter mais informações sobre esta etapa, consulte [Creating the ASF Splitter Object](creating-the-asf-splitter-object.md).</span><span class="sxs-lookup"><span data-stu-id="e15dd-175">For more information about this step, see [Creating the ASF Splitter Object](creating-the-asf-splitter-object.md).</span></span>
5.  <span data-ttu-id="e15dd-176">Chame [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) para obter um descritor de apresentação para o arquivo asf.</span><span class="sxs-lookup"><span data-stu-id="e15dd-176">Call [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) to get a presentation descriptor for the ASF file.</span></span>
6.  <span data-ttu-id="e15dd-177">Obtenha o valor do atributo [**de \_ \_ deslocamento de \_ \_ início de \_ dados MF PD ASF**](mf-pd-asf-data-start-offset-attribute.md) do descritor de apresentação.</span><span class="sxs-lookup"><span data-stu-id="e15dd-177">Get the value of the [**MF\_PD\_ASF\_DATA\_START\_OFFSET**](mf-pd-asf-data-start-offset-attribute.md) attribute from the presentation descriptor.</span></span> <span data-ttu-id="e15dd-178">Esse valor é o local do objeto de dados ASF no arquivo, como um deslocamento de bytes a partir do início do arquivo.</span><span class="sxs-lookup"><span data-stu-id="e15dd-178">This value is the location of the ASF Data Object in the file, as a byte offset from the start of the file.</span></span>
7.  <span data-ttu-id="e15dd-179">Obtenha o valor do atributo [**de \_ \_ comprimento de \_ dados \_ MF PD ASF**](mf-pd-asf-data-length-attribute.md) do descritor de apresentação.</span><span class="sxs-lookup"><span data-stu-id="e15dd-179">Get the value of the [**MF\_PD\_ASF\_DATA\_LENGTH**](mf-pd-asf-data-length-attribute.md) attribute from the presentation descriptor.</span></span> <span data-ttu-id="e15dd-180">Esse valor é o tamanho total do objeto de dados ASF, em bytes.</span><span class="sxs-lookup"><span data-stu-id="e15dd-180">This value is the total size of the ASF Data Object, in bytes.</span></span> <span data-ttu-id="e15dd-181">Para obter mais informações, consulte [obtendo informações de objetos de cabeçalho ASF](getting-information-from-asf-header-objects.md).</span><span class="sxs-lookup"><span data-stu-id="e15dd-181">For more information, see [Getting Information from ASF Header Objects](getting-information-from-asf-header-objects.md).</span></span>

<span data-ttu-id="e15dd-182">O código de exemplo a seguir mostra uma função que consolida todas as etapas.</span><span class="sxs-lookup"><span data-stu-id="e15dd-182">The following example code shows a function that consolidates all of the steps.</span></span> <span data-ttu-id="e15dd-183">Essa função usa um ponteiro para o fluxo de bytes de origem e retorna ponteiros para o objeto ContentInfo de origem e para o divisor.</span><span class="sxs-lookup"><span data-stu-id="e15dd-183">This function takes a pointer to the source byte stream and returns pointers to the source ContentInfo object and the splitter.</span></span> <span data-ttu-id="e15dd-184">Além disso, ele recebe o comprimento e os deslocamentos para o objeto de dados ASF.</span><span class="sxs-lookup"><span data-stu-id="e15dd-184">Also, it receives the length and offsets to the ASF Data Object.</span></span>


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



## <a name="5-create-an-audio-profile"></a><span data-ttu-id="e15dd-185">5. criar um perfil de áudio</span><span class="sxs-lookup"><span data-stu-id="e15dd-185">5. Create an Audio Profile</span></span>

<span data-ttu-id="e15dd-186">Em seguida, você criará um objeto de perfil para o arquivo de entrada obtendo-o do objeto ContentInfo de origem.</span><span class="sxs-lookup"><span data-stu-id="e15dd-186">Next, you will create a profile object for the input file by obtaining it from the source ContentInfo object.</span></span> <span data-ttu-id="e15dd-187">Em seguida, você irá configurar o perfil para que ele contenha apenas os fluxos de áudio do arquivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="e15dd-187">You will then configure the profile so that it contains only the audio streams of the input file.</span></span> <span data-ttu-id="e15dd-188">Para fazer isso, enumere os fluxos e remova os fluxos de não áudio do perfil.</span><span class="sxs-lookup"><span data-stu-id="e15dd-188">To do this, enumerate the streams and remove non-audio streams from the profile.</span></span> <span data-ttu-id="e15dd-189">O objeto de perfil de áudio será usado posteriormente neste tutorial para inicializar o objeto ContentInfo de saída.</span><span class="sxs-lookup"><span data-stu-id="e15dd-189">The audio profile object will be used later in this tutorial to initialize the output ContentInfo object.</span></span>

<span data-ttu-id="e15dd-190">Para criar um perfil de áudio</span><span class="sxs-lookup"><span data-stu-id="e15dd-190">To create an audio profile</span></span>

1.  <span data-ttu-id="e15dd-191">Obtenha o objeto de perfil para o arquivo de entrada do objeto ContentInfo de origem chamando [**IMFASFContentInfo:: GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).</span><span class="sxs-lookup"><span data-stu-id="e15dd-191">Get the profile object for the input file from the source ContentInfo object by calling [**IMFASFContentInfo::GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).</span></span> <span data-ttu-id="e15dd-192">O método retorna um ponteiro para um objeto de perfil que contém todos os fluxos no arquivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="e15dd-192">The method returns a pointer to a profile object that contains all of the streams in the input file.</span></span> <span data-ttu-id="e15dd-193">Para obter mais informações, consulte [criando um perfil de ASF](creating-an-asf-profile.md).</span><span class="sxs-lookup"><span data-stu-id="e15dd-193">For more information see [Creating an ASF Profile](creating-an-asf-profile.md).</span></span>
2.  <span data-ttu-id="e15dd-194">Remova todos os objetos de exclusão mútua do perfil.</span><span class="sxs-lookup"><span data-stu-id="e15dd-194">Remove any mutual exclusion objects from the profile.</span></span> <span data-ttu-id="e15dd-195">Esta etapa é necessária porque os fluxos que não são de áudio serão removidos do perfil, o que pode invalidar os objetos de exclusão mútua.</span><span class="sxs-lookup"><span data-stu-id="e15dd-195">This step is required because non-audio streams will be removed from the profile, which could invalidate the mutual exclusion objects.</span></span>
3.  <span data-ttu-id="e15dd-196">Remova todos os fluxos de não áudio do perfil, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="e15dd-196">Remove all non-audio streams from the profile, as follows:</span></span>
    -   <span data-ttu-id="e15dd-197">Chame [**IMFASFProfile:: GetStreamCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount) para obter o número de fluxos.</span><span class="sxs-lookup"><span data-stu-id="e15dd-197">Call [**IMFASFProfile::GetStreamCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount) to get the number of streams.</span></span>
    -   <span data-ttu-id="e15dd-198">Em um loop, chame [**IMFASFProfile:: GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) para obter cada fluxo por índice.</span><span class="sxs-lookup"><span data-stu-id="e15dd-198">In a loop, call [**IMFASFProfile::GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) to get each stream by index.</span></span>
    -   <span data-ttu-id="e15dd-199">Chame [**IMFASFStreamConfig:: Getstreamtype**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getstreamtype) para obter o tipo de fluxo.</span><span class="sxs-lookup"><span data-stu-id="e15dd-199">Call [**IMFASFStreamConfig::GetStreamType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getstreamtype) to get the stream type.</span></span>
    -   <span data-ttu-id="e15dd-200">Para fluxos sem áudio, chame [**IMFASFProfile:: RemoveStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream) para remover o fluxo.</span><span class="sxs-lookup"><span data-stu-id="e15dd-200">For non-audio streams, call [**IMFASFProfile::RemoveStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream) to remove the stream.</span></span>
4.  <span data-ttu-id="e15dd-201">Armazene o número de fluxo do primeiro fluxo de áudio.</span><span class="sxs-lookup"><span data-stu-id="e15dd-201">Store the stream number of the first audio stream.</span></span> <span data-ttu-id="e15dd-202">Isso será selecionado no divisor para gerar amostras de fluxo.</span><span class="sxs-lookup"><span data-stu-id="e15dd-202">This will be selected on the splitter to generate stream samples.</span></span> <span data-ttu-id="e15dd-203">Se o número do fluxo for zero, o chamador poderá pressupor que não havia nenhum arquivo de fluxos de áudio.</span><span class="sxs-lookup"><span data-stu-id="e15dd-203">If the stream number is zero, the caller can assume that there were no audio streams file.</span></span>

<span data-ttu-id="e15dd-204">O código a seguir segue estas etapas:</span><span class="sxs-lookup"><span data-stu-id="e15dd-204">The following code these steps:</span></span>


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



<span data-ttu-id="e15dd-205">A `RemoveMutexes` função remove todos os objetos de exclusão mútua do perfil:</span><span class="sxs-lookup"><span data-stu-id="e15dd-205">The `RemoveMutexes` function removes any mutual exclusion objects from the profile:</span></span>


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



## <a name="6-initialize-objects-for-the-output-file"></a><span data-ttu-id="e15dd-206">6. inicializar objetos para o arquivo de saída</span><span class="sxs-lookup"><span data-stu-id="e15dd-206">6. Initialize Objects for the Output File</span></span>

<span data-ttu-id="e15dd-207">Em seguida, você criará o objeto ContentInfo de saída e o multiplexador para gerar pacotes de dados para o arquivo de saída.</span><span class="sxs-lookup"><span data-stu-id="e15dd-207">Next, you will create the output ContentInfo object and the multiplexer for generating data packets for the output file.</span></span>

<span data-ttu-id="e15dd-208">O perfil de áudio criado na etapa 4 será usado para preencher o objeto ContentInfo de saída.</span><span class="sxs-lookup"><span data-stu-id="e15dd-208">The audio profile created in step 4 will be used to populate the output ContentInfo object.</span></span> <span data-ttu-id="e15dd-209">Esse objeto contém informações como atributos de arquivo global e propriedades de fluxo.</span><span class="sxs-lookup"><span data-stu-id="e15dd-209">This object contains information such as global file attributes and stream properties.</span></span> <span data-ttu-id="e15dd-210">O objeto ContentInfo de saída será usado para inicializar o multiplexador que irá gerar pacotes de dados para o arquivo de saída.</span><span class="sxs-lookup"><span data-stu-id="e15dd-210">The output ContentInfo object will be used to initialize the multiplexer that will generate data packets for the output file.</span></span> <span data-ttu-id="e15dd-211">Depois que os pacotes de dados são gerados, o objeto ContentInfo deve ser atualizado para refletir os novos valores.</span><span class="sxs-lookup"><span data-stu-id="e15dd-211">After the data packets are generated, the ContentInfo object must be updated to reflect the new values.</span></span>

<span data-ttu-id="e15dd-212">Para criar e inicializar componentes do ASF para o arquivo de saída</span><span class="sxs-lookup"><span data-stu-id="e15dd-212">To create and initialize ASF components for the output file</span></span>

1.  <span data-ttu-id="e15dd-213">Crie um objeto ContentInfo vazio chamando [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) e popule-o com informações do perfil de áudio criado na etapa 3 chamando [**IMFASFContentInfo:: setprofile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile).</span><span class="sxs-lookup"><span data-stu-id="e15dd-213">Create an empty ContentInfo object by calling [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) and populate it with information from the audio profile created in step 3 by calling [**IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile).</span></span> <span data-ttu-id="e15dd-214">Para obter mais informações, consulte [inicializando o objeto ContentInfo de um novo arquivo ASF](initializing-the-contentinfo-object-of-a-new-asf-file.md).</span><span class="sxs-lookup"><span data-stu-id="e15dd-214">For more information, see [Initializing the ContentInfo Object of a New ASF File](initializing-the-contentinfo-object-of-a-new-asf-file.md).</span></span>
2.  <span data-ttu-id="e15dd-215">Crie e inicialize o objeto multiplexador usando o objeto ContentInfo de saída.</span><span class="sxs-lookup"><span data-stu-id="e15dd-215">Create and initialize the multiplexer object by using the output ContentInfo object.</span></span> <span data-ttu-id="e15dd-216">Para obter mais informações, consulte [criando o objeto multiplexador](creating-the-multiplexer-object.md).</span><span class="sxs-lookup"><span data-stu-id="e15dd-216">For more information, see [Creating the Multiplexer Object](creating-the-multiplexer-object.md).</span></span>

<span data-ttu-id="e15dd-217">O código de exemplo a seguir mostra uma função que consolida as etapas.</span><span class="sxs-lookup"><span data-stu-id="e15dd-217">The following example code shows a function that consolidates the steps.</span></span> <span data-ttu-id="e15dd-218">Essa função usa um ponteiro para um objeto de perfil e retorna ponteiros para o objeto ContentInfo de saída e o multiplexador.</span><span class="sxs-lookup"><span data-stu-id="e15dd-218">This function takes a pointer to a profile object and returns pointers to the output ContentInfo object and the multiplexer.</span></span>


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



## <a name="7-generate-new-asf-data-packets"></a><span data-ttu-id="e15dd-219">7. gerar novos pacotes de dados ASF</span><span class="sxs-lookup"><span data-stu-id="e15dd-219">7. Generate New ASF Data Packets</span></span>

<span data-ttu-id="e15dd-220">Em seguida, você vai gerar amostras de fluxo de áudio do fluxo de bytes de origem usando o divisor e enviá-los ao multiplexador para criar pacotes de dados ASF.</span><span class="sxs-lookup"><span data-stu-id="e15dd-220">Next, you will generate audio stream samples from the source byte stream by using the splitter and send them to the multiplexer to create ASF data packets.</span></span> <span data-ttu-id="e15dd-221">Esses pacotes de dados constituem o objeto de dados ASF final para o novo arquivo.</span><span class="sxs-lookup"><span data-stu-id="e15dd-221">These data packets will constitute the final ASF Data Object for the new file.</span></span>

<span data-ttu-id="e15dd-222">Para gerar amostras de fluxo de áudio</span><span class="sxs-lookup"><span data-stu-id="e15dd-222">To generate audio stream samples</span></span>

1.  <span data-ttu-id="e15dd-223">Selecione o primeiro fluxo de áudio no divisor chamando [**IMFASFSplitter:: SelectStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams).</span><span class="sxs-lookup"><span data-stu-id="e15dd-223">Select the first audio stream on the splitter by calling [**IMFASFSplitter::SelectStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams).</span></span>
2.  <span data-ttu-id="e15dd-224">Ler blocos de tamanho fixo de dados de mídia do fluxo de bytes de origem em um buffer de mídia.</span><span class="sxs-lookup"><span data-stu-id="e15dd-224">Read fixed-size blocks of media data from the source byte stream into a media buffer.</span></span>
3.  <span data-ttu-id="e15dd-225">Colete os exemplos de fluxo como amostras de mídia do divisor chamando [**IMFASFSplitter:: GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) em um loop, contanto que ele receba o \_ sinalizador ASF STATUSFLAGS \_ incompleto no parâmetro *pdwStatusFlags* .</span><span class="sxs-lookup"><span data-stu-id="e15dd-225">Collect the stream samples as media samples from the splitter by calling [**IMFASFSplitter::GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) in a loop as long as it receives the ASF\_STATUSFLAGS\_INCOMPLETE flag in the *pdwStatusFlags* parameter.</span></span> <span data-ttu-id="e15dd-226">Para obter mais informações, consulte Gerando amostras para pacotes de dados ASF "em [gerando amostras de fluxo de um objeto de dados ASF existente](generating-stream-samples-from-an-existing-asf-data-object.md).</span><span class="sxs-lookup"><span data-stu-id="e15dd-226">For more information, see Generating Samples for ASF Data Packets" in [Generating Stream Samples from an Existing ASF Data Object](generating-stream-samples-from-an-existing-asf-data-object.md).</span></span>
4.  <span data-ttu-id="e15dd-227">Para cada exemplo de mídia, chame [**IMFASFMultiplexer::P rocesssample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) para enviar o exemplo de mídia para o multiplexador.</span><span class="sxs-lookup"><span data-stu-id="e15dd-227">For each media sample, call [**IMFASFMultiplexer::ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) to send the media sample to the multiplexer.</span></span> <span data-ttu-id="e15dd-228">O multiplexador gera os pacotes de dados para o objeto de dados ASF.</span><span class="sxs-lookup"><span data-stu-id="e15dd-228">The multiplexer generates the data packets for the ASF Data Object.</span></span>
5.  <span data-ttu-id="e15dd-229">Grave o pacote de dados gerado pelo multiplexador no fluxo de bytes de dados.</span><span class="sxs-lookup"><span data-stu-id="e15dd-229">Write the data packet generated by the multiplexer to the data byte stream.</span></span>
6.  <span data-ttu-id="e15dd-230">Depois que todos os pacotes de dados tiverem sido gerados, chame [**IMFASFMultiplexer:: End**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end) para atualizar o objeto ContentInfo de saída com informações coletadas durante a geração de pacotes de dados ASF.</span><span class="sxs-lookup"><span data-stu-id="e15dd-230">After all the data packets have been generated, call [**IMFASFMultiplexer::End**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end) to update the output ContentInfo object with information collected during ASF data packet generation.</span></span>

<span data-ttu-id="e15dd-231">O código de exemplo a seguir gera amostras de fluxo do divisor de ASF e os envia para o multiplexador.</span><span class="sxs-lookup"><span data-stu-id="e15dd-231">The following example code generates stream samples from the ASF splitter and sends them to the multiplexer.</span></span> <span data-ttu-id="e15dd-232">O multiplexador gera pacotes de dados ASF e os grava em um fluxo.</span><span class="sxs-lookup"><span data-stu-id="e15dd-232">The multiplexer generates ASF data packets and writes it to a stream.</span></span>


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



<span data-ttu-id="e15dd-233">Para obter pacotes do divisor de ASF, o código anterior chama a `GetPacketsFromSplitter` função, mostrada aqui:</span><span class="sxs-lookup"><span data-stu-id="e15dd-233">To get packets from the ASF splitter, the previous code calls the `GetPacketsFromSplitter` function, shown here:</span></span>


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



<span data-ttu-id="e15dd-234">A `GenerateDataPackets` função obtém pacotes de dados do Multiplexador.</span><span class="sxs-lookup"><span data-stu-id="e15dd-234">The `GenerateDataPackets` function gets data packets from multiplexer.</span></span> <span data-ttu-id="e15dd-235">Para obter mais informações, consulte [obtendo pacotes de dados ASF](generating-new-asf-data-packets.md).</span><span class="sxs-lookup"><span data-stu-id="e15dd-235">For more information, see [Getting ASF Data Packets](generating-new-asf-data-packets.md).</span></span>


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



## <a name="8-write-the-asf-objects-in-the-new-file"></a><span data-ttu-id="e15dd-236">8. gravar os objetos ASF no novo arquivo</span><span class="sxs-lookup"><span data-stu-id="e15dd-236">8. Write the ASF Objects in the New File</span></span>

<span data-ttu-id="e15dd-237">Em seguida, você gravará o conteúdo do objeto ContentInfo de saída em um buffer de mídia chamando [**IMFASFContentInfo:: GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader).</span><span class="sxs-lookup"><span data-stu-id="e15dd-237">Next, you will write the contents of the output ContentInfo object to a media buffer by calling [**IMFASFContentInfo::GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader).</span></span> <span data-ttu-id="e15dd-238">Esse método converte os dados armazenados no objeto ContentInfo em dados binários no formato de objeto de cabeçalho ASF.</span><span class="sxs-lookup"><span data-stu-id="e15dd-238">This method converts data stored in the ContentInfo object into binary data in ASF Header Object format.</span></span> <span data-ttu-id="e15dd-239">Para obter mais informações, consulte [gerando um novo objeto de cabeçalho ASF](generating-a-new-asf-header-object.md).</span><span class="sxs-lookup"><span data-stu-id="e15dd-239">For more information, see [Generating a New ASF Header Object](generating-a-new-asf-header-object.md).</span></span>

<span data-ttu-id="e15dd-240">Depois que o novo objeto de cabeçalho ASF tiver sido gerado, grave o arquivo de saída gravando primeiro o objeto de cabeçalho no fluxo de bytes de saída criado na etapa 2 chamando a função auxiliar WriteBufferToByteStream.</span><span class="sxs-lookup"><span data-stu-id="e15dd-240">After the new ASF Header Object has been generated, write the output file by first writing the Header Object to the output byte stream created in step 2 by calling the helper function WriteBufferToByteStream.</span></span> <span data-ttu-id="e15dd-241">Siga o objeto de cabeçalho com o objeto de dados contido no fluxo de bytes de dados.</span><span class="sxs-lookup"><span data-stu-id="e15dd-241">Follow the Header Object with the Data Object contained in the data byte stream.</span></span> <span data-ttu-id="e15dd-242">O código de exemplo mostra uma função que transfere o conteúdo do fluxo de bytes de dados para o fluxo de bytes de saída.</span><span class="sxs-lookup"><span data-stu-id="e15dd-242">The example code shows a function that transfers contents of the data bytes stream to the output byte stream.</span></span>


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



## <a name="9-write-the-entry-point-function"></a><span data-ttu-id="e15dd-243">9 gravar a função Entry-Point</span><span class="sxs-lookup"><span data-stu-id="e15dd-243">9 Write the Entry-Point Function</span></span>

<span data-ttu-id="e15dd-244">Agora você pode colocar as etapas anteriores juntas em um aplicativo completo.</span><span class="sxs-lookup"><span data-stu-id="e15dd-244">Now you can put the previous steps together into a complete application.</span></span> <span data-ttu-id="e15dd-245">Antes de usar qualquer um dos objetos Media Foundation, inicialize a plataforma Media Foundation chamando [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup).</span><span class="sxs-lookup"><span data-stu-id="e15dd-245">Before using any of the Media Foundation objects, initialize the Media Foundation platform by calling [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup).</span></span> <span data-ttu-id="e15dd-246">Quando terminar, chame [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span><span class="sxs-lookup"><span data-stu-id="e15dd-246">When you are done, call [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span></span> <span data-ttu-id="e15dd-247">Para obter mais informações, consulte [inicializando Media Foundation](initializing-media-foundation.md).</span><span class="sxs-lookup"><span data-stu-id="e15dd-247">For more information, see [Initializing Media Foundation](initializing-media-foundation.md).</span></span>

<span data-ttu-id="e15dd-248">O código a seguir mostra o aplicativo de console completo.</span><span class="sxs-lookup"><span data-stu-id="e15dd-248">The following code shows the complete console application.</span></span> <span data-ttu-id="e15dd-249">O argumento de linha de comando especifica o nome do arquivo a ser convertido e o nome do novo arquivo de áudio.</span><span class="sxs-lookup"><span data-stu-id="e15dd-249">The command-line argument specifies the name of the file to convert and the name of the new audio file.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="e15dd-250">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e15dd-250">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e15dd-251">Componentes ASF WMContainer</span><span class="sxs-lookup"><span data-stu-id="e15dd-251">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> <dt>

[<span data-ttu-id="e15dd-252">Suporte a ASF no Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e15dd-252">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



