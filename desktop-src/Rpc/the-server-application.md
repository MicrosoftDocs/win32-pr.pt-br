---
title: O aplicativo de servidor
description: O exemplo a seguir é do aplicativo ' Olá, Mundo ' no diretório RPC \\ Hello do SDK (Software Development Kit) da plataforma.
ms.assetid: 82ccfd67-6626-49c4-8974-86ebc5841444
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e6f13e2c8fecdcff820c62f3076dd2a8edd1a5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822658"
---
# <a name="the-server-application"></a><span data-ttu-id="edd3f-103">O aplicativo de servidor</span><span class="sxs-lookup"><span data-stu-id="edd3f-103">The Server Application</span></span>

<span data-ttu-id="edd3f-104">O exemplo a seguir é do aplicativo ' Olá, Mundo ' no diretório RPC \\ Hello do SDK (Software Development Kit) da plataforma.</span><span class="sxs-lookup"><span data-stu-id="edd3f-104">The example below is from the 'Hello World' application in the RPC\\Hello directory of the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="edd3f-105">O lado do servidor do aplicativo distribuído informa ao sistema que seus serviços estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="edd3f-105">The server side of the distributed application informs the system that its services are available.</span></span> <span data-ttu-id="edd3f-106">Em seguida, ele aguarda as solicitações do cliente.</span><span class="sxs-lookup"><span data-stu-id="edd3f-106">It then waits for client requests.</span></span> <span data-ttu-id="edd3f-107">O compilador MIDL deve ser usado com o exemplo abaixo.</span><span class="sxs-lookup"><span data-stu-id="edd3f-107">The MIDL compiler must be used with the example below.</span></span>

<span data-ttu-id="edd3f-108">Dependendo do tamanho do seu aplicativo e das suas preferências de codificação, você pode optar por implementar procedimentos remotos em um ou mais arquivos separados.</span><span class="sxs-lookup"><span data-stu-id="edd3f-108">Depending on the size of your application and your coding preferences, you can choose to implement remote procedures in one or more separate files.</span></span> <span data-ttu-id="edd3f-109">Neste programa tutorial, o arquivo de origem hellos. c contém a rotina de servidor principal.</span><span class="sxs-lookup"><span data-stu-id="edd3f-109">In this tutorial program, the source file Hellos.c contains the main server routine.</span></span> <span data-ttu-id="edd3f-110">O arquivo Hellop. c contém o procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="edd3f-110">The file Hellop.c contains the remote procedure.</span></span>

<span data-ttu-id="edd3f-111">O benefício de organizar os procedimentos remotos em arquivos separados é que os procedimentos podem ser vinculados a um programa autônomo para depurar o código antes que ele seja convertido em um aplicativo distribuído.</span><span class="sxs-lookup"><span data-stu-id="edd3f-111">The benefit of organizing the remote procedures in separate files is that the procedures can be linked with a standalone program to debug the code before it is converted to a distributed application.</span></span> <span data-ttu-id="edd3f-112">Depois que os procedimentos funcionam no programa autônomo, você pode compilar e vincular os arquivos de origem que contêm os procedimentos remotos com o aplicativo de servidor.</span><span class="sxs-lookup"><span data-stu-id="edd3f-112">After the procedures work in the standalone program, you can compile and link the source files containing the remote procedures with the server application.</span></span> <span data-ttu-id="edd3f-113">Assim como no arquivo de origem do aplicativo cliente, o arquivo de origem do aplicativo do servidor deve incluir o arquivo de cabeçalho Hello. h.</span><span class="sxs-lookup"><span data-stu-id="edd3f-113">As with the client-application source file, the server-application source file must include the Hello.h header file.</span></span>

<span data-ttu-id="edd3f-114">O servidor chama as funções de tempo de execução RPC [**RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep) e [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) para tornar as informações de associação disponíveis para o cliente.</span><span class="sxs-lookup"><span data-stu-id="edd3f-114">The server calls the RPC run-time functions [**RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep) and [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) to make binding information available to the client.</span></span> <span data-ttu-id="edd3f-115">Este programa de exemplo passa o nome do identificador de interface para **RpcServerRegisterIf**.</span><span class="sxs-lookup"><span data-stu-id="edd3f-115">This example program passes the interface handle name to **RpcServerRegisterIf**.</span></span> <span data-ttu-id="edd3f-116">Os outros parâmetros são definidos como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="edd3f-116">The other parameters are set to **NULL**.</span></span> <span data-ttu-id="edd3f-117">Em seguida, o servidor chama a função [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) para indicar que está aguardando as solicitações do cliente.</span><span class="sxs-lookup"><span data-stu-id="edd3f-117">The server then calls the [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) function to indicate that it is waiting for client requests.</span></span>

<span data-ttu-id="edd3f-118">O aplicativo de servidor também deve incluir as duas funções de gerenciamento de memória que o stub de servidor chama: [**\_ \_ alocar usuário**](the-midl-user-allocate-function.md) de MIDL e [**usuário de MIDL \_ \_ gratuito**](the-midl-user-free-function.md).</span><span class="sxs-lookup"><span data-stu-id="edd3f-118">The server application must also include the two memory management functions that the server stub calls: [**midl\_user\_allocate**](the-midl-user-allocate-function.md) and [**midl\_user\_free**](the-midl-user-free-function.md).</span></span> <span data-ttu-id="edd3f-119">Essas funções alocam e liberam memória no servidor quando um procedimento remoto passa parâmetros para o servidor.</span><span class="sxs-lookup"><span data-stu-id="edd3f-119">These functions allocate and free memory on the server when a remote procedure passes parameters to the server.</span></span> <span data-ttu-id="edd3f-120">Neste programa de exemplo, **o \_ usuário \_ de MIDL Allocate** e o **usuário de MIDL \_ \_ Free** são simplesmente invólucros para as funções [**malloc**](pointers-and-memory-allocation.md) e **Free** da biblioteca C.</span><span class="sxs-lookup"><span data-stu-id="edd3f-120">In this example program, **midl\_user\_allocate** and **midl\_user\_free** are simply wrappers for the C-library functions [**malloc**](pointers-and-memory-allocation.md) and **free**.</span></span> <span data-ttu-id="edd3f-121">(Observe que, nas declarações de encaminhamento geradas pelo compilador MIDL, "MIDL" é maiúsculo.</span><span class="sxs-lookup"><span data-stu-id="edd3f-121">(Note that, in the MIDL compiler- generated forward declarations, "MIDL" is uppercase.</span></span> <span data-ttu-id="edd3f-122">O arquivo de cabeçalho Rpcndr. h define o \_ usuário MIDL \_ gratuito e o \_ usuário de MIDL \_ alocar para ser o \_ usuário MIDL \_ gratuito e o \_ usuário MIDL \_ ALLOCATE, respectivamente.)</span><span class="sxs-lookup"><span data-stu-id="edd3f-122">The header file Rpcndr.h defines midl\_user\_free and midl\_user\_allocate to be MIDL\_user\_free and MIDL\_user\_allocate, respectively.)</span></span>


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



 

 




