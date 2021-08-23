---
description: Este tópico descreve como usar a origem da sequência para reproduzir uma sequência de arquivos.
ms.assetid: 5a760492-bd52-40b8-a652-8a62646db6ae
title: Como criar uma lista de reprodução
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57d2a36735d29510e0622882a399fff199fd2289261453a51f281414b5076826
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828166"
---
# <a name="how-to-create-a-playlist"></a>Como criar uma lista de reprodução

Este tópico descreve como usar a origem da sequência para reproduzir uma sequência de arquivos.

## <a name="overview"></a>Visão geral

Para reproduzir arquivos de mídia em uma sequência, o aplicativo deve adicionar topologias em uma sequência para criar uma lista de reprodução e enfileirar essas topologias na sessão de mídia para reprodução.

A origem do sequenciador garante a reprodução contínua inicializando e carregando a próxima topologia antes que a sessão de mídia comece a reproduzir a topologia atual. Isso permite que o aplicativo inicie a próxima topologia rapidamente sempre que for necessário.

A sessão de mídia é responsável por alimentar dados para os coletores e reproduzir as topologias na origem da sequência. Além disso, a sessão de mídia gerencia o tempo de apresentação dos segmentos.

Para obter mais informações sobre como a origem do Sequencer gerencia topologias, consulte [sobre a origem do sequenciador](about-the-sequencer-source.md).

Este passo a passo contém as seguintes etapas:

1.  [Pré-requisitos](#prerequisites)
2.  [Inicializando Media Foundation](#initializing-media-foundation)
3.  [Criando objetos de Media Foundation](#creating-media-foundation-objects)
4.  [Criando a origem da mídia](#creating-the-media-source)
5.  [Criando topologias parciais](#creating-partial-topologies)
6.  [Adicionando topologias à origem do sequenciador](#adding-topologies-to-the-sequencer-source)
7.  [Definindo a primeira topologia na sessão de mídia](#setting-the-first-topology-on-the-media-session)
8.  [Enfileirando a próxima topologia na sessão de mídia](#queuing-the-next-topology-on-the-media-session)
9.  [Liberando a origem do sequenciador](#releasing-the-sequencer-source)

Os exemplos de código mostrados neste tópico são trechos do [código de exemplo de origem do sequenciador](sequencer-source-example-code.md)de tópico, que contém o código de exemplo completo.

## <a name="prerequisites"></a>Pré-requisitos

Antes de iniciar este passo a passo, familiarize-se com os seguintes conceitos de Media Foundation:

-   [Sessão de mídia](media-session.md)
-   [Topologias](topologies.md)
-   [Geradores de eventos de mídia](media-event-generators.md)
-   [Descritores de apresentação](presentation-descriptors.md)

Leia também [como reproduzir arquivos de mídia com Media Foundation](how-to-play-unprotected-media-files.md), pois o código de exemplo shwon aqui se expande no código desse tópico.

## <a name="initializing-media-foundation"></a>Inicializando Media Foundation

Antes de poder usar qualquer Media Foundation interfaces ou métodos, inicialize Media Foundation chamando a função [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) . Para obter mais informações, consulte [inicializando Media Foundation](initializing-media-foundation.md).


```C++
    hr = MFStartup(MF_VERSION);
```



## <a name="creating-media-foundation-objects"></a>Criando objetos de Media Foundation

Em seguida, crie os seguintes objetos de Media Foundation:

-   Sessão de mídia. Esse objeto expõe a interface [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) , que fornece métodos para reproduzir, pausar e parar a topologia atual.
-   Origem do sequenciador. Esse objeto expõe a interface [**IMFSequencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource) , que fornece métodos para adicionar, atualizar e excluir topologias em uma sequência.

1.  Chame a função [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) para criar a sessão de mídia.
2.  Chame [**IMFMediaEventQueue:: BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-begingetevent) para solicitar o primeiro evento da sessão de mídia.
3.  Chame a função [**MFCreateSequencerSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersource) para criar a origem do sequenciador.

O código a seguir cria a sessão de mídia e solicita o primeiro evento:


```C++
//  Create a new instance of the media session.
HRESULT CPlayer::CreateSession()
{
    // Close the old session, if any.
    HRESULT hr = CloseSession();
    if (FAILED(hr))
    {
        goto done;
    }

    assert(m_state == Closed);

    // Create the media session.
    hr = MFCreateMediaSession(NULL, &m_pSession);
    if (FAILED(hr))
    {
        goto done;
    }

    // Start pulling events from the media session
    hr = m_pSession->BeginGetEvent((IMFAsyncCallback*)this, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    m_state = Ready;

done:
    return hr;
}
```



## <a name="creating-the-media-source"></a>Criando a origem da mídia

Em seguida, crie uma fonte de mídia para o primeiro segmento de playlist. Use o [resolvedor de origem](source-resolver.md) para criar uma fonte de mídia a partir de uma URL. Para fazer isso, chame a função [**MFCreateSourceResolver**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesourceresolver) para criar um resolvedor de origem e, em seguida, chame o método [**IMFSourceResolver:: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) para criar a origem da mídia.

Para obter informações sobre fontes de mídia, consulte [fontes de mídia](media-sources.md).

## <a name="creating-partial-topologies"></a>Criando topologias parciais

Cada segmento na origem do sequenciador tem sua própria topologia parcial. Em seguida, crie topologias parciais para fontes de mídia. Para uma topologia parcial, os nós de origem da topologia são conectados diretamente aos nós de saída, sem especificar transformações intermediárias. A sessão de mídia usa o objeto de carregador de topologia para resolver a topologia. Depois que uma topologia é resolvida, os decodificadores necessários e outros nós de transformação são adicionados. A origem do sequenciador também pode conter topologias completas.

Para criar o objeto de topologia, use a função [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology) e, em seguida, use a interface [**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode) para criar nós de fluxo.

Para obter instruções completas sobre como usar esses elementos de programação para criar topologias, consulte [criando topologias de reprodução](creating-playback-topologies.md).

Um aplicativo pode reproduzir uma parte selecionada da fonte nativa Configurando o nó de origem. Para fazer isso, defina o atributo [**MF \_ TOPONODE \_ MEDIASTART**](mf-toponode-mediastart-attribute.md) e o atributo [**MF \_ TOPONODE \_ MEDIASTOP**](mf-toponode-mediastop-attribute.md) na topologia MF nós de topologia de **\_ \_ \_ nó SOURCESTREAM** . Especifique a hora de início da mídia e a hora de parada da mídia em relação ao início da origem nativa como tipos de **UINT64** .

## <a name="adding-topologies-to-the-sequencer-source"></a>Adicionando topologias à origem do sequenciador

Em seguida, adicione à origem do Sequencer as topologias parciais que você criou. Cada elemento Sequence, chamado *Segment*, é atribuído a um identificador **MFSequencerElementId** . Para obter mais informações sobre como a origem do Sequencer gerencia topologias, consulte [sobre a origem do sequenciador](about-the-sequencer-source.md).

Depois que todas as topologias são adicionadas à origem do sequenciador, o aplicativo deve sinalizar o último segmento na sequência para encerrar a reprodução no pipeline. Sem esse sinalizador, a origem do sequenciador espera que mais topologias sejam adicionadas.

1.  Chame o método [**IMFSequencerSource:: AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) para adicionar uma topologia específica à origem do sequenciador.

    ```C++
        hr = m_pSequencerSource->AppendTopology(
            pTopology, 
            SequencerTopologyFlags_Last, 
            &SegmentId
            );
    ```

    

    [**AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) adiciona a topologia especificada à sequência. Esse método retorna o identificador de segmento no parâmetro *pdwId* .

    Se a topologia for a última na origem do sequenciador, passe SequencerTopologyFlags \_ por último no parâmetro *dwFlags* . Esse valor é definido na enumeração [**MFSequencerTopologyFlags**](/windows/desktop/api/mfidl/ne-mfidl-mfsequencertopologyflags) .

2.  Chame [**IMFSequencerSource:: UpdateTopologyFlags**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopologyflags) para atualizar os sinalizadores para a topologia associada ao identificador de segmento na lista de entrada. Nesse caso, a chamada indica que o segmento especificado é o último segmento no Sequencer. (Essa chamada será opcional se a última topologia for especificada na chamada [**AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) .)

    ```C++
        BOOL bFirstSegment = (NumSegments() == 0);

        if (!bFirstSegment)
        {
            // Remove the "last segment" flag from the last segment.
            hr = m_pSequencerSource->UpdateTopologyFlags(LastSegment(), 0);
            if (FAILED(hr))
            {
                goto done;
            }
        }
    ```

    

O aplicativo pode substituir a topologia de um segmento por outra topologia chamando o [**IMFSequencerSource:: UpdateTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) e passando a nova topologia em *pTopology*. Se houver novas fontes nativas na nova topologia, as fontes serão adicionadas ao cache de origem. A lista de preversão também é atualizada.

## <a name="setting-the-first-topology-on-the-media-session"></a>Definindo a primeira topologia na sessão de mídia

Em seguida, enfileirar a primeira topologia na origem da sequência na sessão de mídia. Para obter a primeira topologia da origem do Sequencer, o aplicativo deve chamar o método [**IMFMediaSourceTopologyProvider:: GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) . Esse método retorna a topologia parcial, que é resolvida pela sessão de mídia.

Para obter informações sobre topologias parciais, consulte [about topologias](about-topologies.md).

1.  Recupere a origem de mídia nativa para a primeira topologia da origem da sequência.
2.  Crie um descritor de apresentação para a origem da mídia chamando o método [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) .
3.  Recupere a topologia associada para a apresentação chamando o método [**IMFMediaSourceTopologyProvider:: GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) .
4.  Defina a primeira topologia na sessão de mídia chamando [**IMFMediaSession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).

    Chame [**settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) com o parâmetro *DwSetTopologyFlags* definido como **nulo**. Isso instrui a sessão de mídia a iniciar a topologia especificada quando a topologia atual for concluída. Como nesse caso, a topologia especificada é a primeira topologia e não há apresentação atual, a sessão de mídia inicia a nova apresentação imediatamente.

    O valor **nulo** também indica que a sessão de mídia deve resolver a topologia porque a topologia retornada pelo provedor de topologia é sempre uma topologia parcial.


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



## <a name="queuing-the-next-topology-on-the-media-session"></a>Enfileirando a próxima topologia na sessão de mídia

Em seguida, o aplicativo precisa manipular o evento [MENewPresentation](menewpresentation.md) .

A origem do Sequencer gera [MENewPresentation](menewpresentation.md) quando a sessão de mídia começa a reproduzir um segmento que tem outro segmento após ele. Esse evento informa o aplicativo sobre a próxima topologia na origem da sequência, fornecendo o descritor de apresentação para o próximo segmento na lista de preversão. O aplicativo deve recuperar a topologia associada, usando o provedor de topologia e enfileirando-a na sessão de mídia. Em seguida, a origem do Sequencer então reverte essa topologia, o que garante uma transição tranqüila entre as apresentações.

Quando o aplicativo busca em segmentos, o aplicativo recebe vários eventos [MENewPresentation](menewpresentation.md) , pois a origem do sequenciador atualiza a lista de preversão e configura a topologia correta. O aplicativo deve tratar cada evento e enfileirar a topologia retornada nos dados do evento, na sessão de mídia. Para obter informações sobre como ignorar segmentos, consulte [usando a origem do sequenciador](using-the-sequencer-source.md).

Para obter informações sobre como obter notificações de origem do Sequencer, consulte [eventos de origem do Sequencer](sequencer-source-events.md).

1.  No manipulador de eventos [MENewPresentation](menewpresentation.md) , recupere o descritor de apresentação para o próximo segmento dos dados de evento.
2.  Obtenha a topologia associada para a apresentação chamando o método [**IMFMediaSourceTopologyProvider:: GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) .
3.  Defina a topologia na sessão de mídia chamando o método [**IMFMediaSession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) .

    A sessão de mídia inicia a nova apresentação quando a apresentação atual é concluída.


```C++
HRESULT CPlaylist::OnNewPresentation(IMFMediaEvent *pEvent)
{
    IMFPresentationDescriptor *pPD = NULL;

    HRESULT hr = GetEventObject(pEvent, &pPD);

    if (SUCCEEDED(hr))
    {
        // Queue the next segment on the media session
        hr = QueueNextSegment(pPD);
    }

    SafeRelease(&pPD);
    return hr;
}
```



## <a name="releasing-the-sequencer-source"></a>Liberando a origem do sequenciador

Por fim, desligue a origem do sequenciador. Para fazer isso, chame o método [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) na origem do sequenciador. Essa chamada desliga todas as fontes de mídia nativas subjacentes na origem do sequenciador.

Depois de liberar a origem do sequenciador, o aplicativo deve fechar e desligar a sessão de mídia chamando [**IMFMediaSession:: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) e [**IMFMediaSession:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown), nessa ordem.

Para evitar vazamentos de memória, o aplicativo deve liberar ponteiros para Media Foundation interfaces quando eles não forem mais necessários.

## <a name="next-steps"></a>Próximas etapas

Este guia passo a passo ilustra como criar uma lista de reprodução básica usando a origem do sequenciador. Depois de criar a lista de reprodução, talvez você queira adicionar recursos avançados, como ignorar o segmento, alterar o estado de reprodução e procurar dentro de um segmento. A lista a seguir fornece links para os tópicos relacionados:

-   [Como controlar os Estados de apresentação](how-to-control-presentation-states.md): a origem do sequenciador depende da sessão de mídia para fornecer controle de transporte como, reproduzir, pausar e parar.
-   [Como executar a depuração](how-to-perform-scrubbing.md) descreve as etapas necessárias para buscar uma posição específica em um fluxo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Origem do sequenciador](sequencer-source.md)
</dt> </dl>

 

 



