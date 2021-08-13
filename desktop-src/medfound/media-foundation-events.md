---
description: Media Foundation eventos
ms.assetid: d925f63d-3359-4ba1-802f-0c2b11a3f973
title: Media Foundation eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38a922127941bd94103eac9cfb02ef33d1c0b789eb632f2689a3adc81494c377
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119268812"
---
# <a name="media-foundation-events"></a>Media Foundation eventos



| Evento                                                                                        | Descrição                                                                                                                                              |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MEAudioSessionDeviceRemoved](meaudiosessiondeviceremoved.md)                               | O dispositivo de áudio foi removido.                                                                                                                            |
| [MEAudioSessionDisconnected](meaudiosessiondisconnected.md)                                 | A sessão de áudio foi desconectada de uma sessão Terminal do Windows Services                                                                              |
| [MEAudioSessionExclusiveModeOverride](meaudiosessionexclusivemodeoverride.md)               | A sessão de áudio foi preempção por uma conexão de modo exclusivo.                                                                                         |
| [MEAudioSessionFormatChanged](meaudiosessionformatchanged.md)                               | O formato de áudio padrão para o dispositivo de áudio foi alterado.                                                                                                   |
| [MEAudioSessionGroupingParamChanged](meaudiosessiongroupingparamchanged.md)                 | Os parâmetros de agrupação foram alterados para a sessão de áudio.                                                                                                   |
| [MEAudioSessionIconChanged](meaudiosessioniconchanged.md)                                   | O ícone de sessão de áudio foi alterado.                                                                                                                          |
| [MEAudioSessionNameChanged](meaudiosessionnamechanged.md)                                   | O nome de exibição da sessão de áudio foi alterado.                                                                                                                  |
| [MEAudioSessionServerShutdown](meaudiosessionservershutdown.md)                             | O Windows do servidor de áudio foi desligado.                                                                                                           |
| [MEAudioSessionVolumeChanged](meaudiosessionvolumechanged.md)                               | O estado de volume ou mudo da sessão de áudio foi alterado                                                                                                    |
| [MEBufferingStarted](mebufferingstarted.md)                                                 | Uma fonte de mídia começou a buffer de dados.                                                                                                                   |
| [MEBufferingStopped](mebufferingstopped.md)                                                 | Uma fonte de mídia interrompeu o buffer de dados.                                                                                                                   |
| [MECaptureAudioSessionDeviceRemoved](mecaptureaudiosessiondeviceremoved.md)                 | O dispositivo foi removido.                                                                                                                                  |
| [MECaptureAudioSessionDisconnected](mecaptureaudiosessiondisconnected.md)                   | A sessão de áudio está desconectada porque o usuário fez logon de uma sessão Terminal do Windows Services (WTS) .                                            |
| [MECaptureAudioSessionExclusiveModeOverride](mecaptureaudiosessionexclusivemodeoverride.md) | O usuário abriu um fluxo de áudio no modo exclusivo.                                                                                                       |
| [MECaptureAudioSessionFormatChanged](mecaptureaudiosessionformatchanged.md)                 | O formato de áudio foi alterado.                                                                                                                                |
| [MECaptureAudioSessionServerShutdown](mecaptureaudiosessionservershutdown.md)               | O desligamento do servidor de sessão de áudio.                                                                                                                       |
| [MECaptureAudioSessionVolumeChanged](mecaptureaudiosessionvolumechanged.md)                 | O volume foi alterado.                                                                                                                                      |
| [MEConnectEnd](meconnectend.md)                                                             | A fonte de rede terminou de abrir uma URL.                                                                                                               |
| [MEConnectStart](meconnectstart.md)                                                         | A origem da rede começou a abrir uma URL.                                                                                                                |
| [MEContentProtectionMessage](mecontentprotectionmessage.md)                                 | A configuração foi alterada para um esquema de proteção de saída.                                                                                               |
| [MEEnablerCompleted](meenablercompleted.md)                                                 | A ação de um objeto do habilitador de conteúdo foi concluída.                                                                                                           |
| [MEEnablerProgress](meenablerprogress.md)                                                   | Sinaliza o progresso de um objeto do habilitador de conteúdo.                                                                                                        |
| [MEEndOfPresentation](meendofpresentation.md)                                               | Gerado por uma fonte de mídia quando uma apresentação termina.                                                                                                       |
| [MEEndOfPresentationSegment](meendofpresentationsegment.md)                                 | Gerado pela origem do sequenciador quando um segmento é concluído e é seguido por outro segmento.                                                           |
| [MEEndOfStream](meendofstream.md)                                                           | Gerado por um fluxo de mídia quando o fluxo termina.                                                                                                           |
| [MEError](meerror.md)                                                                       | Sinaliza um erro grave.                                                                                                                                 |
| [MEExtendedType](meextendedtype.md)                                                         | Tipo de evento personalizado.                                                                                                                                       |
| [MEIndividualizationCompleted](meindividualizationcompleted.md)                             | A individualização foi concluída.                                                                                                                           |
| [MEIndividualizationStart](meindividualizationstart.md)                                     | A individualização está prestes a começar.                                                                                                                     |
| [MELicenseAcquisitionCompleted](melicenseacquisitioncompleted.md)                           | A aquisição de licença foi concluída.                                                                                                                         |
| [MELicenseAcquisitionStart](melicenseacquisitionstart.md)                                   | A aquisição de licença está prestes a começar.                                                                                                                   |
| [MEMediaSample](memediasample.md)                                                           | Gerado quando um fluxo de mídia fornece um novo exemplo.                                                                                                        |
| [MENewPresentation](menewpresentation.md)                                                   | Gerado por uma fonte de mídia, uma nova apresentação está pronta.                                                                                                    |
| [MENewStream](menewstream.md)                                                               | Gerado por uma fonte de mídia quando ele inicia um novo fluxo.                                                                                                    |
| [MENonFatalError](menonfatalerror.md)                                                       | Ocorreu um erro não fatal durante o streaming.                                                                                                             |
| [MEPolicyChanged](mepolicychanged.md)                                                       | A política de saída para um fluxo foi alterada.                                                                                                                  |
| [MEPolicyError](mepolicyerror.md)                                                           | Gerado por uma saída confiável se ocorrer um erro ao impor a política de saída.                                                                         |
| [MEPolicyReport](mepolicyreport.md)                                                         | Contém informações de status sobre a imposição de uma política de saída.                                                                                   |
| [MEPolicySet](mepolicyset.md)                                                               | O [**método IMFOutputTrustAuthority::SetPolicy**](/windows/desktop/api/mfidl/nf-mfidl-imfoutputtrustauthority-setpolicy) foi concluído.                                                    |
| [MEQualityNotify](mequalitynotify.md)                                                       | Fornece comentários sobre a qualidade da reprodução para o gerenciador de qualidade.                                                                                         |
| [MEReconnectEnd](mereconnectend.md)                                                         | Gerado por uma fonte de mídia no final de uma tentativa de reconexão.                                                                                           |
| [MEReconnectStart](mereconnectstart.md)                                                     | Gerado por uma fonte de mídia no início de uma tentativa de reconexão.                                                                                         |
| [MERendererEvent](merendererevent.md)                                                       | Gerado pelo renderizador de vídeo aprimorado (EVR) quando ele recebe um evento de usuário do apresentador.                                                            |
| [MESequencerSourceTopologyUpdated](mesequencersourcetopologyupdated.md)                     | Gerado pela origem do sequenciador quando o [**método IMFSequencerSource::UpdateTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) é concluído de forma assíncrona. |
| [MESessionCapabilitiesChanged](mesessioncapabilitieschanged.md)                             | Gerado pela Sessão de Mídia quando os recursos de sessão são alterados.                                                                                        |
| [MESessionClosed](mesessionclosed.md)                                                       | Gerado quando [**o método IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) é concluído de forma assíncrona.                                                 |
| [MESessionEnded](mesessionended.md)                                                         | Gerado pela Sessão de Mídia quando terminar de reproduzir a última apresentação na fila de reprodução.                                                    |
| [MESessionNotifyPresentationTime](mesessionnotifypresentationtime.md)                       | Gerado pela sessão de mídia quando uma nova apresentação é iniciada.                                                                                              |
| [MESessionPaused](mesessionpaused.md)                                                       | Gerado quando o método [**IMFMediaSession::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) é concluído de forma assíncrona.                                                 |
| [MESessionRateChanged](mesessionratechanged.md)                                             | Gerado pela sessão de mídia quando a taxa de reprodução é alterada.                                                                                              |
| [MESessionScrubSampleComplete](mesessionscrubsamplecomplete.md)                             | Gerado pela sessão de mídia quando ele conclui uma solicitação de depuração.                                                                                       |
| [MESessionStarted](mesessionstarted.md)                                                     | Gerado quando o método [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) é concluído de forma assíncrona.                                                 |
| [MESessionStopped](mesessionstopped.md)                                                     | Gerado quando o método [**IMFMediaSession:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop) é concluído de forma assíncrona.                                                   |
| [MESessionStreamSinkFormatChanged](mesessionstreamsinkformatchanged.md)                     | Gerado pela sessão de mídia quando o formato é alterado em um coletor de mídia.                                                                                     |
| [MESessionTopologiesCleared](mesessiontopologiescleared.md)                                 | Gerado pela sessão de mídia quando o método [**IMFMediaSession:: ClearTopologies**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-cleartopologies) é concluído de forma assíncrona.        |
| [MESessionTopologySet](mesessiontopologyset.md)                                             | Gerado depois que o método [**IMFMediaSession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) é concluído de forma assíncrona                                     |
| [MESessionTopologyStatus](mesessiontopologystatus.md)                                       | Gerado pela sessão de mídia quando o status de uma topologia é alterado.                                                                                       |
| [MESinkInvalidated](mesinkinvalidated.md)                                                   | Gerado quando um coletor de mídia se torna inválido.                                                                                                                |
| [MESourceCharacteristicsChanged](mesourcecharacteristicschanged.md)                         | Gerado por uma origem de mídia quando as características da fonte são alteradas.                                                                                       |
| [MESourceMetadataChanged](mesourcemetadatachanged.md)                                       | Gerado por uma origem de mídia quando ele atualiza seus metadados.                                                                                                   |
| [MESourcePaused](mesourcepaused.md)                                                         | Gerado por uma origem de mídia quando o método [**IMFMediaSource::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) é concluído de forma assíncrona.                                 |
| [MESourceRateChanged](mesourceratechanged.md)                                               | Gerado por uma origem de mídia quando a taxa de reprodução é alterada.                                                                                                 |
| [MESourceRateChangeRequested](mesourceratechangerequested.md)                               | Gerado por uma fonte de mídia para solicitar uma nova taxa de reprodução.                                                                                                 |
| [MESourceSeeked](mesourceseeked.md)                                                         | Gerado quando uma fonte de mídia busca uma nova posição.                                                                                                      |
| [MESourceStarted](mesourcestarted.md)                                                       | Gerado quando uma fonte de mídia é iniciada sem busca.                                                                                                       |
| [MESourceStopped](mesourcestopped.md)                                                       | Gerado por uma origem de mídia quando o método [**IMFMediaSource:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) é concluído de forma assíncrona.                                   |
| [MEStreamFormatChanged](mestreamformatchanged.md)                                           | Gerado por um fluxo de mídia quando o tipo de mídia do fluxo é alterado.                                                                                      |
| [MEStreamPaused](mestreampaused.md)                                                         | Gerado por um fluxo de mídia quando o método [**IMFMediaSource::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) é concluído de forma assíncrona.                                 |
| [MEStreamSeeked](mestreamseeked.md)                                                         | Gerado por um fluxo de mídia após uma chamada para [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) causa uma busca no fluxo.                              |
| [MEStreamSinkDeviceChanged](mestreamsinkdevicechanged.md)                                   | Gerado pelos coletores de fluxo do EVR se o dispositivo de vídeo for alterado.                                                                                       |
| [MEStreamSinkFormatChanged](mestreamsinkformatchanged.md)                                   | Gerado por um coletor de fluxo quando o tipo de mídia do coletor não é mais válido.                                                                                   |
| [MEStreamSinkMarker](mestreamsinkmarker.md)                                                 | Gerado por um coletor de fluxo após o método [**IMFStreamSink::P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) é chamado.                                      |
| [MEStreamSinkPaused](mestreamsinkpaused.md)                                                 | Gerado por um coletor de fluxo quando ele conclui a transição para o estado em pausa.                                                                            |
| [MEStreamSinkPrerolled](mestreamsinkprerolled.md)                                           | Gerado por um coletor de fluxo quando o fluxo recebeu dados de preversão suficientes para começar a renderização.                                                             |
| [MEStreamSinkRateChanged](mestreamsinkratechanged.md)                                       | Gerado por um coletor de fluxo quando a taxa é alterada.                                                                                                       |
| [MEStreamSinkRequestSample](mestreamsinkrequestsample.md)                                   | Gerado por um coletor de fluxo para solicitar um novo exemplo de mídia do pipeline.                                                                                 |
| [MEStreamSinkScrubSampleComplete](mestreamsinkscrubsamplecomplete.md)                       | Gerado por um coletor de fluxo quando ele conclui uma solicitação de depuração.                                                                                           |
| [MEStreamSinkStarted](mestreamsinkstarted.md)                                               | Gerado por um coletor de fluxo quando ele conclui a transição para o estado de execução.                                                                           |
| [MEStreamSinkStopped](mestreamsinkstopped.md)                                               | Gerado por um coletor de fluxo quando ele conclui a transição para o estado parado.                                                                           |
| [MEStreamStarted](mestreamstarted.md)                                                       | Gerado por um fluxo de mídia quando a origem é iniciada sem busca.                                                                                         |
| [MEStreamStopped](mestreamstopped.md)                                                       | Gerado por um fluxo de mídia quando o método [**IMFMediaSource:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) é concluído de forma assíncrona.                                   |
| [MEStreamThinMode](mestreamthinmode.md)                                                     | Gerado por um fluxo de mídia quando ele inicia ou interrompe a finamento do fluxo.                                                                                    |
| [MEStreamTick](mestreamtick.md)                                                             | Sinaliza que um fluxo de mídia não tem dados disponíveis em um horário especificado.                                                                            |
| [METransformDrainComplete](metransformdraincomplete.md)                                     | Enviado por uma Media Foundation de transformação assíncrona (MFT) quando uma operação de descarga é concluída.                                                             |
| [METransformHaveOutput](metransformhaveoutput.md)                                           | Enviado por um MFT assíncrono quando novos dados de saída estão disponíveis no MFT.                                                                              |
| [METransformMarker](metransformmarker.md)                                                   | Enviado por um MFT assíncrono em resposta a uma mensagem de [**\_ marcador de \_ comando \_ de mensagem MFT**](mft-message-command-marker.md) .                               |
| [METransformNeedInput](metransformneedinput.md)                                             | Enviado por um MFT assíncrono para solicitar um novo exemplo de entrada.                                                                                               |
| [MEUnknown](meunknown.md)                                                                   | Tipo de evento desconhecido.                                                                                                                                      |
| [MEUpdatedStream](meupdatedstream.md)                                                       | Gerado por uma origem de mídia quando ele é reiniciado ou busca um fluxo que já está ativo.                                                                      |
| [MEVideoCaptureDevicePreempted](mevideocapturedevicepreempted.md)                           | O dispositivo foi admitido com preempção.                                                                                                                           |
| [MEVideoCaptureDeviceRemoved](mevideocapturedeviceremoved.md)                               | O dispositivo foi removido.                                                                                                                             |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de programação do Media Foundation](media-foundation-programming-reference.md)
</dt> <dt>

[Geradores de eventos de mídia](media-event-generators.md)
</dt> <dt>

[**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
</dt> </dl>

 

 



