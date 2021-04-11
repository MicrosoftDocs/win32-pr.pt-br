---
description: Depois que o cliente estiver concluindo o envio e o recebimento de dados, o cliente se desconecta do servidor e desliga o soquete.
ms.assetid: 33165e5b-e304-42b1-9542-45d8fe8a5218
title: Desconectando o cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c6ac34036cc92386d7d68b3d5debda4d37a92ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296355"
---
# <a name="disconnecting-the-client"></a><span data-ttu-id="c1413-103">Desconectando o cliente</span><span class="sxs-lookup"><span data-stu-id="c1413-103">Disconnecting the Client</span></span>

<span data-ttu-id="c1413-104">Depois que o cliente estiver concluindo o envio e o recebimento de dados, o cliente se desconecta do servidor e desliga o soquete.</span><span class="sxs-lookup"><span data-stu-id="c1413-104">Once the client is completed sending and receiving data, the client disconnects from the server and shutdowns the socket.</span></span>

<span data-ttu-id="c1413-105">**Para desconectar e desligar um soquete**</span><span class="sxs-lookup"><span data-stu-id="c1413-105">**To disconnect and shutdown a socket**</span></span>

1.  <span data-ttu-id="c1413-106">Quando o cliente é concluído enviando dados para o servidor, a função de [**desligamento**](/windows/desktop/api/winsock/nf-winsock-shutdown) pode ser chamada especificando \_ o envio SD para desligar o lado de envio do soquete.</span><span class="sxs-lookup"><span data-stu-id="c1413-106">When the client is done sending data to the server, the [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) function can be called specifying SD\_SEND to shutdown the sending side of the socket.</span></span> <span data-ttu-id="c1413-107">Isso permite que o servidor Libere alguns dos recursos para este Soquete.</span><span class="sxs-lookup"><span data-stu-id="c1413-107">This allows the server to release some of the resources for this socket.</span></span> <span data-ttu-id="c1413-108">O aplicativo cliente ainda pode receber dados no soquete.</span><span class="sxs-lookup"><span data-stu-id="c1413-108">The client application can still receive data on the socket.</span></span>
    ```C++
    // shutdown the send half of the connection since no more data will be sent
    iResult = shutdown(ConnectSocket, SD_SEND);
    if (iResult == SOCKET_ERROR) {
        printf("shutdown failed: %d\n", WSAGetLastError());
        closesocket(ConnectSocket);
        WSACleanup();
        return 1;
    }
    ```

    

2.  <span data-ttu-id="c1413-109">Quando o aplicativo cliente é terminado de receber dados, a função [**fechamento**](/windows/desktop/api/winsock/nf-winsock-closesocket) é chamada para fechar o soquete.</span><span class="sxs-lookup"><span data-stu-id="c1413-109">When the client application is done receiving data, the [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) function is called to close the socket.</span></span>

    <span data-ttu-id="c1413-110">Quando o aplicativo cliente é concluído usando a DLL do Windows Sockets, a função [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) é chamada para liberar recursos.</span><span class="sxs-lookup"><span data-stu-id="c1413-110">When the client application is completed using the Windows Sockets DLL, the [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) function is called to release resources.</span></span>

    ```C++
    // cleanup
    closesocket(ConnectSocket);
    WSACleanup();

    return 0;
    ```

    

## <a name="complete-client-source-code"></a><span data-ttu-id="c1413-111">Código-fonte completo do cliente</span><span class="sxs-lookup"><span data-stu-id="c1413-111">Complete Client Source Code</span></span>

-   [<span data-ttu-id="c1413-112">Código completo do cliente</span><span class="sxs-lookup"><span data-stu-id="c1413-112">Complete Client Code</span></span>](complete-client-code.md)

## <a name="related-topics"></a><span data-ttu-id="c1413-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c1413-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1413-114">Introdução com o Winsock</span><span class="sxs-lookup"><span data-stu-id="c1413-114">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="c1413-115">Aplicativo cliente Winsock</span><span class="sxs-lookup"><span data-stu-id="c1413-115">Winsock Client Application</span></span>](winsock-client-application.md)
</dt> <dt>

[<span data-ttu-id="c1413-116">Enviando e recebendo dados no cliente</span><span class="sxs-lookup"><span data-stu-id="c1413-116">Sending and Receiving Data on the Client</span></span>](sending-and-receiving-data-on-the-client.md)
</dt> </dl>

 

 



