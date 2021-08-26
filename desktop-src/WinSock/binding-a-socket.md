---
description: Para que um servidor aceite conexões de cliente, ele deve estar associado a um endereço de rede dentro do sistema.
ms.assetid: d08fb1a5-af17-4116-8757-ba0a513fb323
title: Ligando um soquete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cda9e745395209228584ea5535864cca57e30494b2e30bfff02fe2abc527ed5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996907"
---
# <a name="binding-a-socket"></a>Ligando um soquete

Para que um servidor aceite conexões de cliente, ele deve estar associado a um endereço de rede dentro do sistema. O código a seguir demonstra como associar um soquete que já foi criado a um endereço IP e a uma porta. Os aplicativos cliente usam o endereço IP e a porta para se conectar à rede do host.

## <a name="to-bind-a-socket"></a>Para associar um soquete

A estrutura [**SOCKADDR**](sockaddr-2.md) contém informações sobre a família de endereços, o endereço IP e o número da porta.

Chame a função [**BIND**](/windows/desktop/api/winsock/nf-winsock-bind) , passando o **soquete** criado e a estrutura [**SOCKADDR**](sockaddr-2.md) retornada da função [**Getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) como parâmetros. Verifique se há erros gerais.


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



Depois que a função [**BIND**](/windows/desktop/api/winsock/nf-winsock-bind) é chamada, as informações de endereço retornadas pela função [**Getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) não são mais necessárias. A função [**freeaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfo) é chamada para liberar a memória alocada pela função **Getaddrinfo** para essas informações de endereço.


```C++
    freeaddrinfo(result);

```



Próxima etapa: [ouvindo em um soquete](listening-on-a-socket.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Introdução com o Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Aplicativo de servidor Winsock](winsock-server-application.md)
</dt> <dt>

[Criando um soquete para o servidor](creating-a-socket-for-the-server.md)
</dt> </dl>

 

 



