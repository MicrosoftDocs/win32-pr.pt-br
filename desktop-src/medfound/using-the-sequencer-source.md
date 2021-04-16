---
description: Este tópico descreve como usar a origem do Sequencer.
ms.assetid: 7ce8dc67-02b1-4fd4-9e4d-6614fdb40620
title: Usando a origem do sequenciador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba99202838fbdc8be86f2f1d8931e5aa99ae9bf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765330"
---
# <a name="using-the-sequencer-source"></a>Usando a origem do sequenciador

Este tópico descreve como usar a [origem do Sequencer](sequencer-source.md). Ele contém as seções a seguir:

-   [Visão geral](#overview)
-   [Adicionando topologias](#adding-topologies)
-   [Excluindo topologias](#deleting-topologies)
-   [Ignorando para um segmento](#skipping-to-a-segment)
-   [Tópicos relacionados](#related-topics)

Para obter uma visão geral da origem do sequenciador, consulte [sobre a origem do sequenciador](about-the-sequencer-source.md).

## <a name="overview"></a>Visão geral

A origem do sequenciador expõe as interfaces a seguir.



| Interface                                                                        | Descrição                                                                        |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                                         | Expõe a funcionalidade de origem de mídia genérica.                                        |
| [**IMFSequencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource)                                 | Permite que o aplicativo adicione ou remova topologias.                               |
| [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider)         | Recupera a próxima topologia a ser enfileirada na sessão de mídia.                         |
| [**IMFMediaSourcePresentationProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcepresentationprovider) | Usado pela sessão de mídia para segmentos finais. Os aplicativos não usam essa interface. |
| [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                                           | Consulta a origem do sequenciador para [interfaces de serviço](service-interfaces.md).     |



 

Para reproduzir uma sequência de fontes de mídia, execute as seguintes etapas:

1.  Para criar a origem do sequenciador, chame a função [**MFCreateSequencerSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersource) .
2.  Para cada segmento, crie uma topologia de reprodução, conforme descrito em [criando topologias de reprodução](creating-playback-topologies.md). Para adicionar a topologia à apresentação, chame [**IMFSequencerSource:: AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology).
3.  Antes de iniciar a reprodução, chame [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) na origem do sequenciador. Esse método retorna um ponteiro para um descritor de apresentação para o primeiro segmento. Para obter a topologia associada a esse segmento, chame **QueryInterface** na origem do sequenciador para a interface [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) . Passe o descritor de apresentação para o método [**IMFMediaSourceTopologyProvider:: GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) . Esse método retorna um ponteiro para a topologia.
4.  Passe a topologia do primeiro segmento para a sessão de mídia chamando o método [**IMFMediaSession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) da sessão de mídia.
5.  Inicie a reprodução chamando [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).
6.  Quando a origem do sequenciador está pronta para lançar o próximo segmento, ele envia um evento [MENewPresentation](menewpresentation.md) cujos dados de evento são um ponteiro de interface [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) . Novamente, obtenha a topologia para o segmento chamando [**GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) na origem do sequenciador e defina a topologia na sessão de mídia chamando [**settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology). Não é necessário reiniciar a origem da mídia; Ele passará automaticamente para o próximo segmento.
7.  Antes de o aplicativo sair, desligue a origem do sequenciador chamando [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).

O código a seguir mostra como obter a topologia e defini-la na sessão de mídia:


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



Para obter um exemplo de código completo, consulte [código de exemplo de origem do Sequencer](sequencer-source-example-code.md).

## <a name="adding-topologies"></a>Adicionando topologias

A origem do sequenciador mantém duas listas de topologias: a *lista de entrada* e a *lista de preversão*.

A lista de entrada é uma coleção de topologias correspondentes aos segmentos de playlist, na ordem em que foram adicionadas pelo aplicativo chamando [**IMFSequencerSource:: AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology). Esse método atribui a cada topologia um identificador de *segmento* exclusivo do tipo **MFSequencerElementId**. O identificador de segmento é definido como um atributo para todos os nós de topologia de origem. Um aplicativo pode obter o identificador de segmento a partir de um nó de origem usando o atributo [MF \_ TOPONODE \_ Sequence \_ ElementID](mf-toponode-sequence-elementid-attribute.md) . A lista de entrada pode ter topologias duplicadas se o aplicativo chamou **AppendTopology** na mesma topologia mais de uma vez; no entanto, elas são identificadas por seus identificadores de segmento exclusivos.

A lista de preversão é uma coleção de topologias de lista de entrada que foram inicializadas na preparação para reprodução. Isso permite que a sessão de mídia seja transferida para a próxima topologia diretamente quando a topologia ativa termina. O aplicativo não pode adicionar ou remover topologias diretamente da lista de preversão; Ele é gerado pela origem do sequenciador quando uma topologia da lista de entrada é selecionada para reprodução. Isso faz com que a origem do sequenciador adicione a próxima topologia da lista de entrada à lista de preversão. Depois de fazer isso, a origem do Sequencer gera de forma assíncrona o evento [MENewPresentation](menewpresentation.md) e passa o descritor de apresentação para a topologia de preversão como dados de evento. O aplicativo deve escutar esse evento usando a interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) da sessão de mídia e enfileirar a topologia de preversão na sessão de mídia chamando [**IMFMediaSession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology). Isso deve ser feito antes que a sessão de mídia conclua a reprodução da topologia ativa. **Settopology** informa a sessão de mídia sobre a próxima topologia que ela deve reproduzir após o término da reprodução da topologia ativa. Para garantir um treansition contínuo, o aplicativo deve chamar **settopology** antes que a sessão de mídia conclua a execução da topologia anterior. Caso contrário, haverá uma lacuna entre os segmentos.

O evento [MENewPresentation](menewpresentation.md) é gerado contanto que haja uma topologia após a topologia ativa. Consequentemente, se a lista de entrada contiver apenas uma topologia ou se a topologia ativa for a última na lista de entrada, esse evento não será gerado.

A lista de preversão é sincronizada com a lista de entrada e é atualizada toda vez que uma topologia é adicionada ou excluída da lista de entrada.

## <a name="deleting-topologies"></a>Excluindo topologias

Para remover uma topologia da origem do Sequencer, um aplicativo deve chamar o método [**IMFSequencerSource::D eletetopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-deletetopology) e especificar o identificador do segmento.

Antes de chamar [**DeleteTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-deletetopology), o aplicativo deve garantir que a sessão de mídia não esteja usando a topologia que o aplicativo deseja excluir. Para fazer isso, os dois itens a seguir devem ocorrer antes que o aplicativo chame **DeleteTopology**:

-   O evento [MESessionTopologyStatus](mesessiontopologystatus.md) com MF \_ TOPOSTATUS \_ encerrado é recebido para a topologia para garantir que a sessão de mídia concluiu a reprodução.

-   [MESessionTopologyStatus](mesessiontopologystatus.md) com a \_ origem MF TOPOSTATUS \_ iniciada \_ é recebida para a próxima topologia para garantir que a sessão de mídia tenha iniciado a reprodução da próxima topologia, o evento [MESessionEnded](mesessionended.md) é recebido para garantir que a sessão de mídia seja feita com a última topologia na origem do sequenciador.

Se o segmento que está sendo excluído for a topologia ativa, a reprodução será interrompida e a origem do sequenciador gerará o evento [MEEndOfPresentationSegment](meendofpresentationsegment.md) . Se a topologia ativa também for a última topologia, o evento [MEEndOfPresentation](meendofpresentation.md) será gerado.

## <a name="skipping-to-a-segment"></a>Ignorando para um segmento

Um aplicativo pode pular para um segmento específico na sequência iniciando a sessão de [mídia](media-session.md) com um deslocamento de segmento, da seguinte maneira:

1.  Chame a função [**MFCreateSequencerSegmentOffset**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersegmentoffset) para criar o deslocamento de segmento. Especifique o identificador do segmento no parâmetro *dwID* . (O identificador foi retornado pelo método [**IMFSequencerSource:: AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) quando você adicionou pela primeira vez a topologia à origem do sequenciador.) O parâmetro *hnsOffset* especifica um deslocamento de tempo, em relação ao início do segmento. A reprodução será iniciada no momento. Para o parâmetro *pvarSegmentOffset* , passe o endereço de um **PROPVARIANT** vazio. Quando a função retorna, esse **PROPVARIANT** contém o deslocamento de segmento.

2.  Chame o método [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) na sessão de mídia. Para o parâmetro *pguidTimeFormat* , use o deslocamento de segmento do formato de tempo MF do valor do GUID \_ \_ \_ \_ . Esse valor indica a busca por deslocamento de segmento. Para o parâmetro *pvarStartPosition* , passe o endereço do **PROPVARIANT** criado na etapa anterior.

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



Quando o aplicativo busca em segmentos, o aplicativo recebe vários eventos, pois a origem do sequenciador encerra o segmento atual e se prepara para reproduzir o novo segmento. Como esses eventos são recebidos de forma assíncrona, é difícil prever a sequência exata de eventos. Esses eventos são os seguintes:

-   A origem do sequenciador envia um evento [MENewPresentation](menewpresentation.md) para o novo segmento ao qual a sessão de mídia está sendo ignorada.

-   Quando a origem do sequenciador encerra o segmento ativo, ele envia o evento [MEEndOfPresentationSegment](meendofpresentationsegment.md) .
-   A origem do sequenciador, em seguida, cancela a topologia de preroll. Isso resulta nos seguintes eventos para a topologia cancelada:

    -   Evento [MESessionTopologyStatus](mesessiontopologystatus.md) com o \_ sinalizador MF TOPOSTATUS \_ Ready.
    -   Evento [MESessionTopologyStatus](mesessiontopologystatus.md) com o \_ sinalizador de origem MF TOPOSTATUS \_ iniciado \_ .
    -   Evento [MEEndOfPresentationSegment](meendofpresentationsegment.md) com o atributo de [topologia de origem de evento MF \_ \_ \_ \_ cancelado](mf-event-source-topology-canceled-attribute.md) para indicar que a topologia foi cancelada pela origem do sequenciador.

-   Em seguida, a origem do sequenciador envia eventos para o novo segmento, incluindo vários eventos [MESessionTopologyStatus](mesessiontopologystatus.md) .
-   Se o novo segmento não for o último na lista, a origem do sequenciador atualizará a lista de preversão e gerará outro [MENewPresentation](menewpresentation.md) para a nova topologia de preroll. Para obter informações sobre topologias na lista de preversão, consulte [sobre a origem do sequenciador](about-the-sequencer-source.md).

Mais detalhes sobre os eventos enviados pela origem do sequenciador podem ser encontrados no tópico [eventos de origem do Sequencer](sequencer-source-events.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como criar uma lista de reprodução](how-to-create-a-playlist.md)
</dt> <dt>

[Origem do sequenciador](sequencer-source.md)
</dt> </dl>

 

 



