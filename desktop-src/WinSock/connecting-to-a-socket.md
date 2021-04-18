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
# <a name="connecting-to-a-socket"></a>Conectando a um soquete

Para que um cliente se comunique em uma rede, ele deve se conectar a um servidor.

## <a name="to-connect-to-a-socket"></a>Para se conectar a um soquete

Chame a função [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) , passando o soquete criado e a estrutura [**SOCKADDR**](sockaddr-2.md) como parâmetros. Verifique se há erros gerais.


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



A função [**Getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) é usada para determinar os valores na estrutura [**SOCKADDR**](sockaddr-2.md) . Neste exemplo, o primeiro endereço IP retornado pela função **Getaddrinfo** é usado para especificar a estrutura **SOCKADDR** passada para a [**conexão**](/windows/desktop/api/Winsock2/nf-winsock2-connect). Se a chamada de **conexão** falhar no primeiro endereço IP, tente a próxima estrutura [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) na lista vinculada retornada da função **Getaddrinfo** .

As informações especificadas na estrutura [**SOCKADDR**](sockaddr-2.md) incluem:

-   o endereço IP do servidor ao qual o cliente tentará se conectar.
-   o número da porta no servidor ao qual o cliente se conectará. Essa porta foi especificada como a porta 27015 quando o cliente chamou a função [**Getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) .

Próxima etapa: [Enviar e receber dados no cliente](sending-and-receiving-data-on-the-client.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Introdução com o Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Aplicativo cliente Winsock](winsock-client-application.md)
</dt> <dt>

[Criando um soquete para o cliente](creating-a-socket-for-the-client.md)
</dt> </dl>

 

 
