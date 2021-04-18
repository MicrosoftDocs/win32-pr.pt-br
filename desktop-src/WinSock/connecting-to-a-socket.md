---
description: Para que um cliente se comunique em uma rede, ele deve se conectar a um servidor.
ms.assetid: fb52d2b7-70fa-497a-bbb4-42b25ea9d136
title: Conectando a um soquete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03aa4461e1b00ba073320529d03e3b0fe32cdae1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762411"
---
# <a name="connecting-to-a-socket"></a><span data-ttu-id="f2ff2-103">Conectando a um soquete</span><span class="sxs-lookup"><span data-stu-id="f2ff2-103">Connecting to a Socket</span></span>

<span data-ttu-id="f2ff2-104">Para que um cliente se comunique em uma rede, ele deve se conectar a um servidor.</span><span class="sxs-lookup"><span data-stu-id="f2ff2-104">For a client to communicate on a network, it must connect to a server.</span></span>

## <a name="to-connect-to-a-socket"></a><span data-ttu-id="f2ff2-105">Para se conectar a um soquete</span><span class="sxs-lookup"><span data-stu-id="f2ff2-105">To connect to a socket</span></span>

<span data-ttu-id="f2ff2-106">Chame a função [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) , passando o soquete criado e a estrutura [**SOCKADDR**](sockaddr-2.md) como parâmetros.</span><span class="sxs-lookup"><span data-stu-id="f2ff2-106">Call the [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) function, passing the created socket and the [**sockaddr**](sockaddr-2.md) structure as parameters.</span></span> <span data-ttu-id="f2ff2-107">Verifique se há erros gerais.</span><span class="sxs-lookup"><span data-stu-id="f2ff2-107">Check for general errors.</span></span>


```C++
// Connect to server.
iResult = connect( ConnectSocket, ptr->ai_addr, (int)ptr->ai_addrlen);
if (iResult == SOCKET_ERROR) {
    closesocket(ConnectSocket);
    ConnectSocket = INVALID_SOCKET;
}

// Should really try the next address returned by getaddrinfo
// if the connect call failed
// But for this simple example we just free the resources
// returned by getaddrinfo and print an error message

freeaddrinfo(result);

if (ConnectSocket == INVALID_SOCKET) {
    printf("Unable to connect to server!\n");
    WSACleanup();
    return 1;
}
```



<span data-ttu-id="f2ff2-108">A função [**Getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) é usada para determinar os valores na estrutura [**SOCKADDR**](sockaddr-2.md) .</span><span class="sxs-lookup"><span data-stu-id="f2ff2-108">The [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function is used to determine the values in the [**sockaddr**](sockaddr-2.md) structure.</span></span> <span data-ttu-id="f2ff2-109">Neste exemplo, o primeiro endereço IP retornado pela função **Getaddrinfo** é usado para especificar a estrutura **SOCKADDR** passada para a [**conexão**](/windows/desktop/api/Winsock2/nf-winsock2-connect).</span><span class="sxs-lookup"><span data-stu-id="f2ff2-109">In this example, the first IP address returned by the **getaddrinfo** function is used to specify the **sockaddr** structure passed to the [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect).</span></span> <span data-ttu-id="f2ff2-110">Se a chamada de **conexão** falhar no primeiro endereço IP, tente a próxima estrutura [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) na lista vinculada retornada da função **Getaddrinfo** .</span><span class="sxs-lookup"><span data-stu-id="f2ff2-110">If the **connect** call fails to the first IP address, then try the next [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) structure in the linked list returned from the **getaddrinfo** function.</span></span>

<span data-ttu-id="f2ff2-111">As informações especificadas na estrutura [**SOCKADDR**](sockaddr-2.md) incluem:</span><span class="sxs-lookup"><span data-stu-id="f2ff2-111">The information specified in the [**sockaddr**](sockaddr-2.md) structure includes:</span></span>

-   <span data-ttu-id="f2ff2-112">o endereço IP do servidor ao qual o cliente tentará se conectar.</span><span class="sxs-lookup"><span data-stu-id="f2ff2-112">the IP address of the server that the client will try to connect to.</span></span>
-   <span data-ttu-id="f2ff2-113">o número da porta no servidor ao qual o cliente se conectará.</span><span class="sxs-lookup"><span data-stu-id="f2ff2-113">the port number on the server that the client will connect to.</span></span> <span data-ttu-id="f2ff2-114">Essa porta foi especificada como a porta 27015 quando o cliente chamou a função [**Getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) .</span><span class="sxs-lookup"><span data-stu-id="f2ff2-114">This port was specified as port 27015 when the client called the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function.</span></span>

<span data-ttu-id="f2ff2-115">Próxima etapa: [Enviar e receber dados no cliente](sending-and-receiving-data-on-the-client.md)</span><span class="sxs-lookup"><span data-stu-id="f2ff2-115">Next Step: [Sending and Receiving Data on the Client](sending-and-receiving-data-on-the-client.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2ff2-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f2ff2-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2ff2-117">Introdução com o Winsock</span><span class="sxs-lookup"><span data-stu-id="f2ff2-117">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="f2ff2-118">Aplicativo cliente Winsock</span><span class="sxs-lookup"><span data-stu-id="f2ff2-118">Winsock Client Application</span></span>](winsock-client-application.md)
</dt> <dt>

[<span data-ttu-id="f2ff2-119">Criando um soquete para o cliente</span><span class="sxs-lookup"><span data-stu-id="f2ff2-119">Creating a Socket for the Client</span></span>](creating-a-socket-for-the-client.md)
</dt> </dl>

 

 
