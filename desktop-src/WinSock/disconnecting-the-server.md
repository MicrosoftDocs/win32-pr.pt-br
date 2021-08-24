---
description: Depois que o servidor for concluído, recebendo dados do cliente e enviando dados de volta para o cliente, o servidor desconectará do cliente e desligará o soquete.
ms.assetid: 67f33645-d57a-48bd-9f0c-9e816f528204
title: Desconectando o servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f644b8727898a9d77ab5aa5fb10b0a0ae5b58cdf88a3beb1b9642215d142b6b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898356"
---
# <a name="disconnecting-the-server"></a>Desconectando o servidor

Depois que o servidor for concluído, recebendo dados do cliente e enviando dados de volta para o cliente, o servidor desconectará do cliente e desligará o soquete.

**Para desconectar e desligar um soquete**

1.  Quando o servidor é concluído enviando dados para o cliente, a função de [**desligamento**](/windows/desktop/api/winsock/nf-winsock-shutdown) pode ser chamada especificando \_ o envio SD para desligar o lado de envio do soquete. Isso permite que o cliente Libere alguns dos recursos para este Soquete. O aplicativo de servidor ainda pode receber dados no soquete.
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

    

2.  Quando o aplicativo cliente é terminado de receber dados, a função [**fechamento**](/windows/desktop/api/winsock/nf-winsock-closesocket) é chamada para fechar o soquete.

    quando o aplicativo cliente é concluído usando a DLL Windows sockets, a função [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) é chamada para liberar recursos.

    ```C++
    // cleanup
    closesocket(ClientSocket);
    WSACleanup();

    return 0;
    ```

    

## <a name="complete-server-source-code"></a>Código-fonte completo do servidor

-   [Código de servidor completo](complete-server-code.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Introdução com o Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Aplicativo de servidor Winsock](winsock-server-application.md)
</dt> <dt>

[Recebendo e enviando dados no servidor](receiving-and-sending-data-on-the-server.md)
</dt> <dt>

[Executando o cliente Winsock e o exemplo de código do servidor](finished-server-and-client-code.md)
</dt> </dl>

 

 



