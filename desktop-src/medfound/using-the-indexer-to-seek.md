---
description: O indexador ASF é um componente de camada WMContainer que é usado para ler ou gravar objetos de índice em um arquivo ASF (Advanced Systems Format). Este tópico fornece informações sobre como usar o indexador ASF para buscar em um arquivo ASF.
ms.assetid: 9c501d33-847e-448e-a19c-39dfbc7757ca
title: Usando o indexador para buscar em um arquivo ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c40c35f876fdc5452c596048d121fb0c2933094a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105791615"
---
# <a name="using-the-indexer-to-seek-within-an-asf-file"></a><span data-ttu-id="1aff8-104">Usando o indexador para buscar em um arquivo ASF</span><span class="sxs-lookup"><span data-stu-id="1aff8-104">Using the Indexer to Seek Within an ASF File</span></span>

<span data-ttu-id="1aff8-105">O *indexador* ASF é um componente de camada WMContainer que é usado para ler ou gravar objetos de índice em um arquivo ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="1aff8-105">The ASF *indexer* is a WMContainer layer component that is used to read or write Index Objects in an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="1aff8-106">Este tópico fornece informações sobre como usar o indexador ASF para buscar em um arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="1aff8-106">This topic provides information about using the ASF indexer to seek within an ASF file.</span></span>

-   [<span data-ttu-id="1aff8-107">Inicializando o indexador para busca</span><span class="sxs-lookup"><span data-stu-id="1aff8-107">Initializing the Indexer for Seeking</span></span>](#initializing-the-indexer-for-seeking)
-   [<span data-ttu-id="1aff8-108">Obtendo a posição de busca.</span><span class="sxs-lookup"><span data-stu-id="1aff8-108">Getting the Seek Position.</span></span>](#getting-the-seek-position)
-   [<span data-ttu-id="1aff8-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1aff8-109">Related topics</span></span>](#related-topics)

<span data-ttu-id="1aff8-110">Para obter informações sobre a estrutura de um arquivo ASF, consulte [estrutura de arquivo ASF](asf-file-structure.md).</span><span class="sxs-lookup"><span data-stu-id="1aff8-110">For information about the structure of an ASF file, see [ASF File Structure](asf-file-structure.md).</span></span>

## <a name="initializing-the-indexer-for-seeking"></a><span data-ttu-id="1aff8-111">Inicializando o indexador para busca</span><span class="sxs-lookup"><span data-stu-id="1aff8-111">Initializing the Indexer for Seeking</span></span>

<span data-ttu-id="1aff8-112">Para inicializar o indexador ASF para busca:</span><span class="sxs-lookup"><span data-stu-id="1aff8-112">To initialize the ASF indexer for seeking:</span></span>

1.  <span data-ttu-id="1aff8-113">Chame [**MFCreateASFIndexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexer) para criar uma nova instância do indexador ASF.</span><span class="sxs-lookup"><span data-stu-id="1aff8-113">Call [**MFCreateASFIndexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexer) to create a new instance of the ASF indexer.</span></span>
2.  <span data-ttu-id="1aff8-114">Chame [**IMFASFIndexer:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize) para inicializar o indexador.</span><span class="sxs-lookup"><span data-stu-id="1aff8-114">Call [**IMFASFIndexer::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize) to initialize the indexer.</span></span> <span data-ttu-id="1aff8-115">Esse método obtém informações do cabeçalho ASF para determinar quais fluxos ASF são indexados.</span><span class="sxs-lookup"><span data-stu-id="1aff8-115">This method gets information from the ASF header to determine which ASF streams are indexed.</span></span> <span data-ttu-id="1aff8-116">Por padrão, o objeto indexador é configurado para busca.</span><span class="sxs-lookup"><span data-stu-id="1aff8-116">By default, the indexer object is configured for seeking.</span></span>
3.  <span data-ttu-id="1aff8-117">Chame [**IMFASFIndexer:: GetIndexPosition**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexposition) para localizar o deslocamento do índice no arquivo asf.</span><span class="sxs-lookup"><span data-stu-id="1aff8-117">Call [**IMFASFIndexer::GetIndexPosition**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexposition) to find the offset of the index within the ASF file.</span></span>
4.  <span data-ttu-id="1aff8-118">Chame a função [**MFCreateASFIndexerByteStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexerbytestream) para criar um fluxo de bytes para ler o índice.</span><span class="sxs-lookup"><span data-stu-id="1aff8-118">Call the [**MFCreateASFIndexerByteStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexerbytestream) function to create a byte stream for reading the index.</span></span> <span data-ttu-id="1aff8-119">A entrada para essa função é um ponteiro para um fluxo de bytes que contém o arquivo ASF e o deslocamento do índice (da etapa anterior).</span><span class="sxs-lookup"><span data-stu-id="1aff8-119">The input to this function is a pointer to a byte stream that contains the ASF file, and the offset of the index (from the previous step).</span></span>
5.  <span data-ttu-id="1aff8-120">Chame [**IMFASFIndexer:: SetIndexByteStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexbytestreams) para definir o fluxo de bytes de índice no indexador.</span><span class="sxs-lookup"><span data-stu-id="1aff8-120">Call [**IMFASFIndexer::SetIndexByteStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexbytestreams) to set the index byte stream on the indexer.</span></span>

<span data-ttu-id="1aff8-121">O código a seguir mostra estas etapas:</span><span class="sxs-lookup"><span data-stu-id="1aff8-121">The following code shows these steps:</span></span>


```C++
HRESULT CreateASFIndexer(
    IMFByteStream *pContentByteStream,  // Pointer to the content byte stream
    IMFASFContentInfo *pContentInfo,
    IMFASFIndexer **ppIndexer
    )
{
    IMFASFIndexer *pIndexer = NULL;
    IMFByteStream *pIndexerByteStream = NULL;

    QWORD qwLength = 0, qwIndexOffset = 0, qwBytestreamLength = 0;

    // Create the indexer.
    HRESULT hr = MFCreateASFIndexer(&pIndexer);
    if (FAILED(hr))
    {
        goto done;
    }

    //Initialize the indexer to work with this ASF library
    hr =  pIndexer->Initialize(pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }

    //Check if the index exists. You can only do this after creating the indexer

    //Get byte stream length
    hr = pContentByteStream->GetLength(&qwLength);
    if (FAILED(hr))
    {
        goto done;
    }

    //Get index offset
    hr = pIndexer->GetIndexPosition(pContentInfo, &qwIndexOffset);
    if (FAILED(hr))
    {
        goto done;
    }

    if ( qwIndexOffset >= qwLength)
    {
        //index object does not exist, release the indexer
        goto done;
    }
    else
    {
        // initialize the indexer
        // Create a byte stream that the Indexer will use to read in
        // and parse the indexers.
         hr = MFCreateASFIndexerByteStream(
             pContentByteStream,
             qwIndexOffset,
             &pIndexerByteStream
             );

        if (FAILED(hr))
        {
            goto done;
        }
   }

    hr = pIndexer->SetIndexByteStreams(&pIndexerByteStream, 1);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.
    *ppIndexer = pIndexer;
    (*ppIndexer)->AddRef();

done:
    SafeRelease(&pIndexer);
    SafeRelease(&pIndexerByteStream);
    return hr;
}
```



## <a name="getting-the-seek-position"></a><span data-ttu-id="1aff8-122">Obtendo a posição de busca.</span><span class="sxs-lookup"><span data-stu-id="1aff8-122">Getting the Seek Position.</span></span>

1.  <span data-ttu-id="1aff8-123">Para descobrir se um fluxo específico está indexado, chame [**IMFASFIndexer:: GetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexstatus).</span><span class="sxs-lookup"><span data-stu-id="1aff8-123">To find out if a particular stream is indexed, call [**IMFASFIndexer::GetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexstatus).</span></span> <span data-ttu-id="1aff8-124">Se o fluxo for indexado, o parâmetro *pfIsIndexed* receberá o valor **true**; caso contrário, ele receberá o valor **false**.</span><span class="sxs-lookup"><span data-stu-id="1aff8-124">If the stream is indexed, the *pfIsIndexed* parameter receives the value **TRUE**; otherwise it receives the value **FALSE**.</span></span>
2.  <span data-ttu-id="1aff8-125">Por padrão, o indexador usa a busca direta.</span><span class="sxs-lookup"><span data-stu-id="1aff8-125">By default, the indexer uses forward seeking.</span></span> <span data-ttu-id="1aff8-126">Para busca inversa (ou seja, busca do final do arquivo), chame [**IMFASFIndexer:: SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) e defina o sinalizador **MFASF \_ do indexador \_ de leitura \_ para \_ REVERSEPLAYBACK** .</span><span class="sxs-lookup"><span data-stu-id="1aff8-126">For reverse seeking (that is, seeking from the end of the file), call [**IMFASFIndexer::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) and set the **MFASF\_INDEXER\_READ\_FOR\_REVERSEPLAYBACK** flag.</span></span> <span data-ttu-id="1aff8-127">Caso contrário, pule essa etapa.</span><span class="sxs-lookup"><span data-stu-id="1aff8-127">Otherwise, skip this step.</span></span>
3.  <span data-ttu-id="1aff8-128">Se o fluxo for indexado, obtenha a posição de busca para um tempo de apresentação especificado chamando [**IMFASFIndexer:: GetSeekPositionForValue**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getseekpositionforvalue).</span><span class="sxs-lookup"><span data-stu-id="1aff8-128">If the stream is indexed, get the seek position for a specified presentation time by calling [**IMFASFIndexer::GetSeekPositionForValue**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getseekpositionforvalue).</span></span> <span data-ttu-id="1aff8-129">Esse método lê o índice ASF e localiza a entrada de índice mais próxima da hora solicitada.</span><span class="sxs-lookup"><span data-stu-id="1aff8-129">This method reads the ASF index and finds the index entry that is closest to the requested time.</span></span> <span data-ttu-id="1aff8-130">O método retorna o deslocamento de bytes do pacote de dados especificado pela entrada de índice.</span><span class="sxs-lookup"><span data-stu-id="1aff8-130">The method returns the byte offset of the data packet specified by the index entry.</span></span> <span data-ttu-id="1aff8-131">O deslocamento de byte é relativo ao início do objeto de dados ASF.</span><span class="sxs-lookup"><span data-stu-id="1aff8-131">The byte offset is relative to the start of the ASF Data Object.</span></span>

<span data-ttu-id="1aff8-132">O método [**GetSeekPositionForValue**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getseekpositionforvalue) usa um ponteiro para a estrutura do [**\_ \_ identificador de índice do ASF**](/windows/desktop/api/wmcontainer/ns-wmcontainer-asf_index_identifier) .</span><span class="sxs-lookup"><span data-stu-id="1aff8-132">The [**GetSeekPositionForValue**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getseekpositionforvalue) method takes a pointer to the [**ASF\_INDEX\_IDENTIFIER**](/windows/desktop/api/wmcontainer/ns-wmcontainer-asf_index_identifier) structure.</span></span> <span data-ttu-id="1aff8-133">Essa estrutura especifica um tipo de índice e um identificador de fluxo.</span><span class="sxs-lookup"><span data-stu-id="1aff8-133">This structure specifies an index type and a stream identifier.</span></span> <span data-ttu-id="1aff8-134">Atualmente, o tipo de índice deve ser \_ NULL GUID, que especifica a indexação baseada em tempo.</span><span class="sxs-lookup"><span data-stu-id="1aff8-134">Currently, the index type must be GUID\_NULL, which specifies time-based indexing.</span></span>

<span data-ttu-id="1aff8-135">O código a seguir obtém uma posição de busca, dado um identificador de fluxo e um tempo de apresentação de destino.</span><span class="sxs-lookup"><span data-stu-id="1aff8-135">The following code gets a seek position, given a stream identifier and target presentation time.</span></span> <span data-ttu-id="1aff8-136">Se a chamada for realizada com sucesso, ela retornará o deslocamento de dados no parâmetro *pcbDataOffset* e o tempo de busca real aproximado em *phnsApproxSeekTime*.</span><span class="sxs-lookup"><span data-stu-id="1aff8-136">If the call succeeds, it returns the data offset in the *pcbDataOffset* parameter and the approximate actual seek time in *phnsApproxSeekTime*.</span></span>


```C++
HRESULT GetSeekPositionWithIndexer(
    IMFASFIndexer *pIndexer,
    WORD          wStreamNumber,
    MFTIME        hnsSeekTime,          // Desired seek time, in 100-nsec.
    BOOL          bReverse,
    QWORD         *pcbDataOffset,       // Receives the offset in bytes.
    MFTIME        *phnsApproxSeekTime   // Receives the approximate seek time.
    )
{
    // Query whether the stream is indexed.

    ASF_INDEX_IDENTIFIER IndexIdentifier = { GUID_NULL, wStreamNumber };

    BOOL fIsIndexed = FALSE;

    ASF_INDEX_DESCRIPTOR descriptor;

    DWORD cbIndexDescriptor = sizeof(descriptor);

    HRESULT hr = pIndexer->GetIndexStatus(
        &IndexIdentifier,
        &fIsIndexed,
        (BYTE*)&descriptor,
        &cbIndexDescriptor
        );

    if (hr == MF_E_BUFFERTOOSMALL)
    {
        hr = S_OK;
    }
    else if (FAILED(hr))
    {
        goto done;
    }

    if (!fIsIndexed)
    {
        hr = MF_E_ASF_NOINDEX;
        goto done;
    }

    if (bReverse)
    {
        hr = pIndexer->SetFlags(MFASF_INDEXER_READ_FOR_REVERSEPLAYBACK);
        if (FAILED(hr))
        {
            goto done;
        }
    }

    // Get the offset from the indexer.

    PROPVARIANT var;

    var.vt = VT_I8;
    var.hVal.QuadPart = hnsSeekTime;

    hr = pIndexer->GetSeekPositionForValue(
        &var,
        &IndexIdentifier,
        pcbDataOffset,
        phnsApproxSeekTime,
        0
        );

done:
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="1aff8-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1aff8-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1aff8-138">Indexador ASF</span><span class="sxs-lookup"><span data-stu-id="1aff8-138">ASF Indexer</span></span>](asf-index-object.md)
</dt> </dl>

 

 



