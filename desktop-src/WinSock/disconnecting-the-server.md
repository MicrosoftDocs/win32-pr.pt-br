---
description: Depois que o servidor for concluído, recebendo dados do cliente e enviando dados de volta para o cliente, o servidor desconectará do cliente e desligará o soquete.
ms.assetid: 67f33645-d57a-48bd-9f0c-9e816f528204
title: Desconectando o servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6abf7754da39a891b3d29c69f6c835706debd36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827116"
---
# <a name="disconnecting-the-server"></a><span data-ttu-id="75f02-103">Desconectando o servidor</span><span class="sxs-lookup"><span data-stu-id="75f02-103">Disconnecting the Server</span></span>

<span data-ttu-id="75f02-104">Depois que o servidor for concluído, recebendo dados do cliente e enviando dados de volta para o cliente, o servidor desconectará do cliente e desligará o soquete.</span><span class="sxs-lookup"><span data-stu-id="75f02-104">Once the server is completed receiving data from the client and sending data back to the client, the server disconnects from the client and shutdowns the socket.</span></span>

<span data-ttu-id="75f02-105">**Para desconectar e desligar um soquete**</span><span class="sxs-lookup"><span data-stu-id="75f02-105">**To disconnect and shutdown a socket**</span></span>

1.  <span data-ttu-id="75f02-106">Quando o servidor é concluído enviando dados para o cliente, a função de [**desligamento**](/windows/desktop/api/winsock/nf-winsock-shutdown) pode ser chamada especificando \_ o envio SD para desligar o lado de envio do soquete.</span><span class="sxs-lookup"><span data-stu-id="75f02-106">When the server is done sending data to the client, the [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) function can be called specifying SD\_SEND to shutdown the sending side of the socket.</span></span> <span data-ttu-id="75f02-107">Isso permite que o cliente Libere alguns dos recursos para este Soquete.</span><span class="sxs-lookup"><span data-stu-id="75f02-107">This allows the client to release some of the resources for this socket.</span></span> <span data-ttu-id="75f02-108">O aplicativo de servidor ainda pode receber dados no soquete.</span><span class="sxs-lookup"><span data-stu-id="75f02-108">The server application can still receive data on the socket.</span></span>
    ```C++
    // shutdown the send half of the connection since no more data will be sent
    iResult = shutdown(ClientSocket, SD_SEND);
    if (iResult == SOCKET_ERROR) {
        printf("shutdown failed: %d\n", WSAGetLastError());
        closesocket(ClientSocket);
        WSACleanup();
        return 1;
    }
    ```

    

2.  <span data-ttu-id="75f02-109">Quando o aplicativo cliente é terminado de receber dados, a função [**fechamento**](/windows/desktop/api/winsock/nf-winsock-closesocket) é chamada para fechar o soquete.</span><span class="sxs-lookup"><span data-stu-id="75f02-109">When the client application is done receiving data, the [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) function is called to close the socket.</span></span>

    <span data-ttu-id="75f02-110">Quando o aplicativo cliente é concluído usando a DLL do Windows Sockets, a função [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) é chamada para liberar recursos.</span><span class="sxs-lookup"><span data-stu-id="75f02-110">When the client application is completed using the Windows Sockets DLL, the [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) function is called to release resources.</span></span>

    ```C++
    // cleanup
    closesocket(ClientSocket);
    WSACleanup();

    return 0;
    ```

    

## <a name="complete-server-source-code"></a><span data-ttu-id="75f02-111">Código-fonte completo do servidor</span><span class="sxs-lookup"><span data-stu-id="75f02-111">Complete Server Source Code</span></span>

-   [<span data-ttu-id="75f02-112">Código de servidor completo</span><span class="sxs-lookup"><span data-stu-id="75f02-112">Complete Server Code</span></span>](complete-server-code.md)

## <a name="related-topics"></a><span data-ttu-id="75f02-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="75f02-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75f02-114">Introdução com o Winsock</span><span class="sxs-lookup"><span data-stu-id="75f02-114">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="75f02-115">Aplicativo de servidor Winsock</span><span class="sxs-lookup"><span data-stu-id="75f02-115">Winsock Server Application</span></span>](winsock-server-application.md)
</dt> <dt>

[<span data-ttu-id="75f02-116">Recebendo e enviando dados no servidor</span><span class="sxs-lookup"><span data-stu-id="75f02-116">Receiving and Sending Data on the Server</span></span>](receiving-and-sending-data-on-the-server.md)
</dt> <dt>

[<span data-ttu-id="75f02-117">Executando o cliente Winsock e o exemplo de código do servidor</span><span class="sxs-lookup"><span data-stu-id="75f02-117">Running the Winsock Client and Server Code Sample</span></span>](finished-server-and-client-code.md)
</dt> </dl>

 

 



