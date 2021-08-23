---
description: novas funções foram introduzidas na interface Windows sockets especificamente projetadas para facilitar a programação Windows sockets. um dos benefícios dessas novas funções de soquetes de Windows é o suporte integrado para IPv6 e IPv4.
ms.assetid: 83262f2b-a335-4bbd-b2e3-6c7744b3ee50
title: Chamadas de função para aplicativos Winsock IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 241db1f7e07264fe4f0c776834d17c48cff4780b06e6a42816d36a50fa22cef7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051664"
---
# <a name="function-calls-for-ipv6-winsock-applications"></a>Chamadas de função para aplicativos Winsock IPv6

novas funções foram introduzidas na interface Windows sockets especificamente projetadas para facilitar a programação Windows sockets. um dos benefícios dessas novas funções de soquetes de Windows é o suporte integrado para IPv6 e IPv4.

essas novas funções de soquetes de Windows incluem o seguinte:

-   [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)
-   [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)
-   [**Getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) Family of Functions **(getaddrinfo**, [**GetAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa), [**GetAddrInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow), [**freeaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfo), [**FreeAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfoex), [**FreeAddrInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfow)e [**SetAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-setaddrinfoexa))
-   [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) Family of Functions (**getnameinfo** e [**GetNameInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfow))

além disso, novas funções auxiliares de IP com suporte para IPv6 e IPv4 foram adicionadas para simplificar a programação de Windows soquetes. Essas novas funções auxiliares de IP incluem o seguinte:

-   [**GetAdaptersAddresses**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses)

Ao adicionar suporte a IPv6 a um aplicativo, as seguintes diretrizes devem ser usadas:

-   Use [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) para estabelecer uma conexão com um ponto de extremidade, dado um nome de host e uma porta. a função **WSAConnectByName** está disponível no Windows Vista e posterior.
-   Use [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) para estabelecer uma conexão com uma de uma coleção de pontos de extremidade possíveis representados por um conjunto de endereços de destino (nomes de host e portas). a função **WSAConnectByList** está disponível no Windows Vista e posterior.
-   substitua as chamadas de função [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) por chamadas para uma das novas funções [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) Windows sockets. a função **getaddrinfo** com suporte para o protocolo IPv6 está disponível no Windows XP e versões posteriores. o protocolo ipv6 também tem suporte no Windows 2000 quando a versão prévia da tecnologia IPv6 para Windows 2000 está instalada.
-   substitua as chamadas de função [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) por chamadas para uma das novas funções de soquetes de [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) Windows. a função **getnameinfo** com suporte para o protocolo IPv6 está disponível no Windows XP e versões posteriores. o protocolo ipv6 também tem suporte no Windows 2000 quando a versão prévia da tecnologia IPv6 para Windows 2000 está instalada.

## <a name="wsaconnectbyname"></a>WSAConnectByName

A função [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) simplifica a conexão com um ponto de extremidade usando um soquete baseado em fluxo, dado o nome de host ou endereço IP do destino (IPv4 ou IPv6). Essa função reduz o código-fonte necessário para criar um aplicativo IP que é independente da versão do protocolo IP usado. O **WSAConnectByName** substitui as seguintes etapas em um aplicativo TCP típico para uma única chamada de função:

-   Resolva um nome de host para um conjunto de endereços IP.
-   Para cada endereço IP:
    -   Crie um soquete da família de endereços apropriada.
    -   Tentativas de conexão com o endereço IP remoto. Se a conexão foi bem-sucedida, ela retorna; caso contrário, será tentado o próximo endereço IP remoto para o host.

A função [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) vai além de apenas resolver o nome e, em seguida, tentar se conectar. A função usa todos os endereços remotos retornados pela resolução de nomes e todos os endereços IP de origem do computador local. Ele tenta primeiro se conectar usando pares de endereços com a maior chance de sucesso. Portanto, **WSAConnectByName** não apenas garante que uma conexão será estabelecida, se possível, mas também minimiza o tempo para estabelecer a conexão.

Para habilitar as comunicações IPv6 e IPv4, use o seguinte método:

-   A função [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) deve ser chamada em um soquete criado para a \_ família de endereços INET6 da AF para desabilitar a opção de soquete **IPv6 \_ V6ONLY** antes de chamar [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea). Isso é feito chamando a função **setsockopt** no soquete com o parâmetro *Level* definido como **IPPROTO \_ IPv6** (consulte Opções de [ \_ soquete IPPROTO IPv6](ipproto-ipv6-socket-options.md)), o parâmetro *OptName* definido como **IPv6 \_ V6ONLY** e o valor do parâmetro *optvalue* definido como zero.

Se um aplicativo precisar se associar a um endereço local ou a uma porta específica, [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) não poderá ser usado, pois o parâmetro Socket para **WSAConnectByName** deve ser um soquete não associado.

O exemplo de código a seguir mostra apenas algumas linhas de código que são necessárias para usar essa função para implementar um aplicativo que seja independente da versão de IP.

Estabelecer uma conexão usando o [ **WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

SOCKET OpenAndConnect(LPWSTR NodeName, LPWSTR PortName) 
{
    SOCKET ConnSocket;
    DWORD ipv6only = 0;
    int iResult;
    BOOL bSuccess;
    SOCKADDR_STORAGE LocalAddr = {0};
    SOCKADDR_STORAGE RemoteAddr = {0};
    DWORD dwLocalAddr = sizeof(LocalAddr);
    DWORD dwRemoteAddr = sizeof(RemoteAddr);
  
    ConnSocket = socket(AF_INET6, SOCK_STREAM, 0);
    if (ConnSocket == INVALID_SOCKET){
        return INVALID_SOCKET;
    }

    iResult = setsockopt(ConnSocket, IPPROTO_IPV6,
        IPV6_V6ONLY, (char*)&ipv6only, sizeof(ipv6only) );
    if (iResult == SOCKET_ERROR){
        closesocket(ConnSocket);
        return INVALID_SOCKET;       
    }

    bSuccess = WSAConnectByName(ConnSocket, NodeName, 
            PortName, &dwLocalAddr,
            (SOCKADDR*)&LocalAddr,
            &dwRemoteAddr,
            (SOCKADDR*)&RemoteAddr,
            NULL,
            NULL);
    if (bSuccess){
        return ConnSocket;
    } else {
        return INVALID_SOCKET;
    }
}
```



## <a name="wsaconnectbylist"></a>WSAConnectByList

A função [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) estabelece uma conexão com um host, dado um conjunto de hosts possíveis (representado por um conjunto de portas e endereços IP de destino). A função usa todos os endereços IP e portas para o ponto de extremidade e todos os endereços IP do computador local e tenta uma conexão usando todas as combinações de endereços possíveis.

[**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) está relacionado à função [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) . Em vez de usar um único nome de host, o **WSAConnectByList** aceita uma lista de hosts (endereços de destino e pares de porta) e se conecta a um dos endereços e portas na lista fornecida. Essa função foi projetada para dar suporte a cenários nos quais um aplicativo precisa se conectar a qualquer host disponível fora de uma lista de hosts potenciais.

Semelhante ao [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea), a função [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) reduz significativamente o código-fonte necessário para criar, ligar e conectar um soquete. Essa função facilita muito a implementação de um aplicativo que seja independente da versão do IP. A lista de endereços para um host aceito por essa função pode ser endereços IPv6 ou IPv4.

Para permitir que os endereços IPv6 e IPv4 sejam passados na lista de endereços única aceita pela função, as etapas a seguir devem ser executadas antes de chamar a função:

-   A função [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) deve ser chamada em um soquete criado para a \_ família de endereços INET6 da AF para desabilitar a opção de soquete **IPv6 \_ V6ONLY** antes de chamar [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist). Isso é feito chamando a função **setsockopt** no soquete com o parâmetro *Level* definido como **IPPROTO \_ IPv6** (consulte Opções de [ \_ soquete IPPROTO IPv6](ipproto-ipv6-socket-options.md)), o parâmetro *OptName* definido como **IPv6 \_ V6ONLY** e o valor do parâmetro *optvalue* definido como zero.
-   Todos os endereços IPv4 devem ser representados no formato de endereço IPv6 mapeado para IPv4, o que permite que um aplicativo somente IPv6 se comunique com um nó IPv4. O formato de endereço IPv6 mapeado para IPv4 permite que o endereço IPv4 de um nó IPv4 seja representado como um endereço IPv6. O endereço IPv4 é codificado em 32 bits de ordem inferior do endereço IPv6 e os bits 96 de ordem superior contêm o prefixo fixo 0:0: 0:0: 0: FFFF. O formato de endereço IPv6 mapeado para IPv4 é especificado no RFC 4291. Para obter mais informações, consulte [www.ietf.org/rfc/rfc4291.txt](https://tools.ietf.org/html/rfc4291). A \_ macro IN6ADDR SETV4MAPPED em *Mstcpip. h* pode ser usada para converter um endereço IPv4 para o formato de endereço IPv6 mapeado para IPv4 necessário.

Estabelecer uma conexão usando o [ **WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

SOCKET OpenAndConnect(SOCKET_ADDRESS_LIST *AddressList) 
{
    SOCKET ConnSocket;
    DWORD ipv6only = 0;
    int iResult;
    BOOL bSuccess;
    SOCKADDR_STORAGE LocalAddr = {0};
    SOCKADDR_STORAGE RemoteAddr = {0};
    DWORD dwLocalAddr = sizeof(LocalAddr);
    DWORD dwRemoteAddr = sizeof(RemoteAddr);

    ConnSocket = socket(AF_INET6, SOCK_STREAM, 0);
    if (ConnSocket == INVALID_SOCKET){
        return INVALID_SOCKET;
    }

    iResult = setsockopt(ConnSocket, IPPROTO_IPV6,
        IPV6_V6ONLY, (char*)&ipv6only, sizeof(ipv6only) );
    if (iResult == SOCKET_ERROR){
        closesocket(ConnSocket);
        return INVALID_SOCKET;       
    }

    // AddressList may contain IPv6 and/or IPv4Mapped addresses
    bSuccess = WSAConnectByList(ConnSocket,
            AddressList,
            &dwLocalAddr,
            (SOCKADDR*)&LocalAddr,
            &dwRemoteAddr,
            (SOCKADDR*)&RemoteAddr,
            NULL,
            NULL);
    if (bSuccess){
        return ConnSocket;
    } else {
        return INVALID_SOCKET;
    }
}
```



## <a name="getaddrinfo"></a>getaddrinfo

A função **Getaddrinfo** também executa o trabalho de processamento de muitas funções. anteriormente, as chamadas para um número de funções de soquetes de Windows eram necessárias para criar, abrir e associar um endereço a um soquete. Com a função **Getaddrinfo** , as linhas de código-fonte necessárias para executar esse trabalho podem ser significativamente reduzidas. Os dois exemplos a seguir ilustram o código-fonte necessário para executar essas tarefas com e sem a função **Getaddrinfo** .

executar uma Conexão, abrir e ligar usando o **getaddrinfo**


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

SOCKET OpenAndConnect(char *ServerName, char *PortName, int SocketType)
{
    SOCKET ConnSocket;
    ADDRINFO *AI;

    if (getaddrinfo(ServerName, PortName, NULL, &AI) != 0) {
        return INVALID_SOCKET;
    }

    ConnSocket = socket(AI->ai_family, SocketType, 0);
    if (ConnSocket == INVALID_SOCKET) {
        freeaddrinfo(AI);
        return INVALID_SOCKET;
    }

    if (connect(ConnSocket, AI->ai_addr, (int) AI->ai_addrlen) == SOCKET_ERROR) {
        closesocket(ConnSocket);
        freeaddrinfo(AI);
        return INVALID_SOCKET;
    }

    return ConnSocket;
}
```



executar uma Conexão, abrir e associar sem usar o **getaddrinfo**


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

SOCKET OpenAndConnect(char *ServerName, unsigned short Port, int SocketType) 
{
    SOCKET ConnSocket;
    LPHOSTENT hp;
    SOCKADDR_IN ServerAddr;
    
    ConnSocket = socket(AF_INET, SocketType, 0); /* Open a socket */
    if (ConnSocket < 0 ) {
        return INVALID_SOCKET;
    }

    memset(&ServerAddr, 0, sizeof(ServerAddr));
    ServerAddr.sin_family = AF_INET;
    ServerAddr.sin_port = htons(Port);

    if (isalpha(ServerName[0])) {   /* server address is a name */
        hp = gethostbyname(ServerName);
        if (hp == NULL) {
            return INVALID_SOCKET;
        }
        ServerAddr.sin_addr.s_addr = (ULONG) hp->h_addr;
    } else { /* Convert nnn.nnn address to a usable one */
        ServerAddr.sin_addr.s_addr = inet_addr(ServerName);
    } 

    if (connect(ConnSocket, (LPSOCKADDR)&ServerAddr, 
        sizeof(ServerAddr)) == SOCKET_ERROR)
    {
        closesocket(ConnSocket);
        return INVALID_SOCKET;
    }

    return ConnSocket;
}
```



Observe que ambos os exemplos de código-fonte executam as mesmas tarefas, mas o primeiro exemplo, usando a função **Getaddrinfo** , requer menos linhas de código-fonte e pode manipular endereços IPv6 ou IPv4. O número de linhas do código-fonte eliminado usando a função **Getaddrinfo** varia.

> [!Note]  
> No código-fonte de produção, o aplicativo itera o conjunto de endereços retornados pela função [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) ou [**Getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) . Esses exemplos omitem essa etapa em favor da simplicidade.

 

Outro problema que você deve abordar ao modificar um aplicativo IPv4 existente para dar suporte ao IPv6 é associado à ordem em que as funções são chamadas. [**Getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) e [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) exigem que uma sequência de chamadas de função seja feita em uma ordem específica.

Em plataformas nas quais o IPv4 e o IPv6 são usados, a família de endereços do nome do host remoto não é conhecida antecipadamente. Portanto, a resolução de endereço usando a função [**Getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) deve ser executada primeiro para determinar o endereço IP e a família de endereços do host remoto. Em seguida, a função [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) pode ser chamada para abrir um soquete da família de endereços retornada por [**Getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo). essa é uma mudança importante em como Windows aplicativos de soquetes são gravados, já que muitos aplicativos IPv4 tendem a usar uma ordem diferente de chamadas de função.

A maioria dos aplicativos IPv4 cria primeiro um soquete para a \_ família de endereços inet da série AF, depois a resolução de nomes e, em seguida, usa o soquete para se conectar ao endereço IP resolvido. Ao tornar esses aplicativos compatíveis com IPv6, a chamada de função de [**soquete**](/windows/desktop/api/Winsock2/nf-winsock2-socket) deve ser atrasada até após a resolução de nome quando a família de endereços for deteremined. Observe que, se a resolução de nomes retornar endereços IPv4 e IPv6, os soquetes IPv4 e IPv6 separados deverão ser usados para se conectar a esses endereços de destino. todas essas complexidades podem ser evitadas com o uso da função [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) no Windows Vista e posterior, para que os desenvolvedores de aplicativos sejam incentivados a usar essa nova função.

O exemplo de código a seguir mostra a sequência apropriada para executar a resolução de nome primeiro (realizada na quarta linha no exemplo de código-fonte a seguir) e, em seguida, abrir um soquete (executado na<sup>linha 19 no</sup> exemplo de código a seguir). Este exemplo é um trecho do arquivo client. c encontrado no código do [cliente habilitado para IPv6](ipv6-enabled-client-code-2.md) no apêndice B. A função de erro de suplemento chamada no exemplo de código a seguir está listada no exemplo de Client. c.


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

SOCKET OpenAndConnect(char *Server, char *PortName, int Family, int SocketType)
{

    int iResult = 0;
    SOCKET ConnSocket = INVALID_SOCKET;

    ADDRINFO *AddrInfo = NULL;
    ADDRINFO *AI = NULL;
    ADDRINFO Hints;

    char *AddrName = NULL;

    memset(&Hints, 0, sizeof (Hints));
    Hints.ai_family = Family;
    Hints.ai_socktype = SocketType;

    iResult = getaddrinfo(Server, PortName, &Hints, &AddrInfo);
    if (iResult != 0) {
        printf("Cannot resolve address [%s] and port [%s], error %d: %s\n",
               Server, PortName, WSAGetLastError(), gai_strerror(iResult));
        return INVALID_SOCKET;
    }
    //
    // Try each address getaddrinfo returned, until we find one to which
    // we can successfully connect.
    //
    for (AI = AddrInfo; AI != NULL; AI = AI->ai_next) {

        // Open a socket with the correct address family for this address.
        ConnSocket = socket(AI->ai_family, AI->ai_socktype, AI->ai_protocol);
        if (ConnSocket == INVALID_SOCKET) {
            printf("Error Opening socket, error %d\n", WSAGetLastError());
            continue;
        }
        //
        // Notice that nothing in this code is specific to whether we 
        // are using UDP or TCP.
        //
        // When connect() is called on a datagram socket, it does not 
        // actually establish the connection as a stream (TCP) socket
        // would. Instead, TCP/IP establishes the remote half of the
        // (LocalIPAddress, LocalPort, RemoteIP, RemotePort) mapping.
        // This enables us to use send() and recv() on datagram sockets,
        // instead of recvfrom() and sendto().
        //

        printf("Attempting to connect to: %s\n", Server ? Server : "localhost");
        if (connect(ConnSocket, AI->ai_addr, (int) AI->ai_addrlen) != SOCKET_ERROR)
            break;

        if (getnameinfo(AI->ai_addr, (socklen_t) AI->ai_addrlen, AddrName,
                        sizeof (AddrName), NULL, 0, NI_NUMERICHOST) != 0) {
            strcpy_s(AddrName, sizeof (AddrName), "<unknown>");
            printf("connect() to %s failed with error %d\n", AddrName, WSAGetLastError());
            closesocket(ConnSocket);
            ConnSocket = INVALID_SOCKET;
        }    
    }
    return ConnSocket;
}

```



## <a name="ip-helper-functions"></a>Funções auxiliares de IP

Por fim, os aplicativos que usam a função auxiliar de IP [**GetAdaptersInfo**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersinfo)e suas [**informações de \_ adaptador \_ IP**](/windows/win32/api/iptypes/ns-iptypes-ip_adapter_info)de estrutura associadas, devem reconhecer que essa função e estrutura são limitadas a endereços IPv4. As substituições habilitadas para IPv6 para essa função e estrutura são a função [**GetAdaptersAddresses**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) e a estrutura de [**\_ \_ endereços de adaptador IP**](/windows/win32/api/iptypes/ns-iptypes-ip_adapter_addresses_lh) . os aplicativos habilitados para ipv6 que usam a API auxiliar de IP devem usar a função **GetAdaptersAddresses** e a estrutura de **\_ \_ endereços de adaptador IP** habilitada para ipv6 correspondente, ambas definidas no SDK (Software Development Kit) do Microsoft Windows.

## <a name="recommendations"></a>Recomendações

A melhor abordagem para garantir que seu aplicativo esteja usando chamadas de função compatíveis com IPv6 é usar a função [**Getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) para obter a conversão de host para endereço. a partir do Windows XP, a função **getaddrinfo** torna a função [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) desnecessária e seu aplicativo deve, portanto, usar a função **getaddrinfo** em vez de projetos de programação futuros. Enquanto a Microsoft continuará a dar suporte a **gethostbyname**, essa função não será estendida para dar suporte a IPv6. Para obter suporte transparente para obter informações de host IPv6 e IPv4, você deve usar **Getaddrinfo**.

O exemplo a seguir mostra como usar melhor a função **Getaddrinfo** . Observe que a função, quando usada corretamente, como demonstra este exemplo, trata a conversão de host para endereço IPv6 e IPv4 corretamente, mas também obtém outras informações úteis sobre o host, como o tipo de soquetes com suporte. Este exemplo é um trecho do exemplo de Client. c encontrado no apêndice B.


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

int ResolveName(char *Server, char *PortName, int Family, int SocketType)
{

    int iResult = 0;

    ADDRINFO *AddrInfo = NULL;
    ADDRINFO *AI = NULL;
    ADDRINFO Hints;

   //
    // By not setting the AI_PASSIVE flag in the hints to getaddrinfo, we're
    // indicating that we intend to use the resulting address(es) to connect
    // to a service.  This means that when the Server parameter is NULL,
    // getaddrinfo will return one entry per allowed protocol family
    // containing the loopback address for that family.
    //
    
    memset(&Hints, 0, sizeof(Hints));
    Hints.ai_family = Family;
    Hints.ai_socktype = SocketType;
    iResult = getaddrinfo(Server, PortName, &Hints, &AddrInfo);
    if (iResult != 0) {
        printf("Cannot resolve address [%s] and port [%s], error %d: %s\n",
               Server, PortName, WSAGetLastError(), gai_strerror(iResult));
        return SOCKET_ERROR;
    }
     return 0;
}
```



> [!Note]  
> a versão da função [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) que dá suporte a IPv6 é nova para a versão Windows XP do Windows.

 

Código a ser evitado

A conversão de endereço de host tradicionalmente foi obtida usando a função [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) . a partir do Windows XP:

-   A função **Getaddrinfo** torna obsoleta a função **gethostbyname** .
-   Seus aplicativos devem usar a função **Getaddrinfo** em vez da função **gethostbyname** .

Tarefas de codificação

**Para modificar um aplicativo IPv4 existente para adicionar suporte para IPv6**

1.  Adquira o utilitário Checkv4.exe. esse utilitário é instalado como parte do SDK do Windows. o SDK do Windows está disponível por meio de uma assinatura do MSDN e também pode ser baixado do site da Microsoft ( https://msdn.microsoft.com) . uma versão mais antiga da ferramenta de *Checkv4.exe* também foi incluída como parte do Microsoft IPv6 Technology Preview para Windows 2000.
2.  Execute o utilitário *Checkv4.exe* em relação ao seu código. Consulte [usando o utilitário Checkv4.exe](using-the-checkv4-exe-utility-2.md) para saber mais sobre como executar o utilitário de versão em seus arquivos.
3.  O utilitário alerta você sobre o uso de [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname), [**GetHostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)e outras funções somente IPv4 e fornece recomendações sobre como substituí-los pela função compatível com IPv6, como [**Getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) e [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo).
4.  Substitua todas as instâncias da função **gethostbyname** e o código associado conforme apropriado, com a função **Getaddrinfo** . no Windows Vista, use a função [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) ou [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) quando apropriado.
5.  Substitua todas as instâncias da função [**GetHostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) e o código associado conforme apropriado, com a função [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) .

Como alternativa, você pode pesquisar sua base de código para instâncias das funções **gethostbyname** e [**GetHostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) e alterar todo o uso (e outro código associado, conforme apropriado) para as funções **Getaddrinfo** e [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[guia de IPv6 para aplicativos de Windows sockets](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[Alterando estruturas de dados para aplicativos Winsock do IPv6](changing-data-structures-2.md)
</dt> <dt>

[Soquetes de pilha dupla para aplicativos Winsock do IPv6](dual-stack-sockets.md)
</dt> <dt>

[Uso de endereços IPv4 codificados](use-of-hardcoded-ipv4-addresses-2.md)
</dt> <dt>

[Problemas de interface do usuário para aplicativos Winsock do IPv6](user-interface-issues-2.md)
</dt> <dt>

[Protocolos subjacentes para aplicativos Winsock IPv6](underlying-protocols-2.md)
</dt> </dl>

 

 
