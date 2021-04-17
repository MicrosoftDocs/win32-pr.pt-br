---
description: O SPI de transporte do Winsock é semelhante à API do Winsock, pois todas as funções básicas de soquete são exibidas.
ms.assetid: 37ef8a69-2aa0-4824-8ca9-4b84158086db
title: Mapeamento de transporte entre as funções API e SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0f11b950c48d0887f1e593c65f9d77e27c33917
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782509"
---
# <a name="transport-mapping-between-api-and-spi-functions"></a>Mapeamento de transporte entre as funções API e SPI

O SPI de transporte do Winsock é semelhante à API do Winsock, pois todas as funções básicas de soquete são exibidas. Quando uma nova versão de uma função do Winsock e a versão original existirem na API, somente a nova versão aparecerá no SPI. Isso é ilustrado na lista a seguir.

-   [**conectar**](/windows/desktop/api/Winsock2/nf-winsock2-connect) e [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect) mapear para [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85))
-   [**aceitar**](/windows/desktop/api/Winsock2/nf-winsock2-accept) e [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) o mapa para [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept)
-   [**soquete**](/windows/desktop/api/Winsock2/nf-winsock2-socket) e mapa de [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) para [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket)

Outras funções de API recolhidas nas versões aprimoradas do SPI incluem:

-   [**Enviar**](/windows/desktop/api/Winsock2/nf-winsock2-send)
-   [**Enviar**](/windows/desktop/api/winsock/nf-winsock-sendto)
-   [**recebidos**](/windows/desktop/api/winsock/nf-winsock-recv)
-   [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom)
-   [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket)

Funções de suporte como [**htonl**](/windows/desktop/api/winsock/nf-winsock-htonl), [**htons**](/windows/desktop/api/winsock/nf-winsock-htons), [**ntohl**](/windows/desktop/api/winsock/nf-winsock-ntohl)e [**ntohs**](/windows/desktop/api/winsock/nf-winsock-ntohs) são implementadas no Ws2 \_32.dll e não são passadas para provedores de serviço. O mesmo se aplica às versões de WSA dessas funções.

A enumeração do provedor de serviços do Windows Sockets e as funções relacionadas ao gancho de bloqueio são realizadas no \_32.dll Ws2, portanto, [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [WSAIsBlocking](/windows/desktop/api/winsock2/nf-winsock2-wsaisblocking), [WSASetBlockingHook](/windows/desktop/api/winsock2/nf-winsock2-wsasetblockinghook)e [WSAUnhookBlockingHook](/windows/desktop/api/winsock2/nf-winsock2-wsaunhookblockinghook) não aparecem como funções SPI.

Como os códigos de erro são retornados juntamente com as funções SPI, os equivalentes de [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) e [**WSASetLastError**](/windows/desktop/api/winsock/nf-winsock-wsasetlasterror) não são necessários no SPI.

As funções de manipulação e espera do objeto de evento, incluindo [**WSACreateEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent), [**WSACloseEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacloseevent), [**WSASetEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetevent), [**WSAResetEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsaresetevent)e [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) , são mapeadas diretamente para serviços nativos do Windows e, portanto, não estão presentes no SPI.

Todas as funções de conversão e resolução de nome específicas de TCP/IP no Windows Sockets 1,1, como **GetXbyY**, **WSAAsyncGetXByY** e [**WSACancelAsyncRequest**](/windows/desktop/api/winsock/nf-winsock-wsacancelasyncrequest), bem como [**GetHostName**](/windows/desktop/api/winsock/nf-winsock-gethostname) , são implementadas dentro do ws2 \_32.dll em termos de novos recursos de resolução de nomes. Para obter mais informações, consulte [resolução de nome compatível para TCP/IP no SPI do Windows sockets 1,1](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-spi-2.md). Funções de conversão, como o [**\_ endereço inet**](/windows/win32/api/winsock2/nf-winsock2-inet_addr) e [**\_ NTOA inet**](/windows/win32/api/winsock2/nf-winsock2-inet_ntoa) , são implementadas dentro do32.dll de ws2 \_ .

 

 
