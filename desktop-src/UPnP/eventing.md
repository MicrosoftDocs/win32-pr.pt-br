---
title: Eventos
description: Um serviço hospedado deve implementar a interface IUPnPEventSource se ela tiver variáveis de estado com eventos.
ms.assetid: 7558496d-c909-4602-bfaa-d21108392fed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68a6382ee88d2ca5168c94eac20727bbfee4a598
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822695"
---
# <a name="eventing"></a>Eventos

Um serviço hospedado deve implementar a interface [**IUPnPEventSource**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpeventsource) se ela tiver variáveis de estado com eventos. Essa interface tem dois métodos: [**Advise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-advise) e [**Unadvise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-unadvise). Essa interface fornece um mecanismo para o host do dispositivo assinar notificações de eventos geradas pelo serviço hospedado. Não haverá mais de um coletor de eventos registrado por vez.

Um serviço hospedado deve implementar o método [**Advise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-advise) mantendo uma referência à interface [**IUPnPEventSink**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpeventsink) , que foi passada como um parâmetro. Se a interface for encontrada, o método **Advise** manterá uma referência a essa interface até que [**Unadvise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-unadvise) seja invocado ou até que o objeto de serviço hospedado seja removido. O **aviso** é chamado apenas uma vez.

Para remover a assinatura, o host do dispositivo invoca [**Unadvise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-unadvise) e passa no ponteiro do objeto usado quando ele chamou [**Advise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-advise). O serviço hospedado remove a assinatura se o ponteiro for o mesmo passado para **Advise**.

Quando o valor de uma variável de estado é alterado, o serviço hospedado deve sinalizar que ocorreu um evento. Os serviços faz isso invocando o método [**IUPnPEventSink:: OnStateChanged**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsink-onstatechanged) .

Quando o host do dispositivo não precisa mais receber notificações do serviço hospedado, ele invoca [**IUPnPEventSource:: Unadvise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-unadvise), passando o mesmo ponteiro de objeto recebido de [**Advise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-advise). O host do dispositivo invoca esse método quando o dispositivo não está mais na rede.

 

 




