---
description: Suporte a IPv6, anexo TCP/IP e Windows Sockets.
ms.assetid: 03e29ef1-2105-4cec-8b80-0f9acab046f6
title: Suporte a IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0ffc720a41c896653c74df2cb76f944cbbb310a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090380"
---
# <a name="ipv6-support"></a>Suporte a IPv6

Para dar suporte a IPv4 e IPv6 no Windows XP com Service Pack 1 (SP1) e no Windows Server 2003, um aplicativo precisa criar dois soquetes, um soquete para uso com IPv4 e um soquete para uso com IPv6. Esses dois soquetes devem ser tratados separadamente pelo aplicativo.

Se um provedor de serviços TCP/IP no Windows XP com SP1 e no Windows Server 2003 oferecer suporte ao endereçamento IPv4 e IPv6, ele deverá criar dois soquetes separados e escutar separadamente nesses soquetes:

-   Uma vez para IPv4.
-   Uma vez para a família de endereços IPv6.

O Windows Vista e versões posteriores oferecem a capacidade de criar um único soquete IPv6 que pode lidar com tráfego IPv6 e IPv4. Por exemplo, um soquete de escuta TCP para IPv6 é criado, colocado em modo de pilha dupla e vinculado à porta 5001. Esse soquete de pilha dupla pode aceitar conexões de clientes IPv6 TCP conectando-se à porta 5001 e de clientes TCP IPv4 conectando-se à porta 5001. Esse recurso permite um design de aplicativo bastante simplificado e reduz a sobrecarga de recursos necessária ao lançamento de operações em dois soquetes separados. No entanto, há algumas restrições que devem ser atendidas para que você possa usar um soquete de pilha dupla. Para obter mais informações, consulte [soquetes de pilha dupla](dual-stack-sockets.md).

[**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) retorna duas estruturas de [**\_ informações de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para cada um dos tipos de soquete com suporte (Sock \_ Stream, Sock \_ DGRAM, Sock \_ RAW). O **iAddressFamily** deve ser definido como \_ inet de AF para endereçamento IPv4 e para AF \_ INET6 para endereçamento IPv6.

Os endereços IPv6 são descritos nas estruturas a seguir.

``` syntax
struct in_addr6 {
    u_char    s6_addr[16];             /* IPv6 address */
};

struct sockaddr_in6 {
    short             sin6_family;     /* AF_INET6 */
    u_short           sin6_port;       /* Transport level port number */
    u_long            sin6_flowinfo;   /* IPv6 flow information */
    struct in_addr6   sin6_addr;       /* IPv6 address */
    u_long            sin6_scope_id;   /* set of interfaces for a scope */
   };
```

Se um aplicativo usa funções do Windows Sockets 1,1 e deseja usar endereços IPv6, ele pode continuar a usar todas as funções antigas que usam a estrutura [**SOCKADDR**](sockaddr-2.md) como um dos parâmetros ([**BIND**](/windows/desktop/api/winsock/nf-winsock-bind), [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto)e [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom), [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept)e assim por diante). A única alteração necessária é usar **SOCKADDR \_ In6** em vez de **SOCKADDR \_ no**.

No entanto, as funções de resolução de nome ([**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname), [**GetHostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)e assim por diante) e funções de conversão de endereço (endereço [**inet \_**](/windows/win32/api/winsock2/nf-winsock2-inet_addr), [**inet \_ NTOA**](/windows/win32/api/winsock2/nf-winsock2-inet_ntoa)) não podem ser reutilizadas porque supõem que um endereço IP tem 4 bytes de comprimento. Um aplicativo que deseja executar a resolução de nomes e a conversão de endereços para endereços IPv6 deve usar funções específicas do Windows Sockets 2. Muitas novas funções foram introduzidas para permitir que aplicativos do Windows Sockets 2 tirem proveito do IPv6, incluindo as funções [**Getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) e [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) .

Para obter mais informações sobre como habilitar recursos IPv6 em um aplicativo, consulte o [guia IPv6 para aplicativos do Windows Sockets](ipv6-guide-for-windows-sockets-applications-2.md).

 

 
