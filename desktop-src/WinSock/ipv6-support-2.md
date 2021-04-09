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
# <a name="ipv6-support"></a><span data-ttu-id="1b28d-103">Suporte a IPv6</span><span class="sxs-lookup"><span data-stu-id="1b28d-103">IPv6 Support</span></span>

<span data-ttu-id="1b28d-104">Para dar suporte a IPv4 e IPv6 no Windows XP com Service Pack 1 (SP1) e no Windows Server 2003, um aplicativo precisa criar dois soquetes, um soquete para uso com IPv4 e um soquete para uso com IPv6.</span><span class="sxs-lookup"><span data-stu-id="1b28d-104">In order to support both IPv4 and IPv6 on Windows XP with Service Pack 1 (SP1) and on Windows Server 2003, an application has to create two sockets, one socket for use with IPv4 and one socket for use with IPv6.</span></span> <span data-ttu-id="1b28d-105">Esses dois soquetes devem ser tratados separadamente pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1b28d-105">These two sockets must be handled separately by the application.</span></span>

<span data-ttu-id="1b28d-106">Se um provedor de serviços TCP/IP no Windows XP com SP1 e no Windows Server 2003 oferecer suporte ao endereçamento IPv4 e IPv6, ele deverá criar dois soquetes separados e escutar separadamente nesses soquetes:</span><span class="sxs-lookup"><span data-stu-id="1b28d-106">If a TCP/IP service provider on Windows XP with SP1 and on Windows Server 2003 supports IPv4 and IPv6 addressing, it must create two separate sockets and listen separately on these sockets:</span></span>

-   <span data-ttu-id="1b28d-107">Uma vez para IPv4.</span><span class="sxs-lookup"><span data-stu-id="1b28d-107">Once for IPv4.</span></span>
-   <span data-ttu-id="1b28d-108">Uma vez para a família de endereços IPv6.</span><span class="sxs-lookup"><span data-stu-id="1b28d-108">Once for the IPv6 address family.</span></span>

<span data-ttu-id="1b28d-109">O Windows Vista e versões posteriores oferecem a capacidade de criar um único soquete IPv6 que pode lidar com tráfego IPv6 e IPv4.</span><span class="sxs-lookup"><span data-stu-id="1b28d-109">Windows Vista and later offer the ability to create a single IPv6 socket which can handle both IPv6 and IPv4 traffic.</span></span> <span data-ttu-id="1b28d-110">Por exemplo, um soquete de escuta TCP para IPv6 é criado, colocado em modo de pilha dupla e vinculado à porta 5001.</span><span class="sxs-lookup"><span data-stu-id="1b28d-110">For example, a TCP listening socket for IPv6 is created, put into dual stack mode, and bound to port 5001.</span></span> <span data-ttu-id="1b28d-111">Esse soquete de pilha dupla pode aceitar conexões de clientes IPv6 TCP conectando-se à porta 5001 e de clientes TCP IPv4 conectando-se à porta 5001.</span><span class="sxs-lookup"><span data-stu-id="1b28d-111">This dual-stack socket can accept connections from IPv6 TCP clients connecting to port 5001 and from IPv4 TCP clients connecting to port 5001.</span></span> <span data-ttu-id="1b28d-112">Esse recurso permite um design de aplicativo bastante simplificado e reduz a sobrecarga de recursos necessária ao lançamento de operações em dois soquetes separados.</span><span class="sxs-lookup"><span data-stu-id="1b28d-112">This feature allows for greatly simplified application design and reduces the resource overhead required of posting operations on two separate sockets.</span></span> <span data-ttu-id="1b28d-113">No entanto, há algumas restrições que devem ser atendidas para que você possa usar um soquete de pilha dupla.</span><span class="sxs-lookup"><span data-stu-id="1b28d-113">However, there are some restrictions that must be met in order to use a dual-stack socket.</span></span> <span data-ttu-id="1b28d-114">Para obter mais informações, consulte [soquetes de pilha dupla](dual-stack-sockets.md).</span><span class="sxs-lookup"><span data-stu-id="1b28d-114">For more information, see [Dual-Stack Sockets](dual-stack-sockets.md).</span></span>

<span data-ttu-id="1b28d-115">[**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) retorna duas estruturas de [**\_ informações de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para cada um dos tipos de soquete com suporte (Sock \_ Stream, Sock \_ DGRAM, Sock \_ RAW).</span><span class="sxs-lookup"><span data-stu-id="1b28d-115">[**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) returns two [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structures for each of the supported socket types (SOCK\_STREAM, SOCK\_DGRAM, SOCK\_RAW).</span></span> <span data-ttu-id="1b28d-116">O **iAddressFamily** deve ser definido como \_ inet de AF para endereçamento IPv4 e para AF \_ INET6 para endereçamento IPv6.</span><span class="sxs-lookup"><span data-stu-id="1b28d-116">The **iAddressFamily** must by set to AF\_INET for IPv4 addressing, and to AF\_INET6 for IPv6 addressing.</span></span>

<span data-ttu-id="1b28d-117">Os endereços IPv6 são descritos nas estruturas a seguir.</span><span class="sxs-lookup"><span data-stu-id="1b28d-117">The IPv6 addresses are described in the following structures.</span></span>

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

<span data-ttu-id="1b28d-118">Se um aplicativo usa funções do Windows Sockets 1,1 e deseja usar endereços IPv6, ele pode continuar a usar todas as funções antigas que usam a estrutura [**SOCKADDR**](sockaddr-2.md) como um dos parâmetros ([**BIND**](/windows/desktop/api/winsock/nf-winsock-bind), [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto)e [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom), [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept)e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="1b28d-118">If an application uses Windows Sockets 1.1 functions and wants to use IPv6 addresses, it may continue to use all the old functions that take the [**sockaddr**](sockaddr-2.md) structure as one of the parameters ([**bind**](/windows/desktop/api/winsock/nf-winsock-bind), [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto), and [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom), [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), and so forth).</span></span> <span data-ttu-id="1b28d-119">A única alteração necessária é usar **SOCKADDR \_ In6** em vez de **SOCKADDR \_ no**.</span><span class="sxs-lookup"><span data-stu-id="1b28d-119">The only change that is required is to use **sockaddr\_in6** instead of **sockaddr\_in**.</span></span>

<span data-ttu-id="1b28d-120">No entanto, as funções de resolução de nome ([**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname), [**GetHostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)e assim por diante) e funções de conversão de endereço (endereço [**inet \_**](/windows/win32/api/winsock2/nf-winsock2-inet_addr), [**inet \_ NTOA**](/windows/win32/api/winsock2/nf-winsock2-inet_ntoa)) não podem ser reutilizadas porque supõem que um endereço IP tem 4 bytes de comprimento.</span><span class="sxs-lookup"><span data-stu-id="1b28d-120">However, the name resolution functions ([**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname), [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr), and so forth) and address conversion functions ([**inet\_addr**](/windows/win32/api/winsock2/nf-winsock2-inet_addr), [**inet\_ntoa**](/windows/win32/api/winsock2/nf-winsock2-inet_ntoa)) cannot be reused because they assume an IP address is 4 bytes in length.</span></span> <span data-ttu-id="1b28d-121">Um aplicativo que deseja executar a resolução de nomes e a conversão de endereços para endereços IPv6 deve usar funções específicas do Windows Sockets 2.</span><span class="sxs-lookup"><span data-stu-id="1b28d-121">An application that wants to perform name resolution and address conversion for IPv6 addresses must use Windows Sockets 2-specific functions.</span></span> <span data-ttu-id="1b28d-122">Muitas novas funções foram introduzidas para permitir que aplicativos do Windows Sockets 2 tirem proveito do IPv6, incluindo as funções [**Getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) e [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) .</span><span class="sxs-lookup"><span data-stu-id="1b28d-122">Many new functions have been introduced to enable Windows Sockets 2 applications to take advantage of IPv6, including the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) and [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) functions.</span></span>

<span data-ttu-id="1b28d-123">Para obter mais informações sobre como habilitar recursos IPv6 em um aplicativo, consulte o [guia IPv6 para aplicativos do Windows Sockets](ipv6-guide-for-windows-sockets-applications-2.md).</span><span class="sxs-lookup"><span data-stu-id="1b28d-123">For more information on how to enable IPv6 capabilities in an application, see the [IPv6 Guide for Windows Sockets Applications](ipv6-guide-for-windows-sockets-applications-2.md).</span></span>

 

 
