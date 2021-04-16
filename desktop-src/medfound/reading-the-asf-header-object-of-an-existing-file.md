---
description: Lendo o objeto de cabeçalho ASF de um arquivo existente
ms.assetid: 0e37f0d3-a37b-4f36-a133-7b1922e9944b
title: Lendo o objeto de cabeçalho ASF de um arquivo existente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b231cb0b9af6b24f84efaa6403a4774e66bbb646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765606"
---
# <a name="reading-the-asf-header-object-of-an-existing-file"></a><span data-ttu-id="bbe7a-103">Lendo o objeto de cabeçalho ASF de um arquivo existente</span><span class="sxs-lookup"><span data-stu-id="bbe7a-103">Reading the ASF Header Object of an Existing File</span></span>

<span data-ttu-id="bbe7a-104">O objeto ASF ContentInfo armazena informações que representam os objetos de cabeçalho ASF de um arquivo de mídia.</span><span class="sxs-lookup"><span data-stu-id="bbe7a-104">The ASF ContentInfo object stores information that represents the ASF Header Objects of a media file.</span></span> <span data-ttu-id="bbe7a-105">Um objeto ContentInfo populado é necessário para ler e analisar um arquivo ASF existente.</span><span class="sxs-lookup"><span data-stu-id="bbe7a-105">A populated ContentInfo object is required in order to read and parse an existing ASF file.</span></span>

<span data-ttu-id="bbe7a-106">Depois de criar o objeto ContentInfo chamando a função [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) , o aplicativo deve inicializá-lo com informações de cabeçalho do arquivo ASF a ser lido.</span><span class="sxs-lookup"><span data-stu-id="bbe7a-106">After creating the ContentInfo object by calling the [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) function, the application must initialize it with header information from the ASF file that is to be read.</span></span> <span data-ttu-id="bbe7a-107">Para popular o objeto, chame [**IMFASFContentInfo::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader).</span><span class="sxs-lookup"><span data-stu-id="bbe7a-107">To populate the object, call [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader).</span></span>

<span data-ttu-id="bbe7a-108">**ParseHeader** requer um buffer de mídia que contenha o objeto de cabeçalho do arquivo asf.</span><span class="sxs-lookup"><span data-stu-id="bbe7a-108">**ParseHeader** requires a media buffer that contains the Header Object of the ASF file.</span></span> <span data-ttu-id="bbe7a-109">Uma opção é preencher um buffer de mídia com o objeto de cabeçalho para criar um fluxo de bytes para o arquivo e, em seguida, ler os primeiros 30 bytes de dados do fluxo de bytes em um buffer de mídia.</span><span class="sxs-lookup"><span data-stu-id="bbe7a-109">One option is to fill a media buffer with the Header Object to create a byte stream for the file and then read the first 30 bytes of data from the byte stream into a media buffer.</span></span> <span data-ttu-id="bbe7a-110">Em seguida, você pode obter o tamanho passando os primeiros 24 bytes do objeto de cabeçalho para o método [**IMFASFContentInfo:: Getheaders**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) .</span><span class="sxs-lookup"><span data-stu-id="bbe7a-110">You can then get the size by passing the first 24 bytes of the Header Object to the [**IMFASFContentInfo::GetHeaderSize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) method.</span></span> <span data-ttu-id="bbe7a-111">Depois de obter o tamanho, você pode ler o objeto de cabeçalho inteiro em um buffer de mídia e passá-lo para **ParseHeader**.</span><span class="sxs-lookup"><span data-stu-id="bbe7a-111">After getting the size, you can read the entire Header Object in a media buffer and pass it to **ParseHeader**.</span></span> <span data-ttu-id="bbe7a-112">O método inicia a análise no deslocamento a partir do início do buffer de mídia especificado no parâmetro *cbOffsetWithinHeader* .</span><span class="sxs-lookup"><span data-stu-id="bbe7a-112">The method starts parsing at the offset from the start of the media buffer specified in the *cbOffsetWithinHeader* parameter.</span></span>

<span data-ttu-id="bbe7a-113">O código de exemplo a seguir cria e inicializa um objeto ContentInfo para ler um arquivo ASF existente contido em um fluxo de bytes.</span><span class="sxs-lookup"><span data-stu-id="bbe7a-113">The following example code creates and initializes a ContentInfo object for reading an existing ASF file contained in a byte stream.</span></span> <span data-ttu-id="bbe7a-114">Primeiro, definimos uma função auxiliar que lê dados de um fluxo de bytes e aloca um buffer de mídia para manter os dados:</span><span class="sxs-lookup"><span data-stu-id="bbe7a-114">First, we define a helper function that reads data from a byte stream and allocates a media buffer to hold the data:</span></span>


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



<span data-ttu-id="bbe7a-115">O exemplo a seguir lê o objeto de cabeçalho ASF de um fluxo de bytes e popula um objeto ContentInfo do ASF.</span><span class="sxs-lookup"><span data-stu-id="bbe7a-115">The next example reads the ASF Header Object from a byte stream and populates an ASF ContentInfo object.</span></span>


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



> [!Note]  
> <span data-ttu-id="bbe7a-116">Esses exemplos usam a função [SafeRelease](saferelease.md) para liberar ponteiros de interface.</span><span class="sxs-lookup"><span data-stu-id="bbe7a-116">These examples use the [SafeRelease](saferelease.md) function to release interface pointers.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="bbe7a-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bbe7a-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbe7a-118">Objeto ASF ContentInfo</span><span class="sxs-lookup"><span data-stu-id="bbe7a-118">ASF ContentInfo Object</span></span>](asf-contentinfo-object.md)
</dt> <dt>

[<span data-ttu-id="bbe7a-119">Objeto de cabeçalho ASF</span><span class="sxs-lookup"><span data-stu-id="bbe7a-119">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="bbe7a-120">Suporte a ASF no Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bbe7a-120">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="bbe7a-121">Obtendo informações de objetos de cabeçalho ASF</span><span class="sxs-lookup"><span data-stu-id="bbe7a-121">Getting Information from ASF Header Objects</span></span>](getting-information-from-asf-header-objects.md)
</dt> </dl>

 

 



