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
# <a name="creating-a-socket-for-the-client"></a><span data-ttu-id="1ca0a-103">Criando um soquete para o cliente</span><span class="sxs-lookup"><span data-stu-id="1ca0a-103">Creating a socket for the client</span></span>

<span data-ttu-id="1ca0a-104">Após a inicialização, um objeto de **soquete** deve ser instanciado para ser usado pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="1ca0a-104">After initialization, a **SOCKET** object must be instantiated for use by the client.</span></span>

<span data-ttu-id="1ca0a-105">**Para criar um soquete**</span><span class="sxs-lookup"><span data-stu-id="1ca0a-105">**To create a socket**</span></span>

1.  <span data-ttu-id="1ca0a-106">Declare um objeto [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) que contenha uma estrutura [**SOCKADDR**](sockaddr-2.md) e inicialize esses valores.</span><span class="sxs-lookup"><span data-stu-id="1ca0a-106">Declare an [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) object that contains a [**sockaddr**](sockaddr-2.md) structure and initialize these values.</span></span> <span data-ttu-id="1ca0a-107">Para este aplicativo, a família de endereços da Internet não é especificada para que um endereço IPv6 ou IPv4 possa ser retornado.</span><span class="sxs-lookup"><span data-stu-id="1ca0a-107">For this application, the Internet address family is unspecified so that either an IPv6 or IPv4 address can be returned.</span></span> <span data-ttu-id="1ca0a-108">O aplicativo solicita que o tipo de soquete seja um soquete de fluxo para o protocolo TCP.</span><span class="sxs-lookup"><span data-stu-id="1ca0a-108">The application requests the socket type to be a stream socket for the TCP protocol.</span></span>
    ```C++
    struct addrinfo *result = NULL,
                    *ptr = NULL,
                    hints;

    ZeroMemory( &hints, sizeof(hints) );
    hints.ai_family = AF_UNSPEC;
    hints.ai_socktype = SOCK_STREAM;
    hints.ai_protocol = IPPROTO_TCP;
    ```

    

2.  <span data-ttu-id="1ca0a-109">Chame a função [**Getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) solicitando o endereço IP para o nome do servidor passado na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="1ca0a-109">Call the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function requesting the IP address for the server name passed on the command line.</span></span> <span data-ttu-id="1ca0a-110">A porta TCP no servidor ao qual o cliente se conectará é definida pela \_ porta padrão como 27015 neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="1ca0a-110">The TCP port on the server that the client will connect to is defined by DEFAULT\_PORT as 27015 in this sample.</span></span> <span data-ttu-id="1ca0a-111">A função **Getaddrinfo** retorna seu valor como um inteiro que é verificado quanto a erros.</span><span class="sxs-lookup"><span data-stu-id="1ca0a-111">The **getaddrinfo** function returns its value as an integer that is checked for errors.</span></span>
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

    

3.  <span data-ttu-id="1ca0a-112">Crie um objeto de **soquete** chamado ConnectSocket.</span><span class="sxs-lookup"><span data-stu-id="1ca0a-112">Create a **SOCKET** object called ConnectSocket.</span></span>
    ```C++
    SOCKET ConnectSocket = INVALID_SOCKET;
    ```

    

4.  <span data-ttu-id="1ca0a-113">Chame a função [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) e retorne seu valor para a variável ConnectSocket.</span><span class="sxs-lookup"><span data-stu-id="1ca0a-113">Call the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function and return its value to the ConnectSocket variable.</span></span> <span data-ttu-id="1ca0a-114">Para este aplicativo, use o primeiro endereço IP retornado pela chamada para [**Getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) que correspondeu à família de endereços, ao tipo de soquete e ao protocolo especificado no parâmetro *Hints* .</span><span class="sxs-lookup"><span data-stu-id="1ca0a-114">For this application, use the first IP address returned by the call to [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) that matched the address family, socket type, and protocol specified in the *hints* parameter.</span></span> <span data-ttu-id="1ca0a-115">Neste exemplo, um soquete de fluxo TCP foi especificado com um tipo de soquete de \_ fluxo Sock e um protocolo de IPPROTO \_ TCP.</span><span class="sxs-lookup"><span data-stu-id="1ca0a-115">In this example, a TCP stream socket was specified with a socket type of SOCK\_STREAM and a protocol of IPPROTO\_TCP.</span></span> <span data-ttu-id="1ca0a-116">A família de endereços deixou não especificada (AF \_ inspec), portanto, o endereço IP retornado pode ser um endereço IPv6 ou IPv4 para o servidor.</span><span class="sxs-lookup"><span data-stu-id="1ca0a-116">The address family was left unspecified (AF\_UNSPEC), so the returned IP address could be either an IPv6 or IPv4 address for the server.</span></span>

    <span data-ttu-id="1ca0a-117">Se o aplicativo cliente quiser se conectar usando apenas IPv6 ou IPv4, a família de endereços precisará ser definida como AF \_ INET6 para IPv6 ou o \_ inet de AF para IPv4 no parâmetro *Hints* .</span><span class="sxs-lookup"><span data-stu-id="1ca0a-117">If the client application wants to connect using only IPv6 or IPv4, then the address family needs to be set to AF\_INET6 for IPv6 or AF\_INET for IPv4 in the *hints* parameter.</span></span>

    ```C++
    // Attempt to connect to the first address returned by
    // the call to getaddrinfo
    ptr=result;

    // Create a SOCKET for connecting to server
    ConnectSocket = socket(ptr->ai_family, ptr->ai_socktype, 
        ptr->ai_protocol);
    ```

    

5.  <span data-ttu-id="1ca0a-118">Verifique se há erros para garantir que o soquete é um soquete válido.</span><span class="sxs-lookup"><span data-stu-id="1ca0a-118">Check for errors to ensure that the socket is a valid socket.</span></span>
    ```C++
    if (ConnectSocket == INVALID_SOCKET) {
        printf("Error at socket(): %ld\n", WSAGetLastError());
        freeaddrinfo(result);
        WSACleanup();
        return 1;
    }
    ```

    

<span data-ttu-id="1ca0a-119">Os parâmetros passados para a função [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) podem ser alterados para diferentes implementações.</span><span class="sxs-lookup"><span data-stu-id="1ca0a-119">The parameters passed to the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function can be changed for different implementations.</span></span>

<span data-ttu-id="1ca0a-120">A detecção de erros é uma parte importante do código de rede bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="1ca0a-120">Error detection is a key part of successful networking code.</span></span> <span data-ttu-id="1ca0a-121">Se a chamada de [**soquete**](/windows/desktop/api/Winsock2/nf-winsock2-socket) falhar, ela retornará um \_ soquete inválido.</span><span class="sxs-lookup"><span data-stu-id="1ca0a-121">If the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) call fails, it returns INVALID\_SOCKET.</span></span> <span data-ttu-id="1ca0a-122">A instrução **If** no código anterior é usada para capturar quaisquer erros que possam ter ocorrido durante a criação do soquete.</span><span class="sxs-lookup"><span data-stu-id="1ca0a-122">The **if** statement in the previous code is used to catch any errors that may have occurred while creating the socket.</span></span> <span data-ttu-id="1ca0a-123">[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retorna um número de erro associado ao último erro que ocorreu.</span><span class="sxs-lookup"><span data-stu-id="1ca0a-123">[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns an error number associated with the last error that occurred.</span></span>

> [!Note]  
> <span data-ttu-id="1ca0a-124">A verificação de erros mais abrangente pode ser necessária dependendo do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1ca0a-124">More extensive error checking may be necessary depending on the application.</span></span>
>
> <span data-ttu-id="1ca0a-125">Por exemplo, definir *hints.ai_family* como **AF_UNSPEC** pode fazer com que a chamada de conexão falhe.</span><span class="sxs-lookup"><span data-stu-id="1ca0a-125">For example, setting *hints.ai_family* to **AF_UNSPEC** can cause the connect call to fail.</span></span> <span data-ttu-id="1ca0a-126">Se isso acontecer, use um valor IPv4 (**AF_INET**) ou IPv6 (**AF_INET6**) específico.</span><span class="sxs-lookup"><span data-stu-id="1ca0a-126">If that happens, then use a specific IPv4 (**AF_INET**) or IPv6 (**AF_INET6**) value instead.</span></span>

<span data-ttu-id="1ca0a-127">[**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) é usado para encerrar o uso da DLL Ws2 \_ 32.</span><span class="sxs-lookup"><span data-stu-id="1ca0a-127">[**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) is used to terminate the use of the WS2\_32 DLL.</span></span>

<span data-ttu-id="1ca0a-128">Próxima etapa: [conectando-se a um soquete](connecting-to-a-socket.md)</span><span class="sxs-lookup"><span data-stu-id="1ca0a-128">Next Step: [Connecting to a Socket](connecting-to-a-socket.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="1ca0a-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1ca0a-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ca0a-130">Introdução com o Winsock</span><span class="sxs-lookup"><span data-stu-id="1ca0a-130">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="1ca0a-131">Inicializando o Winsock</span><span class="sxs-lookup"><span data-stu-id="1ca0a-131">Initializing Winsock</span></span>](initializing-winsock.md)
</dt> <dt>

[<span data-ttu-id="1ca0a-132">Aplicativo cliente Winsock</span><span class="sxs-lookup"><span data-stu-id="1ca0a-132">Winsock Client Application</span></span>](winsock-client-application.md)
</dt> </dl>

 

 
