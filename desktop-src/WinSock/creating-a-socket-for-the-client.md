---
description: Após a inicialização, um objeto de soquete deve ser instanciado para ser usado pelo cliente.
ms.assetid: 088a79ef-b430-4860-8edc-902a1a03ed0d
title: Criando um soquete para o cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f64467406f13ed40bdbe134e7796dd2aa5ff7bee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827118"
---
# <a name="creating-a-socket-for-the-client"></a>Criando um soquete para o cliente

Após a inicialização, um objeto de **soquete** deve ser instanciado para ser usado pelo cliente.

**Para criar um soquete**

1.  Declare um objeto [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) que contenha uma estrutura [**SOCKADDR**](sockaddr-2.md) e inicialize esses valores. Para este aplicativo, a família de endereços da Internet não é especificada para que um endereço IPv6 ou IPv4 possa ser retornado. O aplicativo solicita que o tipo de soquete seja um soquete de fluxo para o protocolo TCP.
    ```C++
    struct addrinfo *result = NULL,
                    *ptr = NULL,
                    hints;

    ZeroMemory( &hints, sizeof(hints) );
    hints.ai_family = AF_UNSPEC;
    hints.ai_socktype = SOCK_STREAM;
    hints.ai_protocol = IPPROTO_TCP;
    ```

    

2.  Chame a função [**Getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) solicitando o endereço IP para o nome do servidor passado na linha de comando. A porta TCP no servidor ao qual o cliente se conectará é definida pela \_ porta padrão como 27015 neste exemplo. A função **Getaddrinfo** retorna seu valor como um inteiro que é verificado quanto a erros.
    ```C++
    #define DEFAULT_PORT "27015"

    // Resolve the server address and port
    iResult = getaddrinfo(argv[1], DEFAULT_PORT, &hints, &result);
    if (iResult != 0) {
        printf("getaddrinfo failed: %d\n", iResult);
        WSACleanup();
        return 1;
    }
    ```

    

3.  Crie um objeto de **soquete** chamado ConnectSocket.
    ```C++
    SOCKET ConnectSocket = INVALID_SOCKET;
    ```

    

4.  Chame a função [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) e retorne seu valor para a variável ConnectSocket. Para este aplicativo, use o primeiro endereço IP retornado pela chamada para [**Getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) que correspondeu à família de endereços, ao tipo de soquete e ao protocolo especificado no parâmetro *Hints* . Neste exemplo, um soquete de fluxo TCP foi especificado com um tipo de soquete de \_ fluxo Sock e um protocolo de IPPROTO \_ TCP. A família de endereços deixou não especificada (AF \_ inspec), portanto, o endereço IP retornado pode ser um endereço IPv6 ou IPv4 para o servidor.

    Se o aplicativo cliente quiser se conectar usando apenas IPv6 ou IPv4, a família de endereços precisará ser definida como AF \_ INET6 para IPv6 ou o \_ inet de AF para IPv4 no parâmetro *Hints* .

    ```C++
    // Attempt to connect to the first address returned by
    // the call to getaddrinfo
    ptr=result;

    // Create a SOCKET for connecting to server
    ConnectSocket = socket(ptr->ai_family, ptr->ai_socktype, 
        ptr->ai_protocol);
    ```

    

5.  Verifique se há erros para garantir que o soquete é um soquete válido.
    ```C++
    if (ConnectSocket == INVALID_SOCKET) {
        printf("Error at socket(): %ld\n", WSAGetLastError());
        freeaddrinfo(result);
        WSACleanup();
        return 1;
    }
    ```

    

Os parâmetros passados para a função [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) podem ser alterados para diferentes implementações.

A detecção de erros é uma parte importante do código de rede bem-sucedido. Se a chamada de [**soquete**](/windows/desktop/api/Winsock2/nf-winsock2-socket) falhar, ela retornará um \_ soquete inválido. A instrução **If** no código anterior é usada para capturar quaisquer erros que possam ter ocorrido durante a criação do soquete. [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retorna um número de erro associado ao último erro que ocorreu.

> [!Note]  
> A verificação de erros mais abrangente pode ser necessária dependendo do aplicativo.
>
> Por exemplo, definir *hints.ai_family* como **AF_UNSPEC** pode fazer com que a chamada de conexão falhe. Se isso acontecer, use um valor IPv4 (**AF_INET**) ou IPv6 (**AF_INET6**) específico.

[**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) é usado para encerrar o uso da DLL Ws2 \_ 32.

Próxima etapa: [conectando-se a um soquete](connecting-to-a-socket.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Introdução com o Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Inicializando o Winsock](initializing-winsock.md)
</dt> <dt>

[Aplicativo cliente Winsock](winsock-client-application.md)
</dt> </dl>

 

 
