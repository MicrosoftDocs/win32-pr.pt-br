---
description: A introdução à e/s sobreposta exige um mecanismo para que os aplicativos associem de forma não ambígua as solicitações de envio e recebimento às suas indicações de conclusão subsequentes.
ms.assetid: 944d87bd-388f-420d-ac7d-69c4a28f8a5c
title: Objetos de evento (Windows Sockets 2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e72b60442f9c56ae2c8e9af905bd14b6536b8e10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296353"
---
# <a name="event-objects-windows-sockets-2"></a>Objetos de evento (Windows Sockets 2)

A introdução à e/s sobreposta exige um mecanismo para que os aplicativos associem de forma não ambígua as solicitações de envio e recebimento às suas indicações de conclusão subsequentes. No Windows Sockets 2, isso é feito com objetos de evento que são modelados após eventos do Windows. Os objetos de evento do Windows Sockets são construções bastante simples que podem ser criados e fechados, definidos e limpos, e aguardados e sondados. Seu principal utilitário é a capacidade de um aplicativo bloquear e aguardar até que um ou mais objetos de evento sejam definidos.

Os aplicativos usam [**WSACreateEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent) para obter um identificador de objeto de evento que pode ser fornecido como um parâmetro necessário para as versões sobrepostas de chamadas de envio e recebimento ( [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend), [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom)). O objeto de evento, que é limpo quando criado pela primeira vez, é definido pelos provedores de transporte quando a operação de e/s sobreposta associada é concluída (com êxito ou com erros). Cada objeto de evento criado pelo **WSACreateEvent** deve ter um [**WSACloseEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacloseevent) correspondente para destruí-lo.

Os objetos de evento também são usados em [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) para associar um ou mais \_ eventos de rede FD xxx a um objeto de evento. Isso é descrito em [notificação assíncrona usando objetos de evento](asynchronous-notification-using-event-objects-2.md).

Em ambientes de 32 bits, as funções relacionadas a objeto de evento, incluindo [**WSACreateEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent), [**WSACloseEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacloseevent), [**WSASetEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetevent), [**WSAResetEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsaresetevent)e [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) são diretamente mapeadas para as funções nativas do Windows correspondentes, usando o mesmo nome de função, mas sem o prefixo de WSA.

 

 



