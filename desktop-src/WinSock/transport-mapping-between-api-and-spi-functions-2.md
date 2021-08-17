---
description: A SPI de Transporte do Winsock é semelhante à API winsock, na forma como todas as funções básicas de soquete aparecem.
ms.assetid: 37ef8a69-2aa0-4824-8ca9-4b84158086db
title: Mapeamento de transporte entre funções DE API e SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebf4167353fa05c5656c588a9dff99c96564a5202ffdc4d21edf358c340634e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739936"
---
# <a name="transport-mapping-between-api-and-spi-functions"></a>Mapeamento de transporte entre funções DE API e SPI

A SPI de Transporte do Winsock é semelhante à API winsock, na forma como todas as funções básicas de soquete aparecem. Quando uma nova versão de uma função Winsock e a versão original existirem na API, somente a nova versão será aparecer na SPI. Isso é ilustrado na lista a seguir.

-   [**conectar**](/windows/desktop/api/Winsock2/nf-winsock2-connect) e [**WSAConectar ambos**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect) mapa para [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85))
-   [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) e [**WSAAccept map**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) para [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept)
-   [**soquete**](/windows/desktop/api/Winsock2/nf-winsock2-socket) [**e mapa WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) para [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket)

Outras funções de API que são recolhidos nas versões aprimoradas no SPI incluem:

-   [**Enviar**](/windows/desktop/api/Winsock2/nf-winsock2-send)
-   [**Sendto**](/windows/desktop/api/winsock/nf-winsock-sendto)
-   [**Recv**](/windows/desktop/api/winsock/nf-winsock-recv)
-   [**Recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom)
-   [**Ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket)

Funções de suporte como [**htonl,**](/windows/desktop/api/winsock/nf-winsock-htonl) [**htons**](/windows/desktop/api/winsock/nf-winsock-htons), [**ntohl**](/windows/desktop/api/winsock/nf-winsock-ntohl)e [**ntohs**](/windows/desktop/api/winsock/nf-winsock-ntohs) são implementadas no Ws232.dll e não são passadas para provedores \_ de serviços. O mesmo se mantém verdadeiro para as versões do WSA dessas funções.

Windows A enumeração do provedor de serviços sockets e as funções relacionadas ao gancho de bloqueio são realizadas no Ws232.dll, portanto, \_ [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [WSAIsBlocking,](/windows/desktop/api/winsock2/nf-winsock2-wsaisblocking) [WSASetBlockingHook](/windows/desktop/api/winsock2/nf-winsock2-wsasetblockinghook)e [WSAUnhookBlockingHook](/windows/desktop/api/winsock2/nf-winsock2-wsaunhookblockinghook) não aparecem como funções SPI.

Como os códigos de erro são retornados junto com as funções SPI, os equivalentes de [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) e [**WSASetLastError**](/windows/desktop/api/winsock/nf-winsock-wsasetlasterror) não são necessários na SPI.

As funções de espera e manipulação de objeto de evento, incluindo [**WSACreateEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent), [**WSACloseEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacloseevent), [**WSASetEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetevent), [**WSAResetEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsaresetevent)e [**WSAWaitForMultipleEvents,**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) são mapeadas diretamente para serviços Windows nativos e, portanto, não estão presentes na SPI.

Todas as funções de conversão e resolução de nome específicas de TCP/IP no Windows Sockets 1.1, como **GetXbyY,** **WSAAsyncGetXByY** e [**WSACancelAsyncRequest,**](/windows/desktop/api/winsock/nf-winsock-wsacancelasyncrequest)bem como [**gethostname,**](/windows/desktop/api/winsock/nf-winsock-gethostname) são implementadas no Ws232.dll em termos dos novos recursos de resolução \_ de nomes. Para obter mais informações, consulte [Resolução de nomes compatíveis para TCP/IP na SPI Windows Soquetes 1.1](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-spi-2.md). As funções de conversão, como [**\_ addr inet**](/windows/win32/api/winsock2/nf-winsock2-inet_addr) e [**inet \_ ntoa,**](/windows/win32/api/winsock2/nf-winsock2-inet_ntoa) são implementadas no Ws2 \_32.dll.

 

 
