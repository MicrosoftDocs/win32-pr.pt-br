---
description: Após a inicialização, um objeto de soquete deve ser instanciado para ser usado pelo servidor.
ms.assetid: 2f3a7cab-3296-41ec-ac7e-224655b92a7c
title: Criando um soquete para o servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e71d6ee0117153b00a9ab77c53bd7555aa031b3fa9d1f7a425ea9aaf0e358f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118322196"
---
# <a name="creating-a-socket-for-the-server"></a>Criando um soquete para o servidor

Após a inicialização, um objeto de **soquete** deve ser instanciado para ser usado pelo servidor.

**Para criar um soquete para o servidor**

1.  A função [**Getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) é usada para determinar os valores na estrutura [**SOCKADDR**](sockaddr-2.md) :

    -   **AF \_ O INET** é usado para especificar a família de endereços IPv4.
    -   **Sock \_ O fluxo** é usado para especificar um soquete de fluxo.
    -   **IPPROTO \_ O TCP** é usado para especificar o protocolo TCP.
    -   **Ia \_ Sinalizador passivo** indica que o chamador pretende usar a estrutura de endereço de soquete retornada em uma chamada para a função de [**Associação**](/windows/desktop/api/winsock/nf-winsock-bind) . Quando o **sinalizador \_ passivo de ai** é definido e o parâmetro *NodeName* para a função [**Getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) é um ponteiro **NULL** , a parte de endereço IP da estrutura de endereço de soquete é definida como **inaddr \_** para endereços IPv4 ou **IN6ADDR \_ qualquer \_ init** para endereços IPv6.
    -   27015 é o número da porta associada ao servidor ao qual o cliente se conectará.

    A estrutura [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) é usada pela função [**Getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) .

    ```C++
    #define DEFAULT_PORT "27015"

    struct addrinfo *result = NULL, *ptr = NULL, hints;

    ZeroMemory(&hints, sizeof (hints));
    hints.ai_family = AF_INET;
    hints.ai_socktype = SOCK_STREAM;
    hints.ai_protocol = IPPROTO_TCP;
    hints.ai_flags = AI_PASSIVE;

    // Resolve the local address and port to be used by the server
    iResult = getaddrinfo(NULL, DEFAULT_PORT, &hints, &result);
    if (iResult != 0) {
        printf("getaddrinfo failed: %d\n", iResult);
        WSACleanup();
        return 1;
    }
    ```

    

2.  Crie um objeto de **soquete** chamado ListenSocket para o servidor para escutar conexões de cliente.
    ```C++
    SOCKET ListenSocket = INVALID_SOCKET;
    ```

    

3.  Chame a função [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) e retorne seu valor para a variável ListenSocket. Para este aplicativo de servidor, use o primeiro endereço IP retornado pela chamada para [**Getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) que correspondeu à família de endereços, ao tipo de soquete e ao protocolo especificado no parâmetro *Hints* . Neste exemplo, um soquete de fluxo TCP para IPv4 foi solicitado com uma família de endereços IPv4, um tipo de soquete de \_ fluxo Sock e um protocolo de IPPROTO \_ TCP. Portanto, um endereço IPv4 é solicitado para o ListenSocket.

    Se o aplicativo de servidor quiser escutar no IPv6, a família de endereços precisará ser definida como AF \_ INET6 no parâmetro *Hints* . Se um servidor quiser escutar no IPv6 e no IPv4, dois soquetes de escuta deverão ser criados, um para IPv6 e outro para IPv4. Esses dois soquetes devem ser tratados separadamente pelo aplicativo.

    Windows O Vista e versões posteriores oferecem a capacidade de criar um único soquete IPv6 que é colocado no modo de pilha dual para escutar no IPv6 e no IPv4. Para obter mais informações sobre esse recurso, consulte [soquetes de pilha dupla](dual-stack-sockets.md).

    ```C++
    // Create a SOCKET for the server to listen for client connections

    ListenSocket = socket(result->ai_family, result->ai_socktype, result->ai_protocol);
    ```

    

4.  Verifique se há erros para garantir que o soquete é um soquete válido.
    ```C++
    if (ListenSocket == INVALID_SOCKET) {
        printf("Error at socket(): %ld\n", WSAGetLastError());
        freeaddrinfo(result);
        WSACleanup();
        return 1;
    }
    ```

    

Próxima etapa: [ligando um soquete](binding-a-socket.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Introdução com o Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Inicializando o Winsock](initializing-winsock.md)
</dt> <dt>

[Aplicativo de servidor Winsock](winsock-server-application.md)
</dt> </dl>

 

 
