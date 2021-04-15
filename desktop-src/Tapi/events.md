---
description: Os eventos são uma parte crucial do tratamento de chamadas sob a TAPI 3. A manipulação de eventos inclui quatro estágios.
ms.assetid: db43f4e0-f2f5-49b1-a03d-3df3de0e5611
title: Eventos (API de telefonia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6a9a7d994c7bc9f8019224d826d586d698bc605
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505867"
---
# <a name="events-telephony-api"></a>Eventos (API de telefonia)

Os eventos são uma parte crucial do tratamento de chamadas sob a TAPI 3. A manipulação de eventos inclui quatro estágios.

**Para se registrar e habilitar a recepção de eventos**

1.  Implemente o método [**ITTAPIEventNotification:: Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) . (TAPI chama esse método quando ocorre um evento.) Normalmente, essa implementação não tem mais do que **AddRef** o ponteiro da interface **IDispatch** e depois posta para a bomba de mensagens do aplicativo.
2.  Registre a interface de saída do [**ITTAPIEventNotification**](/windows/desktop/api/Tapi3if/nn-tapi3if-ittapieventnotification) usando as interfaces [**IConnectionPointContainer**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) e [**IConnectionPoint**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpoint) padrão com e passe o método [**IConnectionPoint:: Advise**](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) um ponteiro para [**ITTAPIEventNotification:: Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event).
3.  Chame o método [**ITTAPI::p UT \_ EventFilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) para informar à TAPI quais eventos o aplicativo manipulará. O filtro de eventos consiste em **ou** Ed membros da enumeração de [**\_ eventos TAPI**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event) .
    > [!Note]  
    > Você deve chamar o método **ITTAPI::p UT \_ EventFilter** para definir a máscara de filtro de eventos e habilitar a recepção de eventos. Se você não chamar **ITTAPI::p UT \_ EventFilter**, seu aplicativo não receberá nenhum evento.

     

Você também deve chamar o método [**ITTAPI:: RegisterCallNotifications**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications) para cada objeto de endereço no qual o aplicativo tratará chamadas.

Consulte [interfaces de evento](./event-interfaces.md) para obter uma lista de todas as interfaces de evento. Consulte [registrar eventos](register-events.md) para obter exemplos de código que ilustram o processo de registro e [recebem uma chamada](receive-a-call.md) para um exemplo de código que mostra um uso de eventos.

 

 
