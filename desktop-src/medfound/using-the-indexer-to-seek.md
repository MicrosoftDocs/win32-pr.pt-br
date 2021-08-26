---
description: O indexador ASF é um componente de camada WMContainer usado para ler ou gravar objetos de índice em um arquivo ASF (Advanced Systems Format). Este tópico fornece informações sobre como usar o indexador ASF para buscar em um arquivo ASF.
ms.assetid: 9c501d33-847e-448e-a19c-39dfbc7757ca
title: Usando o indexador para buscar dentro de um arquivo ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3c674aa809c858856abf0c0e84c5d854b399c6fbc125ac9210e19b695380bd0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887236"
---
# <a name="using-the-indexer-to-seek-within-an-asf-file"></a>Usando o indexador para buscar dentro de um arquivo ASF

O *indexador* ASF é um componente de camada WMContainer usado para ler ou gravar objetos de índice em um arquivo ASF (Advanced Systems Format). Este tópico fornece informações sobre como usar o indexador ASF para buscar em um arquivo ASF.

-   [Inicializando o indexador para busca](#initializing-the-indexer-for-seeking)
-   [Obter a posição de busca.](#getting-the-seek-position)
-   [Tópicos relacionados](#related-topics)

Para obter informações sobre a estrutura de um arquivo ASF, consulte [Estrutura de arquivos ASF](asf-file-structure.md).

## <a name="initializing-the-indexer-for-seeking"></a>Inicializando o indexador para busca

Para inicializar o indexador ASF para busca:

1.  Chame [**MFCreateASFIndexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexer) para criar uma nova instância do indexador ASF.
2.  Chame [**IMFASFIndexer::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize) para inicializar o indexador. Esse método obtém informações do header ASF para determinar quais fluxos ASF são indexados. Por padrão, o objeto indexador é configurado para busca.
3.  Chame [**IMFASFIndexer::GetIndexPosition**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexposition) para encontrar o deslocamento do índice dentro do arquivo ASF.
4.  Chame a [**função MFCreateASFIndexerByteStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexerbytestream) para criar um fluxo de byte para ler o índice. A entrada para essa função é um ponteiro para um fluxo de byte que contém o arquivo ASF e o deslocamento do índice (da etapa anterior).
5.  Chame [**IMFASFIndexer::SetIndexByteStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexbytestreams) para definir o fluxo de byte de índice no indexador.

O código a seguir mostra essas etapas:


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



## <a name="getting-the-seek-position"></a>Obter a posição de busca.

1.  Para descobrir se um fluxo específico está indexado, chame [**IMFASFIndexer::GetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexstatus). Se o fluxo for indexado, o *parâmetro pfIsIndexed* receberá o valor **TRUE**; caso contrário, ele receberá o valor **FALSE.**
2.  Por padrão, o indexador usa a busca de encaminhamento. Para busca inversa (ou seja, buscando desde o final do arquivo), chame [**IMFASFIndexer::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) e defina o sinalizador **MFASF \_ INDEXER \_ READ FOR \_ \_ REVERSEPLAYBACK.** Caso contrário, pule essa etapa.
3.  Se o fluxo for indexado, obter a posição de busca para um tempo de apresentação especificado chamando [**IMFASFIndexer::GetSeekPositionForValue**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getseekpositionforvalue). Esse método lê o índice ASF e localiza a entrada de índice mais próxima da hora solicitada. O método retorna o deslocamento de byte do pacote de dados especificado pela entrada de índice. O deslocamento de byte é relativo ao início do objeto de dados ASF.

O [**método GetSeekPositionForValue**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getseekpositionforvalue) leva um ponteiro para a [**estrutura ASF INDEX \_ \_ IDENTIFIER.**](/windows/desktop/api/wmcontainer/ns-wmcontainer-asf_index_identifier) Essa estrutura especifica um tipo de índice e um identificador de fluxo. Atualmente, o tipo de índice deve ser GUID \_ NULL, que especifica a indexação baseada em tempo.

O código a seguir obtém uma posição de busca, considerando um identificador de fluxo e o tempo de apresentação de destino. Se a chamada for bem-sucedida, ela retornará o deslocamento de dados no parâmetro *pcbDataOffset* e o tempo de busca real aproximado *em phnsApproxSeekTime*.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Indexador ASF](asf-index-object.md)
</dt> </dl>

 

 



