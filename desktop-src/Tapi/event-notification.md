---
description: A notificação de eventos é o principal meio pelo qual um aplicativo obtém informações da TAPI e dos provedores de serviços.
ms.assetid: 02160f10-dc3f-484c-9cd3-bcfb07ded822
title: Notificação de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21a83ed721ed22049baeaf3de15626ed8deecf2a7562d883658195eb1eb590f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003664"
---
# <a name="event-notification"></a>Notificação de eventos

A notificação de eventos é o principal meio pelo qual um aplicativo obtém informações da TAPI e dos provedores de serviços. Essas informações podem ser o status de uma operação assíncrona provocada pelo aplicativo ou podem se preocupar com um processo iniciado fora do aplicativo, como notificações de novas chamadas de entrada.

**TAPI 2. x:** Os aplicativos manipulam a notificação de uma das três maneiras: janela oculta, manipulador de eventos ou porta de conclusão. Para obter informações adicionais sobre esses mecanismos de notificação, consulte a seção comentários para [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa). Um aplicativo especifica o mecanismo definindo o membro **dwOptions** da estrutura [**LINEINITIALIZEEXPARAMS**](/windows/win32/api/tapi/ns-tapi-lineinitializeexparams) antes de chamar [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa).

A função [**lineSetStatusMessages**](/windows/win32/api/tapi/nf-tapi-linesetstatusmessages) permite que um aplicativo especifique quais mensagens de notificação receber para eventos relacionados a alterações de status da linha especificada ou de qualquer um de seus endereços.

**TAPI 3. x:** Os aplicativos manipulam a notificação geral usando [objetos de conexão](../com/events-in-com-and-connectable-objects.md)padrão com. [**ITTAPIEventNotification**](/windows/desktop/api/Tapi3if/nn-tapi3if-ittapieventnotification) é a interface de saída que deve ser registrada com o objeto Container da TAPI, e [**ITTAPIEventNotification:: Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) é o método que a TAPI chama para determinar a resposta do aplicativo. O método [**ITTAPI::p UT \_ EventFilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) informa à TAPI quais eventos são interessantes para o aplicativo. Se um filtro de eventos não for inserido, o aplicativo não receberá a notificação de nenhum evento. O método [**ITTAPI:: RegisterCallNotifications**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications) informa à TAPI os tipos de mídia e os endereços para os quais o aplicativo tratará as sessões de entrada. Para obter informações adicionais sobre manipulação de eventos TAPI 3, consulte a visão geral de [eventos](events.md) ou o exemplo de código [registrar eventos](register-events.md) .

Provedores de serviço de telefonia implementam [**TSPI \_ LineSetDefaultMediaDetection**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection) e [**TSPI \_ lineSetStatusMessages**](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages). A TAPI chama essas funções para indicar o conjunto de todos os eventos de linha, endereço e tipo de mídia solicitados pelos aplicativos.

 

 
