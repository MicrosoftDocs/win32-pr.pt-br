---
description: Depois que o soquete estiver ouvindo uma conexão, o programa deverá lidar com as solicitações de conexão nesse soquete.
ms.assetid: d01f3d90-4d83-442e-aada-e7b082ef7699
title: Aceitando uma conexão (Windows Sockets 2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03e066b53c22dd9964ad44dc8d67c15969641362
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751997"
---
# <a name="accepting-a-connection-windows-sockets-2"></a><span data-ttu-id="54457-103">Aceitando uma conexão (Windows Sockets 2)</span><span class="sxs-lookup"><span data-stu-id="54457-103">Accepting a Connection (Windows Sockets 2)</span></span>

<span data-ttu-id="54457-104">Depois que o soquete estiver ouvindo uma conexão, o programa deverá lidar com as solicitações de conexão nesse soquete.</span><span class="sxs-lookup"><span data-stu-id="54457-104">Once the socket is listening for a connection, the program must handle connection requests on that socket.</span></span>

<span data-ttu-id="54457-105">**Para aceitar uma conexão em um soquete**</span><span class="sxs-lookup"><span data-stu-id="54457-105">**To accept a connection on a socket**</span></span>

1.  <span data-ttu-id="54457-106">Crie um objeto de **soquete** temporário chamado ClientSocket para aceitar conexões de clientes.</span><span class="sxs-lookup"><span data-stu-id="54457-106">Create a temporary **SOCKET** object called ClientSocket for accepting connections from clients.</span></span>
    ```C++
    
    SOCKET ClientSocket;

    
    ```

    

2.  <span data-ttu-id="54457-107">Normalmente, um aplicativo de servidor seria projetado para escutar conexões de vários clientes.</span><span class="sxs-lookup"><span data-stu-id="54457-107">Normally a server application would be designed to listen for connections from multiple clients.</span></span> <span data-ttu-id="54457-108">Para servidores de alto desempenho, vários threads são comumente usados para lidar com várias conexões de cliente.</span><span class="sxs-lookup"><span data-stu-id="54457-108">For high-performance servers, multiple threads are commonly used to handle the multiple client connections.</span></span>

    <span data-ttu-id="54457-109">Há várias técnicas de programação diferentes usando o Winsock que podem ser usadas para escutar várias conexões de cliente.</span><span class="sxs-lookup"><span data-stu-id="54457-109">There are several different programming techniques using Winsock that can be used to listen for multiple client connections.</span></span> <span data-ttu-id="54457-110">Uma técnica de programação é criar um loop contínuo que verifica as solicitações de conexão usando a função [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) (Confira [escuta em um soquete](listening-on-a-socket.md)).</span><span class="sxs-lookup"><span data-stu-id="54457-110">One programming technique is to create a continuous loop that checks for connection requests using the [**listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) function (see [Listening on a Socket](listening-on-a-socket.md)).</span></span> <span data-ttu-id="54457-111">Se ocorrer uma solicitação de conexão, o aplicativo chamará a função [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex)ou [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) e passará o trabalho para outro thread para lidar com a solicitação.</span><span class="sxs-lookup"><span data-stu-id="54457-111">If a connection request occurs, the application calls the [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex), or [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) function and passes the work to another thread to handle the request.</span></span> <span data-ttu-id="54457-112">Várias outras técnicas de programação são possíveis.</span><span class="sxs-lookup"><span data-stu-id="54457-112">Several other programming techniques are possible.</span></span>

    <span data-ttu-id="54457-113">Observe que esse exemplo básico é muito simples e não usa vários threads.</span><span class="sxs-lookup"><span data-stu-id="54457-113">Note that this basic example is very simple and does not use multiple threads.</span></span> <span data-ttu-id="54457-114">O exemplo também apenas ouve e aceita uma única conexão.</span><span class="sxs-lookup"><span data-stu-id="54457-114">The example also just listens for and accepts only a single connection.</span></span>

    ```C++
    
    ClientSocket = INVALID_SOCKET;

    // Accept a client socket
    ClientSocket = accept(ListenSocket, NULL, NULL);
    if (ClientSocket == INVALID_SOCKET) {
        printf("accept failed: %d\n", WSAGetLastError());
        closesocket(ListenSocket);
        WSACleanup();
        return 1;
    }
     
    
    ```

    

3.  <span data-ttu-id="54457-115">Quando a conexão do cliente tiver sido aceita, um aplicativo de servidor normalmente passaria o soquete de cliente aceito (a variável ClientSocket no código de exemplo acima) para um thread de trabalho ou uma porta de conclusão de e/s e continuaria aceitando conexões adicionais.</span><span class="sxs-lookup"><span data-stu-id="54457-115">When the client connection has been accepted, a server application would normally pass the accepted client socket (the ClientSocket variable in the above sample code) to a worker thread or an I/O completion port and continue accepting additional connections.</span></span> <span data-ttu-id="54457-116">Neste exemplo básico, o servidor continua para a próxima etapa.</span><span class="sxs-lookup"><span data-stu-id="54457-116">In this basic example, the server continues to the next step.</span></span>

    <span data-ttu-id="54457-117">Há uma série de outras técnicas de programação que podem ser usadas para escutar e aceitar várias conexões.</span><span class="sxs-lookup"><span data-stu-id="54457-117">There are a number of other programming techniques that can be used to listen for and accept multiple connections.</span></span> <span data-ttu-id="54457-118">Isso inclui o uso das funções [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) ou [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) .</span><span class="sxs-lookup"><span data-stu-id="54457-118">These include using the [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) functions.</span></span> <span data-ttu-id="54457-119">Exemplos de algumas dessas várias técnicas de programação são ilustrados nos [exemplos de Winsock avançados](getting-started-with-winsock.md) incluídos no SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="54457-119">Examples of some of these various programming techniques are illustrated in the [Advanced Winsock Samples](getting-started-with-winsock.md) included with the Microsoft Windows Software Development Kit (SDK).</span></span>

    > [!Note]  
    > <span data-ttu-id="54457-120">Em sistemas UNIX, uma técnica de programação comum para servidores era para um aplicativo escutar conexões.</span><span class="sxs-lookup"><span data-stu-id="54457-120">On Unix systems, a common programming technique for servers was for an application to listen for connections.</span></span> <span data-ttu-id="54457-121">Quando uma conexão foi aceita, o processo pai chamaria a função **Fork** para criar um novo processo filho para lidar com a conexão do cliente, herdando o soquete do pai.</span><span class="sxs-lookup"><span data-stu-id="54457-121">When a connection was accepted, the parent process would call the **fork** function to create a new child process to handle the client connection, inheriting the socket from the parent.</span></span> <span data-ttu-id="54457-122">Não há suporte para essa técnica de programação no Windows, pois não há suporte para a função **Fork** .</span><span class="sxs-lookup"><span data-stu-id="54457-122">This programming technique is not supported on Windows, since the **fork** function is not supported.</span></span> <span data-ttu-id="54457-123">Essa técnica também não é normalmente adequada para servidores de alto desempenho, pois os recursos necessários para criar um novo processo são muito maiores do que os necessários para um thread.</span><span class="sxs-lookup"><span data-stu-id="54457-123">This technique is also not usually suitable for high-performance servers, since the resources needed to create a new process are much greater than those needed for a thread.</span></span>

     

<span data-ttu-id="54457-124">Próxima etapa: [recebendo e enviando dados no servidor](receiving-and-sending-data-on-the-server.md)</span><span class="sxs-lookup"><span data-stu-id="54457-124">Next Step: [Receiving and Sending Data on the Server](receiving-and-sending-data-on-the-server.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="54457-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="54457-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54457-126">Introdução com o Winsock</span><span class="sxs-lookup"><span data-stu-id="54457-126">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="54457-127">Aplicativo de servidor Winsock</span><span class="sxs-lookup"><span data-stu-id="54457-127">Winsock Server Application</span></span>](winsock-server-application.md)
</dt> <dt>

[<span data-ttu-id="54457-128">Ouvindo em um soquete</span><span class="sxs-lookup"><span data-stu-id="54457-128">Listening on a Socket</span></span>](listening-on-a-socket.md)
</dt> </dl>

 

 
