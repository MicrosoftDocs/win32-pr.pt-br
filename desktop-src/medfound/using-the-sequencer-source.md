---
description: Este tópico descreve como usar a origem do Sequencer.
ms.assetid: 7ce8dc67-02b1-4fd4-9e4d-6614fdb40620
title: Usando a origem do Sequencer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2b0607d65d02e507f576a5177ea432f3f7e0fab57c3b575fbb34240a46e91be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972725"
---
# <a name="using-the-sequencer-source"></a>Usando a origem do Sequencer

Este tópico descreve como usar a [Origem do Sequencer.](sequencer-source.md) Ele contém as seções a seguir:

-   [Visão geral](#overview)
-   [Adicionando topologias](#adding-topologies)
-   [Excluindo topologias](#deleting-topologies)
-   [Ignorando para um segmento](#skipping-to-a-segment)
-   [Tópicos relacionados](#related-topics)

Para uma visão geral da origem do sequenciador, consulte Sobre a [origem do Sequencer.](about-the-sequencer-source.md)

## <a name="overview"></a>Visão geral

A origem do sequenciador expõe as interfaces a seguir.



| Interface                                                                        | Descrição                                                                        |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                                         | Expõe a funcionalidade de fonte de mídia genérica.                                        |
| [**IMFSequencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource)                                 | Permite que o aplicativo adicione ou remova topologias.                               |
| [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider)         | Recupera a próxima topologia na fila na Sessão de Mídia.                         |
| [**IMFMediaSourcePresentationProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcepresentationprovider) | Usado pela Sessão de Mídia para encerrar segmentos. Os aplicativos não usam essa interface. |
| [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                                           | Consulta a origem do sequenciador para [Interfaces de Serviço](service-interfaces.md).     |



 

Para executar uma sequência de fontes de mídia, execute as seguintes etapas:

1.  Para criar a origem do sequenciador, chame a [**função MFCreateSequencerSource.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersource)
2.  Para cada segmento, crie uma topologia de reprodução, conforme descrito em [Criando topologias de reprodução.](creating-playback-topologies.md) Para adicionar a topologia à apresentação, chame [**IMFSequencerSource::AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology).
3.  Antes de iniciar a reprodução, chame [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) na origem do sequenciador. Esse método retorna um ponteiro para um descritor de apresentação para o primeiro segmento. Para obter a topologia associada a esse segmento, chame **QueryInterface** na origem do sequenciador para a interface [**IMFMediaSourceTopologyProvider.**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) Passe o descritor de apresentação para o [**método IMFMediaSourceTopologyProvider::GetMediaSourceTopology.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) Esse método retorna um ponteiro para a topologia.
4.  Passe a topologia do primeiro segmento para a Sessão de Mídia chamando o método [**IMFMediaSession::SetTopology da**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) Sessão de Mídia.
5.  Inicie a reprodução chamando [**IMFMediaSession::Start.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start)
6.  Quando a origem do sequenciador está pronta para pré-fazer o pré-roll do próximo segmento, ela envia um evento [MENewPresentation](menewpresentation.md) cujos dados de evento são um ponteiro de interface [**IMFPresentationDescriptor.**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) Novamente, obter a topologia do segmento chamando [**GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) na origem do sequenciador e definir a topologia na Sessão de Mídia chamando [**SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology). Não é necessário iniciar a fonte de mídia; ele passará automaticamente para o próximo segmento.
7.  Antes de o aplicativo ser encerrado, desligue a origem do sequenciador chamando [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).

O código a seguir mostra como obter a topologia e defini-la na Sessão de Mídia:


```C++
// Queues the next topology on the session.

HRESULT CPlaylist::QueueNextSegment(IMFPresentationDescriptor *pPD)
{
    IMFMediaSourceTopologyProvider *pTopoProvider = NULL;
    IMFTopology *pTopology = NULL;

    //Get the topology for the presentation descriptor
    HRESULT hr = m_pSequencerSource->QueryInterface(IID_PPV_ARGS(&pTopoProvider));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pTopoProvider->GetMediaSourceTopology(pPD, &pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    //Set the topology on the media session
    m_pSession->SetTopology(NULL, pTopology);

done:
    SafeRelease(&pTopoProvider);
    SafeRelease(&pTopology);
    return hr;
}
```



Para ver um exemplo de código completo, consulte [Código de exemplo de origem do Sequencer](sequencer-source-example-code.md).

## <a name="adding-topologies"></a>Adicionando topologias

A origem do sequenciador mantém duas listas de topologias: a *lista de entrada* e a lista de *pré-rolagem*.

A lista de entrada é uma coleção de topologias correspondentes a segmentos de playlist, na ordem em que foram adicionadas pelo aplicativo chamando [**IMFSequencerSource::AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology). Esse método atribui a cada topologia um *identificador* de segmento exclusivo do tipo **MFSequencerElementId**. O identificador de segmento é definido como um atributo para todos os nós de topologia de origem. Um aplicativo pode obter o identificador de segmento de um nó de origem usando o atributo [MF \_ TOPONODE \_ SEQUENCE \_ ELEMENTID.](mf-toponode-sequence-elementid-attribute.md) A lista de entrada poderá ter topologias duplicadas se o aplicativo chamado **AppendTopology** na mesma topologia mais de uma vez; no entanto, eles são identificados por seus identificadores de segmento exclusivos.

A lista de pré-lista é uma coleção de topologias de lista de entrada que foram inicializadas na preparação para reprodução. Isso permite que a Sessão de Mídia transicionar para a próxima topologia perfeitamente quando a topologia ativa terminar. O aplicativo não pode adicionar ou remover topologias diretamente da lista de pré-registro; ele é gerado pela origem do sequenciador quando uma topologia da lista de entrada é selecionada para reprodução. Isso faz com que a origem do sequenciador adicione a próxima topologia da lista de entrada à lista de pré-lista. Depois de fazer isso, a origem do sequenciador aciona de forma assíncrona o evento [MENewPresentation](menewpresentation.md) e passa o descritor de apresentação para a topologia de pré-inscrição como dados de evento. O aplicativo deve escutar esse evento usando a interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) da Sessão de Mídia e colocar a topologia de pré-registro na sessão de mídia chamando [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology). Isso deve ser feito antes que a Sessão de Mídia conclua a reprodução da topologia ativa. **SetTopology** informa à Sessão de Mídia sobre a próxima topologia que ele deve reproduzir após o fim da reprodução da topologia ativa. Para garantir uma confirmação contínua, o aplicativo deve chamar **SetTopology** antes que a Sessão de Mídia seja concluída, ao tocar a topologia anterior. Caso contrário, haverá uma lacuna entre os segmentos.

O [evento MENewPresentation](menewpresentation.md) é gerado desde que haja uma topologia após a topologia ativa. Consequentemente, se a lista de entrada contiver apenas uma topologia ou se a topologia ativa for a última na lista de entrada, esse evento não será gerado.

A lista de pré-lista é sincronizada com a lista de entrada e é atualizada sempre que uma topologia é adicionada ou excluída da lista de entrada.

## <a name="deleting-topologies"></a>Excluindo topologias

Para remover uma topologia da origem do sequenciador, um aplicativo deve chamar o método [**IMFSequencerSource::D eleteTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-deletetopology) e especificar o identificador de segmento.

Antes de [**chamar DeleteTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-deletetopology), o aplicativo deve garantir que a Sessão de Mídia não está usando a topologia que o aplicativo deseja excluir. Para fazer isso, ambos os seguintes devem ocorrer antes que o aplicativo chama **DeleteTopology**:

-   [O evento MESessionTopologyStatus](mesessiontopologystatus.md) com MF TOPOSTATUS ENDED é recebido para a topologia para garantir que a Sessão de Mídia \_ tenha concluído a \_ reprodução.

-   [MESessionTopologyStatus](mesessiontopologystatus.md) com MF TOPOSTATUS STARTED SOURCE é recebido para a próxima topologia para garantir que a Sessão de Mídia tenha iniciado a reprodução da próxima topologia, o evento \_ \_ \_ [MESessionEnded](mesessionended.md) é recebido para garantir que a Sessão de Mídia seja feita com a última topologia na origem do sequenciador.

Se o segmento que está sendo excluído for a topologia ativa, a reprodução será interrompida e a origem do sequenciador acionará o [evento MEEndOfPresentationSegment.](meendofpresentationsegment.md) Se a topologia ativa também for a última topologia, [o evento MEEndOfPresentation](meendofpresentation.md) será gerado.

## <a name="skipping-to-a-segment"></a>Ignorando para um segmento

Um aplicativo pode pular para um segmento específico na sequência iniciando a Sessão [de](media-session.md) Mídia com um deslocamento de segmento, da seguinte forma:

1.  Chame a [**função MFCreateSequencerSegmentOffset**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersegmentoffset) para criar o deslocamento do segmento. Especifique o identificador do segmento no *parâmetro dwId.* (O identificador foi retornado pelo método [**IMFSequencerSource::AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) quando você adicionou pela primeira vez a topologia à origem do sequenciador.) O *parâmetro hnsOffset* especifica um deslocamento de tempo, relativo ao início do segmento. A reprodução será iniciada neste momento. Para o *parâmetro pvarSegmentOffset,* passe o endereço de um **PROPVARIANT vazio.** Quando a função retorna, esse **PROPVARIANT** contém o deslocamento de segmento.

2.  Chame o [**método IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) na Sessão de Mídia. Para o *parâmetro pguidTimeFormat,* use o valor GUID MF \_ TIME FORMAT SEGMENT \_ \_ \_ OFFSET. Esse valor indica a busca por deslocamento de segmento. Para o *parâmetro pvarStartPosition,* passe o endereço do **PROPVARIANT** criado na etapa anterior.

O exemplo de código a seguir mostra como pular para o início de um segmento especificado em uma sequência.


```C++
// Skips to the specified segment in the sequencer source

HRESULT CPlaylist::SkipTo(DWORD index)
{
    if (index >= m_count)
    {
        return E_INVALIDARG;
    }

    MFSequencerElementId ID = m_segments[index].SegmentID;

    PROPVARIANT var;

    HRESULT hr = MFCreateSequencerSegmentOffset(ID, NULL, &var);
    
    if (SUCCEEDED(hr))
    {
        hr = m_pSession->Start(&MF_TIME_FORMAT_SEGMENT_OFFSET, &var);
        PropVariantClear(&var);
    }
    return hr;
}
```



Quando o aplicativo busca entre segmentos, o aplicativo recebe vários eventos à medida que a origem do sequenciador encerra o segmento atual e se prepara para reproduzir o novo segmento. Como esses eventos são recebidos de forma assíncrona, é difícil prever a sequência exata de eventos. Esses eventos são os seguinte:

-   A origem do sequenciador envia [um evento MENewPresentation](menewpresentation.md) para o novo segmento ao qual a Sessão de Mídia está ignorando.

-   Quando a origem do sequenciador encerra o segmento ativo, ela envia [o evento MEEndOfPresentationSegment.](meendofpresentationsegment.md)
-   Em seguida, a origem do sequenciador cancela a topologia de pré-registros. Isso resulta nos seguintes eventos para a topologia cancelada:

    -   [Evento MESessionTopologyStatus](mesessiontopologystatus.md) com o sinalizador MF \_ TOPOSTATUS \_ READY.
    -   [Evento MESessionTopologyStatus](mesessiontopologystatus.md) com o sinalizador MF \_ TOPOSTATUS \_ STARTED \_ SOURCE.
    -   [Evento MEEndOfPresentationSegment](meendofpresentationsegment.md) com o atributo [ \_ MF EVENT \_ SOURCE \_ TOPOLOGY \_ CANCELED](mf-event-source-topology-canceled-attribute.md) para indicar que a topologia foi cancelada pela origem do sequenciador.

-   Em seguida, a origem do sequenciador envia eventos para o novo segmento, incluindo vários [eventos MESessionTopologyStatus.](mesessiontopologystatus.md)
-   Se o novo segmento não for o último da lista, a origem do sequenciador atualizará a lista de pré-lançamento e acionará outra [MENewPresentation](menewpresentation.md) para a nova topologia de pré-lançamento. Para obter informações sobre topologias na lista de pré-lista, consulte [Sobre a origem do Sequencer.](about-the-sequencer-source.md)

Mais detalhes sobre os eventos enviados pela origem do sequenciador podem ser encontrados no tópico Eventos de [origem do Sequencer](sequencer-source-events.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como criar uma playlist](how-to-create-a-playlist.md)
</dt> <dt>

[Origem do sequenciador](sequencer-source.md)
</dt> </dl>

 

 



