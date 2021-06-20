---
title: O aplicativo de servidor
description: Veja a parte do aplicativo do servidor de um exemplo de RPC (chamada de procedimento remoto). O exemplo é do aplicativo "Olá, Mundo" no SDK da Plataforma.
ms.assetid: 82ccfd67-6626-49c4-8974-86ebc5841444
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34b8a2bb66fd415a9b8f778134edb4903f88a717
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406059"
---
# <a name="the-server-application"></a><span data-ttu-id="d9286-104">O aplicativo de servidor</span><span class="sxs-lookup"><span data-stu-id="d9286-104">The Server Application</span></span>

<span data-ttu-id="d9286-105">O exemplo a seguir é do aplicativo "Olá, Mundo" no diretório RPC Hello do SDK (Kit de Desenvolvimento de Software de \\ Plataforma).</span><span class="sxs-lookup"><span data-stu-id="d9286-105">The example below is from the 'Hello World' application in the RPC\\Hello directory of the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="d9286-106">O lado do servidor do aplicativo distribuído informa ao sistema que seus serviços estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="d9286-106">The server side of the distributed application informs the system that its services are available.</span></span> <span data-ttu-id="d9286-107">Em seguida, ele aguarda solicitações do cliente.</span><span class="sxs-lookup"><span data-stu-id="d9286-107">It then waits for client requests.</span></span> <span data-ttu-id="d9286-108">O compilador MIDL deve ser usado com o exemplo abaixo.</span><span class="sxs-lookup"><span data-stu-id="d9286-108">The MIDL compiler must be used with the example below.</span></span>

<span data-ttu-id="d9286-109">Dependendo do tamanho do aplicativo e das preferências de codificação, você pode optar por implementar procedimentos remotos em um ou mais arquivos separados.</span><span class="sxs-lookup"><span data-stu-id="d9286-109">Depending on the size of your application and your coding preferences, you can choose to implement remote procedures in one or more separate files.</span></span> <span data-ttu-id="d9286-110">Neste programa de tutorial, o arquivo de origem Hellos.c contém a rotina principal do servidor.</span><span class="sxs-lookup"><span data-stu-id="d9286-110">In this tutorial program, the source file Hellos.c contains the main server routine.</span></span> <span data-ttu-id="d9286-111">O arquivo Hellop.c contém o procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="d9286-111">The file Hellop.c contains the remote procedure.</span></span>

<span data-ttu-id="d9286-112">O benefício de organizar os procedimentos remotos em arquivos separados é que os procedimentos podem ser vinculados a um programa autônomo para depurar o código antes que ele seja convertido em um aplicativo distribuído.</span><span class="sxs-lookup"><span data-stu-id="d9286-112">The benefit of organizing the remote procedures in separate files is that the procedures can be linked with a standalone program to debug the code before it is converted to a distributed application.</span></span> <span data-ttu-id="d9286-113">Depois que os procedimentos funcionarem no programa autônomo, você poderá compilar e vincular os arquivos de origem que contêm os procedimentos remotos com o aplicativo de servidor.</span><span class="sxs-lookup"><span data-stu-id="d9286-113">After the procedures work in the standalone program, you can compile and link the source files containing the remote procedures with the server application.</span></span> <span data-ttu-id="d9286-114">Assim como no arquivo de origem do aplicativo cliente, o arquivo de origem do aplicativo de servidor deve incluir o arquivo de header Hello.h.</span><span class="sxs-lookup"><span data-stu-id="d9286-114">As with the client-application source file, the server-application source file must include the Hello.h header file.</span></span>

<span data-ttu-id="d9286-115">O servidor chama as funções de tempo de run time [**RPC RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep) e [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) para disponibilizar informações de associação ao cliente.</span><span class="sxs-lookup"><span data-stu-id="d9286-115">The server calls the RPC run-time functions [**RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep) and [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) to make binding information available to the client.</span></span> <span data-ttu-id="d9286-116">Este programa de exemplo passa o nome do alça de interface **para RpcServerRegisterIf.**</span><span class="sxs-lookup"><span data-stu-id="d9286-116">This example program passes the interface handle name to **RpcServerRegisterIf**.</span></span> <span data-ttu-id="d9286-117">Os outros parâmetros são definidos como **NULL.**</span><span class="sxs-lookup"><span data-stu-id="d9286-117">The other parameters are set to **NULL**.</span></span> <span data-ttu-id="d9286-118">Em seguida, o servidor chama a [**função RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) para indicar que está aguardando solicitações do cliente.</span><span class="sxs-lookup"><span data-stu-id="d9286-118">The server then calls the [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) function to indicate that it is waiting for client requests.</span></span>

<span data-ttu-id="d9286-119">O aplicativo de servidor também deve incluir as duas funções de gerenciamento de memória chamadas pelo stub do servidor: [**midl \_ user \_ allocate**](the-midl-user-allocate-function.md) e [**midl \_ user \_ free.**](the-midl-user-free-function.md)</span><span class="sxs-lookup"><span data-stu-id="d9286-119">The server application must also include the two memory management functions that the server stub calls: [**midl\_user\_allocate**](the-midl-user-allocate-function.md) and [**midl\_user\_free**](the-midl-user-free-function.md).</span></span> <span data-ttu-id="d9286-120">Essas funções alocam e liberam memória no servidor quando um procedimento remoto passa parâmetros para o servidor.</span><span class="sxs-lookup"><span data-stu-id="d9286-120">These functions allocate and free memory on the server when a remote procedure passes parameters to the server.</span></span> <span data-ttu-id="d9286-121">Neste programa de exemplo, **\_ \_ alocar** usuário médio e usuário **midl \_ \_** gratuito são simplesmente wrappers para as funções de biblioteca C [**malloc**](pointers-and-memory-allocation.md) e **free**.</span><span class="sxs-lookup"><span data-stu-id="d9286-121">In this example program, **midl\_user\_allocate** and **midl\_user\_free** are simply wrappers for the C-library functions [**malloc**](pointers-and-memory-allocation.md) and **free**.</span></span> <span data-ttu-id="d9286-122">(Observe que, nas declarações de encaminhamento geradas pelo compilador MIDL, "MIDL" está em letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="d9286-122">(Note that, in the MIDL compiler- generated forward declarations, "MIDL" is uppercase.</span></span> <span data-ttu-id="d9286-123">O arquivo de header Rpcndr.h define o usuário midl gratuito e o usuário médio alocado para ser usuário MIDL gratuito e alocar usuário \_ \_ \_ \_ \_ \_ \_ MIDL, \_ respectivamente.)</span><span class="sxs-lookup"><span data-stu-id="d9286-123">The header file Rpcndr.h defines midl\_user\_free and midl\_user\_allocate to be MIDL\_user\_free and MIDL\_user\_allocate, respectively.)</span></span>


```C++
/* file: hellos.c */
#include <stdlib.h>
#include <stdio.h>
#include <ctype.h>
#include "hello.h"
#include <windows.h>

void main()
{
    RPC_STATUS status;
    unsigned char * pszProtocolSequence = "ncacn_np";
    unsigned char * pszSecurity         = NULL; 
    unsigned char * pszEndpoint         = "\\pipe\\hello";
    unsigned int    cMinCalls = 1;
    unsigned int    fDontWait = FALSE;
 
    status = RpcServerUseProtseqEp(pszProtocolSequence,
                                   RPC_C_LISTEN_MAX_CALLS_DEFAULT,
                                   pszEndpoint,
                                   pszSecurity); 
 
    if (status) exit(status);
 
    status = RpcServerRegisterIf(hello_ServerIfHandle,  
                                 NULL,   
                                 NULL); 
 
    if (status) exit(status);
 
    status = RpcServerListen(cMinCalls,
                             RPC_C_LISTEN_MAX_CALLS_DEFAULT,
                             fDontWait);
 
    if (status) exit(status);
 }

/******************************************************/
/*         MIDL allocate and free                     */
/******************************************************/
 
void __RPC_FAR * __RPC_USER midl_user_allocate(size_t len)
{
    return(malloc(len));
}
 
void __RPC_USER midl_user_free(void __RPC_FAR * ptr)
{
    free(ptr);
}
```



 

 




