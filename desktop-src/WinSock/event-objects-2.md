---
description: A introdução de E/S sobressalo requer um mecanismo para que os aplicativos associem solicitações de envio e recebimento de forma não ambígua às suas indicações de conclusão subsequentes.
ms.assetid: 944d87bd-388f-420d-ac7d-69c4a28f8a5c
title: Objetos de evento (Windows Soquetes 2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34820d7df92704d86f7dbdc100816789488426e2fdd553456be94da921811c3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132589"
---
# <a name="event-objects-windows-sockets-2"></a>Objetos de evento (Windows Soquetes 2)

A introdução de E/S sobressalo requer um mecanismo para que os aplicativos associem solicitações de envio e recebimento de forma não ambígua às suas indicações de conclusão subsequentes. No Windows Soquetes 2, isso é feito com objetos de evento que são modelados após Windows eventos. Windows Os objetos de evento sockets são constructos bastante simples que podem ser criados e fechados, definidos e limpos e aguardados e sondados. Seu principal utilitário é a capacidade de um aplicativo bloquear e aguardar até que um ou mais objetos de evento se tornem definidos.

Os [**aplicativos usam WSACreateEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent) para obter um identificador de objeto de evento que pode ser fornecido como um parâmetro necessário para as versões sobrecarrecidas de chamadas de envio e recebimento ( [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend), [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom)). O objeto de evento, que é limpo quando criado pela primeira vez, é definido pelos provedores de transporte quando a operação de E/S sobresalo associada é concluída (com êxito ou com erros). Cada objeto de evento criado **por WSACreateEvent** deve ter um [**WSACloseEvent correspondente**](/windows/desktop/api/Winsock2/nf-winsock2-wsacloseevent) para destruir.

Os objetos de evento também são usados [**em WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) para associar um ou mais eventos de rede FD \_ XXX a um objeto de evento. Isso é descrito em [Notificação assíncrona usando objetos de evento](asynchronous-notification-using-event-objects-2.md).

Em ambientes de 32 bits, funções relacionadas ao objeto de evento, incluindo [**WSACreateEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent), [**WSACloseEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacloseevent), [**WSASetEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetevent), [**WSAResetEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsaresetevent)e [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) são mapeadas diretamente para as funções Windows nativas correspondentes, usando o mesmo nome de função, mas sem o prefixo WSA.

 

 



