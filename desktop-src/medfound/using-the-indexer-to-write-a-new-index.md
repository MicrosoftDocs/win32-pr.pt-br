---
description: Este tópico mostra como gravar um índice para um arquivo ASF (Advanced Systems Format).
ms.assetid: a14e3bef-0232-4259-930a-d860ed9230fd
title: Usando o indexador para gravar um novo índice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d37922b693c83a8417dea4006fc38397b805fb71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647733"
---
# <a name="using-the-indexer-to-write-a-new-index"></a><span data-ttu-id="04308-103">Usando o indexador para gravar um novo índice</span><span class="sxs-lookup"><span data-stu-id="04308-103">Using the Indexer to Write a New Index</span></span>

<span data-ttu-id="04308-104">Este tópico mostra como gravar um índice para um arquivo ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="04308-104">This topic shows how to write an index for an Advanced Systems Format (ASF) file.</span></span>

<span data-ttu-id="04308-105">Aqui está o procedimento geral para criar um índice ASF:</span><span class="sxs-lookup"><span data-stu-id="04308-105">Here is the general procedure for creating an ASF index:</span></span>

1.  <span data-ttu-id="04308-106">Inicialize uma nova instância do objeto do indexador ASF, conforme descrito em [criação e configuração do indexador](indexer-creation-and-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="04308-106">Initialize a new instance of the ASF indexer object, as described in [Indexer Creation and Configuration](indexer-creation-and-configuration.md).</span></span>
2.  <span data-ttu-id="04308-107">Opcionalmente, configure o indexador.</span><span class="sxs-lookup"><span data-stu-id="04308-107">Optionally, configure the indexer.</span></span>
3.  <span data-ttu-id="04308-108">Enviar pacotes de dados ASF para o indexador.</span><span class="sxs-lookup"><span data-stu-id="04308-108">Send ASF data packets to the indexer.</span></span>
4.  <span data-ttu-id="04308-109">Confirme o índice.</span><span class="sxs-lookup"><span data-stu-id="04308-109">Commit the index.</span></span>
5.  <span data-ttu-id="04308-110">Obtenha o índice concluído do indexador e grave-o em um fluxo.</span><span class="sxs-lookup"><span data-stu-id="04308-110">Get the completed index from the indexer, and write it to a stream.</span></span>

## <a name="configure-the-indexer"></a><span data-ttu-id="04308-111">Configurar o indexador</span><span class="sxs-lookup"><span data-stu-id="04308-111">Configure the Indexer</span></span>

<span data-ttu-id="04308-112">Para usar o indexador para gravar um novo objeto de índice, o objeto indexador deve ter o sinalizador MFASF \_ \_ gravar \_ novo conjunto de \_ índice com uma chamada para [**IMFASFIndexer:: SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) antes de ser inicializado com [**IMFASFIndexer:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize).</span><span class="sxs-lookup"><span data-stu-id="04308-112">To use the indexer to write a new index object, the indexer object must have the flag MFASF\_INDEXER\_WRITE\_NEW\_INDEX set with a call to [**IMFASFIndexer::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) before it is initialized with [**IMFASFIndexer::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize).</span></span>

<span data-ttu-id="04308-113">Quando o indexador é configurado para gravar um índice, o chamador escolhe os fluxos a serem indexados.</span><span class="sxs-lookup"><span data-stu-id="04308-113">When the indexer is configured for writing an index, the caller chooses the streams to be indexed.</span></span> <span data-ttu-id="04308-114">Por padrão, o indexador tenta criar um objeto de índice para todos os fluxos.</span><span class="sxs-lookup"><span data-stu-id="04308-114">By default, the indexer attempts to create an Index Object for all streams.</span></span> <span data-ttu-id="04308-115">O intervalo de tempo padrão é de um segundo.</span><span class="sxs-lookup"><span data-stu-id="04308-115">The default time interval is one second.</span></span>

<span data-ttu-id="04308-116">[**IMFASFIndexer:: SetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus) pode ser usado para substituir a opção padrão do objeto indexer de fluxos e tipos de índice.</span><span class="sxs-lookup"><span data-stu-id="04308-116">[**IMFASFIndexer::SetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus) can be used to override the indexer object's default choice of streams and index types.</span></span>

<span data-ttu-id="04308-117">O código de exemplo a seguir mostra a inicialização de \_ um \_ descritor de índice ASF e um \_ identificador de índice ASF \_ antes de uma chamada para [**SetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus).</span><span class="sxs-lookup"><span data-stu-id="04308-117">The following example code shows the initialization of an ASF\_INDEX\_DESCRIPTOR and an ASF\_INDEX\_IDENTIFIER before a call to [**SetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus).</span></span>


```
ASF_INDEX_DESCRIPTOR IndexerType;
ZeroMemory(&IndexerType, sizeof(ASF_INDEX_DESCRIPTOR));

ASF_INDEX_IDENTIFIER IndexIdentifier;
ZeroMemory(&IndexIdentifier, sizeof(ASF_INDEX_IDENTIFIER));

IndexIdentifier.guidIndexType = GUID_NULL;
IndexIdentifier.wStreamNumber = 1;

IndexerType.Identifier = IndexIdentifier;
IndexerType.cPerEntryBytes  = MFASFINDEXER_PER_ENTRY_BYTES_DYNAMIC;
IndexerType.dwInterval  = MFASFINDEXER_NO_FIXED_INTERVAL;

hr = pIndexer->SetIndexStatus((BYTE*)&IndexerType, sizeof(ASF_INDEX_DESCRIPTOR), TRUE);
```



<span data-ttu-id="04308-118">O identificador de índice deve ter o tipo de índice GUID definido como GUID \_ NULL para indicar que o tipo de índice será baseado em tempo de apresentação.</span><span class="sxs-lookup"><span data-stu-id="04308-118">The index identifier must have its GUID index type set to GUID\_NULL to indicate that the index type will be presentation time-based.</span></span> <span data-ttu-id="04308-119">O identificador de índice também deve ser inicializado com o número de fluxo do fluxo de ASF a ser indexado.</span><span class="sxs-lookup"><span data-stu-id="04308-119">The index identifier must also be initialized with the stream number of the ASF stream to be indexed.</span></span> <span data-ttu-id="04308-120">Depois que o identificador de índice for definido, use-o para inicializar o descritor de índice.</span><span class="sxs-lookup"><span data-stu-id="04308-120">After the index identifier is set, use it to initialize the index descriptor.</span></span>

<span data-ttu-id="04308-121">A estrutura do descritor de índice tem membros que devem ser definidos antes da chamada para [**SetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus).</span><span class="sxs-lookup"><span data-stu-id="04308-121">The index descriptor structure has members which must be set before the call to [**SetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus).</span></span> <span data-ttu-id="04308-122">O **identificador** é uma estrutura de [**\_ \_ identificador de índice ASF**](/windows/desktop/api/wmcontainer/ns-wmcontainer-asf_index_identifier) que identifica o número de fluxo e o tipo de índice.</span><span class="sxs-lookup"><span data-stu-id="04308-122">**Identifier** is an [**ASF\_INDEX\_IDENTIFIER**](/windows/desktop/api/wmcontainer/ns-wmcontainer-asf_index_identifier) structure that identifies the stream number and the type of index.</span></span> <span data-ttu-id="04308-123">**cPerEntryBytes** é o número de bytes usados para cada entrada de índice.</span><span class="sxs-lookup"><span data-stu-id="04308-123">**cPerEntryBytes** is the number of bytes used for each index entry.</span></span> <span data-ttu-id="04308-124">Se o valor for MFASFINDEXER \_ por \_ bytes de entrada \_ \_ dinâmicos, as entradas de índice terão tamanho variável.</span><span class="sxs-lookup"><span data-stu-id="04308-124">If the value is MFASFINDEXER\_PER\_ENTRY\_BYTES\_DYNAMIC, the index entries have variable size.</span></span> <span data-ttu-id="04308-125">**dwInterval** é o intervalo de indexação.</span><span class="sxs-lookup"><span data-stu-id="04308-125">**dwInterval** is the indexing interval.</span></span> <span data-ttu-id="04308-126">Um valor de MFASFINDEXER \_ nenhum \_ \_ intervalo fixo indica que não há nenhum intervalo de indexação fixo.</span><span class="sxs-lookup"><span data-stu-id="04308-126">A value of MFASFINDEXER\_NO\_FIXED\_INTERVAL indicates that there is no fixed indexing interval.</span></span>

## <a name="send-asf-data-packets-to-the-indexer"></a><span data-ttu-id="04308-127">Enviar pacotes de dados ASF para o indexador</span><span class="sxs-lookup"><span data-stu-id="04308-127">Send ASF Data Packets to the Indexer</span></span>

<span data-ttu-id="04308-128">Como o indexador é um objeto de nível WMContainer, ele deve ser usado em conjunto com o multiplexador durante a geração de pacotes.</span><span class="sxs-lookup"><span data-stu-id="04308-128">Because the indexer is a WMContainer level object, it must be used in conjunction with the multiplexer during packet generation.</span></span>

<span data-ttu-id="04308-129">Os pacotes retornados de [**GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) podem ser enviados ao objeto indexador por meio de chamadas para [**GenerateIndexEntries**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-generateindexentries) , em que ele cria entradas de índice para cada pacote enviado.</span><span class="sxs-lookup"><span data-stu-id="04308-129">Packets returned from [**GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) can be sent to the indexer object through calls to [**GenerateIndexEntries**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-generateindexentries) where it creates index entries for each packet sent.</span></span>

<span data-ttu-id="04308-130">O código a seguir demonstra como isso pode ser feito:</span><span class="sxs-lookup"><span data-stu-id="04308-130">The following code demonstrates how this may be done:</span></span>


```C++
HRESULT SendSampleToMux(
    IMFASFMultiplexer *pMux,
    IMFASFIndexer *pIndex,
    IMFSample *pSample,
    WORD wStream,
    IMFByteStream *pDestStream
    )
{
    IMFSample *pOutputSample = NULL;
    IMFMediaBuffer *pDataPacket = NULL;

    DWORD dwMuxStatus = ASF_STATUSFLAGS_INCOMPLETE;

    HRESULT hr = pMux->ProcessSample(wStream, pSample, 0);
    if (FAILED(hr))
    {
        goto done;
    }

    while (dwMuxStatus & ASF_STATUSFLAGS_INCOMPLETE)
    {
        hr = pMux->GetNextPacket(&dwMuxStatus, &pOutputSample);
        if (FAILED(hr))
        {
            goto done;
        }

        if (pOutputSample)
        {
            // Send the data packet to the indexer
            hr = pIndex->GenerateIndexEntries(pOutputSample);
            if (FAILED(hr))
            {
                goto done;
            }

            // Convert the sample to a contiguous buffer.
            hr = pOutputSample->ConvertToContiguousBuffer(&pDataPacket);
            if (FAILED(hr))
            {
                goto done;
            }

            // Write the buffer to the byte stream.
            hr = WriteBufferToByteStream(pDestStream, pDataPacket, NULL);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        SafeRelease(&pOutputSample);
        SafeRelease(&pDataPacket);
    }

done:
    SafeRelease(&pOutputSample);
    SafeRelease(&pDataPacket);
    return hr;
}
```



<span data-ttu-id="04308-131">Para obter mais informações, consulte [gerando novos pacotes de dados ASF](generating-new-asf-data-packets.md).</span><span class="sxs-lookup"><span data-stu-id="04308-131">For more information, see [Generating New ASF Data Packets](generating-new-asf-data-packets.md).</span></span>

## <a name="commit-the-index"></a><span data-ttu-id="04308-132">Confirmar o índice</span><span class="sxs-lookup"><span data-stu-id="04308-132">Commit the Index</span></span>

<span data-ttu-id="04308-133">Depois que o último pacote tiver uma entrada de índice criada para ele, o índice deverá ser confirmado.</span><span class="sxs-lookup"><span data-stu-id="04308-133">After the last packet has had an index entry created for it, the index must be committed.</span></span> <span data-ttu-id="04308-134">Isso é feito com uma chamada para [**IMFASFIndexer:: CommitIndex**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-commitindex).</span><span class="sxs-lookup"><span data-stu-id="04308-134">This is done with a call to [**IMFASFIndexer::CommitIndex**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-commitindex).</span></span> <span data-ttu-id="04308-135">**CommitIndex** usa um ponteiro para o objeto ContentInfo que descreve o conteúdo do arquivo asf.</span><span class="sxs-lookup"><span data-stu-id="04308-135">**CommitIndex** takes a pointer to the ContentInfo object which describes the content of the ASF file.</span></span> <span data-ttu-id="04308-136">A confirmação do índice conclui a indexação e atualiza o cabeçalho com novas informações sobre o tamanho do arquivo e a buscabilidade.</span><span class="sxs-lookup"><span data-stu-id="04308-136">Committing the index finishes the indexing and updates the header with new information about file size and seekability.</span></span>

## <a name="get-the-completed-index"></a><span data-ttu-id="04308-137">Obter o índice concluído</span><span class="sxs-lookup"><span data-stu-id="04308-137">Get the Completed Index</span></span>

<span data-ttu-id="04308-138">Para obter o índice concluído do indexador, execute as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="04308-138">To get the completed index from the indexer, perform the following steps:</span></span>

1.  <span data-ttu-id="04308-139">Chame [**IMFASFIndexer:: GetIndexWriteSpace**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexwritespace) para obter o tamanho do índice.</span><span class="sxs-lookup"><span data-stu-id="04308-139">Call [**IMFASFIndexer::GetIndexWriteSpace**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexwritespace) to get the size of the index.</span></span>
2.  <span data-ttu-id="04308-140">Chame [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) para criar um buffer de mídia.</span><span class="sxs-lookup"><span data-stu-id="04308-140">Call [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) to create a media buffer.</span></span> <span data-ttu-id="04308-141">Você pode alocar um buffer que seja grande o suficiente para manter o índice inteiro, de alocar um buffer menor e obter o índice em partes.</span><span class="sxs-lookup"><span data-stu-id="04308-141">You can either allocate an buffer that is large enough to hold the entire index, of allocate a smaller buffer and get the index in chunks.</span></span>
3.  <span data-ttu-id="04308-142">Chame [**IMFASFIndexer:: GetCompletedIndex**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getcompletedindex) para obter os dados do índice.</span><span class="sxs-lookup"><span data-stu-id="04308-142">Call [**IMFASFIndexer::GetCompletedIndex**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getcompletedindex) to get the index data.</span></span> <span data-ttu-id="04308-143">Na primeira chamada, defina o parâmetro *cbOffsetWithinIndex* como zero.</span><span class="sxs-lookup"><span data-stu-id="04308-143">On the first call, set the *cbOffsetWithinIndex* parameter to zero.</span></span> <span data-ttu-id="04308-144">Se você obter o índice em partes, incrementar *cbOffsetWithinIndex* cada vez pelo tamanho dos dados da chamada anterior.</span><span class="sxs-lookup"><span data-stu-id="04308-144">If you get the index in chunks, increment *cbOffsetWithinIndex* each time by the size of the data from the previous call.</span></span>
4.  <span data-ttu-id="04308-145">Chame [**IMFMediaBuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) para obter um ponteiro para os dados do índice e o tamanho dos dados.</span><span class="sxs-lookup"><span data-stu-id="04308-145">Call [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) to get a pointer to the index data and the size of the data.</span></span>
5.  <span data-ttu-id="04308-146">Grave os dados de índice no arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="04308-146">Write the index data to the ASF file.</span></span>
6.  <span data-ttu-id="04308-147">Chame [**IMFMediaBuffer:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) para desbloquear o buffer de mídia.</span><span class="sxs-lookup"><span data-stu-id="04308-147">Call [**IMFMediaBuffer::Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) to unlock the media buffer.</span></span>
7.  <span data-ttu-id="04308-148">Repita as etapas 3 a 6 até que você tenha escrito o índice inteiro.</span><span class="sxs-lookup"><span data-stu-id="04308-148">Repeat steps 3–6 until you have written the entire index.</span></span>

<span data-ttu-id="04308-149">O código a seguir mostra estas etapas:</span><span class="sxs-lookup"><span data-stu-id="04308-149">The following code shows these steps:</span></span>


```C++
HRESULT WriteASFIndex(IMFASFIndexer *pIndex,IMFByteStream *pStream)
{
    const DWORD cbChunkSize = 4096;

    IMFMediaBuffer *pBuffer = NULL;

    QWORD cbIndex = 0;
    DWORD cbIndexWritten = 0;

    HRESULT hr = pIndex->GetIndexWriteSpace(&cbIndex);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFCreateMemoryBuffer(cbChunkSize, &pBuffer);
    if (FAILED(hr))
    {
        goto done;
    }

    while (cbIndexWritten < cbIndex)
    {
        BYTE *pData = NULL;
        DWORD cbData = 0;
        DWORD cbWritten = 0;

        hr = pIndex->GetCompletedIndex(pBuffer, cbIndexWritten);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pBuffer->Lock(&pData, NULL, &cbData);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pStream->Write(pData, cbData, &cbWritten);

        (void)pBuffer->Unlock();

        if (FAILED(hr))
        {
            goto done;
        }

        cbIndexWritten += cbData;
    }

done:
    SafeRelease(&pBuffer);
    return hr;
};
```



## <a name="related-topics"></a><span data-ttu-id="04308-150">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="04308-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04308-151">Indexador ASF</span><span class="sxs-lookup"><span data-stu-id="04308-151">ASF Indexer</span></span>](asf-index-object.md)
</dt> </dl>

 

 



