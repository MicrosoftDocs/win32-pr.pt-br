---
description: As interfaces do Call Center fornecem métodos que enfileiram e distribuem chamadas em um Call Center.
ms.assetid: 0b9a455d-a614-4698-90ab-e81f020fad3e
title: Referência rápida de controles do Call Center
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbfc34f1f30fc1f06d543cb7d5fa811517040523
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757228"
---
# <a name="call-center-controls-quick-reference"></a>Referência rápida de controles do Call Center

As interfaces do Call Center fornecem métodos que enfileiram e distribuem chamadas em um Call Center. A TAPI 3. x define cinco objetos principais do Call Center: ACDGroup, Agent, AgentHandler, AgentSession e Queue. Todos esses objetos podem ser estendidos para fornecer métodos específicos de implementação. Além disso, a interface [**ITTAPICallCenter**](/windows/win32/api/tapi3cc/nn-tapi3cc-ittapicallcenter) no objeto TAPI fornece métodos para enumerar objetos AgentHandler.



| Interface do Call Center                              | Descrição                                                              |
|----------------------------------------------------|--------------------------------------------------------------------------|
| [**ITACDGroup**](/windows/win32/api/tapi3cc/nn-tapi3cc-itacdgroup)                   | Obtém informações de nome e fila para um grupo de AD.                        |
| [**ITACDGroupEvent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itacdgroupevent)         | Obtém a descrição dos eventos do grupo ad.                                    |
| [**ITAgent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagent)                         | Fornece métodos para definir e obter informações sobre um agente.         |
| [**ITAgentEvent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagentevent)               | Interface de notificação para [**ITAgent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagent).                   |
| [**ITAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler)           | Fornece métodos para criar objetos de agente e enumerar grupos de AD.       |
| [**ITAgentHandlerEvent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandlerevent) | Obtém a descrição dos eventos de AgentHandler.                                 |
| [**ITAgentSession**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagentsession)           | Fornece métodos para definir e obter informações sobre uma sessão de agente. |
| [**ITAgentSessionEvent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagentsessionevent) | Interface de notificação para [**ITAgentSession**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagentsession).     |
| [**ITQueue**](/windows/win32/api/tapi3cc/nn-tapi3cc-itqueue)                         | Obtém e define informações relacionadas a uma fila.                            |
| [**ITQueueEvent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itqueueevent)               | Obtém informações relacionadas a um evento de fila.                               |
| [**IEnumACDGroup**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumacdgroup)             | Enumera [**ITACDGroup**](/windows/win32/api/tapi3cc/nn-tapi3cc-itacdgroup).                             |
| [**IEnumAgent**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumagent)                   | Enumera [**ITAgent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagent).                                   |
| [**IEnumAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumagenthandler)     | Enumera [**ITAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler).                     |
| [**IEnumAgentSession**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumagentsession)     | Enumera [**ITAgentSession**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagentsession).                     |
| [**IEnumQueue**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumqueue)                   | Enumera [**ITQueue**](/windows/win32/api/tapi3cc/nn-tapi3cc-itqueue).                                   |



 

As interfaces a seguir enumeram elementos TAPI 3. x de acordo com os padrões COM. Essas interfaces constituem objetos autônomos e também são resumidas com seus objetos relacionados.



| Interface do enumerador                           | Descrição                                          |
|------------------------------------------------|------------------------------------------------------|
| [**IEnumACDGroup**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumacdgroup)         | Enumera [**ITACDGroup**](/windows/win32/api/tapi3cc/nn-tapi3cc-itacdgroup).         |
| [**IEnumAgent**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumagent)               | Enumera [**ITAgent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagent).               |
| [**IEnumAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumagenthandler) | Enumera [**ITAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler). |
| [**IEnumAgentSession**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumagentsession) | Enumera [**ITAgentSession**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagentsession). |
| [**IEnumQueue**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumqueue)               | Enumera [**ITQueue**](/windows/win32/api/tapi3cc/nn-tapi3cc-itqueue).               |



 

As interfaces de evento (notificação) permitem que um aplicativo TAPI 3. x responda a eventos assíncronos. Você deve chamar o método [**ITTAPI::p UT \_ EventFilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) e definir uma máscara de filtro de eventos para habilitar a recepção de eventos de solicitação. Se você não chamar **ITTAPI::p UT \_ EventFilter**, seu aplicativo não receberá nenhum evento.



| Interface de evento                                    | Descrição                                                                  |
|----------------------------------------------------|------------------------------------------------------------------------------|
| [**ITACDGroupEvent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itacdgroupevent)         | Recupera a descrição de eventos de grupo de distribuição de chamada automática (AD). |
| [**ITAgentEvent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagentevent)               | Recupera a descrição dos eventos do agente.                                   |
| [**ITAgentHandlerEvent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandlerevent) | Recupera a descrição dos eventos do manipulador de agente.                           |
| [**ITAgentSessionEvent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagentsessionevent) | Recupera a descrição dos eventos de sessão do agente.                           |



 

 

 
