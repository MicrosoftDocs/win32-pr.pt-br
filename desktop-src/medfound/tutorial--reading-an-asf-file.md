---
description: Este tutorial mostra como obter pacotes de dados de um arquivo ASF (Advanced Systems Format) usando o divisor de ASF.
ms.assetid: e3a55275-e8f0-4ab7-98db-a2f2c54d5a51
title: 'Tutorial: lendo um arquivo ASF usando objetos WMContainer'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0225f434f650f0423771122e6fc345022e69ec1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781159"
---
# <a name="tutorial-reading-an-asf-file-by-using-wmcontainer-objects"></a><span data-ttu-id="2ae85-103">Tutorial: lendo um arquivo ASF usando objetos WMContainer</span><span class="sxs-lookup"><span data-stu-id="2ae85-103">Tutorial: Reading an ASF File by Using WMContainer Objects</span></span>

<span data-ttu-id="2ae85-104">Este tutorial mostra como obter pacotes de dados de um arquivo ASF (Advanced Systems Format) usando o [divisor de ASF](asf-splitter.md).</span><span class="sxs-lookup"><span data-stu-id="2ae85-104">This tutorial shows how to get data packets from an Advanced Systems Format (ASF) file using the [ASF Splitter](asf-splitter.md).</span></span> <span data-ttu-id="2ae85-105">Neste tutorial, você criará um aplicativo de console simples que lê um arquivo ASF e gera amostras de mídia compactadas para o primeiro fluxo de vídeo no arquivo.</span><span class="sxs-lookup"><span data-stu-id="2ae85-105">In this tutorial, you will create a simple console application that reads an ASF file and generates compressed media samples for the first video stream in the file.</span></span> <span data-ttu-id="2ae85-106">O aplicativo exibe informações sobre os quadros-chave no fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="2ae85-106">The application displays information about the key frames in the video stream.</span></span>

<span data-ttu-id="2ae85-107">Este tutorial contém as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="2ae85-107">This tutorial contains the following steps:</span></span>

-   [<span data-ttu-id="2ae85-108">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="2ae85-108">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="2ae85-109">1. configurar o projeto</span><span class="sxs-lookup"><span data-stu-id="2ae85-109">1. Set up the Project</span></span>](#1-set-up-the-project)
-   [<span data-ttu-id="2ae85-110">2. abrir um arquivo ASF</span><span class="sxs-lookup"><span data-stu-id="2ae85-110">2. Open an ASF File</span></span>](#2-open-an-asf-file)
-   [<span data-ttu-id="2ae85-111">3. ler o objeto de cabeçalho ASF</span><span class="sxs-lookup"><span data-stu-id="2ae85-111">3. Read the ASF Header Object</span></span>](#3-read-the-asf-header-object)
-   [<span data-ttu-id="2ae85-112">4. criar o divisor de ASF</span><span class="sxs-lookup"><span data-stu-id="2ae85-112">4. Create the ASF Splitter</span></span>](#4-create-the-asf-splitter)
-   [<span data-ttu-id="2ae85-113">5. selecionar um fluxo para análise</span><span class="sxs-lookup"><span data-stu-id="2ae85-113">5. Select a Stream for Parsing</span></span>](#5-select-a-stream-for-parsing)
-   [<span data-ttu-id="2ae85-114">6. gerar amostras de mídia compactadas</span><span class="sxs-lookup"><span data-stu-id="2ae85-114">6. Generate Compressed Media Samples</span></span>](#6-generate-compressed-media-samples)
-   [<span data-ttu-id="2ae85-115">7. gravar a função Entry-Point</span><span class="sxs-lookup"><span data-stu-id="2ae85-115">7. Write the Entry-Point Function</span></span>](#7-write-the-entry-point-function)
-   [<span data-ttu-id="2ae85-116">Listagem de programas</span><span class="sxs-lookup"><span data-stu-id="2ae85-116">Program Listing</span></span>](#program-listing)
-   [<span data-ttu-id="2ae85-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2ae85-117">Related topics</span></span>](#related-topics)

<span data-ttu-id="2ae85-118">O tutorial não aborda como decodificar os dados compactados que o aplicativo obtém do divisor de ASF.</span><span class="sxs-lookup"><span data-stu-id="2ae85-118">The tutorial does not cover how to decode the compressed data that the application gets from the ASF splitter.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2ae85-119">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="2ae85-119">Prerequisites</span></span>

<span data-ttu-id="2ae85-120">Este tutorial pressupõe o seguinte:</span><span class="sxs-lookup"><span data-stu-id="2ae85-120">This tutorial assumes the following:</span></span>

-   <span data-ttu-id="2ae85-121">Você está familiarizado com a estrutura de um arquivo ASF e os componentes fornecidos pelo Media Foundation para trabalhar com objetos ASF.</span><span class="sxs-lookup"><span data-stu-id="2ae85-121">You are familiar with the structure of an ASF file and the components provided by Media Foundation to work with ASF Objects.</span></span> <span data-ttu-id="2ae85-122">Esses componentes incluem o objeto ContentInfo, o Splitter, o multiplexador e o perfil.</span><span class="sxs-lookup"><span data-stu-id="2ae85-122">These components include the ContentInfo object, splitter, multiplexer, and profile.</span></span> <span data-ttu-id="2ae85-123">Para obter mais informações, consulte [componentes ASF do WMContainer](wmcontainer-asf-components.md).</span><span class="sxs-lookup"><span data-stu-id="2ae85-123">For more information, see [WMContainer ASF Components](wmcontainer-asf-components.md).</span></span>
-   <span data-ttu-id="2ae85-124">Você está familiarizado com [buffers de mídia](media-buffers.md) e fluxos de bytes: especificamente, operações de arquivo usando um fluxo de bytes, lendo de um fluxo de bytes em um buffer de mídia e gravando o conteúdo de um buffer de mídia em um fluxo de bytes.</span><span class="sxs-lookup"><span data-stu-id="2ae85-124">You are familiar with [Media Buffers](media-buffers.md) and byte streams: Specifically, file operations using a byte stream, reading from a byte stream into a media buffer, and writing the contents of a media buffer to a byte stream.</span></span>

## <a name="1-set-up-the-project"></a><span data-ttu-id="2ae85-125">1. configurar o projeto</span><span class="sxs-lookup"><span data-stu-id="2ae85-125">1. Set up the Project</span></span>

<span data-ttu-id="2ae85-126">Inclua os seguintes cabeçalhos no arquivo de origem:</span><span class="sxs-lookup"><span data-stu-id="2ae85-126">Include the following headers in your source file:</span></span>


```C++
#include <stdio.h>       // Standard I/O
#include <windows.h>     // Windows headers
#include <mfapi.h>       // Media Foundation platform
#include <wmcontainer.h> // ASF interfaces
#include <Mferror.h>
```



<span data-ttu-id="2ae85-127">Link para os seguintes arquivos de biblioteca:</span><span class="sxs-lookup"><span data-stu-id="2ae85-127">Link to the following library files:</span></span>

-   <span data-ttu-id="2ae85-128">mfplat. lib</span><span class="sxs-lookup"><span data-stu-id="2ae85-128">mfplat.lib</span></span>
-   <span data-ttu-id="2ae85-129">MF. lib</span><span class="sxs-lookup"><span data-stu-id="2ae85-129">mf.lib</span></span>
-   <span data-ttu-id="2ae85-130">mfuuid. lib</span><span class="sxs-lookup"><span data-stu-id="2ae85-130">mfuuid.lib</span></span>

<span data-ttu-id="2ae85-131">Declare a função [SafeRelease](saferelease.md) :</span><span class="sxs-lookup"><span data-stu-id="2ae85-131">Declare the [SafeRelease](saferelease.md) function:</span></span>


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



## <a name="2-open-an-asf-file"></a><span data-ttu-id="2ae85-132">2. abrir um arquivo ASF</span><span class="sxs-lookup"><span data-stu-id="2ae85-132">2. Open an ASF File</span></span>

<span data-ttu-id="2ae85-133">Em seguida, abra o arquivo especificado chamando a função [**MFCreateFile**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatefile) .</span><span class="sxs-lookup"><span data-stu-id="2ae85-133">Next, open the specified file by calling the [**MFCreateFile**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatefile) function.</span></span> <span data-ttu-id="2ae85-134">O método retorna um ponteiro para o objeto de fluxo de bytes que contém o conteúdo do arquivo.</span><span class="sxs-lookup"><span data-stu-id="2ae85-134">The method returns a pointer to the byte stream object that contains the contents of the file.</span></span> <span data-ttu-id="2ae85-135">O nome de arquivo é especificado pelo usuário por meio de argumentos de linha de comando do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2ae85-135">The filename is specified by the user through command line arguments of the application.</span></span>

<span data-ttu-id="2ae85-136">O código de exemplo a seguir usa um nome de arquivo e retorna um ponteiro para um objeto de fluxo de bytes que pode ser usado para ler o arquivo.</span><span class="sxs-lookup"><span data-stu-id="2ae85-136">The following example code takes a file name and returns a pointer to a byte stream object that can be used to read the file.</span></span>


```C++
        // Open the file.
        hr = MFCreateFile(MF_ACCESSMODE_READ, MF_OPENMODE_FAIL_IF_NOT_EXIST, 
            MF_FILEFLAGS_NONE, pszFileName, &pStream);
```



## <a name="3-read-the-asf-header-object"></a><span data-ttu-id="2ae85-137">3. ler o objeto de cabeçalho ASF</span><span class="sxs-lookup"><span data-stu-id="2ae85-137">3. Read the ASF Header Object</span></span>

<span data-ttu-id="2ae85-138">Em seguida, crie o [objeto ContentInfo do ASF](asf-contentinfo-object.md) e use-o para analisar o objeto de cabeçalho ASF do arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="2ae85-138">Next, create the [ASF ContentInfo Object](asf-contentinfo-object.md) and use it to parse the ASF Header Object of the specified file.</span></span> <span data-ttu-id="2ae85-139">O objeto ContentInfo armazena informações do cabeçalho ASF, incluindo atributos de arquivo global e informações sobre cada fluxo.</span><span class="sxs-lookup"><span data-stu-id="2ae85-139">The ContentInfo object stores information from the ASF header, including global file attributes and information about each stream.</span></span> <span data-ttu-id="2ae85-140">Você usará o objeto ContentInfo posteriormente no tutorial para inicializar o divisor de ASF e obter o número de fluxo do fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="2ae85-140">You will use the ContentInfo object later in the tutorial to initialize the ASF splitter and get the stream number of the video stream.</span></span>

<span data-ttu-id="2ae85-141">Para criar o objeto ContentInfo do ASF:</span><span class="sxs-lookup"><span data-stu-id="2ae85-141">To create the ASF ContentInfo object:</span></span>

1.  <span data-ttu-id="2ae85-142">Chame a função [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) para criar um objeto ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="2ae85-142">Call the [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) function to create a ContentInfo object.</span></span> <span data-ttu-id="2ae85-143">O método retorna um ponteiro para a interface [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) .</span><span class="sxs-lookup"><span data-stu-id="2ae85-143">The method returns a pointer to the [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) interface.</span></span>
2.  <span data-ttu-id="2ae85-144">Leia os primeiros 30 bytes de dados do arquivo ASF em um buffer de mídia.</span><span class="sxs-lookup"><span data-stu-id="2ae85-144">Read the first 30 bytes of data from the ASF file into a media buffer.</span></span>
3.  <span data-ttu-id="2ae85-145">Passe o buffer de mídia para o método [**IMFASFContentInfo:: Getheadize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) .</span><span class="sxs-lookup"><span data-stu-id="2ae85-145">Pass the media buffer to the [**IMFASFContentInfo::GetHeaderSize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) method.</span></span> <span data-ttu-id="2ae85-146">Esse método retorna o tamanho total do objeto de cabeçalho no arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="2ae85-146">This method returns the total size of the Header Object in the ASF file.</span></span>
4.  <span data-ttu-id="2ae85-147">Passe o mesmo buffer de mídia para o método [**IMFASFContentInfo::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) .</span><span class="sxs-lookup"><span data-stu-id="2ae85-147">Pass the same media buffer to the [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) method.</span></span>
5.  <span data-ttu-id="2ae85-148">Leia o restante do objeto de cabeçalho em um novo buffer de mídia.</span><span class="sxs-lookup"><span data-stu-id="2ae85-148">Read the remainder of the Header Object into a new media buffer.</span></span>
6.  <span data-ttu-id="2ae85-149">Passe o segundo buffer para o método [**ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) .</span><span class="sxs-lookup"><span data-stu-id="2ae85-149">Pass the second buffer to the [**ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) method.</span></span> <span data-ttu-id="2ae85-150">Especifique o deslocamento de 30 bytes no parâmetro *cbOffsetWithinHeader* de **ParseHeader**.</span><span class="sxs-lookup"><span data-stu-id="2ae85-150">Specify the 30-byte offset in the *cbOffsetWithinHeader* parameter of **ParseHeader**.</span></span> <span data-ttu-id="2ae85-151">O método **ParseHeader** Inicializa o objeto ContentInfo com informações coletadas dos vários objetos ASF contidos no objeto header.</span><span class="sxs-lookup"><span data-stu-id="2ae85-151">The **ParseHeader** method initializes the ContentInfo object with information gathered from the various ASF objects contained in the Header Object.</span></span>


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



<span data-ttu-id="2ae85-152">Essa função usa a `ReadFromByteStream` função para ler de um fluxo de bytes em um buffer de mídia:</span><span class="sxs-lookup"><span data-stu-id="2ae85-152">This function uses the `ReadFromByteStream` function to read from a byte stream into a media buffer:</span></span>


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



## <a name="4-create-the-asf-splitter"></a><span data-ttu-id="2ae85-153">4. criar o divisor de ASF</span><span class="sxs-lookup"><span data-stu-id="2ae85-153">4. Create the ASF Splitter</span></span>

<span data-ttu-id="2ae85-154">Em seguida, crie o objeto [divisor de ASF](asf-splitter.md) .</span><span class="sxs-lookup"><span data-stu-id="2ae85-154">Next, create the [ASF Splitter](asf-splitter.md) object.</span></span> <span data-ttu-id="2ae85-155">Você usará o divisor de ASF para analisar o objeto de dados ASF, que contém dados de mídia em pacotes para o arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="2ae85-155">You will use the ASF splitter to parse the ASF Data Object, which contains packetized media data for the ASF file.</span></span>

<span data-ttu-id="2ae85-156">Para criar um objeto divisor para o arquivo ASF:</span><span class="sxs-lookup"><span data-stu-id="2ae85-156">To create a splitter object for the ASF File:</span></span>

1.  <span data-ttu-id="2ae85-157">Chame a função [**MFCreateASFSplitter**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) para criar o divisor de ASF.</span><span class="sxs-lookup"><span data-stu-id="2ae85-157">Call the [**MFCreateASFSplitter**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) function to create the ASF splitter.</span></span> <span data-ttu-id="2ae85-158">A função retorna um ponteiro para a interface [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) .</span><span class="sxs-lookup"><span data-stu-id="2ae85-158">The function returns a pointer to the [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) interface.</span></span>
2.  <span data-ttu-id="2ae85-159">Chame [**IMFASFSplitter:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) para inicializar o divisor de ASF.</span><span class="sxs-lookup"><span data-stu-id="2ae85-159">Call [**IMFASFSplitter::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) to initialize the ASF splitter.</span></span> <span data-ttu-id="2ae85-160">Esse método usa um ponteiro para o objeto ContentInfo, que foi criado no procedimento 3.</span><span class="sxs-lookup"><span data-stu-id="2ae85-160">This method takes a pointer to the ContentInfo object, which was created in procedure 3.</span></span>


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



## <a name="5-select-a-stream-for-parsing"></a><span data-ttu-id="2ae85-161">5. selecionar um fluxo para análise</span><span class="sxs-lookup"><span data-stu-id="2ae85-161">5. Select a Stream for Parsing</span></span>

<span data-ttu-id="2ae85-162">Em seguida, enumere os fluxos no arquivo ASF e selecione o primeiro fluxo de vídeo para análise.</span><span class="sxs-lookup"><span data-stu-id="2ae85-162">Next, enumerate the streams in the ASF file and select the first video stream for parsing.</span></span> <span data-ttu-id="2ae85-163">Para enumerar os fluxos, você usará um objeto de perfil ASF e pesquisará os fluxos que têm um tipo de mídia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="2ae85-163">To enumerate the streams, you will use an ASF profile object and search for streams that have a video media type.</span></span>

<span data-ttu-id="2ae85-164">Para selecionar o fluxo de vídeo:</span><span class="sxs-lookup"><span data-stu-id="2ae85-164">To select the video stream:</span></span>

1.  <span data-ttu-id="2ae85-165">Chame [**IMFASFContentInfo:: GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile) no objeto ContentInfo para criar um perfil de ASF.</span><span class="sxs-lookup"><span data-stu-id="2ae85-165">Call [**IMFASFContentInfo::GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile) on the ContentInfo object to create an ASF profile.</span></span> <span data-ttu-id="2ae85-166">Entre outras informações, o perfil descreve os fluxos no arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="2ae85-166">Among other information, the profile describes the streams in the ASF file.</span></span>
2.  <span data-ttu-id="2ae85-167">Chame [**IMFASFProfile:: GetStreamCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount) para obter o número de fluxos no arquivo asf.</span><span class="sxs-lookup"><span data-stu-id="2ae85-167">Call [**IMFASFProfile::GetStreamCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount) to get the number of streams in the ASF file.</span></span>
3.  <span data-ttu-id="2ae85-168">Chame [**IMFASFProfile:: GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) em um loop para enumerar os fluxos.</span><span class="sxs-lookup"><span data-stu-id="2ae85-168">Call [**IMFASFProfile::GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) in a loop to enumerate the streams.</span></span> <span data-ttu-id="2ae85-169">O método retorna um ponteiro para a interface [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) .</span><span class="sxs-lookup"><span data-stu-id="2ae85-169">The method returns a pointer to the [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) interface.</span></span> <span data-ttu-id="2ae85-170">Ele também retorna o identificador de fluxo.</span><span class="sxs-lookup"><span data-stu-id="2ae85-170">It also returns the stream identifier.</span></span>
4.  <span data-ttu-id="2ae85-171">Chame [**IMFASFStreamConfig:: Getstreamtype**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getstreamtype) para obter o GUID de tipo principal para o fluxo.</span><span class="sxs-lookup"><span data-stu-id="2ae85-171">Call [**IMFASFStreamConfig::GetStreamType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getstreamtype) to get the major type GUID for the stream.</span></span> <span data-ttu-id="2ae85-172">Se o GUID de tipo principal for MFMediaType \_ Video, o fluxo conterá vídeo.</span><span class="sxs-lookup"><span data-stu-id="2ae85-172">If the major type GUID is MFMediaType\_Video, the stream contains video.</span></span>
5.  <span data-ttu-id="2ae85-173">Se você encontrar um fluxo de vídeo na etapa 4, chame [**IMFASFSplitter:: SelectStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams) para selecionar o fluxo.</span><span class="sxs-lookup"><span data-stu-id="2ae85-173">If you found a video stream in step 4, call [**IMFASFSplitter::SelectStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams) to select the stream.</span></span> <span data-ttu-id="2ae85-174">Esse método usa uma matriz de identificadores de fluxo.</span><span class="sxs-lookup"><span data-stu-id="2ae85-174">This method takes an array of stream identifiers.</span></span> <span data-ttu-id="2ae85-175">Para este tutorial, o tamanho da matriz é 1 porque o aplicativo analisará um único fluxo.</span><span class="sxs-lookup"><span data-stu-id="2ae85-175">For this tutorial, the array size is 1 because the application will parse a single stream.</span></span>

<span data-ttu-id="2ae85-176">O código de exemplo a seguir enumera os fluxos no arquivo ASF e seleciona o primeiro fluxo de vídeo no divisor de ASF:</span><span class="sxs-lookup"><span data-stu-id="2ae85-176">The following example code enumerates the streams in the ASF file and selects the first video stream on the ASF splitter:</span></span>


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



## <a name="6-generate-compressed-media-samples"></a><span data-ttu-id="2ae85-177">6. gerar amostras de mídia compactadas</span><span class="sxs-lookup"><span data-stu-id="2ae85-177">6. Generate Compressed Media Samples</span></span>

<span data-ttu-id="2ae85-178">Em seguida, use o divisor de ASF para analisar o objeto de dados ASF e obter os pacotes de dados para o fluxo de vídeo selecionado.</span><span class="sxs-lookup"><span data-stu-id="2ae85-178">Next, use the ASF splitter to parse the ASF Data Object and get the data packets for the selected video stream.</span></span> <span data-ttu-id="2ae85-179">O aplicativo lê os dados do arquivo ASF em blocos de tamanho fixo e passa os dados para o divisor de ASF.</span><span class="sxs-lookup"><span data-stu-id="2ae85-179">The application reads data from the ASF file in fixed-size blocks and passes the data to the ASF splitter.</span></span> <span data-ttu-id="2ae85-180">O divisor analisa os dados e gera amostras de [mídia](media-samples.md) que contêm os dados de vídeo compactados.</span><span class="sxs-lookup"><span data-stu-id="2ae85-180">The splitter parses the data and generates [Media Samples](media-samples.md) that contain the compressed video data.</span></span> <span data-ttu-id="2ae85-181">O aplicativo verifica se cada amostra representa um quadro-chave.</span><span class="sxs-lookup"><span data-stu-id="2ae85-181">The application checks whether each sample represents a key frame.</span></span> <span data-ttu-id="2ae85-182">Nesse caso, o aplicativo exibe algumas informações básicas sobre o exemplo:</span><span class="sxs-lookup"><span data-stu-id="2ae85-182">If so, the application displays some basic information about the sample:</span></span>

-   <span data-ttu-id="2ae85-183">Número de buffers de mídia</span><span class="sxs-lookup"><span data-stu-id="2ae85-183">Number of media buffers</span></span>
-   <span data-ttu-id="2ae85-184">Tamanho total dos dados</span><span class="sxs-lookup"><span data-stu-id="2ae85-184">Total size of the data</span></span>
-   <span data-ttu-id="2ae85-185">Carimbo de data/hora</span><span class="sxs-lookup"><span data-stu-id="2ae85-185">Time stamp</span></span>

<span data-ttu-id="2ae85-186">Para gerar amostras de mídia compactadas:</span><span class="sxs-lookup"><span data-stu-id="2ae85-186">To generate compressed media samples:</span></span>

1.  <span data-ttu-id="2ae85-187">Aloque um novo buffer de mídia.</span><span class="sxs-lookup"><span data-stu-id="2ae85-187">Allocate a new media buffer.</span></span>
2.  <span data-ttu-id="2ae85-188">Ler dados do fluxo de bytes no buffer de mídia.</span><span class="sxs-lookup"><span data-stu-id="2ae85-188">Read data from the byte stream into the media buffer.</span></span>
3.  <span data-ttu-id="2ae85-189">Passe o buffer de mídia para o método [**IMFASFSplitter::P arsedata**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) .</span><span class="sxs-lookup"><span data-stu-id="2ae85-189">Pass the media buffer to the [**IMFASFSplitter::ParseData**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) method.</span></span> <span data-ttu-id="2ae85-190">O método analisa os dados do ASF no buffer.</span><span class="sxs-lookup"><span data-stu-id="2ae85-190">The method parses the ASF data in the buffer.</span></span>
4.  <span data-ttu-id="2ae85-191">Em um loop, obtenha amostras de mídia do divisor chamando [**IMFASFSplitter:: GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample).</span><span class="sxs-lookup"><span data-stu-id="2ae85-191">In a loop, get media samples from the splitter by calling [**IMFASFSplitter::GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample).</span></span> <span data-ttu-id="2ae85-192">Se o parâmetro *ppISample* receber um ponteiro [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) válido, isso significará que o divisor de ASF analisou um ou mais pacotes de dados.</span><span class="sxs-lookup"><span data-stu-id="2ae85-192">If the *ppISample* parameter receives a valid [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) pointer, it means the ASF splitter has parsed one or more data packets.</span></span> <span data-ttu-id="2ae85-193">Se *ppISample* receber o valor **NULL**, interrompa do loop e volte para a etapa 1.</span><span class="sxs-lookup"><span data-stu-id="2ae85-193">If *ppISample* receives the value **NULL**, break from the loop and go back to step 1.</span></span>
5.  <span data-ttu-id="2ae85-194">Exiba informações sobre o exemplo.</span><span class="sxs-lookup"><span data-stu-id="2ae85-194">Display information about the sample.</span></span>
6.  <span data-ttu-id="2ae85-195">Interromper do loop nas seguintes condições:</span><span class="sxs-lookup"><span data-stu-id="2ae85-195">Break from the loop in the following conditions:</span></span>
    -   <span data-ttu-id="2ae85-196">O parâmetro *ppISample* recebe o valor **NULL**.</span><span class="sxs-lookup"><span data-stu-id="2ae85-196">The *ppISample* parameter receives the value **NULL**.</span></span>
    -   <span data-ttu-id="2ae85-197">O parâmetro *pdwStatusFlags* não recebe o sinalizador **ASF \_ STATUSFLAGS \_ incompleto** .</span><span class="sxs-lookup"><span data-stu-id="2ae85-197">The *pdwStatusFlags* parameter does not receive the **ASF\_STATUSFLAGS\_INCOMPLETE** flag.</span></span>

<span data-ttu-id="2ae85-198">Repita essas etapas até chegar ao final do arquivo.</span><span class="sxs-lookup"><span data-stu-id="2ae85-198">Repeat these steps until you reach the end of the file.</span></span> <span data-ttu-id="2ae85-199">O código a seguir mostra estas etapas:</span><span class="sxs-lookup"><span data-stu-id="2ae85-199">The following code shows these steps:</span></span>


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



<span data-ttu-id="2ae85-200">A função iskeyframe testa se um exemplo é um quadro-chave, obtendo o valor do atributo [**MFSampleExtension \_ CleanPoint**](mfsampleextension-cleanpoint-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="2ae85-200">The IsKeyFrame function tests whether a sample is a key frame, by getting the value of the [**MFSampleExtension\_CleanPoint**](mfsampleextension-cleanpoint-attribute.md) attribute.</span></span>


```C++
inline BOOL IsRandomAccessPoint(IMFSample *pSample)
{
    // Check for the "clean point" attribute. Default to FALSE.
    return MFGetAttributeUINT32(pSample, MFSampleExtension_CleanPoint, FALSE);
}
```



<span data-ttu-id="2ae85-201">Para fins de ilustração, este tutorial exibe algumas informações para cada quadro de chave de vídeo, chamando a seguinte função:</span><span class="sxs-lookup"><span data-stu-id="2ae85-201">For illustration purposes, this tutorial displays some information for each video key frame, by calling the following function:</span></span>


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



<span data-ttu-id="2ae85-202">Um aplicativo típico usaria os pacotes de dados para decodificação, remuxing, envio pela rede ou alguma outra tarefa.</span><span class="sxs-lookup"><span data-stu-id="2ae85-202">A typical application would use the data packets for decoding, remuxing, sending over the network, or some other task.</span></span>

## <a name="7-write-the-entry-point-function"></a><span data-ttu-id="2ae85-203">7. gravar a função Entry-Point</span><span class="sxs-lookup"><span data-stu-id="2ae85-203">7. Write the Entry-Point Function</span></span>

<span data-ttu-id="2ae85-204">Agora você pode colocar as etapas anteriores juntas em um aplicativo completo.</span><span class="sxs-lookup"><span data-stu-id="2ae85-204">Now you can put the previous steps together into a complete application.</span></span> <span data-ttu-id="2ae85-205">Antes de usar qualquer um dos objetos Media Foundation, inicialize a plataforma Media Foundation chamando [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup).</span><span class="sxs-lookup"><span data-stu-id="2ae85-205">Before using any of the Media Foundation objects, initialize the Media Foundation platform by calling [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup).</span></span> <span data-ttu-id="2ae85-206">Quando terminar, chame [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span><span class="sxs-lookup"><span data-stu-id="2ae85-206">When you are done, call [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span></span> <span data-ttu-id="2ae85-207">Para obter mais informações, [inicializando Media Foundation](initializing-media-foundation.md).</span><span class="sxs-lookup"><span data-stu-id="2ae85-207">For more information, [Initializing Media Foundation](initializing-media-foundation.md).</span></span>


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



## <a name="program-listing"></a><span data-ttu-id="2ae85-208">Listagem de programas</span><span class="sxs-lookup"><span data-stu-id="2ae85-208">Program Listing</span></span>

<span data-ttu-id="2ae85-209">O código a seguir mostra a listagem completa para o tutorial.</span><span class="sxs-lookup"><span data-stu-id="2ae85-209">The following code shows the complete listing for the tutorial.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="2ae85-210">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2ae85-210">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ae85-211">Componentes ASF WMContainer</span><span class="sxs-lookup"><span data-stu-id="2ae85-211">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> <dt>

[<span data-ttu-id="2ae85-212">Suporte a ASF no Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2ae85-212">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



