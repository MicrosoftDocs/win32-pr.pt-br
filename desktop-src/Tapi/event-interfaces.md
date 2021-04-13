---
description: As interfaces de evento (notificação) permitem que um aplicativo TAPI 3 responda a eventos assíncronos.
ms.assetid: 27fd91e8-b628-49ee-af4e-9aec0afa5449
title: Interfaces de evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd7b705c89988ff62d972e594ceb936bb01db78e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501744"
---
# <a name="event-interfaces"></a>Interfaces de evento

As interfaces de evento (notificação) permitem que um aplicativo TAPI 3 responda a eventos assíncronos.

Você deve chamar o método [**ITTAPI::p UT \_ EventFilter**](/windows/win32/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) e definir uma máscara de filtro de eventos para habilitar a recepção de eventos de solicitação. Se você não chamar **ITTAPI::p UT \_ EventFilter**, seu aplicativo não receberá nenhum evento.

Consulte a visão geral de [eventos](./asynchronous-spontaneous-events.md) para obter uma descrição de como um aplicativo garante a recepção de notificações. Consulte as interfaces individuais listadas na tabela a seguir para obter mais informações sobre como definir uma máscara de filtro para tipos de evento individuais.



| Interface                                                           | Descrição                                                                                                                                 |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITAddressEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itaddressevent)                   | Recupera a descrição dos eventos de endereço.                                                                                                |
| [**ITASRTerminalEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itasrterminalevent)           | Recupera a descrição de eventos de terminal de reconhecimento automático de fala.                                                                  |
| [**ITCallHubEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itcallhubevent)                   | Recupera a descrição dos eventos CallHub.                                                                                                |
| [**ITCallInfoChangeEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itcallinfochangeevent)     | Recupera a descrição de eventos de alteração de informações de chamada.                                                                                |
| [**ITCallMediaEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itcallmediaevent)               | Recupera a descrição dos eventos de mídia de chamada.                                                                                             |
| [**ITCallNotificationEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itcallnotificationevent) | Recupera a descrição dos eventos de notificação de chamada.                                                                                      |
| [**ITCallStateEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itcallstateevent)               | Recupera a descrição dos eventos de estado da chamada.                                                                                             |
| [**ITDigitDetectionEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itdigitdetectionevent)     | Recupera informações sobre eventos de dígito DTMF durante uma chamada.                                                                                |
| [**ITDigitGenerationEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itdigitgenerationevent)   | Recupera informações sobre chamadas que exigem a geração de dígitos DTMF.                                                               |
| [**ITDigitsGatheredEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itdigitsgatheredevent)     | Recupera os dados relacionados à solicitação de coleta de dígitos de um aplicativo.                                                                         |
| [**ITFileTerminalEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itfileterminalevent)         | Recupera a descrição dos eventos de terminal do arquivo.                                                                                          |
| [**ITParticipantEvent**](./itparticipantevent.md)           | Recupera a descrição dos eventos do participante da conferência.                                                                                 |
| [**ITPhoneEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itphoneevent)                       | Recupera a descrição de eventos do telefone.                                                                                                  |
| [**ITQOSEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itqosevent)                           | Recupera a descrição de eventos de qualidade de serviço (QOS).                                                                               |
| [**ITQueueEvent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itqueueevent)                       | Recupera a descrição de eventos de fila de distribuição de chamada automática (AD).                                                                |
| [**ITRequestEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itrequestevent)                   | Recupera a descrição de eventos de solicitação de [telefonia assistida](./assisted-telephony-overview.md) .                                 |
| [**ITTAPIObjectEvent**](/windows/win32/api/tapi3if/nn-tapi3if-ittapiobjectevent)             | Recupera a descrição de eventos de objeto TAPI.                                                                                            |
| [**ITTAPIObjectEvent2**](/windows/win32/api/tapi3if/nn-tapi3if-ittapiobjectevent2)           | Estende [**ITTAPIObjectEvent**](/windows/win32/api/tapi3if/nn-tapi3if-ittapiobjectevent); Recupera um ponteiro para o objeto de telefone que causou o evento de objeto TAPI. |
| [**ITToneDetectionEvent**](/windows/win32/api/tapi3if/nn-tapi3if-ittonedetectionevent)       | Recupera informações sobre um evento de detecção de Tom.                                                                                         |
| [**ITToneTerminalEvent**](/windows/win32/api/tapi3if/nn-tapi3if-ittoneterminalevent)         | Recupera a descrição dos eventos de terminal de Tom.                                                                                          |
| [**ITTTSTerminalEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itttsterminalevent)           | Recupera a descrição de eventos de terminal de conversão de texto em fala (TTS).                                                                          |



 



| Interface                                                                                             | Descrição                                                                                      |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**ITPluggableTerminalEventSink**](/windows/win32/api/tapi3/nn-tapi3-itpluggableterminaleventsink)                         | Notifica os aplicativos cliente sobre as alterações em um terminal conectável.                              |
| [**ITPluggableTerminalEventSinkRegistration**](/windows/win32/api/tapi3/nn-tapi3-itpluggableterminaleventsinkregistration) | Registra e cancela o registro de um aplicativo cliente para notificação sobre eventos de terminal conectável. |



 

 

 
