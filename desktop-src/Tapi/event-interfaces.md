---
description: As interfaces de evento (notificação) permitem que um aplicativo TAPI 3 responda a eventos assíncronos.
ms.assetid: 27fd91e8-b628-49ee-af4e-9aec0afa5449
title: Interfaces de evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01a4ecf097d761e98b723b37d9de6adcfd7ebb60696ce5e389426965534d63f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660836"
---
# <a name="event-interfaces"></a>Interfaces de evento

As interfaces de evento (notificação) permitem que um aplicativo TAPI 3 responda a eventos assíncronos.

Você deve chamar o [**método ItTAPI::p ut \_ EventFilter**](/windows/win32/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) e definir uma máscara de filtro de evento para habilitar a recepção de eventos de solicitação. Se você não chamar **ITTAPI::p ut \_ EventFilter,** seu aplicativo não receberá nenhum evento.

Confira a Visão [geral de](./asynchronous-spontaneous-events.md) eventos para ver uma descrição de como um aplicativo garante a recepção de notificações. Consulte as interfaces individuais listadas na tabela a seguir para obter mais informações sobre como definir uma máscara de filtro para tipos de evento individuais.



| Interface                                                           | Descrição                                                                                                                                 |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITAddressEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itaddressevent)                   | Recupera a descrição dos eventos de endereço.                                                                                                |
| [**ITASRTerminalEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itasrterminalevent)           | Recupera a descrição dos eventos de terminal de Reconhecimento Automático de Fala.                                                                  |
| [**ITCallHubEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itcallhubevent)                   | Recupera a descrição dos eventos do CallHub.                                                                                                |
| [**ITCallInfoChangeEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itcallinfochangeevent)     | Recupera a descrição dos eventos de alteração de informações de chamada.                                                                                |
| [**ITCallMediaEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itcallmediaevent)               | Recupera a descrição dos eventos de mídia de chamada.                                                                                             |
| [**ITCallNotificationEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itcallnotificationevent) | Recupera a descrição dos eventos de notificação de chamada.                                                                                      |
| [**ITCallStateEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itcallstateevent)               | Recupera a descrição dos eventos de estado de chamada.                                                                                             |
| [**ITDigitDetectionEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itdigitdetectionevent)     | Recupera informações sobre eventos de dígito DTMF durante uma chamada.                                                                                |
| [**ITDigitGenerationEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itdigitgenerationevent)   | Recupera informações sobre chamadas que exigem a geração de dígitos DTMF.                                                               |
| [**ITDigitsGatheredEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itdigitsgatheredevent)     | Recupera dados relacionados à solicitação de coleta de dígitos de um aplicativo.                                                                         |
| [**ITFileTerminalEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itfileterminalevent)         | Recupera a descrição dos eventos do terminal de arquivo.                                                                                          |
| [**ITParticipantEvent**](./itparticipantevent.md)           | Recupera a descrição dos eventos do participante da conferência.                                                                                 |
| [**ITPhoneEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itphoneevent)                       | Recupera a descrição dos eventos de telefone.                                                                                                  |
| [**ITQOSEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itqosevent)                           | Recupera a descrição dos eventos QOS (qualidade de serviço).                                                                               |
| [**ITQueueEvent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itqueueevent)                       | Recupera a descrição dos eventos de fila da ACD (Distribuição Automática de Chamada).                                                                |
| [**ITRequestEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itrequestevent)                   | Recupera a descrição dos [eventos de solicitação de Telefonia](./assisted-telephony-overview.md) Assistida.                                 |
| [**ITTAPIObjectEvent**](/windows/win32/api/tapi3if/nn-tapi3if-ittapiobjectevent)             | Recupera a descrição dos eventos de objeto TAPI.                                                                                            |
| [**ITTAPIObjectEvent2**](/windows/win32/api/tapi3if/nn-tapi3if-ittapiobjectevent2)           | Estende [**ITTAPIObjectEvent**](/windows/win32/api/tapi3if/nn-tapi3if-ittapiobjectevent); recupera um ponteiro para o objeto de telefone que causou o evento de objeto TAPI. |
| [**ITToneDetectionEvent**](/windows/win32/api/tapi3if/nn-tapi3if-ittonedetectionevent)       | Recupera informações sobre um evento de detecção de tom.                                                                                         |
| [**ITToneTerminalEvent**](/windows/win32/api/tapi3if/nn-tapi3if-ittoneterminalevent)         | Recupera a descrição dos eventos de terminal de tom.                                                                                          |
| [**ITTTSTerminalEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itttsterminalevent)           | Recupera a descrição de eventos de terminal de TTS (texto em fala).                                                                          |



 



| Interface                                                                                             | Descrição                                                                                      |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**ITPluggableTerminalEventSink**](/windows/win32/api/tapi3/nn-tapi3-itpluggableterminaleventsink)                         | Notifica os aplicativos cliente sobre alterações em um terminal que pode ser conectado.                              |
| [**ITPluggableTerminalEventSinkRegistration**](/windows/win32/api/tapi3/nn-tapi3-itpluggableterminaleventsinkregistration) | Registra e registra um aplicativo cliente para notificação sobre eventos de terminal que podem ser conectados. |



 

 

 
