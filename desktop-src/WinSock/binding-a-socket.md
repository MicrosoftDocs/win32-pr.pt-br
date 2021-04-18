---
description: Para que um servidor aceite conexões de cliente, ele deve estar associado a um endereço de rede dentro do sistema.
ms.assetid: d08fb1a5-af17-4116-8757-ba0a513fb323
title: Ligando um soquete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc71ad25837a070074fefa2e3693c5546839ec17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812276"
---
# <a name="binding-a-socket"></a><span data-ttu-id="f1d2c-103">Ligando um soquete</span><span class="sxs-lookup"><span data-stu-id="f1d2c-103">Binding a Socket</span></span>

<span data-ttu-id="f1d2c-104">Para que um servidor aceite conexões de cliente, ele deve estar associado a um endereço de rede dentro do sistema.</span><span class="sxs-lookup"><span data-stu-id="f1d2c-104">For a server to accept client connections, it must be bound to a network address within the system.</span></span> <span data-ttu-id="f1d2c-105">O código a seguir demonstra como associar um soquete que já foi criado a um endereço IP e a uma porta.</span><span class="sxs-lookup"><span data-stu-id="f1d2c-105">The following code demonstrates how to bind a socket that has already been created to an IP address and port.</span></span> <span data-ttu-id="f1d2c-106">Os aplicativos cliente usam o endereço IP e a porta para se conectar à rede do host.</span><span class="sxs-lookup"><span data-stu-id="f1d2c-106">Client applications use the IP address and port to connect to the host network.</span></span>

## <a name="to-bind-a-socket"></a><span data-ttu-id="f1d2c-107">Para associar um soquete</span><span class="sxs-lookup"><span data-stu-id="f1d2c-107">To bind a socket</span></span>

<span data-ttu-id="f1d2c-108">A estrutura [**SOCKADDR**](sockaddr-2.md) contém informações sobre a família de endereços, o endereço IP e o número da porta.</span><span class="sxs-lookup"><span data-stu-id="f1d2c-108">The [**sockaddr**](sockaddr-2.md) structure holds information regarding the address family, IP address, and port number.</span></span>

<span data-ttu-id="f1d2c-109">Chame a função [**BIND**](/windows/desktop/api/winsock/nf-winsock-bind) , passando o **soquete** criado e a estrutura [**SOCKADDR**](sockaddr-2.md) retornada da função [**Getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) como parâmetros.</span><span class="sxs-lookup"><span data-stu-id="f1d2c-109">Call the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function, passing the created **socket** and [**sockaddr**](sockaddr-2.md) structure returned from the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function as parameters.</span></span> <span data-ttu-id="f1d2c-110">Verifique se há erros gerais.</span><span class="sxs-lookup"><span data-stu-id="f1d2c-110">Check for general errors.</span></span>


```C++
    // Setup the TCP listening socket
    iResult = bind( ListenSocket, result->ai_addr, (int)result->ai_addrlen);
    if (iResult == SOCKET_ERROR) {
        printf("bind failed with error: %d\n", WSAGetLastError());
        freeaddrinfo(result);
        closesocket(ListenSocket);
        WSACleanup();
        return 1;
    }
```



<span data-ttu-id="f1d2c-111">Depois que a função [**BIND**](/windows/desktop/api/winsock/nf-winsock-bind) é chamada, as informações de endereço retornadas pela função [**Getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) não são mais necessárias.</span><span class="sxs-lookup"><span data-stu-id="f1d2c-111">Once the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function is called, the address information returned by the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function is no longer needed.</span></span> <span data-ttu-id="f1d2c-112">A função [**freeaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfo) é chamada para liberar a memória alocada pela função **Getaddrinfo** para essas informações de endereço.</span><span class="sxs-lookup"><span data-stu-id="f1d2c-112">The [**freeaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfo) function is called to free the memory allocated by the **getaddrinfo** function for this address information.</span></span>


```C++
    freeaddrinfo(result);

```



<span data-ttu-id="f1d2c-113">Próxima etapa: [ouvindo em um soquete](listening-on-a-socket.md)</span><span class="sxs-lookup"><span data-stu-id="f1d2c-113">Next Step: [Listening on a Socket](listening-on-a-socket.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="f1d2c-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f1d2c-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1d2c-115">Introdução com o Winsock</span><span class="sxs-lookup"><span data-stu-id="f1d2c-115">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="f1d2c-116">Aplicativo de servidor Winsock</span><span class="sxs-lookup"><span data-stu-id="f1d2c-116">Winsock Server Application</span></span>](winsock-server-application.md)
</dt> <dt>

[<span data-ttu-id="f1d2c-117">Criando um soquete para o servidor</span><span class="sxs-lookup"><span data-stu-id="f1d2c-117">Creating a Socket for the Server</span></span>](creating-a-socket-for-the-server.md)
</dt> </dl>

 

 



