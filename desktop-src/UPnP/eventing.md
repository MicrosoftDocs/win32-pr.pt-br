---
title: Eventos
description: Um serviço hospedado deve implementar a interface IUPnPEventSource se ele tiver variáveis de estado evento.
ms.assetid: 7558496d-c909-4602-bfaa-d21108392fed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 313f979072a447f41b9edadfeec7bf4407463be67c86e9c3b34f43f4dcc47874
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008076"
---
# <a name="eventing"></a>Eventos

Um serviço hospedado deve implementar a interface [**IUPnPEventSource**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpeventsource) se ele tiver variáveis de estado evento. Essa interface tem dois métodos: [**Advise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-advise) e [**Unadvise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-unadvise). Essa interface fornece um mecanismo para o host do dispositivo assinar notificações de eventos geradas pelo serviço hospedado. Não haverá mais de um sink de evento registrado por vez.

Um serviço hospedado deve implementar o método [**Advise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-advise) mantendo uma referência à interface [**IUPnPEventSink,**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpeventsink) que foi passada como um parâmetro. Se a interface for encontrada, o método **Advise** manterá uma referência a essa interface até que [**Unadvise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-unadvise) seja invocado ou até que o objeto de serviço hospedado seja removido. **A consultoria** é chamada apenas uma vez.

Para remover a assinatura, o host do dispositivo invoca [**Unadvise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-unadvise) e passa o ponteiro do objeto usado quando ele chamou [**Avisar**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-advise). O serviço hospedado removerá a assinatura se o ponteiro for o mesmo que o passado para **Avisar**.

Quando o valor de uma variável de estado muda, o serviço hospedado deve sinalizar que ocorreu um evento. Os serviços faz isso invocando o [**método IUPnPEventSink::OnStateChanged.**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsink-onstatechanged)

Quando o host do dispositivo não precisa mais receber notificações do serviço hospedado, ele invoca [**IUPnPEventSource::Unadvise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-unadvise), passando o mesmo ponteiro de objeto recebido de [**Aviso**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-advise). O host do dispositivo invoca esse método quando o dispositivo não estará mais na rede.

 

 




