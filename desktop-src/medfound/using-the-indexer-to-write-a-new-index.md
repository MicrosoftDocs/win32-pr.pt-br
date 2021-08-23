---
description: Este tópico mostra como gravar um índice para um arquivo ASF (Advanced Systems Format).
ms.assetid: a14e3bef-0232-4259-930a-d860ed9230fd
title: Usando o indexador para gravar um novo índice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9fbc604a9493f7feea61e34500e0f620a051b05b1431ec2d4917df9f8ed15b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034524"
---
# <a name="using-the-indexer-to-write-a-new-index"></a>Usando o indexador para gravar um novo índice

Este tópico mostra como gravar um índice para um arquivo ASF (Advanced Systems Format).

Aqui está o procedimento geral para criar um índice ASF:

1.  Inicialize uma nova instância do objeto do indexador ASF, conforme descrito em [criação e configuração do indexador](indexer-creation-and-configuration.md).
2.  Opcionalmente, configure o indexador.
3.  Enviar pacotes de dados ASF para o indexador.
4.  Confirme o índice.
5.  Obtenha o índice concluído do indexador e grave-o em um fluxo.

## <a name="configure-the-indexer"></a>Configurar o indexador

Para usar o indexador para gravar um novo objeto de índice, o objeto indexador deve ter o sinalizador MFASF \_ \_ gravar \_ novo conjunto de \_ índice com uma chamada para [**IMFASFIndexer:: SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) antes de ser inicializado com [**IMFASFIndexer:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize).

Quando o indexador é configurado para gravar um índice, o chamador escolhe os fluxos a serem indexados. Por padrão, o indexador tenta criar um objeto de índice para todos os fluxos. O intervalo de tempo padrão é de um segundo.

[**IMFASFIndexer:: SetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus) pode ser usado para substituir a opção padrão do objeto indexer de fluxos e tipos de índice.

O código de exemplo a seguir mostra a inicialização de \_ um \_ descritor de índice ASF e um \_ identificador de índice ASF \_ antes de uma chamada para [**SetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus).


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



O identificador de índice deve ter o tipo de índice GUID definido como GUID \_ NULL para indicar que o tipo de índice será baseado em tempo de apresentação. O identificador de índice também deve ser inicializado com o número de fluxo do fluxo de ASF a ser indexado. Depois que o identificador de índice for definido, use-o para inicializar o descritor de índice.

A estrutura do descritor de índice tem membros que devem ser definidos antes da chamada para [**SetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus). O **identificador** é uma estrutura de [**\_ \_ identificador de índice ASF**](/windows/desktop/api/wmcontainer/ns-wmcontainer-asf_index_identifier) que identifica o número de fluxo e o tipo de índice. **cPerEntryBytes** é o número de bytes usados para cada entrada de índice. Se o valor for MFASFINDEXER \_ por \_ bytes de entrada \_ \_ dinâmicos, as entradas de índice terão tamanho variável. **dwInterval** é o intervalo de indexação. Um valor de MFASFINDEXER \_ nenhum \_ \_ intervalo fixo indica que não há nenhum intervalo de indexação fixo.

## <a name="send-asf-data-packets-to-the-indexer"></a>Enviar pacotes de dados ASF para o indexador

Como o indexador é um objeto de nível WMContainer, ele deve ser usado em conjunto com o multiplexador durante a geração de pacotes.

Os pacotes retornados de [**GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) podem ser enviados ao objeto indexador por meio de chamadas para [**GenerateIndexEntries**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-generateindexentries) , em que ele cria entradas de índice para cada pacote enviado.

O código a seguir demonstra como isso pode ser feito:


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



Para obter mais informações, consulte [gerando novos pacotes de dados ASF](generating-new-asf-data-packets.md).

## <a name="commit-the-index"></a>Confirmar o índice

Depois que o último pacote tiver uma entrada de índice criada para ele, o índice deverá ser confirmado. Isso é feito com uma chamada para [**IMFASFIndexer:: CommitIndex**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-commitindex). **CommitIndex** usa um ponteiro para o objeto ContentInfo que descreve o conteúdo do arquivo asf. A confirmação do índice conclui a indexação e atualiza o cabeçalho com novas informações sobre o tamanho do arquivo e a buscabilidade.

## <a name="get-the-completed-index"></a>Obter o índice concluído

Para obter o índice concluído do indexador, execute as seguintes etapas:

1.  Chame [**IMFASFIndexer:: GetIndexWriteSpace**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexwritespace) para obter o tamanho do índice.
2.  Chame [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) para criar um buffer de mídia. Você pode alocar um buffer que seja grande o suficiente para manter o índice inteiro, de alocar um buffer menor e obter o índice em partes.
3.  Chame [**IMFASFIndexer:: GetCompletedIndex**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getcompletedindex) para obter os dados do índice. Na primeira chamada, defina o parâmetro *cbOffsetWithinIndex* como zero. Se você obter o índice em partes, incrementar *cbOffsetWithinIndex* cada vez pelo tamanho dos dados da chamada anterior.
4.  Chame [**IMFMediaBuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) para obter um ponteiro para os dados do índice e o tamanho dos dados.
5.  Grave os dados de índice no arquivo ASF.
6.  Chame [**IMFMediaBuffer:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) para desbloquear o buffer de mídia.
7.  Repita as etapas 3 a 6 até que você tenha escrito o índice inteiro.

O código a seguir mostra essas etapas:


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Indexador ASF](asf-index-object.md)
</dt> </dl>

 

 



