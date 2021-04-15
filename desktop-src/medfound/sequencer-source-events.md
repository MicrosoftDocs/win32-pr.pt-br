---
description: Eventos de origem do Sequencer
ms.assetid: 28654bae-9ce2-467b-b769-63279d69b173
title: Eventos de origem do Sequencer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdf97cc5ff25c8a5fc40fa4990bf38c652f94e63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760726"
---
# <a name="sequencer-source-events"></a>Eventos de origem do Sequencer

Quando a [origem do sequenciador](sequencer-source.md) reproduz uma sequência de arquivos, a sessão de mídia geralmente envia todos os mesmos eventos que são enviados durante a reprodução normal e que são listados em [eventos de sessão de mídia](media-session-events.md). O aplicativo obtém esses eventos usando a interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) da sessão de mídia.

Além disso, há alguns eventos que são específicos para segmentos de playlist.



| Evento                                                                                                   | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MENewPresentation](menewpresentation.md)                                                              | Sinaliza o aplicativo para preverter a próxima topologia.<br/> Para fornecer uma transição direta entre duas apresentações consecutivas, a origem do sequenciador carrega a próxima topologia com antecedência. Embora a topologia ativa ainda esteja sendo executada, a origem do sequenciador envia esse evento para a próxima topologia, desde que haja uma topologia subsequente disponível na origem.<br/> Esses dados de evento para esse evento são o descritor de apresentação para a próxima topologia. O aplicativo é responsável por definir a topologia correspondente na sessão de mídia, conforme descrito em [usando a origem do sequenciador](using-the-sequencer-source.md).<br/> |
| [MEEndOfPresentationSegment](meendofpresentationsegment.md)                                            | A origem do sequenciador gerará esse evento quando a sessão de mídia tiver concluído a reprodução do segmento atual, se esse segmento for seguido por outro segmento. (Se o segmento atual for o último, a origem do sequenciador gerará o evento [MEEndOfPresentation](meendofpresentation.md) em vez disso.)<br/> A sessão de mídia encaminha esse evento para o aplicativo. Normalmente, o aplicativo recebe [MEEndOfPresentationSegment](meendofpresentationsegment.md) depois que a sessão de mídia começou a processar o próximo segmento, mas enquanto os coletores de mídia ainda estão fornecendo os exemplos para o segmento anterior.<br/>                            |
| [MESessionTopologyStatus](mesessiontopologystatus.md), com status **MF \_ TOPOSTATUS \_ Sink \_ alternado**. | A sessão de mídia gera esse evento quando faz uma transição para a próxima topologia na origem do sequenciador e os coletores de mídia concluíram a execução da topologia anterior. Esse evento contém um ponteiro para a próxima topologia.                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="example-1-playback-without-skipping"></a>Exemplo 1: reprodução sem ignorar

Quando a origem do sequenciador está envolvida, o número de eventos obtidos da sessão de mídia pode ser confuso, especialmente porque os eventos associados a um segmento geralmente são intercalados com eventos para o próximo segmento.

No primeiro exemplo, o aplicativo enfileira três segmentos, S1, S2 e S3. O terceiro segmento tem o **\_ último sinalizador SequencerTopologyFlags** para sinalizar que é o último segmento na sequência. O segmento ao qual cada evento corresponde é fornecido entre parênteses. As chamadas [**settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) do aplicativo também são listadas para tornar a ordem das operações mais clara.

-   Chamadas de aplicativo [**IMFMediaSession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) (S1)
-   [MESessionTopologySet](mesessiontopologyset.md) (S1)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ Ready** (S1)
-   [MENewPresentation](menewpresentation.md) (S2)
-   O aplicativo chama [**IMFMediaSession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) (S2)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ iniciou \_ origem** (início de S1)
-   [MESessionTopologySet](mesessiontopologyset.md) (S2)
-   [MEEndOfPresentationSegment](meendofpresentationsegment.md) (fim de S1)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ encerrado** (S1)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **\_ coletor de TOPOSTATUS MF \_ \_ alternado** (transição para S2)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ Ready** (S2)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ iniciou \_ origem** (início de S2)
-   [MENewPresentation](menewpresentation.md) (preversão S3)
-   O aplicativo chama [**IMFMediaSession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) (S2)
-   [MESessionTopologySet](mesessiontopologyset.md) (S3)
-   [MEEndOfPresentationSegment](meendofpresentationsegment.md) (fim de S2)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ encerrado** (S2)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **o \_ coletor TOPOSTATUS do MF foi \_ \_ alternado** (transição para S3)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ Ready** (S3)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ iniciou \_ origem** (início de S3)
-   [MEEndOfPresentation](meendofpresentation.md) (fim do S3; último segmento)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ encerrado**
-   [MESessionEnded](mesessionended.md)

Essa lista não inclui todos os eventos que você possa receber. (Por exemplo, ele omite o evento [MESessionCapabilitiesChanged](mesessioncapabilitieschanged.md) , que é enviado sempre que os recursos da sessão são alterados. Um aplicativo normalmente recebe vários eventos MESessionCapabilitiesChanged em uma apresentação.) Os eventos listados aqui são aqueles que mostram a transição de um segmento para o próximo. Os eventos mais importantes são [MENewPresentation](menewpresentation.md), que sinalizam o aplicativo para a próxima topologia, e [MEEndOfPresentationSegment](meendofpresentationsegment.md), que sinaliza o final de um segmento (exceto para o último segmento).

Como os eventos em Media Foundation são assíncronos e não são serializados com chamadas de método, a ordem exata pode variar. Por exemplo, você pode receber **a \_ origem MF TOPOSTATUS \_ iniciada \_** para S1 antes que o aplicativo chame [**settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) para S2.

Além disso, você pode não obter todos os eventos listados aqui. Os eventos [MEEndOfPresentation](meendofpresentation.md) e [MESessionEnded](mesessionended.md) , por exemplo, não são enviados, a menos que o último segmento tenha o **\_ último sinalizador SequencerTopologyFlags** .

Por fim, essa lista não indica a passagem do tempo. O tempo de "início de S1" para "fim de S1" é a duração total de S1, que pode ser de alguns segundos ou várias horas, dependendo da origem.

## <a name="example-2-playback-with-segment-skipping"></a>Exemplo 2: reprodução com o segmento ignorando

Neste exemplo, o aplicativo enfileira os mesmos segmentos, mas pula para o segmento 3 enquanto o segmento 1 está sendo reproduzido. Nesse caso, os seguintes eventos são enviados:

-   Chamadas de aplicativo [**IMFMediaSession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) (S1)
-   [MESessionTopologySet](mesessiontopologyset.md) (S1)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ Ready** (S1)
-   [MENewPresentation](menewpresentation.md) (S2)
-   O aplicativo chama [**IMFMediaSession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) (S2)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ iniciou \_ origem** (início de S1)
-   [MESessionTopologySet](mesessiontopologyset.md) (S2)
-   O aplicativo chama [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) (pular para S3)
-   [MENewPresentation](menewpresentation.md) (preversão S3)
-   O aplicativo chama [**IMFMediaSession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) (S3)
-   [MESessionStarted](mesessionstarted.md)
-   [MEEndOfPresentationSegment](meendofpresentationsegment.md) (S1 cancelado)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ encerrado** (S1)
-   [MESessionTopologySet](mesessiontopologyset.md) (S3)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **\_ coletor de TOPOSTATUS MF \_ \_ alternado** (transição para S2)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ Ready** (S2)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ iniciou \_ origem** (S2)
-   [MEEndOfPresentationSegment](meendofpresentationsegment.md) (S2 cancelado)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ encerrado** (S2)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **o \_ coletor TOPOSTATUS do MF foi \_ \_ alternado** (transição para S3)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **TOPOSTATUS \_ Ready** (S3)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ iniciou \_ origem** (S3)

Quando o aplicativo chama o [**início**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) para pular para o segmento 3, a origem do sequenciador cancela o segmento 1, que ainda está em execução. O evento [MEEndOfPresentationSegment](meendofpresentationsegment.md) para esse segmento contém o atributo de [**topologia de origem de evento MF \_ \_ \_ \_ cancelado**](mf-event-source-topology-canceled-attribute.md) , indicando que o segmento terminou porque foi cancelado. Em seguida, como o segmento 2 já foi previamente revertido, esse segmento é iniciado, mas, em seguida, cancelado imediatamente. O evento MEEndOfPresentationSegment para o segmento 2 também contém o atributo de **\_ topologia de origem de evento MF \_ \_ \_ cancelado** . A sessão pode então mudar para o segmento 3 e reproduzi-lo normalmente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre a origem do sequenciador](about-the-sequencer-source.md)
</dt> <dt>

[Origem do sequenciador](sequencer-source.md)
</dt> </dl>

 

 




