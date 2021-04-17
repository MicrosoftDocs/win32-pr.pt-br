---
description: O código a seguir demonstra as funções recv e Send usadas pelo servidor.
ms.assetid: 26990b06-196a-4fb1-92d8-c5fa096d2b09
title: Recebendo e enviando dados no servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31ab20f074db750bef6459c6b9fcb5fd5636a522
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762435"
---
# <a name="receiving-and-sending-data-on-the-server"></a><span data-ttu-id="27971-103">Recebendo e enviando dados no servidor</span><span class="sxs-lookup"><span data-stu-id="27971-103">Receiving and Sending Data on the Server</span></span>

<span data-ttu-id="27971-104">O código a seguir demonstra as funções [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) e [**Send**](/windows/desktop/api/Winsock2/nf-winsock2-send) usadas pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="27971-104">The following code demonstrates the [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) and [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send) functions used by the server.</span></span>

### <a name="to-receive-and-send-data-on-a-socket"></a><span data-ttu-id="27971-105">Para receber e enviar dados em um soquete</span><span class="sxs-lookup"><span data-stu-id="27971-105">To receive and send data on a socket</span></span>


```C++
#define DEFAULT_BUFLEN 512

char recvbuf[DEFAULT_BUFLEN];
int iResult, iSendResult;
int recvbuflen = DEFAULT_BUFLEN;

// Receive until the peer shuts down the connection
do {

    iResult = recv(ClientSocket, recvbuf, recvbuflen, 0);
    if (iResult > 0) {
        printf("Bytes received: %d\n", iResult);

        // Echo the buffer back to the sender
        iSendResult = send(ClientSocket, recvbuf, iResult, 0);
        if (iSendResult == SOCKET_ERROR) {
            printf("send failed: %d\n", WSAGetLastError());
            closesocket(ClientSocket);
            WSACleanup();
            return 1;
        }
        printf("Bytes sent: %d\n", iSendResult);
    } else if (iResult == 0)
        printf("Connection closing...\n");
    else {
        printf("recv failed: %d\n", WSAGetLastError());
        closesocket(ClientSocket);
        WSACleanup();
        return 1;
    }

} while (iResult > 0);
```



<span data-ttu-id="27971-106">As funções [**Send**](/windows/desktop/api/Winsock2/nf-winsock2-send) e [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) retornam um valor inteiro do número de bytes enviados ou recebidos, respectivamente ou um erro.</span><span class="sxs-lookup"><span data-stu-id="27971-106">The [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send) and [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) functions both return an integer value of the number of bytes sent or received, respectively, or an error.</span></span> <span data-ttu-id="27971-107">Cada função também usa os mesmos parâmetros: o soquete ativo, um buffer de **caracteres** , o número de bytes a serem enviados ou recebidos e os sinalizadores a serem usados.</span><span class="sxs-lookup"><span data-stu-id="27971-107">Each function also takes the same parameters: the active socket, a **char** buffer, the number of bytes to send or receive, and any flags to use.</span></span>

<span data-ttu-id="27971-108">Próxima etapa: [desconectando o servidor](disconnecting-the-server.md)</span><span class="sxs-lookup"><span data-stu-id="27971-108">Next Step: [Disconnecting the Server](disconnecting-the-server.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="27971-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="27971-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27971-110">Introdução com o Winsock</span><span class="sxs-lookup"><span data-stu-id="27971-110">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="27971-111">Aplicativo de servidor Winsock</span><span class="sxs-lookup"><span data-stu-id="27971-111">Winsock Server Application</span></span>](winsock-server-application.md)
</dt> <dt>

[<span data-ttu-id="27971-112">Aceitando uma conexão</span><span class="sxs-lookup"><span data-stu-id="27971-112">Accepting a Connection</span></span>](accepting-a-connection.md)
</dt> </dl>

 

 



