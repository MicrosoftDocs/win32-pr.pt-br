---
description: Depois que o soquete estiver associado a um endereço IP e a uma porta no sistema, o servidor deverá escutar nesse endereço IP e na porta para solicitações de conexão de entrada.
ms.assetid: 83c9f0e7-2e6d-449b-8d97-3d13154112cd
title: Ouvindo em um soquete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48c36fe1718493d1b92ca52bb3c648ebd1aa5b0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781219"
---
# <a name="listening-on-a-socket"></a><span data-ttu-id="6979b-103">Ouvindo em um soquete</span><span class="sxs-lookup"><span data-stu-id="6979b-103">Listening on a Socket</span></span>

<span data-ttu-id="6979b-104">Depois que o soquete estiver associado a um endereço IP e a uma porta no sistema, o servidor deverá escutar nesse endereço IP e na porta para solicitações de conexão de entrada.</span><span class="sxs-lookup"><span data-stu-id="6979b-104">After the socket is bound to an IP address and port on the system, the server must then listen on that IP address and port for incoming connection requests.</span></span>

## <a name="to-listen-on-a-socket"></a><span data-ttu-id="6979b-105">Para escutar em um soquete</span><span class="sxs-lookup"><span data-stu-id="6979b-105">To listen on a socket</span></span>

<span data-ttu-id="6979b-106">Chame a função [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) , passando como parâmetros o soquete criado e um valor para a *pendência*, o comprimento máximo da fila de conexões pendentes a serem aceitas.</span><span class="sxs-lookup"><span data-stu-id="6979b-106">Call the [**listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) function, passing as parameters the created socket and a value for the *backlog*, maximum length of the queue of pending connections to accept.</span></span> <span data-ttu-id="6979b-107">Neste exemplo, o parâmetro *backlog* foi definido como **SOMAXCONN**.</span><span class="sxs-lookup"><span data-stu-id="6979b-107">In this example, the *backlog* parameter was set to **SOMAXCONN**.</span></span> <span data-ttu-id="6979b-108">Esse valor é uma constante especial que instrui o provedor Winsock para esse soquete para permitir um número máximo razoável de conexões pendentes na fila.</span><span class="sxs-lookup"><span data-stu-id="6979b-108">This value is a special constant that instructs the Winsock provider for this socket to allow a maximum reasonable number of pending connections in the queue.</span></span> <span data-ttu-id="6979b-109">Verifique o valor de retorno de erros gerais.</span><span class="sxs-lookup"><span data-stu-id="6979b-109">Check the return value for general errors.</span></span>


```C++
if ( listen( ListenSocket, SOMAXCONN ) == SOCKET_ERROR ) {
    printf( "Listen failed with error: %ld\n", WSAGetLastError() );
    closesocket(ListenSocket);
    WSACleanup();
    return 1;
}
```



<span data-ttu-id="6979b-110">Próxima etapa: [aceitando uma conexão](accepting-a-connection.md)</span><span class="sxs-lookup"><span data-stu-id="6979b-110">Next Step: [Accepting a Connection](accepting-a-connection.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="6979b-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6979b-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6979b-112">Introdução com o Winsock</span><span class="sxs-lookup"><span data-stu-id="6979b-112">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="6979b-113">Aplicativo de servidor Winsock</span><span class="sxs-lookup"><span data-stu-id="6979b-113">Winsock Server Application</span></span>](winsock-server-application.md)
</dt> <dt>

[<span data-ttu-id="6979b-114">Ligando um soquete</span><span class="sxs-lookup"><span data-stu-id="6979b-114">Binding a Socket</span></span>](binding-a-socket.md)
</dt> </dl>

 

 



