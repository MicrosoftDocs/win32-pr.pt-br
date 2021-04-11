---
description: Após a inicialização, um objeto de soquete deve ser instanciado para ser usado pelo servidor.
ms.assetid: 2f3a7cab-3296-41ec-ac7e-224655b92a7c
title: Criando um soquete para o servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd3fb00cb8b1155f4d26d94c9a88328256effe23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090399"
---
# <a name="creating-a-socket-for-the-server"></a><span data-ttu-id="b0043-103">Criando um soquete para o servidor</span><span class="sxs-lookup"><span data-stu-id="b0043-103">Creating a Socket for the Server</span></span>

<span data-ttu-id="b0043-104">Após a inicialização, um objeto de **soquete** deve ser instanciado para ser usado pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="b0043-104">After initialization, a **SOCKET** object must be instantiated for use by the server.</span></span>

<span data-ttu-id="b0043-105">**Para criar um soquete para o servidor**</span><span class="sxs-lookup"><span data-stu-id="b0043-105">**To create a socket for the server**</span></span>

1.  <span data-ttu-id="b0043-106">A função [**Getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) é usada para determinar os valores na estrutura [**SOCKADDR**](sockaddr-2.md) :</span><span class="sxs-lookup"><span data-stu-id="b0043-106">The [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function is used to determine the values in the [**sockaddr**](sockaddr-2.md) structure:</span></span>

    -   <span data-ttu-id="b0043-107">**AF \_ O INET** é usado para especificar a família de endereços IPv4.</span><span class="sxs-lookup"><span data-stu-id="b0043-107">**AF\_INET** is used to specify the IPv4 address family.</span></span>
    -   <span data-ttu-id="b0043-108">**Sock \_ O fluxo** é usado para especificar um soquete de fluxo.</span><span class="sxs-lookup"><span data-stu-id="b0043-108">**SOCK\_STREAM** is used to specify a stream socket.</span></span>
    -   <span data-ttu-id="b0043-109">**IPPROTO \_ O TCP** é usado para especificar o protocolo TCP.</span><span class="sxs-lookup"><span data-stu-id="b0043-109">**IPPROTO\_TCP** is used to specify the TCP protocol .</span></span>
    -   <span data-ttu-id="b0043-110">**Ia \_ Sinalizador passivo** indica que o chamador pretende usar a estrutura de endereço de soquete retornada em uma chamada para a função de [**Associação**](/windows/desktop/api/winsock/nf-winsock-bind) .</span><span class="sxs-lookup"><span data-stu-id="b0043-110">**AI\_PASSIVE** flag indicates the caller intends to use the returned socket address structure in a call to the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function.</span></span> <span data-ttu-id="b0043-111">Quando o **sinalizador \_ passivo de ai** é definido e o parâmetro *NodeName* para a função [**Getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) é um ponteiro **NULL** , a parte de endereço IP da estrutura de endereço de soquete é definida como **inaddr \_** para endereços IPv4 ou **IN6ADDR \_ qualquer \_ init** para endereços IPv6.</span><span class="sxs-lookup"><span data-stu-id="b0043-111">When the **AI\_PASSIVE** flag is set and *nodename* parameter to the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function is a **NULL** pointer, the IP address portion of the socket address structure is set to **INADDR\_ANY** for IPv4 addresses or **IN6ADDR\_ANY\_INIT** for IPv6 addresses.</span></span>
    -   <span data-ttu-id="b0043-112">27015 é o número da porta associada ao servidor ao qual o cliente se conectará.</span><span class="sxs-lookup"><span data-stu-id="b0043-112">27015 is the port number associated with the server that the client will connect to.</span></span>

    <span data-ttu-id="b0043-113">A estrutura [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) é usada pela função [**Getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) .</span><span class="sxs-lookup"><span data-stu-id="b0043-113">The [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) structure is used by the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function.</span></span>

    ```C++
    #define DEFAULT_PORT "27015"

    struct addrinfo *result = NULL, *ptr = NULL, hints;

    ZeroMemory(&hints, sizeof (hints));
    hints.ai_family = AF_INET;
    hints.ai_socktype = SOCK_STREAM;
    hints.ai_protocol = IPPROTO_TCP;
    hints.ai_flags = AI_PASSIVE;

    // Resolve the local address and port to be used by the server
    iResult = getaddrinfo(NULL, DEFAULT_PORT, &hints, &result);
    if (iResult != 0) {
        printf("getaddrinfo failed: %d\n", iResult);
        WSACleanup();
        return 1;
    }
    ```

    

2.  <span data-ttu-id="b0043-114">Crie um objeto de **soquete** chamado ListenSocket para o servidor para escutar conexões de cliente.</span><span class="sxs-lookup"><span data-stu-id="b0043-114">Create a **SOCKET** object called ListenSocket for the server to listen for client connections.</span></span>
    ```C++
    SOCKET ListenSocket = INVALID_SOCKET;
    ```

    

3.  <span data-ttu-id="b0043-115">Chame a função [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) e retorne seu valor para a variável ListenSocket.</span><span class="sxs-lookup"><span data-stu-id="b0043-115">Call the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function and return its value to the ListenSocket variable.</span></span> <span data-ttu-id="b0043-116">Para este aplicativo de servidor, use o primeiro endereço IP retornado pela chamada para [**Getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) que correspondeu à família de endereços, ao tipo de soquete e ao protocolo especificado no parâmetro *Hints* .</span><span class="sxs-lookup"><span data-stu-id="b0043-116">For this server application, use the first IP address returned by the call to [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) that matched the address family, socket type, and protocol specified in the *hints* parameter.</span></span> <span data-ttu-id="b0043-117">Neste exemplo, um soquete de fluxo TCP para IPv4 foi solicitado com uma família de endereços IPv4, um tipo de soquete de \_ fluxo Sock e um protocolo de IPPROTO \_ TCP.</span><span class="sxs-lookup"><span data-stu-id="b0043-117">In this example, a TCP stream socket for IPv4 was requested with an address family of IPv4, a socket type of SOCK\_STREAM and a protocol of IPPROTO\_TCP.</span></span> <span data-ttu-id="b0043-118">Portanto, um endereço IPv4 é solicitado para o ListenSocket.</span><span class="sxs-lookup"><span data-stu-id="b0043-118">So an IPv4 address is requested for the ListenSocket.</span></span>

    <span data-ttu-id="b0043-119">Se o aplicativo de servidor quiser escutar no IPv6, a família de endereços precisará ser definida como AF \_ INET6 no parâmetro *Hints* .</span><span class="sxs-lookup"><span data-stu-id="b0043-119">If the server application wants to listen on IPv6, then the address family needs to be set to AF\_INET6 in the *hints* parameter.</span></span> <span data-ttu-id="b0043-120">Se um servidor quiser escutar no IPv6 e no IPv4, dois soquetes de escuta deverão ser criados, um para IPv6 e outro para IPv4.</span><span class="sxs-lookup"><span data-stu-id="b0043-120">If a server wants to listen on both IPv6 and IPv4, two listen sockets must be created, one for IPv6 and one for IPv4.</span></span> <span data-ttu-id="b0043-121">Esses dois soquetes devem ser tratados separadamente pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b0043-121">These two sockets must be handled separately by the application.</span></span>

    <span data-ttu-id="b0043-122">O Windows Vista e versões posteriores oferecem a capacidade de criar um único soquete IPv6 que é colocado no modo de pilha dual para escutar no IPv6 e no IPv4.</span><span class="sxs-lookup"><span data-stu-id="b0043-122">Windows Vista and later offer the ability to create a single IPv6 socket that is put in dual stack mode to listen on both IPv6 and IPv4.</span></span> <span data-ttu-id="b0043-123">Para obter mais informações sobre esse recurso, consulte [soquetes de pilha dupla](dual-stack-sockets.md).</span><span class="sxs-lookup"><span data-stu-id="b0043-123">For more information on this feature, see [Dual-Stack Sockets](dual-stack-sockets.md).</span></span>

    ```C++
    // Create a SOCKET for the server to listen for client connections

    ListenSocket = socket(result->ai_family, result->ai_socktype, result->ai_protocol);
    ```

    

4.  <span data-ttu-id="b0043-124">Verifique se há erros para garantir que o soquete é um soquete válido.</span><span class="sxs-lookup"><span data-stu-id="b0043-124">Check for errors to ensure that the socket is a valid socket.</span></span>
    ```C++
    if (ListenSocket == INVALID_SOCKET) {
        printf("Error at socket(): %ld\n", WSAGetLastError());
        freeaddrinfo(result);
        WSACleanup();
        return 1;
    }
    ```

    

<span data-ttu-id="b0043-125">Próxima etapa: [ligando um soquete](binding-a-socket.md)</span><span class="sxs-lookup"><span data-stu-id="b0043-125">Next Step: [Binding a Socket](binding-a-socket.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="b0043-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b0043-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0043-127">Introdução com o Winsock</span><span class="sxs-lookup"><span data-stu-id="b0043-127">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="b0043-128">Inicializando o Winsock</span><span class="sxs-lookup"><span data-stu-id="b0043-128">Initializing Winsock</span></span>](initializing-winsock.md)
</dt> <dt>

[<span data-ttu-id="b0043-129">Aplicativo de servidor Winsock</span><span class="sxs-lookup"><span data-stu-id="b0043-129">Winsock Server Application</span></span>](winsock-server-application.md)
</dt> </dl>

 

 
