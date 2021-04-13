---
description: Gerando um novo objeto de cabeçalho ASF
ms.assetid: cf73306d-156a-45c0-a3d6-ae48734f5709
title: Gerando um novo objeto de cabeçalho ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f303be4eb3353a0e7ddf1dad0eff9956f68d7db5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501165"
---
# <a name="generating-a-new-asf-header-object"></a><span data-ttu-id="03211-103">Gerando um novo objeto de cabeçalho ASF</span><span class="sxs-lookup"><span data-stu-id="03211-103">Generating a New ASF Header Object</span></span>

<span data-ttu-id="03211-104">Para converter as informações contidas no objeto ContentInfo em um formato de objeto de cabeçalho ASF binário, o aplicativo deve chamar [**IMFASFContentInfo:: GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader).</span><span class="sxs-lookup"><span data-stu-id="03211-104">To convert the information contained in the ContentInfo object to a binary ASF Header Object format, the application must call [**IMFASFContentInfo::GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader).</span></span> <span data-ttu-id="03211-105">Essa chamada deve ser feita depois que os pacotes de dados são gerados e o objeto ContentInfo contém informações atualizadas.</span><span class="sxs-lookup"><span data-stu-id="03211-105">This call must be made after the data packets are generated and the ContentInfo object contains updated information.</span></span> <span data-ttu-id="03211-106">**GenerateHeader** retorna um ponteiro para um buffer de mídia que contém as informações de cabeçalho no formato válido.</span><span class="sxs-lookup"><span data-stu-id="03211-106">**GenerateHeader** returns a pointer to a media buffer that contains the header information in the valid format.</span></span> <span data-ttu-id="03211-107">Em seguida, o aplicativo pode gravar os dados, apontados pelo buffer de mídia, no início de um novo arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="03211-107">The application can then write the data, pointed to by the media buffer, at the beginning of a new ASF file.</span></span>

## <a name="to-write-a-new-header-object-by-using-the-contentinfo-object"></a><span data-ttu-id="03211-108">Para gravar um novo objeto de cabeçalho usando o objeto ContentInfo</span><span class="sxs-lookup"><span data-stu-id="03211-108">To write a new Header Object by using the ContentInfo object</span></span>

1.  <span data-ttu-id="03211-109">Chame [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) para criar um objeto ContentInfo vazio.</span><span class="sxs-lookup"><span data-stu-id="03211-109">Call [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) to create an empty ContentInfo object.</span></span>
2.  <span data-ttu-id="03211-110">Chame [**IMFASFContentInfo:: setprofile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) para fornecer o objeto de perfil ao objeto ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="03211-110">Call [**IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) to supply the profile object to the ContentInfo object.</span></span> <span data-ttu-id="03211-111">Para obter informações sobre como criar perfis, consulte [criando um perfil de ASF](creating-an-asf-profile.md).</span><span class="sxs-lookup"><span data-stu-id="03211-111">For information about creating profiles, see [Creating an ASF Profile](creating-an-asf-profile.md).</span></span>
3.  <span data-ttu-id="03211-112">Chame [**IMFASFContentInfo:: GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader) e passe **NULL** no parâmetro *pIHeader* e receba o tamanho do objeto ContentInfo populado no parâmetro *pcbHeader* .</span><span class="sxs-lookup"><span data-stu-id="03211-112">Call [**IMFASFContentInfo::GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader) and pass **NULL** in the *pIHeader* parameter and receive the size of the populated ContentInfo object in the *pcbHeader* parameter.</span></span> <span data-ttu-id="03211-113">O aplicativo pode usar esse valor para alocar memória ou o buffer de mídia que conterá o objeto de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="03211-113">The application can use this value to allocate memory or the media buffer that will contain the Header Object.</span></span>

    <span data-ttu-id="03211-114">O tamanho do cabeçalho recebido inclui o tamanho do preenchimento, que é ajustado dependendo do tamanho real dos objetos de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="03211-114">The header size received includes the padding size, which is adjusted depending on the actual size of the header objects.</span></span> <span data-ttu-id="03211-115">O tamanho máximo dos objetos de cabeçalho é 10 MB.</span><span class="sxs-lookup"><span data-stu-id="03211-115">The maximum size of the header objects is 10 MB.</span></span> <span data-ttu-id="03211-116">Se o tamanho exceder esse valor, **GenerateHeader** falhará com o \_ erro de INVALIDDATA MF E \_ ASF \_ .</span><span class="sxs-lookup"><span data-stu-id="03211-116">If the size exceeds this value, **GenerateHeader** fails with the MF\_E\_ASF\_INVALIDDATA error.</span></span>

4.  <span data-ttu-id="03211-117">Chame [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) para criar um buffer de mídia do tamanho recebido na etapa 3.</span><span class="sxs-lookup"><span data-stu-id="03211-117">Call [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) to create a media buffer of the received size in step 3.</span></span>
5.  <span data-ttu-id="03211-118">Chame **GenerateHeader** novamente para gerar o novo objeto de cabeçalho ASF do objeto ContentInfo no buffer de mídia criado na etapa 4.</span><span class="sxs-lookup"><span data-stu-id="03211-118">Call **GenerateHeader** again to generate the new ASF Header Object from the ContentInfo object in the media buffer created in step 4.</span></span>

    <span data-ttu-id="03211-119">O comprimento dos dados no buffer de mídia é atualizado e o novo tamanho é retornado no parâmetro *pcbHeader* .</span><span class="sxs-lookup"><span data-stu-id="03211-119">The length of the data in the media buffer is updated and the new size is returned in the *pcbHeader* parameter.</span></span>

6.  <span data-ttu-id="03211-120">Grave o conteúdo do buffer de mídia no início do arquivo.</span><span class="sxs-lookup"><span data-stu-id="03211-120">Write the contents of the media buffer at the beginning of the file.</span></span> <span data-ttu-id="03211-121">O aplicativo pode usar o fluxo de bytes para executar a operação de gravação.</span><span class="sxs-lookup"><span data-stu-id="03211-121">The application can use the byte stream to perform the writing operation.</span></span> <span data-ttu-id="03211-122">Para obter um exemplo de código, consulte [**IMFByteStream:: Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write).</span><span class="sxs-lookup"><span data-stu-id="03211-122">For example code, see [**IMFByteStream::Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write).</span></span>

### <a name="example"></a><span data-ttu-id="03211-123">Exemplo</span><span class="sxs-lookup"><span data-stu-id="03211-123">Example</span></span>

<span data-ttu-id="03211-124">O código de exemplo a seguir mostra como criar um objeto ContentInfo e gerar um buffer de mídia para armazenar o novo objeto de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="03211-124">The following example code shows how to create a ContentInfo object and generate a media buffer to store the new Header Object.</span></span> <span data-ttu-id="03211-125">Para obter um exemplo completo que usa esse código, consulte [tutorial: copiando fluxos ASF de um arquivo para outro](tutorial--copying-asf-streams-from-one-file-to-another.md).</span><span class="sxs-lookup"><span data-stu-id="03211-125">For a complete example that uses this code, see [Tutorial: Copying ASF Streams from One File to Another](tutorial--copying-asf-streams-from-one-file-to-another.md).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="03211-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="03211-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03211-127">Gravando um objeto de cabeçalho ASF para um novo arquivo</span><span class="sxs-lookup"><span data-stu-id="03211-127">Writing an ASF Header Object for a New File</span></span>](writing-an-asf-header-object-for-a-new-file.md)
</dt> </dl>

 

 



