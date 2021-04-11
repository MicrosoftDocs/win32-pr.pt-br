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
# <a name="disconnecting-the-client"></a>Desconectando o cliente

Depois que o cliente estiver concluindo o envio e o recebimento de dados, o cliente se desconecta do servidor e desliga o soquete.

**Para desconectar e desligar um soquete**

1.  Quando o cliente é concluído enviando dados para o servidor, a função de [**desligamento**](/windows/desktop/api/winsock/nf-winsock-shutdown) pode ser chamada especificando \_ o envio SD para desligar o lado de envio do soquete. Isso permite que o servidor Libere alguns dos recursos para este Soquete. O aplicativo cliente ainda pode receber dados no soquete.
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

    

2.  Quando o aplicativo cliente é terminado de receber dados, a função [**fechamento**](/windows/desktop/api/winsock/nf-winsock-closesocket) é chamada para fechar o soquete.

    Quando o aplicativo cliente é concluído usando a DLL do Windows Sockets, a função [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) é chamada para liberar recursos.

    ```C++
    // cleanup
    closesocket(ConnectSocket);
    WSACleanup();

    return 0;
    ```

    

## <a name="complete-client-source-code"></a>Código-fonte completo do cliente

-   [Código completo do cliente](complete-client-code.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Introdução com o Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Aplicativo cliente Winsock](winsock-client-application.md)
</dt> <dt>

[Enviando e recebendo dados no cliente](sending-and-receiving-data-on-the-client.md)
</dt> </dl>

 

 



