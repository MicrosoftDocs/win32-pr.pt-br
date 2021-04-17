---
description: Novas funções foram introduzidas na interface do Windows Sockets especificamente projetadas para facilitar a programação do Windows Sockets. Um dos benefícios dessas novas funções do Windows Sockets é o suporte integrado para IPv6 e IPv4.
ms.assetid: 83262f2b-a335-4bbd-b2e3-6c7744b3ee50
title: Chamadas de função para aplicativos Winsock IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a56fe5087e17a9a4eb1337ac803b8500b1fe9c27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105784666"
---
# <a name="function-calls-for-ipv6-winsock-applications"></a><span data-ttu-id="847cd-104">Chamadas de função para aplicativos Winsock IPv6</span><span class="sxs-lookup"><span data-stu-id="847cd-104">Function Calls for IPv6 Winsock Applications</span></span>

<span data-ttu-id="847cd-105">Novas funções foram introduzidas na interface do Windows Sockets especificamente projetadas para facilitar a programação do Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="847cd-105">New functions have been introduced to the Windows Sockets interface specifically designed to make Windows Sockets programming easier.</span></span> <span data-ttu-id="847cd-106">Um dos benefícios dessas novas funções do Windows Sockets é o suporte integrado para IPv6 e IPv4.</span><span class="sxs-lookup"><span data-stu-id="847cd-106">One of the benefits of these new Windows Sockets functions is integrated support for both IPv6 and IPv4.</span></span>

<span data-ttu-id="847cd-107">Essas novas funções do Windows Sockets incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="847cd-107">These new Windows Sockets functions include the following:</span></span>

-   [<span data-ttu-id="847cd-108">**WSAConnectByName**</span><span class="sxs-lookup"><span data-stu-id="847cd-108">**WSAConnectByName**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)
-   [<span data-ttu-id="847cd-109">**WSAConnectByList**</span><span class="sxs-lookup"><span data-stu-id="847cd-109">**WSAConnectByList**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)
-   <span data-ttu-id="847cd-110">[**Getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) Family of Functions **(getaddrinfo**, [**GetAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa), [**GetAddrInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow), [**freeaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfo), [**FreeAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfoex), [**FreeAddrInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfow)e [**SetAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-setaddrinfoexa))</span><span class="sxs-lookup"><span data-stu-id="847cd-110">[**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) family of functions (**getaddrinfo**, [**GetAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa), [**GetAddrInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow), [**freeaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfo), [**FreeAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfoex), [**FreeAddrInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfow), and [**SetAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-setaddrinfoexa))</span></span>
-   <span data-ttu-id="847cd-111">[**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) Family of Functions (**getnameinfo** e [**GetNameInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfow))</span><span class="sxs-lookup"><span data-stu-id="847cd-111">[**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) family of functions (**getnameinfo** and [**GetNameInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfow))</span></span>

<span data-ttu-id="847cd-112">Além disso, novas funções auxiliares de IP com suporte para IPv6 e IPv4 foram adicionadas para simplificar a programação do Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="847cd-112">In addition, new IP Helper functions with support for both IPv6 and IPv4 have been added to simplify Windows Sockets programming.</span></span> <span data-ttu-id="847cd-113">Essas novas funções auxiliares de IP incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="847cd-113">These new IP Helper functions include the following:</span></span>

-   [<span data-ttu-id="847cd-114">**GetAdaptersAddresses**</span><span class="sxs-lookup"><span data-stu-id="847cd-114">**GetAdaptersAddresses**</span></span>](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses)

<span data-ttu-id="847cd-115">Ao adicionar suporte a IPv6 a um aplicativo, as seguintes diretrizes devem ser usadas:</span><span class="sxs-lookup"><span data-stu-id="847cd-115">When adding IPv6 support to an application the following guidelines should be used:</span></span>

-   <span data-ttu-id="847cd-116">Use [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) para estabelecer uma conexão com um ponto de extremidade, dado um nome de host e uma porta.</span><span class="sxs-lookup"><span data-stu-id="847cd-116">Use [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) to establish a connection to an endpoint given a host name and port.</span></span> <span data-ttu-id="847cd-117">A função **WSAConnectByName** está disponível no Windows Vista e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="847cd-117">The **WSAConnectByName** function is available on Windows Vista and later.</span></span>
-   <span data-ttu-id="847cd-118">Use [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) para estabelecer uma conexão com uma de uma coleção de pontos de extremidade possíveis representados por um conjunto de endereços de destino (nomes de host e portas).</span><span class="sxs-lookup"><span data-stu-id="847cd-118">Use [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) to establish a connection to one out of a collection of possible endpoints represented by a set of destination addresses (host names and ports).</span></span> <span data-ttu-id="847cd-119">A função **WSAConnectByList** está disponível no Windows Vista e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="847cd-119">The **WSAConnectByList** function is available on Windows Vista and later.</span></span>
-   <span data-ttu-id="847cd-120">Substitua as chamadas de função [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) por chamadas para uma das novas funções [**Getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) do Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="847cd-120">Replace [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) function calls with calls to one of the new [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) Windows Sockets functions.</span></span> <span data-ttu-id="847cd-121">A função **Getaddrinfo** com suporte para o protocolo IPv6 está disponível no Windows XP e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="847cd-121">The **getaddrinfo** function with support for the IPv6 protocol is available on Windows XP and later.</span></span> <span data-ttu-id="847cd-122">O protocolo IPv6 também tem suporte no Windows 2000 quando a versão prévia da tecnologia IPv6 para Windows 2000 está instalada.</span><span class="sxs-lookup"><span data-stu-id="847cd-122">The IPv6 protocol is also supported on Windows 2000 when the IPv6 Technology Preview for Windows 2000 is installed.</span></span>
-   <span data-ttu-id="847cd-123">Substitua as chamadas de função [**GetHostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) por chamadas para uma das novas funções do Windows Sockets do [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) .</span><span class="sxs-lookup"><span data-stu-id="847cd-123">Replace [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) function calls with calls to one of the new [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) Windows Sockets functions.</span></span> <span data-ttu-id="847cd-124">A função **getnameinfo** com suporte para o protocolo IPv6 está disponível no Windows XP e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="847cd-124">The **getnameinfo** function with support for the IPv6 protocol is available on Windows XP and later.</span></span> <span data-ttu-id="847cd-125">O protocolo IPv6 também tem suporte no Windows 2000 quando a versão prévia da tecnologia IPv6 para Windows 2000 está instalada.</span><span class="sxs-lookup"><span data-stu-id="847cd-125">The IPv6 protocol is also supported on Windows 2000 when the IPv6 Technology Preview for Windows 2000 is installed.</span></span>

## <a name="wsaconnectbyname"></a><span data-ttu-id="847cd-126">WSAConnectByName</span><span class="sxs-lookup"><span data-stu-id="847cd-126">WSAConnectByName</span></span>

<span data-ttu-id="847cd-127">A função [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) simplifica a conexão com um ponto de extremidade usando um soquete baseado em fluxo, dado o nome de host ou endereço IP do destino (IPv4 ou IPv6).</span><span class="sxs-lookup"><span data-stu-id="847cd-127">The [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) function simplifies connecting to an endpoint using a stream-based socket given the destination's hostname or IP address (IPv4 or IPv6).</span></span> <span data-ttu-id="847cd-128">Essa função reduz o código-fonte necessário para criar um aplicativo IP que é independente da versão do protocolo IP usado.</span><span class="sxs-lookup"><span data-stu-id="847cd-128">This function reduces the source code required to create an IP application that is agnostic to the version of the IP protocol used.</span></span> <span data-ttu-id="847cd-129">O **WSAConnectByName** substitui as seguintes etapas em um aplicativo TCP típico para uma única chamada de função:</span><span class="sxs-lookup"><span data-stu-id="847cd-129">**WSAConnectByName** replaces the following steps in a typical TCP application to a single function call:</span></span>

-   <span data-ttu-id="847cd-130">Resolva um nome de host para um conjunto de endereços IP.</span><span class="sxs-lookup"><span data-stu-id="847cd-130">Resolve a hostname to a set of IP addresses.</span></span>
-   <span data-ttu-id="847cd-131">Para cada endereço IP:</span><span class="sxs-lookup"><span data-stu-id="847cd-131">For each IP address:</span></span>
    -   <span data-ttu-id="847cd-132">Crie um soquete da família de endereços apropriada.</span><span class="sxs-lookup"><span data-stu-id="847cd-132">Create a socket of the appropriate address family.</span></span>
    -   <span data-ttu-id="847cd-133">Tentativas de conexão com o endereço IP remoto.</span><span class="sxs-lookup"><span data-stu-id="847cd-133">Attempts to connect to the remote IP address.</span></span> <span data-ttu-id="847cd-134">Se a conexão foi bem-sucedida, ela retorna; caso contrário, será tentado o próximo endereço IP remoto para o host.</span><span class="sxs-lookup"><span data-stu-id="847cd-134">If the connection was successful, it returns; otherwise the next remote IP address for the host is tried.</span></span>

<span data-ttu-id="847cd-135">A função [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) vai além de apenas resolver o nome e, em seguida, tentar se conectar.</span><span class="sxs-lookup"><span data-stu-id="847cd-135">The [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) function goes beyond just resolving the name and then attempting to connect.</span></span> <span data-ttu-id="847cd-136">A função usa todos os endereços remotos retornados pela resolução de nomes e todos os endereços IP de origem do computador local.</span><span class="sxs-lookup"><span data-stu-id="847cd-136">The function uses all of the remote addresses returned by name resolution and all of the local machine's source IP addresses.</span></span> <span data-ttu-id="847cd-137">Ele tenta primeiro se conectar usando pares de endereços com a maior chance de sucesso.</span><span class="sxs-lookup"><span data-stu-id="847cd-137">It first attempts to connect using address pairs with the highest chance of success.</span></span> <span data-ttu-id="847cd-138">Portanto, **WSAConnectByName** não apenas garante que uma conexão será estabelecida, se possível, mas também minimiza o tempo para estabelecer a conexão.</span><span class="sxs-lookup"><span data-stu-id="847cd-138">Therefore, **WSAConnectByName** not only ensures that a connection will be established if possible, but it also minimizes the time to establish the connection.</span></span>

<span data-ttu-id="847cd-139">Para habilitar as comunicações IPv6 e IPv4, use o seguinte método:</span><span class="sxs-lookup"><span data-stu-id="847cd-139">To enable both IPv6 and IPv4 communications, use the following method:</span></span>

-   <span data-ttu-id="847cd-140">A função [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) deve ser chamada em um soquete criado para a \_ família de endereços INET6 da AF para desabilitar a opção de soquete **IPv6 \_ V6ONLY** antes de chamar [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea).</span><span class="sxs-lookup"><span data-stu-id="847cd-140">The [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function must be called on a socket created for the AF\_INET6 address family to disable the **IPV6\_V6ONLY** socket option before calling [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea).</span></span> <span data-ttu-id="847cd-141">Isso é feito chamando a função **setsockopt** no soquete com o parâmetro *Level* definido como **IPPROTO \_ IPv6** (consulte Opções de [ \_ soquete IPPROTO IPv6](ipproto-ipv6-socket-options.md)), o parâmetro *OptName* definido como **IPv6 \_ V6ONLY** e o valor do parâmetro *optvalue* definido como zero.</span><span class="sxs-lookup"><span data-stu-id="847cd-141">This is accomplished by calling the **setsockopt** function on the socket with the *level* parameter set to **IPPROTO\_IPV6** (see [IPPROTO\_IPV6 Socket Options](ipproto-ipv6-socket-options.md)), the *optname* parameter set to **IPV6\_V6ONLY**, and the *optvalue* parameter value set to zero.</span></span>

<span data-ttu-id="847cd-142">Se um aplicativo precisar se associar a um endereço local ou a uma porta específica, [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) não poderá ser usado, pois o parâmetro Socket para **WSAConnectByName** deve ser um soquete não associado.</span><span class="sxs-lookup"><span data-stu-id="847cd-142">If an application needs to bind to a specific local address or port, then [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) cannot be used since the socket parameter to **WSAConnectByName** must be an unbound socket.</span></span>

<span data-ttu-id="847cd-143">O exemplo de código a seguir mostra apenas algumas linhas de código que são necessárias para usar essa função para implementar um aplicativo que seja independente da versão de IP.</span><span class="sxs-lookup"><span data-stu-id="847cd-143">The code example below shows only a few lines of code are needed to use this function to implement an application that is agnostic to the IP version.</span></span>

<span data-ttu-id="847cd-144">Estabelecer uma conexão usando o [ **WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)</span><span class="sxs-lookup"><span data-stu-id="847cd-144">Establish a connection using [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

SOCKET OpenAndConnect(LPWSTR NodeName, LPWSTR PortName) 
{
    SOCKET ConnSocket;
    DWORD ipv6only = 0;
    int iResult;
    BOOL bSuccess;
    SOCKADDR_STORAGE LocalAddr = {0};
    SOCKADDR_STORAGE RemoteAddr = {0};
    DWORD dwLocalAddr = sizeof(LocalAddr);
    DWORD dwRemoteAddr = sizeof(RemoteAddr);
  
    ConnSocket = socket(AF_INET6, SOCK_STREAM, 0);
    if (ConnSocket == INVALID_SOCKET){
        return INVALID_SOCKET;
    }

    iResult = setsockopt(ConnSocket, IPPROTO_IPV6,
        IPV6_V6ONLY, (char*)&ipv6only, sizeof(ipv6only) );
    if (iResult == SOCKET_ERROR){
        closesocket(ConnSocket);
        return INVALID_SOCKET;       
    }

    bSuccess = WSAConnectByName(ConnSocket, NodeName, 
            PortName, &dwLocalAddr,
            (SOCKADDR*)&LocalAddr,
            &dwRemoteAddr,
            (SOCKADDR*)&RemoteAddr,
            NULL,
            NULL);
    if (bSuccess){
        return ConnSocket;
    } else {
        return INVALID_SOCKET;
    }
}
```



## <a name="wsaconnectbylist"></a><span data-ttu-id="847cd-145">WSAConnectByList</span><span class="sxs-lookup"><span data-stu-id="847cd-145">WSAConnectByList</span></span>

<span data-ttu-id="847cd-146">A função [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) estabelece uma conexão com um host, dado um conjunto de hosts possíveis (representado por um conjunto de portas e endereços IP de destino).</span><span class="sxs-lookup"><span data-stu-id="847cd-146">The [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) function establishes a connection to a host given a set of possible hosts (represented by a set of destination IP addresses and ports).</span></span> <span data-ttu-id="847cd-147">A função usa todos os endereços IP e portas para o ponto de extremidade e todos os endereços IP do computador local e tenta uma conexão usando todas as combinações de endereços possíveis.</span><span class="sxs-lookup"><span data-stu-id="847cd-147">The function takes all IP addresses and ports for the endpoint and all of the local machine's IP addresses, and attempts a connection using all possible address combinations.</span></span>

<span data-ttu-id="847cd-148">[**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) está relacionado à função [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) .</span><span class="sxs-lookup"><span data-stu-id="847cd-148">[**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) is related to the [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) function.</span></span> <span data-ttu-id="847cd-149">Em vez de usar um único nome de host, o **WSAConnectByList** aceita uma lista de hosts (endereços de destino e pares de porta) e se conecta a um dos endereços e portas na lista fornecida.</span><span class="sxs-lookup"><span data-stu-id="847cd-149">Instead of taking a single hostname, **WSAConnectByList** accepts a list of hosts (destination addresses and port pairs) and connects to one of the addresses and ports in the provided list.</span></span> <span data-ttu-id="847cd-150">Essa função foi projetada para dar suporte a cenários nos quais um aplicativo precisa se conectar a qualquer host disponível fora de uma lista de hosts potenciais.</span><span class="sxs-lookup"><span data-stu-id="847cd-150">This function is designed to support scenarios in which an application needs to connect to any available host out of a list of potential hosts.</span></span>

<span data-ttu-id="847cd-151">Semelhante ao [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea), a função [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) reduz significativamente o código-fonte necessário para criar, ligar e conectar um soquete.</span><span class="sxs-lookup"><span data-stu-id="847cd-151">Similar to [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea), the [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) function significantly reduces the source code required to create, bind and connect a socket.</span></span> <span data-ttu-id="847cd-152">Essa função facilita muito a implementação de um aplicativo que seja independente da versão do IP.</span><span class="sxs-lookup"><span data-stu-id="847cd-152">This function makes it much easier to implement an application that is agnostic to the IP version.</span></span> <span data-ttu-id="847cd-153">A lista de endereços para um host aceito por essa função pode ser endereços IPv6 ou IPv4.</span><span class="sxs-lookup"><span data-stu-id="847cd-153">The list of addresses for a host accepted by this function may be IPv6 or IPv4 addresses.</span></span>

<span data-ttu-id="847cd-154">Para permitir que os endereços IPv6 e IPv4 sejam passados na lista de endereços única aceita pela função, as etapas a seguir devem ser executadas antes de chamar a função:</span><span class="sxs-lookup"><span data-stu-id="847cd-154">To enable both IPv6 and IPv4 addresses to be passed in the single address list accepted by the function, the following steps must be performed prior to calling the function:</span></span>

-   <span data-ttu-id="847cd-155">A função [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) deve ser chamada em um soquete criado para a \_ família de endereços INET6 da AF para desabilitar a opção de soquete **IPv6 \_ V6ONLY** antes de chamar [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist).</span><span class="sxs-lookup"><span data-stu-id="847cd-155">The [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function must be called on a socket created for the AF\_INET6 address family to disable the **IPV6\_V6ONLY** socket option before calling [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist).</span></span> <span data-ttu-id="847cd-156">Isso é feito chamando a função **setsockopt** no soquete com o parâmetro *Level* definido como **IPPROTO \_ IPv6** (consulte Opções de [ \_ soquete IPPROTO IPv6](ipproto-ipv6-socket-options.md)), o parâmetro *OptName* definido como **IPv6 \_ V6ONLY** e o valor do parâmetro *optvalue* definido como zero.</span><span class="sxs-lookup"><span data-stu-id="847cd-156">This is accomplished by calling the **setsockopt** function on the socket with the *level* parameter set to **IPPROTO\_IPV6** (see [IPPROTO\_IPV6 Socket Options](ipproto-ipv6-socket-options.md)), the *optname* parameter set to **IPV6\_V6ONLY**, and the *optvalue* parameter value set to zero.</span></span>
-   <span data-ttu-id="847cd-157">Todos os endereços IPv4 devem ser representados no formato de endereço IPv6 mapeado para IPv4, o que permite que um aplicativo somente IPv6 se comunique com um nó IPv4.</span><span class="sxs-lookup"><span data-stu-id="847cd-157">Any IPv4 addresses must be represented in the IPv4-mapped IPv6 address format which enables an IPv6 only application to communicate with an IPv4 node.</span></span> <span data-ttu-id="847cd-158">O formato de endereço IPv6 mapeado para IPv4 permite que o endereço IPv4 de um nó IPv4 seja representado como um endereço IPv6.</span><span class="sxs-lookup"><span data-stu-id="847cd-158">The IPv4-mapped IPv6 address format allows the IPv4 address of an IPv4 node to be represented as an IPv6 address.</span></span> <span data-ttu-id="847cd-159">O endereço IPv4 é codificado em 32 bits de ordem inferior do endereço IPv6 e os bits 96 de ordem superior contêm o prefixo fixo 0:0: 0:0: 0: FFFF.</span><span class="sxs-lookup"><span data-stu-id="847cd-159">The IPv4 address is encoded into the low-order 32 bits of the IPv6 address, and the high-order 96 bits hold the fixed prefix 0:0:0:0:0:FFFF.</span></span> <span data-ttu-id="847cd-160">O formato de endereço IPv6 mapeado para IPv4 é especificado no RFC 4291.</span><span class="sxs-lookup"><span data-stu-id="847cd-160">The IPv4-mapped IPv6 address format is specified in RFC 4291.</span></span> <span data-ttu-id="847cd-161">Para obter mais informações, consulte [www.ietf.org/rfc/rfc4291.txt](https://tools.ietf.org/html/rfc4291).</span><span class="sxs-lookup"><span data-stu-id="847cd-161">For more information, see [www.ietf.org/rfc/rfc4291.txt](https://tools.ietf.org/html/rfc4291).</span></span> <span data-ttu-id="847cd-162">A \_ macro IN6ADDR SETV4MAPPED em *Mstcpip. h* pode ser usada para converter um endereço IPv4 para o formato de endereço IPv6 mapeado para IPv4 necessário.</span><span class="sxs-lookup"><span data-stu-id="847cd-162">The IN6ADDR\_SETV4MAPPED macro in *Mstcpip.h* can be used to convert an IPv4 address to the required IPv4-mapped IPv6 address format.</span></span>

<span data-ttu-id="847cd-163">Estabelecer uma conexão usando o [ **WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)</span><span class="sxs-lookup"><span data-stu-id="847cd-163">Establish a Connection Using [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

SOCKET OpenAndConnect(SOCKET_ADDRESS_LIST *AddressList) 
{
    SOCKET ConnSocket;
    DWORD ipv6only = 0;
    int iResult;
    BOOL bSuccess;
    SOCKADDR_STORAGE LocalAddr = {0};
    SOCKADDR_STORAGE RemoteAddr = {0};
    DWORD dwLocalAddr = sizeof(LocalAddr);
    DWORD dwRemoteAddr = sizeof(RemoteAddr);

    ConnSocket = socket(AF_INET6, SOCK_STREAM, 0);
    if (ConnSocket == INVALID_SOCKET){
        return INVALID_SOCKET;
    }

    iResult = setsockopt(ConnSocket, IPPROTO_IPV6,
        IPV6_V6ONLY, (char*)&ipv6only, sizeof(ipv6only) );
    if (iResult == SOCKET_ERROR){
        closesocket(ConnSocket);
        return INVALID_SOCKET;       
    }

    // AddressList may contain IPv6 and/or IPv4Mapped addresses
    bSuccess = WSAConnectByList(ConnSocket,
            AddressList,
            &dwLocalAddr,
            (SOCKADDR*)&LocalAddr,
            &dwRemoteAddr,
            (SOCKADDR*)&RemoteAddr,
            NULL,
            NULL);
    if (bSuccess){
        return ConnSocket;
    } else {
        return INVALID_SOCKET;
    }
}
```



## <a name="getaddrinfo"></a><span data-ttu-id="847cd-164">getaddrinfo</span><span class="sxs-lookup"><span data-stu-id="847cd-164">getaddrinfo</span></span>

<span data-ttu-id="847cd-165">A função **Getaddrinfo** também executa o trabalho de processamento de muitas funções.</span><span class="sxs-lookup"><span data-stu-id="847cd-165">The **getaddrinfo** function also performs the processing work of many functions.</span></span> <span data-ttu-id="847cd-166">Anteriormente, as chamadas para várias funções do Windows Socket eram necessárias para criar, abrir e associar um endereço a um soquete.</span><span class="sxs-lookup"><span data-stu-id="847cd-166">Previously, calls to a number of Windows Sockets functions were required to create, open, and then bind an address to a socket.</span></span> <span data-ttu-id="847cd-167">Com a função **Getaddrinfo** , as linhas de código-fonte necessárias para executar esse trabalho podem ser significativamente reduzidas.</span><span class="sxs-lookup"><span data-stu-id="847cd-167">With the **getaddrinfo** function, the lines of source code necessary to perform such work can be significantly reduced.</span></span> <span data-ttu-id="847cd-168">Os dois exemplos a seguir ilustram o código-fonte necessário para executar essas tarefas com e sem a função **Getaddrinfo** .</span><span class="sxs-lookup"><span data-stu-id="847cd-168">The following two examples illustrate the source code necessary to perform these tasks with and without the **getaddrinfo** function.</span></span>

<span data-ttu-id="847cd-169">Executar um Open, Connect e BIND usando **Getaddrinfo**</span><span class="sxs-lookup"><span data-stu-id="847cd-169">Perform an Open, Connect, and Bind Using **getaddrinfo**</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

SOCKET OpenAndConnect(char *ServerName, char *PortName, int SocketType)
{
    SOCKET ConnSocket;
    ADDRINFO *AI;

    if (getaddrinfo(ServerName, PortName, NULL, &AI) != 0) {
        return INVALID_SOCKET;
    }

    ConnSocket = socket(AI->ai_family, SocketType, 0);
    if (ConnSocket == INVALID_SOCKET) {
        freeaddrinfo(AI);
        return INVALID_SOCKET;
    }

    if (connect(ConnSocket, AI->ai_addr, (int) AI->ai_addrlen) == SOCKET_ERROR) {
        closesocket(ConnSocket);
        freeaddrinfo(AI);
        return INVALID_SOCKET;
    }

    return ConnSocket;
}
```



<span data-ttu-id="847cd-170">Executar um Open, Connect e BIND sem usar **Getaddrinfo**</span><span class="sxs-lookup"><span data-stu-id="847cd-170">Perform an Open, Connect, and Bind Without Using **getaddrinfo**</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

SOCKET OpenAndConnect(char *ServerName, unsigned short Port, int SocketType) 
{
    SOCKET ConnSocket;
    LPHOSTENT hp;
    SOCKADDR_IN ServerAddr;
    
    ConnSocket = socket(AF_INET, SocketType, 0); /* Open a socket */
    if (ConnSocket < 0 ) {
        return INVALID_SOCKET;
    }

    memset(&ServerAddr, 0, sizeof(ServerAddr));
    ServerAddr.sin_family = AF_INET;
    ServerAddr.sin_port = htons(Port);

    if (isalpha(ServerName[0])) {   /* server address is a name */
        hp = gethostbyname(ServerName);
        if (hp == NULL) {
            return INVALID_SOCKET;
        }
        ServerAddr.sin_addr.s_addr = (ULONG) hp->h_addr;
    } else { /* Convert nnn.nnn address to a usable one */
        ServerAddr.sin_addr.s_addr = inet_addr(ServerName);
    } 

    if (connect(ConnSocket, (LPSOCKADDR)&ServerAddr, 
        sizeof(ServerAddr)) == SOCKET_ERROR)
    {
        closesocket(ConnSocket);
        return INVALID_SOCKET;
    }

    return ConnSocket;
}
```



<span data-ttu-id="847cd-171">Observe que ambos os exemplos de código-fonte executam as mesmas tarefas, mas o primeiro exemplo, usando a função **Getaddrinfo** , requer menos linhas de código-fonte e pode manipular endereços IPv6 ou IPv4.</span><span class="sxs-lookup"><span data-stu-id="847cd-171">Notice that both of these source code examples perform the same tasks, but the first example, using the **getaddrinfo** function, requires fewer lines of source code, and can handle either IPv6 or IPv4 addresses.</span></span> <span data-ttu-id="847cd-172">O número de linhas do código-fonte eliminado usando a função **Getaddrinfo** varia.</span><span class="sxs-lookup"><span data-stu-id="847cd-172">The number of lines of source code eliminated by using the **getaddrinfo** function varies.</span></span>

> [!Note]  
> <span data-ttu-id="847cd-173">No código-fonte de produção, o aplicativo itera o conjunto de endereços retornados pela função [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) ou [**Getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) .</span><span class="sxs-lookup"><span data-stu-id="847cd-173">In production source code, your application would iterate through the set of addresses returned by the [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) or [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function.</span></span> <span data-ttu-id="847cd-174">Esses exemplos omitem essa etapa em favor da simplicidade.</span><span class="sxs-lookup"><span data-stu-id="847cd-174">These examples omit that step in favor of simplicity.</span></span>

 

<span data-ttu-id="847cd-175">Outro problema que você deve abordar ao modificar um aplicativo IPv4 existente para dar suporte ao IPv6 é associado à ordem em que as funções são chamadas.</span><span class="sxs-lookup"><span data-stu-id="847cd-175">Another issue you must address when modifying an existing IPv4 application to support IPv6 is associated with the order in which functions are called.</span></span> <span data-ttu-id="847cd-176">[**Getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) e [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) exigem que uma sequência de chamadas de função seja feita em uma ordem específica.</span><span class="sxs-lookup"><span data-stu-id="847cd-176">Both [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) and [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) require that a sequence of function calls are made in a specific order.</span></span>

<span data-ttu-id="847cd-177">Em plataformas nas quais o IPv4 e o IPv6 são usados, a família de endereços do nome do host remoto não é conhecida antecipadamente.</span><span class="sxs-lookup"><span data-stu-id="847cd-177">On platforms where both IPv4 and IPv6 are used, the address family of the remote host name is not known ahead of time.</span></span> <span data-ttu-id="847cd-178">Portanto, a resolução de endereço usando a função [**Getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) deve ser executada primeiro para determinar o endereço IP e a família de endereços do host remoto.</span><span class="sxs-lookup"><span data-stu-id="847cd-178">So address resolution using the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function must be executed first to determine the IP address and address family of the remote host.</span></span> <span data-ttu-id="847cd-179">Em seguida, a função [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) pode ser chamada para abrir um soquete da família de endereços retornada por [**Getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo).</span><span class="sxs-lookup"><span data-stu-id="847cd-179">Then the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function can be called to open a socket of the address family returned by [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo).</span></span> <span data-ttu-id="847cd-180">Essa é uma mudança importante na forma como os aplicativos do Windows Sockets são escritos, pois muitos aplicativos IPv4 tendem a usar uma ordem diferente de chamadas de função.</span><span class="sxs-lookup"><span data-stu-id="847cd-180">This is an important change in how Windows Sockets applications are written, since many IPv4 applications tend to use a different order of function calls.</span></span>

<span data-ttu-id="847cd-181">A maioria dos aplicativos IPv4 cria primeiro um soquete para a \_ família de endereços inet da série AF, depois a resolução de nomes e, em seguida, usa o soquete para se conectar ao endereço IP resolvido.</span><span class="sxs-lookup"><span data-stu-id="847cd-181">Most IPv4 applications first create a socket for the AF\_INET address family, then do name resolution, and then use the socket to connect to the resolved IP address.</span></span> <span data-ttu-id="847cd-182">Ao tornar esses aplicativos compatíveis com IPv6, a chamada de função de [**soquete**](/windows/desktop/api/Winsock2/nf-winsock2-socket) deve ser atrasada até após a resolução de nome quando a família de endereços for deteremined.</span><span class="sxs-lookup"><span data-stu-id="847cd-182">When making such applications IPv6-capable, the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function call must be delayed until after name resolution when the address family has been deteremined.</span></span> <span data-ttu-id="847cd-183">Observe que, se a resolução de nomes retornar endereços IPv4 e IPv6, os soquetes IPv4 e IPv6 separados deverão ser usados para se conectar a esses endereços de destino.</span><span class="sxs-lookup"><span data-stu-id="847cd-183">Note that if name resolution returns both IPv4 and IPv6 addresses, then separate IPv4 and IPv6 sockets must be used to connect to these destination addresses.</span></span> <span data-ttu-id="847cd-184">Todas essas complexidades podem ser evitadas usando a função [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) no Windows Vista e versões posteriores, para que os desenvolvedores de aplicativos sejam incentivados a usar essa nova função.</span><span class="sxs-lookup"><span data-stu-id="847cd-184">All of these complexities can be avoided by using the [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) function on Windows Vista and later, so application developers are encouraged to use this new function.</span></span>

<span data-ttu-id="847cd-185">O exemplo de código a seguir mostra a sequência apropriada para executar a resolução de nome primeiro (realizada na quarta linha no exemplo de código-fonte a seguir) e, em seguida, abrir um soquete (executado na<sup>linha 19 no</sup> exemplo de código a seguir).</span><span class="sxs-lookup"><span data-stu-id="847cd-185">The following code example shows the proper sequence for performing name resolution first (performed in the fourth line in the following source code example), then opening a socket (performed in the 19<sup>th</sup> line in the following code example).</span></span> <span data-ttu-id="847cd-186">Este exemplo é um trecho do arquivo client. c encontrado no código do [cliente habilitado para IPv6](ipv6-enabled-client-code-2.md) no apêndice B. A função de erro de suplemento chamada no exemplo de código a seguir está listada no exemplo de Client. c.</span><span class="sxs-lookup"><span data-stu-id="847cd-186">This example is an excerpt from the Client.c file found in the [IPv6-Enabled Client Code](ipv6-enabled-client-code-2.md) in Appendix B. The PrintError function called in the following code example is listed in the Client.c sample.</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

SOCKET OpenAndConnect(char *Server, char *PortName, int Family, int SocketType)
{

    int iResult = 0;
    SOCKET ConnSocket = INVALID_SOCKET;

    ADDRINFO *AddrInfo = NULL;
    ADDRINFO *AI = NULL;
    ADDRINFO Hints;

    char *AddrName = NULL;

    memset(&Hints, 0, sizeof (Hints));
    Hints.ai_family = Family;
    Hints.ai_socktype = SocketType;

    iResult = getaddrinfo(Server, PortName, &Hints, &AddrInfo);
    if (iResult != 0) {
        printf("Cannot resolve address [%s] and port [%s], error %d: %s\n",
               Server, PortName, WSAGetLastError(), gai_strerror(iResult));
        return INVALID_SOCKET;
    }
    //
    // Try each address getaddrinfo returned, until we find one to which
    // we can successfully connect.
    //
    for (AI = AddrInfo; AI != NULL; AI = AI->ai_next) {

        // Open a socket with the correct address family for this address.
        ConnSocket = socket(AI->ai_family, AI->ai_socktype, AI->ai_protocol);
        if (ConnSocket == INVALID_SOCKET) {
            printf("Error Opening socket, error %d\n", WSAGetLastError());
            continue;
        }
        //
        // Notice that nothing in this code is specific to whether we 
        // are using UDP or TCP.
        //
        // When connect() is called on a datagram socket, it does not 
        // actually establish the connection as a stream (TCP) socket
        // would. Instead, TCP/IP establishes the remote half of the
        // (LocalIPAddress, LocalPort, RemoteIP, RemotePort) mapping.
        // This enables us to use send() and recv() on datagram sockets,
        // instead of recvfrom() and sendto().
        //

        printf("Attempting to connect to: %s\n", Server ? Server : "localhost");
        if (connect(ConnSocket, AI->ai_addr, (int) AI->ai_addrlen) != SOCKET_ERROR)
            break;

        if (getnameinfo(AI->ai_addr, (socklen_t) AI->ai_addrlen, AddrName,
                        sizeof (AddrName), NULL, 0, NI_NUMERICHOST) != 0) {
            strcpy_s(AddrName, sizeof (AddrName), "<unknown>");
            printf("connect() to %s failed with error %d\n", AddrName, WSAGetLastError());
            closesocket(ConnSocket);
            ConnSocket = INVALID_SOCKET;
        }    
    }
    return ConnSocket;
}

```



## <a name="ip-helper-functions"></a><span data-ttu-id="847cd-187">Funções auxiliares de IP</span><span class="sxs-lookup"><span data-stu-id="847cd-187">IP Helper Functions</span></span>

<span data-ttu-id="847cd-188">Por fim, os aplicativos que usam a função auxiliar de IP [**GetAdaptersInfo**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersinfo)e suas [**informações de \_ adaptador \_ IP**](/windows/win32/api/iptypes/ns-iptypes-ip_adapter_info)de estrutura associadas, devem reconhecer que essa função e estrutura são limitadas a endereços IPv4.</span><span class="sxs-lookup"><span data-stu-id="847cd-188">Finally, applications making use of the IP Helper function [**GetAdaptersInfo**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersinfo), and its associated structure [**IP\_ADAPTER\_INFO**](/windows/win32/api/iptypes/ns-iptypes-ip_adapter_info), must recognize that both this function and structure are limited to IPv4 addresses.</span></span> <span data-ttu-id="847cd-189">As substituições habilitadas para IPv6 para essa função e estrutura são a função [**GetAdaptersAddresses**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) e a estrutura de [**\_ \_ endereços de adaptador IP**](/windows/win32/api/iptypes/ns-iptypes-ip_adapter_addresses_lh) .</span><span class="sxs-lookup"><span data-stu-id="847cd-189">IPv6-enabled replacements for this function and structure are the [**GetAdaptersAddresses**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) function and the [**IP\_ADAPTER\_ADDRESSES**](/windows/win32/api/iptypes/ns-iptypes-ip_adapter_addresses_lh) structure.</span></span> <span data-ttu-id="847cd-190">Os aplicativos habilitados para IPv6 que usam a API auxiliar de IP devem usar a função **GetAdaptersAddresses** e a estrutura de **\_ \_ endereços de adaptador IP** habilitada para IPv6 correspondente, ambas definidas no SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="847cd-190">IPv6-enabled applications making use of the IP Helper API should use the **GetAdaptersAddresses** function and the corresponding IPv6-enabled **IP\_ADAPTER\_ADDRESSES** structure, both defined in the Microsoft Windows Software Development Kit (SDK).</span></span>

## <a name="recommendations"></a><span data-ttu-id="847cd-191">Recomendações</span><span class="sxs-lookup"><span data-stu-id="847cd-191">Recommendations</span></span>

<span data-ttu-id="847cd-192">A melhor abordagem para garantir que seu aplicativo esteja usando chamadas de função compatíveis com IPv6 é usar a função [**Getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) para obter a conversão de host para endereço.</span><span class="sxs-lookup"><span data-stu-id="847cd-192">The best approach to ensure your application is using IPv6-compatible function calls is to use the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function for obtaining host-to-address translation.</span></span> <span data-ttu-id="847cd-193">A partir do Windows XP, a função **Getaddrinfo** torna a função [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) desnecessária e seu aplicativo deve, portanto, usar a função **Getaddrinfo** em vez de projetos de programação futuros.</span><span class="sxs-lookup"><span data-stu-id="847cd-193">Beginning with Windows XP, the **getaddrinfo** function makes the [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) function unnecessary, and your application should therefore use the **getaddrinfo** function instead for future programming projects.</span></span> <span data-ttu-id="847cd-194">Enquanto a Microsoft continuará a dar suporte a **gethostbyname**, essa função não será estendida para dar suporte a IPv6.</span><span class="sxs-lookup"><span data-stu-id="847cd-194">While Microsoft will continue to support **gethostbyname**, this function will not be extended to support IPv6.</span></span> <span data-ttu-id="847cd-195">Para obter suporte transparente para obter informações de host IPv6 e IPv4, você deve usar **Getaddrinfo**.</span><span class="sxs-lookup"><span data-stu-id="847cd-195">For transparent support for obtaining IPv6 and IPv4 host information, you must use **getaddrinfo**.</span></span>

<span data-ttu-id="847cd-196">O exemplo a seguir mostra como usar melhor a função **Getaddrinfo** .</span><span class="sxs-lookup"><span data-stu-id="847cd-196">The following example shows how to best use the **getaddrinfo** function.</span></span> <span data-ttu-id="847cd-197">Observe que a função, quando usada corretamente, como demonstra este exemplo, trata a conversão de host para endereço IPv6 e IPv4 corretamente, mas também obtém outras informações úteis sobre o host, como o tipo de soquetes com suporte.</span><span class="sxs-lookup"><span data-stu-id="847cd-197">Notice that the function, when used properly as this example demonstrates, handles both IPv6 and IPv4 host-to-address translation properly, but it also obtains other useful information about the host, such as the type of sockets supported.</span></span> <span data-ttu-id="847cd-198">Este exemplo é um trecho do exemplo de Client. c encontrado no apêndice B.</span><span class="sxs-lookup"><span data-stu-id="847cd-198">This sample is an excerpt from the Client.c sample found in Appendix B.</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

int ResolveName(char *Server, char *PortName, int Family, int SocketType)
{

    int iResult = 0;

    ADDRINFO *AddrInfo = NULL;
    ADDRINFO *AI = NULL;
    ADDRINFO Hints;

   //
    // By not setting the AI_PASSIVE flag in the hints to getaddrinfo, we're
    // indicating that we intend to use the resulting address(es) to connect
    // to a service.  This means that when the Server parameter is NULL,
    // getaddrinfo will return one entry per allowed protocol family
    // containing the loopback address for that family.
    //
    
    memset(&Hints, 0, sizeof(Hints));
    Hints.ai_family = Family;
    Hints.ai_socktype = SocketType;
    iResult = getaddrinfo(Server, PortName, &Hints, &AddrInfo);
    if (iResult != 0) {
        printf("Cannot resolve address [%s] and port [%s], error %d: %s\n",
               Server, PortName, WSAGetLastError(), gai_strerror(iResult));
        return SOCKET_ERROR;
    }
     return 0;
}
```



> [!Note]  
> <span data-ttu-id="847cd-199">A versão da função [**Getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) que dá suporte a IPv6 é nova para a versão Windows XP do Windows.</span><span class="sxs-lookup"><span data-stu-id="847cd-199">The version of the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function that supports IPv6 is new for the Windows XP release of Windows.</span></span>

 

<span data-ttu-id="847cd-200">Código a ser evitado</span><span class="sxs-lookup"><span data-stu-id="847cd-200">Code to Avoid</span></span>

<span data-ttu-id="847cd-201">A conversão de endereço de host tradicionalmente foi obtida usando a função [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) .</span><span class="sxs-lookup"><span data-stu-id="847cd-201">Host address translation has traditionally been achieved using the [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) function.</span></span> <span data-ttu-id="847cd-202">A partir do Windows XP:</span><span class="sxs-lookup"><span data-stu-id="847cd-202">Beginning with Windows XP:</span></span>

-   <span data-ttu-id="847cd-203">A função **Getaddrinfo** torna obsoleta a função **gethostbyname** .</span><span class="sxs-lookup"><span data-stu-id="847cd-203">The **getaddrinfo** function makes the **gethostbyname** function obsolete.</span></span>
-   <span data-ttu-id="847cd-204">Seus aplicativos devem usar a função **Getaddrinfo** em vez da função **gethostbyname** .</span><span class="sxs-lookup"><span data-stu-id="847cd-204">Your applications should use the **getaddrinfo** function instead of the **gethostbyname** function.</span></span>

<span data-ttu-id="847cd-205">Tarefas de codificação</span><span class="sxs-lookup"><span data-stu-id="847cd-205">Coding Tasks</span></span>

<span data-ttu-id="847cd-206">**Para modificar um aplicativo IPv4 existente para adicionar suporte para IPv6**</span><span class="sxs-lookup"><span data-stu-id="847cd-206">**To modify an existing IPv4 application to add support for IPv6**</span></span>

1.  <span data-ttu-id="847cd-207">Adquira o utilitário Checkv4.exe.</span><span class="sxs-lookup"><span data-stu-id="847cd-207">Acquire the Checkv4.exe utility.</span></span> <span data-ttu-id="847cd-208">Esse utilitário é instalado como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="847cd-208">This utility is installed as part of the Windows SDK.</span></span> <span data-ttu-id="847cd-209">O SDK do Windows está disponível por meio de uma assinatura do MSDN e também pode ser baixado do site da Microsoft ( https://msdn.microsoft.com) .</span><span class="sxs-lookup"><span data-stu-id="847cd-209">The Windows SDK is available through an MSDN subscription and can also be downloaded from the Microsoft website (https://msdn.microsoft.com).</span></span> <span data-ttu-id="847cd-210">Uma versão mais antiga da ferramenta de *Checkv4.exe* também foi incluída como parte do Microsoft IPv6 Technology Preview para Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="847cd-210">An older version of the *Checkv4.exe* tool was also as included as part of the Microsoft IPv6 Technology Preview for Windows 2000.</span></span>
2.  <span data-ttu-id="847cd-211">Execute o utilitário *Checkv4.exe* em relação ao seu código.</span><span class="sxs-lookup"><span data-stu-id="847cd-211">Run the *Checkv4.exe* utility against your code.</span></span> <span data-ttu-id="847cd-212">Consulte [usando o utilitário Checkv4.exe](using-the-checkv4-exe-utility-2.md) para saber mais sobre como executar o utilitário de versão em seus arquivos.</span><span class="sxs-lookup"><span data-stu-id="847cd-212">See [Using the Checkv4.exe Utility](using-the-checkv4-exe-utility-2.md) to learn about running the version utility against your files.</span></span>
3.  <span data-ttu-id="847cd-213">O utilitário alerta você sobre o uso de [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname), [**GetHostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)e outras funções somente IPv4 e fornece recomendações sobre como substituí-los pela função compatível com IPv6, como [**Getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) e [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo).</span><span class="sxs-lookup"><span data-stu-id="847cd-213">The utility alerts you to usage of the [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname), [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr), and other IPv4-only functions, and provides recommendations on how to replace them with the IPv6-compatible function such as [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) and [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo).</span></span>
4.  <span data-ttu-id="847cd-214">Substitua todas as instâncias da função **gethostbyname** e o código associado conforme apropriado, com a função **Getaddrinfo** .</span><span class="sxs-lookup"><span data-stu-id="847cd-214">Replace any instances of the **gethostbyname** function, and associated code as appropriate, with the **getaddrinfo** function.</span></span> <span data-ttu-id="847cd-215">No Windows Vista, use a função [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) ou [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) quando apropriado.</span><span class="sxs-lookup"><span data-stu-id="847cd-215">On Windows Vista, use the [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) or [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) function when appropriate.</span></span>
5.  <span data-ttu-id="847cd-216">Substitua todas as instâncias da função [**GetHostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) e o código associado conforme apropriado, com a função [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) .</span><span class="sxs-lookup"><span data-stu-id="847cd-216">Replace any instances of the [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) function, and associated code as appropriate, with the [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) function.</span></span>

<span data-ttu-id="847cd-217">Como alternativa, você pode pesquisar sua base de código para instâncias das funções **gethostbyname** e [**GetHostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) e alterar todo o uso (e outro código associado, conforme apropriado) para as funções **Getaddrinfo** e [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) .</span><span class="sxs-lookup"><span data-stu-id="847cd-217">Alternatively, you can search your code base for instances of the **gethostbyname** and [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) functions, and change all such usage (and other associated code, as appropriate) to the **getaddrinfo** and [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) functions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="847cd-218">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="847cd-218">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="847cd-219">Guia IPv6 para aplicativos do Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="847cd-219">IPv6 Guide for Windows Sockets Applications</span></span>](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="847cd-220">Alterando estruturas de dados para aplicativos Winsock do IPv6</span><span class="sxs-lookup"><span data-stu-id="847cd-220">Changing Data Structures for IPv6 Winsock Appications</span></span>](changing-data-structures-2.md)
</dt> <dt>

[<span data-ttu-id="847cd-221">Soquetes de pilha dupla para aplicativos Winsock do IPv6</span><span class="sxs-lookup"><span data-stu-id="847cd-221">Dual-Stack Sockets for IPv6 Winsock Applications</span></span>](dual-stack-sockets.md)
</dt> <dt>

[<span data-ttu-id="847cd-222">Uso de endereços IPv4 codificados</span><span class="sxs-lookup"><span data-stu-id="847cd-222">Use of Hardcoded IPv4 Addresses</span></span>](use-of-hardcoded-ipv4-addresses-2.md)
</dt> <dt>

[<span data-ttu-id="847cd-223">Problemas de interface do usuário para aplicativos Winsock do IPv6</span><span class="sxs-lookup"><span data-stu-id="847cd-223">User Interface Issues for IPv6 Winsock Applications</span></span>](user-interface-issues-2.md)
</dt> <dt>

[<span data-ttu-id="847cd-224">Protocolos subjacentes para aplicativos Winsock IPv6</span><span class="sxs-lookup"><span data-stu-id="847cd-224">Underlying Protocols for IPv6 Winsock Applications</span></span>](underlying-protocols-2.md)
</dt> </dl>

 

 
