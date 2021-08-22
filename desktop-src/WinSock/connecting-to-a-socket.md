---
description: Para que um cliente se comunique em uma rede, ele deve se conectar a um servidor.
ms.assetid: fb52d2b7-70fa-497a-bbb4-42b25ea9d136
title: Conectando-se a um soquete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59a5a81c18089bdf5f35e96aa55a8ede87dc88598a98acd3bc5ab8338afb1208
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132669"
---
# <a name="connecting-to-a-socket"></a>Conectando-se a um soquete

Para que um cliente se comunique em uma rede, ele deve se conectar a um servidor.

## <a name="to-connect-to-a-socket"></a>Para se conectar a um soquete

Chame a [**função connect,**](/windows/desktop/api/Winsock2/nf-winsock2-connect) passando o soquete criado e a [**estrutura sockaddr**](sockaddr-2.md) como parâmetros. Verifique se há erros gerais.


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



A [**função getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) é usada para determinar os valores na estrutura [**sockaddr.**](sockaddr-2.md) Neste exemplo, o primeiro endereço IP retornado pela **função getaddrinfo** é usado para especificar a estrutura **sockaddr** passada para [**a conexão**](/windows/desktop/api/Winsock2/nf-winsock2-connect). Se a **chamada** de conexão falhar para o primeiro endereço IP, tente a próxima estrutura [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) na lista vinculada retornada da **função getaddrinfo.**

As informações especificadas na estrutura [**sockaddr**](sockaddr-2.md) incluem:

-   o endereço IP do servidor ao que o cliente tentará se conectar.
-   o número da porta no servidor ao que o cliente se conectará. Essa porta foi especificada como a porta 27015 quando o cliente chamou a [**função getaddrinfo.**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)

Próxima etapa: [enviar e receber dados no cliente](sending-and-receiving-data-on-the-client.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Ponto de Partida com Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Aplicativo cliente Winsock](winsock-client-application.md)
</dt> <dt>

[Criando um soquete para o cliente](creating-a-socket-for-the-client.md)
</dt> </dl>

 

 
