---
description: O erro de soquete constante de manifesto \_ é fornecido para verificar a falha da função. Embora o uso dessa constante não seja obrigatório, é recomendável. O exemplo a seguir ilustra o uso da constante de erro de soquete \_ .
ms.assetid: b46203dc-5666-413b-90fe-8432318f3037
title: Valores de retorno em falha de função
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b94280d47d705833528c03c0d98a4a31232a0c6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165224"
---
# <a name="return-values-on-function-failure"></a><span data-ttu-id="c5262-105">Valores de retorno em falha de função</span><span class="sxs-lookup"><span data-stu-id="c5262-105">Return Values on Function Failure</span></span>

<span data-ttu-id="c5262-106">O erro de **soquete \_** constante de manifesto é fornecido para verificar a falha da função.</span><span class="sxs-lookup"><span data-stu-id="c5262-106">The manifest constant **SOCKET\_ERROR** is provided for checking function failure.</span></span> <span data-ttu-id="c5262-107">Embora o uso dessa constante não seja obrigatório, é recomendável.</span><span class="sxs-lookup"><span data-stu-id="c5262-107">Although use of this constant is not mandatory, it is recommended.</span></span> <span data-ttu-id="c5262-108">O exemplo a seguir ilustra o uso da constante de **\_ erro de soquete** .</span><span class="sxs-lookup"><span data-stu-id="c5262-108">The following example illustrates the use of the **SOCKET\_ERROR** constant.</span></span>

<span data-ttu-id="c5262-109">Estilo BSD típico (não funcionará no Windows)</span><span class="sxs-lookup"><span data-stu-id="c5262-109">Typical BSD Style (will not work on Windows)</span></span>


```C++
        r = recv(ClientSocket, recvbuf, recvbuflen, 0);
        if (r == -1     /* or r < 0 */
            && errno == EWOULDBLOCK) {
            printf("recv failed with error: EWOULDBLOCK\n");
        }    
```



<span data-ttu-id="c5262-110">Estilo do Windows</span><span class="sxs-lookup"><span data-stu-id="c5262-110">Windows Style</span></span>


```C++
        iResult = recv(ClientSocket, recvbuf, recvbuflen, 0);
        if (iResult == SOCKET_ERROR ) {
            iError = WSAGetLastError();
            if (iError == WSAEWOULDBLOCK)
                printf("recv failed with error: WSAEWOULDBLOCK\n");
            else
                printf("recv failed with error: %ld\n", iError);

            closesocket(ClientSocket);
            WSACleanup();
            return 1;
        }    
```



## <a name="related-topics"></a><span data-ttu-id="c5262-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c5262-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5262-112">Códigos de erro-errno, h \_ errno e WSAGetLastError</span><span class="sxs-lookup"><span data-stu-id="c5262-112">Error Codes - errno, h\_errno and WSAGetLastError</span></span>](error-codes-errno-h-errno-and-wsagetlasterror-2.md)
</dt> <dt>

[<span data-ttu-id="c5262-113">Manipulando erros do Winsock</span><span class="sxs-lookup"><span data-stu-id="c5262-113">Handling Winsock Errors</span></span>](handling-winsock-errors.md)
</dt> <dt>

[<span data-ttu-id="c5262-114">Portando aplicativos de soquete para Winsock</span><span class="sxs-lookup"><span data-stu-id="c5262-114">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="c5262-115">Considerações sobre programação do Winsock</span><span class="sxs-lookup"><span data-stu-id="c5262-115">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> <dt>

[<span data-ttu-id="c5262-116">Códigos de erro do Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="c5262-116">Windows Sockets Error Codes</span></span>](windows-sockets-error-codes-2.md)
</dt> </dl>

 

 



